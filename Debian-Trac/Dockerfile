FROM debian:jessie
COPY start.sh /start.sh
RUN apt-get update && \
  apt-get install -y apt-utils gcc \
    python2.7 python2.7-dev python-setuptools \
    python-sqlite \
    git && \
  apt-get autoremove -y && \
  apt-get clean
RUN easy_install Genshi && \
  easy_install Trac
EXPOSE 8000
VOLUME /srv/trac
CMD ["/start.sh"]
