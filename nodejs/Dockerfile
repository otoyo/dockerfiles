FROM otoyo/base

WORKDIR /root

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y \
    libssl-dev \
    mysql-client \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# Install exenv
RUN ["/bin/zsh", "-c", "anyenv install ndenv"]
