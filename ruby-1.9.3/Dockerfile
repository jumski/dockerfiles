FROM gliderlabs/alpine:3.2
MAINTAINER Wojtek Majewski <jumski@gmail.com>

RUN apk update 
RUN apk upgrade 
RUN apk add curl 
RUN apk add wget 
RUN apk add bash 
RUN apk add alpine-sdk

ENV RUBY_VERSION 1.9.3-p551
ENV RUBY_FAMILY 1.9
ENV RUBY_TARBALL ruby-${RUBY_VERSION}.tar.gz
ENV RUBY_URL https://cache.ruby-lang.org/pub/ruby/${RUBY_FAMILY}/${RUBY_TARBALL}

WORKDIR /usr/local/src
RUN wget --quiet ${RUBY_URL}
RUN tar zxf ${RUBY_TARBALL}

WORKDIR /usr/local/src/ruby-${RUBY_VERSION}

RUN apk add zlib-dev
RUN apk add openssl-dev
RUN apk add gdbm-dev
RUN apk add db-dev
RUN apk add readline-dev
RUN apk add libffi-dev
RUN apk add coreutils
RUN apk add yaml-dev
RUN apk add autoconf
RUN apk add clang

ENV CFLAGS "-fno-omit-frame-pointer -fno-strict-aliasing"
# RUN ./configure 
# RUN make
# RUN make install
# RUN rm -rf /usr/local/src/ruby-*
#
# # # Install ruby and ruby-bundler
# # RUN apk add ruby ruby-bundler
