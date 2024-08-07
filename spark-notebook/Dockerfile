FROM quay.io/jupyter/all-spark-notebook
RUN pip install spylon-kernel
USER jovyan
RUN python -m spylon_kernel install --user
