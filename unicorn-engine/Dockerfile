FROM debian:stretch

RUN apt-get update && \
    apt-get dist-upgrade -y && \
    apt-get install -y build-essential python-dev python-setuptools wget

RUN cd && \
    wget https://github.com/unicorn-engine/unicorn/archive/1.0.1.tar.gz && \
    tar xf 1.0.1.tar.gz && \
    cd unicorn-1.0.1 && \
    make -j $(nproc) && \
    make install && \
    cd bindings-python && \
