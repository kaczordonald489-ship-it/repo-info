## `postgres:alpine3.22`

```console
$ docker pull postgres@sha256:270579ee277a572fa8cfdbaec0e1ff588bb7247da92d25165c7237c483e565d9
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

### `postgres:alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:b727c0d850d524e22a1b7c955784c671c8db4d9cda3112b968f8fbca0277433c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111495211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6f6e303e3c9a6551731a57c55a60236206727605afe87e4191ca84e0dc2d31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:38:58 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 29 Jan 2026 19:39:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 29 Jan 2026 19:39:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Jan 2026 19:39:01 GMT
ENV LANG=en_US.utf8
# Thu, 29 Jan 2026 19:39:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:39:01 GMT
ENV PG_MAJOR=18
# Thu, 29 Jan 2026 19:39:01 GMT
ENV PG_VERSION=18.1
# Thu, 29 Jan 2026 19:39:01 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 29 Jan 2026 19:39:01 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 29 Jan 2026 19:41:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 29 Jan 2026 19:41:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 29 Jan 2026 19:41:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 29 Jan 2026 19:41:37 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 29 Jan 2026 19:41:37 GMT
VOLUME [/var/lib/postgresql]
# Thu, 29 Jan 2026 19:41:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:41:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 29 Jan 2026 19:41:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:41:37 GMT
STOPSIGNAL SIGINT
# Thu, 29 Jan 2026 19:41:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 29 Jan 2026 19:41:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c323f6460343aa39583ac47de14a57666cfa7678cad2bcbc7919e43cf2b986f`  
		Last Modified: Thu, 29 Jan 2026 19:41:53 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e12a0d721cf06484f400cbd96f2ed350d953d67862ef560944c94e2fb9c481`  
		Last Modified: Thu, 29 Jan 2026 19:41:54 GMT  
		Size: 918.3 KB (918294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac96749dc05776fec7be302368dc10a6338d5c51fe41718c139489697d4e8c2`  
		Last Modified: Thu, 29 Jan 2026 19:41:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae36db76db0c5b541b9bfeed10f6f455e65f88ad6c69b44fb6641de35630d10`  
		Last Modified: Thu, 29 Jan 2026 19:41:56 GMT  
		Size: 106.7 MB (106746029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0716afd5d850723eb5707db24835c49999ec4179d21af41bc74a16a16f65a768`  
		Last Modified: Thu, 29 Jan 2026 19:41:54 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c6d4c4ce0050a22508355f07587644bd9d2bcce4509d181b122a4d29b22c0d`  
		Last Modified: Thu, 29 Jan 2026 19:41:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fdfc3688ad31ad1326a65117e3b52481b102661dd5fcf1d846ba143b59638f`  
		Last Modified: Thu, 29 Jan 2026 19:41:55 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853963d81c02bdf5cbc30430cd59b516d3701cd0ebf54246715d0a05e2409eb7`  
		Last Modified: Thu, 29 Jan 2026 19:41:56 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:4b464702932f9bf42d0c323d83d2e40eba3da08e7b581cbdf556ea9e6ec432be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.9 KB (637870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49e4b8cd3fee1bb106194497f850586ad7017b3eb7a7cb06cc0d4f72a2a6a1f`

```dockerfile
```

-	Layers:
	-	`sha256:3587911d537486c602a22b944c9500e0a2dcfbf7f79ee4c0eee1de2d47fa54e6`  
		Last Modified: Thu, 29 Jan 2026 19:41:53 GMT  
		Size: 598.2 KB (598244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f65450ced3a2168128ecbae32b43f6b2e2198dd668a395c42f3f61658efe336`  
		Last Modified: Thu, 29 Jan 2026 19:41:53 GMT  
		Size: 39.6 KB (39626 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:1846fd01ca83b815163cb0dd4726952c19c2a9ee9a77f36a454ce7970e3df469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91079569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f321a9e734ddf8adba0a31b4fc896bde873b31ae3d18363713ac38f21f48497d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:38:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 29 Jan 2026 19:38:53 GMT
ENV GOSU_VERSION=1.19
# Thu, 29 Jan 2026 19:38:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Jan 2026 19:38:53 GMT
ENV LANG=en_US.utf8
# Thu, 29 Jan 2026 19:38:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:38:53 GMT
ENV PG_MAJOR=18
# Thu, 29 Jan 2026 19:38:53 GMT
ENV PG_VERSION=18.1
# Thu, 29 Jan 2026 19:38:53 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 29 Jan 2026 19:38:53 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 29 Jan 2026 19:41:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 29 Jan 2026 19:41:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 29 Jan 2026 19:41:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 29 Jan 2026 19:41:41 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 29 Jan 2026 19:41:41 GMT
VOLUME [/var/lib/postgresql]
# Thu, 29 Jan 2026 19:41:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:41:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 29 Jan 2026 19:41:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:41:41 GMT
STOPSIGNAL SIGINT
# Thu, 29 Jan 2026 19:41:41 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 29 Jan 2026 19:41:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f418299fec09d79b21550bb7bc0f404dc52ff4b8553b43e25fde1a31eb432c`  
		Last Modified: Thu, 29 Jan 2026 19:41:52 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d350ab249dba8fc7fc86f1e43a286b9a2a32752d3e3904d743a85f29ac3435`  
		Last Modified: Thu, 29 Jan 2026 19:41:52 GMT  
		Size: 886.1 KB (886129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b556042fbd2899518cff53ac327b0a3aa3f9334f09b48f491129fb0cdf309d`  
		Last Modified: Thu, 29 Jan 2026 19:41:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24cff9b1c2ea147cadf9495a5ba774569c8c5bdd1f314e82a8503297f9bd872`  
		Last Modified: Thu, 29 Jan 2026 19:41:54 GMT  
		Size: 86.7 MB (86662390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa01001b9a193a0fd12f964a7e90be100ea3f86716548c0f3bc74e992049812`  
		Last Modified: Thu, 29 Jan 2026 19:41:53 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d802d6c03fa51a6b01a8917596b6ad78ecf8a62838bbf9d3072d38a2224582`  
		Last Modified: Thu, 29 Jan 2026 19:41:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a55b00930b25d40cc2f1126c79530671361573b707100e3cfd89ee2b9c31641`  
		Last Modified: Thu, 29 Jan 2026 19:41:53 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68967cab54bcb5dac1b490196f790afb8ea0659ad31a64ebb437929e34c43dd`  
		Last Modified: Thu, 29 Jan 2026 19:41:54 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:79cf14df8022e603b033cb1b4b6ff9f2956739da8763122abff0d1ec0cda5367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e963c8f6292cbe746022ce45008aecbe54bbaa3fbdca85197304fbff0d8585f`

```dockerfile
```

-	Layers:
	-	`sha256:e153e25ebbf950215ffdfcf58424af40e48a83ae100e8beb2c0c2b1069aca9ab`  
		Last Modified: Thu, 29 Jan 2026 19:41:51 GMT  
		Size: 39.6 KB (39556 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:14fef734321abc7e95209a1dac51882ef73a240973af8fc8bf09f707c242f304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86290897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7421712ce02ed7ef0cf64317a650b75e343bbb34d052adacc1271176081dc070`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:40:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 29 Jan 2026 19:40:13 GMT
ENV GOSU_VERSION=1.19
# Thu, 29 Jan 2026 19:40:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Jan 2026 19:40:13 GMT
ENV LANG=en_US.utf8
# Thu, 29 Jan 2026 19:40:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:40:13 GMT
ENV PG_MAJOR=18
# Thu, 29 Jan 2026 19:40:13 GMT
ENV PG_VERSION=18.1
# Thu, 29 Jan 2026 19:40:13 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 29 Jan 2026 19:40:13 GMT
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
# Thu, 29 Jan 2026 19:42:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:42:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 29 Jan 2026 19:42:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:42:59 GMT
STOPSIGNAL SIGINT
# Thu, 29 Jan 2026 19:42:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 29 Jan 2026 19:42:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2715d7a33ae4ace4123967dc77069fece19ac71d95bb39d72dcb6ed19a69a7`  
		Last Modified: Thu, 29 Jan 2026 19:43:10 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1028186cf33c37c3e39b8648ef178e880f359216f16ed504320d1ba866542d`  
		Last Modified: Thu, 29 Jan 2026 19:43:11 GMT  
		Size: 886.1 KB (886132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbf711f19aa49f47de13c16f7a64da058476b2f70f5a3f54cb43cc8d2e6a9e2`  
		Last Modified: Thu, 29 Jan 2026 19:43:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b499b939d86735f3cbb778c1c298e9d527a9dc54f54b639bc1bfee091594f3`  
		Last Modified: Thu, 29 Jan 2026 19:43:13 GMT  
		Size: 82.2 MB (82155109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aee00576d0aafa54c99f9ae7b78bb4c1d38ce75e8e2c7fa5d03dc7ff924590`  
		Last Modified: Thu, 29 Jan 2026 19:43:12 GMT  
		Size: 18.8 KB (18780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778e4c3b843832db76ac022879e4a426693016c9935388fab7f6bb427c2a147e`  
		Last Modified: Thu, 29 Jan 2026 19:43:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d2a83e27d4a8321b0bb2d21486d0024722422bdf0e4cec2cff62730676d448`  
		Last Modified: Thu, 29 Jan 2026 19:43:12 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e02be955361d49300dfc387590e94ee1e62776345acd8cb1c1766c888d7b50a`  
		Last Modified: Thu, 29 Jan 2026 19:43:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:2a3f03d9db9463bb09db1eee2dfd4b432aed72a4f24b138397865ecc4c37139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.0 KB (638043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db7a67a004047175217ff577995f4a53120a1ade342feb64f78e3faa4092a3a`

```dockerfile
```

-	Layers:
	-	`sha256:e551907a4ae2bcfd5f5983188cbd848d2f8067bd2d8403ca053426a0382c9586`  
		Last Modified: Thu, 29 Jan 2026 19:43:11 GMT  
		Size: 598.3 KB (598272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c4b5a2eaf2b5b0eaadca476e9a493a727176c83b37756033ecbcc323a8efefb`  
		Last Modified: Thu, 29 Jan 2026 19:43:10 GMT  
		Size: 39.8 KB (39771 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:dbcfefa8d3fcbbabe46bbadf257d8e453bf5a6ffb02b3b86b34fbcd82f8b2343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107447352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af6b625e7cbf6e059cf3f36051be0a61d10e2a66042fd19cbaf0fcc8272a33c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:39:04 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 29 Jan 2026 19:39:07 GMT
ENV GOSU_VERSION=1.19
# Thu, 29 Jan 2026 19:39:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Jan 2026 19:39:07 GMT
ENV LANG=en_US.utf8
# Thu, 29 Jan 2026 19:39:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:39:07 GMT
ENV PG_MAJOR=18
# Thu, 29 Jan 2026 19:39:07 GMT
ENV PG_VERSION=18.1
# Thu, 29 Jan 2026 19:39:07 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 29 Jan 2026 19:39:07 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 29 Jan 2026 19:41:34 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 29 Jan 2026 19:41:35 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 29 Jan 2026 19:41:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 29 Jan 2026 19:41:35 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 29 Jan 2026 19:41:35 GMT
VOLUME [/var/lib/postgresql]
# Thu, 29 Jan 2026 19:41:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:41:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 29 Jan 2026 19:41:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:41:35 GMT
STOPSIGNAL SIGINT
# Thu, 29 Jan 2026 19:41:35 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 29 Jan 2026 19:41:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b545ba04b20ac8f6f7eda815093fb10fbd68051d8b047234ceaf1f87b9a069`  
		Last Modified: Thu, 29 Jan 2026 19:41:49 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d8a6362c40b69e4aac1120d15e073e2b5eaa5b3214059d3e148a4e288a06ee`  
		Last Modified: Thu, 29 Jan 2026 19:41:49 GMT  
		Size: 873.5 KB (873482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe7e1fcd2375e4efa0540871368a11cdf3e272fe393d6f72395f6129282d4b2`  
		Last Modified: Thu, 29 Jan 2026 19:41:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f49690d184dcd1ed6537c8d5c3a18b910d8c1db34feb061a1f91656d1388b7`  
		Last Modified: Thu, 29 Jan 2026 19:41:52 GMT  
		Size: 102.4 MB (102408340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b75f071827bb7ba7e57b9bb0a9951471101868bcc4f46d9b484bd94e4e6d95a`  
		Last Modified: Thu, 29 Jan 2026 19:41:51 GMT  
		Size: 18.8 KB (18776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f3a6e20f1d3d558d0459ea64c3ad14ab9cec915f5900d0120dda4611706ccc`  
		Last Modified: Thu, 29 Jan 2026 19:41:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc94dcc4f7ab5a5f0f5d63a6ce93c9d89b6b3991ebf415b4520c3623ec24a60e`  
		Last Modified: Thu, 29 Jan 2026 19:41:51 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff145f302a11d7110c757896290b363db48e5fa8f4e2e4dc946563893fa442b`  
		Last Modified: Thu, 29 Jan 2026 19:41:52 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:ea144c4b60758055fc6830e76e260638901a67b5605975d21185d90b034c3668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.1 KB (638096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d42bc0422625b8d5e64391759947d4cc554d340dcbdc62c697d06423f121e0`

```dockerfile
```

-	Layers:
	-	`sha256:19212c114c95b6650d774139e176a6cee5943104493f722430b7ebe0868323af`  
		Last Modified: Thu, 29 Jan 2026 19:41:49 GMT  
		Size: 598.3 KB (598288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39a47327e4149fb9bbec46c17e8d0a3f23949d3d9f9f0c9a29e4e29cd35ef57e`  
		Last Modified: Thu, 29 Jan 2026 19:41:49 GMT  
		Size: 39.8 KB (39808 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:06efe1556a1f303908a9368aa5e920cbeca45bc47723a99761df25c58690c59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117872339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf48b0d438ead3848910d593195727f1fa87bcb9df5540b00f40c1e4fe42e3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:39:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 29 Jan 2026 19:39:16 GMT
ENV GOSU_VERSION=1.19
# Thu, 29 Jan 2026 19:39:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Jan 2026 19:39:16 GMT
ENV LANG=en_US.utf8
# Thu, 29 Jan 2026 19:39:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:39:16 GMT
ENV PG_MAJOR=18
# Thu, 29 Jan 2026 19:39:16 GMT
ENV PG_VERSION=18.1
# Thu, 29 Jan 2026 19:39:16 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 29 Jan 2026 19:39:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 29 Jan 2026 19:41:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 29 Jan 2026 19:41:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 29 Jan 2026 19:41:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 29 Jan 2026 19:41:52 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 29 Jan 2026 19:41:52 GMT
VOLUME [/var/lib/postgresql]
# Thu, 29 Jan 2026 19:41:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:41:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 29 Jan 2026 19:41:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:41:52 GMT
STOPSIGNAL SIGINT
# Thu, 29 Jan 2026 19:41:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 29 Jan 2026 19:41:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67530fe5df1ba6184c7dc7c4053e632a236753aaf9bb23b8993b6a01900c6ec`  
		Last Modified: Thu, 29 Jan 2026 19:42:08 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb51f9cbfd66abedbea1906097514970fc213eb22cae3dfab5cf5e10012e3fa6`  
		Last Modified: Thu, 29 Jan 2026 19:42:08 GMT  
		Size: 890.6 KB (890638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e428f4b8a671d45d00bfbc299da340bb7313159e64de865459ff2bb152eb4a`  
		Last Modified: Thu, 29 Jan 2026 19:42:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77832bc52b6428ed0e62613a7fdb8ddb90e0b41a4fa75ebdf0cacaa125c964e6`  
		Last Modified: Thu, 29 Jan 2026 19:42:10 GMT  
		Size: 113.3 MB (113334962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4c4845ac4231260db4004dbc2544b7b7556ea158bf20c4e3b9d3b35b58683f`  
		Last Modified: Thu, 29 Jan 2026 19:42:09 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae505002f4d5cdee6f673bbff233e3de4931e917a95176a2649cb4a757f1703`  
		Last Modified: Thu, 29 Jan 2026 19:42:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d51b4a71ac899413929f4d1e3f856bbcf45faa2284cd10ddb8e62f05c0face`  
		Last Modified: Thu, 29 Jan 2026 19:42:09 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95494bdbf0623f8b00667b7ff338a92391eceb9e0c5faf6689ffec7a6039934a`  
		Last Modified: Thu, 29 Jan 2026 19:42:10 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:27dc5b7ee15f8bb83678a74ac91f444db89ed2e87a96c32c6beb6ee6b09d63d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e8988361fee416e3ad1ccdebc0ca767121e0e58e2df15aeeae52a9f8a62bf6`

```dockerfile
```

-	Layers:
	-	`sha256:24c24b0de4af01b6a7cbb3aeb170c09673c90c3aaa2dac88b43d524dfc56b843`  
		Last Modified: Thu, 29 Jan 2026 19:42:08 GMT  
		Size: 598.2 KB (598224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c1041fb238616ed48f33ac2de913ff6d375c8b2c449be395ff56935fb5baff0`  
		Last Modified: Thu, 29 Jan 2026 19:42:07 GMT  
		Size: 39.6 KB (39587 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:cda70a06aaa1b6d1b23ed3f0e2f603f46a2a4b3b698842aa43dc38e4ccbdf804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95427231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b4d79111832a7f3f53cd6c45932ffb354964b3e4633705241ca0a04f9e8653`
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
# Wed, 28 Jan 2026 03:33:21 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 03:33:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 03:33:22 GMT
ENV PG_MAJOR=18
# Wed, 28 Jan 2026 03:33:22 GMT
ENV PG_VERSION=18.1
# Wed, 28 Jan 2026 03:33:22 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Wed, 28 Jan 2026 03:33:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 03:36:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 03:36:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 03:36:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 03:36:02 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 28 Jan 2026 03:36:02 GMT
VOLUME [/var/lib/postgresql]
# Thu, 29 Jan 2026 19:53:40 GMT
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
	-	`sha256:5804c3d9b1f7ab711750ef41dbdef64801760ee13d225f03da0373cbaf9601a9`  
		Last Modified: Wed, 28 Jan 2026 03:36:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7f19b5c8f7f993d96f4b0c740348457f2847430d886d7dfac82420fca3c64f`  
		Last Modified: Wed, 28 Jan 2026 03:36:42 GMT  
		Size: 90.8 MB (90787877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567d31441424026b80e99b44fa1cc6d1401cc5639d23b0370af08740464386d0`  
		Last Modified: Wed, 28 Jan 2026 03:36:41 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5744de5479aa8d55dbcac1dbee7af4adf73c9e7ebff2a51df8660649c0c803`  
		Last Modified: Wed, 28 Jan 2026 03:36:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70a9ffc2455edf4e6e2b2df8560cace4fb0d41afe2f962d3481a43f9ba7ab6b`  
		Last Modified: Thu, 29 Jan 2026 19:53:57 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7152d9f9ce66a506cd8c4cd55a109e75d8b0ea4f1a82d4a12a680c6411f52d9e`  
		Last Modified: Thu, 29 Jan 2026 19:53:57 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:5fd97a4aea44cec1187c6421ce1363bb372a7b9edd769c25cdcea766569bdfec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.3 KB (634330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7ca0000eb1f29d4c1d251f2bc92d51684fa0cd412f4ed519472c8a531e00f9`

```dockerfile
```

-	Layers:
	-	`sha256:f37bd960c6984e43c6605d24893f891c6eae1f2b7cefe541e253d4310db80b94`  
		Last Modified: Thu, 29 Jan 2026 19:53:57 GMT  
		Size: 594.7 KB (594659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a6a1aa6a4d9c46815369929fef0cdc6365ec912c550343ae350faa78a61864b`  
		Last Modified: Thu, 29 Jan 2026 19:53:57 GMT  
		Size: 39.7 KB (39671 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:514e27024c57a27368a884b66a7a30597e89554f97764410eee0e9e2ec4eee0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111692269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dce962a1dc1b4035b18226b6e5240e2b33d382a9c1cef733a73b38a99e01534`
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
# Thu, 29 Jan 2026 10:55:38 GMT
ENV LANG=en_US.utf8
# Thu, 29 Jan 2026 10:55:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 10:55:38 GMT
ENV PG_MAJOR=18
# Thu, 29 Jan 2026 10:55:38 GMT
ENV PG_VERSION=18.1
# Thu, 29 Jan 2026 10:55:38 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 29 Jan 2026 10:55:38 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sun, 01 Feb 2026 00:55:29 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sun, 01 Feb 2026 00:55:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sun, 01 Feb 2026 00:55:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sun, 01 Feb 2026 00:55:30 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Sun, 01 Feb 2026 00:55:30 GMT
VOLUME [/var/lib/postgresql]
# Sun, 01 Feb 2026 00:55:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sun, 01 Feb 2026 00:55:31 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sun, 01 Feb 2026 00:55:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 01 Feb 2026 00:55:31 GMT
STOPSIGNAL SIGINT
# Sun, 01 Feb 2026 00:55:31 GMT
EXPOSE map[5432/tcp:{}]
# Sun, 01 Feb 2026 00:55:31 GMT
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
	-	`sha256:776be1c21034041fe1cfae3c3ad99f497aa11c5d675fe919eec69c55932c26e0`  
		Last Modified: Thu, 29 Jan 2026 11:50:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6978219b293324d8e66d933199bfbc47b7ec7b47d8a670655307276b8a80110`  
		Last Modified: Sun, 01 Feb 2026 00:58:40 GMT  
		Size: 107.3 MB (107282193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a58cc6b1aac75001c712e73b568b26850e673f2e9ec8e423c06484e9f19be6`  
		Last Modified: Sun, 01 Feb 2026 00:58:23 GMT  
		Size: 18.8 KB (18783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2b4cccffe1a6a87c36b704f209b990ee436f44946d3525a6cd15f3bd71d33e`  
		Last Modified: Sun, 01 Feb 2026 00:58:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cf0ad893c29e5204efe5c98c3d2068b8e307a45adb349b4dc26c53234530d6`  
		Last Modified: Sun, 01 Feb 2026 00:58:23 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b16b2e53b396c90111e6a2501a7110a6920235077b33f2f170ea05e67de9e7`  
		Last Modified: Sun, 01 Feb 2026 00:58:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:c35fa00bb3e76c7335031745c6e100aa32d53a47e03e35b02808d8e0c6ab6556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 KB (635993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc793be9632c77ca9ad5ac722bde53d5ad83bef96a0c7b78632073e7bf6b48d9`

```dockerfile
```

-	Layers:
	-	`sha256:4c8d99220b99807d1816c626bee8d186dfada4aabd2e65beefdd64273c1b0c4b`  
		Last Modified: Sun, 01 Feb 2026 00:58:23 GMT  
		Size: 596.3 KB (596317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0dfefa81937e3fa8b6ddac2b51ee6d275db2c8d900e21acd50454f444b2d27e`  
		Last Modified: Sun, 01 Feb 2026 00:58:23 GMT  
		Size: 39.7 KB (39676 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:c1b7905508f17d9f6a211b2be2a9ac719ee265fe3706d14a508d62ef9a53eff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120282464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea88bb8267d70ba4204bdcf3d5d93726b9c5183752f8f0ca847b0de65db9d74`
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
# Wed, 28 Jan 2026 02:50:49 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:50:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:50:49 GMT
ENV PG_MAJOR=18
# Wed, 28 Jan 2026 02:50:49 GMT
ENV PG_VERSION=18.1
# Wed, 28 Jan 2026 02:50:49 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Wed, 28 Jan 2026 02:50:49 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:53:54 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:53:54 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:53:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:53:54 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 28 Jan 2026 02:53:54 GMT
VOLUME [/var/lib/postgresql]
# Thu, 29 Jan 2026 19:40:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:40:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 29 Jan 2026 19:40:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:40:17 GMT
STOPSIGNAL SIGINT
# Thu, 29 Jan 2026 19:40:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 29 Jan 2026 19:40:17 GMT
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
	-	`sha256:e772f7553b15ca1aea28c1bc9859433101e91c56a88a99f8aa1c383936874efe`  
		Last Modified: Wed, 28 Jan 2026 02:54:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b7c2efc7c4f5f00966de31764f26c850dc2d16015674c8e284def9b2cff66e`  
		Last Modified: Wed, 28 Jan 2026 02:54:21 GMT  
		Size: 115.7 MB (115711595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce97b897c6c8bdc8a0418b196f6474375a30af10fa16a09ddc33cc43b4e3d0f`  
		Last Modified: Wed, 28 Jan 2026 02:54:20 GMT  
		Size: 18.8 KB (18779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bcafca0601708b66283e4ac6281c3ea681df9f4ac3d12b816973ea02ad65d0`  
		Last Modified: Wed, 28 Jan 2026 02:54:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f300c1eccccfe9a5cfdad4bed59af432cb7147f5c97b74d52a93b56bfbb947`  
		Last Modified: Thu, 29 Jan 2026 19:40:31 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fddfba94c18ae82fc009bde9e71d8440c92d291325fe641ac2600dabc432b6`  
		Last Modified: Thu, 29 Jan 2026 19:40:31 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:b8a038f26be9e2dfab392058b83046f7aa3e9a1f123a17c756e4c05c1a6fe19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.9 KB (635919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6848400a6152d571d7e7d610762be2abdd2bae84e5fdd4aba3df87595c5076`

```dockerfile
```

-	Layers:
	-	`sha256:e7ce4d54a0d2f1d119a7e7ee857675f64ab05218b595c701d63511697d585f78`  
		Last Modified: Thu, 29 Jan 2026 19:40:31 GMT  
		Size: 596.3 KB (596293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6128cfd3a8436586a335817ff5019947a3fd4fa2961b76de9f53ff21048d424b`  
		Last Modified: Thu, 29 Jan 2026 19:40:31 GMT  
		Size: 39.6 KB (39626 bytes)  
		MIME: application/vnd.in-toto+json
