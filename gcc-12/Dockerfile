FROM docker.io/debian:bookworm-slim

LABEL org.opencontainers.image.source=https://github.com/lmichaelis/images
LABEL org.opencontainers.image.description="Debian Bookworm Slim with GCC-12"
LABEL org.opencontainers.image.licenses=MIT

RUN apt update
RUN apt install -y --no-install-recommends cmake make git gcc-12 g++-12 ca-certificates
RUN update-ca-certificates

RUN update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-12 50
RUN update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-12 50

ENTRYPOINT ["bash"]
