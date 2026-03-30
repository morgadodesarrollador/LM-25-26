FROM ubuntu:22.04

RUN apt update && apt install -y curl ca-certificates

RUN curl -sSf https://install.spacetimedb.com | bash

ENV PATH="/root/.local/bin:${PATH}"

WORKDIR /data

EXPOSE 3000

CMD ["sh", "-c", "spacetime init && spacetime start"]