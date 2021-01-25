# Curso Alura Docker

Curso desenvolvido na Alura sobre tecnologia de containers aplicados no Docker com o orquestrador de containers Docker Compose.


## Cheat Sheet

Cheat Sheet construído durante o desenvolvimento do curso.

### List

docker ps: list docker containers

docker ps -a: lista todos os containers

docker ps -q: lista apenas os ids

### Run

docker run image: run a image

docker run -it image: run a image with cli

docker run -d image: run e dettach a imagem do cli

docker run -P image: atribua uma porta para o host interagir com o container

docker run -p 12345:80 image: atribui uma porta específica do host para o container

docker run -e ENV="" image: atribui uma variável de ambiente para o container

docker run image --name: atribui um nome para o container

docker run -w "/var/www" npm

### Start

docker start id: inicia um container parado

docker start -a -i: attach um comando

### Stop

docker stop id: para um container

docker stop -t 0: para um container imediatamente

docker stop -t 0 $(docker ps -q): para todos os container ativos

### Remove

docker rm: remove um container

docker rm -f: para e remove um container

docker container prune: remove todos containers inativos

### Images

docker images: lista todas as imagens

docker rmi: remove uma imagem

### Ports

docker port id: mostra as portas de um container

### Volume

docker run -v "/var/www": roda o container com uma pasta como volume

### Info

docker inspect id: informações sobre container

### Build (generate image)

docker build -f Dockerfile -t andreepdias/node . : cria image a partir do dockerfile

### Docker Hub

docker login: login no docker hub

docker pull image-name: faz pull de uma imagem

docker push image-name: faz push de uma imagem

### Network

docker network create --drive bridge network-name: cria uma rede com o driver bridge

docker network ls: lista as redes

docker run --network network-name image: roda um container em uma rede específica (o nome do container funciona como dns)

docker network inspect network-name: exibe informações da rede, com containers que fazem parte dela

## Docker-Compose

docker-compose build: build todos os containers se houver arquivo docker-compose.yml na pasta

docker-compose up: sobe os containers do build

docker-compose up -d: sobe sem prender o cli

docker-compose ps: lista os containers

docker-compose down: para os containers e deleta

docker-compose restart: reinicia os containers
