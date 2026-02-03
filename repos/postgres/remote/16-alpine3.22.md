## `postgres:16-alpine3.22`

```console
$ docker pull postgres@sha256:4ddcf75a487ff3793dcb8bd5e085304c4b03b99cd7f5fc93f7961ba19e25af08
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

### `postgres:16-alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:ef1306c4c60c19ffe3d88e42028665c72dcc87cf7af068a93f01ca0d995c1d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109492769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61e956c480fe7b58e98033a69bc11576b8b67850f956404fda2bff72b1b1dc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:30:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:30:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:30:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:30:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:30:47 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:30:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:30:47 GMT
ENV PG_MAJOR=16
# Wed, 28 Jan 2026 02:30:47 GMT
ENV PG_VERSION=16.11
# Wed, 28 Jan 2026 02:30:47 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Wed, 28 Jan 2026 02:30:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:33:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:33:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:33:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:33:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:33:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:33:15 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:33:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:33:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:33:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:33:15 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:33:15 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:33:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd86c0dc10268cc02c9c5461e132a8f5e09da83375a21b462948bb50408f2bd0`  
		Last Modified: Wed, 28 Jan 2026 02:33:31 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf559938013dc69be371c3cfdafd1afe71bdb1783ab4081a94fcf4d3213305f`  
		Last Modified: Wed, 28 Jan 2026 02:33:32 GMT  
		Size: 918.3 KB (918291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e007e612c5da65b3b3dc851ab8a29768ba4f8182f79d418a9f22d8ba6bbdcdaa`  
		Last Modified: Wed, 28 Jan 2026 02:33:31 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d4f01f176f54b2cd2c67c7f8ad4189f3ef5f83744c1029602c2001bf67f9c0`  
		Last Modified: Wed, 28 Jan 2026 02:33:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7677dddaf293ee4087b186f95aa7bd755ff885f7aeb89008d3c2e5fa24da2d66`  
		Last Modified: Wed, 28 Jan 2026 02:33:36 GMT  
		Size: 104.8 MB (104752464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3ff2f980f17e8a8a0925d177fb646af1f19341cac79a15703cd07d55603af9`  
		Last Modified: Wed, 28 Jan 2026 02:33:33 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c47c6d875410af71ef9199bd26531d49c2009962aa2dd6f0563636e17e09f11`  
		Last Modified: Wed, 28 Jan 2026 02:33:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940d6769493f3a7f3a8d840a5f958892d21dc6e651ba7c3f4294fd9a7f75b898`  
		Last Modified: Wed, 28 Jan 2026 02:33:33 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f412b7f8d4597f964bdc02f7d67e6f3d1004333ef0e9a812669838a1960e6cc8`  
		Last Modified: Wed, 28 Jan 2026 02:33:34 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4832f99c5f6f3d07a552cce49ab37568f996c005f343bb1553ee99eb01fb31f`  
		Last Modified: Wed, 28 Jan 2026 02:33:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:b9a6519e37ca56e2500b96e228d358efc7c067a5294a2eb5375e5cbe61a84bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (639999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f8a4df6c4f7adeef11a3776a6c5c57b1fe41bcb7372496fd1fa3cb33e280ab`

```dockerfile
```

-	Layers:
	-	`sha256:9413888a4989d6f261f8cc147ab1f42268704c247fb69d2fe184615858319b39`  
		Last Modified: Wed, 28 Jan 2026 02:33:31 GMT  
		Size: 596.3 KB (596315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26142e6504c1c2d388e15f6cccf9a45c07ef6c9bbbea9099fc0a14cd875d1652`  
		Last Modified: Wed, 28 Jan 2026 02:33:31 GMT  
		Size: 43.7 KB (43684 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:813a7d8a8efac7f17bbc0fdd80e451a4cd24722da9d3e17b06df50bbe1cb68eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (89035779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4ab7d1f7177428eee1468977ec536d6fda093dd00766cb7ca02dbdd6d26405`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:49:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:49:24 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:49:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:49:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:49:24 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:49:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:49:24 GMT
ENV PG_MAJOR=16
# Wed, 28 Jan 2026 02:49:24 GMT
ENV PG_VERSION=16.11
# Wed, 28 Jan 2026 02:49:24 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Wed, 28 Jan 2026 02:49:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:52:19 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:52:19 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:52:20 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098dac0d46f933eaeb0c55f77f8040d4c9b5e4c7feeed0118c3a8fd5be1e9e35`  
		Last Modified: Wed, 28 Jan 2026 02:52:30 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce09e442c76e3f9b2f63362c934b32318bbe53fdc96cfff2a6ea1fdc1c17fd8`  
		Last Modified: Wed, 28 Jan 2026 02:52:30 GMT  
		Size: 886.1 KB (886129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d53aa3dc2252cbbe4968f25986cab018f6ab9d7b442667234bae87308ea2a7`  
		Last Modified: Wed, 28 Jan 2026 02:52:30 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a91a1f60be3de891ee18cd02ebcb34f871bd319eb511b8424c56ed9272f12f`  
		Last Modified: Wed, 28 Jan 2026 02:52:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5fcde3ada8929729a1bde12098a2840f94675299810d1353eda3fb6f51a0a0`  
		Last Modified: Wed, 28 Jan 2026 02:52:34 GMT  
		Size: 84.6 MB (84627466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c172e9952347dfb13bb98186b1c5ec671e083b7ffd574a88c0b8a200e3542cb6`  
		Last Modified: Wed, 28 Jan 2026 02:52:31 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74d38cad8fa59353f3b962044523a29012afa135e2c9ace10c2dd1e3a7d66ce`  
		Last Modified: Wed, 28 Jan 2026 02:52:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5661f9e3d4f544d6936808136249959b44ac2c55eb959b551be19b41f829838`  
		Last Modified: Wed, 28 Jan 2026 02:52:31 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ff9e228cd93a3c8c5ff34374f6d20efa3c64299b0ebaa29f8bb044b5fc8f8b`  
		Last Modified: Wed, 28 Jan 2026 02:52:32 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5074cf46b674e0abaaf75d52e7338d3c31b6525e0937514851cf18fc14b13d56`  
		Last Modified: Wed, 28 Jan 2026 02:52:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:2030b335eb5abcae23e0398691543f0c8ccf4a2e802c5010f74a1b19909a3ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 KB (43631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bcb9c6123a390cdfbc6a098cd1ffe85855d8e19b9e026d5bc18e2b54cd9ee4`

```dockerfile
```

-	Layers:
	-	`sha256:710df754f0e9b0cece169314d694b710b5f40077616c34d78cff73983e350ceb`  
		Last Modified: Wed, 28 Jan 2026 02:52:30 GMT  
		Size: 43.6 KB (43631 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:74211d48e0e80c62636c77de7d8dc206b12ecc0dbbec3afbebbb609e05b17c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84307519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16751ec60c9c9930c99c233a737f130d849570dcd56e9618fd2c1defc8edb08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:47:34 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:47:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:47:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:47:37 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:47:37 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:47:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:47:37 GMT
ENV PG_MAJOR=16
# Wed, 28 Jan 2026 02:47:37 GMT
ENV PG_VERSION=16.11
# Wed, 28 Jan 2026 02:47:37 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Wed, 28 Jan 2026 02:47:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:50:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:50:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:50:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:50:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:50:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:50:25 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:50:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:50:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:50:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:50:25 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:50:25 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:50:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11c7d54593fec235a1bdb568a564023789fd0bb94a1dc26539e45e786374a8`  
		Last Modified: Wed, 28 Jan 2026 02:50:37 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d50a83407a48f53d23b76bd31aaa272be51d2bdd39d9199203290e160f66a35`  
		Last Modified: Wed, 28 Jan 2026 02:50:37 GMT  
		Size: 886.1 KB (886132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1763bee7cdab6709c2736ab9d3d7ca6c07497e5b03e70c26fc6fd772e9d747`  
		Last Modified: Wed, 28 Jan 2026 02:50:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce26d66ba2add6a0d83394af5be551f51cd953636ca3db1fb7692cd69145cfa`  
		Last Modified: Wed, 28 Jan 2026 02:50:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f587f0ebf51310f0899749a091e355d1ed53dc1ec36b78f0f8ff7698a32f457e`  
		Last Modified: Wed, 28 Jan 2026 02:50:40 GMT  
		Size: 80.2 MB (80180619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9bf5005929576b846948263db58f7d4f661f638032b0e2d592b51ab25e76ca`  
		Last Modified: Wed, 28 Jan 2026 02:50:38 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8dacd1e6ff7e008330bfb844ab331377fa9e998ed0187ba22998c2d32b6feb`  
		Last Modified: Wed, 28 Jan 2026 02:50:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60af2be8ccdf25736b06ce74ac2a0bce294b0c99e30ad138b3c8526c459f3311`  
		Last Modified: Wed, 28 Jan 2026 02:50:38 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587442808d0ecc3e06dd2f3a73a3b2566b0077665d55b5c1ba184a3ef4bfdace`  
		Last Modified: Wed, 28 Jan 2026 02:50:39 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd83cfafc7e1a5771722bfebc27a32b7e72c00feab55a66312b68384013da3d7`  
		Last Modified: Wed, 28 Jan 2026 02:50:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:794d01dc8b80ce375375bfd0f27151cd13dd65a6d784dac50717257acf3f1cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f168ac4f7b209afd24af78bf3c9d653a88ee87d701900434c14de606c572139`

```dockerfile
```

-	Layers:
	-	`sha256:a83b3bb7317306d5fadbed15efa5260451e9908696c1d0d8535f4820fc90c285`  
		Last Modified: Wed, 28 Jan 2026 02:50:37 GMT  
		Size: 596.3 KB (596335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59cd6cd845cc4af8a46fccbcad65533714621d69bbd71e376e22308f8f7c16e7`  
		Last Modified: Wed, 28 Jan 2026 02:50:37 GMT  
		Size: 43.8 KB (43846 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:9140cc382901a554fea7ef1b263df355035dde3ec49fe64583271478a01a1c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105451880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0672e71f4963ea9d62bfc50da67939482664393cf14463d47e3ef367abfbeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:29 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:32:32 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:32:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:32:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:32:32 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:32:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:32:32 GMT
ENV PG_MAJOR=16
# Wed, 28 Jan 2026 02:32:32 GMT
ENV PG_VERSION=16.11
# Wed, 28 Jan 2026 02:32:32 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Wed, 28 Jan 2026 02:32:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:35:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:35:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:35:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:35:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:35:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:35:18 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:35:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:35:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:18 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:35:18 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:35:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0ef7cc186b508aad0da7dc4540d4dc87e7d4f68f404c80c8548a4db224a32e`  
		Last Modified: Wed, 28 Jan 2026 02:35:32 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb77fe54524d1887b9c828d7532c44f4e642afc7fa83da87c3fc36b4ba2dd46`  
		Last Modified: Wed, 28 Jan 2026 02:35:32 GMT  
		Size: 873.5 KB (873487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabd5adff40d5a076ce54254324ae842578b46762eb87e2229f204216e0f0030`  
		Last Modified: Wed, 28 Jan 2026 02:35:32 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c289b1a5684d7419037c1f2316cdada64f39f36e5abe0f307950cb1fe873cbf`  
		Last Modified: Wed, 28 Jan 2026 02:35:05 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d7303476c3d6aa974769d268fed105c4d7973b33d2cad9033a5845e5c4e0d9`  
		Last Modified: Wed, 28 Jan 2026 02:35:36 GMT  
		Size: 100.4 MB (100421738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ec7697d5175fb8e06f39e2f2d0e573ad4b5b60c8ff4c13d5afacbe2f6872d4`  
		Last Modified: Wed, 28 Jan 2026 02:35:33 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1154988e2077fc8c8afe621aeb09ad7f9c2917eb996535faf407ac961ac72b81`  
		Last Modified: Wed, 28 Jan 2026 02:35:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b46c405cd2df54f53267f642e4c32d0ed7d78bbbc6353944810634726544fb`  
		Last Modified: Wed, 28 Jan 2026 02:35:34 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49acd221538c8a2d0f18870e42f7c198cb8c655fbcf1d5ae12490a5281ec825`  
		Last Modified: Wed, 28 Jan 2026 02:35:34 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23b7d66f67904d216ecae7feb8219494c404aa96c59f30c888793c85fd2376`  
		Last Modified: Wed, 28 Jan 2026 02:35:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:5eb7567945572691ec4d2f10f5ac0a73e017ba26599b1dfe9a1e0d3e00718a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6085dd50a8062ce19908b2a4b4372c9dbd14682f77c48188bacf50bb8ed3c2ec`

```dockerfile
```

-	Layers:
	-	`sha256:d6a5431fe29e36d9e8b0ff66b4eb2d09d659585e97b29210a98bc138ed9bce28`  
		Last Modified: Wed, 28 Jan 2026 02:35:32 GMT  
		Size: 596.3 KB (596347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:372b9886b8972e58b54652bab95fed6300f882b06332abc6c32b69b2b0710beb`  
		Last Modified: Wed, 28 Jan 2026 02:35:32 GMT  
		Size: 43.9 KB (43882 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:a3d5e3856de372648b7c46384460103bf178a30ce0d1b5c60052a6ad6b9fb987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115728010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77c05b9cea89d2d9a18b984aaa6b63d541edeb2cffc1fd4cffea4634cc9d182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:27:54 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:27:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:27:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:27:57 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:27:57 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:27:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:27:57 GMT
ENV PG_MAJOR=16
# Wed, 28 Jan 2026 02:27:57 GMT
ENV PG_VERSION=16.11
# Wed, 28 Jan 2026 02:27:57 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Wed, 28 Jan 2026 02:27:57 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:30:35 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:30:35 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:30:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:30:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:30:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:30:35 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:30:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:30:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:30:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:30:35 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:30:35 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:30:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277c009459198dbdb5ab2cdb4a943df6164d9eadfc1bc24f0d825eac8b6868ae`  
		Last Modified: Wed, 28 Jan 2026 02:30:18 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e2147a93acfdc3c66e254188497c336a88f57acffef3258b0bbad1889cf6d5`  
		Last Modified: Wed, 28 Jan 2026 02:30:52 GMT  
		Size: 890.6 KB (890626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5baa5f3f88ef4ee60f5735fea66e46e88d8f25a20d6b7eed61641756b332a3d`  
		Last Modified: Wed, 28 Jan 2026 02:30:52 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58de2ded5529ce062b3a0f29b6c058600b95c80629a35dc4d4b0f0e1a9b0e2b`  
		Last Modified: Wed, 28 Jan 2026 02:30:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13dc22f005a7f1c16a3c612a9d3eba3a6717083b9b653d1b62206b605098facc`  
		Last Modified: Wed, 28 Jan 2026 02:30:54 GMT  
		Size: 111.2 MB (111199511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983c5cab2873e8895d967dfe51706a05049c3ee585cef93ef98a8a1f4a2f6c7a`  
		Last Modified: Wed, 28 Jan 2026 02:30:52 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9630afbae46b85dc8ea95e3f0ff280d1b843ce8f1b697caf4a8f80e417f3fd14`  
		Last Modified: Wed, 28 Jan 2026 02:30:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6537c02a921e046098d8069618d0965fefeffc601ab71b74c50b92100906ff`  
		Last Modified: Wed, 28 Jan 2026 02:30:53 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0276bddb43feab3282a3faf53bcd08beb10903a024dc99d2788ae2e6abd20469`  
		Last Modified: Wed, 28 Jan 2026 02:30:53 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035e0c642e5dcd2ef6cd9f99249799223deda7f2ab715921fab653139d046ac3`  
		Last Modified: Wed, 28 Jan 2026 02:30:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:5be1e86320796651063bd3e292489f81678b5f4aaa588d7f4a12b2389e79b681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.9 KB (639944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbf191563badd99ae23e0b1e6489cd0696f7786b9cfbc28cea7e4a662b27f96`

```dockerfile
```

-	Layers:
	-	`sha256:3321c91cedd3704871fc2b2ef92522c1b4f2798335c0d2887172d7b38b9aae25`  
		Last Modified: Wed, 28 Jan 2026 02:30:52 GMT  
		Size: 596.3 KB (596300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb0745544ab09b9d7d14f952b96809022af79cdc4a58eda28565cd6c9fe79115`  
		Last Modified: Wed, 28 Jan 2026 02:30:52 GMT  
		Size: 43.6 KB (43644 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:959dd1dd8580624feac63895629461a5ad1818dbbdbb76382a33fb997a79c026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93259245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d653873478daf1c437f31929d4ade9d6aec0c9f34600ecaede26e210f9878e9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:33:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 03:33:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 03:33:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 03:41:23 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 03:41:23 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 03:41:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 03:41:23 GMT
ENV PG_MAJOR=16
# Wed, 28 Jan 2026 03:41:23 GMT
ENV PG_VERSION=16.11
# Wed, 28 Jan 2026 03:41:23 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Wed, 28 Jan 2026 03:41:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 03:44:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 03:44:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 03:44:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 03:44:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 03:44:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 03:44:16 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 03:44:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 03:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:44:17 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 03:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 03:44:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cf718fa459d8840034db063bb9424e81c3d9174a32a4c9dfc267b33036ad07`  
		Last Modified: Wed, 28 Jan 2026 03:36:40 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9227b35430cc92748ff2ebf224e67d8d43cd96411ecdffb11f93f8780a00bd1e`  
		Last Modified: Wed, 28 Jan 2026 03:36:40 GMT  
		Size: 879.0 KB (879034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb8caad2d394d40c900318205bb2a4fab84cb8a4174174889d0d3ba8cd34ec9`  
		Last Modified: Wed, 28 Jan 2026 03:44:43 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea567f655947b15a81f4906d157299d55233dbc5ed74ff062f795cda2c2b610c`  
		Last Modified: Wed, 28 Jan 2026 03:44:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65653971b70e622072f00642664cb9437ea26adecd7260c878b420043ea927d`  
		Last Modified: Wed, 28 Jan 2026 03:44:46 GMT  
		Size: 88.6 MB (88628764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e35faf0bcd4565a916a3a78a144f310a725dbc31ae07256abd4055bbec87080`  
		Last Modified: Wed, 28 Jan 2026 03:44:43 GMT  
		Size: 9.6 KB (9565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e76f474e9270bc7bfe419113a9a90011e790a41fdea6b46d69b17583bc39bfb`  
		Last Modified: Wed, 28 Jan 2026 03:44:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfa68d75d93204c39e1df54903ac9154724f11183adcb1a6813ecea0f803f89`  
		Last Modified: Wed, 28 Jan 2026 03:44:45 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ceae4110e20dd3f94afe1c778f691fd120a5e66f3ad78fc2eeb11991e71cbb9`  
		Last Modified: Wed, 28 Jan 2026 03:44:45 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2961c7cf41b2b808e56ae6115039894d8f2efae6111d83cceb96ac577feb29e`  
		Last Modified: Wed, 28 Jan 2026 03:44:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:27813fa62c561ed6d8e4f6848188a7cadaa6e8d184fe8163e986f85f642e1f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.5 KB (636450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06fb2ad84d8d4e5e9ce2805d6f2cb3b6fedacaedad271bf444168b0e57b0fee`

```dockerfile
```

-	Layers:
	-	`sha256:6b4a386cf76b15c5a56f195428e23909de67876ee9476e59d96d1a776bd114f2`  
		Last Modified: Wed, 28 Jan 2026 03:44:43 GMT  
		Size: 592.7 KB (592724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:433ca1d3be63c17a353b4705a80963f8a4b2ccb8db288d3891739c42251ce844`  
		Last Modified: Wed, 28 Jan 2026 03:44:43 GMT  
		Size: 43.7 KB (43726 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:bbabfa49e052fec2b5cec1fc01ca120d0ffe2280b5970610856765da34b81af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109496842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3cbeaed31708b14a871fa84a78b40c0fd87b7e6e4885b675efa624218f15ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 10:55:26 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 29 Jan 2026 10:55:38 GMT
ENV GOSU_VERSION=1.19
# Thu, 29 Jan 2026 10:55:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Jan 2026 12:45:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 29 Jan 2026 12:45:14 GMT
ENV LANG=en_US.utf8
# Thu, 29 Jan 2026 12:45:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 12:45:14 GMT
ENV PG_MAJOR=16
# Thu, 29 Jan 2026 12:45:14 GMT
ENV PG_VERSION=16.11
# Thu, 29 Jan 2026 12:45:14 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Thu, 29 Jan 2026 12:45:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 29 Jan 2026 13:33:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 29 Jan 2026 13:33:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 29 Jan 2026 13:33:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 29 Jan 2026 13:33:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 29 Jan 2026 13:33:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 29 Jan 2026 13:33:33 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 29 Jan 2026 13:33:33 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 13:33:33 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 29 Jan 2026 13:33:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 13:33:33 GMT
STOPSIGNAL SIGINT
# Thu, 29 Jan 2026 13:33:33 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 29 Jan 2026 13:33:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b9345ee4b489b81ddaa2ed9a1bcf197279deaaacaaa87586c3e9061cd25f55`  
		Last Modified: Thu, 29 Jan 2026 11:50:24 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbcd57fbfcad548bebc5b9be00ad91e0a69472aa73e26898e5411e0b6e1c8c9`  
		Last Modified: Thu, 29 Jan 2026 11:50:24 GMT  
		Size: 866.6 KB (866623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3665fff96da728265b4c38dfb6e41c2ace7af98c8b288cbcbe6185885c05030`  
		Last Modified: Thu, 29 Jan 2026 13:36:23 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa9e212cbcc2c3495f3d236d2c604d65eaae9a5e622f94533d70cd354e670a0`  
		Last Modified: Thu, 29 Jan 2026 13:36:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b9c13f8b5f3246b94907c710c9e7e143d70f46b81a907d74b4fa73f746c10e`  
		Last Modified: Thu, 29 Jan 2026 13:36:39 GMT  
		Size: 105.1 MB (105095633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4303ee36253a1ffb325b4c1669fd6ca623451b3610e8583f4ca7c987269dbcfc`  
		Last Modified: Thu, 29 Jan 2026 13:36:23 GMT  
		Size: 9.6 KB (9569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51b3c240dd1ba93439897ed8a9c7bec8f0ad2728bf3cd612d09c8e0f1d3d270`  
		Last Modified: Thu, 29 Jan 2026 13:36:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85fcb7105269f7cfeb9786b554241b9577935f2c0c00bc496979725e20b08f7`  
		Last Modified: Thu, 29 Jan 2026 13:36:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aabaee2cce8dac9ab53760f1c14e1a58f41a80e82d919458251fe1bd6474465`  
		Last Modified: Thu, 29 Jan 2026 13:36:25 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874f871acbbdd0b316da189c785318692fb69b6775a9f1eb2e3bc7e9d3e1a9df`  
		Last Modified: Thu, 29 Jan 2026 13:36:26 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:e0531ca1d7af141740c93f45c451aeb1ded3eb08f4b3bb71723c90e918418581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.1 KB (638113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ed7082dc18ff0ebd9a0f1aaf10c0b1b6468c131bdd5f48f8bc2fc500212582`

```dockerfile
```

-	Layers:
	-	`sha256:92ffdb8f0be22d3e560b6f4c6ad02807517e888d23159f554a79a3bb1df5df5a`  
		Last Modified: Thu, 29 Jan 2026 13:36:23 GMT  
		Size: 594.4 KB (594382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21a8f2615eafbeb585cf4efb6d94b5557663b6d09d115c774e8f6d6b15d20602`  
		Last Modified: Thu, 29 Jan 2026 13:36:23 GMT  
		Size: 43.7 KB (43731 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:699dc21cfb4032a2d5e57e4d395d07a4b6a44ecff0cde69431e69366616a47f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118184120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4cf22b0da3d5b3f3d54b9795f17e8725e847d2057ec025f74a2f8834d18678`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:50:45 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:50:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:50:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:55:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:55:12 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:55:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:55:12 GMT
ENV PG_MAJOR=16
# Wed, 28 Jan 2026 02:55:12 GMT
ENV PG_VERSION=16.11
# Wed, 28 Jan 2026 02:55:12 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Wed, 28 Jan 2026 02:55:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:58:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:58:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:58:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:58:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:58:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:58:17 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:58:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:58:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:58:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:58:17 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:58:17 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:58:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a3490d5e1eb042b54ebd115cb64d71b766324089640d2f8cbd7dc46f8d1d8a`  
		Last Modified: Wed, 28 Jan 2026 02:54:19 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd22cb56ffc984c4bd184677f0dd02c808e5b19bc2191097d07cefddb0d7c2ce`  
		Last Modified: Wed, 28 Jan 2026 02:54:19 GMT  
		Size: 894.4 KB (894410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a0bb249039a5dd92165b8bcbbae32602cdfe469241d19a88e3cf82a4c990f6`  
		Last Modified: Wed, 28 Jan 2026 02:58:42 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed641ff743f72086db444a70b7f5a7fd829784be59ac6f97c7ee9b3f89131c6b`  
		Last Modified: Wed, 28 Jan 2026 02:58:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf76ac07001db4d4dcb8e2b01dfb290c2dfc12aabe78e3cad286c58a78fdd10a`  
		Last Modified: Wed, 28 Jan 2026 02:58:44 GMT  
		Size: 113.6 MB (113622133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1c3dc59ba5095491e849a9171e07e9abf0a466c0f458f9f893b7458639eb8f`  
		Last Modified: Wed, 28 Jan 2026 02:58:42 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77d9c20093d9caadf2db5132d473d4eba4c7fbd71aea10c877ba5b37f2e997d`  
		Last Modified: Wed, 28 Jan 2026 02:58:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f694a4ae938fbd17f649f9e24ce6df3d7de302356a7c94ace915de1780975ec`  
		Last Modified: Wed, 28 Jan 2026 02:58:43 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845d97bf8d62877897f8f8475aea4a8ab4ff1fd2c84a128bc314e1dab827ec15`  
		Last Modified: Wed, 28 Jan 2026 02:58:43 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce7efee5a774920edbd0090e733c49c99c097000e408d49f2cfc78fc2b65f77`  
		Last Modified: Wed, 28 Jan 2026 02:58:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:b88e99bba6a2ea677be779155ad1f654816fddc340fd9cd4ec76a408d940bf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.0 KB (638048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38148e2f77c520b9dd6c51da516e35f738530ba3cf66e10774ac739f7e5ee4cd`

```dockerfile
```

-	Layers:
	-	`sha256:eb4ea44659a5a48588b72d7a84e07187d0b26ae430a7ce62613b545328170421`  
		Last Modified: Wed, 28 Jan 2026 02:58:42 GMT  
		Size: 594.4 KB (594364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d5d89531139db194d5008ef81462bb7477533702d819a8eca5f872ad3103399`  
		Last Modified: Wed, 28 Jan 2026 02:58:42 GMT  
		Size: 43.7 KB (43684 bytes)  
		MIME: application/vnd.in-toto+json
