# Pin to a specific digest for reproducible builds, or update the tag as needed.
FROM sipeed/picoclaw:latest

USER root

# Install curl, Node.js, npm, and uv (uv available in Alpine community repo since 3.21)
RUN apk add --no-cache curl nodejs npm uv

# Ensure installed binaries are on PATH without requiring manual PATH configuration
ENV PATH="/usr/local/bin:/usr/bin:/bin:${PATH}"
