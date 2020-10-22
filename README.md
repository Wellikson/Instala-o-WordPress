# Instalação do CMS WordPress

## Passo 1

>Criar pasta para o WordPress no diretorio /var/www/

>$ mkdir /var/www/WordPress

## Passo 2

>Baixar o WordPress.

>$ wget https://wordpress.org/latest.tar.gz

## Passo 3

>Desconpactar o arquivo.

>$ tar xf latest.tar.gz

## Passo 4

>mover o arquivo extraido para o diretorio criado.

>$ mv wordpress/* /var/www/WordPress/

## Passo 5

>abrir phpmyadmin

>http://ip_servidor/phpmyadmin

>criar banco de dados

![imagem criando banco de dandos](https://github.com/Wellikson/Instala-o-WordPress/blob/main/Screen%20Capture_select-area_20201021194316.png)

## Passo 6

>Abrir WordPress no servidor Apache

>http://ip_servidor

![imagem servidor web](https://github.com/Wellikson/Instala-o-WordPress/blob/main/Screen%20Capture_select-area_20201021194316.png)

## Passo 7

>Completar configuração WordPress pela web

>1. Selecionar idioma.
>2. Fornecer dados do banco criando anteriormente como nome do banco , nome do usuario e senha.
>3. configurar acesso ao WordPress , definir usuario e senha.