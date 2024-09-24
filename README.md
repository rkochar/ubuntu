# ubuntu

A repository to publish and release images Ubuntu that solve the chicken-and-egg problem of certs required for `apt update` inside a "secure" corporate network. The images are published to [Docker Hub](https://hub.docker.com/r/rkochar/ubuntu).

- The default lts image installs `ca-certificates` so that certificates can simply be mounted and installed with `update-ca-certificates`.
- The nix image installs nix onto a Ubuntu lts image.
