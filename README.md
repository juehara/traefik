# traefik

Para executar o traefik execute o comando:

docker container run -d -p 8080:8080 -p 80:80 \
-v <pwd>/traefik.yml:/etc/traefik/traefik.yml
-v /var/run/docker.sock:/var/run/docker.sock \
traefik:latest

## O Traefik utiliza o nome do container para executar o reverso
Quando voce executar um container por exemplo:

docker container run -d --name apache httpd

o traefik ira responder na url http://apache.docker.localhost