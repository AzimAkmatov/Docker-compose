FROM ubuntu
RUN apt update -y
RUN apt install nginx -y
WORKDIR /var/www/html
COPY ./index.html /var/www/html/index.html
COPY chicago.jpeg /var/www/html/
COPY . .
VOLUME . /var/www/html/
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]