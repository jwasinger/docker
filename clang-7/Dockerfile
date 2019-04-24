FROM debian:stretch

ADD sources.list /etc/apt/sources.list

RUN apt-get --allow-unauthenticated update -y && apt-get --allow-unauthenticated install -y wget gnupg && \
  wget -O - https://apt.llvm.org/llvm-snapshot.gpg.key | apt-key add - && \
  apt-get --allow-unauthenticated install -y clang-7 lldb-7 lld-7

RUN apt-get --allow-unauthenticated install -y make

ENV PATH="${PATH}:/usr/lib/llvm-7/bin"
