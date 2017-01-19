# What is XMR-Stak-CPU?

XMR-Stak-CPU is a universal Stratum pool miner. This is the CPU-mining version.

## Links

- [Discussion](https://www.reddit.com/r/Monero/comments/5nduep/xmrstakcpu_v101_update/)
- [Source Code](https://github.com/fireice-uk/xmr-stak-cpu)
- [Dockerfile](https://github.com/minecoins/docker-xmr-stak-cpu)

# How to use this image

## Configuration file

Create `config.txt` configuration file and adapt to your need before running.
You can copy file from a container:

```console
$ docker run -d --name some-xmr-stak-cpu-config minecoins/xmr-stak-cpu
$ docker cp some-xmr-stak-cpu-config:/usr/local/etc/config.txt .
$ docker stop some-xmr-stak-cpu-config
$ docker rm some-xmr-stak-cpu-config
```

or copy example from [GitHub](https://github.com/fireice-uk/xmr-stak-cpu/blob/v1.1.0-1.1.0/config.txt).

## Running

Run in background:

```console
$ docker run -itd --name some-xmr-stak-cpu -v "$PWD"/config.txt:/usr/local/etc/config.txt minecoins/xmr-stak-cpu
```

Use `--privileged` option for large pages support. Lare pages need a properly set up OS.

Fetch logs of a container:

```console
$ docker logs some-xmr-stak-cpu
```

Attach:

```console
$ docker attach some-xmr-stak-cpu
```

# Donations

Donations for work on dockerizing are accepted at:

- BTC: `1NUMFM6UTv9iRVVzjsfhzbAGjwNxQRA8Qz`
- XMR: `49TfoHGd6apXxNQTSHrMBq891vH6JiHmZHbz5Vx36nLRbz6WgcJunTtgcxnoG6snKFeGhAJB5LjyAEnvhBgCs5MtEgML3LU`
