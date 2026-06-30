FROM quay.io/jupyter/all-spark-notebook:spark-3.5.2
LABEL MAINTAINER="Yudha H T"

USER root
RUN pip install --no-cache-dir \
    git+https://github.com/vericast/spylon-kernel.git
RUN apt-get update && \
    apt-get install -y netcat-openbsd && \
    rm -rf /var/lib/apt/lists/* && \
    chown -R ${NB_UID}:${NB_GID} /home/jovyan
RUN mkdir -p /work && \
    chown -R ${NB_UID}:${NB_GID} /work
RUN python -m spylon_kernel install --sys-prefix && \
    chown -R ${NB_UID}:${NB_GID} /home/jovyan && \
    chmod -R u+rwX /home/jovyan
USER ${NB_UID}
WORKDIR /work
