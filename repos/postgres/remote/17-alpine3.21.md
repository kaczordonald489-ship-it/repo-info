## `postgres:17-alpine3.21`

```console
$ docker pull postgres@sha256:5bcb5623bb6999b2f7fbd2109f0bfc1f144d138b52ca35ede95d644d93585c2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:17-alpine3.21` - linux; amd64

```console
$ docker pull postgres@sha256:1c80152b6cda1f6a02a01c78ccec2be847c16048556f77cdc59e1b7313073a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110602817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad6d66a8948ed719c7a564bc24f18906ed2fd0d5fb4761b13b6bfa6b0327636`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:19:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:22 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:19:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:19:22 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:19:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:19:22 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:19:22 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 19:19:22 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 19:19:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:21:53 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:21:53 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:21:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:21:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:21:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:21:53 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:21:53 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:21:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:21:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:21:53 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:21:53 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:21:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc69d4ad680f2dc031081b31dc4fa3f7cd55de1995deabe253ce407bf700c97`  
		Last Modified: Fri, 14 Nov 2025 19:22:18 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d8ea049a821820da5c6cda9d864a12cc89a49934e3141a0a418ed81ead0477`  
		Last Modified: Fri, 14 Nov 2025 19:22:18 GMT  
		Size: 918.3 KB (918257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff91185e6f25c5a0e5e8e8b2e87697477d5d440d5b75c2a92a5829cd68938c5`  
		Last Modified: Fri, 14 Nov 2025 19:22:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68dd8434a4e1567a50320e68a614e48b793befacc21bda69edf2a035aa3cf24`  
		Last Modified: Fri, 14 Nov 2025 19:22:25 GMT  
		Size: 106.0 MB (106024706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20037e7ec4ba46412a886953a5f36289211cc6cebc8cd1b693299d259424f5f`  
		Last Modified: Fri, 14 Nov 2025 19:22:18 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b8ca138a07e5f75267194b0ae7e131e4a0f314b6cb56d56f7f36b807ec549e`  
		Last Modified: Fri, 14 Nov 2025 19:22:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5720be95b206e88fa3d22d58ebe4f1dc6b6fe873e7abc5af641aa3be9ac12d`  
		Last Modified: Fri, 14 Nov 2025 19:22:18 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6913b133c7304484f005a36bd78ed6d24d8fd51648b22853d7f238530c44fa`  
		Last Modified: Fri, 14 Nov 2025 19:22:18 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d979604bca7fee5b2f0bc7a9bd375a9d2eafa5c5c453bfa5cd7b433c7bec48ba`  
		Last Modified: Fri, 14 Nov 2025 19:22:18 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:5a458a9a1b4b8225c0486427c455113cea3f922af64fd1085c105726c0746753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.7 KB (639746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df253cdbfb9b7789014e692c8c50ed79597e74e3841a7f4698e2871d94158c9e`

```dockerfile
```

-	Layers:
	-	`sha256:2c50560ad8fe6e9565980612d2a4cbf27c03b11faed5a03ffa0185b81ef2ab14`  
		Last Modified: Fri, 14 Nov 2025 21:15:54 GMT  
		Size: 598.7 KB (598688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74eefb81acfe14acc35002e6783b1a90f27ff1ed3edca499421425636b9ed410`  
		Last Modified: Fri, 14 Nov 2025 21:15:54 GMT  
		Size: 41.1 KB (41058 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; arm variant v6

```console
$ docker pull postgres@sha256:1369fdb6300f5fd929c5ed40dfac17b088c4cd493805190e59aeb11bbbff1958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90147216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e406e3f10ce39a03f20fa7222a094fea4eba155f98eaa35bf183216fdf9395ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:38:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:38:13 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:38:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:38:13 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:38:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:38:13 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:38:13 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 19:38:13 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 19:38:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:41:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:41:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:41:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:41:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:41:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:41:18 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:41:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:41:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:41:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:41:18 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:41:18 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:41:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4ab308e55a7bf9991d2655761b276b952e9c10918951b743ae97a59673f20e`  
		Last Modified: Fri, 14 Nov 2025 19:41:36 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151c5c6109ba3c4296a1ff3880bf5c6f2defdc3cb6c91b913a1338ef3ddb4a6f`  
		Last Modified: Fri, 14 Nov 2025 19:41:37 GMT  
		Size: 886.1 KB (886110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc50695730191e5e332dd2138bc453146ea7c971667da6070f3faf829764280d`  
		Last Modified: Fri, 14 Nov 2025 19:41:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d75fc1d74fa21f2084c3f8fe73e1010bea825e947dd463ca9fa7d2566c2ab35`  
		Last Modified: Fri, 14 Nov 2025 19:41:52 GMT  
		Size: 85.9 MB (85878347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dcf5de93e856c63548c8e0370a728f9330c2d455dc2203dc531ea23c9995fe`  
		Last Modified: Fri, 14 Nov 2025 19:41:36 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f893f57851d71ab60b219548331d579820c5243889b37d84eaa3dff16f9e06`  
		Last Modified: Fri, 14 Nov 2025 19:41:36 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90c84942d650b060586496e6bacc75d807a89b280caf7f7489c593ff5ba4ae2`  
		Last Modified: Fri, 14 Nov 2025 19:41:36 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0747000c623a2615c3426f8671b2b4489cde841aa3375b8eae2ae5a31e2841`  
		Last Modified: Fri, 14 Nov 2025 19:41:36 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d229735e3922a1136c26e30330cc769980e13845bb0b477c1e5e568b8f907d`  
		Last Modified: Fri, 14 Nov 2025 19:41:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:c1f9cd40b89873dec0fbf5b8f0f1099166198ebd4be7f6a4df44f9c527c6a168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 KB (40992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc1db9dfe144260b0318aaf2dbcbc7efa47e9bc92d9f1f62efaad9e61d2a562`

```dockerfile
```

-	Layers:
	-	`sha256:df96f2fdf3a9156c09e43a9e62ffa6a8a94c82aa27133c3b54071cfc4d6eb854`  
		Last Modified: Fri, 14 Nov 2025 21:15:58 GMT  
		Size: 41.0 KB (40992 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; arm variant v7

```console
$ docker pull postgres@sha256:92bd0560af42b16ab06f983e22e0cafd633d8732be201fb387f9da15e72fa0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.3 MB (85325489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e277f9422bfefc28491b623f830516edd54106a7b2fcb75de1486d5cabe4f1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:16:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:16:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:16:45 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:34:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:34:27 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:34:27 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 19:34:27 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 19:34:27 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:40:35 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:40:35 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:40:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:40:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:40:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:40:35 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:40:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:40:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:40:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:40:36 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:40:36 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:40:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cad30db35621476ae784dacab459455e152597fac904411058f798b6eea418`  
		Last Modified: Fri, 14 Nov 2025 19:20:06 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf537d6eff6a67fa6789119442be210c161af94e4296737f7b382df34fcd6e1`  
		Last Modified: Fri, 14 Nov 2025 19:20:07 GMT  
		Size: 886.1 KB (886109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4011ac9e425ecf64d2c9f00c3ff787853bc9b72d79946466be8b339712f03a`  
		Last Modified: Fri, 14 Nov 2025 19:37:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac5d94974aca1e13f291a1e519e7ec8032a62ea164ef6868d1e029fd5c5b372`  
		Last Modified: Fri, 14 Nov 2025 19:41:06 GMT  
		Size: 81.3 MB (81323476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67461c0b2df4c7955698b9ce84f00d391c10c0429a538d28c8d94ab80a9c085`  
		Last Modified: Fri, 14 Nov 2025 19:40:55 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ced2ec1b6e405c66ed827f12d6dcc7acb937176a6397148b70cf252d9e8275f`  
		Last Modified: Fri, 14 Nov 2025 19:40:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0411bb106fd14010faf8aaedee490350cd93fb4760acdafb8638e4f4ff9ed8`  
		Last Modified: Fri, 14 Nov 2025 19:40:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1949d6fe7154e9ac8663ddd6f2fb6e3e2d029d79358ed2ae9335d0ed246e783a`  
		Last Modified: Fri, 14 Nov 2025 19:40:55 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba77cbb4b389c85b4978a22b9740b055c5c61620e79938eb0c9d836b04455f7`  
		Last Modified: Fri, 14 Nov 2025 19:40:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:264c6e8c433905ea2064b479acb3b2b98310b14f9c6a7f12ae0160e05686bf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.9 KB (639915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8a0981ec8a68abbecac73d6427cff28a0ed757a9355bed5ebd039c600ce3c6`

```dockerfile
```

-	Layers:
	-	`sha256:462a24e458d30d35e0cdc8b2b74a0c025d0cde2038b20bd6045ce449d1c8a9f5`  
		Last Modified: Fri, 14 Nov 2025 21:16:01 GMT  
		Size: 598.7 KB (598708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40c2afb9b22fba0b5ea56498cf107f617a0af4046bcd777bbbb91381194aaf89`  
		Last Modified: Fri, 14 Nov 2025 21:16:02 GMT  
		Size: 41.2 KB (41207 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:1028dae7a17158d11aa3fb8f644d975b5b5dbf139ce6c9a41302baa5e36e9ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106520646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6df89b25e5a1aaa6121092772b4c2f008bec4554f3b17fe82bb0c3cca14350a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:19:42 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:44 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:19:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:19:44 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:19:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:19:44 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:19:44 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 19:19:44 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 19:19:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:22:27 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:22:27 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:22:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:22:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:22:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:22:27 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:22:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:22:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:22:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:22:27 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:22:27 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:22:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5adf673bcc2e8cc91c1b7e7a81103d62bcdba6a5cbbef376c0089a1c3cfcf12`  
		Last Modified: Fri, 14 Nov 2025 19:22:48 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d27f68fedb603cc167ae1ed9daf12b018313a9bd35dac0d5142b922eceb9d80`  
		Last Modified: Fri, 14 Nov 2025 19:22:49 GMT  
		Size: 873.5 KB (873466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c42e8f05199a8da8f9f3529c37dbac5dd5116f9058ff5eb0bf9715853d1658`  
		Last Modified: Fri, 14 Nov 2025 19:22:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec44d22a7a36a69ab122281d4de78e54532fb3de82aa34a4e9d712acb793ed5`  
		Last Modified: Sat, 15 Nov 2025 01:06:56 GMT  
		Size: 101.6 MB (101637541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d4afefed537ddfafcd7888f4bb6d193f454e527ba83b99acbfb89fc771ec6a`  
		Last Modified: Fri, 14 Nov 2025 19:22:49 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf70f1dfb178f32a200c66c4f039ba0141bd052b8723f1150d170c114fec3adc`  
		Last Modified: Fri, 14 Nov 2025 19:22:49 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60aef60c9ffa2d8cdf3e9cd5be2b1c5db7ee504df94501e67e09106922210236`  
		Last Modified: Fri, 14 Nov 2025 19:22:49 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeae8bb44c01d941f841d7533f492f99219c9ccd8e8c2925c8bf3c2e9d8b658`  
		Last Modified: Fri, 14 Nov 2025 19:22:49 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67e89a4842b2e5442a0396e11d8569415e4d0f2a041072ffba9403af2b4c0ad`  
		Last Modified: Fri, 14 Nov 2025 19:22:49 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:e079ca930a9a1370838dcb2e770fc9dbf8109f2a9b597f9f6fad84bb992fa658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (639963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6210a1a862e445a4a9f668be1d113353191859ad0de289cee6c72202c356f15`

```dockerfile
```

-	Layers:
	-	`sha256:54b8d42f9c430a3482ca60abe672cd17da6cb9a7f3d82d8cf4e16ba17258a96c`  
		Last Modified: Fri, 14 Nov 2025 21:16:05 GMT  
		Size: 598.7 KB (598720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:469d05abf50480d7ec35eac1740b17c917138790e6ec08d17b92269b5169bfb9`  
		Last Modified: Fri, 14 Nov 2025 21:16:06 GMT  
		Size: 41.2 KB (41243 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; 386

```console
$ docker pull postgres@sha256:c4ca2d91dbf6e1adb23150b9a9d3c247dafc066fcde9e1f95a7a5a1f2d45623d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116793418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c081b77da53dcfe75411f9c18546335366d09121f41043c56e2c1e19882b6792`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:25 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:19:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:19:25 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:19:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:19:25 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:19:25 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 19:19:25 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 19:19:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:22:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:22:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:22:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:22:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:22:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:22:06 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:22:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:22:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:22:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:22:06 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:22:06 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:22:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91764b6f4c92b18f0f505f23ebf66d9b414faec2159cdb646041e7349d446a8`  
		Last Modified: Fri, 14 Nov 2025 19:22:31 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaa0446167490f26362e0c85c9d7d472d8eb91a371285c63e54e418032416cc`  
		Last Modified: Fri, 14 Nov 2025 19:22:31 GMT  
		Size: 890.6 KB (890613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f589ce095b22533a79e45b66936305df0cc412718f02058ae4f3c2a1f27b4c7`  
		Last Modified: Fri, 14 Nov 2025 19:22:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd2167d9a9127e55abf94b85193e73aa2056cf7758ead44427f7885215d7158`  
		Last Modified: Fri, 14 Nov 2025 19:22:39 GMT  
		Size: 112.4 MB (112420810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647cccdf4d33d9fa33d1462e0430a8ccce7b13d287c06e5a18efff2ed06937c7`  
		Last Modified: Fri, 14 Nov 2025 19:22:31 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52943f96bff117458ab16c84361fb250e63dafe5ca6ce547fa12d066e66d54e3`  
		Last Modified: Fri, 14 Nov 2025 19:22:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42da4ed47c3a904fd65dbdf0fd3f343d9f98e73044f35146773d9ee1d7bda875`  
		Last Modified: Fri, 14 Nov 2025 19:22:31 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbcc24479354db465a243ecb3b6d3725b899104c79fc89e7f5ae0bd4f048d43`  
		Last Modified: Fri, 14 Nov 2025 19:22:31 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866493162013e7bda80a17f614b70192ac8e602bd710796f727f5527cc9b5efb`  
		Last Modified: Fri, 14 Nov 2025 19:22:31 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:64f736645a85375782b4688d6ebdbb0cdee2fde7b6872ea11f248779032c26ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.7 KB (639694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a563ad0cd05142a95d3aaeff41b5d7513440adf3d3042413e31ed06a71b522f`

```dockerfile
```

-	Layers:
	-	`sha256:0953cd79e277d18140081bc5580a3987531f572f7a54ba06a3cb66b41102dbc5`  
		Last Modified: Fri, 14 Nov 2025 21:16:10 GMT  
		Size: 598.7 KB (598673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f044e867085805c7ca950220f4d750f2e0e0c32e758956a8a0163a30fbcb4303`  
		Last Modified: Fri, 14 Nov 2025 21:16:10 GMT  
		Size: 41.0 KB (41021 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; ppc64le

```console
$ docker pull postgres@sha256:055eb6e36e3938c5a8e75ca08bbd5de01b59982670c61faaf46d8d094f9c6a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94448415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b9665609e9ca943bf24a5d805a9d2b409c3326a393bed50967978d92e6e0a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 21:12:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:12:34 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:12:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:12:34 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:12:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:12:35 GMT
ENV PG_MAJOR=17
# Thu, 13 Nov 2025 21:12:35 GMT
ENV PG_VERSION=17.7
# Thu, 13 Nov 2025 21:12:35 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Thu, 13 Nov 2025 21:12:35 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Nov 2025 21:25:54 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:25:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:25:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:25:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:25:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:25:56 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:33:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:33:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:33:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:33:02 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:33:02 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:33:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c0b8f6a3078f16e9ad43953c7b9b3aa5eeeb60fdea99603db285f4ea397529`  
		Last Modified: Thu, 13 Nov 2025 21:16:11 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30251641c2ae62ada139f8dd51fc147a2ee91199d0db457c3045be6d77e93cb4`  
		Last Modified: Thu, 13 Nov 2025 21:16:11 GMT  
		Size: 879.0 KB (879023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b494261e21b5f1b6c58fd626878b1156eed0066037ce88a4bb43335ef2da2a9e`  
		Last Modified: Thu, 13 Nov 2025 21:16:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5751de740686a5fb987f7b726d8e3612d9d3c7da0c536aff37e85de3cacb8516`  
		Last Modified: Thu, 13 Nov 2025 21:26:52 GMT  
		Size: 90.0 MB (89978017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410f1c6ab68cbae85e5e17a35e914d5a9447947286f59402a0b2bf84f8cc438a`  
		Last Modified: Thu, 13 Nov 2025 21:26:40 GMT  
		Size: 9.9 KB (9889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794e165ee9d7f6d3aa6da86629a10f818413742be9a340d814a2e6eab757d13a`  
		Last Modified: Thu, 13 Nov 2025 21:26:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf370a736d703652f480e39fd98bce723f7b3e4fa9c33b13a633f8cadcdc7479`  
		Last Modified: Thu, 13 Nov 2025 21:26:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f87a0ce952c99c61c92d6dcffabeb880de5917455bee6b6caffc6b62ca8a39`  
		Last Modified: Fri, 14 Nov 2025 19:33:28 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f244a5fda73b10c072a634a75b45e72471bbd8fa31f09edba2abf3ecca20b6`  
		Last Modified: Fri, 14 Nov 2025 19:33:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:04ca73d774c981694a2f880e0ed9f4e8ce41d3774d31d77b294d78764bf4494e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.2 KB (636195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9eb89ea942ac7f632fee60820ca2ec063bc01690da757b04a56ea761397d00`

```dockerfile
```

-	Layers:
	-	`sha256:c377aac02ff33c059b6563ed712e1b9a922f5b2ac1422c9e34a3670092e435a4`  
		Last Modified: Fri, 14 Nov 2025 21:16:15 GMT  
		Size: 595.1 KB (595097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3ba2f7eee06ef541493f72e16819aa4867628002c7a404b72aa0634f81652bb`  
		Last Modified: Fri, 14 Nov 2025 21:16:16 GMT  
		Size: 41.1 KB (41098 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; riscv64

```console
$ docker pull postgres@sha256:63698a937206cf10dfc4f21643082116e686432f68503a6c9ec614a9b69c6eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110714813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c5513f1caaf5dae1f3a58cfe155c10d8e60cfb9ee52df51775fbf44737c4d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 01:03:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 01:03:30 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 01:03:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 01:03:30 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 01:03:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 01:03:30 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 01:03:30 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 01:03:30 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 01:03:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 15 Nov 2025 07:36:49 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 15 Nov 2025 07:36:50 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 15 Nov 2025 07:36:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 15 Nov 2025 07:36:50 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 15 Nov 2025 07:36:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sat, 15 Nov 2025 07:36:50 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 15 Nov 2025 07:36:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 15 Nov 2025 07:36:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 15 Nov 2025 07:36:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Nov 2025 07:36:51 GMT
STOPSIGNAL SIGINT
# Sat, 15 Nov 2025 07:36:51 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 15 Nov 2025 07:36:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f874295bfcd01a87ee99265d45f0786d35242cd9d53bc2744cb330bf3be277f5`  
		Last Modified: Wed, 08 Oct 2025 21:19:05 GMT  
		Size: 3.4 MB (3351001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d4c921b3ed022f985d73e7f31999f7feffbff93e43e48a31fb3d653c71c29b`  
		Last Modified: Fri, 14 Nov 2025 01:56:49 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93c9f84f05edcfc62e25277a7096f6750549ddbd38375e1f948b36ed148c780`  
		Last Modified: Fri, 14 Nov 2025 01:56:49 GMT  
		Size: 866.6 KB (866595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c13a51f1d0427de8f9cb631abd18e48ad84d0b2af918da953d2387df7d7a57`  
		Last Modified: Fri, 14 Nov 2025 01:56:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645e2056a2a904e04dc3f1bf2955627f033070175ece78549be613c77ed3769f`  
		Last Modified: Sat, 15 Nov 2025 07:40:16 GMT  
		Size: 106.5 MB (106479911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb4b976b63766863329b7748f9aa4a2d94c427761c3b14c0193e9e65baa6227`  
		Last Modified: Sat, 15 Nov 2025 07:40:05 GMT  
		Size: 9.9 KB (9891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e3f1ee551635934f3dc9f6e92b4f16e16631680ecd43b311cd68bbee6284fa`  
		Last Modified: Sat, 15 Nov 2025 07:40:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec581b8a05ac150ad41154309e81551500cef7fe9d7e0827e082c3fe73492d0b`  
		Last Modified: Sat, 15 Nov 2025 07:40:05 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117b6a2a53c432f6a581c8b7b04a997af92a7404c4038f21bcf75f954f3a06d2`  
		Last Modified: Sat, 15 Nov 2025 07:40:05 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94732595d917cfe91d40e54296faac7689402906c2a07dfac3c4582bbfd89521`  
		Last Modified: Sat, 15 Nov 2025 07:40:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:866bcecd71bc445fafcdcaf2ec15d4bbdebce335dce0f903abdfe06b232a41c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.9 KB (637859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61844c8361209628dcd77340538396aec551ec931dce13d9b25aa26790862caa`

```dockerfile
```

-	Layers:
	-	`sha256:1168d2cdfbbc324a8fcb25751c9f4b03205a73fcce919e9eef2c9a3d92fcc7da`  
		Last Modified: Sat, 15 Nov 2025 09:08:57 GMT  
		Size: 596.8 KB (596755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9daca7a28473181e70c32a99c6e0faa1ef7baed3a5c2ee41e23751cd52ba2535`  
		Last Modified: Sat, 15 Nov 2025 09:08:58 GMT  
		Size: 41.1 KB (41104 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; s390x

```console
$ docker pull postgres@sha256:f57f01ddd400ae078d1eadb9ddf43864e86a9818f9fdc05a408e44fc76d875ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119239613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0a42c5b49cbea07215e78e4fd534a81928ff7c9ccfe77b13aa0bb1d26cb114`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 02:35:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 02:35:46 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 02:35:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 02:35:46 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:16:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:16:00 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:16:00 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 19:16:00 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 19:16:00 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:34:00 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:34:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:34:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:34:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:34:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:34:01 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:34:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:34:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:34:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:34:01 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:34:01 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:34:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98106086f0ed59b669efcd76d96017fb18c0c48b7c8297a0f11a12a86f50392`  
		Last Modified: Fri, 14 Nov 2025 02:38:49 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df8b1951d577c6837ce27874e651cf3003ad2451fc392aab553d758e5103bb4`  
		Last Modified: Fri, 14 Nov 2025 02:38:48 GMT  
		Size: 894.4 KB (894393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3bd4cfb16494f2b26e1a6bc5c7e360e1233dd1e0d14de4f7b4a7a921a9ebb4`  
		Last Modified: Fri, 14 Nov 2025 19:20:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c2921208169aa9d18c2b71f44d9bdab67eb7366230a379d559c2ae4c7a40f5`  
		Last Modified: Fri, 14 Nov 2025 19:34:39 GMT  
		Size: 114.9 MB (114861504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651427c6d6b8c73d975d4d15c2b48aa146ed1f73b616f7f53b7b6b5695034f16`  
		Last Modified: Fri, 14 Nov 2025 19:34:30 GMT  
		Size: 9.9 KB (9880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ce35638f621a713ff511e6ac3d7d44bf0b5db09a5dbf8f13c4c138f8942337`  
		Last Modified: Fri, 14 Nov 2025 19:34:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabb74a05fadb7e670f65b45907d750e948c29f5daa35758bf4a2e5d8132330d`  
		Last Modified: Fri, 14 Nov 2025 19:34:30 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85f68762bf95f0889315bacb8b714929e06bc5dff4de6fe6fd695a084b895a5`  
		Last Modified: Fri, 14 Nov 2025 19:34:30 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1407368b667dd2404740164d450f5ac80c884a3de68ae9d1147507488506b27`  
		Last Modified: Fri, 14 Nov 2025 19:34:30 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:1a4bdd17078a3c508db784252ed829f583fdd6bd5c3515f3266f9754a84892d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef699f5682456b641f8ccd2a766deef057e7a008e1be0e2d9c5462794c51f755`

```dockerfile
```

-	Layers:
	-	`sha256:81dcde00971bce08e5d5c1b2f23137d7f23d138beda36334b1e13f16a0739893`  
		Last Modified: Fri, 14 Nov 2025 21:16:21 GMT  
		Size: 596.7 KB (596737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c12de95c3ad17df2e5bf30f63004339f7734cf04ff54c43c87b7886511660f4a`  
		Last Modified: Fri, 14 Nov 2025 21:16:22 GMT  
		Size: 41.1 KB (41058 bytes)  
		MIME: application/vnd.in-toto+json
