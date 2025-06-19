# Use the latest Debian slim image
FROM debian:bullseye-slim

# Set environment to non-interactive for apt
ENV DEBIAN_FRONTEND=noninteractive

# Install common tools
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    bash \
    curl \
    vim \
    nano \
    dnsutils \
    iputils-ping \
    net-tools \
    procps \
    ca-certificates && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Set the default shell
SHELL ["/bin/bash", "-c"]

# Set working directory
WORKDIR /root

# Set the default command to an interactive shell
CMD [ "bash" ]
