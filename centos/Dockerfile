#
# DOCKER-VERSION    1.7.1
#
# 自动构建centos7基础镜像的Dockerfile
#:
FROM       daocloud.io/library/centos:latest
MAINTAINER yybirdcf <haipengchencf@gmail.com>

ENV TZ "Asia/Shanghai"
ENV TERM xterm

ADD aliyun-mirror.repo /etc/yum.repos.d/CentOS-Base.repo
ADD aliyun-epel.repo /etc/yum.repos.d/epel.repo

RUN yum install -y curl wget tar bzip2 unzip vim-enhanced passwd sudo yum-utils hostname net-tools rsync man && \
    yum install -y gcc gcc-c++ git make automake cmake patch logrotate python-devel libpng-devel libjpeg-devel && \
    yum install -y --enablerepo=epel pwgen python-pip && \
    yum clean all

EXPOSE 22

ENTRYPOINT ["/bin/bash"]
