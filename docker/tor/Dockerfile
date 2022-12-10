FROM alpine:latest

HEALTHCHECK --interval=30s --timeout=4s CMD sh -c "[[ $(curl --socks5 127.0.0.1:9050 https://check.torproject.org/api/ip) =~ "true" ]] || exit 1"

RUN apk update
RUN apk add --no-cache tor

COPY torrc /etc/tor/torrc
RUN chown -R tor /etc/tor

USER tor

ENTRYPOINT ["tor"]

CMD ["-f", "/etc/tor/torrc"]