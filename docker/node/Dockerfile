# imagen base Ubuntu 22.04
FROM ubuntu:22.04

# evitar prompt interactivos durante apt install
ENV DEBIAN_FRONTEND=noninteractive

# paquetes necesarios
RUN apt update && apt install -y \
    openssh-server \
    curl \
    && rm -rf /var/lib/apt/lists/*

# dir requerido por openssh
RUN mkdir -p /var/run/sshd

# dir de datos de Teleport
RUN mkdir -p /var/lib/teleport

# instalar Teleport
RUN curl -L https://get.gravitational.com/teleport-v18.7.3-linux-amd64-bin.tar.gz \
    | tar -xz && mv teleport/* /usr/local/bin/

# copia config del nodo
COPY teleport.yaml /etc/teleport.yaml

# expone el puerto SSH del nodo(Teleport lo usara internamente)
EXPOSE 3022

# arranca Teleport con la config del nodo
CMD ["/usr/local/bin/teleport", "start", "--config=/etc/teleport.yaml"]
