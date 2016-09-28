# alpin3/chromium

Chromium browser on Alpine through X11

Image is based on the [openjdk](https://hub.docker.com/_/alpine/) base image

## Docker image size

[![Latest](https://badge.imagelayers.io/alpin3/chromium.svg)](https://imagelayers.io/?images=alpin3/chromium:latest 'latest')

## Docker image usage

```
docker run [docker-options] alpin3/chromium
```

## Examples

Typical usage:

```
XSOCK=/tmp/.X11-unix
XAUTH=/tmp/.docker.xauth
xauth nlist :0 | sed -e 's/^..../ffff/' | xauth -f $XAUTH nmerge -
docker run -v $XSOCK:$XSOCK -v $XAUTH:$XAUTH -e XAUTHORITY=$XAUTH alpin3/chromium
```

### Todo
- [ ] Provide more examples
