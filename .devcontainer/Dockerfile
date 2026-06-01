FROM mcr.microsoft.com/devcontainers/base:2.0.4-noble

# Install Python and pip
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends python3 python3-pip python3-venv pipx \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

# Install GAM (Google Apps Manager) for the vscode user
USER vscode
RUN pipx install gam7
ENV PATH="/home/vscode/.local/bin:${PATH}"
USER root
