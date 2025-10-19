FROM docker.io/debian:forky-slim

LABEL org.opencontainers.image.source=https://github.com/lmichaelis/images
LABEL org.opencontainers.image.description="Debian Forky Slim with Clang-18"
LABEL org.opencontainers.image.licenses=MIT


RUN apt update
RUN apt install -y --no-install-recommends cmake make git clang-18 ca-certificates libclang-rt-18-dev
RUN update-ca-certificates

RUN update-alternatives --install /usr/bin/clang clang /usr/bin/clang-18 50
RUN update-alternatives --install /usr/bin/cc cc /usr/bin/clang-19 50
RUN update-alternatives --install /usr/bin/clang++ clang++ /usr/bin/clang++-18 50
RUN update-alternatives --install /usr/bin/c++ c++ /usr/bin/clang++-18 50

ENTRYPOINT ["bash"]
