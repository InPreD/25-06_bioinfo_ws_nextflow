FROM nfcore/gitpod:3.2.0
USER root
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        fish=3.3.1+ds-3 \
        fuse-overlayfs=1.7.1-1 \
        silversearcher-ag=2.2.0+git20200805-1 \
    && echo "LC_ALL=en_US.UTF-8" > /etc/default/locale \
    && locale-gen en_US.UTF-8 \
    && apt-get clean \
    && rm -Rf /usr/share/doc && rm -Rf /usr/share/man \
    && rm -rf /var/lib/apt/lists/* \
    && usermod -s /usr/bin/fish root