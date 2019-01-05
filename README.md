![kibana-logo](https://raw.githubusercontent.com/maliceio/kibana/master/docs/kibana-logo.png)

# malice-kibana

[![CircleCI](https://circleci.com/gh/maliceio/kibana.png?style=shield)](https://circleci.com/gh/maliceio/kibana) [![License](http://img.shields.io/:license-mit-blue.svg)](http://doge.mit-license.org) [![Docker Stars](https://img.shields.io/docker/stars/malice/kibana.svg)](https://hub.docker.com/r/malice/kibana/) [![Docker Pulls](https://img.shields.io/docker/pulls/malice/kibana.svg)](https://hub.docker.com/r/malice/kibana/) [![Docker Image](https://img.shields.io/badge/docker%20image-286MB-blue.svg)](https://hub.docker.com/r/malice/kibana/)

> Malice's Custom [Kibana](https://www.elastic.co/products/kibana) Docker Image

![screen-shot](https://raw.githubusercontent.com/maliceio/kibana/master/docs/screen-shot.png)

---

## Dependencies

- [alpine:3.8](https://hub.docker.com/_/alpine/)

## Image Tags

```bash
REPOSITORY        TAG                 SIZE
malice/kibana     latest              286MB
malice/kibana     6.5                 286MB
malice/kibana     6.4                 266MB
malice/kibana     6.3                 314MB
malice/kibana     5.6                 203MB
malice/kibana     5.5                 203MB
```

## Getting Started

```bash
$ docker run --init -d --name elasticsearch -p 9200:9200 malice/elasticsearch
$ docker run --init -d --name kibana --link elasticsearch -p 5601:5601 malice/kibana
```

## Documentation

### To use your own elasticsearch address via `ELASTICSEARCH_URL`

```bash
$ docker run --init -d --name kibana -e ELASTICSEARCH_URL=http://some-elasticsearch:9200 -p 5601:5601 malice/kibana
```

For elasticsearch running on a OSX host it would be

```bash
$ docker run --init -d --name kibana \
  -p 5601:5601 \
  --net host \
  -e ELASTICSEARCH_URL="http://$(ipconfig getifaddr en0):9200" \
  malice/kibana
```

=OR=

```bash
$ docker run --init -d --name kibana \
  -p 5601:5601 \
  --net host \
  -e ELASTICSEARCH_URL=http://localhost:9200 \
  malice/kibana
```

## Issues

Find a bug? Want more features? Find something missing in the documentation? Let me know! Please don't hesitate to [file an issue](https://github.com/maliceio/kibana/issues/new)

## CHANGELOG

See [`CHANGELOG.md`](https://github.com/maliceio/kibana/blob/master/CHANGELOG.md)

## Contributing

[See all contributors on GitHub](https://github.com/maliceio/kibana/graphs/contributors).

Please update the [CHANGELOG.md](https://github.com/maliceio/kibana/blob/master/CHANGELOG.md) and submit a [Pull Request on GitHub](https://help.github.com/articles/using-pull-requests/).

## License

MIT Copyright (c) 2016 **blacktop**
