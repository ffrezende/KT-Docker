Realizar a instalação do [Docker Toolbox on Windows](https://docs.docker.com/docker-for-windows/)

## Teste de ambiente
docker version 

## Baixando uma imagem: DockerHub
docker run hello-world

Ciclo de vida e o poder do Layred FileSytem - > baixar por camadas.

## Mãos no teclado!
docker run ubuntu echo "Ola Mundo"

docker run -it ubuntu  demonstrar

docker run -v “/var/www” ubuntu

docker run -it -v "C:\Users\user\Desktop:/var/www" ubuntu

cd /var/www -> touch KT-docker.txt echo “Fala crafters” > KT-docker.txt

## Download do repositorio

docker run -p 4200:3000 -v "/Desktop/volume-exemplo:/var/www" -w "/var/www" node npm start

## Ciclo de Vida
docker ps -a
docker ps
docker start -a -t /stop images
docker inspect / port

# Buildando uma imagem

  FROM node:latest
  COPY . /var/www
  WORKDIR /var/www
  --RUN npm install--
  EXPOSE 3030
  ENTRYPOINT npm start
  
## Porta do Docker Windowns 192.168.99.100

## Criando o repositorio DockerHub

docker login --username=yourhubusername --password=yourpassword
docker build -t $DOCKER_ACC/$DOCKER_REPO:$IMG_TAG .
docker push $DOCKER_ACC/$DOCKER_REPO:$IMG_TAG


## Comandos diversos do ciclo de vida

docker ps - exibe todos os containers em execução no momento.
docker ps -a - exibe todos os containers, independente de estarem em execução ou não.

docker run -d -p 12345:80 dockersamples/static-site - define uma porta específica para ser atribuída à porta 80 do container, neste caso 12345.

docker run -it NOME_DA_IMAGEM - conecta o terminal que estamos utilizando com o do container.

docker container prune - remove todos os containers que estão parados

docker start ID_CONTAINER - inicia o container com id em questão.
docker stop ID_CONTAINER - interrompe o container com id em questão.
docker start -a -i ID_CONTAINER - inicia o container com id em questão e integra os terminais, além de permitir interação entre ambos.

docker rm ID_CONTAINER - remove o container com id em questão.
docker container prune - remove todos os containers que estão parados.
docker rmi NOME_DA_IMAGEM - remove a imagem passada como parâmetro.
docker run -d -P --name NOME dockersamples/static-site - ao executar, dá um nome ao container.
docker run -d -p 12345:80 dockersamples/static-site - define uma porta específica para ser atribuída à porta 80 do container, neste caso 12345.
docker run -d -e AUTHOR="Fulano" dockersamples/static-site - define uma variável de ambiente AUTHOR com o valor Fulano no container criado.

docker run -v "CAMINHO_VOLUME" NOME_DA_IMAGEM - cria um volume no respectivo caminho do container.
docker inspect ID_CONTAINER - retorna diversas informações sobre o container.






