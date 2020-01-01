# ubuntu-sshd
[![Docker Stars](https://img.shields.io/docker/stars/takeyamajp/ubuntu-sshd.svg)](https://hub.docker.com/r/takeyamajp/ubuntu-sshd/)
[![Docker Pulls](https://img.shields.io/docker/pulls/takeyamajp/ubuntu-sshd.svg)](https://hub.docker.com/r/takeyamajp/ubuntu-sshd/)
[![license](https://img.shields.io/github/license/takeyamajp/docker-ubuntu-sshd.svg)](https://github.com/takeyamajp/docker-ubuntu-sshd/blob/master/LICENSE)

### Supported tags and respective Dockerfile links  
- [`latest`, `ubuntu18.04`](https://github.com/takeyamajp/docker-ubuntu-sshd/blob/master/ubuntu18.04/Dockerfile)
- [`ubuntu16.04`](https://github.com/takeyamajp/docker-ubuntu-sshd/blob/master/ubuntu16.04/Dockerfile)

### Image summary
    FROM ubuntu:18.04  
    MAINTAINER "Hiroki Takeyama"
    
    ENV TZ Asia/Tokyo
    
    ENV ROOT_PASSWORD root
    
    EXPOSE 22

## How to use
This container can be accessed by SSH and SFTP clients.

    docker run -d --name ubuntu-sshd \  
           -e TIMEZONE=Asia/Tokyo \  
           -e ROOT_PASSWORD=root \  
           -p 8023:22 \  
           takeyamajp/ubuntu-sshd

## Timezone
You can use any time zone that can be used in Ubuntu such as America/Chicago.  

See below for zones.  
https://www.unicode.org/cldr/charts/latest/verify/zones/en.html

## Logging
This container logs the beginning, authentication, and termination of each connection.

Use the following command to view the logs in real time.

    docker logs -f postfix
