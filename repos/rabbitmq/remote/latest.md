## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:23abfd791c05664073bcdeac6a5926ff57294a350dfcccfc7b9fc30327144353
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

### `rabbitmq:latest` - linux; amd64

```console
$ docker pull rabbitmq@sha256:649d8a95d62ed2f42ff043301dc3a8a5457fa0155390b631fe6887837f7a3b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112837200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18ffeb3497eadd347d2c48f114a3653204a3a4fcbb0385ecb8ce655d649227f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Tue, 18 Nov 2025 02:56:23 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 18 Nov 2025 02:56:23 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 18 Nov 2025 02:56:23 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 18 Nov 2025 02:56:23 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 18 Nov 2025 02:56:23 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:56:23 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 18 Nov 2025 02:56:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 18 Nov 2025 02:56:25 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 18 Nov 2025 02:56:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 18 Nov 2025 02:56:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 18 Nov 2025 02:56:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:56:46 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 18 Nov 2025 02:56:47 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 18 Nov 2025 02:56:47 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 18 Nov 2025 02:56:47 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 18 Nov 2025 02:56:47 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 18 Nov 2025 02:56:47 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 02:56:47 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 18 Nov 2025 02:56:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:56:47 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 18 Nov 2025 02:56:47 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e50c11f198ebc4e286f57bd2fff6bb4737ad6298d267b6ba0797d343152653b`  
		Last Modified: Tue, 18 Nov 2025 02:57:20 GMT  
		Size: 46.3 MB (46261452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5746ab5df1850526523b1b7478f93379d046ded61a1aef28d36fdc868dbae0f0`  
		Last Modified: Tue, 18 Nov 2025 02:57:18 GMT  
		Size: 9.0 MB (8994549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b00085445fe13d9dcfcaaef107045b96c01f8200bfc2a117919a589fc38cfe9`  
		Last Modified: Tue, 18 Nov 2025 02:57:18 GMT  
		Size: 9.7 KB (9678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7218fe655bf8dbe00f8b5b348108e3fad39dfd4cae8be9263dd97026ea303c7d`  
		Last Modified: Tue, 18 Nov 2025 02:57:21 GMT  
		Size: 27.8 MB (27845083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342269d3962fd39e989bc15749961bb6905cdb2886bd3e21145460ea4369f1eb`  
		Last Modified: Tue, 18 Nov 2025 02:57:18 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0d255a715bcd23587ed767ece0dffb9c77f679c92fce01762f8734d606c3d1`  
		Last Modified: Tue, 18 Nov 2025 02:57:18 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4461d026edc4fb047b3899f173d58c1feb0567f260ed5f64b433441b9e526a`  
		Last Modified: Tue, 18 Nov 2025 02:57:18 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d381ad6ab2745b121220183f0e4ed8309de4608878fc9f85f5d4ec79012962`  
		Last Modified: Tue, 18 Nov 2025 02:57:18 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:663af4fb66f4f22b0d8dc7beac7354ccd3aeac09b95821166e5cdebe45b7b7f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18841170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8093561c5df7671070613499ffb634f48843bc5e76adcbdc83a06ff37c4b8932`

```dockerfile
```

-	Layers:
	-	`sha256:c6aaf6b82ad8195d587c67999661ded0bd08b2cde5b1bb25a4b8378471229e16`  
		Last Modified: Tue, 18 Nov 2025 04:54:03 GMT  
		Size: 2.5 MB (2487854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b225ad4c871f4bf8c8370e8f985b868d075751995b4492f6d7b4ceffaea9f4f8`  
		Last Modified: Tue, 18 Nov 2025 04:54:04 GMT  
		Size: 5.4 MB (5378389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dce7b4d7195ab93b9bdbd56fda2c6cfcc33e7836308d4fc9f2b2259497dfdef7`  
		Last Modified: Tue, 18 Nov 2025 04:54:05 GMT  
		Size: 5.5 MB (5534998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50e960a772948539501e7fd98ea0aa67901561a1c698296881d7073ceb2aa6b`  
		Last Modified: Tue, 18 Nov 2025 04:54:06 GMT  
		Size: 5.4 MB (5380131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70322d8f19af283f3e9fd6d4038389effeb71dc20dbb65cda1ee9a3b35fafbf3`  
		Last Modified: Tue, 18 Nov 2025 04:54:07 GMT  
		Size: 59.8 KB (59798 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:61d8cb0068bcc26d378241024f95b2236f554a84ba009969d15cbdc7563aaa02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95215165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752f205fc6419c02f1ef0456eb4197c0548621a22d992707144a6422fb54e96d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:17 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:17 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:20 GMT
ADD file:dd3740083ecd2e2b1e178f1771ef73043bc7be6c831492453a755b873d8b531b in / 
# Thu, 16 Oct 2025 19:25:21 GMT
CMD ["/bin/bash"]
# Tue, 18 Nov 2025 00:01:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 18 Nov 2025 00:01:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 18 Nov 2025 00:01:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 18 Nov 2025 00:01:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 18 Nov 2025 00:01:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:01:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 18 Nov 2025 00:01:32 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 18 Nov 2025 00:01:32 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 18 Nov 2025 00:01:32 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 18 Nov 2025 00:01:32 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 18 Nov 2025 00:01:32 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:01:56 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 18 Nov 2025 00:01:57 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 18 Nov 2025 00:01:57 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 18 Nov 2025 00:01:57 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 18 Nov 2025 00:01:57 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 18 Nov 2025 00:01:57 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 00:01:57 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 18 Nov 2025 00:01:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 00:01:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 00:01:57 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 18 Nov 2025 00:01:57 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6cdc0abf996c3192bfbda4018d34c282871d4be33fb369176002cb2199673adf`  
		Last Modified: Fri, 17 Oct 2025 08:06:35 GMT  
		Size: 26.9 MB (26852672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c018e8481c87152ee2c5cb4ee3fa596a0ec615777bd9bcc2c97c577e888c8c`  
		Last Modified: Tue, 18 Nov 2025 00:02:40 GMT  
		Size: 33.3 MB (33295196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2c85b8e6e6e54877145781f4422300b06854218a704d8defddd6ba3aec3de3`  
		Last Modified: Tue, 18 Nov 2025 00:02:38 GMT  
		Size: 7.3 MB (7309026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91c4460416d65c8b3d588179b6a4fba19903dd662a2844f31e9e1c11583b375`  
		Last Modified: Tue, 18 Nov 2025 00:02:37 GMT  
		Size: 9.8 KB (9775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2584b3f17c67cb3a5f902071e254b0a0835355e10674cb9b5b44819a48ce9794`  
		Last Modified: Tue, 18 Nov 2025 00:02:40 GMT  
		Size: 27.7 MB (27746750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce1f9b4263c6e3fc5b78c9d4f3837e5e8e2ecc4028bc5f0f2bd497697a5db2a`  
		Last Modified: Tue, 18 Nov 2025 00:02:37 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e311052d34c23b3a7bbbe02516d51560be3aa4b37a91832436439237e0811b`  
		Last Modified: Tue, 18 Nov 2025 00:02:38 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae6311f7c275125e206e637b540adaa58606d7458452454cc2301e40a6bfa34`  
		Last Modified: Tue, 18 Nov 2025 00:02:37 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9cec22ed89236403d088fc2d69855e51c2819cece42317698ba5476d64d004`  
		Last Modified: Tue, 18 Nov 2025 00:02:37 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:544195180bfcfe3a56e6ce1f0c4818552fc679acf387a9719a0b4a9b5bfa5990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18295952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88474bc0889e38fd0d7ddee157c846fe5a90ca952da59af8ba743e4e3f30f048`

```dockerfile
```

-	Layers:
	-	`sha256:f123444a4b2dc0feafa06ca9e28db90a5c733f94a3007862ee2a52bdb52c6928`  
		Last Modified: Tue, 18 Nov 2025 01:52:53 GMT  
		Size: 2.5 MB (2488654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bfe55851d8c5116c25c7944a30ae7ab86aea9c1b00ecccce6e1214ccfa45f46`  
		Last Modified: Tue, 18 Nov 2025 01:52:55 GMT  
		Size: 5.2 MB (5197169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57e81f8b1c2254b803a3d7fa18893dd519d4654e0c306de5e08242e6a16dcc1c`  
		Last Modified: Tue, 18 Nov 2025 01:53:07 GMT  
		Size: 5.4 MB (5351223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db40d6e96742de1c033a6b9373c3234d5c0d45821c817d7adc06478c66ce8748`  
		Last Modified: Tue, 18 Nov 2025 01:53:09 GMT  
		Size: 5.2 MB (5198911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1144e4cabd92226971f18df218638c9f77aeb163e5cd0cc16b11d9e692728903`  
		Last Modified: Tue, 18 Nov 2025 01:53:10 GMT  
		Size: 60.0 KB (59995 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:513b74844ef09314128a5c86e833e0247f8a1aa1d723cc217b7fb8c3cb5e5aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110699889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ac7681f2d70a263bac7d17188381d24ca26f788a9a57b382422b6ed8b993e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Tue, 18 Nov 2025 00:00:56 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 18 Nov 2025 00:00:56 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 18 Nov 2025 00:00:56 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 18 Nov 2025 00:00:56 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 18 Nov 2025 00:00:56 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:00:56 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 18 Nov 2025 00:00:58 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 18 Nov 2025 00:00:58 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 18 Nov 2025 00:00:58 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 18 Nov 2025 00:00:58 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 18 Nov 2025 00:00:58 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:01:18 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 18 Nov 2025 00:01:19 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 18 Nov 2025 00:01:19 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 18 Nov 2025 00:01:19 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 18 Nov 2025 00:01:19 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 18 Nov 2025 00:01:19 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 00:01:19 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 18 Nov 2025 00:01:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 00:01:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 00:01:19 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 18 Nov 2025 00:01:19 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9a11e86d1713a7fc08ad1ec4499a11d9b5aad9c06cec03b72a3770e4583ecf`  
		Last Modified: Tue, 18 Nov 2025 00:01:57 GMT  
		Size: 44.4 MB (44355576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2439577abfe27dec5a3b39ad2ac4d1a2d847bcc4fc10b850a3826af7916d470`  
		Last Modified: Tue, 18 Nov 2025 00:01:57 GMT  
		Size: 9.7 MB (9716274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ce50c45aa5da8003251e9e464fb988a6a042152ca874707bc37d9ab80b77d6`  
		Last Modified: Tue, 18 Nov 2025 00:01:53 GMT  
		Size: 9.7 KB (9680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6077fd4534483e4563ee62f4730db5df3a0056450b8ee9dcd44132d7780f0bf3`  
		Last Modified: Tue, 18 Nov 2025 00:01:57 GMT  
		Size: 27.8 MB (27754652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a064f00086aabb6f63887e9aa6839c4f2635b9ec0a16e4fefdfe82100fecc107`  
		Last Modified: Tue, 18 Nov 2025 00:01:53 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e181e81df8e7caf06529763691a508e9f7bc937e3038dcb9a97bfe87551cd0`  
		Last Modified: Tue, 18 Nov 2025 00:01:53 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db255e99389d6e0384c5fcb198a9057a0ffb1ace05e857fa4b3da50722a5ecd`  
		Last Modified: Tue, 18 Nov 2025 00:01:53 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc43ca3049ce973bb76a537a5d14eb6d80f8709747c1ce497cb07c1a3ca1432`  
		Last Modified: Tue, 18 Nov 2025 00:01:53 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ad32a7eb7b2d8a0290b8fcd5039fbf3d7b711ec28c5d59af109477514ad8e6df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18900150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ed112bf17c6ff708cff70b7a3d7381b5fac8f6257a2bc353a776e1d8e0505d`

```dockerfile
```

-	Layers:
	-	`sha256:6b6d66beec9ff8d104add3d778bd856d575df8e83c470f81c681273190237c46`  
		Last Modified: Tue, 18 Nov 2025 01:53:19 GMT  
		Size: 2.5 MB (2488914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e7e8898b23d7779138adcde46c9f9f32f5b42d7afe73ed0d8a71942f016b5c`  
		Last Modified: Tue, 18 Nov 2025 01:53:21 GMT  
		Size: 5.4 MB (5397610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63bcba7ac490dc98094ff6895377b9c8414d5e5fdeb7b1c82671fa8e824ea37f`  
		Last Modified: Tue, 18 Nov 2025 01:53:23 GMT  
		Size: 5.6 MB (5554237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da13a62f0a6c81418ef2bb27c8b220f09e02b98d653040c0522fd9120229300`  
		Last Modified: Tue, 18 Nov 2025 01:53:24 GMT  
		Size: 5.4 MB (5399352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:994e05ff6bd95ea0c7862ce72f54d1f8d5269b8ee41111fd68608ccce30d61e0`  
		Last Modified: Tue, 18 Nov 2025 01:53:25 GMT  
		Size: 60.0 KB (60037 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:08c5cf76828a0e3801a94dcc70c639383c493071a8f0e196f80a10cccc8bc27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111229798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f43f8c5b4697eb4380dd6b950421840f8aa0fba949e62391b974cbe5d00d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 19:13:02 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 14 Nov 2025 19:13:02 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 14 Nov 2025 19:13:02 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 14 Nov 2025 19:13:10 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 14 Nov 2025 19:13:10 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 19:13:10 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 14 Nov 2025 19:13:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 14 Nov 2025 19:13:13 GMT
ENV RABBITMQ_VERSION=4.2.1
# Fri, 14 Nov 2025 19:13:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 14 Nov 2025 19:13:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 14 Nov 2025 19:13:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:08:55 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 18 Nov 2025 00:08:57 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 18 Nov 2025 00:08:58 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 18 Nov 2025 00:08:58 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 18 Nov 2025 00:08:58 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 18 Nov 2025 00:08:58 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 00:08:59 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 18 Nov 2025 00:09:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 00:09:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 00:09:01 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 18 Nov 2025 00:09:01 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aca544a4c75276e59b4240a78ef3e6b84b3ff47d98f91017896374d7904778`  
		Last Modified: Fri, 14 Nov 2025 19:15:28 GMT  
		Size: 39.5 MB (39509671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c3605c27538c6ca4cb7e43022bbad01ce80ad26cc9b1435768014a94927828`  
		Last Modified: Fri, 14 Nov 2025 19:15:24 GMT  
		Size: 9.6 MB (9598405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79e6621a2b18898e95def5a9fcbd0740f40e098b840e4bc7aaac4e5c5859eef`  
		Last Modified: Fri, 14 Nov 2025 19:15:23 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1b5bd4f05b106b6edf4a513787199169a9ceb5bf8afe20cad963a96dbfa319`  
		Last Modified: Tue, 18 Nov 2025 00:16:22 GMT  
		Size: 27.8 MB (27805918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80511751fad297b5e94b0fbe033471dc06063b304e2abbc245fd2f4b22270ccc`  
		Last Modified: Tue, 18 Nov 2025 00:16:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7369781f8a59720be3e616a7d16fae120130a6716d58d2ab84d69a72eb976783`  
		Last Modified: Tue, 18 Nov 2025 00:16:20 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b5bd0629dcc76135379ac8eedc811a9633da22bb2dbc80dc526d0265aba4cc`  
		Last Modified: Tue, 18 Nov 2025 00:16:20 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5272887d3790ae306479e61b03638807a50319b41559a4b1d76f5536cf0865d9`  
		Last Modified: Tue, 18 Nov 2025 00:16:20 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b8d912b4c1215f57af4a51a66ab0d4daaeca7e2834ebcd455492f235435a604b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18755541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70e68c08d1fd632687c8132f4cb60ed8831be0765b1e6d3b24b084e96243ab5`

```dockerfile
```

-	Layers:
	-	`sha256:fe67181856b1cd3cd090427bf631cad72cb7899b53a480e3f2458bf3b665b3a3`  
		Last Modified: Tue, 18 Nov 2025 01:53:34 GMT  
		Size: 2.5 MB (2492307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0c8fdfd336cc10f26f4fe36440b63dc41e42d122dae1fda090b66bbcd16a6d3`  
		Last Modified: Tue, 18 Nov 2025 01:53:35 GMT  
		Size: 5.3 MB (5348331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e2baf3d410a69be0443103a1494036d80166e0696990df206821b05931bc27`  
		Last Modified: Tue, 18 Nov 2025 01:53:38 GMT  
		Size: 5.5 MB (5504970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d851f3b64160147074d7045e7cdf1de898e41f63a0e9e306fd6a37a804a73b3a`  
		Last Modified: Tue, 18 Nov 2025 01:53:39 GMT  
		Size: 5.4 MB (5350073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f90d608f527e5bfcee3eaeb3cb62754b1b98aea2ac11b604df0e4b47eefb5e1d`  
		Last Modified: Tue, 18 Nov 2025 01:53:40 GMT  
		Size: 59.9 KB (59860 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:d6dff3f005fc367064e88c55ea9ee8b9f5924354e11c537eeb0609017e548c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104700944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d3bc4f2ab96829c13a93686ebe6040d2d5a5eab22bb42e2c1a9164824d3482`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:53:04 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:53:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:53:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:53:05 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:53:45 GMT
ADD file:6c2a12ec42d9e6c7e02041a8483a3a93ab9b91131ca66ecb93506ba161a4909d in / 
# Thu, 16 Oct 2025 19:53:49 GMT
CMD ["/bin/bash"]
# Sat, 15 Nov 2025 14:46:31 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 15 Nov 2025 14:46:31 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 15 Nov 2025 14:46:31 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 15 Nov 2025 14:46:32 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 15 Nov 2025 14:46:32 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 14:46:32 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 15 Nov 2025 14:46:36 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Sat, 15 Nov 2025 14:46:36 GMT
ENV RABBITMQ_VERSION=4.2.1
# Sat, 15 Nov 2025 14:46:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 15 Nov 2025 14:46:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 15 Nov 2025 14:46:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:07:06 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 18 Nov 2025 02:07:15 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 18 Nov 2025 02:07:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 18 Nov 2025 02:07:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 18 Nov 2025 02:07:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 18 Nov 2025 02:07:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 02:07:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 18 Nov 2025 02:07:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:07:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 18 Nov 2025 02:07:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4f36e1b0a2cc427e5979b49608ef4e52795313f083fdc941cab616d5ab2b861b`  
		Last Modified: Sat, 15 Nov 2025 10:03:37 GMT  
		Size: 31.0 MB (30952148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606650a61dbbc93efe83db6c01f31098ae14abd4834968121b22948aa3594218`  
		Last Modified: Sat, 15 Nov 2025 14:55:42 GMT  
		Size: 35.1 MB (35148108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894681447bb26bf478bea3393756ebd369dbe3c51970e4acdedc0b1d8f9876e8`  
		Last Modified: Sat, 15 Nov 2025 14:55:39 GMT  
		Size: 10.8 MB (10831054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ace5028ea6ad662e89ea950028a3569eea4433bdf62c87e8ce84d58b6133cc`  
		Last Modified: Sat, 15 Nov 2025 14:55:38 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b4bf9104636ca1401983244b1716aec5ea4e9f927160b6a48cb9733c4c3666`  
		Last Modified: Tue, 18 Nov 2025 03:17:16 GMT  
		Size: 27.8 MB (27758214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9f4e0b9f1ccd082384104a464df2eebaa194d1927a3c6c3e756bd9b50dfdbc`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be3ceb28403430901d0e4e2ca5736a8cd336328d2cf842a89d932a6c9633051`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccbba1ffc329f8aba69e5168671d96d93885802356fc3421130bead91af084c`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34337440b2d44efb13a1a3a0de245cee5dec16798af8dfb50a4f83ce6e9face0`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2e2b3b6ac7e665dd7207e91d393f62c407a7d606c9d3e8ec8312c0d663b6ea4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18724174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b7ee41b79ad0437d04de90633d916dbe8128fcb437f85143a49dc1779791d1`

```dockerfile
```

-	Layers:
	-	`sha256:a9e203963ab6a4c6ac1be54585dae5f6ec784b23098b30a356ee1dfa77e2b47e`  
		Last Modified: Tue, 18 Nov 2025 04:54:40 GMT  
		Size: 2.5 MB (2480221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cbf4a7011f53fcb9a298a7c4abd2728205fa34aa040e558f1cbc7ad8a076a66`  
		Last Modified: Tue, 18 Nov 2025 04:54:41 GMT  
		Size: 5.3 MB (5342764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6524fee27762667bd2cf79e38bc2624618dcd42fe278a959d5151eace9197930`  
		Last Modified: Tue, 18 Nov 2025 04:54:42 GMT  
		Size: 5.5 MB (5496816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b6fe7d69e0837cf705d86de351c4fc206efb9740db5383331ebaf88fbddf7e1`  
		Last Modified: Tue, 18 Nov 2025 04:54:43 GMT  
		Size: 5.3 MB (5344506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b94d4fa81b9399253f0b70fba72ed733cb31c5f32a0981b170d17fcde78bbe`  
		Last Modified: Tue, 18 Nov 2025 04:54:44 GMT  
		Size: 59.9 KB (59867 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:b5a45657b541723500dc98a7337257340538ae7bae6fab95c8785843c5611d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104952291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4ed0d527c8efceb125a88bf9521efe16cfd72a78f70a874adc3e14c97be7d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:14 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:16 GMT
ADD file:f7335d462150d31c3c91b13ccd3e927bc9a1b9c6664fa8905ccf68bbe3d86cd3 in / 
# Thu, 16 Oct 2025 19:25:16 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 17:32:37 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 14 Nov 2025 17:32:37 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 14 Nov 2025 17:32:37 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 14 Nov 2025 17:32:37 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 14 Nov 2025 17:32:37 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:32:37 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:32:38 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 14 Nov 2025 17:32:38 GMT
ENV RABBITMQ_VERSION=4.2.1
# Fri, 14 Nov 2025 17:32:38 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 14 Nov 2025 17:32:38 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 14 Nov 2025 17:32:38 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:57:57 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 17 Nov 2025 23:57:58 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 17 Nov 2025 23:57:59 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 17 Nov 2025 23:57:59 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 17 Nov 2025 23:57:59 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 17 Nov 2025 23:57:59 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 17 Nov 2025 23:57:59 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 17 Nov 2025 23:57:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Nov 2025 23:57:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Nov 2025 23:57:59 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 17 Nov 2025 23:57:59 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7d5b0205a5ff16c2b58f20a113b5eb9a80393a644df077beab5d90635153dc66`  
		Last Modified: Thu, 16 Oct 2025 21:17:39 GMT  
		Size: 29.9 MB (29907597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becfaa46b24ce0d23e3b38f61afed95e4e32f74c45305bc6851131fe06112c14`  
		Last Modified: Fri, 14 Nov 2025 17:33:36 GMT  
		Size: 38.6 MB (38581223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8fbc3d039beb8621ada316e309eeee4b477db2d477f9e64a78a5ded784081a`  
		Last Modified: Fri, 14 Nov 2025 17:33:34 GMT  
		Size: 8.6 MB (8623275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38c9640e22f4e110edbf01a64d8ee92a2f6fc7818e530a67a6e464570ee5abb`  
		Last Modified: Fri, 14 Nov 2025 17:33:33 GMT  
		Size: 9.8 KB (9809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c72512a082ced19bffb6e14d3ada4fb22c939cdd6bb275d32790ec692d3bc4`  
		Last Modified: Tue, 18 Nov 2025 00:05:28 GMT  
		Size: 27.8 MB (27828635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb64f465ba1f4d4d581685883cba61c4a3bab767ce0336c101d189f6382f7ae`  
		Last Modified: Tue, 18 Nov 2025 00:05:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c53f9ee77616d35698470ed0d7597763988c4ff5c55210ab46f7394ecc5e05`  
		Last Modified: Tue, 18 Nov 2025 00:05:26 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ad19bc8aca8df1279deb9dd50fc0d3c6f416747ae2d3bbcd1539b3d8a4b997`  
		Last Modified: Tue, 18 Nov 2025 00:05:26 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937a8a209e056cb70b17652521a7836877bba63555d807c5e2261fa47843145e`  
		Last Modified: Tue, 18 Nov 2025 00:05:26 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:84e7989af53a9a170f3bb71dbbec52f6b9cb9e6bbd2e196b5f6737c44806f416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18381316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9480bb4b0c00051b48285f26a893a3027f1963b3bd82ed8c062ee27d93e9f3a5`

```dockerfile
```

-	Layers:
	-	`sha256:82e7e214922b4e6ce51f70b1ca2101c498878cb058f2300138d6ff5306db4828`  
		Last Modified: Tue, 18 Nov 2025 01:53:59 GMT  
		Size: 2.5 MB (2489964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae72b4b2744b4594c2a46d970fd4db920124ed1f005a847573b376387638a276`  
		Last Modified: Tue, 18 Nov 2025 01:54:01 GMT  
		Size: 5.2 MB (5224836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02e5275040cdb0c2f614fb64e49d61dc7158ea7ac229390f5853f24a54e8143c`  
		Last Modified: Tue, 18 Nov 2025 01:54:02 GMT  
		Size: 5.4 MB (5380141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ad935798e72f34264e14aace455ec7e8c5c154b5480363475314e22d2f3d2f1`  
		Last Modified: Tue, 18 Nov 2025 01:54:04 GMT  
		Size: 5.2 MB (5226578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fce394cb3194ba077721ea5be0af3cbf79334c4bf165d5f41a9ca96218fcfa03`  
		Last Modified: Tue, 18 Nov 2025 01:54:05 GMT  
		Size: 59.8 KB (59797 bytes)  
		MIME: application/vnd.in-toto+json
