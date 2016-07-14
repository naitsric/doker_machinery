FROM ysaotome/ubuntu:14.04

MAINTAINER Cristian Duque <anticris9303@gmail.com>


# Install go tarball
ENV GOLANG_VERSION 1.6.2
RUN wget -qO- http://golang.org/dl/go${GOLANG_VERSION}.linux-amd64.tar.gz | tar -C /usr/local -xzf -

# Set user
ENV HOME /root
ENV GOPATH ${HOME}/go
ENV PATH ${PATH}:${GOPATH}/bin:/usr/local/go/bin
RUN touch ${HOME}/.zshrc
WORKDIR ${HOME}

# Install machinery
RUN go get github.com/RichardKnop/machinery

EXPOSE 9000
VOLUME ${GOPATH}/src
WORKDIR ${GOPATH}/src
