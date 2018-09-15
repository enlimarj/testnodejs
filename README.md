# INSTRUÇÕES PARA INSTALAÇÃO

## REQUISITOS

Instalar:
- Docker Community Edition (CE) ou Enterprise Edition (EE)
- Docker Compose

Link: https://www.docker.com/products/docker-engine

## VERSÃO UTILIZADA

### Docker CE:

 Version: 18.06.1-ce

### Docker Compose:

Version 1.22.0

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

Neste caso o IP: 192.168.56.102 é o endereço atribuído a máquina virtual onde o Docker está rodando o Engine
### UTILIZADO O POSTMAN

Utilizado o aplicativo da Google Chrome Apps Store.

Link: https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop/related?hl=pt-BR

O mesmo pode ser obtido no site oficial:

Link: https://www.getpostman.com

1 - Passo: Abra o aplicativo Postman




