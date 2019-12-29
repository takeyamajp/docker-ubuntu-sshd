FROM ubuntu:18.04
MAINTAINER "Hiroki Takeyama"

# sshd
RUN mkdir /run/sshd;\
    apt update;\
    apt install -y openssh-server; \
    sed -i 's/^#\(PermitRootLogin\s*\).*/\1 yes/' /etc/ssh/sshd_config;\
    apt clean;

# entrypoint
RUN { \
    echo '#!/bin/bash -eu'; \
    echo 'echo "root:${ROOT_PASSWORD}" | chpasswd'; \
    echo 'exec "$@"'; \
    } > /usr/local/bin/entry_point.sh; \
    chmod +x /usr/local/bin/entry_point.sh;
ENTRYPOINT ["entry_point.sh"]

# timezone
ENV TZ Asia/Tokyo

ENV ROOT_PASSWORD root

EXPOSE 22

CMD    ["/usr/sbin/sshd", "-D"]
