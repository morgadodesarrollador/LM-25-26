FROM ubuntu:22.04

RUN apt update && apt install -y curl ca-certificates

# Descargar binario directamente (sin script interactivo)
RUN curl -L https://github.com/clockworklabs/SpacetimeDB/releases/latest/download/spacetime-linux-x86_64 \
    -o /usr/local/bin/spacetime && \
    chmod +x /usr/local/bin/spacetime

WORKDIR /data

EXPOSE 3000

CMD ["sh", "-c", "spacetime init || true && spacetime start"]