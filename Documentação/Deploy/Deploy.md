# Explicação do deploy <a id="deployment"></a>

## O que é Deployment?

 De forma simples, Deployment é basicamente a "colocação em prática" de um novo software ou de uma atualização. É quando o que foi construído pelos desenvolvedores passa a estar disponível para as pessoas usarem. Imagine como a inauguração de uma loja, onde após construir o prédio (escrever o código), a inauguração (deployment) é o momento em que a loja abre suas portas para os clientes (usuários finais), mantendo-a aberta para os produtos oferecidos serem usados.
 Esse processo envolve várias etapas, como testar se tudo funciona bem, organizar o ambiente para receber o software (como organizar uma loja antes da inauguração), e finalmente, tornar o software acessível para as pessoas. O objetivo é garantir que o software novo ou uma nova versão(atualização) funcione corretamente e esteja pronto para ser usado por quem precisa, seja um aplicativo no seu telefone ou um site na internet.

## Qual o objetivo do DevOps de deploy?

O objetivo específico do DevOps no contexto do deployment é otimizar e aprimorar o processo de colocar uma aplicação ou atualização de software em um ambiente operacional. Isso inclui todas as etapas desde a preparação do código até a disponibilização para os usuários finais.

## Pontos principais:

Entrega Rápida e Contínua:
- Garantir que as novas funcionalidades e atualizações sejam entregues de maneira rápida, contínua e confiável, reduzindo os tempos de espera entre o desenvolvimento e a disponibilidade para os usuários.

Automatização Eficiente:
- Automatizar o máximo possível do processo de deployment para reduzir erros humanos, garantir consistência e aumentar a eficiência operacional.

Feedback Imediato:
- Implementar práticas que proporcionem feedback imediato sobre o desempenho do software após o deploy, permitindo ajustes rápidos e melhorias contínuas.

Minimização de Downtime:
- Reduzir ou eliminar o tempo de inatividade durante o deployment, assegurando que a aplicação esteja sempre disponível para os usuários.

Garantia de Qualidade:
- Integrar testes automatizados e práticas de garantia de qualidade no processo de deployment para garantir que o software entregue seja confiável e atenda aos requisitos esperados.

## Requisitos do projeto

 Conversando com o cliente, foi levantado que o projeto deveria ser desenvolvido para o sistema Linux, os requisitos para a máquina de produção levantados foram:

- Memória (RAM): 32 GB
- Armazenamento: 40 GB
- Número Máximo de Usuários Simultâneos: 100
- Utilização Máxima da CPU: Até 60%
- Uso de RDS(Relational Database Service) para backup automático ou manual, e snapshot de banco de dados.
- Criação de AMIs (Amazon Machine Images) para Rollback.
- Mínimo de testes unitários e de integração

 Foi-se então realizado a configuração global no servidor, como a instalação do Node para executar os projetos e do TypeScript para compilar de TypeScript para JavaScript.
 Posteriormente, foram criadas duas pastas para onde os backends do projeto seriam levantados: "Backend" e "BackendReceptor". Cada uma dessas pastas contém duas subpastas, "main", que consiste no servidor do produto final, e "develop", que consiste no servidor de produção.

- **Backend**
  - **main**
    - [ambiente de produção]
  - **develop**
    - [ambiente de desenvolvimento]
- **BackendReceptor**
  - **main**
    - [ambiente de produção]
  - **develop**
    - [ambiente de desenvolvimento]

 Após a organização das pastas e testes manuais, tentou-se instalar o banco de dados MySQL na máquina. No entanto, essa tentativa foi infrutífera devido à baixa quantidade de espaço disponível, necessitando assim de uma solução alternativa. Ao procurar na internet, encontrou-se o site da empresa Neon Tech (https://neon.tech/), que permite a criação de bancos de dados relacionais online por meio da ferramenta PostgreSQL. Agora, o banco de dados relacional está hospedado lá, com cada backend acessando um banco de dados diferente: um para a "main" e outro para o "develop".
 Finalmente, foi desenvolvido um script que, ao abrir um terminal na pasta contendo o arquivo de senha da máquina AWS, possibilita a qualquer pessoa seguir as instruções linha por linha, simplesmente colando e executando. Esse script torna o processo de deploy uma tarefa de apenas alguns segundos, e com essa abordagem, não há necessidade de se preocupar com configurações complexas ou algum risco de segurança. Essa solução resulta em uma significativa economia de tempo e aumento da eficiência, simplificando todo o processo de desenvolvimento de maneira rápida e fácil.

**Backend - main**
```markdown
# Conectar à instância AWS
ssh -i FATEC-EQ2.pem ubuntu@34.193.65.107

# Navegar até o diretório do backend main
cd Backend/main

# Remover versão anterior do backend
rm -rf Back-end

# Clonar o repositório do GitHub
git clone https://github.com/Vitality-4DSM/Back-end.git

# Entrar no diretório do backend
cd Back-end

# Instalar as dependências do Node.js
npm install

# Encerrar qualquer processo usando a porta 3001
fuser -k 3001/tcp

# Iniciar o servidor do backend
npm start
```

**Backend - develop**
```markdown
# Conectar à instância AWS
ssh -i FATEC-EQ2.pem ubuntu@34.193.65.107

# Navegar até o diretório do backend develop
cd Backend/develop

# Remover versão anterior do backend
rm -rf Back-end

# Clonar o repositório do GitHub
git clone https://github.com/Vitality-4DSM/Back-end.git

# Entrar no diretório do backend
cd Back-end

# Mudar para a branch develop
git checkout develop

# Instalar as dependências do Node.js
npm install

# Encerrar qualquer processo usando a porta 3001
fuser -k 3001/tcp

# Iniciar o servidor do backend em modo de desenvolvimento
npm run dev
```


**Backend receptor - main**
```markdown
# Conectar à instância AWS
ssh -i FATEC-EQ2.pem ubuntu@34.193.65.107

# Navegar até o diretório do backend receptor main
cd BackendReceptor/main

# Remover versão anterior do backend receptor
rm -rf Back-end-receptor

# Clonar o repositório do GitHub
git clone https://github.com/Vitality-4DSM/Back-end-receptor.git

# Entrar no diretório do backend receptor
cd Back-end-receptor

# Instalar as dependências do Node.js
npm install

# Encerrar qualquer processo usando a porta 3002
fuser -k 3002/tcp

# Compilar o código TypeScript para JavaScript
npx tsc

# Iniciar o servidor do backend receptor
npm start
```


**Backend receptor - develop**
```markdown
# Conectar à instância AWS
ssh -i FATEC-EQ2.pem ubuntu@34.193.65.107

# Navegar até o diretório do backend receptor develop
cd BackendReceptor/develop

# Remover versão anterior do backend receptor
rm -rf Back-end-receptor

# Clonar o repositório do GitHub
git clone https://github.com/Vitality-4DSM/Back-end-receptor.git

# Entrar no diretório do backend receptor
cd Back-end-receptor

# Mudar para a branch develop
git checkout develop

# Instalar as dependências do Node.js
npm install

# Encerrar qualquer processo usando a porta 3002
fuser -k 3002/tcp

# Compilar o código TypeScript para JavaScript
npx tsc

# Iniciar o servidor do backend receptor em modo de desenvolvimento
npm run dev
```

**Frontend - main**
```markdown
# Conectar à instância AWS
ssh -i FATEC-EQ2.pem ubuntu@34.193.65.107

# Navegar até o diretório do backend receptor develop
cd Frontend/develop

# Remover versão anterior do backend receptor
rm -rf Front-end

# Clonar o repositório do GitHub
git clone https://github.com/Vitality-4DSM/Front-end.git

# Entrar no diretório do frontend
cd Front-end

# Instalar as dependências do Node.js
npm install

# Encerrar qualquer processo usando a porta 3000
fuser -k 3000/tcp

# Compilar o código TypeScript para JavaScript
npx tsc

# Iniciar o servidor do frontend em modo de desenvolvimento
npm run dev
```


**Frontend - develop**
```markdown
# Conectar à instância AWS
ssh -i FATEC-EQ2.pem ubuntu@34.193.65.107

# Navegar até o diretório do backend receptor develop
cd Frontend/develop

# Remover versão anterior do backend receptor
rm -rf Front-end

# Clonar o repositório do GitHub
git clone https://github.com/Vitality-4DSM/Front-end.git

# Entrar no diretório do frontend
cd Front-end

# Mudar para a branch develop
git checkout develop

# Instalar as dependências do Node.js
npm install

# Encerrar qualquer processo usando a porta 3000
fuser -k 3000/tcp

# Compilar o código TypeScript para JavaScript
npx tsc

# Iniciar o servidor do frontend em modo de desenvolvimento
npm run dev
```
