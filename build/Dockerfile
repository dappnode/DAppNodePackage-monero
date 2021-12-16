FROM debian:bullseye-slim as build

ARG UPSTREAM_VERSION
ENV FILENAME monero-linux-x64-${UPSTREAM_VERSION}.tar.bz2
ENV DOWNLOAD_URL https://downloads.getmonero.org/cli/${FILENAME}
ENV SHA256SUM 0fb6f53b7b9b3b205151c652b6c9ca7e735f80bfe78427d1061f042723ee6381

RUN apt update && \
    apt install -y --assume-yes --no-install-recommends curl ca-certificates bzip2 && \
    curl https://downloads.getmonero.org/cli/monero-linux-x64-${UPSTREAM_VERSION}.tar.bz2 -o monero-linux-x64-${UPSTREAM_VERSION}.tar.bz2 && \
    tar --strip-components=1 -C /usr/bin -jxvf monero-linux-x64-${UPSTREAM_VERSION}.tar.bz2

FROM debian:bullseye-slim

COPY --from=build /usr/bin/monerod /usr/bin/monerod

ENTRYPOINT monerod --p2p-bind-ip=0.0.0.0 --p2p-bind-port=18080 --rpc-bind-ip=0.0.0.0 --rpc-bind-port=18081 --non-interactive --confirm-external-bind $EXTRA_FLAGS
