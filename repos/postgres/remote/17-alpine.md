## `postgres:17-alpine`

```console
$ docker pull postgres@sha256:9a78577340f3d26384b6aebeb475c0d46d664fd4ffa68503b4be4e4462745f94
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

### `postgres:17-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:29d1c09928636be90e3365144f4794e1a4193faf58c037475a4d0c509bd8906f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110611167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bf692a8125ea8311500f8e16b79b8103822e8f9302cb166aceda8e6bfd5cd6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:17:51 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:17:54 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:17:54 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:17:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:17:54 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:17:54 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 19:17:54 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 19:17:54 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:20:04 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:20:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:20:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:20:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:20:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:20:05 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:20:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:20:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:20:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:20:05 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:20:05 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:20:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0994e2a6ce3a81fb431dc0c3fe293b8dc682328ca75ced21aae8188cce4ff521`  
		Last Modified: Fri, 14 Nov 2025 19:20:33 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed24ebfd38baded179e8a6f820fc645a6f0f3b22f3e00cc18adccbece1a6cc55`  
		Last Modified: Fri, 14 Nov 2025 19:20:33 GMT  
		Size: 918.3 KB (918291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa9b0a7f3bddc07d4b0f6458611069019536dd6f3b7f189518de6c7f375f988`  
		Last Modified: Fri, 14 Nov 2025 19:20:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fdc01cfb64af494df8709629ed2ce0f5320bcc05a5e06599232c5720bc0df9`  
		Last Modified: Fri, 14 Nov 2025 19:20:42 GMT  
		Size: 105.9 MB (105873135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004c438aca5b3ffaceed0e23c5c8ef77b275ecc1a5013b7b766d5e0aed198fbf`  
		Last Modified: Fri, 14 Nov 2025 19:20:33 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656ca692f8ee7c8539551035672430dc6663d01a882f3188a7b3362864ed1eed`  
		Last Modified: Fri, 14 Nov 2025 19:20:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40df805578103c3c1b2424174c45c2e3cf43a423f0d0bd502ad9576d91c3c9ed`  
		Last Modified: Fri, 14 Nov 2025 19:20:32 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8444cb202a3f25f2dc3237b34bcacab7b11a2fe38f3d138553d4d67606243b66`  
		Last Modified: Fri, 14 Nov 2025 19:20:34 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7344f10d1096e90b097c3ff28147a81bbe30c3b9291d4e6a8ab4e667b7a2c636`  
		Last Modified: Fri, 14 Nov 2025 19:20:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:a972e5a7881cf62100ebce0ef6fc3be3ba4514063198939fd6c9cbf4c78214c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.6 KB (638609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272fe30ebf8f84c92ac58664ad034c7af997f4367694ba41c15804cae103e662`

```dockerfile
```

-	Layers:
	-	`sha256:6e124dcaa3be565d4fc88a254181e295d86aa416facdcd177928ed1ae34665e2`  
		Last Modified: Fri, 14 Nov 2025 21:15:27 GMT  
		Size: 596.9 KB (596931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0bd37b39e7760efa7e3046f0093c22e05699e55cc5fc917e1bd10332e520aec`  
		Last Modified: Fri, 14 Nov 2025 21:15:28 GMT  
		Size: 41.7 KB (41678 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:08a9b88cf715b6534ca6c72b80f777ff0b8af0fc78b6dbda6524dacc41c711e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90129881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f520b1bd2b0f01d74035d691985ed4483f7368a68f034512e26721658f4fd08e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:16:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:16:43 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:16:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:16:43 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:16:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:16:43 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:16:43 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 19:16:43 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 19:16:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:19:53 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:19:53 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:19:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:19:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:19:53 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:19:53 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:19:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:19:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:19:53 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:19:53 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:19:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d747b4495e300d8d86bec1f2e70800c38ff0d1629c7cfa79d26535c03ec6ff`  
		Last Modified: Fri, 14 Nov 2025 19:20:18 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea33d9347f314fd31d2580279613454f5a86770ee95b3005e22a0b3ecb43b9f2`  
		Last Modified: Fri, 14 Nov 2025 19:20:18 GMT  
		Size: 886.1 KB (886135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c3319c62b3c16874a4c1cee65de5e835770d43b6248ca033472f0439c6c53e`  
		Last Modified: Fri, 14 Nov 2025 19:20:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75cbe407e19a6f17ff1d22e7c88920ea3b3045d01a632130c09387c91115c24`  
		Last Modified: Fri, 14 Nov 2025 19:20:23 GMT  
		Size: 85.7 MB (85722374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f59dd3c8a1ccb29ed556e1fd6bebec53bce5307691a550eda5954b11a6e11f`  
		Last Modified: Fri, 14 Nov 2025 19:20:18 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf0f3eed6ef7f7376af061ff70ae24160779f880225df100f1d327c5cbeab37`  
		Last Modified: Fri, 14 Nov 2025 19:20:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78a82204a6a2ef0006d1af9fd7121b6f7d290fd1f2ea3a1404c7b3dfab13f57`  
		Last Modified: Fri, 14 Nov 2025 19:20:18 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25162a5ad9b86f1eb69b7fa0edc9799713996a2483f3368c39ad5c8f6ae67467`  
		Last Modified: Fri, 14 Nov 2025 19:20:19 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92f1814988f2ec9324b890ddc8a26a514d1949382ddf39380003c54798e0e19`  
		Last Modified: Fri, 14 Nov 2025 19:20:18 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:6eecb9d22a9de9e090799759725d52ee795784201a640b5f57901410e2f0a8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 KB (41627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f280b0dac4bc955fe044dd8149ef862587ce95aa12d4cd6a648855c2d01e7b9d`

```dockerfile
```

-	Layers:
	-	`sha256:44e93fdf3ec47638e46629c9ed14f14761c0c30ae446a8dffc07921b15797261`  
		Last Modified: Fri, 14 Nov 2025 21:15:32 GMT  
		Size: 41.6 KB (41627 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b0e6891ddbdb40e15c61be56c7647a14e945461782c4e609bef420c093616686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85366317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d1ae29b5361e01ea02f4457c02dd595765fc1ffb972ce6aeb8cc42184917a9`
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
# Fri, 14 Nov 2025 19:36:46 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:36:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:36:46 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:36:46 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 19:36:46 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 19:36:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:39:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:39:45 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:39:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:39:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:39:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:39:45 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:39:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:39:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:39:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:39:45 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:39:45 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:39:45 GMT
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
	-	`sha256:1d9e990d60dacc5ab83d6c0009c282d5d9a1d7862ae45e5732b8cd18b280e9fa`  
		Last Modified: Fri, 14 Nov 2025 19:40:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be41f413943cae7bebedf87510d2ab71db87cbea5a9b3bca50658ba5a7116f49`  
		Last Modified: Fri, 14 Nov 2025 19:40:10 GMT  
		Size: 81.2 MB (81241340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1665fb6de118e6356152e8f35d7dbc315f188e212e2b15087789d7d98f1b16bd`  
		Last Modified: Fri, 14 Nov 2025 19:40:04 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b64c1a5d9baf00117c8ed129ac6004580a1f0130591b5194ed32c4de5b50acb`  
		Last Modified: Fri, 14 Nov 2025 19:40:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d32181a1109b8a510da86160bac2ddfa732155266798f4a4aa3e33b7fb8202`  
		Last Modified: Fri, 14 Nov 2025 19:40:04 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b66c6f206b0b204bbec08bfc931b44c7022186d9aa8d00854520ea7f48eb251`  
		Last Modified: Fri, 14 Nov 2025 19:40:04 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c66eb8ae117c524a23d4b370e873825538b189860b476ba1f235f74d8d5706`  
		Last Modified: Fri, 14 Nov 2025 19:40:04 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:f1fa9135ece95828010452933510648d1541880faf3b3660d61ddfd0346d3896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.8 KB (638810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159b60c104852788673432a8954ba5c47e67b1fcf883c269a765f76fcb762055`

```dockerfile
```

-	Layers:
	-	`sha256:5f62a03777af1920b14ae77875317fa45d1292e82dd128285a950d4e42985b3b`  
		Last Modified: Fri, 14 Nov 2025 21:15:35 GMT  
		Size: 597.0 KB (596967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90a2a2524d947292988afd700017aa7beea2442e9c465c6c63649c48361bcd79`  
		Last Modified: Fri, 14 Nov 2025 21:15:36 GMT  
		Size: 41.8 KB (41843 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:b7785613246b73e43d51780a39d43d1f93b12001f053e0205b9eab3372453f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106570441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54678687cee167743dee17801b7b4c22ca1dd5da2212b63b23dc1fc1a412a77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:18:29 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:18:32 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:18:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:18:32 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:18:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:18:32 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:18:32 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 19:18:32 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 19:18:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:21:21 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:21:21 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:21:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:21:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:21:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:21:21 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:21:21 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:21:21 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:21:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:21:21 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:21:21 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:21:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bd6fee94a9b7e35cebc638503f7fe0a7e5cc0934a0f0f1ff34ba2d48a1bfe0`  
		Last Modified: Fri, 14 Nov 2025 19:21:46 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8974472d5a10b9b37b1358ee292eca354118e2012e9295fc896fefdc5507da2e`  
		Last Modified: Fri, 14 Nov 2025 19:21:46 GMT  
		Size: 873.5 KB (873485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e152b197a77fa3282cfcb3fecf893f7e12ddecd7112a99a0e53cdb5a526f59c`  
		Last Modified: Fri, 14 Nov 2025 19:21:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02dccb3be76e1c142dbde0bc6c4d94fa51e99353900e1d467c1f01df53eb88f0`  
		Last Modified: Fri, 14 Nov 2025 19:21:52 GMT  
		Size: 101.5 MB (101541595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c613172c5d8bf1a267541b5d289d09ea7a56707f17d40e7fb55570f9590e1759`  
		Last Modified: Fri, 14 Nov 2025 19:21:45 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea03402caa5590be567119ef3ed04adb1dcee60bcbfddbb8b70395d6c282ab4`  
		Last Modified: Fri, 14 Nov 2025 19:21:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea979d86196795700da441c3c12c3a66a07b1d920378bae2e39fae67a22d0183`  
		Last Modified: Fri, 14 Nov 2025 19:21:46 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0a9cbe0c4a42d5a436005f7ae6f792bcda17104e7e0c3658a7821ef457e18b`  
		Last Modified: Fri, 14 Nov 2025 19:21:46 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39381aa22444f4115941deac3269100adf2de57541180fd39077661bbb4d888`  
		Last Modified: Fri, 14 Nov 2025 19:21:46 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:384e95b1aa8b6ba0fdd347bb331438ad7c6a512f2be0a65d242d2ab02a4dc1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.9 KB (638874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a793ac771b78a62568b15306185a65fb12184cd23cc768aafec12b21126920c`

```dockerfile
```

-	Layers:
	-	`sha256:b8cf4b2fed3dea1dd9baf8017593e4ac20eebb17aa173d921ab8ef1729593d09`  
		Last Modified: Fri, 14 Nov 2025 21:15:40 GMT  
		Size: 597.0 KB (596987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9c28213bf110064f12510405d40beff55688476d1661e31b3d0bb553f181113`  
		Last Modified: Fri, 14 Nov 2025 21:15:41 GMT  
		Size: 41.9 KB (41887 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; 386

```console
$ docker pull postgres@sha256:b4fdb34c62518a5a606a675fc229c0476234778faf37dc4ca356290844d85a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116901293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71db03c1fc5f46972d12bc22bc13ed6b83854c0acf926d777143bc5921a80e0`
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
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:19:30 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 19:19:30 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 19:19:30 GMT
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
	-	`sha256:2c8505dcd1621474b9493c3ff03a4340b34a036c080301c6907ce467bf9540a0`  
		Last Modified: Fri, 14 Nov 2025 19:22:33 GMT  
		Size: 112.4 MB (112374430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9b74b912516215683605bd37c77b67f8eb1e39b34cf28e39f495054cfa4724`  
		Last Modified: Fri, 14 Nov 2025 19:22:25 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b8ca138a07e5f75267194b0ae7e131e4a0f314b6cb56d56f7f36b807ec549e`  
		Last Modified: Fri, 14 Nov 2025 19:22:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ded7765b9a2a3a96ecb13fe0e448cbe4e393caa6dbb4db9277c408e976f384`  
		Last Modified: Fri, 14 Nov 2025 19:22:25 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a93d39292a414b43c333f0541ee910d03963f60a6567d7774374c1c964bd89`  
		Last Modified: Fri, 14 Nov 2025 19:22:25 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb0638f9bb72fe8febd7afbb33bbb535dc894e62812f59285aa7154ac75cf3e`  
		Last Modified: Fri, 14 Nov 2025 19:22:25 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:db958d975538305ee2b88f15a1d6ebe993583f9ddd5b3ea0a27a838f50627e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.5 KB (638538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89e867cf1cc742f03512adf9880aa8b18c9dddb2a03e1058b815a19ed34a476`

```dockerfile
```

-	Layers:
	-	`sha256:cb860b89ac9d2eba3d5af486cd23b273313e52b9bfc7107dc41863f74805c14a`  
		Last Modified: Fri, 14 Nov 2025 21:15:44 GMT  
		Size: 596.9 KB (596906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0558492667013c08f9f5dde84205e31601d88b53107fd88be9d800b24425cee`  
		Last Modified: Fri, 14 Nov 2025 21:15:45 GMT  
		Size: 41.6 KB (41632 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:082495c8625d24f65d09965f6c131646c3b18d9782dbc10813b771e87c1024a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94461675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907dcba38594692baf8c99d974d66b021d436d7e88b42c0cb0157ff1cff77562`
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
ENV PG_MAJOR=17
# Thu, 13 Nov 2025 21:08:48 GMT
ENV PG_VERSION=17.7
# Thu, 13 Nov 2025 21:08:48 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Thu, 13 Nov 2025 21:08:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Nov 2025 21:22:18 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:22:19 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:22:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:22:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:22:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:22:20 GMT
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
	-	`sha256:fde2a2aae351ffbcf995631c079c0b97ded2f7c3661002ac08134cdddae2335d`  
		Last Modified: Thu, 13 Nov 2025 21:23:10 GMT  
		Size: 89.8 MB (89833103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867e45e5d5552b85adc59ef02d327485fe82c6e27b8de34d00850b7527ee2b55`  
		Last Modified: Thu, 13 Nov 2025 21:23:04 GMT  
		Size: 9.9 KB (9887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0627fc51dcc9c0ece8fc0c5c8bf6ac3711ddcdcee9e0813db7736d198baabc`  
		Last Modified: Thu, 13 Nov 2025 21:23:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f8d7fc1e5c0a3b9a07885988d69056af9b83e638663e5543da0f72813e68a7`  
		Last Modified: Thu, 13 Nov 2025 21:23:03 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ae4147bd721558dac3d0c0db9f5236bbec4dcc5ea60e77083c81ebea0d9b88`  
		Last Modified: Fri, 14 Nov 2025 19:33:28 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cdff11f6593e49ede255ad20fc7b6ce595b49d16596d52c1a89a72aeb5a3ea`  
		Last Modified: Fri, 14 Nov 2025 19:33:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:687c41456529aafebaf4a5c2aa5b4eecb59d678c1df871f68f59cffb2de8cb44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.1 KB (635082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9b2fccc16a9bed2d5d9907e776c072f52cc771fa662462947537fb049a2cb4`

```dockerfile
```

-	Layers:
	-	`sha256:080d21eeb7e228d8bdbaa8894495cd9e0378de392ddcdec2a4f993f53e3dc6f7`  
		Last Modified: Fri, 14 Nov 2025 21:15:49 GMT  
		Size: 593.4 KB (593352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3397995e38a0e4768cd4f8ea538ac5dfb2fa6b5fd25ebbed9704e6a11721552`  
		Last Modified: Fri, 14 Nov 2025 21:15:50 GMT  
		Size: 41.7 KB (41730 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:7c8692da732bc4eec4f757bad5c47d5b8590a04eb3f460a12cc49ecb67f6f7bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110692968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9306a4f63907ad80183d6ec14c3be5b4acb34dadfa14202738a0836761fbd4e`
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
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 00:10:14 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 00:10:14 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 00:10:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 05:01:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 05:01:38 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 05:01:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 05:01:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 05:01:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 05:01:39 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 15 Nov 2025 06:42:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 15 Nov 2025 06:42:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 15 Nov 2025 06:42:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Nov 2025 06:42:25 GMT
STOPSIGNAL SIGINT
# Sat, 15 Nov 2025 06:42:25 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 15 Nov 2025 06:42:25 GMT
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
	-	`sha256:f6bfee44a95c2692e0be95cd1de3ccf422d1dae2d3106275c20b3fc5c413593a`  
		Last Modified: Fri, 14 Nov 2025 05:05:07 GMT  
		Size: 106.3 MB (106293785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5d54e1613593bfb94c66fd0899c56767ab464a0e5c520206d8de2e3134e7c7`  
		Last Modified: Fri, 14 Nov 2025 05:04:57 GMT  
		Size: 9.9 KB (9892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782122b5d1cc069c59afc87cd1a20b097f6d4332247ba9dccfe974af52d4144`  
		Last Modified: Fri, 14 Nov 2025 05:04:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc9a04bb26a1312b2cfe81cb8b3290a3b5bd5659162af6868ff24ccdba909b4`  
		Last Modified: Fri, 14 Nov 2025 05:04:57 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51acceafee787db144b1f8115258302f3fe54a5b5abe4d922fa3818992b15ae6`  
		Last Modified: Sat, 15 Nov 2025 06:43:45 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7eacdcb01f8e11af93d8386386b56fbf9c6587824351ff15b5b5bd988fe4001`  
		Last Modified: Sat, 15 Nov 2025 06:43:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:f3826bc748f178b382b792a22f089463d2f581ab09e54f8d2d8fed7dccd0c9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.7 KB (636746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b2591a1f19eaf3378cf76275024a69c598f31850da66ac8dffe7a0d8a3a662`

```dockerfile
```

-	Layers:
	-	`sha256:df0be019d0918f066f8d55b5698dc5825ec2a09dd7f7e640dd347c468374f6b6`  
		Last Modified: Sat, 15 Nov 2025 09:08:52 GMT  
		Size: 595.0 KB (595010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40d074232820c1151886e4d3850a4a0040ea9e76f37c5d8c14294842c17e2688`  
		Last Modified: Sat, 15 Nov 2025 09:08:52 GMT  
		Size: 41.7 KB (41736 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:9a6d20c8e5a30502fbbbff0dc8e0a8db5c269cc1447a27411196d6da09b38600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119335733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f608de7f8f0d6df607a6e12442c11e40dda431a66e226836e4780b2666720d`
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
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:15:53 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 19:15:53 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 19:15:53 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:33:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:33:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:33:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:33:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:33:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:33:57 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:33:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:33:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:33:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:33:58 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:33:58 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:33:58 GMT
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
	-	`sha256:e356ee2d0b9c6efd5140b6dda606cc8b4d24a7b56799f4fc7838c3f5f78a03c6`  
		Last Modified: Fri, 14 Nov 2025 19:35:00 GMT  
		Size: 114.8 MB (114774780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23ff3a76b9e5fb887343e1526d8cd05816a25c615bce0d9b3418930c40ca405`  
		Last Modified: Fri, 14 Nov 2025 19:34:30 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232cb81ef013770267183e4a07a17978101f8931eeb60e04bc5d5c2fc8b9ce20`  
		Last Modified: Fri, 14 Nov 2025 19:34:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286eb4cb17a8f2121af656a98941b16ef4660a95f5af5b6a1074ad862aa9006a`  
		Last Modified: Fri, 14 Nov 2025 19:34:30 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc0c372469f52d07f66c97c8a77e8c3353b8986169fc0cf2a016d22a00aae5f`  
		Last Modified: Fri, 14 Nov 2025 19:34:30 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a438a549b252826dbd1deba7329e81001b5ec9ede27452234e0581badee70aa`  
		Last Modified: Fri, 14 Nov 2025 19:34:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:2c5a26e3470208276d98809c9f3355cedb31861647bbecd5049837a06b5c7151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.7 KB (636658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c010cba5c02b2fb21f8177060469aa15e6d9702db1a3fa3228ca10211cf651b1`

```dockerfile
```

-	Layers:
	-	`sha256:8b5a69c8458c70256e2e33d9d22cfe4ab7bc2eb9b1ff9f4457fef02a82fb667c`  
		Last Modified: Fri, 14 Nov 2025 21:15:55 GMT  
		Size: 595.0 KB (594980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3514306b6a716df73c964b516bcd502f2f06fde0cd8c50ab4649d4390ba64c8f`  
		Last Modified: Fri, 14 Nov 2025 21:15:56 GMT  
		Size: 41.7 KB (41678 bytes)  
		MIME: application/vnd.in-toto+json
