FROM ubuntu

RUN apt-get update && \
    apt-get -y dist-upgrade && \
    apt-get -y install bison \
                       build-essential \
                       cmake \
                       flex \
                       git \
                       libboost-all-dev \
                       python \
                       perl \
                       vim-common \
                       wget \
                       zlib1g-dev && \
    apt-get clean


RUN cd && \
    git clone https://github.com/niklasso/minisat.git && \
    cd minisat && \
    mkdir build && cd build && \
    cmake .. && \
    make && \
    make install && \
    ldconfig


RUN cd && \
    git clone https://github.com/msoos/cryptominisat && \
    cd cryptominisat && \
    mkdir build && cd build && \
    cmake .. && \
    make && \
    make install && \
    ldconfig

    
RUN cd && \
    wget https://github.com/stp/stp/archive/stp-2.2.0.tar.gz && \
    tar xf stp-2.2.0.tar.gz && \
    cd stp-stp-2.2.0 && \
    mkdir build && cd build && \
    cmake -DSTATICCOMPILE=ON .. && \
    make && \
    make install && \
    ldconfig