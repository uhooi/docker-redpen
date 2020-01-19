# docker-redpen

[![](http://dockeri.co/image/uhooi/redpen)](https://hub.docker.com/r/uhooi/redpen)  
[![](https://github.com/uhooi/docker-redpen/workflows/CD/badge.svg)](https://github.com/uhooi/docker-redpen/actions?query=workflow%3ACD)

Docker image for RedPen.

## Usage

### Shell

##### Pull the Docker image from Docker Hub:

```bash
$ docker pull uhooi/redpen:latest
```

##### Create a container from the image and run it:

```bash
# Output RedPen version
$ docker run --rm uhooi/redpen --version
1.10.4

# Run RedPen example
$ docker run --rm -v $PWD:/work uhooi/redpen --lang ja --format review --conf redpen-conf.xml --limit 0 foo.re
```

### GitHub Actions

TBD
