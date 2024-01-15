FROM debian:bullseye
RUN apt-get update -y && apt-get upgrade -y
RUN apt-get install -y nginx openssl -y

RUN openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /home/panesico/data/nginx/nginx.key -out /home/panesico/data/nginx/nginx.crt -subj "/CN=jorgfern.42.fr/C=ES/L=Malaga"

EXPOSE 443
CMD ["nginx", "-g", "daemon off;"]