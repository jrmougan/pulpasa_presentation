# Keep in sync with mise.toml ([tools] node / pnpm).
FROM node:26.13.1

# Install basic development tools
RUN apt update && apt install -y less man-db sudo

# Ensure default `node` user has access to `sudo`
ARG USERNAME=node
RUN echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
    && chmod 0440 /etc/sudoers.d/$USERNAME

# Pinned pnpm (same as packageManager in package.json); npm stays the bundled one.
RUN npm install -g pnpm@11.28.12

# Set `DEVCONTAINER` environment variable to help with orientation
ENV DEVCONTAINER=true
