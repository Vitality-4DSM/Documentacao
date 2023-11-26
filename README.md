<p align="center">
      <img src="" alt="" width="200">
      <h1 align="center"> Vitality | Projeto Gaia do 4 DSM </h1>

<hr>

<br>

<p align="center">
  <a href="#api">Aprendizagem por Projetos Integrados</a> • 
  <a href="#desafio">Desafio</a> • 
  <a href="#escopo">Escopo do Projeto</a> • 
  <a href="#backlog">Backlog das Sprints</a> • 
  <a href="#rastreamento">Rastreamento de Requisitos</a> •
  <a href="#devops">DevOps</a> •
  <a href="#tecnologia">Tecnologias</a> •
  <a href="#sprint">Sprints</a> • 
  <a href="#equipe">Equipe</a>  
</p>

<br>

<h4 align="center">  
  Status do Projeto: Em andamento ⏳️ 
</h4>

<br>

## Aprendizagem por Projetos Integrados <a id="api"></a>

  A API (Aprendizagem por Projetos Integrados), desenvolvida no escopo do CADI, é a metodologia de ensino em implantação na Fatec São José dos Campos, desde o Segundo Semestre de 2019, do qual os alunos formam equipes baseadas na metodologia scrum, tendo um aluno como master, Product Owner e os integrates restantes dev team. O time é desafiado por um cliente real (nesse projeto nosso cliente é a MidAll: Tecnologias), a desenvolver uma solução para um problema, tendo que atender requisitos exigidos de tecnologia. <br> 
  
  O API segue tendo como pilares os seguintes valores: <br>
 - Real Problem Based Learning (rPBL) <br>
 - Validação Externa <br>
 - Mindset Ágil (Agile) <br>

<br>

## :pencil2: Desafio <a id="desafio"></a>

Sistema de Coleta de Dados de Estações Meteorológicas <br>

A empresa Tecsus realiza a coleta e processamento de dados através de redes de sensores sem fio,
também conhecidos como IoT (Internet das Coisas) na área de utilidades (água, energia e gás) os
dados são transmitidos por diversos meios de comunicação dentre eles Sigfox, LoRa e GSM. A fim
de expandir o seu portfólio para o monitoramento ambiental a empresa gostaria de experimentar
o desenvolvimento de estações meteorológicas de baixo custo com os seguintes sensores: direção
e velocidade do vento, índice pluviométrico, umidade, temperatura e pressão. Essas informações
devem ser coletadas periodicamente e enviadas para um servidor, onde os dados devem ser
recepcionados, tratados e exibidos em um portal capaz de disponibilizar relatórios e dashboards. <br>

Com o intuito de envolver os alunos do ensino médio com a aprendizagem baseada em problemas
o portal deve demonstrar os conceitos matemáticos envolvidos nos cálculos dos parâmetros bem
como relacionar a importância do monitoramento ambiental como ferramenta para evitar
desastres naturais através da geração de alertas. Serão disponibilizados dois kits de estação
meteorológica que ao final do projeto deverão ser instaladas na Escola Estadual Elmano Ferreira
Veloso e na Fatec de São José dos Campos. <br>

<br>

## :dart: Escopo do Projeto <a id="escopo"></a>

 > *Requisitos Funcionais*

· Desenvolvimento de um datalogger para uma estação meteorológica

· Montagem de uma estação meteorológica

· Cadastro das estações, parâmetros e usuários

· Recepção dos dados das estações meteorológicas

· Dashboards para visualização dos parâmetros meteorológicos

· Tutorial para os alunos do significado de cada parâmetro meteorológico

 > *Requisitos Não Funcionais*

· Prezar pelo UX dos dashboards

· Instigar nos alunos de ensino médio o gosto pelo estudo através da aprendizagem
baseada em problemas

· Documentações de rotas das APIs

· Pipeline de IC

· Deploy automático

<br>

## :dart: Backlog Total <a id="backlog"></a>

| Tarefa | Prioridade | User Stories | Critério de Aceitação | Sprint | Status |
| :----: | :--------: | :----------: | :-------------------: | :----: | :----: |
| Documentação do projeto | Alta 🟥 | Eu, como Fatec, quero que o projeto tenha cada sprint documentada no GitHub para avaliação. | Preencher e atualizar o GitHub com as documentações relevantes do projeto para fins de organização e avaliação. | Entrega contínua | ✅ |
| Ferramentas de DevOps | Alta 🟥 | Eu, como Fatec, quero que sejam incorporados processos de DevOps na realização do projeto. | Uso de processos de DevOps para desenvolver mais as habilidades da equipe em entrega contínua. | Entrega contínua | ✅ |
| Modelo de dados | Alta 🟥 | Eu, como cliente, quero que seja feito um modelo de dados dos bancos que serão usados para visualizar como serão feitos os bancos de dados. | Criar o modelo físico relacional do banco relacional e não relacional. | 1 | ✅ |
| Arquitetura do projeto | Alta 🟥 | Eu, como cliente, quero que seja feito um mapa de como será o fluxo do projeto. | Documentar a arquitetura do projeto. | 1 | ✅ |
| Layout das páginas do projeto | Média 🟨 | Eu, como cliente, quero que seja feito um mockup das páginas do projeto para visualizar como serão feitas. | Criar as páginas no Figma e validar com o cliente. | 1 | ✅ |
| Banco relacional | Alta 🟥 | Eu, como cliente, quero um banco de dados onde as informações possam ser salvas e usadas quando necessário. | Criar o banco relacional no MySQL. | 1 | ✅ |
| Proteção de rotas | Alta 🟥 | Eu, como cliente do sistema, quero que as rotas sejam protegidas para que apenas pessoas autorizadas possam usar certas funções do sistema. | Proteger os backends, permitindo o acesso às rotas apenas com token. | 2 | ✅ |
| Página de estações | Alta 🟥 | Eu, como cliente, quero que o sistema tenha um CRUD completo de estações. | Criar uma página capaz de realizar o CRUD de estações. | 2 | ✅ |
| Página de login | Média 🟨 | Eu, como cliente, quero que o sistema tenha um perfil público e de administrador para manter a segurança do projeto. | Criar uma página que disponibilizará o token após um login bem-sucedido para usar opções de administrador. | 2 | ✅ |
| Banco não relacional | Média 🟨 | Eu, como cliente, quero um banco de dados capaz de lidar com o grande fluxo de dados recebidos das estações. | Criar o banco não relacional no MongoDB para conseguir lidar com grandes volumes de dados recebidos, mantendo a performance e não sobrecarregando o sistema. Os dados serão enviados para o banco relacional a cada 30 segundos. | 2 | ✅ |
| Sincronização do não relacional pro relacional | Alta 🟥 | Eu, como cliente, quero que seja feito uma sincronização entre o banco não relacional e relacional, pegando os dados e os tratando para passar de um para o outro, a cada 30 segundos. | Criar uma sincronização automatica, que passa dados do não relacional pro relacional de 30 em 30 segundos. | 2 | ✅ |
| Página de parâmetros | Alta 🟥 | Eu, como cliente, quero que o sistema tenha um CRUD completo de parâmetros. | Criar uma página capaz de realizar o CRUD de parâmetros. | 3 | ✅ |
| Página de dashboard | Alta 🟥 | Eu, como cliente, quero que o sistema tenha um dashboard que permitirá visualizar as informações salvas no banco de dados. | Criar uma página que terá gráficos exibindo informações do banco relacionadas aos parâmetros coletados. | 3 | ✅ |
| Guia dos parâmetros | Alta 🟥 | Eu, como cliente, quero uma área que descreva sobre os parâmetros usados no projeto para fins educacionais de quem usar o site. | Criar uma página que conterá uma explicação dos parâmetros cadastrados no sistema. | 3 | ✅ |
| Deploy | Alta 🟥 | Eu, como cliente, quero que o projeto tenha um deploy automático. | Criar um script para iniciar a aplicação e integrá-la à entrega contínua. | 3 | ✅ |
| Programar uma estação com C | Alta 🟥 | Eu, como cliente, quero que uma estação seja criada usando código em C e Arduino. | Desenvolver o código que será usado na estação. | 3 | ✅ |
| Página de usuário | Média 🟨 | Eu, como cliente, quero que o sistema tenha um CRUD de usuários para facilitar o controle de administradores. | Criar uma página que conterá o CRUD de usuários do sistema. | 3 | ✅ |
| Página de alerta | Média 🟨 | Eu, como cliente, quero que tenha um CRUD completo de alertas que devem ser disparados e listados em um histórico. | Criar uma página que terá um CRUD dos alertas. Os alertas poderão ser cadastrados com base em certos tipos de verificações, e ao serem acionados, criarão uma notificação e aparecerão no histórico. | 4 | ✅ |
| Construir uma estação com Arduino | Média 🟨 | Eu, como cliente, quero que uma estação seja criada usando código em C e Arduino. | Construção da estação com Arduino, e uso do código desenvolvido. | 4 | ✅ |

<br>

## Rastreamento de Requisitos <a id="rastreamento"></a>

<img src="https://github.com/Vitality-4DSM/Documentacao/blob/main/Documentação/Backlog.png" width="450">

<br>

## Pipeline de DevOps <a id="devops"></a>

- ([Clique aqui para verificar](https://github.com/Vitality-4DSM/Documentacao/blob/main/Documenta%C3%A7%C3%A3o/DevOps/pipeline.md))

<br>

## 🛠 Tecnologias <a id="tecnologia"></a>

As seguintes ferramentas foram usadas na construção do projeto:

- [Node.js](https://nodejs.org/en/)
- [React](https://pt-br.reactjs.org/)
- [TypeScript](https://www.typescriptlang.org/)
- [Jira](https://www.atlassian.com/br/software/jira)
- [Arduino](https://www.arduino.cc/)

<br>

## :date: Sprints <a id="sprint"></a>

[ 🔖SPRINT 1](https://github.com/Vitality-4DSM/Documentacao/tree/main/Documenta%C3%A7%C3%A3o/Sprint/Sprint%201)(✅) - Concluída.

[🔖 SPRINT 2](https://github.com/Vitality-4DSM/Documentacao/tree/main/Documenta%C3%A7%C3%A3o/Sprint/Sprint%202)(✅) - Concluída. 

[🔖 SPRINT 3](https://github.com/Vitality-4DSM/Documentacao/tree/main/Documenta%C3%A7%C3%A3o/Sprint/Sprint%203)(✅) - Concluída.

[🔖 SPRINT 4](https://github.com/Vitality-4DSM/Documentacao/tree/main/Documenta%C3%A7%C3%A3o/Sprint/Sprint%204)(✅) - Concluída.

<br>

## 👨‍💼 Equipe <a id="equipe"></a>
| Membro | Função | Github | Linkedin |
| :----: | :----: | :----: | :------: |
| Julio de Paula        | Product Owner/Desenvolvedor  | [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/JulioPm142) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/j%C3%BAlio-machado-7a07a4250/) |
| Jonatas Mathias       | Scrum Master/Desenvolvedor   | [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Jonatas-Dallo) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jonatas-mathias-147638206/) |
| Gabriel da Cunha      | Desenvolvedor  | [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Tuuca) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabriel-da-cunha-de-macedo-199890250/) |
| Ryan Alves            | Desenvolvedor  | [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/XLryan246) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ryan-alves-661ba823b/) |
| Valderi Douglas       | Desenvolvedor  | [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ValderiDouglas) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://br.linkedin.com/in/valderidouglas) |
| Pedro Antonio         | Desenvolvedor  | [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Pedro-Toledo) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://br.linkedin.com/in/pedro-antonio-rizzo-toledo-71b465232) |
| Lucas Vinicius        | Desenvolvedor  | [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/LucasVinicius32) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/lucasviniciussoares/) |
