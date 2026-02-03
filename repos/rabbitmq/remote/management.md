## `rabbitmq:management`

```console
$ docker pull rabbitmq@sha256:9e537169ec1c6b97f13549c6d3a7a4690a6d5be19d7d6cc42c5beb212fce5873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rabbitmq:management` - linux; amd64

```console
$ docker pull rabbitmq@sha256:40d9a2230ba125b81ce26eff2c7a0a9875309c201c790fb20f92f462e2965f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120218779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade3b7416b2e1cbef6a3bb07817e03626d3f7684500bc5fa62b5f7224caf7e1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 21:28:56 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 27 Jan 2026 21:28:56 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 27 Jan 2026 21:28:56 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 27 Jan 2026 21:28:56 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 27 Jan 2026 21:28:56 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:28:56 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:28:57 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 27 Jan 2026 21:28:57 GMT
ENV RABBITMQ_VERSION=4.2.3
# Tue, 27 Jan 2026 21:28:57 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 27 Jan 2026 21:28:57 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 27 Jan 2026 21:28:57 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:29:16 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 27 Jan 2026 21:29:16 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 27 Jan 2026 21:29:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 27 Jan 2026 21:29:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:29:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 27 Jan 2026 21:29:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 27 Jan 2026 21:29:16 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 27 Jan 2026 21:29:17 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 27 Jan 2026 21:29:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Jan 2026 21:29:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Jan 2026 21:29:17 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 27 Jan 2026 21:29:17 GMT
CMD ["rabbitmq-server"]
# Tue, 27 Jan 2026 22:11:57 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 27 Jan 2026 22:12:07 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-gnu'; digest='62e2c22df73b1f8f04bda5630cb9c32cc60ce2fa28487de0337c039625f5cbda' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-gnu'; digest='9ed29731a27d5aeba44fde8a64a55e04592db915028468a428069cefeee0fc29' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 27 Jan 2026 22:12:07 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9b58cdf77318561e2d83b7c0d475fdea02ceaf358472c3da17ba8f28601cd2`  
		Last Modified: Tue, 27 Jan 2026 21:29:39 GMT  
		Size: 46.3 MB (46261576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ee2be5943a705b7a79768d4defa09a5b596d400dc04aeed3406adb34f7cc19`  
		Last Modified: Tue, 27 Jan 2026 21:29:38 GMT  
		Size: 9.0 MB (8985731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd8f6f9aec506982d748ec1d3bf65b2967f79bab0ba9b0726f597c4d0173ad`  
		Last Modified: Tue, 27 Jan 2026 21:29:37 GMT  
		Size: 9.7 KB (9671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e73a54d79465f38bbba356a61b718c5b5b00b8d2230a8e624ef8af11c9bc47a`  
		Last Modified: Tue, 27 Jan 2026 21:29:39 GMT  
		Size: 30.3 MB (30345544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7522a948869f3d6d1ec6281ead420f57124dd660af0a0b96ed781ca60f0e51f`  
		Last Modified: Tue, 27 Jan 2026 21:29:38 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed40e796386d2648a00c1f1622ef063a884e4f0806aecd7d003ef2f387baeba`  
		Last Modified: Tue, 27 Jan 2026 21:29:32 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6374644c041d4d9ae7a6f1e09905921f3028be309d4e2572dc50693981163f6f`  
		Last Modified: Tue, 27 Jan 2026 21:29:39 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815d06b89642337666e28eb9b6a90a832f2fea8636b8cba2d98db07f0892e6aa`  
		Last Modified: Tue, 27 Jan 2026 21:29:39 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0d5cfb0c94e30816b9314e0e2305a8406b9fb562c49e6811e87b7238f8a099`  
		Last Modified: Tue, 27 Jan 2026 22:12:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f6c9adaad5f9ad1a1d5ab1bb0cdee0b808cb033404855f45e76dda0e68fcc0`  
		Last Modified: Tue, 27 Jan 2026 22:12:15 GMT  
		Size: 4.9 MB (4888226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1e328c4d8b942c2172970115320287ea505f503361829d796c7ee9f390fdbf16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0821a73796206d080898f29e808c1b29518668a17dd62f0d3a75b71b2ba4c1`

```dockerfile
```

-	Layers:
	-	`sha256:79af7ac00feade38d4a1e1a0ad38e4e02823e75ee4ce683d57caec838b63e56a`  
		Last Modified: Tue, 27 Jan 2026 22:12:15 GMT  
		Size: 2.5 MB (2486661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56d076b6cda87b62c267fdf4c9439b8360719573ef7ac6643d9801ebbc36ee69`  
		Last Modified: Tue, 27 Jan 2026 22:12:15 GMT  
		Size: 16.3 KB (16269 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:2f94d0e5f3591b428b22b64c08455ecb2a7848c6d0db4d5822bbf5654d45f2a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97091254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad1d7d024c0f2300683c3e947d5881e881899751246a9fe061ed498ff0851bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:59 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:02 GMT
ADD file:9e6534a5b837dcbcc4b9596878a4feeb07210fb34c7385aeee0217ff03c2460e in / 
# Tue, 13 Jan 2026 05:40:03 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 21:26:56 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 27 Jan 2026 21:26:56 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 27 Jan 2026 21:26:56 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 27 Jan 2026 21:26:56 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 27 Jan 2026 21:26:56 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:26:56 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:26:57 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 27 Jan 2026 21:26:57 GMT
ENV RABBITMQ_VERSION=4.2.3
# Tue, 27 Jan 2026 21:26:57 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 27 Jan 2026 21:26:57 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 27 Jan 2026 21:26:57 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:27:20 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 27 Jan 2026 21:27:21 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 27 Jan 2026 21:27:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 27 Jan 2026 21:27:21 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:27:21 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 27 Jan 2026 21:27:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 27 Jan 2026 21:27:21 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 27 Jan 2026 21:27:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 27 Jan 2026 21:27:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Jan 2026 21:27:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Jan 2026 21:27:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 27 Jan 2026 21:27:21 GMT
CMD ["rabbitmq-server"]
# Tue, 27 Jan 2026 22:09:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 27 Jan 2026 22:09:09 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-gnu'; digest='62e2c22df73b1f8f04bda5630cb9c32cc60ce2fa28487de0337c039625f5cbda' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-gnu'; digest='9ed29731a27d5aeba44fde8a64a55e04592db915028468a428069cefeee0fc29' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 27 Jan 2026 22:09:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:a56277e49d30e9a430d5cefad3038f88470a8681e48b806fff292791ed54f1fc`  
		Last Modified: Tue, 13 Jan 2026 06:35:51 GMT  
		Size: 26.9 MB (26853837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf4a9722a4674c9a6de325262754adca8a7b42ec0b2420ec0bdef3e16f179c3`  
		Last Modified: Tue, 27 Jan 2026 21:27:45 GMT  
		Size: 33.3 MB (33295387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c60a8b6cdb9135111f002cbe44e5d5d3ee7c146039630e70b778d234a44992`  
		Last Modified: Tue, 27 Jan 2026 21:27:44 GMT  
		Size: 7.3 MB (7300749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685a16d0738d17daaa19119ad26889eb6fda928f7b875697eed55e72962b5a08`  
		Last Modified: Tue, 27 Jan 2026 21:27:44 GMT  
		Size: 9.8 KB (9779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48ff9bf6c3f23221bde34bd198464363512a59ea9bff2ae0c7b2388fd614b2e`  
		Last Modified: Tue, 27 Jan 2026 21:27:45 GMT  
		Size: 29.6 MB (29629448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa85c1e158701348b22f89b40a44ed9c7a40b188183c647cb4692d717ee7113a`  
		Last Modified: Tue, 27 Jan 2026 21:27:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3ee2882a837bc2aa66a52704631a114d935029d8cf554a83ad6ae10751f5c5`  
		Last Modified: Tue, 27 Jan 2026 21:27:45 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4499e68eb1626b5428910562ef85166b177c6ad1c5ded974d3ee0debfdb2ad1c`  
		Last Modified: Tue, 27 Jan 2026 21:27:46 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f237ca29f648f001c1f977f530167148cd1828ed6f822a008abdcd0a2e0c4b`  
		Last Modified: Tue, 27 Jan 2026 21:27:47 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af29bb6b97c411940555cc4d374baa67bdb69d8b0371f53d0ef43a6ad029f293`  
		Last Modified: Tue, 27 Jan 2026 22:09:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a4bd349b4f963b4887689d37c3f631bbb2295de36af760b0880c819c1bb70696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0a30d0041fd076ff77b669d1caf5b1e211872a9951a75944422e4dae3adfe0`

```dockerfile
```

-	Layers:
	-	`sha256:f6ae502db4d8e93dc7f1d58946a5b98e0577d16c897296985ec39b30e56bf627`  
		Last Modified: Tue, 27 Jan 2026 22:09:17 GMT  
		Size: 2.5 MB (2487461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1380805c82968577ec2a616e5e79c37974077342411ffa8c517b4d10ff91ddb9`  
		Last Modified: Tue, 27 Jan 2026 22:09:17 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:47ed73867a0322a2ff198e241d7840627dbd41c51e58667a79e00aa3d0e6db9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117648009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b47f97a81722f7a65be8877a979e2b4e21be2e678abcbf68bd4a8517f884f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 21:29:39 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 27 Jan 2026 21:29:39 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 27 Jan 2026 21:29:39 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 27 Jan 2026 21:29:39 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 27 Jan 2026 21:29:39 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:29:39 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:29:41 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 27 Jan 2026 21:29:41 GMT
ENV RABBITMQ_VERSION=4.2.3
# Tue, 27 Jan 2026 21:29:41 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 27 Jan 2026 21:29:41 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 27 Jan 2026 21:29:41 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:30:00 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 27 Jan 2026 21:30:01 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 27 Jan 2026 21:30:01 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 27 Jan 2026 21:30:01 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:30:01 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 27 Jan 2026 21:30:01 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 27 Jan 2026 21:30:01 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 27 Jan 2026 21:30:01 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 27 Jan 2026 21:30:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Jan 2026 21:30:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Jan 2026 21:30:01 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 27 Jan 2026 21:30:01 GMT
CMD ["rabbitmq-server"]
# Tue, 27 Jan 2026 22:12:45 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 27 Jan 2026 22:39:31 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-gnu'; digest='62e2c22df73b1f8f04bda5630cb9c32cc60ce2fa28487de0337c039625f5cbda' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-gnu'; digest='9ed29731a27d5aeba44fde8a64a55e04592db915028468a428069cefeee0fc29' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 27 Jan 2026 22:39:31 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cc6c4d16f4c98ae22580864c321449747e72a39a46da1f540669f5543ce979`  
		Last Modified: Tue, 27 Jan 2026 21:30:28 GMT  
		Size: 44.4 MB (44355456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bb7484a54b55327295fc5bad8460e6f561883aaefb0abb6c7133f958805f85`  
		Last Modified: Tue, 27 Jan 2026 21:30:26 GMT  
		Size: 9.7 MB (9709102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7d3542c5f24268ded56f6aaf0b3c0ccbcbabe9a92f1c519214d38c2ebe7479`  
		Last Modified: Tue, 27 Jan 2026 21:30:26 GMT  
		Size: 9.7 KB (9651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd83a12c74eb33b6ac70e03f0f627489c942eb8389bf77e9414dd4f6d8e33d1`  
		Last Modified: Tue, 27 Jan 2026 21:30:27 GMT  
		Size: 30.1 MB (30067703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a34ae48f5be8b6c623457c0e5d58a33ba6d2353aa3dc1492ec8008de017309`  
		Last Modified: Tue, 27 Jan 2026 21:30:27 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6136ec35138f87d50c48cf9e4bcab72c24beee25fe1aae870a5dafeada5e2f0e`  
		Last Modified: Tue, 27 Jan 2026 21:30:28 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bd0e6342fb4b1c8d240327cf9eb2b94fe5a058f623d36a0a955985bde859d0`  
		Last Modified: Tue, 27 Jan 2026 21:30:28 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0730cd303cd60b6cf40ec799bc0e93a55d2953c0ad90ea4a71afb2ffb3c5f5e`  
		Last Modified: Tue, 27 Jan 2026 21:30:29 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9812a24c74bfcd158bfc4cafa68641c6d455ee2bb9120cc895bc260087caec9`  
		Last Modified: Tue, 27 Jan 2026 22:39:38 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0f993ab0506cf6b05e7394bd0d0579e6332dd6ff0cd4125a4dd260dff87e9c`  
		Last Modified: Tue, 27 Jan 2026 22:39:39 GMT  
		Size: 4.6 MB (4640251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1fec5a5df63973c1bce03f34a72fdce3f716da5f8fe93e1aa3dd5da0f67f0d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2504109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4332f608567ee5f86e9908a5a9092897006539ce69b922b1d5b2a6b8cf300d`

```dockerfile
```

-	Layers:
	-	`sha256:cebd8ace5bda15d06dc20eef4e7a2c25d2139e85cebac1b92616764de0245ba1`  
		Last Modified: Tue, 27 Jan 2026 22:39:39 GMT  
		Size: 2.5 MB (2487721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:789680321115d5cca7dc15bf5b1c546047d23ae0086b77909c196723072f0d4f`  
		Last Modified: Tue, 27 Jan 2026 22:39:38 GMT  
		Size: 16.4 KB (16388 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:5da563c8b845272f6a713d5fc10a4e189157666c06857acb171234cd008529d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113944704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5149a6829af529935fd01803bfaae86e4c6dfae1ef0cda81e72b65e0b9463836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 21:44:24 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 27 Jan 2026 21:44:24 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 27 Jan 2026 21:44:24 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 27 Jan 2026 21:44:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 27 Jan 2026 21:44:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:44:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:44:27 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 27 Jan 2026 21:44:27 GMT
ENV RABBITMQ_VERSION=4.2.3
# Tue, 27 Jan 2026 21:44:27 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 27 Jan 2026 21:44:27 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 27 Jan 2026 21:44:27 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:45:03 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 27 Jan 2026 21:45:05 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 27 Jan 2026 21:45:05 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 27 Jan 2026 21:45:05 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:45:05 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 27 Jan 2026 21:45:05 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 27 Jan 2026 21:45:05 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 27 Jan 2026 21:45:06 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 27 Jan 2026 21:45:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Jan 2026 21:45:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Jan 2026 21:45:06 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 27 Jan 2026 21:45:06 GMT
CMD ["rabbitmq-server"]
# Tue, 27 Jan 2026 22:09:30 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 27 Jan 2026 22:09:31 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-gnu'; digest='62e2c22df73b1f8f04bda5630cb9c32cc60ce2fa28487de0337c039625f5cbda' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-gnu'; digest='9ed29731a27d5aeba44fde8a64a55e04592db915028468a428069cefeee0fc29' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 27 Jan 2026 22:09:31 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be5587526cf324295df236249b0eeed3eadd3a52eb8c226ff3b8d8a820502df`  
		Last Modified: Tue, 27 Jan 2026 21:45:59 GMT  
		Size: 39.5 MB (39509607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c651acb95c29af762fa2fc7b1f802f2e865914c72e94d36f766c6d89c8e9c5e8`  
		Last Modified: Tue, 27 Jan 2026 21:45:58 GMT  
		Size: 9.6 MB (9591402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d798a86af500183b157755c273a4142e7986455081b4bcd15faed4be832bedff`  
		Last Modified: Tue, 27 Jan 2026 21:45:57 GMT  
		Size: 9.6 KB (9634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70de04f62c4fb52af1165c748a33bdff4ab6a4ecc8aba18341cc8b62a6dca829`  
		Last Modified: Tue, 27 Jan 2026 21:45:59 GMT  
		Size: 30.5 MB (30525844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a2ef099bf5f5c776487f48dfe1cd01210b661f7eab636469baedabed3367fc`  
		Last Modified: Tue, 27 Jan 2026 21:45:59 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a51f876e5f451f9610f4ea2191e09538e001067900d00dbd7d8e2b2c293405`  
		Last Modified: Tue, 27 Jan 2026 21:46:00 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8659959afa77b3062482ffac5666058d24a8d0f0345e7f4f20940a6266afb586`  
		Last Modified: Tue, 27 Jan 2026 21:46:00 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70adca05cc752ebf891f8b2022758f2d31481a86f3ae204bbae187a8dafdc88e`  
		Last Modified: Tue, 27 Jan 2026 21:46:01 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1543468d9d369f02130db2a74819a8a3a89c57fa83ca983a6045fad1228cb4`  
		Last Modified: Tue, 27 Jan 2026 22:09:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9d5eb099c130ea5babb896e2d695d3464b8101d804ab11b23b50d84bb66588f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2507424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7ceb2a0eed37a02ad125a272fe5a701c37d2cf0206d2ce4d07d1ae85a4918b`

```dockerfile
```

-	Layers:
	-	`sha256:54074a209676dc58fdda90f3df9e203900eb2e6f5bbdaf87b67d771c9c87033a`  
		Last Modified: Tue, 27 Jan 2026 22:09:50 GMT  
		Size: 2.5 MB (2491114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:366e6218f9d9e79a0441ac47922f55df1f66d62395c19a2d4d767eb58e510dbd`  
		Last Modified: Tue, 27 Jan 2026 22:09:49 GMT  
		Size: 16.3 KB (16310 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:d2c85d195422b2c5081109cf12e38e9f7834bdd22baf6fe8c7a61e1bdc5d22a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106905769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d991fc78b191622e2bd038355e10175fb850f73d66eebf5b1b17816c706eba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Jan 2026 06:14:56 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:14:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:14:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:14:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:15:46 GMT
ADD file:8d0655de001e92042901c645c76202ac355acb6fa186561e7344a0829ffd983d in / 
# Tue, 13 Jan 2026 06:15:51 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:24:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 27 Jan 2026 22:24:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 27 Jan 2026 22:24:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 27 Jan 2026 22:24:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 27 Jan 2026 22:24:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 22:24:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 27 Jan 2026 22:24:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 27 Jan 2026 22:24:20 GMT
ENV RABBITMQ_VERSION=4.2.3
# Tue, 27 Jan 2026 22:24:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 27 Jan 2026 22:24:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 27 Jan 2026 22:24:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 22:26:55 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 27 Jan 2026 22:27:04 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 27 Jan 2026 22:27:05 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 27 Jan 2026 22:27:05 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 27 Jan 2026 22:27:05 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 27 Jan 2026 22:27:05 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 27 Jan 2026 22:27:05 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 27 Jan 2026 22:27:05 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 27 Jan 2026 22:27:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Jan 2026 22:27:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Jan 2026 22:27:05 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 27 Jan 2026 22:27:05 GMT
CMD ["rabbitmq-server"]
# Wed, 28 Jan 2026 03:56:37 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Wed, 28 Jan 2026 03:56:37 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-gnu'; digest='62e2c22df73b1f8f04bda5630cb9c32cc60ce2fa28487de0337c039625f5cbda' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-gnu'; digest='9ed29731a27d5aeba44fde8a64a55e04592db915028468a428069cefeee0fc29' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Wed, 28 Jan 2026 03:56:37 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f151392858868452ec0f1f8d2947624e8dcdecf23bce587cfbd7c38a3264f9df`  
		Last Modified: Tue, 13 Jan 2026 06:36:06 GMT  
		Size: 31.0 MB (30953090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1daf8c16f6bdcea8e9831cddfcacfd9bd9bb167862da7fff6fa39d16bcc3bf7b`  
		Last Modified: Tue, 27 Jan 2026 22:33:30 GMT  
		Size: 35.1 MB (35148121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7384d034e53c92d13b43585433f5aa195482ec789a66bb3ad31ed9f9af6155`  
		Last Modified: Tue, 27 Jan 2026 22:33:22 GMT  
		Size: 10.8 MB (10828964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9fc5563b6fc1094af1ffc4cecdb2357be3b7f478ec738df71bacc6d40d95e0`  
		Last Modified: Tue, 27 Jan 2026 22:33:16 GMT  
		Size: 9.7 KB (9669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdfc7d6005d8afdba435cbc4d7f81127125167c7b6679ee260e5904facfb8e4`  
		Last Modified: Tue, 27 Jan 2026 22:33:29 GMT  
		Size: 30.0 MB (29963866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d00c4dd1360a32bfab118321f58097f674c43c11e7a2eb4dea657b879e1c54`  
		Last Modified: Tue, 27 Jan 2026 22:33:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e291478aaaab9b870a74ccb3e0f9f718abbc86bf795142c5325275b8c43b3c`  
		Last Modified: Tue, 27 Jan 2026 22:33:23 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cdd9f2376f4d0c8a2c7db4fd8253f832f8fe794f4e0268616820a9419af8f9`  
		Last Modified: Tue, 27 Jan 2026 22:33:24 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdc2d7ae9a7f9103a5db113936485bf9a54ba4bf4d7dec73a7aba50a865b5cc`  
		Last Modified: Tue, 27 Jan 2026 22:33:24 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80366469e51a0cd4a06ccaf7d3f86998e6b2552a678b842583d4db2a62d06f7`  
		Last Modified: Wed, 28 Jan 2026 03:58:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1b9a58c195e8f7318bc9334ff4c3222a41ebd417711399332130f49a7a712e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2ba3bbc76a321c78879326b63fb87069fc4e9c61dfb52d3994829ce76ce1d5`

```dockerfile
```

-	Layers:
	-	`sha256:ae4afdb4114f9298ba172b6a3de34aa1e5c12b4b9a19c9db6046e0ee936878b4`  
		Last Modified: Wed, 28 Jan 2026 03:58:05 GMT  
		Size: 2.5 MB (2479028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdb914f9a301a934df646ac1b93b5674a5889ddf0c619ca5ea785b0bad0f099a`  
		Last Modified: Wed, 28 Jan 2026 03:58:05 GMT  
		Size: 16.3 KB (16313 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; s390x

```console
$ docker pull rabbitmq@sha256:2acca9a701bc1cb1ee10afa350a524563d8c91799f0132d40bc24c034b469993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107130862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa576b482c7de6655b1107edd5a63ba8dadb888f9b7134763d89f82314198467`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Jan 2026 06:29:20 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:29:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:29:22 GMT
ADD file:55a7874afa0094b7b4c6edc68b58164a34177fa761bc6e673ddb0c846b91f26f in / 
# Tue, 13 Jan 2026 06:29:22 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 21:28:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 27 Jan 2026 21:28:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 27 Jan 2026 21:28:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 27 Jan 2026 21:28:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 27 Jan 2026 21:28:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:28:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:28:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 27 Jan 2026 21:28:55 GMT
ENV RABBITMQ_VERSION=4.2.3
# Tue, 27 Jan 2026 21:28:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 27 Jan 2026 21:28:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 27 Jan 2026 21:28:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 21:29:19 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 27 Jan 2026 21:29:20 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 27 Jan 2026 21:29:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 27 Jan 2026 21:29:20 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 27 Jan 2026 21:29:20 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 27 Jan 2026 21:29:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 27 Jan 2026 21:29:20 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 27 Jan 2026 21:29:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 27 Jan 2026 21:29:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Jan 2026 21:29:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Jan 2026 21:29:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 27 Jan 2026 21:29:20 GMT
CMD ["rabbitmq-server"]
# Tue, 27 Jan 2026 22:10:26 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 27 Jan 2026 22:10:26 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-gnu'; digest='62e2c22df73b1f8f04bda5630cb9c32cc60ce2fa28487de0337c039625f5cbda' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-gnu'; digest='9ed29731a27d5aeba44fde8a64a55e04592db915028468a428069cefeee0fc29' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 27 Jan 2026 22:10:26 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:88318e41cf944fd93c8b2fdfaeb1378b17ed0e2440ef9811f9820449bf19a6ad`  
		Last Modified: Tue, 13 Jan 2026 06:36:13 GMT  
		Size: 29.9 MB (29909204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7893d41301587bd4b4ff48d7fc8fc0839086ed699361b387bff17234dfbec7af`  
		Last Modified: Tue, 27 Jan 2026 21:29:56 GMT  
		Size: 38.6 MB (38581366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e116417c397307dc0b27cf485299601b76afa46e700de4b934787d621a059e`  
		Last Modified: Tue, 27 Jan 2026 21:29:55 GMT  
		Size: 8.6 MB (8613703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0909b0227f1d5054579bf799a130d0b92ffba0ac9b4877a85e7e759f1b2f4e7`  
		Last Modified: Tue, 27 Jan 2026 21:29:55 GMT  
		Size: 9.8 KB (9809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bc0e9382aaf846d95ae9eaf75ef03854caef9db53889de6d51dd687cd0452a`  
		Last Modified: Tue, 27 Jan 2026 21:29:56 GMT  
		Size: 30.0 MB (30014732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761c64ef7543c3ffd3ad7a0c1cc1e953c0dc0e7c9a9c91efa30620657f3fb561`  
		Last Modified: Tue, 27 Jan 2026 21:29:56 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8094a4c9e92a848923ece224ffc39c170a72c383f327c6228f17ed70a3962197`  
		Last Modified: Tue, 27 Jan 2026 21:29:56 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2772d5e881183aca334aa7eb79bbcc806be7fd6cbc5c0b765b7a0bfc1a06c1db`  
		Last Modified: Tue, 27 Jan 2026 21:29:57 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bab260f0e4acb7859fe1ed3e8b1560c0a0f76e439d18d40f26bc0c4d0751153`  
		Last Modified: Tue, 27 Jan 2026 21:29:57 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8de63903ba01f6b50ba678067da3e29782e40c24df8d990a71b8c0131f42ff`  
		Last Modified: Tue, 27 Jan 2026 22:10:37 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ea13e09fad093b6d43ccdafc07ed57d2efe998ad747d3422d8d5a0edaf37d344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2505035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a194328fa3a83a68c85f864ce0b156d46d5e582deea260eface4daa0a8be8fbc`

```dockerfile
```

-	Layers:
	-	`sha256:c867e08ae1cbfd7e81082921e3916797a4fc5106b7198ca33410ead97a369169`  
		Last Modified: Tue, 27 Jan 2026 22:10:37 GMT  
		Size: 2.5 MB (2488771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72c8f80dac6fab0c2fc277554d789c9f752538dac00491ba39e9702ee7e3b379`  
		Last Modified: Tue, 27 Jan 2026 22:10:37 GMT  
		Size: 16.3 KB (16264 bytes)  
		MIME: application/vnd.in-toto+json
