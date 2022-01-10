# Teradici Docker

## Usage

### The "zero" extra-dependency way

Well, you still need docker.

```console
$ docker build -t pcoip-client --build-arg username=$LOGNAME --build-arg uid=$(id -u) --build-arg gid=$(id -g) .
$ docker run --rm -e DISPLAY=$DISPLAY -e LOGNAME=$LOGNAME -v /home/$LOGNAME/.config/:/home/$LOGNAME/.config/ -v /tmp/.X11-unix:/tmp/.X11-unix pcoip-client
```

### The `docker-compose` way

Run with `docker-compose up -d`

