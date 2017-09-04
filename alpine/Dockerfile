FROM alpine:edge
LABEL maintainer="Stéphane BARON <sbaron@galilee.fr>"

RUN apk add --no-cache \
		bash \
		shadow \
		openssh-client \
		rsync \
	&& chsh -s /bin/bash

RUN mkdir -p /root/.ssh
COPY resources/ssh_config /root/.ssh/config

COPY resources/entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]