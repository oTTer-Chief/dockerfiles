FROM debian:stretch-backports

ARG PDA_VERSION=11.4.7

RUN apt-get update && apt-get install -y \
  gcc g++ make cmake valgrind \
  doxygen libnuma-dev librdmacm-dev libibverbs-dev git \
  libzmq3-dev libkrb5-dev libboost-all-dev libcpprest-dev catch \
  libpci-dev gcc libtool libtool-bin libkmod-dev wget \
  && rm -rf /var/lib/apt/lists/* \
  && cd /tmp \
  && wget https://github.com/cbm-fles/pda/archive/$PDA_VERSION.tar.gz \
  && tar -xf $PDA_VERSION.tar.gz && rm -f $PDA_VERSION.tar.gz \
  && cd /tmp/pda-$PDA_VERSION && mkdir -p /opt/pda/ \
  && ./configure --debug=true --prefix=/opt/pda/$PDA_VERSION/ \
  && make install \
  && rm -rf /tmp/pda-$PDA_VERSION
