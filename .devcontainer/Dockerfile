FROM mcr.microsoft.com/devcontainers/python:1-3.11-bullseye

# Install system dependencies
RUN apt-get update && apt-get install -y \
    git \
    curl \
    vim \
    && rm -rf /var/lib/apt/lists/*

# Set working directory
WORKDIR /workspace

# Copy requirements and install Python dependencies
COPY requirements.txt .
RUN pip install --upgrade pip && \
    pip install -r requirements.txt

# Create jupyter config directory
RUN mkdir -p /home/vscode/.jupyter

# Set the default user
USER vscode

# Expose ports for Jupyter, Dash, and development servers
EXPOSE 8888 8050 5000

# Default command
CMD ["bash"]