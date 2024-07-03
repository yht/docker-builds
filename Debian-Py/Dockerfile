FROM ryht/debian:bookworm
RUN apt-get update && apt-get upgrade -y && \
 apt-get install -y \
  git-core \
  python3 python3-dev libpq-dev python3-setuptools python3-pip python3-virtualenv && \
 apt-get autoremove -y && \
 apt-get clean
CMD ["/bin/bash"]
