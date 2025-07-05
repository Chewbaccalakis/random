FROM debian:bullseye-slim
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    bash \
    screen \
    git\
    wget\
    zip \
    unzip \
    tar \
    man \
    manpages \
    nmap \
    curl \
    vim \
    nano \
    dnsutils \
    iputils-ping \
    net-tools \
    ca-certificates \
    sudo \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
RUN useradd -ms /bin/bash debian && \
    usermod -aG sudo debian && \
    echo 'debian ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers
RUN echo 'PS1="\u@sum:\w\$ "' >> /home/debian/.bashrc
SHELL ["/bin/bash", "-c"]
WORKDIR /home/debian
USER debian
CMD ["bash"]
