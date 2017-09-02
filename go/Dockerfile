FROM otoyo/base

WORKDIR /root

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y \
    mysql-client \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# Set GOPATH and PATH
RUN mkdir go \
 && echo '# Golang' >> .zshrc \
 && echo 'export GOPATH=$HOME/go' >> .zshrc \
 && echo 'export PATH=$PATH:$GOPATH/bin' >> .zshrc

# Install exenv
RUN ["/bin/zsh", "-c", "anyenv install goenv"]
