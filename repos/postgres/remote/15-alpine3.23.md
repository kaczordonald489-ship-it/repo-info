## `postgres:15-alpine3.23`

```console
$ docker pull postgres@sha256:1d1095b0503145be79c79239372aefadfacf6b7c33c9245bbf99ce4b6b89c737
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

### `postgres:15-alpine3.23` - linux; amd64

```console
$ docker pull postgres@sha256:f6498f214984ab10ad90d839204a19effa2ad3aff15fbacd12e43cd8b527c5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109127793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb506a9728d218a29ad9c1fd7ed6acb713214fa3fe10dbc875c5cd1a865ebb46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:31:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:31:39 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:31:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:31:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:31:39 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:31:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:31:39 GMT
ENV PG_MAJOR=15
# Wed, 28 Jan 2026 02:31:39 GMT
ENV PG_VERSION=15.15
# Wed, 28 Jan 2026 02:31:39 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Wed, 28 Jan 2026 02:31:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:33:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:33:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:33:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:33:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:33:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:33:40 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:33:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:33:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:33:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:33:40 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:33:40 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:33:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80880d84c7eeb57bedbca52a87ac323b2b0c27f8c115dd2d32b8bc2a9a7655e6`  
		Last Modified: Wed, 28 Jan 2026 02:33:55 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ab15f7caf3caf94a48aa62d269eec6e0d869cc886c905949866c0f17a59c40`  
		Last Modified: Wed, 28 Jan 2026 02:33:55 GMT  
		Size: 922.9 KB (922929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0f76fbbf7f91d76e45135fae95d276d929a62f3042852acf5de36da4597206`  
		Last Modified: Wed, 28 Jan 2026 02:33:55 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b5376b3898a0e776f38c6933dfbeeecc5f870a11c23bd962070d6806db64e6`  
		Last Modified: Wed, 28 Jan 2026 02:33:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f57618094a253fc9153eb6a762e7610e28bab12ccd52b410a4cc8efdef82`  
		Last Modified: Wed, 28 Jan 2026 02:33:59 GMT  
		Size: 104.3 MB (104326010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89acc9a02475190ea2d7e428a7fabd2a997eed9f2dff3f41b5a04d599fd197a2`  
		Last Modified: Wed, 28 Jan 2026 02:33:56 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76724a94cd793f3e3fb03341fec43ce965bfaaccfb60d2bd68103be5c0aad1bd`  
		Last Modified: Wed, 28 Jan 2026 02:33:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc34e1889eb4c3e6820a4e1b3a79c88b6495c280c3300493d56cad1bdf94d559`  
		Last Modified: Wed, 28 Jan 2026 02:33:56 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e54eccd7e455940d2557c214dce43d40fc67e315c13f64d73f5c011bc561386`  
		Last Modified: Wed, 28 Jan 2026 02:33:57 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ae69fca2448189ab037840644ffb75af1c487b70fd4b9f6e27397131b3f3ac`  
		Last Modified: Wed, 28 Jan 2026 02:33:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:b3d31ad55cee976fbb2822bdbdd2e3de8683e8ee425ad071788339a6f3e40ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.5 KB (642470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37dab65e593068892a99c942a68da830dd56dfee5f6364349ad8ecb6ce4f1edb`

```dockerfile
```

-	Layers:
	-	`sha256:aa1bbebb769af6bcc572c9192eb3ff8c5af4a032ad2f46fd2e2324f5e3240cdf`  
		Last Modified: Wed, 28 Jan 2026 02:33:55 GMT  
		Size: 598.1 KB (598080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55445468600477581af219c8431410564bb69312f5a7a46d872f1e828082b9a5`  
		Last Modified: Wed, 28 Jan 2026 02:33:55 GMT  
		Size: 44.4 KB (44390 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; arm variant v6

```console
$ docker pull postgres@sha256:4f3a2c8e4852035803a9457bed2d58c302026293f08aa0e6ab097f1b232887ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88622149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b73506aa096b61e26c3307de32b9f8cd28fa089fa597eaa89d98d3fd667e7deb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:49:36 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:49:41 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:49:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:49:41 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:49:41 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:49:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:49:41 GMT
ENV PG_MAJOR=15
# Wed, 28 Jan 2026 02:49:41 GMT
ENV PG_VERSION=15.15
# Wed, 28 Jan 2026 02:49:41 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Wed, 28 Jan 2026 02:49:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:52:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:52:28 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:52:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:52:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:52:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:52:28 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:52:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:52:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:52:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:52:28 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:52:28 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:52:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600d725268a4338768932157ca128e9199efb5bcf755cca53e05fb2a4a0c629a`  
		Last Modified: Wed, 28 Jan 2026 02:52:38 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efbb9f0dca126a706c51c20b265a0ef87d7d0494330a2cddeef41d2c4c2dc3a`  
		Last Modified: Wed, 28 Jan 2026 02:52:38 GMT  
		Size: 889.5 KB (889466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e331ba9868504a8f97ac013ec086607921cdf84037943e08c3808e3081e3f564`  
		Last Modified: Wed, 28 Jan 2026 02:52:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e296756c03ddcebb8fbedc6dce257273f98da3e8065a2edaef2a7dda39d12a0`  
		Last Modified: Wed, 28 Jan 2026 02:52:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9e58f8a1e9747cbf212fc477d50e34d111f1a6ff2a197099e08ad509594fb8`  
		Last Modified: Wed, 28 Jan 2026 02:52:42 GMT  
		Size: 84.1 MB (84145839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ece84f2ac4033f60dac537b03d3213bf68beaeb2b8ae95b2ef0a9b0846e1e8`  
		Last Modified: Wed, 28 Jan 2026 02:52:39 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a314b4cd0d0dc6fa7fcbba54c56c71b428e7d457beae7a9d89567c915f4da118`  
		Last Modified: Wed, 28 Jan 2026 02:52:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51835ea9eea5ee2572ce59604e4f7d429672e3b2715be8b42d1b96058197a0f9`  
		Last Modified: Wed, 28 Jan 2026 02:52:39 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddb470e82602e9a04aa22da642ed98f19743aa4e17aaec8b417a946c30ec5c2`  
		Last Modified: Wed, 28 Jan 2026 02:52:40 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f0cd6ac7b72801886a294c5694bed3082c60ff78d3cd341e348bfe9c0f071a`  
		Last Modified: Wed, 28 Jan 2026 02:52:40 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:6f8c042cdb0b8b34d28ce6fe89bd2906aac197b69c95ffac073ce5110779426d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 KB (44353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c756c312c082c8ec6359ff3648b31dd366687370a728488501b79ab86410dc`

```dockerfile
```

-	Layers:
	-	`sha256:ce0f05cec9f7eee3aef62d3e524d55e87539ed95d7acf3a5e58fa4149a225e6a`  
		Last Modified: Wed, 28 Jan 2026 02:52:38 GMT  
		Size: 44.4 KB (44353 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; arm variant v7

```console
$ docker pull postgres@sha256:6563e3c69e35cffd623ff8c86fe1aeb35320955ab1f04f8aa764e661a6eb77ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83875682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f2e5b534154ee85632254b9442781e273cb870dba4bc343a152031da61170a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:48:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:48:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:48:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:48:49 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:48:49 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:48:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:48:49 GMT
ENV PG_MAJOR=15
# Wed, 28 Jan 2026 02:48:49 GMT
ENV PG_VERSION=15.15
# Wed, 28 Jan 2026 02:48:49 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Wed, 28 Jan 2026 02:48:49 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:51:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:51:33 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:51:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:51:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:51:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:51:33 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:51:33 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:51:33 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:51:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:51:33 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:51:33 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:51:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d0537fd222a02838512136f291876a3fcaadd41b8252d5ce610d868469974a`  
		Last Modified: Wed, 28 Jan 2026 02:51:44 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4a1f7e272071802e0a432c517919d8a385db85c3eb0e36c77126c8b5d940ee`  
		Last Modified: Wed, 28 Jan 2026 02:51:44 GMT  
		Size: 889.5 KB (889506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f740d7031255a4c4cd491176450a2a04a6417ebf17908908a7f232c25e181986`  
		Last Modified: Wed, 28 Jan 2026 02:51:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28502cfba2a5eed491a2c109bbf4562b206b9db2f65e7cbfc68498d1a9993ef3`  
		Last Modified: Wed, 28 Jan 2026 02:51:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa735e74852f03fc3fd7a4e604cedf46ae485000bac2741d15c4e83f98295e7`  
		Last Modified: Wed, 28 Jan 2026 02:51:48 GMT  
		Size: 79.7 MB (79687427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46336c08f5ed2c02ac041a3dc9b6434ead21a09862ac284060cadb6855397146`  
		Last Modified: Wed, 28 Jan 2026 02:51:46 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe975686cd54316bd476663f86da40de05088f5227fa5448c56db1075f7259b4`  
		Last Modified: Wed, 28 Jan 2026 02:51:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544ce3829ae5fddb3b265a034c133dd42f799d648e3490da293db609edaf5fde`  
		Last Modified: Wed, 28 Jan 2026 02:51:46 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66717852df21c95e1834edd83387e401e5fd6aa5b14b782030c597b6f1666bf`  
		Last Modified: Wed, 28 Jan 2026 02:51:47 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f07f619e2690b7a565405ef1ea0b9cf8f858f036bfd8b2428832360147cbe3b`  
		Last Modified: Wed, 28 Jan 2026 02:51:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:3d8ec1daab88bfcbbf448e03710b83124b1c362f1238af4314437c4abb5adbb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.0 KB (642034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c928a0f3b489c7b029998a6804b5e87466ad3b44ca596178818d5539bf85aea9`

```dockerfile
```

-	Layers:
	-	`sha256:eac46c63bee0080f86601372ef75d847b9fadd9352dc365e57175f1f25bcbf20`  
		Last Modified: Wed, 28 Jan 2026 02:51:45 GMT  
		Size: 597.5 KB (597466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d8679fcf50c194eb5cae8830ced8f0aec395f09058560ecf3f536aa9d9f05a9`  
		Last Modified: Wed, 28 Jan 2026 02:51:44 GMT  
		Size: 44.6 KB (44568 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:39a18bf1bbdd8847f59e9600a93668f05b1a2fee2aa117247dbff364b1dd65ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107327137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1cea2bd5aad2ca33e92c198cc31364ceb37b09dfc651ad5875cb0633ac76af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:31 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:33:33 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:33:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:33:33 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:33:33 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:33:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:33:33 GMT
ENV PG_MAJOR=15
# Wed, 28 Jan 2026 02:33:33 GMT
ENV PG_VERSION=15.15
# Wed, 28 Jan 2026 02:33:33 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Wed, 28 Jan 2026 02:33:33 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:35:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:35:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:35:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb300e14466056f94423fe5583f4e0443158110305b092df8b671e1c84b99ab`  
		Last Modified: Wed, 28 Jan 2026 02:35:56 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642323d6fae974314b1db912b9e867d51a1759a13975cd0e968b4b3ac1f5dc4a`  
		Last Modified: Wed, 28 Jan 2026 02:35:56 GMT  
		Size: 876.5 KB (876483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b3053082e26c5a09d2f36fe092a30866c15b900cf431de55a42d82a9524825`  
		Last Modified: Wed, 28 Jan 2026 02:35:56 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0274aabf5cd76e60e386002a7e6a6c9fe688ffa4e41a0ebb64ec76b7810ea560`  
		Last Modified: Wed, 28 Jan 2026 02:35:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508ee5a299dd0c118a9c027abc0814fda3556c0f0abe48b20de80bb7af6dd94e`  
		Last Modified: Wed, 28 Jan 2026 02:36:00 GMT  
		Size: 102.2 MB (102236543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6308017104a57a21e2936c933029180034cc608042fb8799672a441a1ba844d`  
		Last Modified: Wed, 28 Jan 2026 02:35:57 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87dec2449d1336f35afa8ca9dc0af85af948e13ba2865d02d3ef93a39f92df4`  
		Last Modified: Wed, 28 Jan 2026 02:35:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126a4895c4489b72858390266c93ded13d001a2c8c2983145d3010cde5b8b7b5`  
		Last Modified: Wed, 28 Jan 2026 02:35:57 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7ea63ba22fc1a8ccbebecdfaa7e6cd95c6fc78bcb76c7a5646713b2fdfaf9a`  
		Last Modified: Wed, 28 Jan 2026 02:35:59 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b39af891d6fecd5c90ff4a83cea5d018f102c27518df7d9291050a3610b6ec2`  
		Last Modified: Wed, 28 Jan 2026 02:35:59 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:0e0aa6bd60ff933e11b3b82ac25b3aeafb3c078db41e339a49d53288b4db07e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.1 KB (642100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5cd3f68208615ff6be9ceb6613c98d05f13eb705db45c00d5bda0cfa99b1d2`

```dockerfile
```

-	Layers:
	-	`sha256:534bab9085f2ebe904d321d295aa7943067c08a88bf016e5d910e225bc6cc27c`  
		Last Modified: Wed, 28 Jan 2026 02:35:56 GMT  
		Size: 597.5 KB (597486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfc4caf6affea2a231cd27cdd47996b5fa535bb60cd5e7a9b02182322655fcdc`  
		Last Modified: Wed, 28 Jan 2026 02:35:56 GMT  
		Size: 44.6 KB (44614 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; 386

```console
$ docker pull postgres@sha256:2ce6c151de74efb99a92ff7dbc261ced08378065061e1acf726634373b8a7d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115189412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0fd6082f0989c32833cb4e024d3603332a482a50d23c199d7859c73c6c02c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
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
ENV PG_MAJOR=15
# Wed, 28 Jan 2026 02:27:57 GMT
ENV PG_VERSION=15.15
# Wed, 28 Jan 2026 02:27:57 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Wed, 28 Jan 2026 02:27:57 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:30:21 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:30:21 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:30:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:30:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:30:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:30:21 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:30:21 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:30:21 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:30:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:30:21 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:30:21 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:30:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88845e232fe79b29e1b11f6058c3229423b055551a37fd416181ab29b6d9ed36`  
		Last Modified: Wed, 28 Jan 2026 02:30:37 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace72bda8b49ae967cb04bf40b33d62e132cc95d640f04648b67198024338a93`  
		Last Modified: Wed, 28 Jan 2026 02:30:37 GMT  
		Size: 893.3 KB (893255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660ec567e9958d7f19324d9fe73c22bcc14054382f2beb137e91fb6e4bdf1e9f`  
		Last Modified: Wed, 28 Jan 2026 02:30:36 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58de2ded5529ce062b3a0f29b6c058600b95c80629a35dc4d4b0f0e1a9b0e2b`  
		Last Modified: Wed, 28 Jan 2026 02:30:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0035684cee0c31245c5901222b30467a22686cc210598d215e134726ba75b1`  
		Last Modified: Wed, 28 Jan 2026 02:30:40 GMT  
		Size: 110.6 MB (110592138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8a2c57d95c78d3d6dd7a6f34691878b4e1f16e51f23849c215b93d156d512f`  
		Last Modified: Wed, 28 Jan 2026 02:30:38 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574815305e066a545e36fc6c3e5a7fccb3a277b4f985e909a766c6676ca17da`  
		Last Modified: Wed, 28 Jan 2026 02:30:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e9baa3f4fb0a18ca350fa648a2543bfa3c9bc3081883450574775b9cad8d48`  
		Last Modified: Wed, 28 Jan 2026 02:30:38 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d9008d544ef6ebb9cdb0f064c2f161c823c4cbdf889d15050c76a2aa08942e`  
		Last Modified: Wed, 28 Jan 2026 02:30:39 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad64519f845e95cead8875a6bfffd613f60ead83b31379f446b319040d9d04f6`  
		Last Modified: Wed, 28 Jan 2026 02:30:39 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:38a249c8d46398554d81157281969285e4235772161bff3c88d4dbc0f27479e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b8498a7ec2b19a99b73e8996103ca68c245b492a2443f3e9a6e24007aa3ba4`

```dockerfile
```

-	Layers:
	-	`sha256:eab57bda02fea52497911503fce15b139d83a1d20b667066b1e33e6c697da888`  
		Last Modified: Wed, 28 Jan 2026 02:30:37 GMT  
		Size: 598.1 KB (598055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97425792046ae594dded0a39a21ae997849149cd81eec7585a3ef430e51eaa08`  
		Last Modified: Wed, 28 Jan 2026 02:30:37 GMT  
		Size: 44.3 KB (44342 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; ppc64le

```console
$ docker pull postgres@sha256:34ef92a70d0958d179917b0ee4449b1f6a2e9350235ba7be1a37d38ba3ba6f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94021368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295e1d13564db0d780db5e0393bf7e07a8926ec8c7cf215df5114563057322b1`
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
# Wed, 28 Jan 2026 03:40:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 03:40:28 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 03:40:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 03:40:29 GMT
ENV PG_MAJOR=15
# Wed, 28 Jan 2026 03:40:29 GMT
ENV PG_VERSION=15.15
# Wed, 28 Jan 2026 03:40:29 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Wed, 28 Jan 2026 03:40:29 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 03:47:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 03:47:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 03:47:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 03:47:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 03:47:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 03:47:33 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 03:47:34 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:47:34 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 03:47:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:47:34 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 03:47:34 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 03:47:34 GMT
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
	-	`sha256:77cf74e995b3eb5bda2a0a5450ee9699ea1b33c26c2df9881fa295efba513429`  
		Last Modified: Wed, 28 Jan 2026 03:44:00 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1825ae71f923b564d2d7e0d2c089aa9e2ba51c8a6ac633c77b1b1881c2d2991`  
		Last Modified: Wed, 28 Jan 2026 03:44:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84250a31428aa73c56dbb1b13495a1368feffd64d00f11701bd55fef35f15de6`  
		Last Modified: Wed, 28 Jan 2026 03:48:12 GMT  
		Size: 89.3 MB (89293146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab0c4736cb57c81278fc434aaf0531e2c782acd7a930af1c8b283e7a43c5848`  
		Last Modified: Wed, 28 Jan 2026 03:48:10 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c139dd626991305623a6dc47f82d444761d1161caae733bd4f75d1529160b033`  
		Last Modified: Wed, 28 Jan 2026 03:48:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e813ddbed114042ad0679a2c2318e39ff4fa1d0059bcf644865a96d3307f27`  
		Last Modified: Wed, 28 Jan 2026 03:48:10 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c45c0f6e70694e68d90031b815c5e3f1ac6d6abe532470c5563eb8d0510cf97`  
		Last Modified: Wed, 28 Jan 2026 03:48:11 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f1a0aa898d08e295761099ea1c6f47ccbdb4f83ac99d4daa3607254f1b8c19`  
		Last Modified: Wed, 28 Jan 2026 03:48:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:572e62049afa812771d78f1bb544b2fd0ccacdcd212dbaba439e054505b2b0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ebb812865010ffc9c1e8baac470ceeb16999f28a6d5394e71216ac5a6cd987`

```dockerfile
```

-	Layers:
	-	`sha256:5e3292ad618042ab998ffaa065c66c38fb4bbc814e196af7ccbbeb2e6d8455f9`  
		Last Modified: Wed, 28 Jan 2026 03:48:10 GMT  
		Size: 595.8 KB (595801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d94fdb4186d8744cd862107b779a7835288d4cd0db8ece6f290c76aa16e6761`  
		Last Modified: Wed, 28 Jan 2026 03:48:10 GMT  
		Size: 44.4 KB (44444 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; riscv64

```console
$ docker pull postgres@sha256:8babeddff7647f6d07bb8f1727cc89004220549a7f2edda361b30b26400d2e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110132374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e45a15c7acb395277958d6cab669e51bb3bbe30f2627487a7dd5f925b3fdf4`
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
# Thu, 29 Jan 2026 11:51:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 29 Jan 2026 11:51:24 GMT
ENV LANG=en_US.utf8
# Thu, 29 Jan 2026 11:51:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 11:51:24 GMT
ENV PG_MAJOR=15
# Thu, 29 Jan 2026 11:51:24 GMT
ENV PG_VERSION=15.15
# Thu, 29 Jan 2026 11:51:24 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Thu, 29 Jan 2026 11:51:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 29 Jan 2026 14:25:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 29 Jan 2026 14:25:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 29 Jan 2026 14:25:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 29 Jan 2026 14:25:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 29 Jan 2026 14:25:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 29 Jan 2026 14:25:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 29 Jan 2026 14:25:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 14:25:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 29 Jan 2026 14:25:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 14:25:58 GMT
STOPSIGNAL SIGINT
# Thu, 29 Jan 2026 14:25:58 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 29 Jan 2026 14:25:58 GMT
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
	-	`sha256:dd2af884a78cd745810524cf78c71299e5b3366ea20a67f8f2c389eb89733245`  
		Last Modified: Thu, 29 Jan 2026 12:44:16 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872215ae444a1f98c781e47b6707e84469163acaf547daf5e834c4582afe9beb`  
		Last Modified: Thu, 29 Jan 2026 12:44:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6c4415b5ddd6511f966a66df3a3a13a7f00c5bdeea7b8bd120bd2fd3e1d597`  
		Last Modified: Thu, 29 Jan 2026 14:29:07 GMT  
		Size: 105.7 MB (105661112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c2404a1991fa88ba0c612cfa30c262dae89116f6dc0792b87f6ad4e72569db`  
		Last Modified: Thu, 29 Jan 2026 14:28:50 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e09bfe11b733e49119a0fc74f01e1725208cd13ef7ea8a1cd2e1491f1a4436`  
		Last Modified: Thu, 29 Jan 2026 14:28:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ff11cbcd7e4c735ea891392b0185b53b67363d55c219b519d827c70ad4163a`  
		Last Modified: Thu, 29 Jan 2026 14:28:50 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9beb1abbaeeccfc699659ae76ca23382e19e61d2a11905886dca404db2677ae`  
		Last Modified: Thu, 29 Jan 2026 14:28:51 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c0c433f7495e3c2f3f8152ed9f635200598d3b23bccdeb660b338bd9203139`  
		Last Modified: Thu, 29 Jan 2026 14:28:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:af698ac332cf30480432de54b0de9c2fc2acdc774f837979f67e4268c2c917ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.9 KB (641909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098063d0cebc54bac8dae08fc7fbb416e2392891f52fa068dc223cf3f3c3a1a7`

```dockerfile
```

-	Layers:
	-	`sha256:c7ebc0a45da953d0a7a9d82c45c85369d69b5bd3c50b17c4062bd726f780e150`  
		Last Modified: Thu, 29 Jan 2026 14:28:50 GMT  
		Size: 597.5 KB (597459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9366ace4c30aaac7c72bfba226b2457b363558c16f7fe8fb7f7f541c73b61c23`  
		Last Modified: Thu, 29 Jan 2026 14:28:50 GMT  
		Size: 44.5 KB (44450 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; s390x

```console
$ docker pull postgres@sha256:9d57b5bde890b623bdc8efda553b685fd90cae483565a106f1b442a620b4660c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117279909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2c358d2602cd71c895092f3bb7bd1fcd18297272ccd29b8c4322c6b8b6a2cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:49:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:49:28 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:49:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:54:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:54:14 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:54:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:54:14 GMT
ENV PG_MAJOR=15
# Wed, 28 Jan 2026 02:54:14 GMT
ENV PG_VERSION=15.15
# Wed, 28 Jan 2026 02:54:14 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Wed, 28 Jan 2026 02:54:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:59:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:59:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:59:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:59:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:59:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:59:44 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:59:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:59:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:59:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:59:44 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:59:44 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:59:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fbf24c2e83b9c01201ca76d0a4e3840b930d1d881ebfeed131e53116c28472`  
		Last Modified: Wed, 28 Jan 2026 02:53:09 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c1d356a9c7ec6c78f8eea92af3e68a6942fdcbf19e4d27ae4133bc86433924`  
		Last Modified: Wed, 28 Jan 2026 02:53:09 GMT  
		Size: 897.4 KB (897413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9070c8bfee140bc1c3f07a7f5a2bacf57b95afb77d2012a1e323964d38d691a`  
		Last Modified: Wed, 28 Jan 2026 02:57:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c417c9a2756a305f8aea6dcf5a2317eec0ae1eccfa3857434847510b425e09`  
		Last Modified: Wed, 28 Jan 2026 02:57:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b05e6cd30295aafa2995f344234e2d04b4af95ee67d0b1b1eb7afcf4196b12e`  
		Last Modified: Wed, 28 Jan 2026 03:00:14 GMT  
		Size: 112.6 MB (112640135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245089c06c4f86e415c722cf055df1363fa43505b2d44b3af610a60b2e2eb679`  
		Last Modified: Wed, 28 Jan 2026 03:00:11 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ef2bfc4d6a63d3507fcce61c530d8a6fbf2bf5bbc78340f386a7673ac048b9`  
		Last Modified: Wed, 28 Jan 2026 03:00:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a626d076e85fd06e5314b1b6e5d7da2af6a2eba2f1f2be8a7b2fb969719f1a`  
		Last Modified: Wed, 28 Jan 2026 03:00:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6438a9088ea86f82c0c9ecc606ec6afe05245e1368c7986f6ddd6a314e346a`  
		Last Modified: Wed, 28 Jan 2026 03:00:15 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3489002e72346e01c7ace50f9b9c8450a25c757f9f1c6605c04e8402c2c982cb`  
		Last Modified: Wed, 28 Jan 2026 03:00:15 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:3587176ade6d639b7050cfe495bf71798af12fbacf7962a96ffa0d608f5ae959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 KB (641819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b7ffc6148c05875a904e0c6c655c12eaec45d5c754a14eed955148a744ae7e`

```dockerfile
```

-	Layers:
	-	`sha256:069d99d4915cd49ba1e56b4aff5b7290a276288c19a4d828f981619b39c8edc7`  
		Last Modified: Wed, 28 Jan 2026 03:00:10 GMT  
		Size: 597.4 KB (597429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4252ee1c0e076b14747170baa8ae4d71c829129cdee0a5e292b37c2e7fd92695`  
		Last Modified: Wed, 28 Jan 2026 03:00:13 GMT  
		Size: 44.4 KB (44390 bytes)  
		MIME: application/vnd.in-toto+json
