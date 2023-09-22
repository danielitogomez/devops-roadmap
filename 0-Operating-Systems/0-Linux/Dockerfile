# Dowloading tag latest ubuntu image
FROM ubuntu:latest

# Installing packages
RUN apt update && apt install openssh-server sudo -y \
    apt net-tools vim -y 

# Adding user
RUN useradd -rm -d /home/ubuntu -s /bin/bash -g root -G sudo -u 1000 ultron
RUN  echo 'ultron:tony' | chpasswd

# Inicialling and expose service
RUN service ssh start
EXPOSE 22

CMD ["/usr/sbin/sshd","-D"]