# docker-pritunl

[![Build Status](https://travis-ci.org/h0tbird/docker-pritunl.svg?branch=master)](https://travis-ci.org/h0tbird/docker-pritunl)

Containerized Pritunl service.

##### 1. Mongodb:

```
docker run -it --rm \
--net host --name mongo \
--volume /var/lib/mongo:/data/db \
mongo:3.2 \
--bind_ip 127.0.0.1
```

##### 2. Pritunl:

```
docker run -it --rm \
--privileged \
--net host --name pritunl \
--env MONGODB_URI=mongodb://127.0.0.1:27017/pritunl \
h0tbird/pritunl:latest
```
