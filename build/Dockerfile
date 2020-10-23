FROM debian:bullseye-slim as build

ARG MONERO_VERSION=v0.17.0.0
ENV FILENAME monero-linux-x64-${MONERO_VERSION}.tar.bz2
ENV DOWNLOAD_URL https://downloads.getmonero.org/cli/${FILENAME}
ENV SHA256SUM 4113cc92314fefebe52024d67a8b5d6d499adb4c3988f5d2b838ed3f80893874

ADD $DOWNLOAD_URL /$FILENAME
RUN if [ x"$( sha256sum /${FILENAME} | awk '{print $1}' )" != x"${SHA256SUM}" ]; then \
    rm -f /$FILENAME; \
    echo "Checksum verification failed."; \
    exit 1; \
    else \
    apt-get update -y;\
    apt-get install bzip2 -y;\
    tar --strip-components=1 -C /usr/bin -jxvf  /$FILENAME; \
    fi

FROM debian:bullseye-slim

EXPOSE 18081
EXPOSE 18080

COPY --from=build /usr/bin/monerod /usr/bin/monerod

ENTRYPOINT monerod --p2p-bind-ip=0.0.0.0 --p2p-bind-port=18080 --rpc-bind-ip=0.0.0.0 --rpc-bind-port=18081 --non-interactive --confirm-external-bind $EXTRA_FLAGS
