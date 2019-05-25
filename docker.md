# Docker

## frequency commands
```
# when want to research in ubuntu
docker run -it ubuntu /bin/bash
```

## Go Build

It is standard for using GOPATH rather than /go?

```
# Build Stage
FROM golang:1.12.5 AS builder
ENV REPOSITORY github.com/laqiiz/<xxx-app>
ADD . $GOPATH/src/$REPOSITORY
WORKDIR $GOPATH/src/$REPOSITORY
RUN GO111MODULE=on GOOS=linux GOARCH=amd64 CGO_ENABLED=0 go build -ldflags '-s -w' -a -installsuffix cgo -o /main main.go

# Runtime Stage
FROM alpine:3.9.4
RUN apk add --no-cache ca-certificates
COPY --from=builder /main .
CMD ["./main", "--host", "0.0.0.0"]

EXPOSE <your expose port number>
```

## Mount

* Windows must start /c
* `-v` path is absolute path
* `ro` is readonly, defalut read-write

```
# Mount
docker run -v /c/Users/laqiiz/Desktop/<any config dir>:/conf:ro alpine

# Mount trouble shooting
docker run -it -v /c/Users/laqiiz/Desktop/<any config dir>:/conf:ro alpine /bin/sh
```


## Actually I made a mistake

* CMD in Dockerfile

```sh
CMD ["./main", "--host 0.0.0.0"]
↓↓↓
unknown flag `host 0.0.0.0'

CMD ["./main", "--host", "0.0.0.0"]
↓↓↓
OK
```
