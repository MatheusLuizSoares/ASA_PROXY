# Base da imagem
FROM ubuntu:latest 

# O comando RUN serve para executar um comando na imagem
# Nesse caso abaixo, estamos atualizando repositórios de pacotes
RUN apt-get update -y 
RUN apt upgrade -y
# Abaixo, estamos atualizando os pacotes constantes na imagem
RUN apt-get install bind9 dnsutils -y
RUN apt install openssl -y


# Copia arquivo para dentro da imagem

EXPOSE 53/tcp
EXPOSE 53/udp

CMD ["/usr/sbin/named", "-g", "-c", "/etc/bind/named.conf", "-u", "bind"]