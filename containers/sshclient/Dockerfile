FROM debian:bullseye-slim
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update
RUN apt-get install -y --no-install-recommends \
    bash \
    screen \
    curl \
    wget \
    vim \
    nano \
    iputils-ping \
    ca-certificates \
    sudo \
    openssh-client
RUN apt-get clean
RUN rm -rf /var/lib/apt/lists/*
RUN useradd -ms /bin/bash debian && \
    usermod -aG sudo debian && \
    echo 'debian ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers
RUN echo 'PS1="\u@sshclient:\w\$ "' >> /home/debian/.bashrc
SHELL ["/bin/bash", "-c"]
WORKDIR /home/debian
USER debian
CMD ["bash"]
