FROM ubuntu:22.04

RUN apt update && apt install -y curl ca-certificates


# Descargar correctamente desde release API
RUN curl -L https://github.com/clockworklabs/SpacetimeDB/releases/latest/download/spacetime-linux-amd64 \
    -o /usr/local/bin/spacetime && \
    chmod +x /usr/local/bin/spacetime

WORKDIR /data

COPY ./start.sh /root/start.sh
RUN chmod +x /root/start.sh
EXPOSE 3000

# CMD ["sh", "-c", "spacetime init || true && spacetime start"]

ENTRYPOINT [ "/root/start.sh" ]