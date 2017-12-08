FROM debian:stretch-backports

RUN apt-get update && apt-get install -y \
  gcc make cmake valgrind \
  doxygen libnuma-dev librdmacm-dev libibverbs-dev git \
  libzmq3-dev libkrb5-dev libboost-all-dev libcpprest-dev catch \
  && rm -rf /var/lib/apt/lists/*
