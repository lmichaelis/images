FROM docker.io/debian:bullseye-slim

LABEL org.opencontainers.image.source=https://github.com/lmichaelis/images
LABEL org.opencontainers.image.description="Debian Bullseye Slim with GCC-9"
LABEL org.opencontainers.image.licenses=MIT

RUN apt update
RUN apt install -y --no-install-recommends cmake make git gcc-9 g++-9 ca-certificates
RUN update-ca-certificates

RUN update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-9 50
RUN update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-9 50

ENTRYPOINT ["bash"]
