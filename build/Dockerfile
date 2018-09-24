FROM gcc:latest
LABEL maintainer "tuan t. pham <tuan@vt.edu>"

ENV	PKGS="libncurses5-dev make git exuberant-ctags bc libssl-dev bison flex \
	debianutils libelf-dev" \
	DEBIAN_FRONTEND=noninteractive

# gcc base image is Debian
RUN	apt-get update && apt-get -yq dist-upgrade && \
	apt-get install -yq ${PKGS} && \
	apt-get autoremove -yq && \
	apt-get autoclean -yq && \
	rm -fr /tmp/* /var/lib/apt/lists/*

COPY	./build_kernel.sh /

ENTRYPOINT ["/build_kernel.sh"]
