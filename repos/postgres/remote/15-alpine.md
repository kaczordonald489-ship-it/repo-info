## `postgres:15-alpine`

```console
$ docker pull postgres@sha256:aa7b1ef595e165f0b780162e3a41edd0a7ed3ea672eb8a0f81615ba725e62bc5
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

### `postgres:15-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:89591860e36c50a660384d075ce684a48a0927a450f71a7f17b59eb2c4eb55cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108675728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df5377b1f74a457fbc870a6ed6a33e60a7a859e8cc691c94025925f608e3571`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:17:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:17:47 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:17:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:17:47 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:17:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:17:47 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 19:17:47 GMT
ENV PG_VERSION=15.15
# Fri, 14 Nov 2025 19:17:47 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Fri, 14 Nov 2025 19:17:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:19:51 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:19:51 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:19:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:19:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:19:52 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:19:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:19:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:19:52 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:19:52 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:19:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf483249d3ce18cd1f72b22ef5934e0b42b13abaf42e28df7bf2909ea84a9e35`  
		Last Modified: Fri, 14 Nov 2025 19:20:18 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cca80c190805368af61c6e488b5b4ad999b98b482e645471d2c1955868287fa`  
		Last Modified: Fri, 14 Nov 2025 19:20:18 GMT  
		Size: 918.3 KB (918291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18556747022261e8b356ab03f2638b95a70cca8c1215db60f9513b8b0b6f7eb`  
		Last Modified: Fri, 14 Nov 2025 19:20:18 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ea33b53489d4af49b161bc6dc31c2949c587c6d55db524f43c74887ec9a293`  
		Last Modified: Fri, 14 Nov 2025 19:20:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af6fa6f0560a9c1df153885bfb08b4e981c58a58def7b2f3c74af03ce94a7f3`  
		Last Modified: Fri, 14 Nov 2025 19:20:26 GMT  
		Size: 103.9 MB (103937962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a697983360637d0d88a89b3e7787d423ab772752ec7d4eed4873b6e9d2bb88`  
		Last Modified: Fri, 14 Nov 2025 19:20:18 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7391a4eb551592843fdb9954811473fa593789b6128ee90a8a4db712412d9f1`  
		Last Modified: Fri, 14 Nov 2025 19:20:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbcbe36cbe3d54e0d2d74cf740dce35c17bf77f4359ca20a7f2154408a3dd54`  
		Last Modified: Fri, 14 Nov 2025 19:20:18 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0a695ab338e37056915af8420c170ee18e1986101f9bc1bb39c5c5cdc5ea2f`  
		Last Modified: Fri, 14 Nov 2025 19:20:18 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8022888ce7ee1fd4c107278fba1475f7119be041b513f02d4659d1a5b34103`  
		Last Modified: Fri, 14 Nov 2025 19:20:18 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:7944259d4c74437f3c918721ec5eeb86dbdca9937dbfa256beccbf91ec3b4e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.3 KB (641327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a000159f7bca2030739e07a1f1977134ce7df3df502e96f71ae027ea646c3f80`

```dockerfile
```

-	Layers:
	-	`sha256:89c27b04335cf7f3a1caca150341f4ab988ab9f55f6aff5a9acd59b9906f48b6`  
		Last Modified: Fri, 14 Nov 2025 21:10:40 GMT  
		Size: 596.9 KB (596937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:180fb9644d7f9818264497286b498d2c431dde114088d24c85945685344e0530`  
		Last Modified: Fri, 14 Nov 2025 21:10:41 GMT  
		Size: 44.4 KB (44390 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:d3194ef787dad6b93a66b95fc0eee096229a4fd3309e47ff7279ca89ca496d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88288701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1075868005ec2d43ac6acd7fe7ac7589beeb9290beb0908ae331974283a6d48b`
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
# Fri, 14 Nov 2025 19:41:38 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:41:38 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:41:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:41:38 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 19:41:38 GMT
ENV PG_VERSION=15.15
# Fri, 14 Nov 2025 19:41:38 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Fri, 14 Nov 2025 19:41:38 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:44:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:44:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:44:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:44:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:44:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:44:24 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:44:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:44:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:44:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:44:25 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:44:25 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:44:25 GMT
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
	-	`sha256:e13dd79c8739f8e51bea30ae0706d5f9463796007d2c627dea4be31a9c080400`  
		Last Modified: Fri, 14 Nov 2025 19:44:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4050bceb1f56fad4ccab7d205d1969a12de5a2ba95027f4f9a76f403a9c4df00`  
		Last Modified: Fri, 14 Nov 2025 19:44:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a15296ddde85f09c1978ad6c7eae092471067277e81e63b0fbcc867ebeb2ee`  
		Last Modified: Fri, 14 Nov 2025 19:44:50 GMT  
		Size: 83.9 MB (83881464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b2217e1f1cf0e1f4ec54499f58f988b2da3ceb695d8b6590c2730ee4d8f537`  
		Last Modified: Fri, 14 Nov 2025 19:44:43 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e475fe2066cb134504eea3b42b46e21e4c57bb78cfa62637595798523f599c`  
		Last Modified: Fri, 14 Nov 2025 19:44:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ea6fab2f515be520edda1894b6f9ae869b895fc68ab72974338442545b910c`  
		Last Modified: Fri, 14 Nov 2025 19:44:43 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e0a1274111bd4627ac9491d073f936c6c9f221336c323b5c923db8b743ff77`  
		Last Modified: Fri, 14 Nov 2025 19:44:44 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd00420e075f129b7e5a0a706b0aa1d38e22f1b7f8d419d4f6837ecbee1552a2`  
		Last Modified: Fri, 14 Nov 2025 19:44:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:0feb21cfee3c22be5fba677b197c4479a4682773aa16941dff5840f8fbafabf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 KB (44350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c263a2a5017cc85571de4a784984425646baaf4fcb72068e533d3c8080c1e515`

```dockerfile
```

-	Layers:
	-	`sha256:ff79a4133e632033b55d495e2bb769e33b98cd7cdba81c5dc87ec9dd3a2c6e51`  
		Last Modified: Fri, 14 Nov 2025 21:10:44 GMT  
		Size: 44.4 KB (44350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:546e9e33fcf67c47c56528b0dab599f039a6b93a6fd4800ea20e0caa28bb325d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83571725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dec74d2c07f8cd64670e2eb0397d0f3c0025c8116f681fdf680b7abc192575`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:48:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:48:17 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:48:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:48:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:48:17 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:48:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:48:17 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 19:48:17 GMT
ENV PG_VERSION=15.15
# Fri, 14 Nov 2025 19:48:17 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Fri, 14 Nov 2025 19:48:17 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:50:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:50:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:50:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:50:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:50:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:50:55 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:50:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:50:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:50:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:50:55 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:50:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:50:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be37132cb101eaca65e5c7cb9ee0a9cf691102979c2f1fd1e6dc0cd1a17b41a`  
		Last Modified: Fri, 14 Nov 2025 19:51:15 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d1677a65db456cef14f09ffe57246b24dc1e4bc3dab8a83e53d655a6c44262`  
		Last Modified: Fri, 14 Nov 2025 19:51:15 GMT  
		Size: 886.1 KB (886131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fc48632997980e1e232a3b73bbc98a92d21bb007dc605a4928864d9ad52209`  
		Last Modified: Fri, 14 Nov 2025 19:51:15 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0065997f3c4952934b9ac80b9c830be962f9c7e0838ecc267ed2ba223d314b40`  
		Last Modified: Fri, 14 Nov 2025 19:51:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4012ac429c90e0f425f9e90a09a262747822f617a61e901b1c733593124bda8c`  
		Last Modified: Fri, 14 Nov 2025 19:51:22 GMT  
		Size: 79.4 MB (79447012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da532405cc18ca1a82a987cfd328cc46cdbeb6eeb063a569e44bf6a8dbff0c48`  
		Last Modified: Fri, 14 Nov 2025 19:51:15 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dbc4c2925a1e20dc1c008ddf835b916d3ff770d9f794a477563004759f2b0`  
		Last Modified: Fri, 14 Nov 2025 19:51:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4570b74a7ff4f22b3854e98645a4b7b62766b2c2d4fcabd01eadaad0bd2ac662`  
		Last Modified: Fri, 14 Nov 2025 19:51:15 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7141a0178e7d77f1d8edf3a00c2d3c08eb8a535c3bd9ca5a5ac8ccde96ec99`  
		Last Modified: Fri, 14 Nov 2025 19:51:15 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becd978f40d31c81b45879eff5048b31579a0df0fe4dee8854725ca1288f5cf8`  
		Last Modified: Fri, 14 Nov 2025 19:51:15 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:ade2a784efbaac5f2cd1fb42ba3abed6777a6263ad52538931f2b3807464c15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.5 KB (641541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87fdcb45332cea232963dcc28f22af3de9d7e5bc5830dad2dd72f43e0ea9780`

```dockerfile
```

-	Layers:
	-	`sha256:5cf30c274261d82e7472210ac528de9ea018636b7f3a4a5c4fe485bcad2b354c`  
		Last Modified: Fri, 14 Nov 2025 21:10:47 GMT  
		Size: 597.0 KB (596973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19a2fbbd0105ec6dc51add3bf09f18d8e851ff1097aa6439ca3993e624bc0d5c`  
		Last Modified: Fri, 14 Nov 2025 21:10:48 GMT  
		Size: 44.6 KB (44568 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:1ecbd7256ab99ba752d2ffd42752cd4c093fc0323651acf756665b99767c3ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104642916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777816e58741a2eba86cf35160088d009456ccb79f85cefdfe8fa137b267e04b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:19:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:19:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:19:57 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:19:57 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:19:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:19:58 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 19:19:58 GMT
ENV PG_VERSION=15.15
# Fri, 14 Nov 2025 19:19:58 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Fri, 14 Nov 2025 19:19:58 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:22:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:22:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:22:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:22:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:22:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:22:25 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:22:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:22:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:22:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:22:25 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:22:25 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:22:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918dc50b0c3b13c1bbdfeb85076d2f45fe6dc93cda956458c775b410570458c1`  
		Last Modified: Fri, 14 Nov 2025 19:22:48 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bea5cec08def158b18bb34727e5e88a1a34413be2774a9ce544b87ef6f3c00`  
		Last Modified: Fri, 14 Nov 2025 19:22:48 GMT  
		Size: 873.5 KB (873484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdd9b43831e254f99c42cbcd0d9c6046ca5747f9fe4d59e3df971511d423ba5`  
		Last Modified: Fri, 14 Nov 2025 19:22:48 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3781a02fc0dd6dbb431cd4882af4781685af70b00d5fa3c56d48fce6723426e6`  
		Last Modified: Fri, 14 Nov 2025 19:22:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28d7ed7398379b2aedda9aac3efe48dd4ba301aabad30f0ba88d907c1d8bd4d`  
		Last Modified: Fri, 14 Nov 2025 19:22:56 GMT  
		Size: 99.6 MB (99614341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddccc642fe77304bfd8800c3c431ee2b022af3c8bdb49c979085e41d261b76fb`  
		Last Modified: Fri, 14 Nov 2025 19:22:48 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00115bedd9d75e4620e3b298df803d7d4522efd097faa120e16277e44dac2bb4`  
		Last Modified: Fri, 14 Nov 2025 19:22:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0787301da5072e6e4de42e525f4d6337b4a2fadaf4c2ed90a0bd93d684126ed0`  
		Last Modified: Fri, 14 Nov 2025 19:22:48 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53aee089bc1bc035cd9dadcafc2e90689e34beb7099410f5ebc767a4506b033`  
		Last Modified: Fri, 14 Nov 2025 19:22:48 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798f0e545a1007db9e2cf325c7adcf833d6798e1804c2e8aafc803ab3a3ce161`  
		Last Modified: Fri, 14 Nov 2025 19:22:48 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:1a6cd861ab1c15373e67a496228d7391f25e65884f805eea3c140af4ba4c5cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 KB (641601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b8d13e753d6e00f12aacefd1085156007ce0b935a8f43d573776d54b700915`

```dockerfile
```

-	Layers:
	-	`sha256:fc57cac4e4e35d2a6fd54e8ec72103c900c91dd89d4e699f7674a12b9afd0f6e`  
		Last Modified: Fri, 14 Nov 2025 21:10:51 GMT  
		Size: 597.0 KB (596993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a92c9a48f810924287d34fc78b5e21272e2fdd232f4ad3230253073664f16b53`  
		Last Modified: Fri, 14 Nov 2025 21:10:52 GMT  
		Size: 44.6 KB (44608 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; 386

```console
$ docker pull postgres@sha256:df030d7d11e51fe3a0e5f0ff50cb0ea4589fa1d2a15e34abc853e08beb2d7c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114941950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c9f31a33812a340775868e9b8662008ce8bbb115077a75bf8864ba94a73588`
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
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 19:22:20 GMT
ENV PG_VERSION=15.15
# Fri, 14 Nov 2025 19:22:20 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Fri, 14 Nov 2025 19:22:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:27:02 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:27:02 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:27:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:27:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:27:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:27:03 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:27:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:27:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:27:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:27:03 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:27:03 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:27:03 GMT
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
	-	`sha256:5150c0512882bead2f94eb128a27ef4a4a1f4dd89e5cf3d1f945ca38f0c73e1a`  
		Last Modified: Fri, 14 Nov 2025 19:27:33 GMT  
		Size: 110.4 MB (110415351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e93caf523784110a7bf79fef8ed59454e0719dc0dc63f82abfb9ff69d898b5d`  
		Last Modified: Fri, 14 Nov 2025 19:27:26 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e47670581b26239feee25b9b89072f096b8e2423eaf6de0148247cf629a9a52`  
		Last Modified: Fri, 14 Nov 2025 19:27:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f32024ba0bcf32c76221c4711742edcf59cb94cbb1aa3020a3cc6875ec3c6`  
		Last Modified: Fri, 14 Nov 2025 19:27:26 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb09ec031babcc3b0b3ba24b9c248d96b6a2664a05ffed13eb03cae8d0162b4`  
		Last Modified: Fri, 14 Nov 2025 19:27:26 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ed71bfeed45a69c0d95d49add4baa116dd1ecca5abecf8dbc9bfcf42d8b9bc`  
		Last Modified: Fri, 14 Nov 2025 19:27:26 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:c8f631b3e0103745430e25090d9fd278c9bc03addfa948569660a2b5acdae0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.3 KB (641252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3418b6933f3e0824de4bcc79c2d201261c27dde15f6cdbba8d452023d44d71`

```dockerfile
```

-	Layers:
	-	`sha256:1edb999f913bfad892741dad53d037e911f63e7dc287021dae2c4dacbdd152b6`  
		Last Modified: Fri, 14 Nov 2025 21:10:54 GMT  
		Size: 596.9 KB (596912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1274fc7cdc38a028ccfc3cbe22aab656fb41ad89073a29ce7069cd71fcb66938`  
		Last Modified: Fri, 14 Nov 2025 21:10:55 GMT  
		Size: 44.3 KB (44340 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:a5af8d6db47d24899b2098c3861d8e227356190f80b8c52b418f96f7c5f194dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92416430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e20ef2f54995e7f2082defc8921127080a7cdf550b7452489f8571c00a44aa3c`
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
ENV PG_MAJOR=15
# Thu, 13 Nov 2025 21:29:53 GMT
ENV PG_VERSION=15.15
# Thu, 13 Nov 2025 21:29:53 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Thu, 13 Nov 2025 21:29:53 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Nov 2025 21:42:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:42:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:42:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:42:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:42:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:42:16 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:36:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:36:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:36:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:36:07 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:36:07 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:36:07 GMT
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
	-	`sha256:965c13175745717e507df68fa654dec4d54e4df98fac6ed6a19130eb950a3988`  
		Last Modified: Thu, 13 Nov 2025 21:43:15 GMT  
		Size: 87.8 MB (87788120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c858c2b44a70878c2eda1ac984c2d771c7ebd475fd72c20dd551e26138461347`  
		Last Modified: Thu, 13 Nov 2025 21:43:05 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1d9a4a34fd0c04745d4e165353792b5d8d453c2234205b8a42528b391a1dc9`  
		Last Modified: Thu, 13 Nov 2025 21:43:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a07c2cdcd1a8bd505b346219fd761476467ab8e83d5c7ea01223f078a754b3`  
		Last Modified: Thu, 13 Nov 2025 21:43:05 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a400125a98a5e5a0cdcd516c668fd1d1cf36b230e754a7b6996fa709eb3ab7`  
		Last Modified: Fri, 14 Nov 2025 19:36:37 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc79c1bfcdf4d25dcf897c920f796e1a5564d6766f713696c5a1a55caf1382c`  
		Last Modified: Fri, 14 Nov 2025 19:36:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:5a49150455eefbb7a9ea6f6f53b3b4e42a75f043b924ca2433ac947952925158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0675ed23e5cc6bfaddf1a552147577a1f4c1ead979c4a8aff9115da1811ff267`

```dockerfile
```

-	Layers:
	-	`sha256:dc7425ba6512aca545728321971fa4bb870349891994b74c7ccf6e5e0985097e`  
		Last Modified: Fri, 14 Nov 2025 21:10:58 GMT  
		Size: 593.4 KB (593358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51b23005c5895618860ecb3aaa8ea62c979944fbbae83eaa50aae909d8cf514e`  
		Last Modified: Fri, 14 Nov 2025 21:10:59 GMT  
		Size: 44.4 KB (44444 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:fe6dcc02e55139ed00c4747cc73ea9432695b784ab87820e3eaf5a51a942f972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108615329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2de6efa4b8c42aa02db5af3ba8acf224e37356e0848dc5c5cc17217b18594c`
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
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 07:42:02 GMT
ENV PG_VERSION=15.15
# Fri, 14 Nov 2025 07:42:02 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Fri, 14 Nov 2025 07:42:02 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 10:22:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 10:22:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 10:22:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 10:22:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 10:22:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 10:22:26 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 15 Nov 2025 09:51:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 15 Nov 2025 09:51:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 15 Nov 2025 09:51:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Nov 2025 09:51:35 GMT
STOPSIGNAL SIGINT
# Sat, 15 Nov 2025 09:51:35 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 15 Nov 2025 09:51:35 GMT
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
	-	`sha256:44143512cbb42a1efd6b3dc7bac9cf5fecf4cdaba24f1ade01989b860c1d9bb7`  
		Last Modified: Fri, 14 Nov 2025 10:25:42 GMT  
		Size: 104.2 MB (104216408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b353d8c3b0f1de46dfadc792ead303ac82bafda1226113fe2d7fbdbafa45b99`  
		Last Modified: Fri, 14 Nov 2025 10:25:38 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f38d82832eaeec386f4e140842f516432df6e8e31d0a61b68c7ed8c6ba093ed`  
		Last Modified: Fri, 14 Nov 2025 10:25:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc7d62b936690497e08cb8acac7952029a6f5a16c3f2d558d4f3d40ee2b9b1a`  
		Last Modified: Fri, 14 Nov 2025 10:25:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e561d4d26263487a383a6cf103f1c2ea9c4c2d34f16b7d745d12a1b273d0a3`  
		Last Modified: Sat, 15 Nov 2025 09:52:56 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6a5f71ce0835154937fa8355fea690c3dedefe1fd4a9b7c168361f5363776`  
		Last Modified: Sat, 15 Nov 2025 09:52:56 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:67c4e6309be8d93e0fea1fa9a05cbbf6d1c669c824d13cbeb596519f389dadd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.5 KB (639466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0c6f00b7487caf1cddeb2cde3859233cd11debdfa6dbb86b1517abe5631963`

```dockerfile
```

-	Layers:
	-	`sha256:f42e447fc1efa5d4c2a7cc285a5434c1edc6b004ecffb72734110992eb2c730a`  
		Last Modified: Sat, 15 Nov 2025 12:29:16 GMT  
		Size: 595.0 KB (595016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a66310147c1f422a1d95e47853679e796af931cbe35d125596d5c807cbbe68dd`  
		Last Modified: Sat, 15 Nov 2025 12:29:19 GMT  
		Size: 44.5 KB (44450 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:12afc4bdcd7724fffc21d97e68d32c775efb70044ff65514e0b4462371ffe9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 MB (117377584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b813f470ac3ed63ce6de2cd267cf77a5b13225f19e95c3b5127fbabffc5584c`
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
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 01:24:12 GMT
ENV PG_VERSION=15.15
# Fri, 14 Nov 2025 01:24:12 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Fri, 14 Nov 2025 01:24:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 02:43:18 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 02:43:18 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 02:43:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 02:43:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 02:43:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 02:43:18 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:35:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:35:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:35:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:35:17 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:35:17 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:35:17 GMT
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
	-	`sha256:2730712dd33522d17e97b5701f3cc62f2050a31301ce02945319e7b2befce107`  
		Last Modified: Fri, 14 Nov 2025 02:44:04 GMT  
		Size: 112.8 MB (112816885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4e1e0681ba1ef3aa5eb57c8dc6a6c7cdb3872bebde0979aece2107d3219d0c`  
		Last Modified: Fri, 14 Nov 2025 02:43:50 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4192e5491af9c3809185888dd7ed36902589a54190290574fd1c90e41bc0ca`  
		Last Modified: Fri, 14 Nov 2025 02:43:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed7c969136a93b72a0b5ab9c06f21fb18e551bf6db5ed6e06204a81eb18931a`  
		Last Modified: Fri, 14 Nov 2025 02:43:49 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fb5b593fa9332505e7244506435b61e6f6c3108a3fd1156742361f80f2aae2`  
		Last Modified: Fri, 14 Nov 2025 19:35:33 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ea3dcff44523a78fa473eb03788fd3ed8a1c95086781e0787935938682c420`  
		Last Modified: Fri, 14 Nov 2025 19:35:33 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:203ada7223eff1a5f19bc143b4f1b788cab0e6ed5079849d0c27a807d38a8852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.4 KB (639376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a606b57c5f95241aca4d1c37affc44dea0066d4db053bc49761688ee3ba845e4`

```dockerfile
```

-	Layers:
	-	`sha256:6c143a0dc8aeeb3f1667cb8316a937864b670d2815554fb4b048acb199199a42`  
		Last Modified: Fri, 14 Nov 2025 21:11:04 GMT  
		Size: 595.0 KB (594986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2501129c72b1e03e66cf0f7355b67376709ca1364d17364e144ac2b92d8549dc`  
		Last Modified: Fri, 14 Nov 2025 21:11:05 GMT  
		Size: 44.4 KB (44390 bytes)  
		MIME: application/vnd.in-toto+json
