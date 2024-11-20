# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.148.1/containers/cpp/.devcontainer/base.Dockerfile

# [Choice] Debian / Ubuntu version: debian-10, debian-9, ubuntu-20.04, ubuntu-18.04
ARG VARIANT="buster"
FROM mcr.microsoft.com/vscode/devcontainers/cpp:${VARIANT}

# [Optional] Uncomment this section to install additional packages.
RUN sed -i 's/deb.debian.org/mirrors.aliyun.com/; s/security.debian.org/mirrors.aliyun.com/' /etc/apt/sources.list.d/debian.sources \
    && apt-get update