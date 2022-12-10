FROM alpine:latest

RUN apk update
RUN apk add --no-cache autossh libressl netcat-openbsd

ENTRYPOINT ["/usr/bin/autossh", \
    "-M", "0", "-T", "-N", "-g", "-v", \
    "-oStrictHostKeyChecking=no", \
    "-oServerAliveInterval=180", \
    "-oUserKnownHostsFile=/dev/null", \
    "-oGlobalKnownHostsFile=/dev/null", \
    "-i/id_ed25519"]