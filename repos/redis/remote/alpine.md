## `redis:alpine`

```console
$ docker pull redis@sha256:6cbef353e480a8a6e7f10ec545f13d7d3fa85a212cdcc5ffaf5a1c818b9d3798
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

### `redis:alpine` - linux; amd64

```console
$ docker pull redis@sha256:8360960f5fb56a282d78686203dd875862cd4b52a4184c17ac753690252d6d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33374981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778c3ea605c2c786ad6f7b9efe50c065903b1b4c7a4f5b2c6d76507b01402470`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 21:47:58 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 18 Nov 2025 21:47:58 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 18 Nov 2025 21:54:28 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Tue, 18 Nov 2025 21:54:28 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Tue, 18 Nov 2025 21:54:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang-static 		clang-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 18 Nov 2025 21:54:28 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 18 Nov 2025 21:54:28 GMT
VOLUME [/data]
# Tue, 18 Nov 2025 21:54:28 GMT
WORKDIR /data
# Tue, 18 Nov 2025 21:54:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 21:54:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 21:54:28 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 18 Nov 2025 21:54:28 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84a6e003d260521e9b2ecb4cdfe80b7fd68dcb5f0bff54b249b6008e157982c`  
		Last Modified: Tue, 18 Nov 2025 21:54:45 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a229eaa0f8a70b83eb3c40f8adc81d4ad54a3e1835a982d2473b269ae7f7dfc`  
		Last Modified: Tue, 18 Nov 2025 21:54:43 GMT  
		Size: 197.0 KB (197005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362eff98b603cadcb31ab0031a47f64fbcf99b9a52045dd55e050c271cdaa5d3`  
		Last Modified: Tue, 18 Nov 2025 21:54:49 GMT  
		Size: 29.4 MB (29372339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793133e9ba6b86a5ffc07e338aaf08216c0479293d1e75846f2cf6b894bb9a41`  
		Last Modified: Tue, 18 Nov 2025 21:54:43 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffa735aaa172bb794d6ae16ec9f9f31fae4e8d1616522d985a732e4dee06622`  
		Last Modified: Tue, 18 Nov 2025 21:54:43 GMT  
		Size: 2.1 KB (2103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:b0e6e976e3027fd08225c1ceb5487371e37bddc0a94d790152bc350ac367f412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.3 KB (501253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86bcb8a38805a1353c10728bffc3b4efaab24d293d4fa4397499b572e79eb569`

```dockerfile
```

-	Layers:
	-	`sha256:be1e78058b83cb842db9fa06333b1a11d4ff071ff071830b7ab5ff085309e8db`  
		Last Modified: Tue, 18 Nov 2025 23:06:08 GMT  
		Size: 468.9 KB (468932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:726d7aa6192d0eb2f90fc1ab03de58ed9d59e4f300e272737aaad48cc6f59a10`  
		Last Modified: Tue, 18 Nov 2025 23:06:09 GMT  
		Size: 32.3 KB (32321 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:1164d3c032eb56b96f54d3fccb9407a75e01cf9238ee428c6bea6b395d2d7017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18305300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d136e565c746e26dba600462218c065417a6ebc7b0f2cfc8b61c7a1e7846cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:59:13 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 18 Nov 2025 19:59:15 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 18 Nov 2025 20:00:11 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Tue, 18 Nov 2025 20:00:11 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Tue, 18 Nov 2025 20:00:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang-static 		clang-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 18 Nov 2025 20:00:11 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 18 Nov 2025 20:00:11 GMT
VOLUME [/data]
# Tue, 18 Nov 2025 20:00:11 GMT
WORKDIR /data
# Tue, 18 Nov 2025 20:00:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 20:00:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 20:00:11 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 18 Nov 2025 20:00:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7d70b0fd8175a26f4fd8977dd9d3aa5632cb222e59e9181a5b2d0012c4e012`  
		Last Modified: Tue, 18 Nov 2025 20:00:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ad4bac946dd5fab1aa9e3d529af3cd22b1e90c9ec2b73da736950774fe468b`  
		Last Modified: Tue, 18 Nov 2025 20:00:48 GMT  
		Size: 197.2 KB (197183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36dc80c6f12f3994cd2abbd63a0981327914a91ee81fe0aa9a387ef3743f0fbd`  
		Last Modified: Tue, 18 Nov 2025 20:00:48 GMT  
		Size: 14.6 MB (14600850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89651c527f03243860b393672cad02a59eb18e099bc7a1d328e1a91317b3ce0`  
		Last Modified: Tue, 18 Nov 2025 20:00:47 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52875b07bfabd02ce97728b83982d8fae613dd90584dca441571ace0081526f0`  
		Last Modified: Tue, 18 Nov 2025 20:00:46 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:184f0a9522b35ee398f7f103adcac1cd60e6c4f55e37c7a65c5eb9bb7dd5eb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0655712ec27bc90c70a12fe5d0b59590f5e3051e339f57bd35695b572e3f7a6c`

```dockerfile
```

-	Layers:
	-	`sha256:c3f18c48b1ad5ea9134f3da5d5f933780be8b826d2f0596214ead99c30245d10`  
		Last Modified: Tue, 18 Nov 2025 23:06:13 GMT  
		Size: 32.3 KB (32254 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:9de991e203a8c0452aa3883fe26316053343b85031787d8e832fa01fe3f9f8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17790082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95cc584c23168af8171f50868617dc8d4c2286a8c433a6046b5058324ae54bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 20:01:15 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 18 Nov 2025 20:01:16 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 18 Nov 2025 20:02:11 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Tue, 18 Nov 2025 20:02:11 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Tue, 18 Nov 2025 20:02:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang-static 		clang-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 18 Nov 2025 20:02:11 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 18 Nov 2025 20:02:11 GMT
VOLUME [/data]
# Tue, 18 Nov 2025 20:02:11 GMT
WORKDIR /data
# Tue, 18 Nov 2025 20:02:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 20:02:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 20:02:11 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 18 Nov 2025 20:02:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82902211152efe876a9de57f932dedc820a1de03409adc9e3b8da67f348aee8`  
		Last Modified: Tue, 18 Nov 2025 20:02:28 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8354438f957b061d34a5dedf5acb43fb0bdb3e1194d8f5fcbcee9bb4bd709fbb`  
		Last Modified: Tue, 18 Nov 2025 20:02:28 GMT  
		Size: 195.6 KB (195567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e3e2625e4b47ab2d240e6f7754dcb09f78fa20e4aabc32ba442c2c904b5c55`  
		Last Modified: Tue, 18 Nov 2025 20:02:30 GMT  
		Size: 14.4 MB (14369774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2da809e14c31d8cf195e8b455c059d01eadf157b8702fbcadf3226e21dd8ce`  
		Last Modified: Tue, 18 Nov 2025 20:02:28 GMT  
		Size: 98.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3fefcc30b12b9072552c814f4c36567449b953cf9ea050a0891e0fd1b0e8d8`  
		Last Modified: Tue, 18 Nov 2025 20:02:28 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:b9b977efbcfa6d821ed365c6554c16889b11f39117dee2282d6cd1115f6a84ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.5 KB (501469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4574b8eb85d9b5334f7c3156c680e5ec33c7a964255411e93c70a0c3aa347d`

```dockerfile
```

-	Layers:
	-	`sha256:f45305bee03845b2e7902d4b8a5914cb16371f2af6d661e2a853d021ae4b2271`  
		Last Modified: Tue, 18 Nov 2025 23:06:16 GMT  
		Size: 469.0 KB (469000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1aef1ea782de65e30ce2a3cfb768644b1db4326c51c34f25f9d092c230aa9dd`  
		Last Modified: Tue, 18 Nov 2025 23:06:17 GMT  
		Size: 32.5 KB (32469 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:1023a5ac993a92700157e724a9aa077428b9f5d1ef54f0ab1aa5e74371eab6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33268826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733d545e87b547f001d2a7965cb668561dd4e92751f84c519c8b6892c4162961`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 20:02:35 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 18 Nov 2025 20:02:36 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 18 Nov 2025 20:09:30 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Tue, 18 Nov 2025 20:09:30 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Tue, 18 Nov 2025 20:09:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang-static 		clang-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 18 Nov 2025 20:09:30 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 18 Nov 2025 20:09:30 GMT
VOLUME [/data]
# Tue, 18 Nov 2025 20:09:30 GMT
WORKDIR /data
# Tue, 18 Nov 2025 20:09:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 20:09:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 20:09:30 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 18 Nov 2025 20:09:30 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3e85348d1524ee75ee16ea693b051e47a77cf7bfc2fd5fb21474f22f1d7ee6`  
		Last Modified: Tue, 18 Nov 2025 20:10:12 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e748fe7e898af4bba0af4ecc768150ae7883bf856f039c2c1051c47bb032a61`  
		Last Modified: Tue, 18 Nov 2025 20:10:12 GMT  
		Size: 198.9 KB (198904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0abe8c185e79f4788817e25569e9b70ecb3d192996c09a18290cbb77f51b923`  
		Last Modified: Tue, 18 Nov 2025 20:10:17 GMT  
		Size: 28.9 MB (28928670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d7a3e38cc296564e247ed12159d54a7ecdd0725b4664fe6d4f70420fa41523`  
		Last Modified: Tue, 18 Nov 2025 20:10:12 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e9d7d40e446acd1c87bc032302c12d6f69eb8ee0006879fb2be002ac7278db`  
		Last Modified: Tue, 18 Nov 2025 20:10:12 GMT  
		Size: 2.1 KB (2103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:b2a4308480d9019d50fbcece08bb7dec94137971137508188d558d9c3758de55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.6 KB (501551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ce2d4020a4a52e548580598bfbccaed1fb492b7eb55d438f9c0ec082eeb4d9`

```dockerfile
```

-	Layers:
	-	`sha256:62039f45610fe59d316b449851b19d3f779f0a0a91db7b636c06aff76bb5c104`  
		Last Modified: Tue, 18 Nov 2025 23:06:20 GMT  
		Size: 469.0 KB (469036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2704dacd6f2ed588b99f69ca34dd7acf611ff75e11dc13cf2f6031e26857b9db`  
		Last Modified: Tue, 18 Nov 2025 23:06:21 GMT  
		Size: 32.5 KB (32515 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; 386

```console
$ docker pull redis@sha256:fdc214182f977643f50ac20cfff2a2c92aa60a8875e956c1dc1aeaca4a4ac982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18197712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5659bf9fb369b6dec5d50282ade11334a09b21ae4d027f03815a37d0af5340ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 20:02:34 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 18 Nov 2025 20:02:35 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 18 Nov 2025 20:03:25 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Tue, 18 Nov 2025 20:03:25 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Tue, 18 Nov 2025 20:03:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang-static 		clang-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 18 Nov 2025 20:03:25 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 18 Nov 2025 20:03:25 GMT
VOLUME [/data]
# Tue, 18 Nov 2025 20:03:25 GMT
WORKDIR /data
# Tue, 18 Nov 2025 20:03:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 20:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 20:03:25 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 18 Nov 2025 20:03:25 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387a9572358fa329e493cbfdadbf0179372eba8cf1a6a3b5f1d99fa6a860b116`  
		Last Modified: Tue, 18 Nov 2025 20:03:41 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e09ddf82e6d65a2a4d82ec8eda49a687d9cb8234f1cda93374c1489d0e9eb47`  
		Last Modified: Tue, 18 Nov 2025 20:03:41 GMT  
		Size: 197.4 KB (197409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0679f9ac2c98c13411c9e7a7584ea116dc5605b15aa26faaee4e6a306b4966d5`  
		Last Modified: Tue, 18 Nov 2025 20:03:43 GMT  
		Size: 14.4 MB (14378185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c4ca844c3e164d350eb2bb01137d53c09b02835973974952c140b596523a38`  
		Last Modified: Tue, 18 Nov 2025 20:03:41 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bf4ff37697d14f01eb2d75cbc2cbc2fc36614e4ae4aac25674e498d0f4bcec`  
		Last Modified: Tue, 18 Nov 2025 20:03:41 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:0a787c5e4787b76942bd9e808f4e82a46999c8c9856e72372b0a5c585e89a32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.1 KB (501147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b37891e3c44d4e878845fefff9a5e81db94fbefa51ed5184cec792b6f2aff7`

```dockerfile
```

-	Layers:
	-	`sha256:423ba0caa0b77c2160cfab8bcd9b253705dc290db9d3bc56099bcf1d11ccd6d0`  
		Last Modified: Tue, 18 Nov 2025 23:06:25 GMT  
		Size: 468.9 KB (468887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9355a6510242be37286ab24f78baf9e5d544a735032690b29481ca09749dacb5`  
		Last Modified: Tue, 18 Nov 2025 23:06:25 GMT  
		Size: 32.3 KB (32260 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:d50a0db24f920ef7810e43a925969a0fb1b3d7664583a448bc3aa4a449fe7b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19556058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3123f0c5a167ada25c9794fc2d4d17cd095da88283f4d75263eea8ddecf58f44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 22:00:43 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 18 Nov 2025 22:00:46 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 18 Nov 2025 22:01:44 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Tue, 18 Nov 2025 22:01:44 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Tue, 18 Nov 2025 22:01:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang-static 		clang-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 18 Nov 2025 22:01:44 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 18 Nov 2025 22:01:44 GMT
VOLUME [/data]
# Tue, 18 Nov 2025 22:01:44 GMT
WORKDIR /data
# Tue, 18 Nov 2025 22:01:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 22:01:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 22:01:45 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 18 Nov 2025 22:01:45 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cda4e71ca47a70bac24076717184b74f8187fa10cb9accfea4e46266ec8b62`  
		Last Modified: Tue, 18 Nov 2025 22:02:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9f8e11ca7476a17dae74a49d2ce7504e980513fa81a9b31be1e75f4d9d161c`  
		Last Modified: Tue, 18 Nov 2025 22:02:03 GMT  
		Size: 199.9 KB (199919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec334a8f6257c91773b79a8f6054dabd5b195e4701beca7fdda210390b2b751a`  
		Last Modified: Tue, 18 Nov 2025 22:02:06 GMT  
		Size: 15.6 MB (15620708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef6d9fbdd59ab6107e918d21fbdf38ece4676fdef865cd2b5c9c26fbab83f0d`  
		Last Modified: Tue, 18 Nov 2025 22:02:04 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ffda8d4ea5cc2b17ceb5b7372ca89feba3c1c475967832d236c3512a1c93e5`  
		Last Modified: Tue, 18 Nov 2025 22:02:04 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:84291b364db48f96abb2140b8758b8fe4b54b7e319d8d21448162e47e601a762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.4 KB (499434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5401fe5b32776fb633eac6b5bd152300ffa2fc8a036c33144f27c4f99532a78e`

```dockerfile
```

-	Layers:
	-	`sha256:b72738ea6b4ffed82ad95edeaeee1df2bde9b44cc3c12cf432d97882696bb520`  
		Last Modified: Tue, 18 Nov 2025 23:06:29 GMT  
		Size: 467.0 KB (467039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3946df10c779a1728ba019834f10dd1f3752d8a8557d38d0c6f7d2c43bd1d838`  
		Last Modified: Tue, 18 Nov 2025 23:06:30 GMT  
		Size: 32.4 KB (32395 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; riscv64

```console
$ docker pull redis@sha256:5dd166a5d3b96f3bfd9d0c2c3df36af03903ace238862f60c3faef5f7abc722d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17780071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490fbc0a28d1829b39bb4eb7e2b26b35394b78f7cc29f58f7f65a4de50a84919`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:26:52 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 20 Nov 2025 19:26:57 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 20 Nov 2025 19:43:37 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Thu, 20 Nov 2025 19:43:37 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Thu, 20 Nov 2025 19:43:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang-static 		clang-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Thu, 20 Nov 2025 19:43:37 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 20 Nov 2025 19:43:37 GMT
VOLUME [/data]
# Thu, 20 Nov 2025 19:43:37 GMT
WORKDIR /data
# Thu, 20 Nov 2025 19:43:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:43:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Nov 2025 19:43:37 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 20 Nov 2025 19:43:37 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610796487a2bfdffd8e447ac998c8a9a6a07b7cd242fd5e55b41d1a05fc1e7`  
		Last Modified: Thu, 20 Nov 2025 19:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1fa0f886f866d1448b1d3f46b5f714e2ca04c81fd64f404e8533fba118c12b`  
		Last Modified: Thu, 20 Nov 2025 19:44:32 GMT  
		Size: 197.1 KB (197098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef6c89cbb5768eae195de2d8235d40c79692589d004c03bf3dbef125e3beeea`  
		Last Modified: Thu, 20 Nov 2025 19:44:34 GMT  
		Size: 14.1 MB (14064540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ac15ebe764b65611f2c0bb1b375fc96180ac0255971f82eddcfbe8063e6eae`  
		Last Modified: Thu, 20 Nov 2025 19:44:32 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaefbf71c37a6fd923559a768969527950d619c46756c96a17c1c89b1d185bb`  
		Last Modified: Thu, 20 Nov 2025 19:44:32 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:7446fe836d1dcc073a4204465f7f73d4ab95a0d6c0d8f3abeaabd18b4f0578a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.4 KB (499430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4fcc2224802fa9559e734ea0644f740a95a1f137556ac197d0ce57005a7275`

```dockerfile
```

-	Layers:
	-	`sha256:f76d47efdb3248625935e744952490a24577dbb277b6f2d0e7a1a9cde345da25`  
		Last Modified: Thu, 20 Nov 2025 20:06:39 GMT  
		Size: 467.0 KB (467035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a8790352e6cca30577214eb005e0b72bdc39969e692a3529d26e7f4985f55ac`  
		Last Modified: Thu, 20 Nov 2025 20:06:40 GMT  
		Size: 32.4 KB (32395 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; s390x

```console
$ docker pull redis@sha256:6473631e158db73948b3704b333cd1a45ccbf0f11411b450274af85f9a8f7090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19200587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2655618d8432d09b19ff05e92ffdb066ae6321ec932ebbd01c9c76d3e68ead2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:59:28 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 18 Nov 2025 19:59:29 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 18 Nov 2025 20:00:22 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Tue, 18 Nov 2025 20:00:22 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Tue, 18 Nov 2025 20:00:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang-static 		clang-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 18 Nov 2025 20:00:22 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 18 Nov 2025 20:00:22 GMT
VOLUME [/data]
# Tue, 18 Nov 2025 20:00:22 GMT
WORKDIR /data
# Tue, 18 Nov 2025 20:00:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 20:00:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 20:00:22 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 18 Nov 2025 20:00:22 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc33e6b8da6d92cc2696b3d11caa4fd881eaa845742e89a9d8caae9c1740bc01`  
		Last Modified: Tue, 18 Nov 2025 20:00:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774158458c83304266c41fb50996e35ecd06a3b9c0198d51a252de35ff484922`  
		Last Modified: Tue, 18 Nov 2025 20:00:53 GMT  
		Size: 199.2 KB (199173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88e910ad114886e062d7e4b275776f3c4b462b058d1cfaad87617e587bd70ac`  
		Last Modified: Tue, 18 Nov 2025 20:00:57 GMT  
		Size: 15.3 MB (15348981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80272f954b59c3c750ef0cd6ad88d7a3f7133bfd896fe9f91a141e549962125`  
		Last Modified: Tue, 18 Nov 2025 20:00:53 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39d2e992f656ebdc79f9cf54b382721f0000a159d32c5ae9153377fb854cc7e`  
		Last Modified: Tue, 18 Nov 2025 20:00:53 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:b2d43827796cfe62b3c9b94abc5e2c8083c4bf2ccdcb887dbbc34923fd5e2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.3 KB (499302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f2c00d9fa53974a76b547428e15948669bb8c5212b09a912c9ae841ae61d7d`

```dockerfile
```

-	Layers:
	-	`sha256:d0eb2f214ecd0d1d0878936a804a27a670d4a60b66bd8522f29c9ebbf326fcf2`  
		Last Modified: Tue, 18 Nov 2025 23:06:35 GMT  
		Size: 467.0 KB (466981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fea32f119e244359ade9f6d1591bc858a88246db731f0415593b04882fb96723`  
		Last Modified: Tue, 18 Nov 2025 23:06:36 GMT  
		Size: 32.3 KB (32321 bytes)  
		MIME: application/vnd.in-toto+json
