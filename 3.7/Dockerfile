FROM python:3.7-alpine3.9
MAINTAINER thapakazi

WORKDIR "/app"

RUN apk add --no-cache --virtual .build-deps \
	gcc \
        g++ && \ 
    apk add --no-cache --virtual .build-run \
        postgresql-dev \
	libpq \
        make \	
	git \
        py-lxml \
	bash && sed -i -e "s/bin\/ash/bin\/bash/" /etc/passwd

ENV LC_ALL=en_US.UTF-8

# copy the generic requirement
COPY requirements.txt /tmp

RUN pip install --no-cache-dir --requirement /tmp/requirements.txt
CMD ["pip","--version"]
