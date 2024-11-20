# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.145.1/containers/rust/.devcontainer/base.Dockerfile
ARG VARIANT="1"
FROM mcr.microsoft.com/vscode/devcontainers/rust:${VARIANT}

ENV RUSTUP_DIST_SERVER=https://mirrors.ustc.edu.cn/rust-static
# ENV RUSTUP_DIST_SERVER=https://mirrors.tuna.tsinghua.edu.cn/rustup
ENV RUSTUP_UPDATE_ROOT=https://mirrors.ustc.edu.cn/rust-static/rustup
ENV CARGO_SOURCE_CRATES-IO_REPLACE-WITH=ustc
ENV CARGO_SOURCE_USTC_REGISTRY=git://mirrors.ustc.edu.cn/crates.io-index

RUN sed -i 's/deb.debian.org/mirrors.aliyun.com/; s/security.debian.org/mirrors.aliyun.com/' /etc/apt/sources.list.d/debian.sources \
    && apt-get update

# [Optional] Uncomment this section to install additional packages.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>
