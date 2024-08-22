###This is the Dockerfile for backend
FROM ubuntu
RUN apt-get update && apt-get install -y \
    nginx \
    php-fpm \
    php-mysql
COPY ./index.html /var/www/html/index.html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
