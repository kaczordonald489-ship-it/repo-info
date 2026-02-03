## `hylang:python3.14-alpine`

```console
$ docker pull hylang@sha256:cbd9e63029419c98aff34df1534fab87b6639f4d14e4cc2626916f258653ce40
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

### `hylang:python3.14-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:9db2c66b0c9049c4ef5c94c764370ce1e1f20a1b636e884208bb2b6723f485cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23272536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df849d51c4b249814e879ce089f0743e4d86fae10d45d993fd1fd61e80aad974`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:32:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:32:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:32:59 GMT
ENV PYTHON_VERSION=3.14.2
# Wed, 28 Jan 2026 03:32:59 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Wed, 28 Jan 2026 03:35:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:35:46 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:35:46 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 05:00:53 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 05:00:53 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 05:00:53 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 05:00:53 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6e0b1647863beafdee1aebbdaeaeb2fda3507fe7e1339bbdd208cc1e50a840`  
		Last Modified: Wed, 28 Jan 2026 03:35:54 GMT  
		Size: 460.9 KB (460934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff83b2b57ff13d7d3ad1ccc77ff3a507c3ec3e1e2114fe6a549e922337320e8e`  
		Last Modified: Wed, 28 Jan 2026 03:35:54 GMT  
		Size: 13.4 MB (13362526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd701e501660028c5c9421ae4ad32b775dd4677863eebf922cab66ae731ee6f7`  
		Last Modified: Wed, 28 Jan 2026 03:35:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d7deeec0957e90fd3a70f981b622f7eaeb81beb04242cc97b98b48d21b6b66`  
		Last Modified: Wed, 28 Jan 2026 05:01:01 GMT  
		Size: 5.6 MB (5587006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:d05f605639044c6cb47e0dd9fe38d256f63023ca8adff810f259ad1fe9a5e29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (639951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344999d454ae74e4db9aa4439caf0664229ea09fc28b9bd90c075566498807ea`

```dockerfile
```

-	Layers:
	-	`sha256:9f4ff9635e9b6f3c4faba308f9a6bd3fadd8979d503c18faa576e2616782e433`  
		Last Modified: Wed, 28 Jan 2026 05:01:04 GMT  
		Size: 628.1 KB (628147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b669629d015f4f5be28365ba8544550a9effcb4b12360e492193ec942d938a99`  
		Last Modified: Wed, 28 Jan 2026 05:00:59 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine` - linux; arm variant v6

```console
$ docker pull hylang@sha256:236a0887f819e76ba9fef71cb8554307a4ff0bda0d3c0fd91fe6922ebd18548c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22603885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914037825ae187cdf41410f26a0a1b6d95c4c09f70428b0179e29c67124be462`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:03:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:03:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:03:32 GMT
ENV PYTHON_VERSION=3.14.2
# Wed, 28 Jan 2026 03:03:32 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Wed, 28 Jan 2026 03:06:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:06:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:06:20 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 04:05:41 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 04:05:41 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 04:05:41 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 04:05:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773b608ff05726281d3136f81e60ce6c20dc1d0693df62f1d6a69dd6bf20c406`  
		Last Modified: Wed, 28 Jan 2026 03:06:26 GMT  
		Size: 461.4 KB (461445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5706452906aecb55749ef0fb0e3fe3dc1847c941a20529c155508719d94319`  
		Last Modified: Wed, 28 Jan 2026 03:06:26 GMT  
		Size: 13.0 MB (12985317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdacc8220994199542da09cd03016899f0d7f0450c5b5fd865de45db9ae623d2`  
		Last Modified: Wed, 28 Jan 2026 03:06:25 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84375fd01b36e58bceafedce207782897c9e70ede627e703449d84b09a399c9`  
		Last Modified: Wed, 28 Jan 2026 04:05:46 GMT  
		Size: 5.6 MB (5587052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:d6624aa3a5957951e1c48be28ccbe541dcf7397844447347606fb072d89f10ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 KB (11765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5176c2c07e85b7bbb9ba504f0f1b77f6634261e6f1b7ab36f259939122164229`

```dockerfile
```

-	Layers:
	-	`sha256:11327adba0d86c96f39e5ddce6b104c8f12a0a13633fedb64af48c0c1db20484`  
		Last Modified: Wed, 28 Jan 2026 04:05:46 GMT  
		Size: 11.8 KB (11765 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine` - linux; arm variant v7

```console
$ docker pull hylang@sha256:77222c3644dfb4aac01102fd02f8ac2a1121566475e9be59f8e600e4dd61adcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21918109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3afdfc097120c2408a8f499b2d4bd22ebb2779df4a3c54d5f6adcb1b0110f9`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:10:35 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:10:35 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:10:35 GMT
ENV PYTHON_VERSION=3.14.2
# Wed, 28 Jan 2026 03:10:35 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Wed, 28 Jan 2026 03:13:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:13:21 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:13:21 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 04:13:09 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 04:13:09 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 04:13:09 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 04:13:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db21d1bf3c84a4b75f11c997de066df8f8560f625bbcd5c4e56028ab14790a9`  
		Last Modified: Wed, 28 Jan 2026 03:13:28 GMT  
		Size: 460.7 KB (460721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92b4173f2ccc3d7763f645ed714ae475c75546c8e32d42809393c6735bfb76e`  
		Last Modified: Wed, 28 Jan 2026 03:13:28 GMT  
		Size: 12.6 MB (12588345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155d8d5184393d8afdf1537f0246407a5580073b18591a7159d7ad18c86277a5`  
		Last Modified: Wed, 28 Jan 2026 03:13:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c9dc94340c83b2bf5f72f89fed53d8f73609905829ac49c643be8d1222b760`  
		Last Modified: Wed, 28 Jan 2026 04:13:15 GMT  
		Size: 5.6 MB (5587072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:eaa48cc3289a0eaa2131c5753ea6ef1f8b47c75eff3e1c2727dc821c234bf804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.6 KB (642599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a9c3b37b00d9d256ec3a89335287af060267c03367ca099254a8877128e800`

```dockerfile
```

-	Layers:
	-	`sha256:0a0e0338c97043634bae21fe966d54f1575a0d5b7688bbf513edaa62c72aedb6`  
		Last Modified: Wed, 28 Jan 2026 04:13:15 GMT  
		Size: 630.6 KB (630619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e80e026fb164300fa430d219fd4055d6603821f4218d483d2f6e6962c21b0e`  
		Last Modified: Wed, 28 Jan 2026 04:13:15 GMT  
		Size: 12.0 KB (11980 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:ecede75758f3e933565a00a8198540c0ca484c0f61f516ee59b964354908429d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23699187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f8fed35253a1dfebb9e4a632c2291df0c03b04c52689b0c11fd84ff7aee31f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:20:15 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:20:15 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:20:15 GMT
ENV PYTHON_VERSION=3.14.2
# Wed, 28 Jan 2026 03:20:15 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Wed, 28 Jan 2026 03:26:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:26:12 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:26:12 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 04:50:03 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 04:50:03 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 04:50:03 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 04:50:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217eb6daea6a539678017b05f049f5b9a73edce1373737c5b5f471ff3a13f3cb`  
		Last Modified: Wed, 28 Jan 2026 03:22:58 GMT  
		Size: 463.0 KB (462982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff4bb98855c76b5fb4face7f2ec94fb6ffc5dbc996eb0f5ca50b4823b0e1ee7`  
		Last Modified: Wed, 28 Jan 2026 03:26:19 GMT  
		Size: 13.5 MB (13451780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd27da92a3729fe1d7a383531f4c67ad67db46e9d2f1bfdf8ec04d2ef5658f6b`  
		Last Modified: Wed, 28 Jan 2026 03:26:19 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82b72a8444c0cffb3777dbc494ea11aca0c66d5eb8590e9933d391d64aa88b6`  
		Last Modified: Wed, 28 Jan 2026 04:50:09 GMT  
		Size: 5.6 MB (5587085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:815cbaae5b4cd76f8ee440d0119ce45f85bc231620e17dea2ba3f906689f28c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.7 KB (639749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cff571a6965abcd45342880d9545fd1c3aaa446cf1196927e4085741664778`

```dockerfile
```

-	Layers:
	-	`sha256:3222f1c64d01700ec2c4fdbe225be2739d9a27ac0ac7ee2fde41e67c603b7718`  
		Last Modified: Wed, 28 Jan 2026 04:50:09 GMT  
		Size: 627.7 KB (627697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb4199b0952d6ada0790f5ab8ed6426bec15db9ace3ca6ecef69f1a22d717be3`  
		Last Modified: Wed, 28 Jan 2026 04:50:09 GMT  
		Size: 12.1 KB (12052 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine` - linux; 386

```console
$ docker pull hylang@sha256:651ce91160183be5dbdca38648c406fb18c3a92eeefee78a979fed2135a7a58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23351116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181ad28a1890786ef7b261d40abd2b40f61862f93bb7eaa24341290ee0545188`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:36:41 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 02:36:41 GMT
ENV PYTHON_VERSION=3.14.2
# Wed, 28 Jan 2026 02:36:41 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Wed, 28 Jan 2026 02:39:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 02:39:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 02:39:11 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 03:56:45 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 03:56:45 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 03:56:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 03:56:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387408edad8de8b3c6e410c6529e62fd1b23b834fcab71c87c358ff9eb5c2c1`  
		Last Modified: Wed, 28 Jan 2026 02:39:18 GMT  
		Size: 461.2 KB (461233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a715f4e19a277b4ae6f16cae496bfeb4af5e8b57e8e8b486a9afafcf36311fdf`  
		Last Modified: Wed, 28 Jan 2026 02:39:18 GMT  
		Size: 13.6 MB (13615594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac2822ba5d347180ff6d16ecc6b5310f6a69b37620648d27f95b7f63a9dd09f`  
		Last Modified: Wed, 28 Jan 2026 02:39:18 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1651a30360cacd96282512022728b120303728008c01b69218fca5b21d07ebf2`  
		Last Modified: Wed, 28 Jan 2026 03:56:51 GMT  
		Size: 5.6 MB (5587044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:994cd905758772a00d5df70cbebd00c742f9afdad83d5628583be57ec07b731c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.8 KB (639774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9818e07c4d0ee28b8f4ee157c9d480d25cc6808af2605209d3240349a1bf3733`

```dockerfile
```

-	Layers:
	-	`sha256:b3d32eaf3ef2e3ca269bc6e22798faf9a8a0ef7d999f41c91c53bc795b28bfcf`  
		Last Modified: Wed, 28 Jan 2026 03:56:51 GMT  
		Size: 628.1 KB (628062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8b485f6b862ae957c513646329c938dbb2b3bef933faa4c18f325f24d91e95`  
		Last Modified: Wed, 28 Jan 2026 03:56:51 GMT  
		Size: 11.7 KB (11712 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine` - linux; ppc64le

```console
$ docker pull hylang@sha256:80d9e8480af87b7f7856522329ef004af53a3d8c6447a81158ab8e023f72716a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24120753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c514db38d9b3cdf70898db7b234973fa0db058fc4a51d1ca9a32aa5a1cd823`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:44:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:44:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 04:44:00 GMT
ENV PYTHON_VERSION=3.14.2
# Wed, 28 Jan 2026 04:44:00 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Wed, 28 Jan 2026 04:48:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 04:48:36 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 04:48:36 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 06:58:03 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 06:58:03 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 06:58:03 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 06:58:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143f2a7bbfcb07998418b0982b0f9e5f599c0db8360efdf65fc48a08ce71b452`  
		Last Modified: Wed, 28 Jan 2026 04:48:50 GMT  
		Size: 463.5 KB (463503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c64234b66d4d0bcc06391db5a81167c00e1e098dc6dc2530112366dedefb2d`  
		Last Modified: Wed, 28 Jan 2026 04:48:51 GMT  
		Size: 14.2 MB (14240321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43de9a1e3d6aa1af1b2affe24e74b44394f5f819a2526fe06e0b5aac0c4cf4d`  
		Last Modified: Wed, 28 Jan 2026 04:48:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ea62243e9ae27ca5e085ef3934e2d4cad964f366ab5312dc145be05640e517`  
		Last Modified: Wed, 28 Jan 2026 06:58:19 GMT  
		Size: 5.6 MB (5587038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:82daf94659c4773625b01ac71eb1861858fe306552d2cdaa52051a136c2bb681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.5 KB (639521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d29f847f5ea10e223f8472fb829cb989985e71cf9c89ebaad220591880bedb`

```dockerfile
```

-	Layers:
	-	`sha256:2e3c571072fb4dfe1081980781c12da406cd59ffabfe6ac96015b3fc6b23d1f4`  
		Last Modified: Wed, 28 Jan 2026 06:58:19 GMT  
		Size: 627.6 KB (627602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2564a517623ddc23524f4e8279fbd4fa6258e3f30a1da10a1920c7c9c18f6d`  
		Last Modified: Wed, 28 Jan 2026 06:58:19 GMT  
		Size: 11.9 KB (11919 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine` - linux; riscv64

```console
$ docker pull hylang@sha256:a4a6c474ebe0bbc6244ca16161b2ba34c57ff5c22fc3b3f5e65bea29c6a99f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23118714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c71f60e97f67e4a474b4ddb8568047b71f7e2cdd9170ea0f8151edba3a331c0`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:30:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 19:30:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Jan 2026 19:30:12 GMT
ENV PYTHON_VERSION=3.14.2
# Thu, 29 Jan 2026 19:30:12 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Thu, 29 Jan 2026 21:31:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 29 Jan 2026 21:31:31 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Jan 2026 21:31:31 GMT
CMD ["python3"]
# Sun, 01 Feb 2026 05:53:14 GMT
ENV HY_VERSION=1.2.0
# Sun, 01 Feb 2026 05:53:14 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 01 Feb 2026 05:53:14 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 01 Feb 2026 05:53:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35a473f7da969ca6a41bd17bd9ab88790821df528b66a16299f480a4d4a1620`  
		Last Modified: Thu, 29 Jan 2026 20:11:12 GMT  
		Size: 461.2 KB (461185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9ffdd3d9fc33f5d3ee4f9ccd53137b99f2cd6425f851eff321e21ee8477180`  
		Last Modified: Thu, 29 Jan 2026 21:32:18 GMT  
		Size: 13.5 MB (13484484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74fbbb95293da59a992254e5dbbfb92d04f5ea429428ae5cd9f9bcfb4b41c01`  
		Last Modified: Thu, 29 Jan 2026 21:32:15 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7457819459d20e9fd7b20d2d86339f8128c8a3fe8f74e30a1b2eed36ed2832`  
		Last Modified: Sun, 01 Feb 2026 05:53:53 GMT  
		Size: 5.6 MB (5587507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:e8d05ce105660049a0dbb9be280524840bb79e95b566a5a28c00962e641bb7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.5 KB (639518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21093382155fefb310d81d9241274615c8e8622c8307faddd754ba845a7e1dbe`

```dockerfile
```

-	Layers:
	-	`sha256:f9fa4d1787023d9da3a28c08c62368d3dc190f6479a2b039e1aecf1397ae9884`  
		Last Modified: Sun, 01 Feb 2026 05:53:52 GMT  
		Size: 627.6 KB (627598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c08e4b7d8a6724d89706b4515888c9a0e665b3652b406367e7babc73896d29`  
		Last Modified: Sun, 01 Feb 2026 05:53:52 GMT  
		Size: 11.9 KB (11920 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:2c71abdc2e7a6cf0c1ae620a6d3445da467bd999ddff9650483cbbc68d0018c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23621977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff092214f86dde9509e991857554cc433fa83faf16a1fa7429fca9c424c1d50`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:21:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 06:21:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 06:21:37 GMT
ENV PYTHON_VERSION=3.14.2
# Wed, 28 Jan 2026 06:21:37 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Wed, 28 Jan 2026 06:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 06:34:35 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 06:34:35 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 07:27:47 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 07:27:47 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 07:27:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 07:27:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b28e47fdb0827b778ce2cc7a5b1ea539b6424c12a2419fbf832e75366e3fc`  
		Last Modified: Wed, 28 Jan 2026 06:27:27 GMT  
		Size: 461.7 KB (461741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347222f42dd70d5c3d5b5fd2d1a7318c817bbb31d5f7c6a774e9eb954f6a4081`  
		Last Modified: Wed, 28 Jan 2026 06:34:46 GMT  
		Size: 13.8 MB (13847629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78654f2b8de425ede4fd4559d18b438e4282c5b3bf656e58070a3180f6049c7c`  
		Last Modified: Wed, 28 Jan 2026 06:34:45 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16b04cf9bfc728cec6449b237059afb8d7f09e059d8517b2402b325c522f305`  
		Last Modified: Wed, 28 Jan 2026 07:27:56 GMT  
		Size: 5.6 MB (5587025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:7d79cbbe9361a0c0394f5ee6e1f812b6a183125b06f78d58e5483c35ab3f1c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.3 KB (639300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4e05091c36b55c190113a0d1668ca8f892134261f9e19e8489b40a1f81c266`

```dockerfile
```

-	Layers:
	-	`sha256:c50a55257d3c1e1acdbd44b0e788cc9de84e6014a7df1b86138144306cf40556`  
		Last Modified: Wed, 28 Jan 2026 07:27:56 GMT  
		Size: 627.5 KB (627496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:482b7fbdd234f073672404d4b2e1b1ec76b8855fcbad557076044a26e67649ef`  
		Last Modified: Wed, 28 Jan 2026 07:27:56 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json
