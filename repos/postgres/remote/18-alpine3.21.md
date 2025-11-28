## `postgres:18-alpine3.21`

```console
$ docker pull postgres@sha256:44d837eb4c2ed263474a95f0cc24745413c50924df60dd73ed6c4c3e36b84259
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

### `postgres:18-alpine3.21` - linux; amd64

```console
$ docker pull postgres@sha256:0dfd3cb12690ebf83387c684c961aa642610e30a391b55af371df517018750bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111491707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde4bff118d4577b81aab69f8831b38db53c930ca5938405fd2a450fa8813820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:18:50 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:18:53 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:18:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:18:53 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:18:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:18:53 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:18:53 GMT
ENV PG_VERSION=18.1
# Fri, 14 Nov 2025 19:18:53 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Fri, 14 Nov 2025 19:18:53 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:21:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:21:28 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:21:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:21:28 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:21:28 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 14 Nov 2025 19:21:28 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:21:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:21:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:21:28 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:21:28 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:21:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf07c5f9f340e0535728fa3d1cfeac42b1fd2b5b4e3145292256dd5edf232ee`  
		Last Modified: Fri, 14 Nov 2025 19:21:55 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a7c13bb714b40082d21fa362ef27f60f0061ec4d472a01965c91efdd25e5c3`  
		Last Modified: Fri, 14 Nov 2025 19:21:55 GMT  
		Size: 918.3 KB (918261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f992d4fdce490df33287772e92b3fca5960a360c7755f503a0aff6264e22419`  
		Last Modified: Fri, 14 Nov 2025 19:19:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027cced560eb4a9190267f30fb4e4db9354bf2f0747e2608590b2918464b0dcd`  
		Last Modified: Fri, 14 Nov 2025 19:22:04 GMT  
		Size: 106.9 MB (106904683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bec8b3f847c84916505c813c20343f66fda7c97959122c38f199faf9d6a3bd`  
		Last Modified: Fri, 14 Nov 2025 19:21:55 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e1956c1a86321ec6b667cb532b1a71f5af2aabd5dc975276d02656ca960f1`  
		Last Modified: Fri, 14 Nov 2025 19:21:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c4ffc455b1727009e7e79a8e658df1a248c3c44ebfb2b50d49beb4d666a6eb`  
		Last Modified: Fri, 14 Nov 2025 19:21:55 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c330b27efb3e79b02fab6c67897868d6c12e2b52a9d1e42e623a9dc029ead1`  
		Last Modified: Fri, 14 Nov 2025 19:21:55 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67592e4daf455862cd36fca196180ee2bae1e56f6eeabe85a66aec0913fff4c4`  
		Last Modified: Fri, 14 Nov 2025 19:21:55 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:415dd364df46c0127bd293832dc99c20e882e6ede07e0930e131780927ed728f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.8 KB (642811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02249c012f7574e11a342803008c6cbbf012942edfe1b43920d3820db1df93eb`

```dockerfile
```

-	Layers:
	-	`sha256:cc340030e88a608ae029355cdcf2a860c98b4c3627143f3f5f2eb90e8d4d26bc`  
		Last Modified: Fri, 14 Nov 2025 21:18:14 GMT  
		Size: 600.6 KB (600621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e01699dea2b49d11959c1fe882cd4cd580579f1fd6eaf4275ee14913ed40a50`  
		Last Modified: Fri, 14 Nov 2025 21:18:15 GMT  
		Size: 42.2 KB (42190 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.21` - linux; arm variant v6

```console
$ docker pull postgres@sha256:7a2577821ec72fbd84acc1f3935e6607bfacf0e010c0d53a91588ee583074146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91099443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ed45e95d1f6b7084fdf3359130f96c79b4d3f707c35de721b554be3faa1aba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:36:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:36:26 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:36:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:36:26 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:36:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:36:27 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:36:27 GMT
ENV PG_VERSION=18.1
# Fri, 14 Nov 2025 19:36:27 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Fri, 14 Nov 2025 19:36:27 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:39:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:39:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:39:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:39:09 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:39:10 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 14 Nov 2025 19:39:10 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:39:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:39:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:39:10 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:39:10 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:39:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a0711ea39216d79210006c020bc9315688f18d7dc4a5a60b4bce5db7556aec`  
		Last Modified: Fri, 14 Nov 2025 19:39:28 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83fe4743ab4a59db762b995a1bbe09f1492c0efd0b573b67098920450a454e0`  
		Last Modified: Fri, 14 Nov 2025 19:39:28 GMT  
		Size: 886.1 KB (886109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94702b59e16936e0d0e12e3433ef5dcb1dc9c6077f63e99e7cafbe26da759b98`  
		Last Modified: Fri, 14 Nov 2025 19:39:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a578fd071b933fbf8a9527bf480c4a927095cb1c2854dbef22c8501dd6b2e6`  
		Last Modified: Fri, 14 Nov 2025 19:39:35 GMT  
		Size: 86.8 MB (86821670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe8ac283482591e95e540d5453299fc6af5fed06ffcfcd98867aa15df2294e7`  
		Last Modified: Fri, 14 Nov 2025 19:39:28 GMT  
		Size: 18.8 KB (18776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454f764913b426f36d733b4c20fd48e9da5ca6e38a2293f8cd20bd51d5b8b4c0`  
		Last Modified: Fri, 14 Nov 2025 19:39:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292345c3b77a0f4f2090261408e6ef7af6ef489cc14226fb2c70dc25f75bb8be`  
		Last Modified: Fri, 14 Nov 2025 19:39:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d190fc8f9bc582709f82ca35131ab9ef769d7a690e5952a9d6b739d4cc45a4`  
		Last Modified: Fri, 14 Nov 2025 19:39:28 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23f1e5a40fab22afab32be16ae54ed8ec91547c5bfd5bbcebed0fe7928beae`  
		Last Modified: Fri, 14 Nov 2025 19:39:28 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:50aa6f200e6ff00eb7e93632f23df285ee4a908fc3e93d2e32c3d90f68235d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 KB (42132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baff9f8890f6e1eaf06057b12f024268ca0fcf12fd71fda3622d6d7b7133490c`

```dockerfile
```

-	Layers:
	-	`sha256:01f7a653b181ed8a986a716a210e843cf3fa97992d40059da3dad6f110bf81a5`  
		Last Modified: Fri, 14 Nov 2025 21:18:18 GMT  
		Size: 42.1 KB (42132 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.21` - linux; arm variant v7

```console
$ docker pull postgres@sha256:4870a9126aac8a254d61724d7449aa2021145ccc172400e9c0b173fb729eb416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86246217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e71a0ee75d0316de193f3ed92acebfea2d4494dcd78a4c960c134c1116965c6`
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
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:34:27 GMT
ENV PG_VERSION=18.1
# Fri, 14 Nov 2025 19:34:27 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Fri, 14 Nov 2025 19:34:27 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:37:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:37:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:37:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:37:09 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:37:09 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 14 Nov 2025 19:37:09 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:37:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:37:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:37:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:37:10 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:37:10 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:37:10 GMT
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
	-	`sha256:cfb1fdd13c61f458b4fc9b2cf7bc740f782e5d00446691e7c253562d5196443b`  
		Last Modified: Fri, 14 Nov 2025 19:37:40 GMT  
		Size: 82.2 MB (82235295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1417dc81930b142f57c05db7e2eee1ef1c2024a074c11973c55db3f5585aac`  
		Last Modified: Fri, 14 Nov 2025 19:37:30 GMT  
		Size: 18.8 KB (18776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a806babb78141262ed19cfb7ef8a1df0125d82cdb30d04ea7352a925540fab0a`  
		Last Modified: Fri, 14 Nov 2025 19:37:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb517e92b0f0885b9678a750b5153fdb3772baf61fe2141e2ec09512d005d1a3`  
		Last Modified: Fri, 14 Nov 2025 19:37:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc85cde33610824169c4ea39f71581fa4fc3fb7f159bc42c58baf16b34e9e52`  
		Last Modified: Fri, 14 Nov 2025 19:37:30 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e279795e2f0b03079675d29822ac29ad9cc2758fe9c6a74604be0191b4729e34`  
		Last Modified: Fri, 14 Nov 2025 19:37:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:5a3cc6ae0b6ab40859277df1204871e649074dd2bcdcda5df97de729a93a97fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.0 KB (642996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8915fb7cbdbe1e5495889bd26f8735006485ed462092ba4c9f34f2c5abd5dd95`

```dockerfile
```

-	Layers:
	-	`sha256:54ea09718c3d9d77e52b49fdfec9360810048281483b35b02b519d59160389c8`  
		Last Modified: Fri, 14 Nov 2025 21:18:22 GMT  
		Size: 600.6 KB (600649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e402e5e7ef62a8b7c27eaab01745650a3a8c3b21db1c52a15665d71b18b0e204`  
		Last Modified: Fri, 14 Nov 2025 21:18:22 GMT  
		Size: 42.3 KB (42347 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:a1856f94536f6494025df5d97ef13c13738f1b7820c1d49a676e7f974bcb9868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107400525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15766de59bbe07192e35519f1c03cd645615bf317e1735bb4ab3a0d79d2c767e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:18:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:18:33 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:18:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:18:33 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:18:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:18:33 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:18:33 GMT
ENV PG_VERSION=18.1
# Fri, 14 Nov 2025 19:18:33 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Fri, 14 Nov 2025 19:18:33 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:20:58 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:20:58 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:20:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:20:58 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:20:58 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 14 Nov 2025 19:20:58 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:20:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:20:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:20:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:20:58 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:20:58 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:20:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc6d32132d8058d164a5b884333755cd275b6a6e6a839d22ec4805db62500cf`  
		Last Modified: Fri, 14 Nov 2025 19:21:21 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f606f7b830ce2711124a1cd13a2c4aa0e0f5e4b51c10733b674ea50f29b91092`  
		Last Modified: Fri, 14 Nov 2025 19:21:21 GMT  
		Size: 873.5 KB (873462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb28240bfd07c307796948bd1350763986eee671b2b25449b9538ee76da34d0b`  
		Last Modified: Fri, 14 Nov 2025 19:21:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a148a017028de23bc5d406acf3a070830679e476b71aae051056b4b413ac15`  
		Last Modified: Fri, 14 Nov 2025 19:21:35 GMT  
		Size: 102.5 MB (102508519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f7bfec056463b1800998bb14703eff801b2f6f0dc7cfc2507fd4f337002921`  
		Last Modified: Fri, 14 Nov 2025 19:21:21 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c08cd185eef6b5a93567c9f03eeb7f013e76de5ea09a227e5d71f4cb7423197`  
		Last Modified: Fri, 14 Nov 2025 19:21:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cc5f8881c0c11e73cb44f92310a01f5ef7b102f2c6e36a24f67756b62a8a29`  
		Last Modified: Fri, 14 Nov 2025 19:21:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2fc772314399ae5f3df4e4040f0469e1f7f842db1313938882d9ccd2f1fc81`  
		Last Modified: Fri, 14 Nov 2025 19:21:21 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f900efb325268b6477caf145587107085a9328fecf500bb8391b8cc5ac0a2dd`  
		Last Modified: Fri, 14 Nov 2025 19:21:21 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:a4a72950239dfd979e073461ad72460214e9be22436ef9c4b5cec8569b70d5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.1 KB (643052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb6f14d7fa1428733cd52f23e085c5aed44dbbd6c261c549f43e3452a73091f`

```dockerfile
```

-	Layers:
	-	`sha256:3d126d1815aaebeb3a8aeb0b8f0c69763d273770f485ceedf73e3cf32ee28bed`  
		Last Modified: Fri, 14 Nov 2025 21:18:26 GMT  
		Size: 600.7 KB (600665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fddf9c6e3e00edf4b71d744686e97fb7981de2e73ba579ac1a8e883edaabf3d`  
		Last Modified: Fri, 14 Nov 2025 21:18:27 GMT  
		Size: 42.4 KB (42387 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.21` - linux; 386

```console
$ docker pull postgres@sha256:ce19456430a0f9979da4486ba98474706cce45171f27f0ed6d83ff03d35f1797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117756407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d94bc62349e9b0425884201cb556f4a5e59db3bc41553011a9ba347658e7511`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:19:29 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:32 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:19:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:19:32 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:19:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:19:32 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:19:32 GMT
ENV PG_VERSION=18.1
# Fri, 14 Nov 2025 19:19:32 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Fri, 14 Nov 2025 19:19:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:22:18 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:22:18 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:22:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:22:18 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:22:18 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 14 Nov 2025 19:22:18 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:22:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:22:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:22:18 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:22:18 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:22:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca791914e3aa2edd1fe946f36dd9608a34ba2bd2b4417d68043e194e07d8e61e`  
		Last Modified: Fri, 14 Nov 2025 19:22:43 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633a78bffeef3325271ec851bda191e808e403f91d48632061c2b26d5e860d5a`  
		Last Modified: Fri, 14 Nov 2025 19:22:43 GMT  
		Size: 890.6 KB (890613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9724eda4585bca80f1dd1da45730c48dc14eac9b2ccb4bffbe924cf3e6fff8a`  
		Last Modified: Fri, 14 Nov 2025 19:22:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f689dfc9d8309fa2ca75f547e0e8d9a5a7aeea23a9a318268a6317241084301`  
		Last Modified: Fri, 14 Nov 2025 19:22:57 GMT  
		Size: 113.4 MB (113374899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb65fa88afe26c43062485f92d76fb4eada16a415ca5c9f40563ce4dca6e027e`  
		Last Modified: Fri, 14 Nov 2025 19:22:43 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c82569e0f2fbdd1a27cd806f6a6b0dc45f8b0e75e3468ba46c63fa0ad7729ec`  
		Last Modified: Fri, 14 Nov 2025 19:22:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dd6aa1f935b1b4c5079e14c34091373a96d4e827d538c9c26b9bca8f14771d`  
		Last Modified: Fri, 14 Nov 2025 19:22:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8800ce39ad55de0569215f620e6fbafdf0bf534646ea5e5fc2af0748e9e6f02b`  
		Last Modified: Fri, 14 Nov 2025 19:22:43 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2405a003984a1109c51b78e40970f669611c0aa434dcf6666a60054e131894a`  
		Last Modified: Fri, 14 Nov 2025 19:22:43 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:d108e0fd2d997a1154dfc9f382d6e193b3c7caa246d44c42d18322d2d4308494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.8 KB (642750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b007fe514a6fa55bcc9ee65a1a2a08ae4a1827b5c980f041aaf47397ddf450`

```dockerfile
```

-	Layers:
	-	`sha256:c83b4ec34bdf1bd1f47ca74173a820ab707e5d83e661f27d9bd84acac16be6cb`  
		Last Modified: Fri, 14 Nov 2025 21:18:31 GMT  
		Size: 600.6 KB (600601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:324d092d44a33ef8dad5fe89e6ae0e0222c6164571cf2c08fb896ccb091c0382`  
		Last Modified: Fri, 14 Nov 2025 21:18:31 GMT  
		Size: 42.1 KB (42149 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.21` - linux; ppc64le

```console
$ docker pull postgres@sha256:7e4cf2c65e26144f251bd7fd8137419ce15888f872d0ea23e49b9439e050f606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95433153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c323c01564c95543bdbdd1a1c57389e975daccc99672cce6869eca117c91bca4`
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
ENV PG_MAJOR=18
# Thu, 13 Nov 2025 21:12:35 GMT
ENV PG_VERSION=18.1
# Thu, 13 Nov 2025 21:12:35 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 13 Nov 2025 21:12:35 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Nov 2025 21:15:19 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:15:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:15:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:15:21 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 13 Nov 2025 21:15:21 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 13 Nov 2025 21:15:21 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:31:15 GMT
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
	-	`sha256:ee5416e71f5048ccf69e5fe2b3d92e4cd7743915b3f616ae7bb6f3c1be9be5a7`  
		Last Modified: Thu, 13 Nov 2025 21:16:22 GMT  
		Size: 91.0 MB (90953844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51d371519067ab98f9dd9ef72608fc605c954f7a29224f7e28ee19b2f7e0a54`  
		Last Modified: Thu, 13 Nov 2025 21:16:11 GMT  
		Size: 18.8 KB (18784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24005eae5cdcba0b98e2ee81f6f20c10780b5effbc869a40a7c844f640afe541`  
		Last Modified: Thu, 13 Nov 2025 21:16:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f6c8cff0c1f67a86bfdd27497d0d2e785785eb33112b445c367c6f3681887d`  
		Last Modified: Thu, 13 Nov 2025 21:16:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cc874a3261cee463f65d29522de3b23bf897867a08f57ee24dce1370370467`  
		Last Modified: Fri, 14 Nov 2025 19:31:40 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a8b94717ce73c0d2974808d00ba3759ba179c8a85b9464a6652e05fbc8537d`  
		Last Modified: Fri, 14 Nov 2025 19:31:40 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:7478fb1105109c28e6a446719468f4e49cd2b759d675610c7f3ba462b38ea563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.3 KB (639271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5709757df87f59d0f4898d58321481214316bab0a275d174076252396568e445`

```dockerfile
```

-	Layers:
	-	`sha256:9e8b1fa02c2e86cdf521406be9c6cabc36d5be1524981751750fd99a5ad0b658`  
		Last Modified: Fri, 14 Nov 2025 21:18:36 GMT  
		Size: 597.0 KB (597036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d853f1be1c169662e38190c9ca703fe7da5c935512ef65cc713e1a4113900b78`  
		Last Modified: Fri, 14 Nov 2025 21:18:36 GMT  
		Size: 42.2 KB (42235 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.21` - linux; riscv64

```console
$ docker pull postgres@sha256:5de71f4c13339c7ea2424a172df2d9a64454965b847127ab1e8d99f8006dcd51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111695897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dcb6d5bbec98aec5f088bb939e112af42c32f1320c62bf557ea304a36ced90`
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
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 01:03:30 GMT
ENV PG_VERSION=18.1
# Fri, 14 Nov 2025 01:03:30 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Fri, 14 Nov 2025 01:03:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 01:53:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 01:53:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 01:53:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 01:53:23 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 01:53:24 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 14 Nov 2025 01:53:24 GMT
VOLUME [/var/lib/postgresql]
# Sat, 15 Nov 2025 06:38:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 15 Nov 2025 06:38:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 15 Nov 2025 06:38:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Nov 2025 06:38:41 GMT
STOPSIGNAL SIGINT
# Sat, 15 Nov 2025 06:38:41 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 15 Nov 2025 06:38:41 GMT
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
	-	`sha256:3c2f9a98a0f588a8cd6874be54380357a162089b5d6e67a3ddd047e25e5d2cd8`  
		Last Modified: Fri, 14 Nov 2025 01:57:01 GMT  
		Size: 107.5 MB (107452088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6964faf9a197c0fa811f87eab7968b3a8d6136538cbbf801de36d226c9f4616f`  
		Last Modified: Fri, 14 Nov 2025 01:56:49 GMT  
		Size: 18.8 KB (18782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cbb8573e14b309a42ff5099730dce5957deaa7a4a037e66ee1ea68182ac02a`  
		Last Modified: Fri, 14 Nov 2025 01:56:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd3e7a23358dde2ebf77bc89027661b58d7f4156acc0d0d2a598938f2b38975`  
		Last Modified: Fri, 14 Nov 2025 01:56:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a4ad3cd80784ebbf14daef59e40180782fe14d2c3b4d346ac8ceea3f518926`  
		Last Modified: Sat, 15 Nov 2025 06:40:02 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c39c055c39041cf64eb2db65967e3fbc7e6c143cdcddb59570248c4504ad84e`  
		Last Modified: Sat, 15 Nov 2025 06:40:02 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:11aa779a47cd9145ab3dc39455a22f09fb82c6921a9d28f655f8fc87630f9595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.9 KB (640936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b049a0823c007bb50dc0e98e9958049633fb7afd9f22f8050f6af136f4e461f`

```dockerfile
```

-	Layers:
	-	`sha256:1e565811801630cf650e131de1ae97bd8ee4eb84d9ca6d038516bf19bf53694b`  
		Last Modified: Sat, 15 Nov 2025 09:09:41 GMT  
		Size: 598.7 KB (598694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6cd7a83f85dcd26b71abcd4b85ed7a7e176227e355d9babf35edbbb9679919d`  
		Last Modified: Sat, 15 Nov 2025 09:09:42 GMT  
		Size: 42.2 KB (42242 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.21` - linux; s390x

```console
$ docker pull postgres@sha256:d5135bffc4233b4925ed7dc48fb04631a2360d3543ad35e6d3012a7a5bf2896e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120181954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342621504d4cf121b500d046dd0e0d7f7436bd66f7d5a90eec3a9c93133a83df`
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
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:16:00 GMT
ENV PG_VERSION=18.1
# Fri, 14 Nov 2025 19:16:00 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Fri, 14 Nov 2025 19:16:00 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:19:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:19:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:19:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:14 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:19:14 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 14 Nov 2025 19:19:14 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:19:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:19:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:19:15 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:19:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:19:15 GMT
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
	-	`sha256:850e1dd9c6934b0c18cc2e9ed718a9457e0e1092056d169ac6a5339318ca549d`  
		Last Modified: Fri, 14 Nov 2025 19:20:12 GMT  
		Size: 115.8 MB (115794926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be5a2bc74d5b1b7a239d15fd4a7cec785fe5b1d5811989559dd9a0af5eaa5b`  
		Last Modified: Fri, 14 Nov 2025 19:20:01 GMT  
		Size: 18.8 KB (18774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb87951babdba048e2537bba37780391c8c4fb31664bf0602d91b6d6666afd7`  
		Last Modified: Fri, 14 Nov 2025 19:20:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f45ab80b333cacded760167480ab3f6d69fbbe58b4eb3aa81492c9903bf2e9`  
		Last Modified: Fri, 14 Nov 2025 19:20:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4c2ad395173c073547274c6ba80353537fd203e3871683415746496a7744d8`  
		Last Modified: Fri, 14 Nov 2025 19:20:01 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83590f7be2537ac49a021dcea743e180f5fccadf5951e81a7d63051a784b4cf`  
		Last Modified: Fri, 14 Nov 2025 19:20:01 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:fcce7f543d53bff045d9d6d4ee92c5cb9092729d8d4e83044888bd91fcd1f192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.9 KB (640860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596fcf21fa9b3630ea2fd0780decc4f3b2beb65cce6a110f1c6853fef4a25e3b`

```dockerfile
```

-	Layers:
	-	`sha256:8e0ee8a3279e5849007857e8521cef029e36561162e7f2153892fc0c0510246f`  
		Last Modified: Fri, 14 Nov 2025 21:18:42 GMT  
		Size: 598.7 KB (598670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7af86f9805cffc4893f68458e06d17e9f68037537f9790e7ed55d5e82b0bb2`  
		Last Modified: Fri, 14 Nov 2025 21:18:43 GMT  
		Size: 42.2 KB (42190 bytes)  
		MIME: application/vnd.in-toto+json
