# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.187.0/containers/debian/.devcontainer/base.Dockerfile

# [Choice] Debian version: buster, stretch
ARG VARIANT="buster"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-${VARIANT}

# ** [Optional] Uncomment this section to install additional packages. **
RUN sed -i 's/deb.debian.org/mirrors.aliyun.com/; s/security.debian.org/mirrors.aliyun.com/' /etc/apt/sources.list \
    && apt-get update

