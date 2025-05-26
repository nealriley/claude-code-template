# Use Microsoft’s official JavaScript/Node template for Dev Containers
ARG VARIANT="20-bullseye"
FROM mcr.microsoft.com/vscode/devcontainers/javascript-node:0-${VARIANT}

# Install Zsh and any other dev tools you prefer
RUN apt-get update \
    && apt-get install -y --no-install-recommends zsh fzf git \
    && rm -rf /var/lib/apt/lists/* \
    && chsh -s /usr/bin/zsh vscode

# (Optional) Install additional global npm tools here

# The Claude Code Dev Container Feature will install the @anthropic-ai/claude-code CLI
# No need to install it manually in the Dockerfile :contentReference[oaicite:6]{index=6} :contentReference[oaicite:7]{index=7}.
