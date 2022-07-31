FROM ubuntu:16.04
RUN apt-get update
RUN apt-get install -y nginx
RUN apt-get install -y mc
EXPOSE 80
RUN rm -rf /var/www/html/*
ADD index.html /var/www/html
CMD ["nginx", "-g", "daemon off;"]

