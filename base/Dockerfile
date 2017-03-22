FROM ubuntu:14.04

ONBUILD CMD ["/bin/zsh"]

WORKDIR /root

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y \
    build-essential \
    curl \
    git \
    language-pack-ja \
    zsh \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# Set localtime to JST
RUN ln -sf /usr/share/zoneinfo/Asia/Tokyo /etc/localtime

# Set locale
RUN echo 'export LANG=ja_JP.UTF-8' >> .zshrc \
 && echo 'export LC_ALL=ja_JP.UTF-8' >> .zshrc

# Register known_hosts
RUN if [ ! -d .ssh ]; then mkdir .ssh; fi \
 && chmod 700 .ssh \
 && ssh-keyscan -H github.com >> .ssh/known_hosts

# Install anyenv
RUN git clone https://github.com/riywo/anyenv .anyenv \
 && echo 'export PATH="$HOME/.anyenv/bin:$PATH"' >> .zshenv \
 && echo 'eval "$(anyenv init - zsh)"' >> .zshenv