FROM redhat/ubi9-micro:9.4

RUN dnf update \
    && dnf install --assumeyes --allowerasing curl xz \
    && useradd -m nixuser \
    && mkdir /nix \
    && chown nixuser /nix \
    && dnf clean all

USER nixuser
ENV USER=nixuser
ENV PATH="/home/nixuser/.nix-profile/bin:${PATH}"
RUN curl -sL https://nixos.org/nix/install | sh -s -- --no-daemon

RUN nix
