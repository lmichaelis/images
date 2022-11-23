FROM docker.io/debian:bullseye-slim

LABEL org.opencontainers.image.source=https://github.com/lmichaelis/images
LABEL org.opencontainers.image.description="Debian Bullseye Slim with Clang-11"
LABEL org.opencontainers.image.licenses=MIT


RUN apt update
RUN apt install -y --no-install-recommends cmake make git clang-11 ca-certificates
RUN update-ca-certificates

ENTRYPOINT ["bash"]
