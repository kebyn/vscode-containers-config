# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.155.1/containers/go/.devcontainer/base.Dockerfile

# [Choice] Go version: 1, 1.15, 1.14
ARG VARIANT="1"
FROM mcr.microsoft.com/vscode/devcontainers/go:${VARIANT}

# [Option] Install Node.js
ARG INSTALL_NODE="true"
ARG NODE_VERSION="lts/*"
RUN if [ "${INSTALL_NODE}" = "true" ]; then su vscode -c "umask 0002 && . /usr/local/share/nvm/nvm.sh && nvm install ${NODE_VERSION} 2>&1"; fi

ENV GO111MODULE=on
ENV GOPROXY=https://goproxy.cn

RUN sed -i 's/deb.debian.org/mirrors.aliyun.com/; s/security.debian.org/mirrors.aliyun.com/' /etc/apt/sources.list.d/debian.sources \
    && apt-get update \
    && npm config set registry https://registry.npmmirror.com \
    && yarn config set registry https://registry.npmmirror.com
    
# [Optional] Uncomment this section to install additional OS packages.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>

# [Optional] Uncomment the next line to use go get to install anything else you need
# RUN go get -x <your-dependency-or-tool>

# [Optional] Uncomment this line to install global node packages.
# RUN su vscode -c "source /usr/local/share/nvm/nvm.sh && npm install -g <your-package-here>" 2>&1