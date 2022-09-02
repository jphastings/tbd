# The version of Go used to compile tamago-go
ARG GO_VERSION=1.18.1

FROM multiarch/crossbuild

RUN curl -L https://github.com/f-secure-foundry/tamago-go/releases/download/tamago-go${GO_VERSION}/tamago-go${GO_VERSION}.linux-amd64.tar.gz | tar -zxf - -C /
ENV TAMAGO=/usr/local/tamago-go/bin/go

ENV CROSS_TRIPLE=arm-linux-gnueabi
COPY . /tbd/

ENTRYPOINT ["crossbuild", "/tbd/build.sh"]
CMD ["."]
