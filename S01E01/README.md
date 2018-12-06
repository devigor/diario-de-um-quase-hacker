# L4B

## Ato 1
Antes de começar a realmente colocar a mão na massa, eu preciso ter um ambiente
controlado pra poder realizar os teste sem prejudicar terceiros.

Meu sistema base é o Fedora 29. Não achei necessário usar o Kali Linux, prefiro
eu mesmo instalar as ferramentas conforme for necessário e os alvos serão
constituídos em duas aplicações web rodando em cima do Docker e uma máquina virtual rodando o Metasploitable 2.

## Ato 2
Chegou a parte de montar nosso ambiente, os seguintes softwares precisaram ser instalados:
  - **[Docker](https://docker.com)**
  - **[VirtualBox](https://www.virtualbox.org/)**

A instalação do [Metasploitable 2](https://sourceforge.net/projects/metasploitable/files/Metasploitable2/) não é nada complicada, logo não irei focar na instalação dela.
A parte importante aqui vai ser colocar as aplicações web para rodar, sempre lembrando que elas iram rodar em cima do Docker.

## Ato 3
A primeira aplicação é a **DVWA**, pra fazer ela rodar precisa apenas de dois comandos 

#### Comandos
> $ docker pull vulnerables/web-dvwa

> $ docker run --rm -it -p 80:80 vulnerables/web-dvwa

Abra o navegador e acesse *localhost:80*

A segunda aplicação é a **WebGoat**, pra fazer ela rodar precisa apenas de dois
comandos

#### Comandos
> $ docker pull webgoat/webgoat-8.0

> $ docker run --rm -it -p 8080:8080 webgoat/webgoat-8.0

Abra o navegador e acesse *localhost:8080/WebGoat*
