# Docker Images

Dockerfiles and build scripts for Lambda Functions Docker images.

## Elixir

A series of images all based on Ubuntu 17.04 and Erlang/OTP 20, but with different versions of Elixir (installed from the Erlang Solutions
Debian repo, following the [official guide](https://elixir-lang.org/install.html#unix-and-unix-like).)

These images are available from the [Docker Hub](https://hub.docker.com/r/lambdafn/elixir/tags/).  The general format of the tags is:

`$ELIXIR_VERSION-otp$OTP_VERSION-[nox|x11]-$DISTRO`

`$ELIXIR_MINOR_VERSION` exists as an alias to `$ELIXIR_VERSION-otp20-nox-ubuntu`, so `1.5` is currently the same as `1.5.0-otp20-nox-ubuntu`.

### Example

```
$ docker run --rm -it lambdafn/elixir:1.5 sh -c "iex --version"
Erlang/OTP 20 [erts-9.0] [source] [64-bit] [smp:4:4] [ds:4:4:10] [async-threads:10] [kernel-poll:false]

IEx 1.5.0

$ docker run --rm -it lambdafn/elixir:1.4 sh -c "iex --version"
Erlang/OTP 20 [erts-9.0] [source] [64-bit] [smp:4:4] [ds:4:4:10] [async-threads:10] [kernel-poll:false]

IEx 1.4.5
```

## Tools

To list the different tags of a repository that are available to be pulled, you might be interested in [Ahab's `docker-tags`](https://github.com/clarkema/ahab).
