FROM ubuntu:17.10

VOLUME /sources

RUN apt-get update && apt-get install -y sbcl buildapp curl
RUN cd /tmp \
    && curl -LO 'https://beta.quicklisp.org/quicklisp.lisp' \
    && sbcl --load /tmp/quicklisp.lisp --eval '(quicklisp-quickstart:install)'
