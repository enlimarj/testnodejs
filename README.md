# INSTRUÇÕES PARA INSTALAÇÃO

## COMPOSIÇÃO DA PILHA DE APLICAÇÕES

- Webserver Nginx
- Aplicação Node.JS
- Banco de Dados Mysql
- SGBD phpMyAdmin (Extra)

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
<a href="http://tinypic.com?ref=2yu0f49" target="_blank"><img src="http://i68.tinypic.com/2yu0f49.png" border="0" alt="Image and video hosting by TinyPic"></a>

- Checar serviços estão UP

```
docker-compose ps
```

<a href="http://tinypic.com?ref=16k7rma" target="_blank"><img src="http://i68.tinypic.com/16k7rma.png" border="0" alt="Image and video hosting by TinyPic"></a>

- Checando logs

```
docker-compose logs -f
```

<a href="http://tinypic.com?ref=2iac4eh" target="_blank"><img src="http://i63.tinypic.com/2iac4eh.png" border="0" alt="Image and video hosting by TinyPic"></a>

- Checando logs por serviço

```
docker-compose logs -f <nome do serviço>
```
<a href="http://tinypic.com?ref=30xitmo" target="_blank"><img src="http://i63.tinypic.com/30xitmo.png" border="0" alt="Image and video hosting by TinyPic"></a>


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

2 - Teste o GET

<a href="http://tinypic.com?ref=2dkilpd" target="_blank"><img src="http://i65.tinypic.com/2dkilpd.jpg" border="0" alt="Image and video hosting by TinyPic"></a>

3 - Teste o POST

<a href="http://tinypic.com?ref=2d6uzdc" target="_blank"><img src="http://i64.tinypic.com/2d6uzdc.png" border="0" alt="Image and video hosting by TinyPic"></a>

4 - Teste o DELETE

<a href="http://tinypic.com?ref=29x8508" target="_blank"><img src="http://i66.tinypic.com/29x8508.png" border="0" alt="Image and video hosting by TinyPic"></a>
