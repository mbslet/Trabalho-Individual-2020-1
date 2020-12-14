# Trabalho Individual 2020-1

Esse trabalho propõe a solução para dockerização e integração contínua para o projeto proposto pela disciplina.

## Atividades

* Conteinerização
* Integração Contínua
* Deploy(**extra**) - Não Realizada

## Ferramentas e Uso

### Docker
* No processo de containerização foram criados três containers, **db**, **api** e **client**.
* Foi criado um *Docker File* para o client e a api, esse documento de texto contém todos os comandos para montar uma imagem.
* Foi criado um docker-compose.yml que descreve a infraestrutura como código e como ela vai se comportar ao ser iniciado.

### GitHub Actions
* A integração contínua do projeto proposto foi feita pelo github actions, com um arquivo nomeado ci.yml. 
* Dividido em dois **jobs**, o *client* e o *api*, e dois **steps** para cada.
* O CI será ativado toda vez que o ousuário der um *push* ou um *pull request* e roda todas as tarefas como build e teste.
* A **coleta de métricas** é feita pelo **SonarCloud** e integrado ao CI.

## Rodando a Solução

### Docker
``docker-compose up --build `` para baixar e subir dependências

``docker-compose up`` para apenas subir todos containers integrados do projeto

### Testes

#### Client
`` docker-compose run client yarn run test:unit``

#### Api
``docker-compose run api bundle exec rails tes`` 