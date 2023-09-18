<p align="center">
      <img src="" alt="" width="200">
      <h1 align="center"> 1 Sprint </h1>
</p>
Na primeira sprint foi avaliado o desafio proposto pelo cliente, e após conversas para entender a dor e soluções, concluiu-se que precisaríamos desenvolver um projeto, capaz de lidar com grandes quantidade de dados, que seriam recebidos de varias estações meteorológicas, que serão feitas usando arduinos capazes de capturar parâmetros atmosféricos, os enviando como json para um Backend, que pegará os dados e salvará num banco não relacional, permitindo uma alta performasse e capacidade de lidar com altas quantidades de dados.
Um segundo Backend será responsável por de 30 em 30 segundos, pegar os dados brutos do não relacional e os tratar, para salvar nos padrões de um banco relacional, onde ficaram salvas as informações com suas devidas relações. Além disso o segundo Backend também ficará responsável, pelas requisições e respostas do Frontent com o banco de dados relacional.
Na primeira sprint, foi acordado com o cliente que o Mvp, seria a documentação do projeto que inclui modelo de dados relacional e não relacional, mockup feito no figma das páginas e CRUD inicial do projeto no backend, com proteção de rota usando JWT.


## 🎲 Modelo de dados

### Modelo do banco relacional:
<img src="https://github.com/whatscodeg3/API-3DSM-Frontend/assets/73721760/956f857a-ad68-4a46-bfbb-e9460bc7c563" width="1000">

### Modelo do banco não relacional:
<img src="https://github.com/whatscodeg3/API-3DSM-Frontend/assets/73721760/489adc8d-fe53-453a-ab86-fe8af4ed52be" width="1000">

## 📝 Mockup

- Página estações
<img src="https://github.com/whatscodeg3/API-3DSM-Frontend/assets/73721760/3a484c0d-32b3-479a-a509-328b7d1bd8a4" width="500">

- Cadastro de estações
<img src="https://github.com/whatscodeg3/API-3DSM-Frontend/assets/73721760/4413dfcc-7246-4ab5-8d02-084d5088e351" width="500">

- Editar estações
<img src="https://github.com/whatscodeg3/API-3DSM-Frontend/assets/73721760/2c3953fa-d6d6-4692-bb99-fd47569b238d" width="500">

- Página de login
<img src="https://github.com/whatscodeg3/API-3DSM-Frontend/assets/73721760/d5e2e1ce-863e-4fe9-a8cd-22674bb18c17" width="500">


## 📉 Burndown 