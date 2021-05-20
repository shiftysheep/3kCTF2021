FROM php:8-apache
LABEL maintainer "shiftysheep"

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install netcat-traditional && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# move php files into directory
COPY ./app /var/www/html
RUN cd /var/www/html

# Expose the web port to the network
EXPOSE 80

CMD ["apache2ctl","-D","FOREGROUND"]