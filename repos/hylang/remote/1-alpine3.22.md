## `hylang:1-alpine3.22`

```console
$ docker pull hylang@sha256:ee01512e2fc6978346787e992ba53d5832703e961ce918da808fe9a693124884
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

### `hylang:1-alpine3.22` - linux; amd64

```console
$ docker pull hylang@sha256:5b4ec508562a643b3f36718a43912be1baaaad7af6aa85958718685abf970ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23204117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d1267e2e1f7e832c747598c6bf43bffc534494cfff76f8827e3f84a2fb6bdc`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.14.0
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:41:27 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:41:27 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:41:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:41:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d375910f52b7c453db7c1e2135c1536210eb84825e8505b1c9e5a34faaf57a`  
		Last Modified: Wed, 08 Oct 2025 23:14:08 GMT  
		Size: 456.9 KB (456919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facdf984afd18f7f52714321a1e8915796191dd98798aef5d1f77a85507e830d`  
		Last Modified: Wed, 08 Oct 2025 23:14:09 GMT  
		Size: 13.2 MB (13227490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13839c1b2c2fc819a0ebcba5bbfcb61b3d29976827c3c86062f87186660baa70`  
		Last Modified: Wed, 08 Oct 2025 23:14:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca013aebdb597a76cb11efb6ec6f97d5577e421446a8e5bd344322d157cd09b`  
		Last Modified: Thu, 20 Nov 2025 19:41:39 GMT  
		Size: 5.7 MB (5717006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:d9a0443022bdf67d1aaa33d4b2035a3664203c73c7cdecea5dddab9701aa6787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.7 KB (640697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a675f5533cea12e38aa34201fa5c3b3f5267f9225d3db1178d19859e65b055aa`

```dockerfile
```

-	Layers:
	-	`sha256:bf3dee0bb81fd339e7d5e81c0d72f2d4b00903626c9103eeac8d61124ce4f8af`  
		Last Modified: Thu, 20 Nov 2025 21:20:31 GMT  
		Size: 628.9 KB (628893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08240929bcdc2afbb080d3a46ef1b8d1966e95d08fbbcb7fdbcc237a04403aef`  
		Last Modified: Thu, 20 Nov 2025 21:20:32 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:a6cc69be2ebe7fd7377b68ee7e565dab7eb01cacb475f4ce2fca35c10653be79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22499594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf243823725bb5c5a6a9d4891ac79efc8dfa89180af462f1a6d81615fc4a33a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.14.0
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:40:46 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:40:46 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:40:46 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:40:46 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d4269b3686e15b4f8f48438764091d5d67812012f7778f9e757a6fa00f7710`  
		Last Modified: Wed, 08 Oct 2025 23:10:22 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aaea1997a295952ef98427590c2fbcd8c77aa54d41ac556a5eea840859537bf`  
		Last Modified: Wed, 08 Oct 2025 23:10:23 GMT  
		Size: 12.8 MB (12820586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5f5ee62c2e3659bebf10eb3823089b81a9accd3f78c27ab0cbf97ae35d0712`  
		Last Modified: Wed, 08 Oct 2025 23:10:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d2348732e79f33da2993fbd56d8dfc5f0842ab2e4ebc7db52fc32d41376f85`  
		Last Modified: Thu, 20 Nov 2025 19:40:56 GMT  
		Size: 5.7 MB (5716940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:64cd7ed56bafeefe312078382c16ba7c65741f4d564efe0970d68174d2950127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 KB (11765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701e32bc7da9c045a3c0752358c383f97f30f0c942b518b3d1ea4769e83646d3`

```dockerfile
```

-	Layers:
	-	`sha256:ad4cc66ee8f1d4d5f3af7e6276c7a3fc5f5f00ff100691be20c525826cc6c225`  
		Last Modified: Thu, 20 Nov 2025 21:20:35 GMT  
		Size: 11.8 KB (11765 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:577103055b3a96d7779fcef21c19e170ea058ae3fcdec7fa90217d52a800ac59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21837524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327d11c969a001d2e8858fa9c5a2e3e9c35bd14e90f25fa72b9df31df74bdae5`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.14.0
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:40:24 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:40:24 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:40:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:40:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3be738120b51667af972badfd4ca211a4730f0169bea69d0bf407aab7879bb`  
		Last Modified: Wed, 08 Oct 2025 23:27:04 GMT  
		Size: 456.9 KB (456927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891a0214ffb6f4feec3e41f610b5d09be335c82fd4ad77e91eea43afcf8fbeb6`  
		Last Modified: Wed, 08 Oct 2025 23:27:05 GMT  
		Size: 12.4 MB (12441911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d6106fe27785167c9c7e334f3ac6d598dae0c3acf0cafb63f49e6aa27ee3c6`  
		Last Modified: Wed, 08 Oct 2025 23:27:04 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803a5fd553c2784d9dc1dcf2c94eabf0b20554f0105be62422e06b8378f7a435`  
		Last Modified: Thu, 20 Nov 2025 19:40:42 GMT  
		Size: 5.7 MB (5716883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:20a70aa3e6b38e700ab330d6a1f2648f59a4f54e2ad43e7c3ba540d1959cbbd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.0 KB (643995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164211258cf10a405db61c4836b7b8719513bc110433aa97bae0a3f4f3ee8ae6`

```dockerfile
```

-	Layers:
	-	`sha256:a98020037a9e46dbcd39d98a8793e7a86969c7c201c9470a8e4c6a3198f15c07`  
		Last Modified: Thu, 20 Nov 2025 21:20:38 GMT  
		Size: 632.0 KB (632015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:396c9765f61a690f7a42baa563896bfe70f4c4bb5ccda7ea7aa0ab2a038a89a1`  
		Last Modified: Thu, 20 Nov 2025 21:20:39 GMT  
		Size: 12.0 KB (11980 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:8e2921917474d93f6ce2af86ba81585c165b6db96fef160e86a7dd222643e895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23526935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3b178953e2eda0dc4d91b9798d4a119f48a5f3f49cd845f22125a6d51e2cdd`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.14.0
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:40:31 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:40:31 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:40:31 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:40:31 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40ae7b26a4339a3a04dafdb41480434b641e8406d65a75dbceb42a4175f9476`  
		Last Modified: Wed, 08 Oct 2025 23:08:18 GMT  
		Size: 459.0 KB (459014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f04d5975a3fdf02bda592cbcdf03105f4ee811d0280c7ec9e563adecbb44f3`  
		Last Modified: Wed, 08 Oct 2025 23:08:20 GMT  
		Size: 13.2 MB (13212747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c6b9aa3f72ec0583de65931ae54e7ad0319c79cc39e268df5ef7c28af783a6`  
		Last Modified: Wed, 08 Oct 2025 23:08:18 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4031830b8a6f859e639c8a68743b4b7e2f36e99b9f9a3d971ec7d7f8ed822b3`  
		Last Modified: Thu, 20 Nov 2025 19:41:59 GMT  
		Size: 5.7 MB (5716856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:5d54042d7ae93cfa0dce967e05779750e88dd8c6a6c264543fdeb8f425faeb4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.1 KB (641144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2d8c43d9f9df1bf736a0e668216ac857c975aeae8a5894d6d9b8c96178943c`

```dockerfile
```

-	Layers:
	-	`sha256:7d7159d5ad145542b3174aa4950da71ae06d69f20d84844356b716519bfca171`  
		Last Modified: Thu, 20 Nov 2025 21:20:42 GMT  
		Size: 629.1 KB (629093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c6b3aee0230d4990b001744795e5cc90ce61f765bcd438e337400a284427fd5`  
		Last Modified: Thu, 20 Nov 2025 21:20:43 GMT  
		Size: 12.1 KB (12051 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:89d4d0dee959229fb675f33eedf11801e621af0153eaad27881b904ee719362b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23300894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1deabdc19fdbf5c11ed7b95cdd660c37cd13cbb19cb47b16c0d1349b762f092`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.14.0
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:41:14 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:41:14 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:41:14 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:41:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6178cfe08200de678032e107b9261b3e14fe1e4f5c75c43f5b5401f39db114`  
		Last Modified: Wed, 08 Oct 2025 21:50:08 GMT  
		Size: 457.4 KB (457370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538e591936527dc6156bd29265b96691a25d703fab6e213c33a9b8618eb39d95`  
		Last Modified: Wed, 08 Oct 2025 21:50:08 GMT  
		Size: 13.5 MB (13507517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad178f74a9e10b54ab913ef74292e8f06b2770487612967dabc75078b09d72e4`  
		Last Modified: Wed, 08 Oct 2025 21:50:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd4f756efb203bfc36dedb18df9c73bfeb67dbfabb90f4c935d384c5fec6193`  
		Last Modified: Thu, 20 Nov 2025 19:41:25 GMT  
		Size: 5.7 MB (5716828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:017206cab8d87b9f5c4f72c8482976b93cffcb0d49466d74a4c70fae0a520fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.5 KB (640519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81239746f41b8a7f280293097bb5d5f2477f89bf8503217bb91f202ec712ed2`

```dockerfile
```

-	Layers:
	-	`sha256:cb9197b1244afb2e60bc79da7a54cace73edc5d65ae13c1ae25b78f84164c617`  
		Last Modified: Thu, 20 Nov 2025 21:20:47 GMT  
		Size: 628.8 KB (628808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee8aa12ea6a231c21b63cd6cbf2b63d4cf002fa82a785d55c138643dc3c7808`  
		Last Modified: Thu, 20 Nov 2025 21:20:47 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:43b8efffcc0fe73c00fa74631264a42f2ea36e2ef600dc24cde057a89103d5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23915626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7a8ec37d4f6bd76e6c33df51a009504ec11bb0f56ba2c7ce9c9275635dd1df`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.14.0
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:39:53 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:39:53 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:39:53 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:39:53 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23714c84328ef3f37492a90472403973b73231e81a2513a552b86e56ddd87a77`  
		Last Modified: Thu, 09 Oct 2025 08:00:15 GMT  
		Size: 459.4 KB (459428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041acd6a0342a5e9ba08501118a1e8fa5ad671026c22bd2f56316acaa9be04d8`  
		Last Modified: Thu, 09 Oct 2025 08:00:16 GMT  
		Size: 14.0 MB (14006700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e678197fe9f381ed3e2d0f4ad199fde8e9209b28ac7adb042dd67e22a702410f`  
		Last Modified: Thu, 09 Oct 2025 08:00:15 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756d837c79dcb9da698b3000777cfb8ffa14770b420fef72523c6be1da4aa871`  
		Last Modified: Thu, 20 Nov 2025 19:40:15 GMT  
		Size: 5.7 MB (5717008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:77d9ca3c477b5de9a2fe7840d6cdb48ec07943fab69f58de2fae8f737c9b5caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.0 KB (638967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b33255287451a9b0c14843c918dcdc377373987424e265fd5d2d1279dc4c42`

```dockerfile
```

-	Layers:
	-	`sha256:0097005b03a9ee3da08ab026311f58b216de75a3f53c1729bc3a208748cb9b37`  
		Last Modified: Thu, 20 Nov 2025 21:20:51 GMT  
		Size: 627.0 KB (627048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a46b948c9c7463122494cd7cfacd1e2351be66b4828cb3151e8962ac8b671e2d`  
		Last Modified: Thu, 20 Nov 2025 21:20:52 GMT  
		Size: 11.9 KB (11919 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:9bb96335a40664d99e2075ce9dbff772fca6c55738954adea2a25394d4ce7f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23087502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b113ab6242c58cc49b24024f39dee7ba6b65c6dfc6c12799ed44fdc1be4f96`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.14.0
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Sat, 22 Nov 2025 22:33:41 GMT
ENV HY_VERSION=1.1.0
# Sat, 22 Nov 2025 22:33:41 GMT
ENV HYRULE_VERSION=1.0.1
# Sat, 22 Nov 2025 22:33:41 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 22 Nov 2025 22:33:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3386baf0e035ea4652fc916d5ecaf8b33fd89200acd2da378d80b4cc1fd3ee`  
		Last Modified: Sat, 11 Oct 2025 01:38:25 GMT  
		Size: 457.3 KB (457263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dc8101efdb9f31ab87072344db31eea1b253232e72cadda91a7c3eef9114e5`  
		Last Modified: Sat, 11 Oct 2025 01:38:26 GMT  
		Size: 13.4 MB (13397203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54455a71dc2a2ecb83f39f65638bbdf0e077fde58369113ddd69825cfff2e25`  
		Last Modified: Sat, 11 Oct 2025 01:38:25 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a258bda2354d4b8277183316b00c2bc182b92692870d5108f65fbd18c24dad94`  
		Last Modified: Sat, 22 Nov 2025 22:34:26 GMT  
		Size: 5.7 MB (5717547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:ed0584755e5606490d45072331547219ff835c69a66205b2c5952e9025b7418c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.0 KB (638964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c5fe5d732efbf990ae4046e56f5255d6ac2ae45f893052aad329734617208b`

```dockerfile
```

-	Layers:
	-	`sha256:468387971901ffbd6fa5a065c1df617039dd30d04e711068962e359023adf2a8`  
		Last Modified: Sun, 23 Nov 2025 00:17:46 GMT  
		Size: 627.0 KB (627044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d46994e5aee79423ef6e56db35929a9f7f78c610d92907d018fdc73875fc9afa`  
		Last Modified: Sun, 23 Nov 2025 00:17:47 GMT  
		Size: 11.9 KB (11920 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:c26fd88e82e7e7ff290a995fd25074bc131f01ad84dcd55bb6a1da7283fafc3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23553858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6954c8bf390f33c90ac7eef8e4acdce5bfe4c536634ae62e646ec245398cbd`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.14.0
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:38:49 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:38:49 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:38:49 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:38:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825710de672f5a5c7768d4c4cf259be1850b49a843e5d8287c4b28ec27b5f190`  
		Last Modified: Thu, 09 Oct 2025 12:34:32 GMT  
		Size: 457.9 KB (457905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e999498e986c1f59b4baebe579bbb69a24fbeb135657f0687c28c5a01e19bc09`  
		Last Modified: Thu, 09 Oct 2025 12:34:34 GMT  
		Size: 13.7 MB (13729515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0168f20dd57295bb57d25a722a906457a291a472ebeaa15f3e2f24f1936952a`  
		Last Modified: Thu, 09 Oct 2025 12:34:33 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140a4fda3ad6013013b5f32ceade8766d368bde0f2d46acaa125e927f9906806`  
		Last Modified: Thu, 20 Nov 2025 19:39:07 GMT  
		Size: 5.7 MB (5716942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:d341a0afc749410da76c9ab465416cabc8618e430ebb598751e59562d17a565e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.7 KB (638746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe468849f13a36b116081aa5afdc8f5ff96d8812a3a0b2c6f5269c3f580301cc`

```dockerfile
```

-	Layers:
	-	`sha256:2fd84ebc07729e43ec015ab8cd63c57c10dd60fb0228c26c3f6e3359110cfd96`  
		Last Modified: Thu, 20 Nov 2025 21:21:02 GMT  
		Size: 626.9 KB (626942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a8fe76f6db1c0d269976c01abef9f760546e6a9fb9d8ec8a807a5c494d9c9b2`  
		Last Modified: Thu, 20 Nov 2025 21:21:03 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json
