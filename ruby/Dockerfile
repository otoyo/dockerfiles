FROM otoyo/base

WORKDIR /root

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y \
    bzip2 \
    libmysqld-dev \
    libreadline-dev \
    libssl-dev \
    mariadb-server-5.5 \
    memcached \
    redis-server \
    zlib1g-dev \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# Install rbenv
RUN ["/bin/zsh", "-c", "anyenv install rbenv"]
