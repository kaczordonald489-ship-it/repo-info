## `postgres:14-alpine3.22`

```console
$ docker pull postgres@sha256:1bf14357b97fe10f21f2eda7f0d230b2514ab5770ab81cb9cd6cce6750d68b26
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

### `postgres:14-alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:5879f2fb23d535b5092b820a170746784628b64374445ea2f64d715fbe12c811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108076103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ae4f5c34d716949b5b97d1e112d8b3d2f08a5240b7863a7bc061086a449659`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:20:36 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:20:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:20:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:20:38 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:20:38 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:20:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:20:39 GMT
ENV PG_MAJOR=14
# Fri, 14 Nov 2025 19:20:39 GMT
ENV PG_VERSION=14.20
# Fri, 14 Nov 2025 19:20:39 GMT
ENV PG_SHA256=7527f10f1640761bc280ad97d105d286d0cf72e54d36d78cf68e5e5f752b646b
# Fri, 14 Nov 2025 19:20:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:22:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:22:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:22:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:22:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:22:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:22:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:22:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:22:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:22:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:22:41 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:22:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:22:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb422fc4bc6484e6ff4d53571d7616e0d0e10a51659ed0d5164e5bcecd0f5e9`  
		Last Modified: Fri, 14 Nov 2025 19:23:03 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707d0a4aef1b839156ab4e3cb8a71d92a0c960af60370905f0ca2f4861d2f8ca`  
		Last Modified: Fri, 14 Nov 2025 19:23:03 GMT  
		Size: 918.3 KB (918289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e80e64a29b0a2218dd8f9d80d4fc202ea08eec18d3e8130e798ee645bc01f2`  
		Last Modified: Fri, 14 Nov 2025 19:23:03 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a586c6b24e0f4d46c92712af94a9919546b4c49770a1c3c2d528371a843c1aaf`  
		Last Modified: Fri, 14 Nov 2025 19:23:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9804449c68b43d4fa52e66827c4e0ef59fb2f71f15ba87c78d789c80cf5ca947`  
		Last Modified: Fri, 14 Nov 2025 19:23:18 GMT  
		Size: 103.3 MB (103338580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18067747d68dd04575a6e536c1dd7f111a74cadf568bdee0843de62f8a3ea8b`  
		Last Modified: Fri, 14 Nov 2025 19:23:03 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a680840cf056497817d361d632a4811ff4337c1e909bca22e5eb63404e43dfe0`  
		Last Modified: Fri, 14 Nov 2025 19:23:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06196a19fb661af0b7725503cdbdce99f505a223d2790a9b33563045fe427c07`  
		Last Modified: Fri, 14 Nov 2025 19:23:03 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7772876f7d6d37366cfb37df9d5a9a6a6a55f78043e3034f8449b0ea30d2b31`  
		Last Modified: Fri, 14 Nov 2025 19:23:03 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f95bd464c3dbf3307d232ace123c29e84899486216ca4ef489aeaa28ee4978`  
		Last Modified: Fri, 14 Nov 2025 19:23:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:f680efdae773005d2bf4e62a7d424f9a7d3359a18a6c5ee435f3ad714c4543be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.0 KB (641008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8fee6a283193533f382906795de2667ead86f5adf65df6249d1831641af935`

```dockerfile
```

-	Layers:
	-	`sha256:3f04573855adfa9433dfd928bc2b42b7613a4e4670e4271bdf104604d277fb61`  
		Last Modified: Fri, 14 Nov 2025 21:08:15 GMT  
		Size: 596.9 KB (596937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:726328064c5273128039e809851d831199bb3f93b12705f4cf6e5aeceb435ed6`  
		Last Modified: Fri, 14 Nov 2025 21:08:15 GMT  
		Size: 44.1 KB (44071 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:a3b3a556c588f1b4e60af49d44daf0783f845c58bf717b24e2e28ebf45ebd462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87694710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dc8fd995cc0b0f330d7d38ff4c76797a2bdc8c4e9364e62102002609823a9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:19:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:19:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:19:27 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:19:27 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:19:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:19:27 GMT
ENV PG_MAJOR=14
# Fri, 14 Nov 2025 19:19:27 GMT
ENV PG_VERSION=14.20
# Fri, 14 Nov 2025 19:19:27 GMT
ENV PG_SHA256=7527f10f1640761bc280ad97d105d286d0cf72e54d36d78cf68e5e5f752b646b
# Fri, 14 Nov 2025 19:19:27 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:22:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:22:07 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:22:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:22:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:22:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:22:07 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:22:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:22:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:22:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:22:07 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:22:07 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:22:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71ce2b3b7f7ddc1039c9f004388ce31c2abf3b2d5b08b9a3cb7cc57699d4e8d`  
		Last Modified: Fri, 14 Nov 2025 19:22:28 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47321e493578c2760b6b5a71119b14d2c5a35512f369ecdff6e099180a41712`  
		Last Modified: Fri, 14 Nov 2025 19:22:28 GMT  
		Size: 886.1 KB (886132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3760aac5a39191eb9b0c6fea88bd1d633ee380ceb73f4dcbe12a00c8790095`  
		Last Modified: Fri, 14 Nov 2025 19:22:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebc281b3c5c2d7944f35721d3997d1c2165a93fa81152d8b90b1077cf6a97d5`  
		Last Modified: Fri, 14 Nov 2025 19:22:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14865a53152a067b12a024d64ade0d5cdeb7660c261c9874250bd43337f16585`  
		Last Modified: Fri, 14 Nov 2025 19:22:34 GMT  
		Size: 83.3 MB (83287713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bb1f70fd8334f77fd3c073dedb72287fbce2249626833d82d6800ae85c72c8`  
		Last Modified: Fri, 14 Nov 2025 19:22:28 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3176bff9400eedc1546d73cadef09e7df569465afb8904fbccb618c582a505b5`  
		Last Modified: Fri, 14 Nov 2025 19:22:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6f81607d5d00f2d43dd8f3fe585502f037d6af6d5a55c38092a2ac61b15b1a`  
		Last Modified: Fri, 14 Nov 2025 19:22:28 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009eaa489cef77a3536cce63bc178ecd7dc50654cf1e93a20752c673dc01bee`  
		Last Modified: Fri, 14 Nov 2025 19:22:28 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b695e09095b9c681d3c807181f0a3b169d11a04258477c52e25e77e6bf4cc995`  
		Last Modified: Fri, 14 Nov 2025 19:22:28 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:2369e9354a29f13daf9ad2d0319c7b78c98c99422cb5637ec4d55eba59c4b503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 KB (44034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3094e97b90c3554530b91c0e9c7652eb3c2a61312b640e377436762d5a24d502`

```dockerfile
```

-	Layers:
	-	`sha256:d9fc805eba543d509f7bc48274cb66721b01c21340ab69edd8d34f63e43407bd`  
		Last Modified: Fri, 14 Nov 2025 21:08:15 GMT  
		Size: 44.0 KB (44034 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:9244a6740bc2d63c80a3f848c783227cf640c81d62e3feb0f8c09d3ac43f56f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (82991319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bfe813c08e286bf427074c2c748112bea1e6ab46658b964a2a17de3b71d29c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:49:36 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:49:39 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:49:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:49:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:49:39 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:49:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:49:39 GMT
ENV PG_MAJOR=14
# Fri, 14 Nov 2025 19:49:39 GMT
ENV PG_VERSION=14.20
# Fri, 14 Nov 2025 19:49:39 GMT
ENV PG_SHA256=7527f10f1640761bc280ad97d105d286d0cf72e54d36d78cf68e5e5f752b646b
# Fri, 14 Nov 2025 19:49:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:52:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:52:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:52:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:52:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:52:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:52:13 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:52:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:52:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:52:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:52:13 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:52:13 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:52:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a5e34f000a28eab2422684fba29b6a084fa2d661de275bab3ab7b7787ef106`  
		Last Modified: Fri, 14 Nov 2025 19:52:37 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876047bf6400d0ffb967b241ba2ee092fe772ed1c1024938eacbffc254591ba8`  
		Last Modified: Fri, 14 Nov 2025 19:52:37 GMT  
		Size: 886.1 KB (886137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f403e4c7b21d228d189eb05f6fc9cdfb4c24cf0a1bb87bbed870440333d1a43`  
		Last Modified: Fri, 14 Nov 2025 19:52:37 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e9203fa15a63ec29363450844134dafb4958e14650d987d189e3c9e83b6c9d`  
		Last Modified: Fri, 14 Nov 2025 19:52:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a151ac20d9880e1528e01ead74aae742e74b6925024373122991068c6a6895`  
		Last Modified: Fri, 14 Nov 2025 19:52:43 GMT  
		Size: 78.9 MB (78866843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806457fcd6427b9988183f14231620e4e9cfe58103022c0e811732d2acb04827`  
		Last Modified: Fri, 14 Nov 2025 19:52:37 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e67477b3123f2a68e83004384d826a05dba24d00bf3a69b742ddde9585f318`  
		Last Modified: Fri, 14 Nov 2025 19:52:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6a2e8a9a0a930e3556a1f9dd70c04118f296dc7c92e4c21c0f4dcbc0a946e6`  
		Last Modified: Fri, 14 Nov 2025 19:52:37 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea6a3f2297793d4e074f593decfab8e14fbaa593f41ab032f91f1af80253282`  
		Last Modified: Fri, 14 Nov 2025 19:52:37 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7259fac9def7e23047ff1b29d230ac74e5dec270a09c72df9e23d4e483b692ff`  
		Last Modified: Fri, 14 Nov 2025 19:52:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:2a8e72f2b2ef1454279a116d9e614ea31f5196fbb5c64b2c2c91cd68e252578e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.2 KB (641222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85ea5e731a850f02d3c3d24d93e9917907c31bd1ebb639d33dc2cc274240451`

```dockerfile
```

-	Layers:
	-	`sha256:062e135da1ef02c72ca063da7a46a35658d20e41a7c0fd74b028907bcfba93d5`  
		Last Modified: Fri, 14 Nov 2025 21:08:18 GMT  
		Size: 597.0 KB (596973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66c70d933af46d01e9393dd2e1fbce16dfd7ca2595c5f0ba761bbda15fc18c69`  
		Last Modified: Fri, 14 Nov 2025 21:08:17 GMT  
		Size: 44.2 KB (44249 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:1e69c0c1216b4911ffb26c31765ecb53bf3e6929e43527a6707a84e062a04ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104045874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0037c2d3a73256287120a636826727b88f805207a8d65ad7952ad44612e6e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:21:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:21:08 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:21:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:21:08 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:21:08 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:21:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:21:08 GMT
ENV PG_MAJOR=14
# Fri, 14 Nov 2025 19:21:08 GMT
ENV PG_VERSION=14.20
# Fri, 14 Nov 2025 19:21:08 GMT
ENV PG_SHA256=7527f10f1640761bc280ad97d105d286d0cf72e54d36d78cf68e5e5f752b646b
# Fri, 14 Nov 2025 19:21:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:23:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:23:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:23:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:23:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:23:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:23:32 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:23:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:23:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:23:32 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:23:32 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:23:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c56ed6296ed591ce6694e57be98c0684cbe350d43278727be23f9eae8da8ca`  
		Last Modified: Fri, 14 Nov 2025 19:23:56 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd8c67b0867ccea0fc33517194dd355e5280c03bdfbd72b2af0443af7e7b41a`  
		Last Modified: Fri, 14 Nov 2025 19:23:56 GMT  
		Size: 873.5 KB (873487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee06bfb1d41781f2b272d3d343bf3209daf1d3aafc58b71b176c7798c35bf0fb`  
		Last Modified: Fri, 14 Nov 2025 19:23:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927c9a2ec89fbdef5c0074abafbf7576361cafefa0ce58525d008ce2195e5a80`  
		Last Modified: Fri, 14 Nov 2025 19:23:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8d29708435123fd928ebff1db73bf92b2098709cbed88630d086849cc1b33c`  
		Last Modified: Fri, 14 Nov 2025 19:24:21 GMT  
		Size: 99.0 MB (99017542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03395a04ab0aa93572ffdd9728b49e45e9c31df459109ad59f140b30f8b7c316`  
		Last Modified: Fri, 14 Nov 2025 19:23:56 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afad3d4532079e0b0c2afbb221d544db6c32d38379b0a5f5f80852d21617379d`  
		Last Modified: Fri, 14 Nov 2025 19:23:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fdb48aa21bc3bb74460541bb74578044e645cb094c0e8f62e6ccc5f836b79d`  
		Last Modified: Fri, 14 Nov 2025 19:23:56 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67e787d2a6868511535f838b76aa36ef29e67d93eac6f562759d37e9896c5ba`  
		Last Modified: Fri, 14 Nov 2025 19:23:56 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc5857f50b0af997fd1028f266eebdd4604d5cf87c2edbfab083aca1a8805a6`  
		Last Modified: Fri, 14 Nov 2025 19:23:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:c0c4cd2d250b06b9b2d3a443e13d5b321db5f34ab86db434e06ee5549a7b3d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.3 KB (641282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65ddb140b07257ae6b9dcf107666dec667b08dd233cdfb323de78791a2a695`

```dockerfile
```

-	Layers:
	-	`sha256:e2111a6a3a74f754a978d2e4d3d0f9feeac147ebdaf5752b71fe683a6394f863`  
		Last Modified: Fri, 14 Nov 2025 21:08:19 GMT  
		Size: 597.0 KB (596993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79cf98c47da3c5c44dc3c9f51b91d4a036e3d0d5872403b8deb7e0a9261e4788`  
		Last Modified: Fri, 14 Nov 2025 21:08:19 GMT  
		Size: 44.3 KB (44289 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:cfe5c7c7a9416d4e301ed358c09cd6adac48a5f1ff17f39655b29dc778725ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114303351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86cf26346fd47a8ccbc6cc13510318cb97e2acd6b8487285a02cadbb2120198f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:28:18 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:28:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:28:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:28:21 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:28:21 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:28:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:28:21 GMT
ENV PG_MAJOR=14
# Fri, 14 Nov 2025 19:28:21 GMT
ENV PG_VERSION=14.20
# Fri, 14 Nov 2025 19:28:21 GMT
ENV PG_SHA256=7527f10f1640761bc280ad97d105d286d0cf72e54d36d78cf68e5e5f752b646b
# Fri, 14 Nov 2025 19:28:21 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:30:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:30:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:30:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:30:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:30:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:30:44 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:30:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:30:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:30:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:30:45 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:30:45 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:30:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594b7f240740c83c459e6b8182045cdb7973a4e2ed2e319a598dc6826a2b2e89`  
		Last Modified: Fri, 14 Nov 2025 19:31:10 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfa8cfbaafdec0a6ebcab40aad40d334b17b827c11d8a3f0754c69d57b320e3`  
		Last Modified: Fri, 14 Nov 2025 19:31:10 GMT  
		Size: 890.6 KB (890641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb546833f8495d098fa42832cccaccb762fa2716a4764fe7c3a732bc56df3d04`  
		Last Modified: Fri, 14 Nov 2025 19:31:10 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dff932691d408aa4cadf848e59e41b3dde94f56c42e22e5374fca6c21b36f3a`  
		Last Modified: Fri, 14 Nov 2025 19:31:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ddd4c91e1d05ca4f93299f91cafb8141a7424bdf2f41a18e19100ee5701a89`  
		Last Modified: Fri, 14 Nov 2025 19:31:25 GMT  
		Size: 109.8 MB (109776996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3419eb1efd0c92a289d6bd28cd9ae020da14b95c52c28837a3fa6bdfa54e2584`  
		Last Modified: Fri, 14 Nov 2025 19:31:10 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c990af84d11319f7cb3a1d53f96fc3497b912e8f865f6c77800a538bb0a2a4d`  
		Last Modified: Fri, 14 Nov 2025 19:31:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86d8ea507b1db3f5debba656e8d694cef66eddfe68f7034e18637e5454228d8`  
		Last Modified: Fri, 14 Nov 2025 19:31:10 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26da96f343322735eada85c4cdf3598118ea28ac9ab86f5464f4e270aa77fd9e`  
		Last Modified: Fri, 14 Nov 2025 19:31:10 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb7c831270c5b0e18a2312016820a205aa08b31ccf3e43f3f77cd2796ff8c79`  
		Last Modified: Fri, 14 Nov 2025 19:31:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:1d6a6a319b896036a877741a04c350fd52d839aaf742901bdf33647c576a2e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.9 KB (640935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2716b502eccd0865f3f8bc27513c5918df0b2e6e69cff6d5021d62be1a3a21`

```dockerfile
```

-	Layers:
	-	`sha256:0953df3d6d8b4fcdb3aabb47e61cc080d3131391c378699aac76e99f7638d674`  
		Last Modified: Fri, 14 Nov 2025 21:08:21 GMT  
		Size: 596.9 KB (596912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24fd7210379842c84cf75b648ead0479764c1d9688b13b27fc42f11de813b1db`  
		Last Modified: Fri, 14 Nov 2025 21:08:21 GMT  
		Size: 44.0 KB (44023 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:fa17b47e8612b873ee72225446e87c1ce2347c7987736217aa45987fc9347147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91777401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992a4e3f17f22c63738a589c951e8802c8634230b7394ce91470ec643b4f976a`
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
# Thu, 13 Nov 2025 21:29:49 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Nov 2025 21:29:49 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:29:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:29:53 GMT
ENV PG_MAJOR=14
# Thu, 13 Nov 2025 21:29:53 GMT
ENV PG_VERSION=14.20
# Thu, 13 Nov 2025 21:29:53 GMT
ENV PG_SHA256=7527f10f1640761bc280ad97d105d286d0cf72e54d36d78cf68e5e5f752b646b
# Thu, 13 Nov 2025 21:29:53 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Nov 2025 21:52:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:52:02 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:52:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:52:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:52:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:52:02 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:37:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:37:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:37:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:37:37 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:37:37 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:37:37 GMT
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
	-	`sha256:216ca5aa5821ad4995759832f643200c20c8462fdb95c608f5d26acdb0c174cd`  
		Last Modified: Thu, 13 Nov 2025 21:33:31 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644daa0fcb4c064f3b99d3a40b830169255aeae1dfab7dc73c91e48231e1cffe`  
		Last Modified: Thu, 13 Nov 2025 21:33:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426b1065b873cb9d407447b8d02ad35f226424a31feb1535d4835a5a10ed7f02`  
		Last Modified: Thu, 13 Nov 2025 21:52:52 GMT  
		Size: 87.1 MB (87149335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1763648f7ad06a368ffed78e1a670565100988adfb17072458f43f0483558d9b`  
		Last Modified: Thu, 13 Nov 2025 21:52:40 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74920cdffae3be15c03883b16ded0022c97119b09c27b75afd826429d0c8151b`  
		Last Modified: Thu, 13 Nov 2025 21:52:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b009f6e5cd5287c018a2840b591b48642111c1225d6d7fc032eea9f41f48a17`  
		Last Modified: Thu, 13 Nov 2025 21:52:40 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3482a9890f5ea98d0050bca544915abc1b4f63425a378d522d68099f5824a075`  
		Last Modified: Fri, 14 Nov 2025 19:38:07 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c50c0c1477a6bfad90c603789d0712b71b7ee799a5d338c172fa275d4fba725`  
		Last Modified: Fri, 14 Nov 2025 19:38:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:7f7ed603d110426603cdfa81997f86c92a35661a9232124119189c37cf3f829f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.5 KB (637483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b443d3135b4bba65a39c14a407203ba10669a9e737cc6d8fb9c45d97edd66336`

```dockerfile
```

-	Layers:
	-	`sha256:df2c9c2eec5a6185b9a599e9c270c29a06ff0db3b251300c2b4b04f6fe424184`  
		Last Modified: Fri, 14 Nov 2025 21:08:23 GMT  
		Size: 593.4 KB (593358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3730aa9f0fd0d2bc2e60497b473f8febc1e538f5dfad316d2528ed9451baf45c`  
		Last Modified: Fri, 14 Nov 2025 21:08:23 GMT  
		Size: 44.1 KB (44125 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:e82578133c6e5fd5a9fc7cd10a6c546bf8425bf084dcad252c78326f4f4042c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 MB (107938741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cfac3b0e076da6c43d700a30c10439f2c76b9fbd170d9a5465aefd79c7163e`
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
# Fri, 14 Nov 2025 07:42:02 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 07:42:02 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 07:42:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 07:42:02 GMT
ENV PG_MAJOR=14
# Fri, 14 Nov 2025 07:42:02 GMT
ENV PG_VERSION=14.20
# Fri, 14 Nov 2025 07:42:02 GMT
ENV PG_SHA256=7527f10f1640761bc280ad97d105d286d0cf72e54d36d78cf68e5e5f752b646b
# Fri, 14 Nov 2025 07:42:02 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 14:02:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 14:02:53 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 14:02:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 14:02:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 14:02:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 14:02:53 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 15 Nov 2025 09:56:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 15 Nov 2025 09:56:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 15 Nov 2025 09:56:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Nov 2025 09:56:57 GMT
STOPSIGNAL SIGINT
# Sat, 15 Nov 2025 09:56:57 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 15 Nov 2025 09:56:57 GMT
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
	-	`sha256:b61568bffe09594f38a4358fa0027d359c02c9e9664c5e3da06f4814c0e9823a`  
		Last Modified: Fri, 14 Nov 2025 08:34:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f405327ef14efadeef909f0df17348553c8e2b5d4662f91456b23d19d7fe6218`  
		Last Modified: Fri, 14 Nov 2025 08:34:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37da6487b45826e489dc5a09342c02cd19543bc158c01606667b7d83d9c24265`  
		Last Modified: Fri, 14 Nov 2025 14:06:21 GMT  
		Size: 103.5 MB (103540060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bced8a9ca536caf9cb5471bf0fc74bee1c175610e1683280032596e0cfdbf16e`  
		Last Modified: Fri, 14 Nov 2025 14:06:11 GMT  
		Size: 9.2 KB (9209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27cf6ca0490263db60663f270cb6fc280df6cd4a0e987bed77695206851c328`  
		Last Modified: Fri, 14 Nov 2025 14:06:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ac6840dc62408a67c6fb2ca42efc5832eb513b4643af51037158f4de0f0ba8`  
		Last Modified: Fri, 14 Nov 2025 14:06:11 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d14b0f548d670ce2f508f195558eac933b59b385ebe9d251b0e10e0afddbf8`  
		Last Modified: Sat, 15 Nov 2025 09:58:15 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3223e6946157a6513eed0120e834523f576954d67ab9800d241f5a1692f8edcd`  
		Last Modified: Sat, 15 Nov 2025 09:58:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:aa92c0ac1cef5faf324d3bd94058ecf64ded1ddf3fa66f92e677801510ed6153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.1 KB (639147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b700bf3a94f772e427a1e5dfcc34cb5dced8073f4e0fa7e28ba3404c1931f9`

```dockerfile
```

-	Layers:
	-	`sha256:35e6766eba2b21b067aad00fc8980679ef4eb0c0a2f0909c27abb4a8b84c6d0c`  
		Last Modified: Sat, 15 Nov 2025 12:11:59 GMT  
		Size: 595.0 KB (595016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:551a765bae018153e9fe5de4fed6de3a179b72d1dbcb8c3632cf717fa8b5d221`  
		Last Modified: Sat, 15 Nov 2025 12:12:05 GMT  
		Size: 44.1 KB (44131 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:76cd94f16674f5ffd244344d93c028114c6da6d106d015b97cb92cfee354c759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116747734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8213bd5d8ed7494e2eb2821de938176b52fabae6b8d5acb29fb0077acdae36b1`
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
# Fri, 14 Nov 2025 01:24:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 01:24:12 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 01:24:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 01:24:12 GMT
ENV PG_MAJOR=14
# Fri, 14 Nov 2025 01:24:12 GMT
ENV PG_VERSION=14.20
# Fri, 14 Nov 2025 01:24:12 GMT
ENV PG_SHA256=7527f10f1640761bc280ad97d105d286d0cf72e54d36d78cf68e5e5f752b646b
# Fri, 14 Nov 2025 01:24:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 02:50:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 02:50:31 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 02:50:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 02:50:31 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 02:50:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 02:50:31 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:47:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:47:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:47:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:47:55 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:47:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:47:55 GMT
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
	-	`sha256:7d26e50aab688246007d981ec03ed0f2ba085e93831f3c2b4a5c41cedb4f6ab4`  
		Last Modified: Fri, 14 Nov 2025 01:27:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d3fda138bdb19608f3408a47a5ceb1f1e5a70ee029d664c864ace4ba7e8e7d`  
		Last Modified: Fri, 14 Nov 2025 01:27:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d05bed435d62cb3b724d1896f7cc0798cc1c284d8992e5c8beee64c50bfeaf8`  
		Last Modified: Fri, 14 Nov 2025 02:51:17 GMT  
		Size: 112.2 MB (112187283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cb90bf1d064df9a4fee74adfffa4287d37f12dd0e743304f9d6f64bb009c2b`  
		Last Modified: Fri, 14 Nov 2025 02:51:02 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa354d0c43e74b4052606f681073f8ea0224aa1d32e0e30b6e92db71e6501129`  
		Last Modified: Fri, 14 Nov 2025 02:51:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142017752fb620082b73ab0d01aed3960c2276f0164cbbbb0366fb48077527cc`  
		Last Modified: Fri, 14 Nov 2025 02:51:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81edde06ac272f5a1071620c3589faa9158bb756b662561e3d77a348e62fc24c`  
		Last Modified: Fri, 14 Nov 2025 19:48:11 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d971952dc106c50aadcd857730a3622fc60867bd4a28d1f6c820357d567d92c3`  
		Last Modified: Fri, 14 Nov 2025 19:48:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:289f12a8c46a1bb0532b6c2d7822856aafce438681ed7397ecc9f6a93628355a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.1 KB (639057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3da7ba0e55a4890f0b23b5852a5ae542d7968247758cf10a188de5ac83a3f9`

```dockerfile
```

-	Layers:
	-	`sha256:2e197dc75b19324109f7091c4c16296c7848d75a9988f8efca0dffa579c5b11f`  
		Last Modified: Fri, 14 Nov 2025 21:08:23 GMT  
		Size: 595.0 KB (594986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71aef064c6663b360a4acb4a8fa701caaf111d054922433bdeeb6e84b44df13c`  
		Last Modified: Fri, 14 Nov 2025 21:08:24 GMT  
		Size: 44.1 KB (44071 bytes)  
		MIME: application/vnd.in-toto+json
