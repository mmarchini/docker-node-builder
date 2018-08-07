FROM debian:stretch-slim

WORKDIR /node

ENV CC clang-3.9
ENV CXX clang++-3.9

RUN apt-get update && apt-get install clang-3.9 make python -y --no-install-recommends && \
    rm -rf /var/lib/apt/lists/*

CMD ./configure && make -j$(getconf _NPROCESSORS_ONLN)
