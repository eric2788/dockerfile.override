# Pin to a specific digest for reproducible builds, or update the tag as needed.
FROM sipeed/picoclaw:nightly-launcher

USER root

# Install curl, Node.js, npm, python3 via apk, and uv via the official installer script.
RUN apk add --no-cache curl nodejs npm python3 && \
    curl -LsSf https://astral.sh/uv/install.sh | UV_INSTALL_DIR=/usr/local/bin sh

# Validate each installed tool is present and directly usable.
RUN curl --version && \
    node --version && \
    npm --version && \
    python3 --version && \
    uv --version
