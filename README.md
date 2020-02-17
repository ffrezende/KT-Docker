Realizar a instalação do [Docker Toolbox on Windows](https://download.docker.com/win/stable/DockerToolbox.exe)

## Teste de ambiente
docker version 

## Baixando uma imagem: DockerHub
docker run hello-world <br/>

Ciclo de vida e o poder do Layred FileSytem - > baixar por camadas.<br/>

## Mãos no teclado!
docker run ubuntu echo "Ola Mundo"<br/>

docker run -it ubuntu  demonstrar<br/>

docker run -v “/var/www” ubuntu<br/>

docker run -it -v "C:\Users\user\Desktop:/var/www" ubuntu<br/>

cd /var/www -> touch KT-docker.txt echo “Fala crafters” > KT-docker.txt<br/>

## Download do repositorio

docker run -p 4200:3000 -v "/Desktop/volume-exemplo:/var/www" -w "/var/www" node npm start<br/>

## Ciclo de Vida
docker ps -a<br/>
docker ps<br/>
docker start -a -t /stop images<br/>
docker inspect / port<br/>

# Buildando uma imagem

  FROM node:latest<br/>
  COPY . /var/www<br/>
  WORKDIR /var/www<br/>
  --RUN npm install--<br/>
  EXPOSE 3030<br/>
  ENTRYPOINT npm start<br/>
  
## Porta do Docker Windows 192.168.99.100

## Criando o repositorio DockerHub

docker login --username=yourhubusername --password=yourpassword
docker build -t $DOCKER_ACC/$DOCKER_REPO:$IMG_TAG .
docker push $DOCKER_ACC/$DOCKER_REPO:$IMG_TAG


## Comandos diversos do ciclo de vida

docker ps - exibe todos os containers em execução no momento.<br/>
docker ps -a - exibe todos os containers, independente de estarem em execução ou não.<br/>

docker run -d -p 12345:80 dockersamples/static-site - define uma porta específica para ser atribuída à porta 80 do container, neste caso 12345.<br/>

docker run -it NOME_DA_IMAGEM - conecta o terminal que estamos utilizando com o do container.<br/>

docker container prune - remove todos os containers que estão parados<br/>

docker start ID_CONTAINER - inicia o container com id em questão.<br/>
docker stop ID_CONTAINER - interrompe o container com id em questão.<br/>
docker start -a -i ID_CONTAINER - inicia o container com id em questão e integra os terminais, além de permitir interação entre ambos.<br/>

docker rm ID_CONTAINER - remove o container com id em questão.<br/>
docker container prune - remove todos os containers que estão parados.<br/>
docker rmi NOME_DA_IMAGEM - remove a imagem passada como parâmetro.<br/>
docker run -d -P --name NOME dockersamples/static-site - ao executar, dá um nome ao container.<br/>
docker run -d -p 12345:80 dockersamples/static-site - define uma porta específica para ser atribuída à porta 80 do container, neste caso 12345.<br/>
docker run -d -e AUTHOR="Fulano" dockersamples/static-site - define uma variável de ambiente AUTHOR com o valor Fulano no container criado.<br/>

docker run -v "CAMINHO_VOLUME" NOME_DA_IMAGEM - cria um volume no respectivo caminho do container.<br/>
docker inspect ID_CONTAINER - retorna diversas informações sobre o container.<br/>






