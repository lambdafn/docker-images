FROM ubuntu:17.04

ARG ERLANG_PACKAGE=erlang-nox
ARG ELIXIR_VERSION

RUN apt-get update                                                          && \
    apt-get install -y wget                                                 && \
    wget https://packages.erlang-solutions.com/erlang-solutions_1.0_all.deb && \
    dpkg -i erlang-solutions_1.0_all.deb                                    && \
    apt-get update
RUN apt-get install -y $ERLANG_PACKAGE
RUN apt-get install -y elixir=$ELIXIR_VERSION
RUN apt-mark hold $ERLANG_PACKAGE elixir
