## `postgres:18-alpine`

```console
$ docker pull postgres@sha256:154ea39af68ff30dec041cd1f1b5600009993724c811dbadde54126eb10bedd1
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

### `postgres:18-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:97f65d288c6f4575749bc69715c4359657a371f455b0308737fc3a458f7d7a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111492449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678d990e0468542b92ccd9f959ce24e844a42e49df092e0d8f8ed6f3a42a3210`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:18:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:18:35 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:18:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:18:35 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:18:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:18:35 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:18:35 GMT
ENV PG_VERSION=18.1
# Fri, 14 Nov 2025 19:18:35 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Fri, 14 Nov 2025 19:18:35 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:21:10 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:21:10 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:21:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:21:10 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:21:10 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 14 Nov 2025 19:21:10 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:21:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:21:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:21:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:21:10 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:21:10 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:21:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aaf2c1f39bacd1e78a0b41e8387e8c4efa7a719f88339f65be885c29b4a32b`  
		Last Modified: Fri, 14 Nov 2025 19:21:34 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae6d252b40f7e6b528f0973dc70706c840ddb8ccb019fc91e9d164bcd0f2c3`  
		Last Modified: Fri, 14 Nov 2025 19:21:34 GMT  
		Size: 918.3 KB (918298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90d8c5ae539f8978634783e0c2d7843afa0316fb7c9e2cd64743ff0a4563f`  
		Last Modified: Fri, 14 Nov 2025 19:21:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58703585b9c72de02049d0db00a7b8703a1880554649d3fcf61447a8abea266`  
		Last Modified: Fri, 14 Nov 2025 19:21:42 GMT  
		Size: 106.7 MB (106745499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3174f2a40dc7a5e962aea534d601f04d377ac81ac06eef0a9bb31bd52a57f63c`  
		Last Modified: Fri, 14 Nov 2025 19:21:34 GMT  
		Size: 18.8 KB (18776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4eaf63327c27001f4d097d8334aacdd4a5372c17f9900980cd2ab43534e04b`  
		Last Modified: Fri, 14 Nov 2025 19:21:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b67a2fbf223e633c5daf0b19d4f8f8e06aa6d62f1cbbb3b30f9fe1003e5a024`  
		Last Modified: Fri, 14 Nov 2025 19:21:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c5971200e232264ffae2554bd86b147b4d9a114a67454c18fe7a080ddd0047`  
		Last Modified: Fri, 14 Nov 2025 19:21:34 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c312a93b89a06cbcfe5c97d007b4f09612022bdd44c82a76f53ad7ff66e320f`  
		Last Modified: Fri, 14 Nov 2025 19:21:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:5e6815954be61f8337631e623625fb645ab8d5d6a5fc70cba09ee123c5247cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.3 KB (642278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ae4e076dd7149e00bac86106105eb031b96e7c86ab019a30d02406d4fb9b82`

```dockerfile
```

-	Layers:
	-	`sha256:ec5c9fe1cb998a0039624ecfca1809692079598292a185f2c63d49a443f85fed`  
		Last Modified: Fri, 14 Nov 2025 21:17:48 GMT  
		Size: 599.2 KB (599166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df8d8a977a40e8b5c8e675501153bfe305b3265d5ad85b860056a2219bd784ac`  
		Last Modified: Fri, 14 Nov 2025 21:17:49 GMT  
		Size: 43.1 KB (43112 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:f008bbd0c3420f854760104f6c3b773a8d50ab3b220d2a989c3eed689e2f00f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91078418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9dccfa1ce3f85f99256332fdf65af2e7a0c3103211e7caaba1e5b25970e61c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:35:02 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:35:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:35:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:35:07 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:35:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:35:07 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:35:07 GMT
ENV PG_VERSION=18.1
# Fri, 14 Nov 2025 19:35:07 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Fri, 14 Nov 2025 19:35:07 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:37:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:37:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:37:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:37:47 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:37:47 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 14 Nov 2025 19:37:47 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:37:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:37:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:37:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:37:48 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:37:48 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:37:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff394fcf6f7178033c7c58216211e2ab0860f1a390a7687ede66b0574d0858b8`  
		Last Modified: Fri, 14 Nov 2025 19:38:10 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25ff5be3dbe79b60122e717c8fd55fca21449ac3798e8687fdae2c833035d51`  
		Last Modified: Fri, 14 Nov 2025 19:38:10 GMT  
		Size: 886.1 KB (886131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958fe918dbc374454fb323254be3cc813f912ed2360cf27a445e13b30719f4de`  
		Last Modified: Fri, 14 Nov 2025 19:38:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a064e6c4a8eebe89e37abe3c4303888096099d49ae866ec077d3d2b72392ced8`  
		Last Modified: Fri, 14 Nov 2025 19:38:19 GMT  
		Size: 86.7 MB (86662013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9803ff5dce234d0e734f46c1801eca009f8d3306178b6335aae950232a3ca6`  
		Last Modified: Fri, 14 Nov 2025 19:38:10 GMT  
		Size: 18.8 KB (18775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533bbaa0934a8b15a56443da6104fa113059fd48ab9385802bb9c8bc68363371`  
		Last Modified: Fri, 14 Nov 2025 19:38:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c53cefb3e44c94cd80ef73890730340bb49128565de14667bdfbbd396bf473d`  
		Last Modified: Fri, 14 Nov 2025 19:38:10 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749fa0c559b8ee4bc638cbbb0f9b090c31b658b8ab412e4668486b336fb11487`  
		Last Modified: Fri, 14 Nov 2025 19:38:10 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17f3d13060740dec00ce76705e74a9fd44f055fd1982bc6e481261360e06599`  
		Last Modified: Fri, 14 Nov 2025 19:38:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:7add49d60213736b514a7e05851ff370c682f97e42cf04fb94bd94d6d386ee62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 KB (43078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a038bf35051756ce9c83fef0751aae6a528408f823b2bee326bafd3003dedcc2`

```dockerfile
```

-	Layers:
	-	`sha256:aff93e6cfe02699a0c750b98402d5983a1717020287a4b7d6a5c038bc622c165`  
		Last Modified: Fri, 14 Nov 2025 21:17:52 GMT  
		Size: 43.1 KB (43078 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:295921cf418f1f9ad3a053cd67c8a6e04b7c36b103852d699e620a72059b0788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86288551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6607554f99e98eb2c0b4e3ea3db4d23ca105d2656bdda9597adbe7a8324afb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:19:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:43 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:19:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:19:43 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:19:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:19:43 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:19:43 GMT
ENV PG_VERSION=18.1
# Fri, 14 Nov 2025 19:19:43 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Fri, 14 Nov 2025 19:19:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:22:21 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:22:21 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:22:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:22:21 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:22:21 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 14 Nov 2025 19:22:21 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:22:21 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:22:21 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:22:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:22:21 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:22:21 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:22:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368f1ccd2aa1caab51a6cd7f373b5058c579c1b25771ad62db863415e11fa748`  
		Last Modified: Fri, 14 Nov 2025 19:22:45 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa859220b604264834be4533f0ef561b815eea8511d5d521e4706d135e73d2f6`  
		Last Modified: Fri, 14 Nov 2025 19:22:45 GMT  
		Size: 886.1 KB (886134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745770c73d8ebe9b8a700a6c4b8a1f41f99655647083c6f437dc93534d19af60`  
		Last Modified: Fri, 14 Nov 2025 19:22:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd6ccfaf969415240ec0034313a6276c497093941c874354d03696f73a84186`  
		Last Modified: Fri, 14 Nov 2025 19:22:49 GMT  
		Size: 82.2 MB (82154672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58606311b25ebc1fc9c59cdd6eafb283c877e6c1b9abb5a6a09e14131eeaaf66`  
		Last Modified: Fri, 14 Nov 2025 19:22:45 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2489b3b70a7bb9c116c8a685dfdd875caabaa33e8bbd0929ee15f33573b995`  
		Last Modified: Fri, 14 Nov 2025 19:22:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90e2c188cba3abf79e8114a767b15436cba671d29e2ac2913a432ff25d549e1`  
		Last Modified: Fri, 14 Nov 2025 19:22:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831eb96f88a342b23f998109a3377102cb4521da38b3ad866a88b7c0e0c1327b`  
		Last Modified: Fri, 14 Nov 2025 19:22:45 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897872400e3c5a3c67f4830a17ce5ade1b6afea14f802a001d3cc69e0b41d1f`  
		Last Modified: Fri, 14 Nov 2025 19:22:45 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:2001f7d0fdacbfca5bfcbbe44c0ca303191e1af266275e245991a92778e4359d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.5 KB (642511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42685b946d40462a2b5080564eda7f1b0cf64c05e3d902b63b5d0845a967a34c`

```dockerfile
```

-	Layers:
	-	`sha256:3c20ce52d098ccfe11bb936d130891d2d216d5d95f09d11b5d9628f905888f21`  
		Last Modified: Fri, 14 Nov 2025 21:17:55 GMT  
		Size: 599.2 KB (599218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c595441f369a054c9c1550c06eb9fb0dd7c8f91eec5fffa25ad3d274658da044`  
		Last Modified: Fri, 14 Nov 2025 21:17:56 GMT  
		Size: 43.3 KB (43293 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:044eb27ebddc4084241a60ebb9992e64cf79d47b3caf60644e4f0bd575da7b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107444947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860724d35cb7b6ee5e51243a1435b28ce315c58ca8126fad32ad673b51c45587`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
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
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:19:22 GMT
ENV PG_VERSION=18.1
# Fri, 14 Nov 2025 19:19:22 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Fri, 14 Nov 2025 19:19:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:21:43 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:21:43 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:21:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:21:44 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:21:44 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 14 Nov 2025 19:21:44 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:21:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:21:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:21:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:21:44 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:21:44 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:21:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cee4289f99ed82395878fa6e50b8e6727b29b0b76093a43aec26bd24eb6063`  
		Last Modified: Fri, 14 Nov 2025 19:22:07 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341c4fd00db912df287b90a0cc87a6b04ac37949cab8cd33a0e18d1b00142752`  
		Last Modified: Fri, 14 Nov 2025 19:22:07 GMT  
		Size: 873.5 KB (873491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff91185e6f25c5a0e5e8e8b2e87697477d5d440d5b75c2a92a5829cd68938c5`  
		Last Modified: Fri, 14 Nov 2025 19:22:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6025a65f887fd0569853a486605dba1a10fd67cd97574d487719cdce0b0e3f82`  
		Last Modified: Fri, 14 Nov 2025 19:22:20 GMT  
		Size: 102.4 MB (102407201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8218b3542bcf0040a5da44ccabfe496c689665f2fde473fb8082212e5c9b4afa`  
		Last Modified: Fri, 14 Nov 2025 19:22:07 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776bb81711d6e7f79e525cefab8d4d84abce81a3761e0202bf18fae9d6705b6`  
		Last Modified: Fri, 14 Nov 2025 19:22:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5411a73d612a43ae9edc4f2a9cb7d479e8f640321e6603267eed3cc523560125`  
		Last Modified: Fri, 14 Nov 2025 19:22:07 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fa4cbe1f49044a113eac3ad747d982dd4161638648765dcf867d1d5c1133c3`  
		Last Modified: Fri, 14 Nov 2025 19:22:07 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f13356b3d8d1b8d7fbea7af41f44b0a7819aeeaa920356a156f230011e0a66`  
		Last Modified: Fri, 14 Nov 2025 19:22:07 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:95bc60d64f19d0f910f7088dbf7964c88027fde6ab3a9f21d5cf313dd6ba31a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.6 KB (642590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3604142e91f3ba121ef5f017d75e3adbb7a653f4444d358f8a9aecd6333a587`

```dockerfile
```

-	Layers:
	-	`sha256:76c19ed381fdc9b313978984c9bd8249d88dfa5d45c9345c7f14ca49065dcdcf`  
		Last Modified: Fri, 14 Nov 2025 21:18:00 GMT  
		Size: 599.2 KB (599246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c894a73e7ef649329858a9934094097bc370012cc6dc55c07f61cc614fb46afb`  
		Last Modified: Fri, 14 Nov 2025 21:18:01 GMT  
		Size: 43.3 KB (43344 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine` - linux; 386

```console
$ docker pull postgres@sha256:3b327dec55d1ebb677aec953782888c454f3197d6b70a0f150a689939360bc6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117870237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9944878e93a578fdf0cb0cbf5f8d0732d03bcebec7164ba15f028fda5b561775`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:19:27 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:30 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:19:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:19:30 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:19:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:19:30 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:19:30 GMT
ENV PG_VERSION=18.1
# Fri, 14 Nov 2025 19:19:30 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Fri, 14 Nov 2025 19:19:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:22:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:22:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:22:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:22:09 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:22:09 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 14 Nov 2025 19:22:09 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:22:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:22:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:22:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:22:09 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:22:09 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:22:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d719b26b9e07e42b0a9ad755948257030745df2073b55842909bea67ebd5f5f0`  
		Last Modified: Fri, 14 Nov 2025 19:22:24 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3deb64144ae7fc24d80d5ae5fdc680a36fcfcdef9f53c3521612013504929b2`  
		Last Modified: Fri, 14 Nov 2025 19:22:24 GMT  
		Size: 890.6 KB (890643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfa2c54f3bc920d58feca47341fc1fe73706f59581976841bb088c2d1def1d2`  
		Last Modified: Fri, 14 Nov 2025 19:22:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a9afe701c1509c1df48e2fd808674142e20e8d35be32d3c79ba65d11437abd`  
		Last Modified: Fri, 14 Nov 2025 19:22:42 GMT  
		Size: 113.3 MB (113334469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20b5acef1f9afb1b426cc265a606180a621ba9ee5747aed7d7f5065365184c3`  
		Last Modified: Fri, 14 Nov 2025 19:22:34 GMT  
		Size: 18.8 KB (18775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7524010066696f17eae95434124eff094322496a29f8c6329121305c4900ad2`  
		Last Modified: Fri, 14 Nov 2025 19:22:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04192127944c79fd705ddeb4e743da660cf2dc2418ccda9d78eebfdb3c52f16`  
		Last Modified: Fri, 14 Nov 2025 19:22:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b318f0b27558801f16a4b274bb5d753b977a8b1a715413328ddbea458f738bb`  
		Last Modified: Fri, 14 Nov 2025 19:22:34 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fe61e9176f75b4d92b30dfefe5e0a6b386103b0d8eb5405a91ec787e0cd96a`  
		Last Modified: Fri, 14 Nov 2025 19:22:34 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:05ea13bf809ea2f65bd71d823a908471e359b0af7e38949697c51a26f6bd83d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.2 KB (642187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67388080aa931abe40ba421d3c556a13f0e4dbc318bf37244af1fbfb6ed6fc4f`

```dockerfile
```

-	Layers:
	-	`sha256:fbb711ae47650163d58fdfa3996d7120b779e813e4bfb40efed90c0a97efcfe4`  
		Last Modified: Fri, 14 Nov 2025 21:18:04 GMT  
		Size: 599.1 KB (599131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a57c07c7aec66ab50de72ccdabc90b03b5025c68d3ac94f10dd0e524052a4fb8`  
		Last Modified: Fri, 14 Nov 2025 21:18:05 GMT  
		Size: 43.1 KB (43056 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:7e8d03fb0aeff067146b793562c2515f7b5631dd696f172de829b6cb5af99c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95425153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37da1a7128ba2aa0fd80a91bb26a5dbd789a277aa8721a8c0d925d74ff3c0bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 21:08:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:08:47 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:08:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:08:47 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:08:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:08:48 GMT
ENV PG_MAJOR=18
# Thu, 13 Nov 2025 21:08:48 GMT
ENV PG_VERSION=18.1
# Thu, 13 Nov 2025 21:08:48 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 13 Nov 2025 21:08:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Nov 2025 21:11:34 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:11:34 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:11:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:11:35 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 13 Nov 2025 21:11:35 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 13 Nov 2025 21:11:35 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:31:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:31:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:31:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:31:15 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:31:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:31:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1c66900cf5c9e7948109598cbb47be0e8fe1ad48b504966e9f3463570cfe1`  
		Last Modified: Thu, 13 Nov 2025 21:12:21 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab349f0bd809fd81036764b04799e3daf5f5b6a3591cc2e794e8c13ea16dec`  
		Last Modified: Thu, 13 Nov 2025 21:12:21 GMT  
		Size: 879.0 KB (879032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c1c42c9dff88c0650506b97e1cc305b15e4d760dcf73fd2e765885d7d26ebd`  
		Last Modified: Thu, 13 Nov 2025 21:12:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e5ef6c3a567b22449e41819427dce8e419ce391a045cd6fedbdce13c709ab2`  
		Last Modified: Thu, 13 Nov 2025 21:12:35 GMT  
		Size: 90.8 MB (90787669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9652c072bf42e8406fa9fa1cfec7c36538e162bcbce5c3e9591a8e3ea903dfcf`  
		Last Modified: Thu, 13 Nov 2025 21:12:21 GMT  
		Size: 18.8 KB (18780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7135e20c260807833f01640ae43daa4c716f7e8e44c692e7536c509874f90e`  
		Last Modified: Thu, 13 Nov 2025 21:12:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e4846336cb0a2df1fb011ef9e1e5845c071f34bc174d43c4e912bd259ed7e7`  
		Last Modified: Thu, 13 Nov 2025 21:12:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eb5b4082a981577cc53cc85bcce324350542dbd9492d2fca956c4f87ac0765`  
		Last Modified: Fri, 14 Nov 2025 19:31:40 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c797df3c89554e42ee6eed8f4cbfb3849ad98d6b26a4194093399fab41ef8f27`  
		Last Modified: Fri, 14 Nov 2025 19:31:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:ef5bf260082b8db7cc045c88c2faaa0e6a6d028656d7d3c66a12231e36b9f734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.8 KB (638775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab23ef6be3a16cedc1b2ce79729f4e6d27ce8d93217bb571fbe5b69a24437a09`

```dockerfile
```

-	Layers:
	-	`sha256:ddf8af98ad32d0b59e6b137238a9fc260ba89a13cee62ffe6c29cc64a04bb1f0`  
		Last Modified: Fri, 14 Nov 2025 21:18:09 GMT  
		Size: 595.6 KB (595599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:469146c3f059e9760d2ffb458f1928b023d5a3e149bc73f922e41024298488ae`  
		Last Modified: Fri, 14 Nov 2025 21:18:10 GMT  
		Size: 43.2 KB (43176 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:cd561d67d58eff17a23960defdf93fdeda0653e9835bbde1618872fd7d7e47c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111689747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b329d8a5bfb13415dc2f1791ada6434475dd45d16ae4c8cd9c35f98830a01f56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 00:10:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 00:10:13 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 00:10:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 00:10:13 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 00:10:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 00:10:14 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 00:10:14 GMT
ENV PG_VERSION=18.1
# Fri, 14 Nov 2025 00:10:14 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Fri, 14 Nov 2025 00:10:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 00:59:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 00:59:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 00:59:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 00:59:17 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 00:59:17 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 14 Nov 2025 00:59:17 GMT
VOLUME [/var/lib/postgresql]
# Sat, 15 Nov 2025 06:36:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 15 Nov 2025 06:36:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 15 Nov 2025 06:36:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Nov 2025 06:36:59 GMT
STOPSIGNAL SIGINT
# Sat, 15 Nov 2025 06:36:59 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 15 Nov 2025 06:36:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d16d13f9766542076f489b4bde8f2b9299f759730ca1132f12a478b4ab5317`  
		Last Modified: Fri, 14 Nov 2025 01:02:37 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f681bb079be6f40bd7adede139f20494c17a8116703e2d4d80cdafbeac44ec0f`  
		Last Modified: Fri, 14 Nov 2025 01:02:37 GMT  
		Size: 866.6 KB (866631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e52b4b277261b1ac3d2524fe15cdca0bad28cdd8d178e74d9fcdc38870c8f45`  
		Last Modified: Fri, 14 Nov 2025 01:02:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7656ef2ae4f61457d7cfd68b5635d50877236dffae16b46f44fb9c20ab0e73`  
		Last Modified: Fri, 14 Nov 2025 01:02:51 GMT  
		Size: 107.3 MB (107281663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e530d35ed7c116d15940760020946e930ad0402e3d95938a396794d67a22a7`  
		Last Modified: Fri, 14 Nov 2025 01:02:37 GMT  
		Size: 18.8 KB (18775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88e6498f2d02c6f4ddc51775a99146fa7c99d263d7c94de48ae336d2dcea026`  
		Last Modified: Fri, 14 Nov 2025 01:02:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e773c288b6d44465a77443e17289be11d0875cd4c9a86f66a4934066ca884229`  
		Last Modified: Fri, 14 Nov 2025 01:02:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b9bb2fde25113c3fccf19c47246dfd7532abcd48573359d892da333753ced8`  
		Last Modified: Sat, 15 Nov 2025 06:38:19 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800b5f5201ab53d7640bfbe258616c23c6614e4d3a8fafceff4c839f6ea581b4`  
		Last Modified: Sat, 15 Nov 2025 06:38:19 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:673694b39f6068999c183b15003cd6667df694a2e9e4248cff977c02778c96ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.4 KB (640439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd13aee265983d137caf24c96b3bd00741cd2d1eee48cb29f97ebddd401908a`

```dockerfile
```

-	Layers:
	-	`sha256:5d8e9a5a3bfffaf3478d05c0113cb6460a146ec85bde35b1c3c6882118018697`  
		Last Modified: Sat, 15 Nov 2025 09:09:37 GMT  
		Size: 597.3 KB (597257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3084ac3d5cb144d974289a9afc4e8f1632383fbca7a7913951b1c2ef7925f3cc`  
		Last Modified: Sat, 15 Nov 2025 09:09:37 GMT  
		Size: 43.2 KB (43182 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:22f67ee47fae386468edba9fa8a56ca0017310833c2f37531269208e79602653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120281294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12dae8db26118058d480a1a523c50b9e55aeb71b3fc4a34689a93374047bb11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 01:24:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 01:24:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 01:24:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 01:24:11 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:15:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:15:53 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:15:53 GMT
ENV PG_VERSION=18.1
# Fri, 14 Nov 2025 19:15:53 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Fri, 14 Nov 2025 19:15:53 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:19:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:19:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:19:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:09 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:19:09 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 14 Nov 2025 19:19:09 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:19:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:19:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:19:09 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:19:09 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:19:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d27f93166421531fe4a5435a9bca3ea4e7a361893fc542ed1fd5124e07175f`  
		Last Modified: Fri, 14 Nov 2025 01:27:35 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5428b16fd632d91d3982d2d488bfbd69daf3b4db82a5d75683ec8a2731260b2b`  
		Last Modified: Fri, 14 Nov 2025 01:27:35 GMT  
		Size: 894.4 KB (894417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c27c21eb6784d7fdff28110f50d2f82caadfe48875a7c67cae465d1149a4aae`  
		Last Modified: Fri, 14 Nov 2025 19:20:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176ce070e70328e89384be475671776e4ab03fdb343758c6e9948b9dd08dc6d1`  
		Last Modified: Fri, 14 Nov 2025 19:20:26 GMT  
		Size: 115.7 MB (115711442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d01f1f3814c52a13fcd5fb95537386c07edb358a234311d84296a20e0bfca0b`  
		Last Modified: Fri, 14 Nov 2025 19:20:02 GMT  
		Size: 18.8 KB (18772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c9ca2238750abaf05e9619535b8ab09e5ea5ced1112164b32abb41c3a1f327`  
		Last Modified: Fri, 14 Nov 2025 19:20:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657ec0f0305a39afd4957a5f2cc0e8633a7b793a4ca5ba7c4e35d53835c976c6`  
		Last Modified: Fri, 14 Nov 2025 19:20:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06c22424e06480099080c824bf20e9f3b926ed1d1265649a1210373e4076c06`  
		Last Modified: Fri, 14 Nov 2025 19:20:02 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cdb38db0f382d7f0de99718bc1a16099deab005f57ae9d82559b56cf8a38f6`  
		Last Modified: Fri, 14 Nov 2025 19:20:02 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:ab33da9d105e1c43731cc5140adf54b0f74d9eddb7984e1452afe8f854e12fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.3 KB (640327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde9792ec8364f79be76a0d3eab20882843f9911fdc294d59d52af7c27b44ca3`

```dockerfile
```

-	Layers:
	-	`sha256:483994a274290b4838522aad6213b586a042252987bf1c11e2125a5861d75aa0`  
		Last Modified: Fri, 14 Nov 2025 21:18:15 GMT  
		Size: 597.2 KB (597215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c5b4274fe96aff9029c72a83399192c16823bef66c904b3a42de5bab5d00d18`  
		Last Modified: Fri, 14 Nov 2025 21:18:16 GMT  
		Size: 43.1 KB (43112 bytes)  
		MIME: application/vnd.in-toto+json
