FROM docker.io/debian:forky-slim

LABEL org.opencontainers.image.source=https://github.com/lmichaelis/images
LABEL org.opencontainers.image.description="Debian Forky Slim with GCC-15"
LABEL org.opencontainers.image.licenses=MIT

RUN apt update
RUN apt install -y --no-install-recommends cmake make git gcc-15 g++-15 ca-certificates
RUN update-ca-certificates

RUN update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-15 50
RUN update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-15 50

ENTRYPOINT ["bash"]
