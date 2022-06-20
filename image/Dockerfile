# Imagen base
FROM ubuntu:latest
# Actualizamos repo... Descargamos NOMBRES de liberias y paquetes que podemos instalar
RUN apt-get update
# Instalamos python3 y software-properties-common, que son requisitos para ansible
RUN apt-get install python3 -y
RUN apt install software-properties-common -y
# Añadimos el repo de ansible
RUN add-apt-repository --yes --update ppa:ansible/ansible
# Instalamos última versión de ansible
RUN apt-get install ansible -y

# Me hago con los roles requeridos
RUN apt-get install git -y
RUN git clone https://github.com/IvanciniGT/cursoITNowAnsible /repo_empresa
ENV ANSIBLE_ROLES_PATH=/repo_empresa/roles

RUN mkdir -p /root/.ssh
RUN touch /root/.ssh/known_hosts

# Lo ejecutamos con: 
#$ docker build . -t miansible

CMD ["sh", "-c", "tail -f /dev/null"]