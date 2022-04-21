FROM alpine:3.14

ENV PYTHONUNBUFFERED=1

RUN apk add --no-cache g++ libx11 libxrender libxext fontconfig freetype build-base

# Install python/pip
RUN apk add --update --no-cache python3 python3-dev && \
    ln -sf python3 /usr/bin/python && \
    python3 -m ensurepip && \
    pip3 install --no-cache --upgrade pip setuptools && \
    pip install wheel numpy matplotlib