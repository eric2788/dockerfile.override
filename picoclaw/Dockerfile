# Pin to a specific digest for reproducible builds, or update the tag as needed.
FROM sipeed/picoclaw:latest

USER root

# Install curl, Node.js, npm via apk, and uv via the official installer script.
RUN apk add --no-cache curl nodejs npm && \
    curl -LsSf https://astral.sh/uv/install.sh | UV_INSTALL_DIR=/usr/local/bin sh

# Validate each installed tool is present and directly usable.
RUN curl --version && \
    node --version && \
    npm --version && \
    uv --version
