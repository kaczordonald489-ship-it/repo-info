## `redis:alpine3.22`

```console
$ docker pull redis@sha256:4eec4565e45aa0b3966554c866bc73211e281b0b3d89fe9a33c982e6faca809d
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

### `redis:alpine3.22` - linux; amd64

```console
$ docker pull redis@sha256:e9a8794f6d9d48751f76eeff9b8402405e208d043b35602a33ea415e7cff347c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33377521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad4195a4376c1018dd6fdadbe7dc9febb799402851a014f006cc77eb27b3e46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:41 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 28 Jan 2026 02:32:42 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Wed, 28 Jan 2026 02:39:14 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Wed, 28 Jan 2026 02:39:14 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Wed, 28 Jan 2026 02:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang-static 		clang-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Wed, 28 Jan 2026 02:39:14 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 28 Jan 2026 02:39:14 GMT
VOLUME [/data]
# Wed, 28 Jan 2026 02:39:14 GMT
WORKDIR /data
# Wed, 28 Jan 2026 02:39:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:39:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:39:14 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 28 Jan 2026 02:39:14 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82811f7b773afed505e756289df470d69c3ee264bc369b2a05733cd7247589c`  
		Last Modified: Wed, 28 Jan 2026 02:39:22 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2499c7b457a8556bda2eb440f265727fe79708a6ed8333e30caab1be0b469`  
		Last Modified: Wed, 28 Jan 2026 02:39:22 GMT  
		Size: 197.1 KB (197093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa398079aad549d68a36eb3a38c2cccc5d8a6494875e1ffbfa0fb117e6075979`  
		Last Modified: Wed, 28 Jan 2026 02:39:23 GMT  
		Size: 29.4 MB (29372368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c55050f77445a1fe500b8780f8d9b96dc2d3cb6dbe74e5017993a4043a08c2c`  
		Last Modified: Wed, 28 Jan 2026 02:39:22 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c137550d2ae446e46973ee9d0263b2df3026e07c2b42adf8403f7e87ad95c1f9`  
		Last Modified: Wed, 28 Jan 2026 02:39:24 GMT  
		Size: 2.1 KB (2104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.22` - unknown; unknown

```console
$ docker pull redis@sha256:f5c53f3551e363c56f869d9a807dd6a99d1627091d11741e08933c4842030fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.3 KB (501253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd1fe8d88a0cc962a62361775422d8c65c8964d3a33b86960f71dffec345e20`

```dockerfile
```

-	Layers:
	-	`sha256:ebd6c5d8564a450f176267966faa8be0460344b174f671f321a6dee7982dd423`  
		Last Modified: Wed, 28 Jan 2026 02:39:22 GMT  
		Size: 468.9 KB (468932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e23e43196528cfc575fa36e793b247860c23fe4e5fd2e73feca248bfab4cec2`  
		Last Modified: Wed, 28 Jan 2026 02:39:22 GMT  
		Size: 32.3 KB (32321 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.22` - linux; arm variant v6

```console
$ docker pull redis@sha256:2a4e374aed69ef0596ef91b4e4d8674ef9062081897cbf16478b08af53b41152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18306423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176ec1c214b3d44fb79df17e3754cee34e71fc5e8a575e8c6b064cf296b5df82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:53:18 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 28 Jan 2026 02:53:19 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Wed, 28 Jan 2026 02:54:14 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Wed, 28 Jan 2026 02:54:14 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Wed, 28 Jan 2026 02:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang-static 		clang-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Wed, 28 Jan 2026 02:54:14 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 28 Jan 2026 02:54:14 GMT
VOLUME [/data]
# Wed, 28 Jan 2026 02:54:14 GMT
WORKDIR /data
# Wed, 28 Jan 2026 02:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:54:14 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 28 Jan 2026 02:54:14 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b29aa42b3ac4494d4d7ba5484a4cf20cac30e06d3f7f8fbb30d424ad827a18`  
		Last Modified: Wed, 28 Jan 2026 02:54:20 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4582521327e55bf8d69b5e357bc664045981f76169b03fe952c3f23143965e89`  
		Last Modified: Wed, 28 Jan 2026 02:54:20 GMT  
		Size: 197.3 KB (197327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38f54eeb89203901b83952187b960f6b9032bad09acff3c63b5e9d21254b467`  
		Last Modified: Wed, 28 Jan 2026 02:54:21 GMT  
		Size: 14.6 MB (14600865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b560b5c51af2c89baffd633aed0bb81d74e07765649510471bf1a4a2fa77c7a6`  
		Last Modified: Wed, 28 Jan 2026 02:54:20 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abaacfcf083660cf9f26365af072e074c73e9f9e7fa2ce8da67a766b8a2c449`  
		Last Modified: Wed, 28 Jan 2026 02:54:21 GMT  
		Size: 2.1 KB (2103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.22` - unknown; unknown

```console
$ docker pull redis@sha256:6f6544c01b367156ce446b99665adde3781b54ca3f16b6ebd1cd014a714e6714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f72ededdb0c834d716e546c9430778a8d63566a9961c4920a3f5d1c84f7ccdd`

```dockerfile
```

-	Layers:
	-	`sha256:ad3e64dcdb75a28a54b2166f8be81b5e3c67cc10cd60d58fa4c9a53983a6412d`  
		Last Modified: Wed, 28 Jan 2026 02:54:19 GMT  
		Size: 32.3 KB (32256 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.22` - linux; arm variant v7

```console
$ docker pull redis@sha256:53354628308993963495135cf7578a99465d7dc1295829c20c2ca3a1663dfe43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17792289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ee23d986f301a5d9984faa35f145cd8ed2a91d065e1b9dea1f37de23d3bac2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:52:56 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 28 Jan 2026 02:52:57 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Wed, 28 Jan 2026 02:53:54 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Wed, 28 Jan 2026 02:53:54 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Wed, 28 Jan 2026 02:53:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang-static 		clang-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Wed, 28 Jan 2026 02:53:54 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 28 Jan 2026 02:53:54 GMT
VOLUME [/data]
# Wed, 28 Jan 2026 02:53:54 GMT
WORKDIR /data
# Wed, 28 Jan 2026 02:53:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:53:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:53:54 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 28 Jan 2026 02:53:54 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dc5e6766201f9c71bf297873a160011892d30e7b2fe906ac328b205c887378`  
		Last Modified: Wed, 28 Jan 2026 02:54:00 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3c645e9f7a037aa83e44d55822d355a9ee4c5f30d5dd653b0dfdca3d4964ea`  
		Last Modified: Wed, 28 Jan 2026 02:54:00 GMT  
		Size: 195.7 KB (195693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404db829a104122138b6a31df4f78e64e6085abb4557dc924804e29c9feb7fc7`  
		Last Modified: Wed, 28 Jan 2026 02:54:01 GMT  
		Size: 14.4 MB (14369782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74f00240fb480856b1384b87aab485356eb5dac3ef72d484dc440fe88471855`  
		Last Modified: Wed, 28 Jan 2026 02:54:00 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd53abc45f412654b707010cb6dae17f062592996c90e8c2493c7794bf8df75`  
		Last Modified: Wed, 28 Jan 2026 02:54:01 GMT  
		Size: 2.1 KB (2103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.22` - unknown; unknown

```console
$ docker pull redis@sha256:5612b1712ab350b5b7d18db99f061f7b5b9c9fb9dde3a49ef800c27b0331e7fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.5 KB (501472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42231e80a33b8b22c10a76be70d396ef309695c2be4ff1419f8f6df18ae562c5`

```dockerfile
```

-	Layers:
	-	`sha256:093073d98b8a86568202b5e5e92ab96801c126b11ffb888e62771bb0f531f533`  
		Last Modified: Wed, 28 Jan 2026 02:54:00 GMT  
		Size: 469.0 KB (469000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:126dc30fc92cef864d969d0a6abadbd39311bd99b9a860aa6d892245fea69535`  
		Last Modified: Wed, 28 Jan 2026 02:54:00 GMT  
		Size: 32.5 KB (32472 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:181fdf3cadeb08efe46464243de43eaf735630cd96451ff1d33a083ab2cb85c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542d079321f51007f4abc662ac2d68fd003b4555517b68589dda90830d08418a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:35:14 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 28 Jan 2026 02:35:15 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Wed, 28 Jan 2026 02:41:46 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Wed, 28 Jan 2026 02:41:46 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Wed, 28 Jan 2026 02:41:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang-static 		clang-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Wed, 28 Jan 2026 02:41:46 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 28 Jan 2026 02:41:46 GMT
VOLUME [/data]
# Wed, 28 Jan 2026 02:41:46 GMT
WORKDIR /data
# Wed, 28 Jan 2026 02:41:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:41:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:41:46 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 28 Jan 2026 02:41:46 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d818fdb0c1daf05988901e08684f1f08fdebeee4e4effb81a308f69f6c11cb60`  
		Last Modified: Wed, 28 Jan 2026 02:41:54 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1e74f2df0023cba95dc7acc9a9ca8e32a30387fcf775d9b26e54c828dd7d42`  
		Last Modified: Wed, 28 Jan 2026 02:41:54 GMT  
		Size: 199.0 KB (199031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2528ff1388fd2ce1b9b509074d8334238d756d6729d46586a5a9d8672d9b1a67`  
		Last Modified: Wed, 28 Jan 2026 02:41:55 GMT  
		Size: 28.9 MB (28928775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870278c815c795daf85bb5fe5a8ae71035d4023fc65e1b911837a439b30daa7`  
		Last Modified: Wed, 28 Jan 2026 02:41:54 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c08739e1caa5a8af2f41ad76fe8b38231fb345321b9666156ada84f0426418`  
		Last Modified: Wed, 28 Jan 2026 02:41:55 GMT  
		Size: 2.1 KB (2102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.22` - unknown; unknown

```console
$ docker pull redis@sha256:b640c1a6115f93bd06bac7cc1b7b80912f99f1dcc3fd258ad86b12174efac2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.6 KB (501554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba02077d99c1792f19dbb294aa247600d87fec0255129f907b10d5a9cc95c8f`

```dockerfile
```

-	Layers:
	-	`sha256:7ac1ac12a731320f084e052f972da20b7fe2e19abbaf1d2a56a0ec00540e86ce`  
		Last Modified: Wed, 28 Jan 2026 02:41:54 GMT  
		Size: 469.0 KB (469036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c0c81820442e8740e67ad8e4b491f6ee261f338d7cc9e2d5f047bb99b5ddebb`  
		Last Modified: Wed, 28 Jan 2026 02:41:54 GMT  
		Size: 32.5 KB (32518 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.22` - linux; 386

```console
$ docker pull redis@sha256:6c4892b32e6a3146fe7fba5deb2b32cd8d2ddf247f23bb19ef238c0f1a61d6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18199626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20961904682fc43c64e30468a66c658be4d52adfd1720c5d66759e29ef3c49e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:29:37 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 28 Jan 2026 02:29:39 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Wed, 28 Jan 2026 02:30:34 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Wed, 28 Jan 2026 02:30:34 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Wed, 28 Jan 2026 02:30:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang-static 		clang-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Wed, 28 Jan 2026 02:30:34 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 28 Jan 2026 02:30:34 GMT
VOLUME [/data]
# Wed, 28 Jan 2026 02:30:35 GMT
WORKDIR /data
# Wed, 28 Jan 2026 02:30:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:30:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:30:35 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 28 Jan 2026 02:30:35 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8313b350ff70168f134130e58525b213ab5d55ce498da5a597691a9251484c`  
		Last Modified: Wed, 28 Jan 2026 02:30:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32991edce3bd9d04a42c1bed76fa8a861914cab3e56f8f38f9a4bdcf154e508`  
		Last Modified: Wed, 28 Jan 2026 02:30:41 GMT  
		Size: 197.6 KB (197559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd39d865e479db3ec533b7ab887f817fe0bc800fd39e2506a638c5d01180449`  
		Last Modified: Wed, 28 Jan 2026 02:30:42 GMT  
		Size: 14.4 MB (14378147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91af4106418fc25de11b4055df73132cbcfa228ca6c948c3e175b88003f8e671`  
		Last Modified: Wed, 28 Jan 2026 02:30:41 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6faac40e29b75c92d9e9180eed6eb64d62c8dc69a37f632d24e8ddf53d86669`  
		Last Modified: Wed, 28 Jan 2026 02:30:42 GMT  
		Size: 2.1 KB (2105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.22` - unknown; unknown

```console
$ docker pull redis@sha256:b0d92f5f90c8dbbd5bcd7109e1b052a58e55b125e9a2f4b167a1f9a3868082b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.1 KB (501150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540da43d04a582c7eefd0285cc4ab21c269bf7a0c8da0ccb32af478d398922d9`

```dockerfile
```

-	Layers:
	-	`sha256:8b626c7d91ab7682ac3ddee0a8e0a9d9d94c8b0cc9882458b0ea54a71ae58900`  
		Last Modified: Wed, 28 Jan 2026 02:30:41 GMT  
		Size: 468.9 KB (468887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2766a3b7d09af8ed9c87079bb931e0d1ee2b663494f48e9ecb5e74a17778ffc4`  
		Last Modified: Wed, 28 Jan 2026 02:30:41 GMT  
		Size: 32.3 KB (32263 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.22` - linux; ppc64le

```console
$ docker pull redis@sha256:f7aee46a5900405db3d02afa7fe289349757c632631c8ab5f59b20821e55647c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19558251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66758b6d5aa7496008e83115a4c72395f3c0c5c93192346da57d014c718d84a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:53:31 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 28 Jan 2026 03:53:35 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Wed, 28 Jan 2026 03:54:32 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Wed, 28 Jan 2026 03:54:32 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Wed, 28 Jan 2026 03:54:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang-static 		clang-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Wed, 28 Jan 2026 03:54:33 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 28 Jan 2026 03:54:33 GMT
VOLUME [/data]
# Wed, 28 Jan 2026 03:54:33 GMT
WORKDIR /data
# Wed, 28 Jan 2026 03:54:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:54:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:54:33 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 28 Jan 2026 03:54:33 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e166b0f0d0c8cff51a6eb3e5f06a7a0e115fd7e64dc0689c8a2b03101944fc`  
		Last Modified: Wed, 28 Jan 2026 03:54:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e054a06c60d73bdcb94d6d428554e211141d1ce4b289a975bb9537951899736b`  
		Last Modified: Wed, 28 Jan 2026 03:54:53 GMT  
		Size: 200.1 KB (200070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4aaf595884e23a5719c392e24211ff84ca501ae600b5baa5841118b5a98abd`  
		Last Modified: Wed, 28 Jan 2026 03:54:53 GMT  
		Size: 15.6 MB (15620698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ddd9f9394eca1ba558c40280042ba329da112aa40cff67dca5d07696395858`  
		Last Modified: Wed, 28 Jan 2026 03:54:53 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97531b8103d378a450253e60f125abcab5385a51dfd25c0bad44f04bab307116`  
		Last Modified: Wed, 28 Jan 2026 03:54:54 GMT  
		Size: 2.1 KB (2105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.22` - unknown; unknown

```console
$ docker pull redis@sha256:ed10aa8112e473d468a770fd86dc9ca88c6a2320aa89b2d0c9e8be9789d42470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.4 KB (499434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babf5baa2f85c37388070eabe1c2cfb3e92fbdf58a2527b6668015f23aa17a71`

```dockerfile
```

-	Layers:
	-	`sha256:919507bd7944156097d16b1d682ab8313d3ec30578a5d2042c9abc9e2ed7ffee`  
		Last Modified: Wed, 28 Jan 2026 03:54:53 GMT  
		Size: 467.0 KB (467039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fef7687b5242c32cb81af196701fc66efd7e70e583c9c6dc556acfd29771249`  
		Last Modified: Wed, 28 Jan 2026 03:54:52 GMT  
		Size: 32.4 KB (32395 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.22` - linux; riscv64

```console
$ docker pull redis@sha256:36c21782c8e529ee6b92292ef34746f9eda46280dc458667b30ca521674dca69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c65379e23a5a3ad560e82b1502e7da3a94c90cd512d91b95c858acb3349b9e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 17:21:36 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 29 Jan 2026 17:21:41 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 29 Jan 2026 17:38:13 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Thu, 29 Jan 2026 17:38:13 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Thu, 29 Jan 2026 17:38:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang-static 		clang-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Thu, 29 Jan 2026 17:38:13 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 29 Jan 2026 17:38:13 GMT
VOLUME [/data]
# Thu, 29 Jan 2026 17:38:13 GMT
WORKDIR /data
# Thu, 29 Jan 2026 17:38:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 17:38:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 17:38:13 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 29 Jan 2026 17:38:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6469b71dcb6c0568c91cf22ae6f3b2b8d90773d584ed9c01b274932393cab5f3`  
		Last Modified: Thu, 29 Jan 2026 17:39:00 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e85fe551bf5a5d35e2313e59ffb210812d14cbc0e654a44efd5f1d96d02cfe`  
		Last Modified: Thu, 29 Jan 2026 17:39:00 GMT  
		Size: 197.2 KB (197225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ef37d5371a7f455677caa37a2b793b42a1b829cdf28c402461a35b3c80e2c`  
		Last Modified: Thu, 29 Jan 2026 17:39:02 GMT  
		Size: 14.1 MB (14064493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5317263eaa07e00ddfed2f53eacd54a0615b0b74753ac3c12e8cd5a71535d45a`  
		Last Modified: Thu, 29 Jan 2026 17:39:00 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ecf4b457305f5f100d84fae30b46ed1dbe00a7b2ac2cb4b13c4cd3f636344f`  
		Last Modified: Thu, 29 Jan 2026 17:39:02 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.22` - unknown; unknown

```console
$ docker pull redis@sha256:c995dac5de0f81d8133b17bcbf27cd981f14b0c3885face848889030ec985689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.4 KB (499430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b2cf5fd29b7dceaca7047f3e18364b30d567c241aa6368210c7e9bd23f0d27`

```dockerfile
```

-	Layers:
	-	`sha256:264146ac3dead45b43463bf5022b1ab87fa3edd699f02e77b7496220a8e262ab`  
		Last Modified: Thu, 29 Jan 2026 17:39:00 GMT  
		Size: 467.0 KB (467035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1ef77dcd369d88abd4120d0df129384c5bf86104723a092dc0d15738bdcf3c1`  
		Last Modified: Thu, 29 Jan 2026 17:39:00 GMT  
		Size: 32.4 KB (32395 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.22` - linux; s390x

```console
$ docker pull redis@sha256:9d397189f6c447adb698b002b773bb7501927dab2959de5beda80ad97a1e06fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19201830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576b3cc959fdcf0a60b18c6325b479f24aaacd5278d2d739bbf01128ed18bad8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:02:04 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 28 Jan 2026 03:02:05 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Wed, 28 Jan 2026 03:03:03 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Wed, 28 Jan 2026 03:03:03 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Wed, 28 Jan 2026 03:03:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang-static 		clang-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Wed, 28 Jan 2026 03:03:03 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 28 Jan 2026 03:03:03 GMT
VOLUME [/data]
# Wed, 28 Jan 2026 03:03:03 GMT
WORKDIR /data
# Wed, 28 Jan 2026 03:03:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:03:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:03:03 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 28 Jan 2026 03:03:03 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bb1f788df50456443edebc4ee40796d88f9f0b6a95d2785f9dc0813f0ba50a`  
		Last Modified: Wed, 28 Jan 2026 03:03:13 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0935b3b4881da2b68c8c585ef38c7d88c71ddc50212b540e97d52fcdb8d8c4`  
		Last Modified: Wed, 28 Jan 2026 03:03:14 GMT  
		Size: 199.3 KB (199307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdef3939c7eaedcbabab87a8d2126e4d98ffb6b51efc29ddc6fe6e1649446c60`  
		Last Modified: Wed, 28 Jan 2026 03:03:14 GMT  
		Size: 15.3 MB (15348907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c649614dfc53524854f12be6cbfae64834f8062f9dfdbb495c032af445b241`  
		Last Modified: Wed, 28 Jan 2026 03:03:13 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e848128d8688b8c162c747fd02440d50c8a1fda366f8f0bb5e155e53bc7246`  
		Last Modified: Wed, 28 Jan 2026 03:03:14 GMT  
		Size: 2.1 KB (2102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.22` - unknown; unknown

```console
$ docker pull redis@sha256:4062f97a944e199529be9ebd35be4e7d4687c5b57d620f4acc73e89f937655d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.3 KB (499299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99473e0a21bc764d85b6737c4bd3d52861d541b99c260d1a007448bd9ef54d1d`

```dockerfile
```

-	Layers:
	-	`sha256:b20d7231c4cba4a53a7bf296fcc446d6c1cc88a7e9376cc00e4c2b5c59e7e40d`  
		Last Modified: Wed, 28 Jan 2026 03:03:13 GMT  
		Size: 467.0 KB (466981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8df6a4d93904cbe0852787a62fa541b1f5e50273be5ca04f685532b744ae4907`  
		Last Modified: Wed, 28 Jan 2026 03:03:13 GMT  
		Size: 32.3 KB (32318 bytes)  
		MIME: application/vnd.in-toto+json
