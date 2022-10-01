FROM rust

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get -q update \
  && apt-get -q -y install --no-install-recommends \
    git \
    httpie \
    curl \
    htop \
    jq \
    mc \
    nano \
    netcat \
    net-tools \
    libsecret-1-dev \
    python2.7 \
    clang \
    cmake \
    wget \
    build-essential

RUN curl -sL https://deb.nodesource.com/setup_14.x | bash -

RUN apt-get -q update \
  && apt-get -q -y install --no-install-recommends \
    nodejs httpie


RUN npm install -g yarn

RUN npm install -g nan

RUN npm i -g @graphprotocol/indexer-cli@0.19.3 --registry https://registry.npmjs.org/ --unsafe-perm=true

RUN npm i -g @graphprotocol/graph-cli --registry https://registry.npmjs.org/ --unsafe-perm=true

RUN mkdir "/root/.config/graph-cli/"

RUN echo 'api = "http://indexer-agent:18000/"' >> "/root/.config/graph-cli/indexing.toml"

ENTRYPOINT [ "cat" ]
