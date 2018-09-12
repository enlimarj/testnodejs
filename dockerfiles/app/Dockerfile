#Imagem para uso da API Notes
FROM node AS node-api
MAINTAINER Edson Nascimento Lima <enlimarj@gmail.com>
RUN apt-get update && apt-get install iputils-ping -y \
net-tools \
vim \
&& rm -rf /var/lib/apt/lists/*
RUN npm install restify && npm install restify-errors && npm install mysql
CMD "node"
