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
  <a href="#devops">DevOps</a> •
  <a href="#tecnologia">Tecnologias</a> •
  <a href="#sprint">Sprints</a> • 
  <a href="#equipe">Equipe</a>  
</p>

<br>

<h4 align="center">  
  Status do Projeto: Concluído ✅
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


## Product Backlog <a id="product"></a>

| **Item**                                     | **Descrição**                                                                                                         |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Desenvolvimento do Datalogger para Estação Meteorológica | Desenvolver o código para o Datalogger que registrará os dados provenientes das estações meteorológicas.            |
| Montagem da Estação Meteorológica              | Montar a estação meteorológica física, possivelmente utilizando hardware como Arduino.                                |
| Cadastro de Estações, Parâmetros e Usuários    | Implementar funcionalidades de cadastro para estações meteorológicas, parâmetros e usuários no sistema.               |
| Recepção de Dados das Estações Meteorológicas  | Desenvolver a capacidade do sistema para receber e processar os dados enviados pelas estações meteorológicas.          |
| Dashboards de Visualização dos Parâmetros Meteorológicos | Criar páginas de dashboard para visualização dos parâmetros meteorológicos, priorizando uma experiência de usuário agradável. |
| Tutorial sobre Significado dos Parâmetros Meteorológicos | Desenvolver uma seção educacional que explique o significado de cada parâmetro meteorológico, especialmente voltada para alunos do ensino médio. |
| Melhoria Contínua do UX nos Dashboards         | Implementar melhorias contínuas na experiência de usuário nas páginas de dashboard, levando em consideração o feedback dos usuários. |
| Aprendizagem para Alunos do Ensino Médio | Desenvolver funcionalidades ou conteúdos educacionais que estimulem o interesse dos alunos do ensino médio por meio da aprendizagem. |
| Documentação de Rotas das APIs                | Documentar as rotas das APIs utilizadas no projeto para facilitar a compreensão e manutenção do sistema.              |
| Configuração da Pipeline de Integração Contínua (IC) | Estabelecer uma pipeline de integração contínua para automatizar testes e garantir a qualidade do código.          |
| Implementação de Deploy Automático             | Desenvolver um processo de deploy automático para facilitar a distribuição e atualização da aplicação.                |

<br>

| **ID** | **Requisitos**                                |                                                                                                           |
|--------|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| 01      | Documentação das Sprints no GitHub            | Eu, como Fatec, quero que cada sprint seja documentada no GitHub para avaliação.                                      |
| 02      | Incorporação de Processos de DevOps           | Eu, como Fatec, quero que sejam incorporados processos de DevOps na realização do projeto.                             |
| 03      | Modelo de Dados                               | Eu, como cliente, quero que seja feito um modelo de dados dos bancos que serão usados para visualizar como serão feitos os bancos de dados. |
| 04      | Arquitetura do Projeto                        | Eu, como cliente, quero que seja feito um mapa de como será o fluxo do projeto.                                        |
| 05      | Layout das Páginas do Projeto                 | Eu, como cliente, quero que seja feito um mockup das páginas do projeto para visualizar como serão feitas.             |
| 06      | Banco Relacional                              | Eu, como cliente, quero um banco de dados onde as informações possam ser salvas e usadas quando necessário.            |
| 07      | Proteção de Rotas                             | Eu, como cliente do sistema, quero que as rotas sejam protegidas para que apenas pessoas autorizadas possam usar certas funções do sistema. |
| 08      | Página de Login                               | Eu, como cliente, quero que o sistema tenha um perfil público e de administrador para manter a segurança do projeto.    |
| 09      | Banco Não Relacional                          | Eu, como cliente, quero um banco de dados capaz de lidar com o grande fluxo de dados recebidos das estações.            |
| 10     | Sincronização Não Relacional para Relacional   | Eu, como cliente, quero que seja feita uma sincronização entre o banco não relacional e relacional, pegando os dados e os tratando para passar de um para o outro, a cada 30 segundos. |
| 11     | Página de Parâmetros                          | Eu, como cliente, quero que o sistema tenha um CRUD completo de parâmetros.                                            |
| 12     | Página de Dashboard                           | Eu, como cliente, quero que o sistema tenha um dashboard que permitirá visualizar as informações salvas no banco de dados. |
| 13     | Guia dos Parâmetros                           | Eu, como cliente, quero uma área que descreva sobre os parâmetros usados no projeto para fins educacionais de quem usar o site. |
| 14     | Deploy Automático                             | Eu, como cliente, quero que o projeto tenha um deploy automático.                                                       |
| 15     | Programar uma Estação com C e Arduino         | Eu, como cliente, quero que uma estação seja criada usando código em C e Arduino.                                      |
| 16     | Página de Usuário                             | Eu, como cliente, quero que o sistema tenha um CRUD de usuários para facilitar o controle de administradores.           |
| 17     | Página de Alerta                               | Eu, como cliente, quero que tenha um CRUD completo de alertas que devem ser disparados e listados em um histórico.      |
| 18     | Construir uma Estação com Arduino             | Eu, como cliente, quero que uma estação seja criada usando código em C e Arduino.                                     |
<br>

## :dart: Backlog Total <a id="backlog"></a>

| Tarefa | Prioridade | Critério de Aceitação | Sprint | Status |
| :----: | :--------: | :-------------------: | :----: | :----: |
| ID 01 - Documentação do projeto | Alta 🟥  | Preencher e atualizar o GitHub com as documentações relevantes do projeto para fins de organização e avaliação. | Entrega contínua | ✅ |
| ID 02 - Ferramentas de DevOps | Alta 🟥  | Uso de processos de DevOps para desenvolver mais as habilidades da equipe em entrega contínua. | Entrega contínua | ✅ |
| ID 03 - Modelo de dados | Alta 🟥 | Criar o modelo físico relacional do banco relacional e não relacional. | 1 | ✅ |
| ID 04 - Arquitetura do projeto | Alta 🟥  | Documentar a arquitetura do projeto. | 1 | ✅ |
| ID 05 - Layout das páginas do projeto | Média 🟨  | Criar as páginas no Figma e validar com o cliente. | 1 | ✅ |
| ID 06 - Banco relacional | Alta 🟥  | Criar o banco relacional no MySQL. | 1 | ✅ |
| ID 07 - Proteção de rotas | Alta 🟥  | Proteger os backends, permitindo o acesso às rotas apenas com token. | 2 | ✅ |
| Página de estações | Alta 🟥  | Criar uma página capaz de realizar o CRUD de estações. | 2 | ✅ |
| ID 08 - Página de login | Média 🟨 | Criar uma página que disponibilizará o token após um login bem-sucedido para usar opções de administrador. | 2 | ✅ |
| ID 09 - Banco não relacional | Média 🟨 | Criar o banco não relacional no MongoDB para conseguir lidar com grandes volumes de dados recebidos, mantendo a performance e não sobrecarregando o sistema. Os dados serão enviados para o banco relacional a cada 30 segundos. | 2 | ✅ |
| ID 10 - Sincronização do não relacional pro relacional | Alta 🟥 | Criar uma sincronização automatica, que passa dados do não relacional pro relacional de 30 em 30 segundos. | 2 | ✅ |
| ID 11 - Página de parâmetros | Alta 🟥 | Criar uma página capaz de realizar o CRUD de parâmetros. | 3 | ✅ |
| ID 12 - Página de dashboard | Alta 🟥 | Criar uma página que terá gráficos exibindo informações do banco relacionadas aos parâmetros coletados. | 3 | ✅ |
| ID 13 - Guia dos parâmetros | Alta 🟥 | Criar uma página que conterá uma explicação dos parâmetros cadastrados no sistema. | 3 | ✅ |
| ID 14 - Deploy | Alta 🟥 | Criar um script para iniciar a aplicação e integrá-la à entrega contínua. | 3 | ✅ |
| ID 15 - Programar uma estação com C | Alta 🟥 | Desenvolver o código que será usado na estação. | 3 | ✅ |
| ID 16 - Página de usuário | Média 🟨 | Criar uma página que conterá o CRUD de usuários do sistema. | 3 | ✅ |
| ID 17 - Página de alerta | Média 🟨 | Criar uma página que terá um CRUD dos alertas. Os alertas poderão ser cadastrados com base em certos tipos de verificações, e ao serem acionados, criarão uma notificação e aparecerão no histórico. | 4 | ✅ |
| ID 18 - Construir uma estação com Arduino | Média 🟨 |  Construção da estação com Arduino, e uso do código desenvolvido. | 4 | ✅ |

<br>

## Documentação DevsOps <a id="devops"></a>
- ([Branch](https://github.com/Vitality-4DSM/Documentacao/blob/main/Documentação/Branch/Branch.md))
- ([Deploy](https://github.com/Vitality-4DSM/Documentacao/blob/main/Documentação/Deploy/Deploy.md))
- ([Integração Continua ](https://github.com/Vitality-4DSM/Documentacao/blob/main/Documentação/Integraçao%20Continua/Integracao%20Continua.md))
- ([Monitoramento ](https://github.com/Vitality-4DSM/Documentacao/blob/main/Documentação/Monitoramento/Monitoramento.md))
- ([Rastreabilidade de requisitos](https://github.com/Vitality-4DSM/Documentacao/blob/main/Documentação/Rastreabilidade%20de%20requisitos/Rastreabilidade%20de%20requisitos.md))
- ([Teste](https://github.com/Vitality-4DSM/Documentacao/blob/main/Documentação/Testes/Teste.md))
- ([Swagger](https://github.com/Vitality-4DSM/Documentacao/blob/main/Documentação/Rotas/Rotas.md))
  

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
