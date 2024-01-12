FROM debian:bullseye
RUN apt-get update -y && apt-get upgrade -y
RUN apt-get install -y nginx openssl -y

EXPOSE 443
CMD ["nginx", "-g", "daemon off;"]