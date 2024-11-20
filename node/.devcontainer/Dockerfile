# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.187.0/containers/typescript-node/.devcontainer/base.Dockerfile

# [Choice] Node.js version: 16, 14, 12
ARG VARIANT="16-buster"
FROM mcr.microsoft.com/vscode/devcontainers/typescript-node:${VARIANT}

# [Optional] Uncomment this section to install additional OS packages.
RUN sed -i 's/deb.debian.org/mirrors.aliyun.com/; s/security.debian.org/mirrors.aliyun.com/' /etc/apt/sources.list.d/debian.sources \
    && apt-get update \
    && npm config set registry https://registry.npmmirror.com \
    && yarn config set registry https://registry.npmmirror.com
    
# [Optional] Uncomment if you want to install an additional version of node using nvm
# ARG EXTRA_NODE_VERSION=10
# RUN su node -c "source /usr/local/share/nvm/nvm.sh && nvm install ${EXTRA_NODE_VERSION}"

# [Optional] Uncomment if you want to install more global node packages
# RUN su node -c "npm install -g <your-package-list -here>"
