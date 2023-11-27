## (Processo automatizado no deploy)

## Prometheus:
- O Prometheus é um sistema de monitoramento e alerta de código aberto projetado para coletar e processar métricas de sistemas distribuídos. Ele é comumente usado em ambientes de servidores Linux para monitorar o desempenho e a saúde de sistemas, aplicativos e serviços.

## Grafana: 

- O Grafana é uma plataforma de visualização e análise de dados de código aberto comumente utilizada em servidores Linux. Ele é projetado para integrar-se a diversas fontes de dados, incluindo sistemas de monitoramento como o Prometheus, bancos de dados, APIs e muito mais. O Grafana oferece recursos poderosos de criação de dashboards e gráficos interativos para facilitar o acompanhamento e a compreensão de dados em ambientes complexos.

## Node exporter:

- O Node Exporter é uma ferramenta específica para coletar métricas do sistema em servidores Linux. Ele funciona extraindo informações detalhadas sobre o hardware, o sistema operacional e outros recursos da máquina, tornando essas métricas disponíveis para sistemas de monitoramento, como o Prometheus.

__________________________________________________________________________________________________________________________________________

>  Acessar a maquina AWS
-> Clonar o repositório da equipe

# Como funciona 

Criando Usuários e Diretório do Sistema para o Prometheus (Teremos que criar um usuário do sistema chamado Prometheus e um diretório Prometheus com o mesmo nome)
```
sudo useradd --no-create-home --shell /bin/false prometheus  
sudo useradd --no-create-home --shell /bin/false node_exporter
sudo mkdir /etc/prometheus
sudo mkdir /var/lib/prometheus
```
**Atualização do Usuário Prometheus** 

Como grupos de usuários e diretórios foram criados com sucesso para armazenar os dados e arquivos do Prometheus.
Agora, precisaremos atualizar a propriedade do grupo e do usuário nos diretórios recém-criados. Ao utilizar o comando abaixo, realizamos a atualização da propriedade:

```
sudo chown prometheus:prometheus /etc/prometheus
sudo chown prometheus:prometheus /var/lib/prometheus
```
**Baixando o pacote de dados binário**

 cd /opt/
wget https://github.com/prometheus/prometheus/releases/download/v2.26.0/prometheus-2.26.0.linux-amd64.tar.gz

**Instalar Prometheus e Grafana no Ubuntu**

> sha256sum prometheus-2.26.0.linux-amd64.tar.gz
f1f2eeabbf7822572dce67565dc96ffaa2dd1897dd1d844562552b11123f151a prometheus-2.26.0.linux-amd64.tar.gz
tar -xvf prometheus-2.26.0.linux-amd64.tar.gz
cd prometheus-2.26.0.linux-amd64
ls

**Copiando os arquivos binários do Prometheus**

```
sudo cp /opt/prometheus-2.26.0.linux-amd64/prometheus /usr/local/bin/
sudo cp /opt/prometheus-2.26.0.linux-amd64/promtool /usr/local/bin/
```
**Permissão para o Prometheus nos binários**

```
sudo chown prometheus:prometheus /usr/local/bin/prometheus
sudo chown prometheus:prometheus /usr/local/bin/promtool
```

**Copiando a biblioteca de console do Prometheus**

```
sudo cp -r /opt/prometheus-2.26.0.linux-amd64/consoles /etc/prometheus
sudo cp -r /opt/prometheus-2.26.0.linux-amd64/console_libraries /etc/prometheus
sudo cp -r /opt/prometheus-2.26.0.linux-amd64/prometheus.yml /etc/prometheus
```


**Permissão para o Prometheus nos diretórios**
```
sudo chown -R prometheus:prometheus /etc/prometheus/consoles
sudo chown -R prometheus:prometheus /etc/prometheus/console_libraries
```

**Checkar a versão do Prometheus**

```
prometheus --version
promtool --version
```
**Arquivo de configuração do Prometheus**

- cat /etc/prometheus/prometheus.yml

- apertar I para mudar para o modo insert e colar

## my global config
global:
  scrape_interval: 15s # Set the scrape interval to every 15 seconds. Default is every 1 minute.
  evaluation_interval: 15s # Evaluate rules every 15 seconds. The default is every 1 minute.
**scrape_timeout is set to the global default (10s).**

## Alertmanager configuration
alerting:
  alertmanagers:
  - static_configs:
    - targets:
        - alertmanager:9093

**Load rules once and periodically evaluate them according to the global 'evaluation_interval**
rule_files:
   - "first_rules.yml"
   - "second_rules.yml"

**A scrape configuration containing exactly one endpoint to scrape:**
** Here it's Prometheus itself.**
scrape_configs:

**The job name is added as a label `job=<job_name>` to any timeseries scraped from this config.**
- job_name: 'prometheus'
- metrics_path defaults to '/metrics'
- scheme defaults to 'http'.

  static_configs:
  - targets: ['localhost:9090']

Salve com :wq!

**Criando o arquivo Prometheus Systemd**
```
sudo -u prometheus /usr/local/bin/prometheus \
        --config.file /etc/prometheus/prometheus.yml \
        --storage.tsdb.path /var/lib/prometheus/ \
        --web.console.templates=/etc/prometheus/consoles \
        --web.console.libraries=/etc/prometheus/console_libraries
```     
```
sudo nano /etc/systemd/system/prometheus.service
```
**Entre no modo insert novamente e cole**

> [Unit]
Description=Prometheus
Wants=network-online.target
After=network-online.target

> [Service]
User=prometheus
Group=prometheus
Type=simple
ExecStart=/usr/local/bin/prometheus \
    --config.file /etc/prometheus/prometheus.yml \
    --storage.tsdb.path /var/lib/prometheus/ \
    --web.console.templates=/etc/prometheus/consoles \
    --web.console.libraries=/etc/prometheus/console_libraries

**Instalação** 

> [Install]
WantedBy=multi-user.target

> Salve com :wq!

> sudo systemctl daemon-reload

> sudo systemctl start prometheus

> sudo systemctl enable prometheus


**Acessando Prometheus**

 - sudo ufw allow 9090/tcp

__coloque no browser: http://server-IP-or-Hostname:9090.__


**Instalando Grafana**
```
> wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add –

__echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list__

> sudo apt-get update

> sudo apt-get install grafana

> sudo systemctl start grafana-server

> sudo systemctl status grafana-server

> sudo systemctl enable grafana-server.service
```

__-> Para acessar o painel do Grafana, abra o seu navegador favorito, digite o endereço IP ou o nome do servidor seguido da porta padrão do Grafana, que é 3000.__

__Username – admin__

__Password – admin__

**-> Troque a senha**

## Configure o Prometheus com o DataSource do Grafana

__-> Add Data sources e selecione Prometheus__

**-> Agora, configure a fonte de dados do Prometheus fornecendo a URL do Prometheus.**


## Instale o Node exporter

wget https://github.com/prometheus/node_exporter/releases/download/v1.2.0/node_exporter-1.2.0.linux-amd64.tar.gz

> sudo tar xvzf node_exporter-1.2.0.linux-amd64.tar.gz

> cd node_exporter-1.2.0.linux-amd64

> sudo cp node_exporter /usr/local/bin


## Criando Node Exporter Systemd service

> cd /lib/systemd/system

> sudo nano node_exporter.service

__-> cole entrando no modo insert novamente__

>[Unit]
Description=Node Exporter
Wants=network-online.target
After=network-online.target
[Service]
Type=simple
User=node_exporter
Group=node_exporter
ExecStart=/usr/local/bin/node_exporter \
— collector.mountstats \
— collector.logind \
— collector.processes \
— collector.ntp \
— collector.systemd \
— collector.tcpstat \
— collector.wifi
Restart=always
RestartSec=10s
[Install]
WantedBy=multi-user.target

__-> Salve o que foi feito__

 > sudo systemctl daemon-reload

 > sudo systemctl enable node_exporter

 > sudo systemctl start node_exporter

 > sudo systemctl status node_exporter
	
## Configure o Node Exporter como o Prometheus target

__cd /etc/prometheus__

> sudo nano prometheus.yml

__-> Coloque o seguinte comando__

 > targets: [‘localhost:9090’, ‘localhost:9100’]

> -> Salve  e resete o Serviço do Prometheus
 sudo systemctl restart prometheus

-> Coloque a URL no navegador

https://localhost:9100/targets


## Criando Painel do Grafana para Monitorar Servidor Linux
> clique no icone de dashboard e selecione a opção import

> Providencie o ID 14513 no import via grafana.com e depois clique em Load

> Coloque o nome e clique em import

> Após os passos, Suas dashboards estarão no ar!


## PROMETHEUS

**COMO RODAR:**
```
cd /etc/prometheus
sudo systemctl start prometheus
sudo systemctl status prometheus
```
**-> caso nao iniciar**
```
sudo systemctl daemon-reload
sudo systemctl start prometheus
sudo systemctl enable prometheus
```
----------------------------------------
COMO PARAR:
```
sudo systemctl stop prometheus
sudo systemctl status prometheus
```
__

## GRAFANA
**COMO RODAR:**
```
cd /etc/grafana
sudo systemctl start grafana-server
sudo systemctl status grafana-server
```
----------------------------------------
**COMO PARAR:**
```
sudo systemctl stop grafana-server
sudo systemctl status grafana-server
```

__

## Node_Exporter

**COMO RODAR:**
```
sudo systemctl start node_exporter
sudo systemctl status node_exporter
```
----------------------------------------
**COMO PARAR:**
```
sudo systemctl stop node_exporter
sudo systemctl status node_exporter
```

__

**COMO VISUALIZAR AS DASHBOARDS:**

dashboard-> http://34.193.65.107:3000/d/rYdddlPWkjbbnkn/api-dashboards?orgId=1&refresh=1m&from=1700259605195&to=1700346005195

outros links:
prometheus
http://34.193.65.107:9090/targets
http://34.193.65.107:9100/targets
---------------------------------------
Grafana login
admin
api123

http://34.193.65.107:3000/










