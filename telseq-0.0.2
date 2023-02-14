FROM ubuntu:14.04
Maintainer Prathima Vembu <pvembu@stanford.edu>
LABEL Description="Telseq docker" Version="0.02"

VOLUME /tmp

WORKDIR /tmp

RUN apt-get update && \
    apt-get install -y \
    samtools>=1.16.1 \
    build-essential \
    zlib1g-dev \
    libncurses5-dev \
    ca-certificates \
    gcc \
    make \
    libpq-dev \
    git \
    apt-transport-https \
    liblzma-dev \
    libbz2-dev \
    libcurl3-dev \
    autotools-dev \
    automake \
    cmake \
    wget 

RUN mkdir -p /deps && \
    cd /deps && \
    wget https://github.com/pezmaster31/bamtools/archive/v2.4.0.tar.gz && \
    tar -xzvf v2.4.0.tar.gz && \
    rm v2.4.0.tar.gz && \
    cd bamtools-2.4.0 && \
    mkdir build && \
    cd build && \
    cmake .. && \
    make

RUN mkdir -p /src && \
    cd /src && \ 
    wget https://github.com/zd1/telseq/archive/refs/tags/v0.0.2.tar.gz && \
    tar -xzvf v0.0.2.tar.gz && \
    rm v0.0.2.tar.gz && \
    cd telseq-0.0.2/src && \
    ./autogen.sh && \
    ./configure --with-bamtools=/deps/bamtools-2.4.0 --prefix=/usr/local && \    
    make && \
    make install 


ENTRYPOINT ["/usr/local/bin/telseq"]
CMD ["--help"]