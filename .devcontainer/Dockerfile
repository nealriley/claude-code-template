# Official VS Code Dev Containers Node 20 image (includes 'node' user)
ARG VARIANT="20-bullseye"
FROM mcr.microsoft.com/vscode/devcontainers/javascript-node:0-${VARIANT}

# Install Zsh, fzf, git, then set Zsh as the login shell for 'node'
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
         zsh fzf git \
    && rm -rf /var/lib/apt/lists/* \
    && chsh -s /usr/bin/zsh node

RUN npm install -g @anthropic-ai/claude-code

# The Claude Code Dev Container Feature installs the @anthropic-ai/claude-code CLI automatically
