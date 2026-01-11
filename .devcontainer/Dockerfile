FROM nvidia/cuda:13.1.0-base-ubuntu24.04

# Non-interactive + timezone
ENV DEBIAN_FRONTEND=noninteractive
ENV TZ=America/Los_Angeles

RUN ln -fs /usr/share/zoneinfo/$TZ /etc/localtime && \
    echo $TZ > /etc/timezone

# System dependencies
RUN apt-get update && apt-get install -y \
    python3.12 \
    python3.12-venv \
    python3-pip \
    git \
    curl \
    ca-certificates \
    && rm -rf /var/lib/apt/lists/*

# Create a virtual environment
RUN python3.12 -m venv /opt/venv

# Copy requirements.txt into the container
COPY ./requirements.txt /tmp/requirements.txt

# Upgrade pip and install all dependencies from requirements.txt
RUN /opt/venv/bin/pip install --upgrade pip \
 && /opt/venv/bin/pip install -r /tmp/requirements.txt

# Register the venv as a Jupyter kernel automatically
RUN /opt/venv/bin/python -m ipykernel install --user \
    --name devcontainer-venv \
    --display-name "Python (devcontainer venv)"

# Set the venv as default Python
ENV PATH="/opt/venv/bin:$PATH"
