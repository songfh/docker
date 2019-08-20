FROM ubuntu:16.04

RUN apt-get update \
    && apt-get install -y software-properties-common \
    && add-apt-repository ppa:jonathonf/python-3.6 \
    && apt-get update \
    && apt-get install --no-install-recommends --no-install-suggests -y vim nginx redis-server python3.6 python3.6-dev uwsgi uwsgi-src uuid-dev libcap-dev libpcre3-dev \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

COPY requirements.txt /tmp/
RUN pip install -r /tmp/requirements.txt
