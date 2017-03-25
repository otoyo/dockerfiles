FROM otoyo/base

WORKDIR /root

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y \
    fop \
    libncurses-dev \
    libssl-dev \
    libxml2-utils \
    mysql-client \
    openjdk-7-jdk \
    unixodbc-dev \
    xsltproc \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# Install Earlang 19.2
RUN wget http://www.erlang.org/download/otp_src_19.2.tar.gz \
 && tar xvzf otp_src_19.2.tar.gz \
 && cd otp_src_19.2 \
 && ./configure --without-wx \
 && make \
 && make install \
 && cd ../ \
 && rm -rf otp_src_19.2*

# Install exenv
RUN ["/bin/zsh", "-c", "anyenv install exenv"]
