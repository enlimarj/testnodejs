#Imagem para uso da API Notes
FROM nginx AS nginxapi
MAINTAINER Edson Nascimento Lima <enlimarj@gmail.com>
RUN apt-get update && apt-get install iputils-ping -y \
net-tools \
vim \
&& rm -rf /var/lib/apt/lists/*
CMD "nginx -g 'daemon off;'"

