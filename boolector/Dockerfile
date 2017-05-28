FROM ubuntu:xenial


RUN apt-get update && \
    apt-get -y dist-upgrade && \
    apt-get -y install \
        build-essential \
        bzip2 \
        wget && \
    apt-get clean


RUN cd && \
    wget http://fmv.jku.at/boolector/boolector-2.4.1-with-lingeling-bbc.tar.bz2 && \
    tar xf boolector-2.4.1-with-lingeling-bbc.tar.bz2 && \
    cd boolector-2.4.1-with-lingeling-bbc && \
    make && \
    cp boolector/bin/* /usr/local/bin