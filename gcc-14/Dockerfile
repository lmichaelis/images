FROM docker.io/debian:trixie-slim

LABEL org.opencontainers.image.source=https://github.com/lmichaelis/images
LABEL org.opencontainers.image.description="Debian Trixie Slim with GCC-14"
LABEL org.opencontainers.image.licenses=MIT

RUN apt update
RUN apt install -y --no-install-recommends cmake make git gcc-14 g++-14 ca-certificates
RUN update-ca-certificates

RUN update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-14 50
RUN update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-14 50

ENTRYPOINT ["bash"]
