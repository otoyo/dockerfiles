FROM otoyo/base

WORKDIR /root

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y \
    silversearcher-ag \
    tmux \
    vim \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# Install git completion
RUN mkdir -p .zsh/completion \
 && cd .zsh/completion \
 && curl -O https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash \
 && curl -O https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.zsh \
 && mv git-completion.zsh _git \
 && echo '# git-completion' >> .zshrc \
 && echo 'fpath=(~/.zsh $fpath)' >> .zshrc
