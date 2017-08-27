FROM python:3.5-alpine
MAINTAINER thapakazi

WORKDIR "/app"

RUN apk add --no-cache --virtual .build-deps \
    	gcc \
	musl-dev \
	linux-headers \
	g++ \
	postgresql-dev \
	libpq 

CMD ["pip" "--version"]
