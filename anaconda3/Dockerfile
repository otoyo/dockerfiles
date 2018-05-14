FROM otoyo/base

WORKDIR /root

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y \
    libbz2-dev \
    libgl1-mesa-glx \
    libreadline-dev \
    libsqlite3-dev \
    libssl-dev \
    zlib1g-dev \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# Install Anaconda
RUN wget https://repo.anaconda.com/archive/Anaconda3-5.1.0-Linux-x86_64.sh \
 && bash Anaconda3-5.1.0-Linux-x86_64.sh -b -p $HOME/anaconda \
 && rm Anaconda3-5.1.0-Linux-x86_64.sh \
 && echo '' >> .zshrc \
 && echo '# Anaconda' >> .zshrc \
 && echo 'source "$HOME/anaconda/bin/activate"' >> .zshrc

RUN ["/bin/zsh", "-c", "source $HOME/anaconda/bin/activate && conda update -y conda"]
