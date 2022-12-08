FROM docker.io/debian:bullseye-slim

LABEL org.opencontainers.image.source=https://github.com/lmichaelis/images
LABEL org.opencontainers.image.description="Debian Bullseye Slim with MinGW-w64 10.2.1"
LABEL org.opencontainers.image.licenses=MIT

RUN apt update
RUN apt install -y --no-install-recommends cmake make git g++-mingw-w64-x86-64 gcc-mingw-w64-x86-64 ca-certificates
RUN update-ca-certificates

RUN update-alternatives --install /usr/bin/cc cc /usr/bin/x86_64-w64-mingw32-g++-win32 50
RUN update-alternatives --install /usr/bin/c++ c++ /usr/bin/x86_64-w64-mingw32-g++-win32 50

ENTRYPOINT ["bash"]
