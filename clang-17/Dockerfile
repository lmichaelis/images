FROM docker.io/debian:trixie-slim

LABEL org.opencontainers.image.source=https://github.com/lmichaelis/images
LABEL org.opencontainers.image.description="Debian Forky Slim with Clang-17"
LABEL org.opencontainers.image.licenses=MIT


RUN apt update
RUN apt install -y --no-install-recommends cmake make git clang-17 ca-certificates libclang-rt-17-dev
RUN update-ca-certificates

RUN update-alternatives --install /usr/bin/clang clang /usr/bin/clang-17 50
RUN update-alternatives --install /usr/bin/cc cc /usr/bin/clang-17 50
RUN update-alternatives --install /usr/bin/clang++ clang++ /usr/bin/clang++-17 50
RUN update-alternatives --install /usr/bin/c++ c++ /usr/bin/clang++-17 50

ENTRYPOINT ["bash"]
