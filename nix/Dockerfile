FROM ubuntu:24.04

RUN apt update \
    && apt install -y ca-certificates curl xz-utils \
    && /sbin/useradd -m nixuser \ 
    && mkdir /nix \
    && chown nixuser /nix \
    && apt clean

USER nixuser
ENV USER=nixuser
ENV PATH="/home/nixuser/.nix-profile/bin:${PATH}"
RUN curl -sL https://nixos.org/nix/install | sh -s -- --no-daemon
