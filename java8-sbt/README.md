# SBT

Dockerfile for any version of sbt (default 0.13.9).

## Usage
Build an image:

```sh
VERSION=0.13.5
docker build -t sbt-$VERSION --build-arg SBT_VERSION=$VERSION .
```

Run a container:

```sh
docker run -it sbt-$VERSION /bin/bash
```

Verify version:

```sh
sbt --version
```
