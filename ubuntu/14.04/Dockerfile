FROM ubuntu:14.04
ENV UBUNTU_VERSION=14.04

RUN apt-get update \
 && apt-get install -y --no-install-recommends \
        software-properties-common \
 && apt-add-repository ppa:git-core/ppa \
 && apt-get update \
 && apt-get install -y --no-install-recommends \
        curl \
        git \
        jq \
        libcurl3 \
        libicu52 \
        libunwind8 \
 && rm -rf /var/lib/apt/lists/*

WORKDIR /vsts

COPY ./start.sh .
RUN chmod +x start.sh

CMD ["./start.sh"]
