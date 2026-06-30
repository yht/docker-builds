FROM jupyter/all-spark-notebook:spark-3.4.1

LABEL maintainer="Yudha H T"

USER root

# Install Spylon
RUN pip install --no-cache-dir \
    git+https://github.com/vericast/spylon-kernel.git

# Utility
RUN apt-get update && \
    apt-get install -y netcat-openbsd && \
    rm -rf /var/lib/apt/lists/*

# Create spark user
RUN groupadd -g 1001 spark && \
    useradd -m -s /bin/bash -u 1001 -g spark spark

# Workspace
RUN mkdir -p /work

# Install kernel
RUN python -m spylon_kernel install --sys-prefix

# Prepare home directory
RUN mkdir -p /home/spark/.local/share/jupyter && \
    chown -R spark:spark /home/spark && \
    chown -R spark:spark /work

# Jupyter environment
ENV NB_USER=spark
ENV NB_UID=1001
ENV NB_GID=1001
ENV HOME=/home/spark

USER spark

WORKDIR /work
