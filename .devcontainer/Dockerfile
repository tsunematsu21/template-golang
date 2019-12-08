FROM golang:1.13.5-buster

ENV DEBIAN_FRONTEND=noninteractive

# Install debian packages
RUN apt-get update \
 && apt-get install -y --no-install-recommends \
    apt-utils \
    dialog \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

ENV GO111MODULE=on

# Install go packages
RUN go get golang.org/x/tools/gopls@latest
