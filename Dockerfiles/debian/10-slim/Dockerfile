FROM wolfsoftwareltd/goenv-debian:buster-slim

RUN \
	VERSION=$(goenv install -l | sed -n '/^[[:space:]]*[0-9]\{1,\}\.[0-9]\{1,\}\.[0-9]\{1,\}[[:space:]]*$/ h;${g;p;}') && \
	goenv install ${VERSION} && \
	goenv global ${VERSION}

WORKDIR /root

ENTRYPOINT ["/bin/bash"]

