FROM debian:bullseye
RUN apt-get update -y && apt-get upgrade -y
RUN apt-get install -y nginx openssl -y

RUN mkdir /etc/nginx/ssl

COPY conf/nginx.conf /etc/nginx/conf.d/default.conf

RUN openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/nginx/ssl/nginx.key -out /etc/nginx/ssl/nginx.crt -subj "/CN=jorgfern.42.fr/C=ES/L=Malaga"

EXPOSE 443
CMD ["nginx", "-g", "daemon off;"]