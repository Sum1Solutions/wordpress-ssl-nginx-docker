FROM ubuntu:16.04
RUN apt-get update --fix-missing
RUN apt-get install -y software-properties-common
RUN apt-get install -y libssl-dev
WORKDIR /ssl-certs
CMD openssl req -x509 -nodes -days $period -subj "/C=CA/ST=QC/O=Company, Inc./CN=$domain_name" -newkey rsa:2048 -keyout /ssl-certs/nginx-selfsigned.key -out /ssl-certs/nginx-selfsigned.crt;