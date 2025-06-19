FROM debian:bullseye-slim
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    bash \
    screen \
    tree \
    ncat \
    git\
    wget\
    zip \
    unzip \
    tar \
    xz-utils \
    jq \
    lsof \
    strace \
    man \
    manpages \
    python3-venv \
    build-essential \
    nmap \
    tcpdump \
    iproute2 \
    netcat \
    socat \
    whois \
    traceroute \
    curl \
    vim \
    nano \
    dnsutils \
    iputils-ping \
    net-tools \
    procps \
    ca-certificates \
    sudo \
    python3 \
    python3-pip \
    nodejs \
    npm && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
RUN useradd -ms /bin/bash debian && \
    usermod -aG sudo debian && \
    echo 'debian ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers
RUN echo 'PS1="\u@sandbox:\w\$ "' >> /home/debian/.bashrc
SHELL ["/bin/bash", "-c"]
WORKDIR /home/debian
USER debian
CMD ["bash"]
