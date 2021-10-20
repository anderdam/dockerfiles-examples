# FROM -> Em qual imagem será baseado a nova imagem que será criada
FROM debian

# RUN -> Comando que será executado durante a criação do container, cada comando run cria uma nova camada na imagem
RUN apt-get update && apt-get install -y apache2 && apt-get clean

# ENV -> Environment, variáveis de ambiente
ENV APACHE_LOCK_DIR="/var/lock"
ENV APACHE_PID_FILE="/var/run/apache2.pid"
ENV APACHE_RUN_USER="www-data"
ENV APACHE_RUN_GROUP="www-data"
ENV APACHE_LOG_DIR="/var/log/apache2"

#LABEL -> comentários e descrições
LABEL description="Webserver"
LABEL version="1.0.0"

VOLUME /var/www/html/
EXPOSE 80