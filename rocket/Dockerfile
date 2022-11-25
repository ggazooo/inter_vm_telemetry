FROM alpine:3.17

RUN apk update
RUN apk add nfs-utils

WORKDIR /rocket
COPY . .

RUN /rocket/setup_nfs-server.sh

CMD ["/bin/sh", "hello_rocket.sh"]
