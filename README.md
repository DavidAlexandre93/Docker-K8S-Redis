<h1>Titulo ou Arte do Projeto</h1> 

<p align="center">
  <img src="https://img.shields.io/static/v1?label=docker%20kubernetes&message=framework&color=blue&style=for-the-badge&logo=DOCKER"/>
  <img src="http://img.shields.io/static/v1?label=License&message=MIT&color=green&style=for-the-badge"/>
  <!--<img src="http://img.shields.io/static/v1?label=Ruby&message=2.6.3&color=red&style=for-the-badge&logo=ruby"/>-->
  <!--<img src="http://img.shields.io/static/v1?label=Ruby%20On%20Rails%20&message=6.0.2.2&color=red&style=for-the-badge&logo=ruby"/>-->
  <img src="http://img.shields.io/static/v1?label=TESTES&message=%3E100&color=GREEN&style=for-the-badge"/>
   <img src="http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=RED&style=for-the-badge"/>
   <img src="http://img.shields.io/static/v1?label=STATUS&message=CONCLUIDO&color=GREEN&style=for-the-badge"/>
</p>

> Status do Projeto: :heavy_check_mark: :warning: (concluido, em desenvolvimento, etc)

### Tópicos 

:small_blue_diamond: [Descrição do projeto](#descrição-do-projeto)

:small_blue_diamond: [Funcionalidades](#funcionalidades)

:small_blue_diamond: [Deploy da Aplicação](#deploy-da-aplicação-dash)

:small_blue_diamond: [Pré-requisitos](#pré-requisitos)

:small_blue_diamond: [Como rodar a aplicação](#como-rodar-a-aplicação-arrow_forward)

... 

Insira os tópicos do README em links para facilitar a navegação do leitor

## Descrição do projeto 

<p align="justify">
  Descrição breve do projeto compondo um paragrafo ou dois. 
</p>

## Funcionalidades

:heavy_check_mark: Funcionalidade 1  

:heavy_check_mark: Funcionalidade 2  

:heavy_check_mark: Funcionalidade 3  

:heavy_check_mark: Funcionalidade 4  

## Layout ou Deploy da Aplicação :dash:

> Link do deploy da aplicação. 

... 

Se ainda não houver deploy, insira capturas de tela da aplicação ou gifs

## Pré-requisitos

:warning: [Node](https://nodejs.org/en/download/)

...

Liste todas as dependencias e libs que o usuário deve ter instalado na máquina antes de rodar a aplicação 

## Como rodar a aplicação :arrow_forward:

No terminal, clone o projeto: 

```
git clone https ou ssh do projeto
```
# Docker-K8S-API
Projeto DevOps


# Build project 
docker build -t pasta_do_projeto .
docker build -t tgmarinho/dockernode .


# Criando o conteiner 
docker run -p 3000:3000 -d tgmarinho/dockernode
docker start ID

# Para verificar logs
docker logs ID

# Executar docker-compose
docker-compose up

# Gerar uma imgagem da estrutura docker criada 
docker build -t seu_usuario_dockerhub/nome_image .

# Subir imagem no docker hub
docker push nome_da_imagem

# Para fazer uso da imagem no docker hub 
docker pull wagnerww/nodejs-docker-mongo-redis

# Para destruir conteiner 
docker-compose down
docker stop ID

# Listando conteiner em execucao
docker ps

# .env
MONGO_USERNAME=sammy
MONGO_PASSWORD=your_password
MONGO_PORT=27017
MONGO_DB=sharkinfo


# Iniciar o K8S
kubectl apply -f wp-dumb.yaml
kubectl scale deployment meu-blog-escalavel --replicas=5

# Para visualizar os PODS do K8S
kubectl get pods

# para buscar um pod por nome
kubectl get pods meu-blog
kubectl get pods -l app=wordpress-escalavel

# para buscar um pod por label
 kubectl get pods -l app=wordpress

# para retornar em outro formato de output
 kubectl get pods -l app=wordpress -o yaml
 kubectl get pods -l app=wordpress -o json

# acessar o pod rodando
  kubectl exec -it meu-blog bash
root@meu-blog:/var/www/html#

# descricao do Pod
  kubectl describe pods -l app=wordpress
  kubectl describe pods meu-blog

# criando um arquivo qualquer
 echo "lala" > arquivo-lala.txt

# copiando um arquivo para o container
 kubectl cp arquivo-lala.txt meu-blog:/var/www/html

# copiando um arquivo do container para sua maquina
 kubectl cp meu-blog:/var/www/html/arquivo-lala.txt arquivo-lele.txt

 # para verificar CPU e Memoria 
  kubectl top pods -l app=wordpress
  kubectl top pods meu-blog

  # para remover Pod
   kubectl delete pods -l app=wordpress
   kubectl delete pods meu-blog

   # Porta do MongoDB
   host:localhost e porta:27017

# Comando docker-compose 
docker-compose up: cria e inicia os contêineres;
docker-compose build: realiza apenas a etapa de build das imagens que serão utilizadas;
docker-compose logs: visualiza os logs dos contêineres;
docker-compose restart: reinicia os contêineres;
docker-compose ps: lista os contêineres;
docker-compose scale: permite aumentar o número de réplicas de um contêiner;
docker-compose start: inicia os contêineres;
docker-compose stop: paralisa os contêineres;
docker-compose down: paralisa e remove todos os contêineres e seus componentes como rede, imagem e volume.


# Comandos docker 
 docker container run hello-world

 docker image ls

 docker image rm hello-world --force

 # POC-TCC-Docker-NodeJS
POC do meu TCC - REST API em NodeJS e Mongo rodando em Docker. 

# Como usar:

* Clone o projeto:

```
  # git clone git@github.com:msfidelis/POC-TCC-Docker-NodeJS.git
```

* Build do projeto

```
  # cd POC-TCC-Docker-NodeJS/
  # docker-compose up -d 
```

* url

```
  http://localhost:8080
```

#Metodos

* Create - POST
```
 http://localhost:8080/api/add {descricao: String, concluido: Boolean}
```

* Update - PUT
```
 http://localhost:8080/api/add {_id, descricao: String, concluido: Boolean}
```

* READ - GET
```
 http://localhost:8080/api/all 
 http://localhost:8080/get/{descricao}
```

* DELETE - DELETE
```
 http://localhost:8080/api/all 
 http://localhost:8080/api/delete/{id}
```

... 

Coloque um passo a passo para rodar a sua aplicação. **Dica: clone o próprio projeto e verfique se o passo a passo funciona**

## Como rodar os testes

Coloque um passo a passo para executar os testes

```
$ npm test, rspec, etc 
```

## Casos de Uso

Explique com mais detalhes como a sua aplicação poderia ser utilizada. O uso de **gifs** aqui seria bem interessante. 

Exemplo: Caso a sua aplicação tenha alguma funcionalidade de login apresente neste tópico os dados necessários para acessá-la.

## JSON :floppy_disk:

### Usuários: 

|name|email|password|token|avatar|
| -------- |-------- |-------- |-------- |-------- |
|David Alexandre|davidalexandrefernandes@outlook.com|davidalexandre93|true|https://avatars.githubusercontent.com/u/38826514?s=400&u=8c88ded33bb7f95ac76772a892ba2ffebc6bb120&v=4|

... 

Se quiser, coloque uma amostra do banco de dados 

## Iniciando/Configurando banco de dados

Se for necessário configurar algo antes de iniciar o banco de dados insira os comandos a serem executados 

## Linguagens, dependencias e libs utilizadas :books:

- [Nome da Linguagem ou dependencia](link)
- [Nome da Linguagem ou dependencia](link)

...

Liste as tecnologias utilizadas no projeto que **não** forem reconhecidas pelo Github 

## Resolvendo Problemas :exclamation:

Em [issues]() foram abertos alguns problemas gerados durante o desenvolvimento desse projeto e como foram resolvidos. 

## Tarefas em aberto

Se for o caso, liste tarefas/funcionalidades que ainda precisam ser implementadas na sua aplicação

:memo: Tarefa 1 

:memo: Tarefa 2 

:memo: Tarefa 3 

## Desenvolvedores/Contribuintes :octocat:

Liste o time responsável pelo desenvolvimento do projeto

| [<img src="https://avatars.githubusercontent.com/u/38826514?s=400&u=8c88ded33bb7f95ac76772a892ba2ffebc6bb120&v=4" width=115><br><sub>David Alexandre</sub>](https://github.com/DavidAlexandre93/) |  
| :---: | :---: | :---: 

## Licença 

The [MIT License]() (MIT)

Copyright :copyright: Ano - Titulo do Projeto
