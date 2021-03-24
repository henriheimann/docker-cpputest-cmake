FROM gcc:10

WORKDIR /usr/src

RUN apt-get update && apt-get install -y cmake && \
    git clone git://github.com/cpputest/cpputest.git --depth 1 --branch v4.0 && \
    cd cpputest && \
    autoreconf . -i && \
    ./configure && \
    make

ENV CPPUTEST_HOME=/usr/src/cpputest

WORKDIR /root
