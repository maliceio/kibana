![kibana-logo](https://raw.githubusercontent.com/maliceio/kibana/master/docs/kibana-logo.png)

malice-kibana
=============

[![CircleCI](https://circleci.com/gh/maliceio/kibana.png?style=shield)](https://circleci.com/gh/maliceio/kibana) [![License](http://img.shields.io/:license-mit-blue.svg)](http://doge.mit-license.org) [![Docker Stars](https://img.shields.io/docker/stars/malice/kibana.svg)](https://hub.docker.com/r/malice/kibana/) [![Docker Pulls](https://img.shields.io/docker/pulls/malice/kibana.svg)](https://hub.docker.com/r/malice/kibana/) [![Docker Image](https://img.shields.io/badge/docker%20image-202MB-blue.svg)](https://hub.docker.com/r/malice/kibana/)

> Malice's Custom [Kibana](https://www.elastic.co/products/kibana) Docker Image

![screen-shot](https://raw.githubusercontent.com/maliceio/kibana/master/docs/screen-shot.png)

---

**Table of Contents**

-	[Dependencies](#dependencies)
-	[Image Tags](#image-tags)
-	[Getting Started](#getting-started)
-	[Documentation](#documentation)
-	[Issues](#issues)
-	[Credits](#credits)
-	[CHANGELOG](#changelog)
-	[Contributing](#contributing)
-	[License](#license)

### Dependencies

-	[alpine:3.6](https://index.docker.io/_/gliderlabs/alpine/)

### Image Tags

```bash
REPOSITORY        TAG                 SIZE
malice/kibana     latest              202MB
malice/kibana     6.0                 187MB
malice/kibana     5.5                 202MB
```

### Getting Started

```bash
$ docker run -d --name elasticsearch -p 9200:9200 malice/elasticsearch
$ docker run -d --name kibana --link elasticsearch -p 5601:5601 malice/kibana
```

### Documentation

#### To use your own elasticsearch address via `ELASTICSEARCH_URL`

```bash
$ docker run -d --name kibana -e ELASTICSEARCH_URL=http://some-elasticsearch:9200 -p 5601:5601 malice/kibana
```

For elasticsearch running on a OSX host it would be

```bash
$ docker run -d --name kibana \
  -p 5601:5601 \
  --net host \
  -e ELASTICSEARCH_URL="http://$(ipconfig getifaddr en0):9200" \
  malice/kibana
```

=OR=

```bash
$ docker run -d --name kibana \
  -p 5601:5601 \
  --net host \
  -e ELASTICSEARCH_URL=http://localhost:9200 \
  malice/kibana
```

### Issues

Find a bug? Want more features? Find something missing in the documentation? Let me know! Please don't hesitate to [file an issue](https://github.com/maliceio/kibana/issues/new)

### CHANGELOG

See [`CHANGELOG.md`](https://github.com/maliceio/kibana/blob/master/CHANGELOG.md)

### Contributing

[See all contributors on GitHub](https://github.com/maliceio/kibana/graphs/contributors).

Please update the [CHANGELOG.md](https://github.com/maliceio/kibana/blob/master/CHANGELOG.md) and submit a [Pull Request on GitHub](https://help.github.com/articles/using-pull-requests/).

### License

MIT Copyright (c) 2016-2017 **blacktop**
