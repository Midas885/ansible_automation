

# Dockerfile
FROM ubuntu:22.04

RUN apt update && apt install -y \
    openssh-server \
    sudo \
    passwd \
    cowsay \
    htop

RUN useradd -m ansible && echo "ansible:ansible" | chpasswd && \
    echo "ansible ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

RUN mkdir /var/run/sshd
EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
