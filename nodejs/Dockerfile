FROM otoyo/base

WORKDIR /root

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y --fix-missing \
    libssl-dev \
    mysql-client

# Install Chrome
RUN wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add - \
 && echo "deb http://dl.google.com/linux/chrome/deb/ stable main" > /etc/apt/sources.list.d/google.list \
 && apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y --fix-missing \
    google-chrome-stable \
    xvfb \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# Install exenv
RUN ["/bin/zsh", "-c", "anyenv install ndenv"]
