FROM python:latest

RUN mkdir -p /usr/src/client
WORKDIR /usr/src/client

ONBUILD COPY requirements.txt /usr/src/client/
ONBUILD RUN pip install --no-cache-dir -r requirements.txt

ONBUILD COPY . /usr/src/client