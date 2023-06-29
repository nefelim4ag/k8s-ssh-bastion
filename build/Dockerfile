FROM ubuntu:22.04
ENV KUBECTL_VERSION=v1.26.6
RUN apt update && apt install -y curl
RUN set -eux; \
    ARCH=$(dpkg --print-architecture); \
    \
    curl -SL "https://storage.googleapis.com/kubernetes-release/release/${KUBECTL_VERSION}/bin/linux/${ARCH}/kubectl" -o /usr/bin/kubectl; \
    chmod +x /usr/bin/kubectl
FROM ubuntu:22.04

RUN apt update && apt install --no-install-recommends -y openssh-server zsh && apt clean && rm -rf /var/log/* /var/cache/debconf/*-old
COPY --from=0 /usr/bin/kubectl /usr/bin/kubectl
