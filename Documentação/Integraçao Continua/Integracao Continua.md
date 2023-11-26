# Explicação de Integração continua <a id="deployment"></a>

## O que é Integração Continua

 A entrega contínua (Continuous Delivery) é uma prática do DevOps que se concentra na automação do processo de entrega de software, desde o desenvolvimento até a produção. O objetivo é permitir que as equipes entreguem novas versões do software de maneira rápida, eficiente e confiável.

 ## Pontos Trabalhados:
 Implantação Automatizada
 - Automação do processo de implantação do software em ambientes de teste e produção.
 
Automação de Testes:
- Execução automática de testes de unidade, integração e aceitação.


## Automatização dos Testes:
- Para a execução de testes foi usado o Git Actions que permite criar uma maquina virtual temporária que pode realizar diversas funções de Integração continua.
- Utilizando um arquivo YML em um repositório com o padrão de pasta sendo: NOME_REPOSITORIO/.github/workflows/Arquivo.yml
<img src="https://github.com/Vitality-4DSM/Documentacao/blob/main/Documentação/Teste.png" alt="" width="800">

## Video de execucão 
- https://youtu.be/Bi_Ob41WQeo?si=28cewdIBwyjo-D2V


## Deploy Automático <a id="deployment"></a>
- Para realizar o deploy automático foi necessário utilizar duas bibliotecas externas junto ao Git Actions
- Uma para se Conectar a Maquina e compartilhar arquivos
- E outra para realizar comandos SSH
<img src="https://github.com/Vitality-4DSM/Documentacao/blob/main/Documentação/Deploy%20Aut.png" alt="" width="800">

- Além de utilizar a função de Secrets no Github para utilizar arquivos confidenciais da maquina virtual

<img src="https://github.com/Vitality-4DSM/Documentacao/blob/main/Documentação/Secret.png" alt="" width="800">
<img src="https://github.com/Vitality-4DSM/Documentacao/blob/main/Documentação/UpSecret.png" alt="" width="800">

## Video de execucão 
https://youtu.be/I99TeYKhRVY?si=fIz-nE3PNJashB4O
