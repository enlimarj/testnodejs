# INSTRUÇÕES PARA INSTALAÇÃO

## REQUISITOS

Instalar:
- Docker Community Edition (CE) ou Enterprise Edition (EE)
- Docker Compose 

## VERSÃO UTILIZADA

Docker CE:
Client:
 Version:           18.06.1-ce
 API version:       1.38
 Go version:        go1.10.3
 Git commit:        e68fc7a
 Built:             Tue Aug 21 17:25:03 2018
 OS/Arch:           linux/amd64
 Experimental:      false

Docker Compose:

docker-compose version 1.22.0, build f46880fe
docker-py version: 3.4.1
CPython version: 3.6.6
OpenSSL version: OpenSSL 1.1.0f  25 May 2017

## REQUISITOS PARA USO

- Criar uma nova rede chamada NETAPP

```
docker network create netapp
```

- Criar um novo volume chamado DB_DATA

```
docker volume create db_data
```

## EXECUTANDO CONTAINERS

- Iniciando pilha de aplicações

```
docker-compose up -d
```
- Checando logs

```
docker-compose logs -f
```

- Checando logs por serviço

```
docker-compose logs -f <nome do serviço>
```

- Checar serviços estão UP

```
docker-compose ps
```

## TESTAS SERVIÇOS

O NGINX responde na porta 80 como proxy reverso para o endereço nodeapi.com.br. O mesmo endereço deve ser adicionado ou seu DNS ou ao arquivo hosts do seu computador.

Exemplo:

Linux:

Adiconar ao arquivo /etc/hosts a entrega com IP e hostname:

192.168.56.102  node-api.local.com.br

Neste caso o IP: 192.168.56.102 é o endereço atribuído a máquina virtual onde o Docker está rodando o Engine.


