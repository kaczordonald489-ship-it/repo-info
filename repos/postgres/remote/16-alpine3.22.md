## `postgres:16-alpine3.22`

```console
$ docker pull postgres@sha256:79c06d285ed9186efbbc45c73413b3c3510c3c94ffede2f25d1e523f74d07f28
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
$ docker pull postgres@sha256:46258a3eb38adf37e77ca5bd41f93ca8b1034f925cf37190a7a8015ba151f3ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109490219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216e5ca6a8144363cf36affd3d72265c9d4978d515e7f5ba5549a4301e65c705`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:19:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:42 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:19:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:19:42 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:19:42 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:19:42 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:19:42 GMT
ENV PG_MAJOR=16
# Fri, 14 Nov 2025 19:19:42 GMT
ENV PG_VERSION=16.11
# Fri, 14 Nov 2025 19:19:42 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Fri, 14 Nov 2025 19:19:42 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:21:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:21:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:21:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:21:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:21:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:21:58 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:21:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:21:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:21:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:21:58 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:21:58 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:21:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d06b7fef7a2330a9473819c3479ec17e8fbc4bf60df46d5449fdb5ccd01f54`  
		Last Modified: Fri, 14 Nov 2025 19:22:24 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc8985c623892d1c787b89738976c06573fbaf42082623a7bf0ba9e89cdeeda`  
		Last Modified: Fri, 14 Nov 2025 19:22:24 GMT  
		Size: 918.3 KB (918290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538c669d4f9448dcf1a269710b1a448ba5d541f5a3f7edf9d09d8f82b60fa2db`  
		Last Modified: Fri, 14 Nov 2025 19:22:24 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2db3dd76baa5444eea7f254a76045218460434c9d185bb55b184d26677762b0`  
		Last Modified: Fri, 14 Nov 2025 19:22:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5443128c21257dac235b8544526fdd74108fd4d5033aaf5ef8181b3b982af727`  
		Last Modified: Fri, 14 Nov 2025 19:22:35 GMT  
		Size: 104.8 MB (104752339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6e868aea79267822d3482474af89017d4fad708f6816aab16c459d0eff25ff`  
		Last Modified: Fri, 14 Nov 2025 19:22:24 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5dc03d34e56ee699d6b73324950599669b61e4470c7dc995ddb4596ab65413`  
		Last Modified: Fri, 14 Nov 2025 19:22:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670559ed8ba9927c8b4a0284b1770206edddfbbf65a93809be719cde4fdc45d4`  
		Last Modified: Fri, 14 Nov 2025 19:22:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23babb82b92a4015ec2c3bd45649e92853cde34224f5bbf6eacdbc7b6e4c70b`  
		Last Modified: Fri, 14 Nov 2025 19:22:24 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab99cec2af71742d800a5200f85170f2c12f989009d9c207f0b1aa31a43d44a`  
		Last Modified: Fri, 14 Nov 2025 19:22:24 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:f28494cf3214da149adb2664397b951585589ab1d470c6b23a6136e6cefbccb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.2 KB (641243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383fdd9d79fd33d9deb52533fb0ebb463dc55c0126a68a9d66a0536a7ff60ebe`

```dockerfile
```

-	Layers:
	-	`sha256:a88806d8f733fd81bfbd5f9c7a4c47653205c3276934ff3f4b10e2aa45576fab`  
		Last Modified: Fri, 14 Nov 2025 21:13:03 GMT  
		Size: 596.9 KB (596937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deb9c241ab9bbfb10bf4b5582265d2ec3a2680bcb7ecc5648aa5a515d9be3407`  
		Last Modified: Fri, 14 Nov 2025 21:13:04 GMT  
		Size: 44.3 KB (44306 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:d86640e0f7fcb80762d8218be133d717972796240bcd41f36d5a99876d31e111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (89034841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef153546179e7472b5de968568ce61c14669ebe394a683da6fa4f5779c6e9f29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:40:22 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:40:25 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:40:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:40:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:40:26 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:40:26 GMT
ENV PG_MAJOR=16
# Fri, 14 Nov 2025 19:40:26 GMT
ENV PG_VERSION=16.11
# Fri, 14 Nov 2025 19:40:26 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Fri, 14 Nov 2025 19:40:26 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:43:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:43:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:43:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:43:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:43:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:43:14 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:43:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:43:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:43:14 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:43:14 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:43:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5037c0bbdbcc5878d7c934a45a9f46b8a1032f69c780f63f26e8ff56ec8103b`  
		Last Modified: Fri, 14 Nov 2025 19:43:33 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25758288a4ae90ea567c95e85347e0ad89dfdf3f9ad80122f804847c6655ea3a`  
		Last Modified: Fri, 14 Nov 2025 19:43:33 GMT  
		Size: 886.1 KB (886134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002a0b60e045fc45ff75aeb01c83aa106515a54907bd0be97895f952bd43ea91`  
		Last Modified: Fri, 14 Nov 2025 19:43:33 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92b21faf2ce157c5b455aaf148add1c37dbadb05fab9dda73a50097143edb4b`  
		Last Modified: Fri, 14 Nov 2025 19:43:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67beca2d05f8894136b9da1c27d7d1e3e1b41fc3fa1633006cdb6cf75a032e99`  
		Last Modified: Fri, 14 Nov 2025 19:43:40 GMT  
		Size: 84.6 MB (84627481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22594a682984617bb166a0115ec4917f1edc3ffd3c72a1ec26ab936f769a7965`  
		Last Modified: Fri, 14 Nov 2025 19:43:34 GMT  
		Size: 9.6 KB (9562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8985b4220db637ffd148d3d0d83784c41e2f4a9939f7b5bef5bad1fcf98545f1`  
		Last Modified: Fri, 14 Nov 2025 19:43:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97f984f4ede5076a864abcf21ba5bb4e2da43c908392f3b1ce1f7aae269e4c0`  
		Last Modified: Fri, 14 Nov 2025 19:43:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad596fab345e37634df46db9c953d83e36beae9ae588ffbdb46228220e8cc56`  
		Last Modified: Fri, 14 Nov 2025 19:43:33 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3429b7f21f4841c8b9dd68bc17299c780697f1b445739cc73abbb0c4acbf31`  
		Last Modified: Fri, 14 Nov 2025 19:43:33 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:384c876cb073f0ec55bedb089868f335f8d9b7fe80ca2422503aabbdce2961b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 KB (44269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86de7fc3ff67594479a172b5ef5c18bcde851cabb1287ac6b1be9d9d5dea90fd`

```dockerfile
```

-	Layers:
	-	`sha256:87899cbec216a6c3cf1168c6611e0851196690832a20782dad06d9d227f85d1f`  
		Last Modified: Fri, 14 Nov 2025 21:13:08 GMT  
		Size: 44.3 KB (44269 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b516754cdcf3929a0bf14d280b7cef1230352007e12cf341f14216448a8ca646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84305266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:315a1114deca29df401284a04e1f7f35a7fbdea540f48bc95d1299d267bb9bff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:36:43 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:36:46 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:36:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:43:35 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:43:35 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:43:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:43:35 GMT
ENV PG_MAJOR=16
# Fri, 14 Nov 2025 19:43:35 GMT
ENV PG_VERSION=16.11
# Fri, 14 Nov 2025 19:43:35 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Fri, 14 Nov 2025 19:43:35 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:46:18 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:46:19 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:46:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:46:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:46:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:46:19 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:46:19 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:46:19 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:46:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:46:19 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:46:19 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:46:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f1476dd2fe5c07cd05179495ef7d4eaf5c9722d4e2ad4f64627b9c6346a825`  
		Last Modified: Fri, 14 Nov 2025 19:40:04 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfde4222cab51534f20c289b67d54273ca47320b31cd708b2ac4e6ca87f6ef95`  
		Last Modified: Fri, 14 Nov 2025 19:40:05 GMT  
		Size: 886.1 KB (886135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf7679b3a7800752191d7f0cbb6e58b0b95364fbe102de26792a84c110212c3`  
		Last Modified: Fri, 14 Nov 2025 19:46:54 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47ec68a54e86029f388e987a016a4a2a6f8e0a6dc574f8646f97d834b551151`  
		Last Modified: Fri, 14 Nov 2025 19:46:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e47d38b0ca77161ace32bdaddaa020128cbb2cc6b192ecd5a9ec96322afcd2`  
		Last Modified: Fri, 14 Nov 2025 19:47:00 GMT  
		Size: 80.2 MB (80180425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1988b0d3bce6514989b707c5da328b0a0faeffe4af3c9ec4df5f13fa127b21fa`  
		Last Modified: Fri, 14 Nov 2025 19:46:54 GMT  
		Size: 9.6 KB (9562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1239ae33ddefbe1554007f00ec0b6c5eda5584957e33556d6103a9ff81a056`  
		Last Modified: Fri, 14 Nov 2025 19:46:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe0376ab1e7d81ee2aaebbefcf8051f608c8a22a7afd28f102c08edd9e547e1`  
		Last Modified: Fri, 14 Nov 2025 19:46:54 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9825cc76eed4c0b1b5a49a684dacdfed43807cbcceeba865a83eb14235734c29`  
		Last Modified: Fri, 14 Nov 2025 19:46:54 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f433d704b83066732a872a65dd4e5a45cd5312df941d162ea6d56b04f481005`  
		Last Modified: Fri, 14 Nov 2025 19:46:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:e035053d1f14bf00e3a36e3f6618d96ae073478651329aab05b669e3ab3dbf80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.5 KB (641457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025f06b5cad1de9b0e672a07b669a9a5609d25652170e7548199a13c05e01956`

```dockerfile
```

-	Layers:
	-	`sha256:c940e7e01d5922cfa03acfb5683e5a58b58d59923d1fa424046e40542b69e6d3`  
		Last Modified: Fri, 14 Nov 2025 21:13:11 GMT  
		Size: 597.0 KB (596973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b107d12d0eceea2e0292c6cf07725de303b58a049ce5e80a77dafcf7def47e7`  
		Last Modified: Fri, 14 Nov 2025 21:13:12 GMT  
		Size: 44.5 KB (44484 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:84762d7dde4708ffa720f83d6f6701ba306319ac7a31f426da3467d04827f77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105449826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4530bc172734867bcc3b52aa619dc574d832998f5d16cecc7b0bdc4587921c39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:18:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:18:31 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:18:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:18:31 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:18:31 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:18:31 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:18:31 GMT
ENV PG_MAJOR=16
# Fri, 14 Nov 2025 19:18:31 GMT
ENV PG_VERSION=16.11
# Fri, 14 Nov 2025 19:18:31 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Fri, 14 Nov 2025 19:18:31 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:21:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:21:03 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:21:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:21:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:21:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:21:03 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:21:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:21:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:21:03 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:21:03 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:21:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7889b12055bab17c7b00d87b28172e2f880a3f1a37402a85096b0ecdd4b679b`  
		Last Modified: Fri, 14 Nov 2025 19:21:27 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c437b93687aa70f311146e196ebc27ea4b01465479389d8934b458b7eef800`  
		Last Modified: Fri, 14 Nov 2025 19:21:27 GMT  
		Size: 873.5 KB (873485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2a1d9905cc762cc1af6ecf89e992219da0a6048c529cf405ac00f55563148`  
		Last Modified: Fri, 14 Nov 2025 19:21:27 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34009c473f652efffc82546a4fef1e6c266fc56f4aef26fdcbd12e35f81560f5`  
		Last Modified: Fri, 14 Nov 2025 19:21:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2364873e7212c3b88cfd20ad8f229d37937cbb679d343758c6b0bd1dfc96c1b2`  
		Last Modified: Fri, 14 Nov 2025 19:21:34 GMT  
		Size: 100.4 MB (100421133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1ae260595e4cf5613d9b43357cd225b37a519a0663afe41dc7162ee6d82edc`  
		Last Modified: Fri, 14 Nov 2025 19:21:27 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb6e8a2fddc7c514cbdd4432d61321ae435b3b16da29fc61b773ff4fadcfd2c`  
		Last Modified: Fri, 14 Nov 2025 19:21:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97b66f84d85685dc439ebe8118e6989ef14222115165793abb82117916d532`  
		Last Modified: Fri, 14 Nov 2025 19:21:27 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbede6f91e4c2ed03b0a71c5f7b0614635081f1daf023376362fa0a67faed9f`  
		Last Modified: Fri, 14 Nov 2025 19:21:27 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e550ea86183ed9f8aa5402f8b28b8a75809213572a47a2dd46105aec53e8d121`  
		Last Modified: Fri, 14 Nov 2025 19:21:27 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:8a23f0f2da930302eda082556c1968788f71e4580a677992608dc070412a3e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.5 KB (641523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a496cc730aa0a61b01325c8ccff0413d55b88840fe8e1fa343e4a2f56dc989f0`

```dockerfile
```

-	Layers:
	-	`sha256:db0eb341c873b0caf6e6ea7f30c57e056b4e4abfba3c7d8bd4aa41b68ce631a9`  
		Last Modified: Fri, 14 Nov 2025 21:13:15 GMT  
		Size: 597.0 KB (596993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c346d1f98b306b04d230a74c2af78ca9abe343bfb899b7f81594fe4f3cb9f14c`  
		Last Modified: Fri, 14 Nov 2025 21:13:16 GMT  
		Size: 44.5 KB (44530 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:508ad380e53576e351390fd5a15f09f0e7f638791c363666cc255c5bc9c7bbc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115724802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26dfd49d2d404a80e56ae4c339df17c68a9cd3b79b29ac7a20f6817cc156cd0`
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
# Fri, 14 Nov 2025 19:22:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:22:20 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:22:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:22:20 GMT
ENV PG_MAJOR=16
# Fri, 14 Nov 2025 19:22:20 GMT
ENV PG_VERSION=16.11
# Fri, 14 Nov 2025 19:22:20 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Fri, 14 Nov 2025 19:22:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:24:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:24:31 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:24:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:24:31 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:24:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:24:31 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:24:31 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:24:31 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:24:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:24:31 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:24:31 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:24:31 GMT
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
	-	`sha256:d94bdb6a4241f754e774d0b5153524a80dc97d3420c04c2cc40b6fb30d8f11ac`  
		Last Modified: Fri, 14 Nov 2025 19:24:53 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6254220a86db56d521c63741dda00fb03434f00ce8157d2608fd011e18a08cdb`  
		Last Modified: Fri, 14 Nov 2025 19:24:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23dd09bf94824a5d58a73e10b8cb08e5cc7fa005eabbf35e839d866b1368834`  
		Last Modified: Fri, 14 Nov 2025 19:25:09 GMT  
		Size: 111.2 MB (111198088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09e92c95ed63ee7a68d8a3a47e3a293eb4875ab7e7e2067528840f996e1eb1a`  
		Last Modified: Fri, 14 Nov 2025 19:24:53 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1a72c7160ee688dc9f2a6aa4a4d24640fb9728e9d7cee873c52a3c60341679`  
		Last Modified: Fri, 14 Nov 2025 19:24:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923eec71b1fbd7e51aaa018ca2a43bc275cd9fa09cc27a4338f17156eef38d28`  
		Last Modified: Fri, 14 Nov 2025 19:24:53 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cd9616447cb6aa95c04fbf4d4e8ec2f354eb9f362f8e1150e45db367a9de18`  
		Last Modified: Fri, 14 Nov 2025 19:24:54 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4011938ee8eff3b6be55627210fa871f908dafff4682f3f8255e3a419772cb64`  
		Last Modified: Fri, 14 Nov 2025 19:24:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:ca00c9e4ac87afc5f1a16cd4eee49447a571c73a9078145c81d101c28b2f7700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.2 KB (641169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bbacc9f00bf974fdbd2e78d7a662c8b75adffdb919fffc191e1256886f99e2`

```dockerfile
```

-	Layers:
	-	`sha256:fae255fa6f9a095c32d9dc814c4f390f832466cac8df0f078b9a1e83293b0b9f`  
		Last Modified: Fri, 14 Nov 2025 21:13:19 GMT  
		Size: 596.9 KB (596912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e93b9fc922a7f2f133d553cf7e741b1990b681483a1d0ca1dc41e45300630955`  
		Last Modified: Fri, 14 Nov 2025 21:13:20 GMT  
		Size: 44.3 KB (44257 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:ebd94c3d3b6d646004d1668bff4da0d9942ea6857fe20a69f9e723db0aa80249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93257512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b725d7390c03678d4de0fed60a179195f0c16aca6be8362bf9a5cf6b4be8f470`
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
ENV PG_MAJOR=16
# Thu, 13 Nov 2025 21:29:53 GMT
ENV PG_VERSION=16.11
# Thu, 13 Nov 2025 21:29:53 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Thu, 13 Nov 2025 21:29:53 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Nov 2025 21:32:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:32:27 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:32:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:32:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:32:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:32:27 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:34:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:34:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:34:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:34:28 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:34:28 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:34:28 GMT
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
	-	`sha256:3734d54796e2b1027a87973d9f15acde0066e6f06f317a57dde84024c132ca43`  
		Last Modified: Thu, 13 Nov 2025 21:33:40 GMT  
		Size: 88.6 MB (88629083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bb07378cbe31c99b4f2077deee7c176237d6008827cafb53105083792278af`  
		Last Modified: Thu, 13 Nov 2025 21:33:31 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13823e9a93091f70cf2b27cba9a3176affc30a722e82c96f903729099f471312`  
		Last Modified: Thu, 13 Nov 2025 21:33:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226776330c0e3ef29276e9c6c40618d1b79b984ae26045f02984d4d6a651e5d2`  
		Last Modified: Thu, 13 Nov 2025 21:33:31 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec59eb164ad928581ae0dbe4b3a92301d2410f4c73e92497533ca9b02b0e5871`  
		Last Modified: Fri, 14 Nov 2025 19:34:55 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d9fc1ba79fabe030a38e2deb87ad0ef5db8cbf5977d5ffaf6f6ebaafe2c981`  
		Last Modified: Fri, 14 Nov 2025 19:34:55 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:8eb6e60132a41ddac9473838f41465036b3989df7d67f37d0bfe82f10b86bed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.7 KB (637717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5effd3983bb52c56e458dca2cd6877937eb8da53244fd5c77e08ecfb0afd8874`

```dockerfile
```

-	Layers:
	-	`sha256:ee28d7b79f338ddace25fa61d8c197599ff06aef8f43c8c50305ed566b5aa05b`  
		Last Modified: Fri, 14 Nov 2025 21:13:24 GMT  
		Size: 593.4 KB (593358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2b7ee0479cefd2f662ae7c12515b8507b265e65b7000e511c61eeccf652653`  
		Last Modified: Fri, 14 Nov 2025 21:13:24 GMT  
		Size: 44.4 KB (44359 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:0cedfbc501d38828a3ac8f9a05b7281f5b35f3d573cc8f8688bb6467cb6edc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109495085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51cfb9f11d93a75d0f8bf7ca25489c60c0b5760ab8fc04f00ed72df239a76496`
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
ENV PG_MAJOR=16
# Fri, 14 Nov 2025 07:42:02 GMT
ENV PG_VERSION=16.11
# Fri, 14 Nov 2025 07:42:02 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Fri, 14 Nov 2025 07:42:02 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 08:31:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 08:31:29 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 08:31:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 08:31:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 08:31:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 08:31:30 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 15 Nov 2025 07:42:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 15 Nov 2025 07:42:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 15 Nov 2025 07:42:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Nov 2025 07:42:38 GMT
STOPSIGNAL SIGINT
# Sat, 15 Nov 2025 07:42:38 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 15 Nov 2025 07:42:38 GMT
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
	-	`sha256:cc32372c630598e9c32e0489613a2ccab3abb48679f36a463a8c2a392e4d6dca`  
		Last Modified: Fri, 14 Nov 2025 08:34:54 GMT  
		Size: 105.1 MB (105096049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a4dba820ccef32b476f89043cbc0d795b96f8d6be79713de715738c19f746d`  
		Last Modified: Fri, 14 Nov 2025 08:34:43 GMT  
		Size: 9.6 KB (9567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1878f9b5ab09ee7d689bb2c7f89959074e3bfc5d26bbd3e53ec7e3e5a49614b4`  
		Last Modified: Fri, 14 Nov 2025 08:34:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fb5ee143a12e841a8b10476fb1bddc316d1b212b4d2e793428becc35bfc34c`  
		Last Modified: Fri, 14 Nov 2025 08:34:44 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f962459f3c54d9fad80b2fd4685fb8381b178db08b221138560c9c1a3fdc8f`  
		Last Modified: Sat, 15 Nov 2025 07:43:59 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d88fb469e6d5ef194abb7c581fc9a7ea64ff792ba35694d9080678d5329af83`  
		Last Modified: Sat, 15 Nov 2025 07:43:59 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:4779282dae47e559f8c87b512388ce251d14dfedfdbbf90a3488d80d189582f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.4 KB (639382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e24fa4da9afbd3d59f05004f24764cd2a979e290fc0c0965cc03e475b94644`

```dockerfile
```

-	Layers:
	-	`sha256:5d6f9e3d9424f932344adc5dfd66b129037b49d573f18451b56d79ed7943255a`  
		Last Modified: Sat, 15 Nov 2025 09:08:06 GMT  
		Size: 595.0 KB (595016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a20efac8e9b6c4dbab617861c8018dbe7ec405292835b52af92e2377a0493b0`  
		Last Modified: Sat, 15 Nov 2025 09:08:07 GMT  
		Size: 44.4 KB (44366 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:f8335d4599dbb92ce14777179b57e05a7ec9b20d626bef6a4ebe604fa149fa24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118182642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec5fd92433549f1041d894a195ab99b165fbc1e4ac80df63f1f281fc58e387f`
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
ENV PG_MAJOR=16
# Fri, 14 Nov 2025 01:24:12 GMT
ENV PG_VERSION=16.11
# Fri, 14 Nov 2025 01:24:12 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Fri, 14 Nov 2025 01:24:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 01:27:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 01:27:03 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 01:27:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 01:27:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 01:27:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 01:27:03 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:34:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:34:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:34:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:34:45 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:34:45 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:34:45 GMT
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
	-	`sha256:79779a960d52b35c2f91a115ab8fe036b19a4a7e4b508b7441700e92ad62a87a`  
		Last Modified: Fri, 14 Nov 2025 01:27:47 GMT  
		Size: 113.6 MB (113621832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff89726acd5d172f80f564aafa849445c779716f5e7a5ba43bad42ee611a3f99`  
		Last Modified: Fri, 14 Nov 2025 01:27:35 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94f9a9f0b8e91e38655eb80d2cb19ad6a68edea804e7bdeb638dce8e3fae7fd`  
		Last Modified: Fri, 14 Nov 2025 01:27:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd213bb65324f3224ed18db3ff9adf080dc14ec4c06e0ea97ef0210eb4c1c9f9`  
		Last Modified: Fri, 14 Nov 2025 01:27:35 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e761d1e0f28417e8426745276702840f5955d0dbe5190ec8821bfa637d57b77`  
		Last Modified: Fri, 14 Nov 2025 19:35:02 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bf0fafd2a2b7997999676bec76d3e345628876ddbd919365f43a589177b563`  
		Last Modified: Fri, 14 Nov 2025 19:35:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:113760a14075e61c4e0b097030ad5a7c904be573062dae9a02e4bc2123bdb34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.3 KB (639292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42a746e46cc775a85000c4db755da80247989263814899c4d33b1f39509e197`

```dockerfile
```

-	Layers:
	-	`sha256:bb1fee8596dafb1318fe41be8d30677271c69d61f93ee8b5a2127ad3be3c47a2`  
		Last Modified: Fri, 14 Nov 2025 21:13:30 GMT  
		Size: 595.0 KB (594986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d46b395c27ac3eb87ac760dbe7a0c25bd9e7140bd438760c4c202ce9cee5230`  
		Last Modified: Fri, 14 Nov 2025 21:13:31 GMT  
		Size: 44.3 KB (44306 bytes)  
		MIME: application/vnd.in-toto+json
