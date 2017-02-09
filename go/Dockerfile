#
#
# 基于centos7基础镜像的go环境(1.7.3版本)
#:
FROM       yybirdcf/centos:v1
MAINTAINER yybirdcf <haipengchencf@gmail.com>

ENV TZ "Asia/Shanghai"
ENV TERM xterm

ADD go1.7.5.linux-amd64.tar.gz /tmp

RUN cp -R /tmp/go /usr/local
RUN mkdir -p /home/go

ENV GOROOT /usr/local/go
ENV GOBIN $GOROOT/bin
ENV PATH $PATH:$GOBIN
ENV GOPATH  /home/go

RUN go version

RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"

EXPOSE 22

ENTRYPOINT ["/bin/bash"]
