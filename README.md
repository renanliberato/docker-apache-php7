# docker-apache-php7
Docker image com PHP 7.0

## Utilização

*clonagem do repo*<br/>
`git clone https://github.com/renanliberato/docker-apache-php7.git` <br/><br/>
*entrar na pasta*<br/>
`cd docker-apache-php7`<br/><br/>
*Criação da imagem com nome de 'docker-apache-php7'*<br/>
`sudo docker build -t docker-apache-php7 .`<br/><br/>

Após, serão realizados alguns passos em um só comando:
  * Criar e iniciar um **container** *silenciosamente* chamado 'application'
  * Criar um **volume** que linka a pasta *application* em nosso host com sua respectiva no container.
  * Criar um **volume** que linka o arquivo *000-default.conf* em nosso host com seu respectivo no container.
  * Utilizando a **imagem** 'docker-apache-php7' criada anteriormente

`sudo docker run -d --name application -v /path/to/application:/var/www/application -v /path/to/000-default.conf:/etc/apache2/sites-enabled/000-default.conf docker-apache-php7`

## Observações

  * O caminho das pastas e arquivos referenciados no volume deve ser **absoluto (full path)**
