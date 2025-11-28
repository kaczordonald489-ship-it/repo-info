## `postgres:15-alpine3.21`

```console
$ docker pull postgres@sha256:55898ede75a212f5294646bb20ed2a6e530c932b020f3ddfd419468e38967ea3
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

### `postgres:15-alpine3.21` - linux; amd64

```console
$ docker pull postgres@sha256:d7a758b36be78ed6c6c1bca661d663d19ab4eca1ef75f3dddfec2b6f58a20c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108675057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7333da58aafd74800bf62f25767a5f9ee800dfb30d434d524810470ef27fa46e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:20:11 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:20:13 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:20:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:20:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:20:14 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:20:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:20:14 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 19:20:14 GMT
ENV PG_VERSION=15.15
# Fri, 14 Nov 2025 19:20:14 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Fri, 14 Nov 2025 19:20:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:22:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:22:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:22:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:22:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:22:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:22:23 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:22:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:22:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:22:23 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:22:23 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:22:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b67cf23a09d11122e048cf03a764332afb5b1f89fd2a13ef15f359ba5eceb97`  
		Last Modified: Fri, 14 Nov 2025 19:22:49 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2536710482cb1e2157d94041975726c05567ed463c8a7fad275ae50628ea1e31`  
		Last Modified: Fri, 14 Nov 2025 19:22:49 GMT  
		Size: 918.3 KB (918259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2219268af863f968fd3a9c31f10b43ada15f4e2157a0a59c77cf4d97222bd44`  
		Last Modified: Fri, 14 Nov 2025 19:22:49 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f6e80fc025f8cc72d8ff3c87e9be0dcfeec45c39c1d23792456d0cb36650ea`  
		Last Modified: Fri, 14 Nov 2025 19:22:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6282c9f10a11dd5757994caa41ae780d4a8ca142c271be999b1d48040c28152`  
		Last Modified: Fri, 14 Nov 2025 19:23:05 GMT  
		Size: 104.1 MB (104097202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690bf18295692aec43a289cb95a579a703dced5b1b7acae1f2177f32dd3cc4fc`  
		Last Modified: Fri, 14 Nov 2025 19:22:49 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402a90669f9836cef85af426cee7e3f5f28e960e95ef72b1e57de257068bdd3c`  
		Last Modified: Fri, 14 Nov 2025 19:22:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea05375fdd0c7019a183897ca67047512f2af14ccf1a999ed1bc45a520065462`  
		Last Modified: Fri, 14 Nov 2025 19:22:50 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acafa5ce427eb89ef9ca2f91c81c9165993eea9515a7834fffa888ff7f04e81`  
		Last Modified: Fri, 14 Nov 2025 19:22:49 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0db6475905e2c3b8a1382531d6baf315c66b706d7ed91c4679ee78b962c3f8`  
		Last Modified: Fri, 14 Nov 2025 19:22:49 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:f1899c7732c7fe11c7660f03cfac3ba7335cee2911e82b9b777506b26c9e3a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.5 KB (642460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e7f8a9bc6f5beb7b9e07b6c67e6f05dfd3c2e5fac55c532caa8f30b236111f`

```dockerfile
```

-	Layers:
	-	`sha256:c9465456a4f1208821456e52870cbe4acb1e17fe9b34ab8ee9ab3fe445a65702`  
		Last Modified: Fri, 14 Nov 2025 21:11:08 GMT  
		Size: 598.7 KB (598692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b003edf29aa6306b4121378b07a2e3a23e9d5a9f6732d863e102d62d7941e4eb`  
		Last Modified: Fri, 14 Nov 2025 21:11:09 GMT  
		Size: 43.8 KB (43768 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; arm variant v6

```console
$ docker pull postgres@sha256:58bedd984a961fe8845b78a1fe6a609522ab78f29bd8637e5745dea64f3bee45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88303488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2186537497b2dc481343dd008f9b5da0a41e9c00124af0823e7faf3905580a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:41:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:41:15 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:41:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:41:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:41:15 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:41:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:41:15 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 19:41:15 GMT
ENV PG_VERSION=15.15
# Fri, 14 Nov 2025 19:41:15 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Fri, 14 Nov 2025 19:41:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:47:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:47:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:47:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:47:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:47:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:47:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:47:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:47:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:47:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:47:15 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:47:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:47:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88c84d325da520474d103033c87f694e69050d62f1a02bea7656fa0002984c6`  
		Last Modified: Fri, 14 Nov 2025 19:44:27 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f7a99e28a79dfe49ef4b92f7a1ec66b05e59a7a20d9d92eb4822e112616d26`  
		Last Modified: Fri, 14 Nov 2025 19:44:27 GMT  
		Size: 886.1 KB (886108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c40b4df8fe1294bbb3cfdbbbf22c671b644a914e9cc54de4295fc6af8195f8`  
		Last Modified: Fri, 14 Nov 2025 19:44:27 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6f2dd1575e16e8ea0f777e3bac7ed8b916f7f32793283d3b3a351b5c03c70f`  
		Last Modified: Fri, 14 Nov 2025 19:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55751519b55f19e0b250f264ae2a0d2a50114b269f8ab7228e2a4053d667984`  
		Last Modified: Fri, 14 Nov 2025 19:47:40 GMT  
		Size: 84.0 MB (84034886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e26881ef105f4e6d8e9acdef05e8441c5b1235b619bb64e994beb532098129`  
		Last Modified: Fri, 14 Nov 2025 19:47:34 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b6a1e1ca0654ec7a27def94897d9f484de04e3660413ffbccebe40d45e044b`  
		Last Modified: Fri, 14 Nov 2025 19:47:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a05379070fc6aa6bab7796bfab4b31028453213ed9e128ed5094cc0b431312a`  
		Last Modified: Fri, 14 Nov 2025 19:47:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba8e49534624c2dab59711eceb4089f716cbe374cf41f6425e0f1527f9712e9`  
		Last Modified: Fri, 14 Nov 2025 19:47:34 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5756e8e130999d6921d00d329e569c56cbb643a36c59af44e0dc4ad69a6f3978`  
		Last Modified: Fri, 14 Nov 2025 19:47:34 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:55034b3a86a18101e1ea1ea3c317292c7ebeca05ada93447196b21ca65ebdba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 KB (43714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0420de408bde30981fa58325f96cc8fc1806383c3f80f1cf3854a4b259cee3e8`

```dockerfile
```

-	Layers:
	-	`sha256:d130f65752be4dce8c2681478246fb22577e6f3949a185379f5f8c5353a0844e`  
		Last Modified: Fri, 14 Nov 2025 21:11:12 GMT  
		Size: 43.7 KB (43714 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; arm variant v7

```console
$ docker pull postgres@sha256:dbd1b13316a896284b0fa66dc27444d27c13f107c72e201e530b9c6acad6be45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83541289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5272e65539cd64a5f2b48cbbc2336f6106a9c8e7942a3a04ca3e2d1e859df508`
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
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:16:45 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:16:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:16:45 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 19:16:45 GMT
ENV PG_VERSION=15.15
# Fri, 14 Nov 2025 19:16:45 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Fri, 14 Nov 2025 19:16:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:19:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:19:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:19:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:19:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:19:25 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:19:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:19:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:19:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:19:26 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:19:26 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:19:26 GMT
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
	-	`sha256:00d092a014d9ce1ac0334515ab8178923bbee2a78891a48c7f96e7fbc4e463b0`  
		Last Modified: Fri, 14 Nov 2025 19:20:06 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9c52eef7238adfc5dba30558ba02604cdb756368194350e8358ac10e021232`  
		Last Modified: Fri, 14 Nov 2025 19:20:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9722100928e517fe0555a2d22e02fc8e70bc4e7f98f61640eb42d7725cd1aa`  
		Last Modified: Fri, 14 Nov 2025 19:20:17 GMT  
		Size: 79.5 MB (79539544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fdf4de87dc79d7c868248a57bee8b47ba0fa23ac2ba4041addf8eb4e024682`  
		Last Modified: Fri, 14 Nov 2025 19:20:06 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1cd30ded95ea3bf5ca9b44dd06f4b7ae9f67282a55b7960c03799eedcd764d`  
		Last Modified: Fri, 14 Nov 2025 19:20:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fc0fd548abf642dfcb45a56219d8455a6ce8221d7737a64548f87ec6dc951e`  
		Last Modified: Fri, 14 Nov 2025 19:20:06 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a69fbf4a0b151e399a1627d4106a2671a5b08bea177170fd15129ec2eb7eba0`  
		Last Modified: Fri, 14 Nov 2025 19:20:06 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa10f3599d780eecf3f22fbda910dc041a97e5c2149892793d6efc9717058b0`  
		Last Modified: Fri, 14 Nov 2025 19:20:06 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:728ff75ed1758411b95f604d8e06f3065afb083ef8fdb810a48d99822b0ac986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.6 KB (642642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5833b79e16f9308cd55b0823a1c8069d0fbce3f2972bffc0dee141270d1a1e`

```dockerfile
```

-	Layers:
	-	`sha256:9a00a79863a161638526f2df441422b0f0a2bc00087fa1760c35ee25e5c15050`  
		Last Modified: Fri, 14 Nov 2025 21:11:15 GMT  
		Size: 598.7 KB (598712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:835dda642f0bb4f6482aa7b6fcc3a46fc975b80fafef436e850e535d1d3c6510`  
		Last Modified: Fri, 14 Nov 2025 21:11:16 GMT  
		Size: 43.9 KB (43930 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:d43f6c5cf1a3414b80cfd09c5ea2166dcde6f15a09dea2a203ebd24aee83cecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104603936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8306b59073c12e3c8f9f5aa32897f9ff2b0e16aeb18b4671f4d72892957c7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:19:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:19:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:19:58 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:19:58 GMT
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
# Fri, 14 Nov 2025 19:22:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:22:22 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:22:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:22:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:22:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:22:23 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:22:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:22:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:22:23 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:22:23 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:22:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb10d513d8437e907263b1ce5af9ce56abe8a4a1e4786fd01b41cf60749d519`  
		Last Modified: Fri, 14 Nov 2025 19:22:46 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1343f3859270b66fdc924118ac46b8962a363cf6ae9ffa7fdaa3e0bc79e8b06b`  
		Last Modified: Fri, 14 Nov 2025 19:22:46 GMT  
		Size: 873.5 KB (873460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bafbf79eade8dd6e9b1b5b7bc982b4390baa7b854f2282c72089f3c5d1c4e2a`  
		Last Modified: Fri, 14 Nov 2025 19:22:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eecd23a9938b66a244e208352801274f082d464324783da5908582d3dd41c2e`  
		Last Modified: Fri, 14 Nov 2025 19:22:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a6fdb7e2d635de06e8864da22cd2d196450434398d27d011665c6d781ab063`  
		Last Modified: Fri, 14 Nov 2025 19:22:55 GMT  
		Size: 99.7 MB (99721096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6719ccb94e175175984215f7f84cba2bcf6c7b6f0df11c515fa4944b8403e294`  
		Last Modified: Fri, 14 Nov 2025 19:22:46 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402a90669f9836cef85af426cee7e3f5f28e960e95ef72b1e57de257068bdd3c`  
		Last Modified: Fri, 14 Nov 2025 19:22:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc8846a277ff9e09c6f72d52597d53768f6f01c4670cd9de76568356c85289`  
		Last Modified: Fri, 14 Nov 2025 19:22:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a2eabb2a0d70894a3011bb6fcca50c7fe4829f5f03d736b1f97568168349a8`  
		Last Modified: Fri, 14 Nov 2025 19:22:46 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e2f8585daaecb09d6e3be5c2a569e7851616570b75406007b33bc7649ca4d7`  
		Last Modified: Fri, 14 Nov 2025 19:22:46 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:d340d4df778068b88f4a0e4ef657f86ecfc8726b871e999199e54832f5f67919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.7 KB (642686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf467b838680aa49a30b68d564297f41b8a7b5569be692a243c6486d62728ab8`

```dockerfile
```

-	Layers:
	-	`sha256:6d51a4c1c0a1052866979f33f2e163b689a19cabe75b7b2fa294182c09f986d0`  
		Last Modified: Fri, 14 Nov 2025 21:11:19 GMT  
		Size: 598.7 KB (598724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea4538186823c098101bcc0f5f887a15f30fc14996bb01d39a1ae11b86e9a89d`  
		Last Modified: Fri, 14 Nov 2025 21:11:20 GMT  
		Size: 44.0 KB (43962 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; 386

```console
$ docker pull postgres@sha256:324fd3480d786df4c68ac12ad0321d1f8f95329335c435fddd20a99ef5abd5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114849624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234247081763bd4fde63c173859973130154f70896e872fe2ff74dcb0defde3b`
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
# Fri, 14 Nov 2025 19:22:33 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:22:33 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:22:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:22:33 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 19:22:33 GMT
ENV PG_VERSION=15.15
# Fri, 14 Nov 2025 19:22:33 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Fri, 14 Nov 2025 19:22:33 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:27:51 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:27:51 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:27:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:27:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:27:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:27:51 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:27:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:27:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:27:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:27:51 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:27:51 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:27:51 GMT
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
	-	`sha256:1d5838c73e955b3f7f0d81f52f7464313b1d3fde53412910d0026cf09fd5c57c`  
		Last Modified: Fri, 14 Nov 2025 19:25:25 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ff14be81a78a4466d6d50561ecc530439dd03eb97d22144f81b751843aa238`  
		Last Modified: Fri, 14 Nov 2025 19:25:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8254f4740a2cd666ece80822b0897cc40d105e740278e54e0897b5c1a875fb44`  
		Last Modified: Fri, 14 Nov 2025 19:28:37 GMT  
		Size: 110.5 MB (110477280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30b45754d223ee107a188e27a2cc28af377a895cdd557107ce2f7095323de71`  
		Last Modified: Fri, 14 Nov 2025 19:28:15 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5b17db6152b64a18063aa34729852abab78a1a23bc09f215faeca6eb60c769`  
		Last Modified: Fri, 14 Nov 2025 19:28:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dd1df08d62ef45b74592eafa77387b83ddb8040947fdaa9c51c4f2c72794c7`  
		Last Modified: Fri, 14 Nov 2025 19:28:15 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a41ca9d8172fde7a46d38e611dabeda9af76242914e8449e2cf80d3cfef528c`  
		Last Modified: Fri, 14 Nov 2025 19:28:15 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483028496c6201c421a01040dee6100ec66f02cbce65bb0b9f34d2767d7a4c58`  
		Last Modified: Fri, 14 Nov 2025 19:28:15 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:ae4173cdd127e10164d343cbf62b5a15dd028b77e411552e5edbd49aafc73c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be5f9c1e5369a5016c004be89eb52aac5758a59ea109a30cfaba34826b95193`

```dockerfile
```

-	Layers:
	-	`sha256:1704ab9158c9e33c28075bae9d21426fa022486e99dab924c107c8d3b04e2e38`  
		Last Modified: Fri, 14 Nov 2025 21:11:24 GMT  
		Size: 598.7 KB (598677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b66e885252a7e99e0fc6525fb3006904f41a08041ff98c5dfbbe27a10f4c7290`  
		Last Modified: Fri, 14 Nov 2025 21:11:25 GMT  
		Size: 43.7 KB (43729 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; ppc64le

```console
$ docker pull postgres@sha256:3759803eb5a94e613fef5376d614813220ff44fbb2af76f7711151902dd4de2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92438087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91782b8c44fe25f577a19d7a312d4fb0dc74a0ac98a32ccce508a9b2fffa235`
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
# Thu, 13 Nov 2025 21:33:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Nov 2025 21:33:13 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:33:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:33:14 GMT
ENV PG_MAJOR=15
# Thu, 13 Nov 2025 21:33:14 GMT
ENV PG_VERSION=15.15
# Thu, 13 Nov 2025 21:33:14 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Thu, 13 Nov 2025 21:33:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Nov 2025 21:45:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:45:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:45:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:45:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:45:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:45:33 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:36:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:36:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:36:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:36:06 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:36:06 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:36:06 GMT
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
	-	`sha256:6354621062687ab445d1a1e68d2fa4b5437beed9fe9ded82634dac7e74af21c9`  
		Last Modified: Thu, 13 Nov 2025 21:36:42 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee678e58e417a0c54a35cfef17e12c948f192ef6ac4aea4ac6bf2f23edad421e`  
		Last Modified: Thu, 13 Nov 2025 21:36:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2101700dd60a10cdf5f85ad3e780483d18bdccd55e10bc7d61e2a73d69f0dc`  
		Last Modified: Thu, 13 Nov 2025 21:46:21 GMT  
		Size: 88.0 MB (87967952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab720f41efaad3a33f4f641c43e7d04ff392dffa14cb0697b3b2026206243f8a`  
		Last Modified: Thu, 13 Nov 2025 21:46:14 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7222c2f54df2bbd2814b37403315afd16c031cd2f714820a9a71a2ede0477a`  
		Last Modified: Thu, 13 Nov 2025 21:46:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1b17e48024d3d92c178b496fad1e28f35d34e61008f59e3858e8fc2b395a15`  
		Last Modified: Thu, 13 Nov 2025 21:46:13 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9032fc0496f1f2a884608a7d301421d5836885fa6fe667ca237b75ecde643f5`  
		Last Modified: Fri, 14 Nov 2025 19:36:37 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54f8dfc37c65f7ac1e5b760141668771f843984700b0c6a4adef8560a23492a`  
		Last Modified: Fri, 14 Nov 2025 19:36:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:f8e959c3f1893d38719b790499165613cba7d4b5c1b006e084ea8675a0d428be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.9 KB (638911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5937b8df3a9b0f2ff979939b8d25bbffe93df7e9cfef522c2036caf159abc297`

```dockerfile
```

-	Layers:
	-	`sha256:7fc9ac4d43086f69e01da7bd1a4e3ccb313461797bc20d9278351b9badb30faa`  
		Last Modified: Fri, 14 Nov 2025 21:11:28 GMT  
		Size: 595.1 KB (595101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d41b67e62e45869417cacf29c7c42eb4b1e1b9068e95463e2e83e7b799d030`  
		Last Modified: Fri, 14 Nov 2025 21:11:29 GMT  
		Size: 43.8 KB (43810 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; riscv64

```console
$ docker pull postgres@sha256:7e17adcb5728337ea5c85c6cf1777078c1f88058139e2675f55cd640655510f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108635265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38aba7ba6bb3b72c14250e4ccb7c73ce243ba31733c5c093c1557c09342789b`
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
# Fri, 14 Nov 2025 08:35:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 08:35:12 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 08:35:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 08:35:13 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 08:35:13 GMT
ENV PG_VERSION=15.15
# Fri, 14 Nov 2025 08:35:13 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Fri, 14 Nov 2025 08:35:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 11:13:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 11:13:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 11:14:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 11:14:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 11:14:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 11:14:00 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 15 Nov 2025 09:53:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 15 Nov 2025 09:53:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 15 Nov 2025 09:53:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Nov 2025 09:53:17 GMT
STOPSIGNAL SIGINT
# Sat, 15 Nov 2025 09:53:17 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 15 Nov 2025 09:53:17 GMT
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
	-	`sha256:65f16dcdfc593a6ede812ba872b76211eda899dafe6787c3347333bf6bed7398`  
		Last Modified: Fri, 14 Nov 2025 09:28:04 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fc9af37df3a694ad3b881fec9477de7821d233e689259b340a0c866d571ba6`  
		Last Modified: Fri, 14 Nov 2025 09:28:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4943fca7bcf9e2efc6e10d530c63c037f16fd4f30f4f0b26d544a1f9f3421b04`  
		Last Modified: Fri, 14 Nov 2025 11:17:22 GMT  
		Size: 104.4 MB (104400621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724a8d0a2e302da43473a13b43092e26c97b460c56f8f23e5caecbbee5e90460`  
		Last Modified: Fri, 14 Nov 2025 11:17:12 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e257424ca181a110852a6ccd374dc4e10cb1cf7504179156380407d09421aa0f`  
		Last Modified: Fri, 14 Nov 2025 11:17:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46807e91966d37cb4b5d1f86dceaa1014ae127877e88b90fa901d7505b3e09ea`  
		Last Modified: Fri, 14 Nov 2025 11:17:12 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5036d334de822e9de640f7fc0a4f27e9681229f1bfa87794391ca461a6dec22b`  
		Last Modified: Sat, 15 Nov 2025 09:54:35 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd29d67db6504635e6f441f0b365ac3c85d7bd407e2057458dbfbaf28338d3ba`  
		Last Modified: Sat, 15 Nov 2025 09:54:35 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:0303339a1a513748253ce5f1d58d4f23655856fe0c70c29f4accc643476d9431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.6 KB (640575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f422db74d2c5d6719d20094ae67afab122e24441dede222d84cbd435dbab74`

```dockerfile
```

-	Layers:
	-	`sha256:3a34e634ea503cc2e5433edfd4c65d398bc174edaa0ab4bb3fdd9ffa58cd8a97`  
		Last Modified: Sat, 15 Nov 2025 23:43:08 GMT  
		Size: 596.8 KB (596759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d625b179cf898f9fd1bd85550f58eeea4f0ad566ea341a009c9ba608d47b5703`  
		Last Modified: Sat, 15 Nov 2025 23:43:09 GMT  
		Size: 43.8 KB (43816 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; s390x

```console
$ docker pull postgres@sha256:3b6be8bcca1b3e2d5ae20b80c4e821ed8c99f5449c0cb460f4979c73fb062afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117285076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a08819e16439de50405a125c6fc2b160f18a55a3e736583a876076dd226e14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 01:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 01:09:46 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 01:09:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:35:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:35:47 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:35:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:35:47 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 19:35:47 GMT
ENV PG_VERSION=15.15
# Fri, 14 Nov 2025 19:35:47 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Fri, 14 Nov 2025 19:35:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:38:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:38:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:38:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:38:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:38:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:38:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:38:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:38:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:38:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:38:40 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:38:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:38:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d682ff10a73d68a38411275dff8e0446ed9f3b97e8a40a39cac409daf208a2ce`  
		Last Modified: Fri, 14 Nov 2025 01:13:19 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20fecfb0177cc1e995dbf553731e3ba685902f57771b3f42cbd88b34c24b4c5`  
		Last Modified: Fri, 14 Nov 2025 01:13:19 GMT  
		Size: 894.4 KB (894396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5c63a02e3631301ebf6887e0077c19f285031e03cf88fc3e81defb3b4ed3db`  
		Last Modified: Fri, 14 Nov 2025 19:39:12 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5931848d33545ba3e3ef2ea291562012134fba875ed97aee883b1dfc2efccd`  
		Last Modified: Fri, 14 Nov 2025 19:39:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7a94387f133338d8615d4fc095fff59e0ef4a9923d6e8ec38c6c9c49585d47`  
		Last Modified: Fri, 14 Nov 2025 19:39:26 GMT  
		Size: 112.9 MB (112907232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef714f16044ab38f606844cea125d415d8ff4f2a8eea75a80c96a0acbb07af6`  
		Last Modified: Fri, 14 Nov 2025 19:39:12 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f48568d9655f6e8fd8100c5bef547e4b75385749f6439bb742ff5ce1d6abd9`  
		Last Modified: Fri, 14 Nov 2025 19:39:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aec208dad6a61849af6eaa27afd91170f76dee4d7922d2fda13db152e08062`  
		Last Modified: Fri, 14 Nov 2025 19:39:12 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f102a66df5cef103248ba0cd6b891802e1cfe646cbebf4a821b1a0a811b05504`  
		Last Modified: Fri, 14 Nov 2025 19:39:12 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd0a56d0bd4dc082519e002f2abd958f415bfeed47ffed8b4284a89710008a8`  
		Last Modified: Fri, 14 Nov 2025 19:39:12 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:946c6bfaddc15b1b24076cfca95c62988522651ac99b8270885c69cd9b839b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.5 KB (640509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e492f8bb50af51c93227e704778affb4e249d32769b6cda0fc32000bfd5b92c9`

```dockerfile
```

-	Layers:
	-	`sha256:1257a2f0cc66ab0888584c57a521b5f3f6bd2e562958ffbc0a2bbc0eeaa0d906`  
		Last Modified: Fri, 14 Nov 2025 21:11:35 GMT  
		Size: 596.7 KB (596741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98dac403eeb5967a4736c15f35cb79744ae3f0796089356a9d597e0490e1aee7`  
		Last Modified: Fri, 14 Nov 2025 21:11:36 GMT  
		Size: 43.8 KB (43768 bytes)  
		MIME: application/vnd.in-toto+json
