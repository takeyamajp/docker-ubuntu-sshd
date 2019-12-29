# docker-ubuntu-sshd
[![Docker Stars](https://img.shields.io/docker/stars/takeyamajp/centos-ubuntu.svg)](https://hub.docker.com/r/takeyamajp/ubuntu-sshd/)
[![Docker Pulls](https://img.shields.io/docker/pulls/takeyamajp/ubuntu-sshd.svg)](https://hub.docker.com/r/takeyamajp/ubuntu-sshd/)
[![license](https://img.shields.io/github/license/takeyamajp/docker-ubuntu-sshd.svg)](https://github.com/takeyamajp/docker-ubuntu-sshd/blob/master/LICENSE)

### Supported tags and respective Dockerfile links  
- [`latest`, `ubuntu18.04`](https://github.com/takeyamajp/docker-centos-sshd/blob/master/ubuntu18.04/Dockerfile)

### Image summary
    FROM ubuntu:18.04  
    MAINTAINER "Hiroki Takeyama"
    
    # timezone  
    ENV TZ Asia/Tokyo
    
    ENV ROOT_PASSWORD root
    
    EXPOSE 22
