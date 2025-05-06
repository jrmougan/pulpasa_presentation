FROM node:22

# Install basic development tools
RUN apt update && apt install -y less man-db sudo

# Ensure default `node` user has access to `sudo`
ARG USERNAME=node
RUN echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
    && chmod 0440 /etc/sudoers.d/$USERNAME

# update npm to the latest version
RUN npm install -g npm@latest
# Install pnpm
RUN npm install -g pnpm

# Set `DEVCONTAINER` environment variable to help with orientation
ENV DEVCONTAINER=true
