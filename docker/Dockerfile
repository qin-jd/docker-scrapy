FROM python:2.7-jessie

RUN apt-get update -qq && \
    apt-get install -qy \
        netbase ca-certificates apt-transport-https \
        build-essential locales \
        libxml2-dev \
        libssl-dev \
        libxslt1-dev \
        libmysqlclient-dev \
        libpq-dev \
        libevent-dev \
        libffi-dev \
        libpcre3-dev \
        libz-dev \
        unixodbc unixodbc-dev \
        telnet vim htop iputils-ping curl wget lsof git sudo \
        ghostscript && \
        pip install --upgrade pip

COPY requirements.txt /requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

RUN mkdir /app
WORKDIR /app


CMD ["scrapy"]
