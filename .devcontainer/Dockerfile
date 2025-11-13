# Use the official Microsoft dev containers base image
FROM mcr.microsoft.com/devcontainers/base:bookworm

# Install additional packages if needed
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
    curl \
    git \
    wget \
    vim \
    && apt-get autoremove -y \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/*

# The docker-in-docker feature will handle Docker installation
# This dockerfile mainly serves as a base for additional customizations

# Set up the workspace
WORKDIR /workspace

# Optional: Install any additional development tools
# RUN npm install -g @angular/cli
# RUN pip install --user some-python-package
