FROM python:3.5-alpine
MAINTAINER thapakazi

WORKDIR "/app"

RUN apk add --no-cache --virtual .build-deps \
    	gcc \
	make \
	musl-dev \
	linux-headers \
	g++ \
	postgresql-dev \
	libpq \
	git \
	libxml2-dev libxslt-dev \
	bash && sed -i -e "s/bin\/ash/bin\/bash/" /etc/passwd

ENV LC_ALL=en_US.UTF-8

CMD ["pip","--version"]
