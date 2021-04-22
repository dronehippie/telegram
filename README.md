# telegram

[![Current Tag](https://img.shields.io/github/v/tag/dronehippie/telegram?sort=semver)](https://github.com/dronehippie/telegram) [![Build Status](http://drone.webhippie.de/api/badges/dronehippie/telegram/status.svg)](http://drone.webhippie.de/api/badges/dronehippie/telegram) [![Join the Matrix chat at https://matrix.to/#/#webhippie:matrix.org](https://img.shields.io/badge/matrix-%23webhippie-7bc9a4.svg)](https://matrix.to/#/#webhippie:matrix.org) [![Docker Size](https://img.shields.io/docker/image-size/dronehippie/telegram/latest)](https://hub.docker.com/r/dronehippie/telegram) [![Docker Pulls](https://img.shields.io/docker/pulls/dronehippie/telegram)](https://hub.docker.com/r/dronehippie/telegram) [![Go Reference](https://pkg.go.dev/badge/github.com/dronehippie/telegram.svg)](https://pkg.go.dev/github.com/dronehippie/telegram) [![Go Report Card](https://goreportcard.com/badge/github.com/dronehippie/telegram)](https://goreportcard.com/report/github.com/dronehippie/telegram) [![Codacy Badge](https://app.codacy.com/project/badge/Grade/5298cef2ec4b4a67876ce1dd991f7547)](https://www.codacy.com/gh/dronehippie/telegram/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=dronehippie/telegram&amp;utm_campaign=Badge_Grade)

Drone plugin send build notifications to Telegram. For the usage information and a listing of the available options please take a look at the [documentation](https://dronehippie.github.io/telegram/).

## Build

Build the binary with the following command:

```console
export GOOS=linux
export GOARCH=amd64

make build
```

## Docker

Build the image with the following command:

```console
docker build \
  --label org.opencontainers.image.source=https://github.com/dronehippie/telegram \
  --label org.opencontainers.image.revision=$(git rev-parse --short HEAD) \
  --label org.opencontainers.image.created=$(date -u +"%Y-%m-%dT%H:%M:%SZ") \
  --file docker/Dockerfile.amd64 --tag dronehippie/telegram .
```

## Usage

```console
docker run --rm \
  -e PLUGIN_DUMMY="dummy" \
  -v $(pwd):$(pwd) \
  -w $(pwd) \
  dronehippie/telegram
```

## Security

If you find a security issue please contact [thomas@webhippie.de](mailto:thomas@webhippie.de) first.

## Contributing

Fork -> Patch -> Push -> Pull Request

## Authors

-   [Thomas Boerger](https://github.com/tboerger)

## License

Apache-2.0

## Copyright

```console
Copyright (c) 2021 Thomas Boerger <thomas@webhippie.de>
```
