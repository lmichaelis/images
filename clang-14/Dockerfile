FROM docker.io/debian:bookworm-slim

LABEL org.opencontainers.image.source=https://github.com/lmichaelis/images
LABEL org.opencontainers.image.description="Debian Bookworm Slim with Clang-14"
LABEL org.opencontainers.image.licenses=MIT


RUN apt update
RUN apt install -y --no-install-recommends cmake make git clang-14 ca-certificates
RUN update-ca-certificates

RUN update-alternatives --install /usr/bin/clang clang /usr/bin/clang-14 50
RUN update-alternatives --install /usr/bin/cc cc /usr/bin/clang-14 50
RUN update-alternatives --install /usr/bin/clang++ clang++ /usr/bin/clang++-14 50
RUN update-alternatives --install /usr/bin/c++ c++ /usr/bin/clang++-14 50

ENTRYPOINT ["bash"]
