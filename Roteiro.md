
Fork Repo
 $git clone https://github.com/ThiagoCRDM/ci-cd-enati-2023.git

(Github)
Criar Repositorio no github


Setar novo Remote
 $git remote set-url origin <URL_REPO>



Configuração GitHub

Profile -> Settings-> Develop Settings -> Personal access Tokens -> Generate new Token

Criar Conta Docker Hub
  <https://hub.docker.com/>

Criar Access Token Docker Hub
  Accont Settings -> Security -> New Access Token


Configuração Repositorio
Repo -> Settings -> Secrets and Variables -> Actions
  Secrets
    ACTIONS_DEPLOY_ACCESS_TOKEN
    DOCKERHUB_TOKEN
    DOCKER_USER

Criar Pipeline CI (Ambiente dev)
  $git checkout -b develop
criar pasta para o GitHUb actions
.github -> workflows -> ci.yaml 

Configuração
  name
  trigger
  jobs
    testes
    build image and push

Criar Pipeline CD
  .github -> workflows -> cd.yaml
  $npm  install --save gh-pages
  conf: package.json -> "homepage": "https://<USER_GITHUB>.github.io/<PROJECT>/",

Configuração
  name
  trigger
  jobs
    testes
    build image and push
    deploy (GH-Pages)
