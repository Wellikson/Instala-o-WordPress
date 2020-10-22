# Instalação do CMS WordPress

## Passo 1

>Criar pasta para o WordPress no diretorio /var/www/
$ mkdir /var/www/wordpress

## Passo 2

>Baixar o WordPress.
$ wget https://wordpress.org/latest.tar.gz

## Passo 3

>Desconpactar o arquivo.
$ tar xf latest.tar.gz

## Passo 4

>mover o arquivo extraido para o diretorio criado.
$ mv wordpress/* /var/www/wordpress/

## Passo 5

>dar permissão completa dos aquivos para o servidor web
$ chown -R www-data: /var/www/wordpress/

## Passo 6

>Configurar o nginx para o WordPress
>Criar arquivo de configuração em /etc/nginx/sites-available/
$ nano /etc/nginx/sites-available/wordpress
~~~
server {
        listen 8080;                                               
        listen [::]:8080;
        root /var/www/wordpress;
        index index.php index.html index.htm index.nginx-debian.html;
        server_name wordpress wp;
        
        location / {
                try_files $uri $uri/ =404;
        }

        location ~ \.php$ {
                include snippets/fastcgi-php.conf;
                fastcgi_pass unix:/var/run/php/php7.2-fpm.sock;
        }

        location ~ /\.ht {
                deny all;
        }
}
~~~

## Passo 7

>checar e reiniciar servidor nginx
$ nginx -t
$ systemctl restart nginx

## Passo 8

>abrir phpmyadmin
http://ip_servidor/phpmyadmin

>criar banco de dados

![imagem criando banco de dandos](https://github.com/Wellikson/Instala-o-WordPress/blob/main/Screen%20Capture_select-area_20201021194316.png)

## Passo 9

>Abrir WordPress no servidor nginx
http://ip_servidor:8080

>Completar configuração WordPress pela web

1. Selecionar idioma.
2. Fornecer dados do banco criando anteriormente como nome do banco , nome do usuario e senha.
3. configurar acesso ao WordPress , definir usuario e senha.

