FROM quay.io/jupyter/all-spark-notebook
LABEL MAINTAINER="Yudha H T"
USER root
RUN pip install spylon-kernel && \
    python -m spylon_kernel install --user
RUN apt update && apt install -y netcat && \
    apt clean
USER jovyan
