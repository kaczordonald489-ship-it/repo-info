## `postgres:alpine3.23`

```console
$ docker pull postgres@sha256:aa6eb304ddb6dd26df23d05db4e5cb05af8951cda3e0dc57731b771e0ef4ab29
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

### `postgres:alpine3.23` - linux; amd64

```console
$ docker pull postgres@sha256:d326bec58d3de8d239df60475941522342723934a2598ae59a0281f077681462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.0 MB (111953772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04468c397044e22f2311a8fd8e5ddb478ab686b67634da068b9bd4b2d2eb3252`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:39:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 29 Jan 2026 19:39:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 29 Jan 2026 19:39:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Jan 2026 19:39:09 GMT
ENV LANG=en_US.utf8
# Thu, 29 Jan 2026 19:39:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:39:09 GMT
ENV PG_MAJOR=18
# Thu, 29 Jan 2026 19:39:09 GMT
ENV PG_VERSION=18.1
# Thu, 29 Jan 2026 19:39:09 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 29 Jan 2026 19:39:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 29 Jan 2026 19:41:42 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 29 Jan 2026 19:41:42 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 29 Jan 2026 19:41:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 29 Jan 2026 19:41:42 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 29 Jan 2026 19:41:42 GMT
VOLUME [/var/lib/postgresql]
# Thu, 29 Jan 2026 19:41:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:41:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 29 Jan 2026 19:41:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:41:42 GMT
STOPSIGNAL SIGINT
# Thu, 29 Jan 2026 19:41:42 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 29 Jan 2026 19:41:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31055bc7acf8f02e8948788a299494b902eabf6a1630bc00dd6e73e81bd4e4fe`  
		Last Modified: Thu, 29 Jan 2026 19:41:59 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cb70c4736cc8f2a16ad16a127038dffb6d02c668b26032753c7d9446738453`  
		Last Modified: Thu, 29 Jan 2026 19:41:59 GMT  
		Size: 922.9 KB (922927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1259989e70571fe22ece8998b7d9df368367a557f6d54306eab9d35a7e5f14fe`  
		Last Modified: Thu, 29 Jan 2026 19:41:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b091927013554b4c58cf0dc6540465c58a56edbb7860c496c4d7fb21b6cf38`  
		Last Modified: Thu, 29 Jan 2026 19:42:01 GMT  
		Size: 107.1 MB (107143006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa25427876673fd435f34e12923a67d82df43c2793eae502b9c1f267d2c3aa68`  
		Last Modified: Thu, 29 Jan 2026 19:42:00 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b223957d226280bf58abc66432f7afe3c96dc3e6843e1d945ed6141ad54dc053`  
		Last Modified: Thu, 29 Jan 2026 19:42:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a9b713c15a1b9ab905d397a965e79081012c576115cc6487f871177fea104f`  
		Last Modified: Thu, 29 Jan 2026 19:42:00 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644c7492dc079f06525810f2fc9e352eff76be88a4c1a816d9b1377a40b6a044`  
		Last Modified: Thu, 29 Jan 2026 19:42:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:8b792418c549075f21771bb7dde8bf407c5d93aa6f8738b868aa9a6f35f947b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.9 KB (640860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f990c0649858822d61d99fe1c7cdb44472c46095b61ec25712aa9f96700fa47`

```dockerfile
```

-	Layers:
	-	`sha256:997603d348c20ac0023c0f332d7257bec831465a7ad3d1f79147123ccc1826c1`  
		Last Modified: Thu, 29 Jan 2026 19:41:59 GMT  
		Size: 600.3 KB (600312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f8db25e674a01da7c8cb4ccb0fceee809efd8cccef6f45e462bb9e576c3bd01`  
		Last Modified: Thu, 29 Jan 2026 19:41:59 GMT  
		Size: 40.5 KB (40548 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.23` - linux; arm variant v6

```console
$ docker pull postgres@sha256:e323163514d981836ab8f999e634aa8f4b18b6f7564df9eda7819e916319f04e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91422846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cba38c09366fc555f76e69d2ebb62d5b059c89898524766c2739b58a88c5d06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:40:04 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 29 Jan 2026 19:40:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 29 Jan 2026 19:40:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Jan 2026 19:40:08 GMT
ENV LANG=en_US.utf8
# Thu, 29 Jan 2026 19:40:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:40:08 GMT
ENV PG_MAJOR=18
# Thu, 29 Jan 2026 19:40:08 GMT
ENV PG_VERSION=18.1
# Thu, 29 Jan 2026 19:40:08 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 29 Jan 2026 19:40:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 29 Jan 2026 19:42:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 29 Jan 2026 19:42:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 29 Jan 2026 19:42:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 29 Jan 2026 19:42:57 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 29 Jan 2026 19:42:57 GMT
VOLUME [/var/lib/postgresql]
# Thu, 29 Jan 2026 19:42:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:42:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 29 Jan 2026 19:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:42:57 GMT
STOPSIGNAL SIGINT
# Thu, 29 Jan 2026 19:42:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 29 Jan 2026 19:42:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88dd63c8946a4a1dfe7ed910c60f736f5befe29ed683aebe82399a8de5cb61bf`  
		Last Modified: Thu, 29 Jan 2026 19:43:07 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f0310402c654b9c5fa07100845ba75f64c279462b1024eaec6ddc521e8c9a`  
		Last Modified: Thu, 29 Jan 2026 19:43:08 GMT  
		Size: 889.5 KB (889469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeca996d998441572e70f1a0618c47d46e5d4c0d39db64dae7fe42a40573121f`  
		Last Modified: Thu, 29 Jan 2026 19:43:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a182d93d94331976db4ea2cb7a570896b4eea307b924f4f6ba1faed608a6b2f5`  
		Last Modified: Thu, 29 Jan 2026 19:43:10 GMT  
		Size: 86.9 MB (86937543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e98d1655eb3f68f0bdb83daa68ad873ab5d7e5ebf788c006e60b9df2c0d6ee5`  
		Last Modified: Thu, 29 Jan 2026 19:43:09 GMT  
		Size: 18.8 KB (18775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c6746f6e8d979ca0683d48e34452a210292daf021bc615dd2dc6785ba452a3`  
		Last Modified: Thu, 29 Jan 2026 19:43:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50eee732d5a28e5a0f1b9243952b868657f935d73f7accc7e29cbad942c7ee51`  
		Last Modified: Thu, 29 Jan 2026 19:43:09 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea959461f388a36818568894ddf2aaa5fdad8fc0acae5313b238c99d349f396`  
		Last Modified: Thu, 29 Jan 2026 19:43:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:0a0410337a94bb7b5471559431b7d763eb74f535c7b9fbdbca23522589286d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 KB (40502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbcd5d8f269db2a0fa8efc7e95c8c9bd38c405cdec7ec5b982d1430b0daf0a95`

```dockerfile
```

-	Layers:
	-	`sha256:0c7c8b47d9c09a4bc6d91abce9f6d2a3ef72b26603a1910c91fa2ab94d88af0f`  
		Last Modified: Thu, 29 Jan 2026 19:43:07 GMT  
		Size: 40.5 KB (40502 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.23` - linux; arm variant v7

```console
$ docker pull postgres@sha256:186b1f1981e486ea9bcdfd9006116a5ad26d6415acc67fe8515a1780bc37cc16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86573850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00277c48473928c0f5b8872a53b022b632664f445ece94194a71102be6a8dc3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:40:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 29 Jan 2026 19:40:15 GMT
ENV GOSU_VERSION=1.19
# Thu, 29 Jan 2026 19:40:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Jan 2026 19:40:15 GMT
ENV LANG=en_US.utf8
# Thu, 29 Jan 2026 19:40:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:40:15 GMT
ENV PG_MAJOR=18
# Thu, 29 Jan 2026 19:40:15 GMT
ENV PG_VERSION=18.1
# Thu, 29 Jan 2026 19:40:15 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 29 Jan 2026 19:40:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 29 Jan 2026 19:42:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 29 Jan 2026 19:42:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 29 Jan 2026 19:42:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 29 Jan 2026 19:42:59 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 29 Jan 2026 19:42:59 GMT
VOLUME [/var/lib/postgresql]
# Thu, 29 Jan 2026 19:43:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:43:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 29 Jan 2026 19:43:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:43:00 GMT
STOPSIGNAL SIGINT
# Thu, 29 Jan 2026 19:43:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 29 Jan 2026 19:43:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac8fb7fe2c6e913036908e5b506c8360cc7536421c2016566da9dfc1602909e`  
		Last Modified: Thu, 29 Jan 2026 19:43:11 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0c8a1419375bbc4f380c0798b7d110f89c892b45e27121edf9252cb1716460`  
		Last Modified: Thu, 29 Jan 2026 19:43:11 GMT  
		Size: 889.5 KB (889506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fc6c49bb0d5594432b7c05a94ab201ddd67d5cab7bc49c55dd8f4b7d87a86b`  
		Last Modified: Thu, 29 Jan 2026 19:43:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e7b2aba19a8e2de0bed58adcbeeecf127f7bfa0ee107e294c8eb03bddc42f`  
		Last Modified: Thu, 29 Jan 2026 19:43:14 GMT  
		Size: 82.4 MB (82376604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4550f7afc641e4f4765081550708c753fdfb66ae5cf907ed49294b4e24d88d29`  
		Last Modified: Thu, 29 Jan 2026 19:43:12 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778e4c3b843832db76ac022879e4a426693016c9935388fab7f6bb427c2a147e`  
		Last Modified: Thu, 29 Jan 2026 19:43:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e199b51947ceea22ad82be0653a9534944b63e857a4679c0c9a84f3add6c943d`  
		Last Modified: Thu, 29 Jan 2026 19:43:13 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b1d4d3ed5bcb829f32260b3d670c41d6945d845f8b7b6b923f68012e7a18c3`  
		Last Modified: Thu, 29 Jan 2026 19:43:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:c4b31ba4c56a8c51272dcf66fe7f30c630c8dbbdf97fd15898cddef5dae2daee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.4 KB (640431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a687652ac97c502a7e9ce69971f421455df8bd13a933f92a5685e4857d798c4`

```dockerfile
```

-	Layers:
	-	`sha256:11413c2b1d24059281a82ab032909f04de7840d2c682ea81fd67204ec2457c11`  
		Last Modified: Thu, 29 Jan 2026 19:43:11 GMT  
		Size: 599.7 KB (599714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:631b03279addca953df1783aa853e5052da379a92917051b88940391c81fa308`  
		Last Modified: Thu, 29 Jan 2026 19:43:11 GMT  
		Size: 40.7 KB (40717 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:70c585d0e816fc96a4a3a0c938170db6cbe2af35f28bbd6997c5291c3ec64239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110133444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f1036a9148b028c43669532b2f1c7eed3c8b63a7e92abea98b70388b27dccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:38:29 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 29 Jan 2026 19:38:31 GMT
ENV GOSU_VERSION=1.19
# Thu, 29 Jan 2026 19:38:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Jan 2026 19:38:31 GMT
ENV LANG=en_US.utf8
# Thu, 29 Jan 2026 19:38:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:38:32 GMT
ENV PG_MAJOR=18
# Thu, 29 Jan 2026 19:38:32 GMT
ENV PG_VERSION=18.1
# Thu, 29 Jan 2026 19:38:32 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 29 Jan 2026 19:38:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 29 Jan 2026 19:40:53 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 29 Jan 2026 19:40:54 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 29 Jan 2026 19:40:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 29 Jan 2026 19:40:54 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 29 Jan 2026 19:40:54 GMT
VOLUME [/var/lib/postgresql]
# Thu, 29 Jan 2026 19:40:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:40:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 29 Jan 2026 19:40:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:40:54 GMT
STOPSIGNAL SIGINT
# Thu, 29 Jan 2026 19:40:54 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 29 Jan 2026 19:40:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e47cf0676d3d3b5854fb4553857c2aec20755ad8b71ca6a7a981ab6caad1b5`  
		Last Modified: Thu, 29 Jan 2026 19:41:09 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ea32af8014119613519059cfe315c541abd4397e5da16887c6b9b7cb90cc0b`  
		Last Modified: Thu, 29 Jan 2026 19:41:09 GMT  
		Size: 876.5 KB (876485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0489a2a67255a6821e500af9172b3ccaeb7fd6ce56f6df5ac21c0194284ab58`  
		Last Modified: Thu, 29 Jan 2026 19:41:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c52a390312226784c58cedd51fb737e3968365a224fd4e1ef40c879723ddf3`  
		Last Modified: Thu, 29 Jan 2026 19:41:11 GMT  
		Size: 105.0 MB (105033844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d3df1e0a07acd277887b2e383040b7e06d633069c4ab99f415a1eb658c9ab0`  
		Last Modified: Thu, 29 Jan 2026 19:41:10 GMT  
		Size: 18.8 KB (18781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985559206ccedfa27156fee72804ac16820fc27dc4d9cc9e61a082a5c1a1fc26`  
		Last Modified: Thu, 29 Jan 2026 19:41:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77ffbdd9c8a4c649077c3dcc6f4fd2fc6f9783ea464c6439b079dcaeb95e37f`  
		Last Modified: Thu, 29 Jan 2026 19:41:10 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a22118cbd7d6333113df3bb972a4fbc1eee509e0e85761a8422a548168e4c4`  
		Last Modified: Thu, 29 Jan 2026 19:41:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:fd0a6cf0eaee2ce2d18d47f99fa75e99dc02ce2f2a1d15fe7caf77ddf66740d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.5 KB (640508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71702f82d350227c8dc7a06568d7dd5c9329de1e50f3c144d1a68f4d2e780675`

```dockerfile
```

-	Layers:
	-	`sha256:8b0c8256bd582758d037d5fa409a3806640241d4a5ec465ee263ae16679c5acb`  
		Last Modified: Thu, 29 Jan 2026 19:41:09 GMT  
		Size: 599.7 KB (599742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1910672ff6d2c50e0dd73f0c130de519c7e22f8190f1ad8826807ee92f975162`  
		Last Modified: Thu, 29 Jan 2026 19:41:09 GMT  
		Size: 40.8 KB (40766 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.23` - linux; 386

```console
$ docker pull postgres@sha256:5d181cfe9939aaef5f9d70c926d3183c7094f0fd37a66de7f9e9f9a51cc80fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118114598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5938e7afda3c783f56f734e6da5dc9815b88e3bfeecd9be09dfda75df06c0d4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:39:54 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 29 Jan 2026 19:39:58 GMT
ENV GOSU_VERSION=1.19
# Thu, 29 Jan 2026 19:39:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Jan 2026 19:39:58 GMT
ENV LANG=en_US.utf8
# Thu, 29 Jan 2026 19:39:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:39:58 GMT
ENV PG_MAJOR=18
# Thu, 29 Jan 2026 19:39:58 GMT
ENV PG_VERSION=18.1
# Thu, 29 Jan 2026 19:39:58 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 29 Jan 2026 19:39:58 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 29 Jan 2026 19:42:36 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 29 Jan 2026 19:42:36 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 29 Jan 2026 19:42:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 29 Jan 2026 19:42:36 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 29 Jan 2026 19:42:36 GMT
VOLUME [/var/lib/postgresql]
# Thu, 29 Jan 2026 19:42:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:42:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 29 Jan 2026 19:42:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:42:36 GMT
STOPSIGNAL SIGINT
# Thu, 29 Jan 2026 19:42:36 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 29 Jan 2026 19:42:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae434485a715411581a4fe5f7097af5d891e772c1572ecf120ce7952eb96efb`  
		Last Modified: Thu, 29 Jan 2026 19:42:52 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19065daf3bff50ccdb45fa8cf33adca49de07321c0e542be9bb18355e57876a`  
		Last Modified: Thu, 29 Jan 2026 19:42:53 GMT  
		Size: 893.3 KB (893254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b317cef5a2181d90a03bbe07e85e21c8ec8cc7d50e4abf6add9b672f4ef22023`  
		Last Modified: Thu, 29 Jan 2026 19:42:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f7e2682328d1bc576497b1bb5b7f613173f1afb82c0ff98ab275e018d929a4`  
		Last Modified: Thu, 29 Jan 2026 19:42:55 GMT  
		Size: 113.5 MB (113508336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705136de90ce89be7ef781d9318736f5a463bbd038daa759f7e83658a3352c4e`  
		Last Modified: Thu, 29 Jan 2026 19:42:54 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f05e0baf3b09de5b838250087672d4697b4236e6985a3eaf3d849723a8fc84`  
		Last Modified: Thu, 29 Jan 2026 19:42:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0bd5b681cf287c38084ac165cbb74c2793df6c0cc9354c255d97188b6ee8f5`  
		Last Modified: Thu, 29 Jan 2026 19:42:54 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee50d32bf177535432c654e0ca6322b668d4088b64917f57496119cedc92ee7`  
		Last Modified: Thu, 29 Jan 2026 19:42:55 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:005b0b6f08f83c709973c39673e912a74af7e2762b6f0bd96b4b3cce9e7a957d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.8 KB (640771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b004349c5d629202e3920703470d41afe95b60092db2c0b952332b08058b49`

```dockerfile
```

-	Layers:
	-	`sha256:5519853ce59bb377466e2265f7a1418a10997a7df24e2d10d9764d33e13f7fd2`  
		Last Modified: Thu, 29 Jan 2026 19:42:53 GMT  
		Size: 600.3 KB (600277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc08612b49d9222a97fffbd6f7fb785e19949a76c9970ab7c390d3e6b11e6fbe`  
		Last Modified: Thu, 29 Jan 2026 19:42:52 GMT  
		Size: 40.5 KB (40494 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.23` - linux; ppc64le

```console
$ docker pull postgres@sha256:ecec5504aac5a9f80c67e9bbce8772496339cc00a7d67c6994b7d4f0d0606292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97053391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c313c12105cb839d6ea7acc33c54412b39dabc8aaff5f7b2b387a6c6c209f949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:31:57 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 03:32:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 03:32:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 03:32:03 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 03:32:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 03:32:03 GMT
ENV PG_MAJOR=18
# Wed, 28 Jan 2026 03:32:03 GMT
ENV PG_VERSION=18.1
# Wed, 28 Jan 2026 03:32:03 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Wed, 28 Jan 2026 03:32:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 03:34:43 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 03:34:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 03:34:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 03:34:44 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 28 Jan 2026 03:34:44 GMT
VOLUME [/var/lib/postgresql]
# Thu, 29 Jan 2026 19:53:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:53:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 29 Jan 2026 19:53:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:53:40 GMT
STOPSIGNAL SIGINT
# Thu, 29 Jan 2026 19:53:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 29 Jan 2026 19:53:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd4e647df17c82db9ca398b2f463b9b25ee74420a55b31a9516facb1afa9c46`  
		Last Modified: Wed, 28 Jan 2026 03:35:18 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71de422e36f20b27957805987c70f9baf3d78aeb5185cefb6ba5e8f87a61453`  
		Last Modified: Wed, 28 Jan 2026 03:35:19 GMT  
		Size: 881.5 KB (881539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7649bce93f6f6f2482a38dc7082290155239a95f5f9f1e205d69594e44341386`  
		Last Modified: Wed, 28 Jan 2026 03:35:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f900a7baf6eac79f5c90f10696279190ae9b15a955a40f2c5c807e0caeea7f9`  
		Last Modified: Wed, 28 Jan 2026 03:35:21 GMT  
		Size: 92.3 MB (92316178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2705587bad70461e86cbfe439f16d82d433d196df2734a4eae9e44f1562965`  
		Last Modified: Wed, 28 Jan 2026 03:35:20 GMT  
		Size: 18.8 KB (18784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ff2c826717172b086ab7d5e4fd1196e8fc91f8ed526eab7f23970158ed944c`  
		Last Modified: Wed, 28 Jan 2026 03:35:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6d87f012ae38f4c6b611ae2336641d0b21019d9bf47db34c2c89d783bb650f`  
		Last Modified: Thu, 29 Jan 2026 19:53:57 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb28f327aae40a11598d0980941ba7d5a38de7c0e052f334e41ccec55f3678e5`  
		Last Modified: Thu, 29 Jan 2026 19:53:57 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:c3cb3210bb0092bb63b86906062ea4e20fe810f2ccc2499aaa8f339a332d203e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.7 KB (638656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfe221cb9cedc2ef1271043966f605e9f802f664a27a4a40279a648a0ad49db`

```dockerfile
```

-	Layers:
	-	`sha256:ba88f695899175ca6176165bdf6591e66f4743c4e1586b8d0a6f07c365b35c4f`  
		Last Modified: Thu, 29 Jan 2026 19:53:57 GMT  
		Size: 598.0 KB (598045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eddd2847bd190f563573c6f5eca83fc1108d680da72cdb7bac465e3cd0e69d1d`  
		Last Modified: Thu, 29 Jan 2026 19:53:56 GMT  
		Size: 40.6 KB (40611 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.23` - linux; riscv64

```console
$ docker pull postgres@sha256:d988570297bce7de9af2df5ee6a28cb903a967f062739ee43ce0c13d08a73c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113210121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa7e27e5fcda0d756ef9031a5d4a86dae8afdb79ba41f3fa2e7503fdd44e633`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 09:58:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 29 Jan 2026 09:58:31 GMT
ENV GOSU_VERSION=1.19
# Thu, 29 Jan 2026 09:58:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Jan 2026 09:58:31 GMT
ENV LANG=en_US.utf8
# Thu, 29 Jan 2026 09:58:31 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 09:58:31 GMT
ENV PG_MAJOR=18
# Thu, 29 Jan 2026 09:58:31 GMT
ENV PG_VERSION=18.1
# Thu, 29 Jan 2026 09:58:31 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 29 Jan 2026 09:58:31 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sun, 01 Feb 2026 00:02:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sun, 01 Feb 2026 00:02:26 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sun, 01 Feb 2026 00:02:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sun, 01 Feb 2026 00:02:26 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Sun, 01 Feb 2026 00:02:26 GMT
VOLUME [/var/lib/postgresql]
# Sun, 01 Feb 2026 00:02:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sun, 01 Feb 2026 00:02:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sun, 01 Feb 2026 00:02:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 01 Feb 2026 00:02:27 GMT
STOPSIGNAL SIGINT
# Sun, 01 Feb 2026 00:02:27 GMT
EXPOSE map[5432/tcp:{}]
# Sun, 01 Feb 2026 00:02:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cd0423c54304765761b5714497271a760ee5b91f2e20ac5431b606eea75e09`  
		Last Modified: Thu, 29 Jan 2026 10:54:28 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23d3b79973bc6cdb8e14d0563cf090fb72b2938c43650f9431a43694c7832ff`  
		Last Modified: Thu, 29 Jan 2026 10:54:28 GMT  
		Size: 868.9 KB (868946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d03fa7f67297779ea9f388f1019c89b16a9ebec346a6915ce5dd0c30696e2c`  
		Last Modified: Thu, 29 Jan 2026 10:54:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbfd870c17dc4ff3bafc048fcadb5f9ec2d681760354bbda7276155473b0f96`  
		Last Modified: Sun, 01 Feb 2026 00:05:34 GMT  
		Size: 108.7 MB (108729859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce566cc607eee6193c1a3400e744bc61b8e3e2e5c0aca99c64ecf224ed9e55b`  
		Last Modified: Sun, 01 Feb 2026 00:05:19 GMT  
		Size: 18.8 KB (18783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2688c5fb44051707b159173a1d32e656ef749dcfdd3bf7688c0bc3ffb9b5ac23`  
		Last Modified: Sun, 01 Feb 2026 00:05:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b6f68940bec74e2def897d19c349027bf0ac4a0c8ed6bd5cc8e53dfcdcb7b`  
		Last Modified: Sun, 01 Feb 2026 00:05:19 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff88c2f954479ef230bd495b324b9afba00c6f49a7645e16abc24b7b2331f468`  
		Last Modified: Sun, 01 Feb 2026 00:05:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:014e4ab08955a1515a854ca5eb202a9b90f2255c83a1804582262643cf780008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.3 KB (640319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bde8c49251de77f39c844e590671a37a7c6bd75e121cb932019e01594d7df2`

```dockerfile
```

-	Layers:
	-	`sha256:b00361ef7258912dc5103d4ddb1a126b00cc90a484280e2750cf9ae1ef187a58`  
		Last Modified: Sun, 01 Feb 2026 00:05:19 GMT  
		Size: 599.7 KB (599703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a938ba8f7bcf21b2d38838079dacf505f6dd6ca97b897667d2631987be3fbe0d`  
		Last Modified: Sun, 01 Feb 2026 00:05:18 GMT  
		Size: 40.6 KB (40616 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.23` - linux; s390x

```console
$ docker pull postgres@sha256:a3d3b260911fa0a7943b9074c6271a512c22a079300a3bbf96ee36de63967eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120178173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2d74ac44acc3b5acab277ad1bcd4d57d8a1c80cc9f3c1a98953dd21798e65b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:40:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 29 Jan 2026 19:40:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 29 Jan 2026 19:40:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Jan 2026 19:40:21 GMT
ENV LANG=en_US.utf8
# Thu, 29 Jan 2026 19:40:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:40:21 GMT
ENV PG_MAJOR=18
# Thu, 29 Jan 2026 19:40:21 GMT
ENV PG_VERSION=18.1
# Thu, 29 Jan 2026 19:40:21 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 29 Jan 2026 19:40:21 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 29 Jan 2026 19:43:02 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 29 Jan 2026 19:43:02 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 29 Jan 2026 19:43:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 29 Jan 2026 19:43:03 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 29 Jan 2026 19:43:03 GMT
VOLUME [/var/lib/postgresql]
# Thu, 29 Jan 2026 19:43:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:43:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 29 Jan 2026 19:43:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:43:03 GMT
STOPSIGNAL SIGINT
# Thu, 29 Jan 2026 19:43:03 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 29 Jan 2026 19:43:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023cc4ef4cdd9b53414cd9a8388e81521346cd592de6a14c400bd849a0374e29`  
		Last Modified: Thu, 29 Jan 2026 19:43:25 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e51970f5768df5901c53b1b1b5d5863ddcfb1a059f2e76d86d4b2793aa552e`  
		Last Modified: Thu, 29 Jan 2026 19:43:25 GMT  
		Size: 897.4 KB (897421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fd13c0e4f5aa51f85dcd7707806e1cb56b83a5f1bbb1a476ed119ab503ec34`  
		Last Modified: Thu, 29 Jan 2026 19:43:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca18b8f4406dd108a6f6498d23768ede633c9f590aff40dada43b1124aeb7bf`  
		Last Modified: Thu, 29 Jan 2026 19:43:28 GMT  
		Size: 115.5 MB (115529404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfbad23421b105019e73ae32434e905ba944f9509cf266a7f57f03eba0c2a35`  
		Last Modified: Thu, 29 Jan 2026 19:43:26 GMT  
		Size: 18.8 KB (18774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0022eae008b0e9067a22f35c329e2f247bb6285df139ab5ccdff4f651ad4d6`  
		Last Modified: Thu, 29 Jan 2026 19:43:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d36b49f42c7984b4d4444bb8de6793c4a95d3c4f2af24127f176acd7ed15d09`  
		Last Modified: Thu, 29 Jan 2026 19:43:27 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413aa2239171ff32d8fe0d693dce5717293426fe821406218db69a12d85dedd6`  
		Last Modified: Thu, 29 Jan 2026 19:43:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:36ef46696029b37453604e5ea7b3c8fe489dc52fdce488bb8a56b6580e206c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbff741d749d0a7454c7da8763c9ed4adb7bfaec19ac40e26bfa5d7bec0f7ea`

```dockerfile
```

-	Layers:
	-	`sha256:1a707bcbb459add0d0c14b7cb841d8f32a9da12ff96202dd79b79c4b7c0b47fc`  
		Last Modified: Thu, 29 Jan 2026 19:43:25 GMT  
		Size: 599.7 KB (599661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:841708082d917074c6441ce3f3d5a9c238651535122435e51f712c3f7bd93cc9`  
		Last Modified: Thu, 29 Jan 2026 19:43:25 GMT  
		Size: 40.5 KB (40548 bytes)  
		MIME: application/vnd.in-toto+json
