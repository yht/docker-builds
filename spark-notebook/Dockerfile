FROM quay.io/jupyter/all-spark-notebook:spark-4.0.0
LABEL MAINTAINER="Yudha H T"

USER root
RUN apt-get update && \
    apt-get install -y netcat-openbsd && \
    rm -rf /var/lib/apt/lists/* && \
    chown -R ${NB_UID}:${NB_GID} /home/jovyan
RUN mkdir -p /work && \
    chown -R ${NB_UID}:${NB_GID} /work
USER ${NB_UID}
WORKDIR /work
