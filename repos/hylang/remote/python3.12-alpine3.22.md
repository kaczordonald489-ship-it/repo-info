## `hylang:python3.12-alpine3.22`

```console
$ docker pull hylang@sha256:9d1be7494f3b6fb4fffa103edae1c322cc33db5033e79c4ec664205d508289f9
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

### `hylang:python3.12-alpine3.22` - linux; amd64

```console
$ docker pull hylang@sha256:e9196b8a33b7ca8df5da3060732c99f862e1320fe6ff180b5e6141a40628c317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23488838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca55bfd821e0cf0dd020ee6f18fdd1c33b8d9d6824ff3b3f24766da88424d6d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 15:49:21 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PYTHON_VERSION=3.12.12
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PYTHON_SHA256=fb85a13414b028c49ba18bbd523c2d055a30b56b18b92ce454ea2c51edc656c4
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:42:36 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:42:36 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:42:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:42:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ba1c2e1d456e9c1db056c2c9ffdd5fad3455d7c5733cb29c990e7c09909bc8`  
		Last Modified: Thu, 09 Oct 2025 22:38:31 GMT  
		Size: 456.9 KB (456932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99639dbba0122b4f15f27ef4a15a2aadb33c2a22a531b2cdc6388505e207525`  
		Last Modified: Thu, 09 Oct 2025 22:38:31 GMT  
		Size: 13.7 MB (13684629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362fe14d6ada1ae5a74ed043a3daf3d5a77a321db1a4d384244e05fa73ff9d0a`  
		Last Modified: Thu, 09 Oct 2025 22:38:30 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d628b3a37a97504318fffa7d9647f21dd929fa684a4ae97f0c6ff6291101337`  
		Last Modified: Thu, 20 Nov 2025 19:42:49 GMT  
		Size: 5.5 MB (5544577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:f63d5fb00bbcf44c48f77d5a275be5563a652b8298af83e43ef45a148ac552f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.3 KB (664335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e17686f70fd81d58825b71d3d7273dfb478456a3becd7a63db7ec12766f19c`

```dockerfile
```

-	Layers:
	-	`sha256:dd22589f66706d3848d10bcb32431a23884acca014003f951120c970c444254e`  
		Last Modified: Thu, 20 Nov 2025 21:25:43 GMT  
		Size: 654.9 KB (654928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4da0cfb9069ea52c59e0f4de97083bfd82760833c2626deacbbafb56e4fedb9b`  
		Last Modified: Thu, 20 Nov 2025 21:25:44 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:17f12c3f7f01273a792ceae3a16b486a5574ada2b2270967162364c925b36b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22719573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb699a96d46f375f9b6193268f9d2d5a620f2f449704310f05f8d05d38d97ceb`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 15:49:21 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PYTHON_VERSION=3.12.12
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PYTHON_SHA256=fb85a13414b028c49ba18bbd523c2d055a30b56b18b92ce454ea2c51edc656c4
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:41:43 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:41:43 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:41:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:41:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7745ee696ce94c130002e019e3035b95a5011a6a206a04676dd1bb41b82e08`  
		Last Modified: Thu, 09 Oct 2025 22:41:07 GMT  
		Size: 457.8 KB (457751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bf52a25e023fd9b6419adc1b1aa4c45491d50ed7708205db64c1f22407f276`  
		Last Modified: Thu, 09 Oct 2025 22:41:08 GMT  
		Size: 13.2 MB (13212846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85e7d1a3710c50452d53ff58a3ada75a49cc6fc0adefd35cb5aaf557bfbc6c1`  
		Last Modified: Thu, 09 Oct 2025 22:41:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13f4a8857fc7c436feddd6338360c0130806242108bfd6c4511337d2b2eba5a`  
		Last Modified: Thu, 20 Nov 2025 19:41:55 GMT  
		Size: 5.5 MB (5544647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:cc35dd2fec803e2032f38be18f2832bd1c0651890830effbe8bb27d31b281623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b60e8cb996750611f2360108327ef4a64b70be316931a5f161d510f7e1f2e7`

```dockerfile
```

-	Layers:
	-	`sha256:a7865943833ed326f6af8bb46ffb38ae2f47a4087b9488f977f337915f14e97b`  
		Last Modified: Thu, 20 Nov 2025 21:25:48 GMT  
		Size: 9.3 KB (9304 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:58792fd44a086fc80d5337b5dffe79d851b05bb65ad538773029d704b3859839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22057243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74f2b7ef04e3ccf4f0520390152fb282c82bf982a86e35c9c8018b0f8dd205c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 15:49:21 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PYTHON_VERSION=3.12.12
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PYTHON_SHA256=fb85a13414b028c49ba18bbd523c2d055a30b56b18b92ce454ea2c51edc656c4
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:43:34 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:43:34 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:43:34 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:43:34 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e815ffbb78eeac1f23cc99c4def7045284b5b1b3e96cf3c44ce00a080777cd`  
		Last Modified: Thu, 09 Oct 2025 22:42:02 GMT  
		Size: 456.9 KB (456929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c054b294195bfe3252b34c14188207fe0f118335a9573320a59e0335c7074e8f`  
		Last Modified: Thu, 09 Oct 2025 22:42:02 GMT  
		Size: 12.8 MB (12833854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6257194677a6f33a5b4dd138ad2ddea4dd573e1f68097f5a2b92580cb47c1288`  
		Last Modified: Thu, 09 Oct 2025 22:42:01 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d293bbf9679ea8e180170b6f830cfd0295ae52b544e02f054d81cf65f7cd92`  
		Last Modified: Thu, 20 Nov 2025 19:43:46 GMT  
		Size: 5.5 MB (5544657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:68c9727b034f6d36985b88be4ae1e81ed26415f266e5093fb3ed96abd74c08bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.5 KB (667504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3eeccd72e280c4a2a85cec8611f95576f29a1fb29a92ab67c739326066044f0`

```dockerfile
```

-	Layers:
	-	`sha256:2cd757e82ad8f4d864f4511b17ddaa8801ecc3bbdded62eeeb71d73432881ce9`  
		Last Modified: Thu, 20 Nov 2025 21:25:51 GMT  
		Size: 658.0 KB (657986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0df6e8fc1bed420ed008f84001c45ad9d5ae9a8f267e54135b895c1d4cee80f0`  
		Last Modified: Thu, 20 Nov 2025 21:25:52 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:c16665069f1bf48d4dbe913084525ab9cfbbca4e691d60ce348c7eb5f9824855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23872436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a8df6e612a68993e58fc2cadfc6983fc8be943bbc852e995a8921739a4d0de`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 15:49:21 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PYTHON_VERSION=3.12.12
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PYTHON_SHA256=fb85a13414b028c49ba18bbd523c2d055a30b56b18b92ce454ea2c51edc656c4
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:43:12 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:43:12 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:43:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:43:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea766752e87d00f8d063c3dd79843a5e8d8743aa2768bce48f88829f65c5254`  
		Last Modified: Thu, 09 Oct 2025 23:15:18 GMT  
		Size: 459.0 KB (459009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8267e2da03f4abde02977efd44c4dd2422b35435b8cfd5b7088dbde1c3850e`  
		Last Modified: Thu, 09 Oct 2025 23:15:20 GMT  
		Size: 13.7 MB (13730464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c203602dfd4741f6cebe0a4c9b87a66ca11b201e5ec2ec7878ea712059e154`  
		Last Modified: Thu, 09 Oct 2025 23:15:18 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cc4ecf403ee245ad877c7c38d7cc25f153be66a7068f9283a47642e5a94bcf`  
		Last Modified: Thu, 20 Nov 2025 19:43:26 GMT  
		Size: 5.5 MB (5544645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:b42ca31de13c19feb5961aae94f4425606aa6c0c31c2929847191c82e4131cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.6 KB (664591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219383de2e0f8bf565c05387dcb55885eb5e9e3985b81ca7ae0c5935bc149f9e`

```dockerfile
```

-	Layers:
	-	`sha256:330570a3ba4a4fed57cc9b1003e05edb3ccbebbad00e29965393dd0cb6ee3965`  
		Last Modified: Thu, 20 Nov 2025 21:25:56 GMT  
		Size: 655.0 KB (655032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:892e8ac94139ad16384d76d8415e7a40829c21308dcbe89426f6aa081eaedd01`  
		Last Modified: Thu, 20 Nov 2025 21:25:57 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:cf5a984d4f22449d26bf8ae7dfc69b4462181bee2dd00a92115962276c53f17d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23533459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a9fa03d7d298e4d839e94fe1ad462397a23bbf03360cdd44cef849cec13bb4`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 15:49:21 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PYTHON_VERSION=3.12.12
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PYTHON_SHA256=fb85a13414b028c49ba18bbd523c2d055a30b56b18b92ce454ea2c51edc656c4
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:43:37 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:43:37 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:43:37 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:43:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5275af2a50271bb641713ab1e4ddbc1ddf1fb7b5142b2c062839457623c4b4f1`  
		Last Modified: Thu, 09 Oct 2025 22:40:58 GMT  
		Size: 457.4 KB (457367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed29bc2f18c12edf56a3286fb765d6e3303a892e16503e93dec50e8029c1b4a`  
		Last Modified: Thu, 09 Oct 2025 22:40:59 GMT  
		Size: 13.9 MB (13912344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fdf80329abe46fffc4696a20d22845fffc00013fac7617eb3050c8ce28908c`  
		Last Modified: Thu, 09 Oct 2025 22:40:57 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7ca102413a8c7d5fe9d3f472590a19fe586c7bea33cc9c8d72af165a7addbb`  
		Last Modified: Thu, 20 Nov 2025 19:43:47 GMT  
		Size: 5.5 MB (5544568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:17043eb8d0f5628c19ee76f167bcef5f5de65055fbf211b713837bc8b6c433e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.2 KB (664238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03678628fd5cfae95971ea087bf0bed092a84379e400d42fc30ce2d552745c8`

```dockerfile
```

-	Layers:
	-	`sha256:bdebfe1c2c50a88c10a9c182daeac101cf135a5a5be834dbf6177b82262c6ad4`  
		Last Modified: Thu, 20 Nov 2025 21:26:01 GMT  
		Size: 654.9 KB (654883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b63bb6202226ae13039b8d42eb96d182668ce208946ef33adaa38a638e737e5c`  
		Last Modified: Thu, 20 Nov 2025 21:26:02 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:0f39580e4fb872adbc8cc0cfe098b259d8a3550673a68401adebd2a0ce805473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24195047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47957c88abcb736d831b3580a8cd4081dcd6af137d53bc7c109fc6b64ec5b443`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 15:49:21 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PYTHON_VERSION=3.12.12
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PYTHON_SHA256=fb85a13414b028c49ba18bbd523c2d055a30b56b18b92ce454ea2c51edc656c4
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:45:06 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:45:06 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:45:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:45:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d59558aec49aa561bba128776098134d977c895162d47f6feb60e130039a68`  
		Last Modified: Thu, 09 Oct 2025 08:28:28 GMT  
		Size: 459.4 KB (459435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebd1b5174efcfae30eee80ac7968ae88dae13d2caefa65b9a6b97e30af783a2`  
		Last Modified: Fri, 10 Oct 2025 00:53:01 GMT  
		Size: 14.5 MB (14458497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b42fa32d8ab8ac4c04330071daaaf25fd0a4fe7a5fd4ab13ba2c4793c25a45`  
		Last Modified: Fri, 10 Oct 2025 00:53:00 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee1efa932350d17ec4b7d31cf8c258d01d957be2c29ef71caff8bcd6fd29084`  
		Last Modified: Thu, 20 Nov 2025 19:45:28 GMT  
		Size: 5.5 MB (5544622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:fb2a761ba8ee96377acd9ee8225952d5158a28a62ad9b36fe235a63142498918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.5 KB (662510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bd80fbc3172c05c445c08a9f2e12fc2578a0fff851d842f23e658df9721810`

```dockerfile
```

-	Layers:
	-	`sha256:72b5aef657dbe991a863ff2c189c8e26fac1c2ef1e3fa48b9a5cf3ec8286eec4`  
		Last Modified: Thu, 20 Nov 2025 21:26:05 GMT  
		Size: 653.0 KB (653035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a99579df074183386064cec3806a9862ec076f2e4b64d4b1bc94f1a01009d58`  
		Last Modified: Thu, 20 Nov 2025 21:26:06 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:429def401e5861692fff626af4230b1557c05b4f2ecc490dc77724b9d7408945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23244526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ddfcd4b18d378f92d2231c82e7006133197b94f8345f9b4b6b85bb5bea1b70`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 15:49:21 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PYTHON_VERSION=3.12.12
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PYTHON_SHA256=fb85a13414b028c49ba18bbd523c2d055a30b56b18b92ce454ea2c51edc656c4
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
CMD ["python3"]
# Sat, 22 Nov 2025 22:58:10 GMT
ENV HY_VERSION=1.1.0
# Sat, 22 Nov 2025 22:58:10 GMT
ENV HYRULE_VERSION=1.0.1
# Sat, 22 Nov 2025 22:58:10 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 22 Nov 2025 22:58:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879bd470fd11b0111acf6d20db06ac6a0b955448eb55f42b1ca31bc17c8f4dd9`  
		Last Modified: Mon, 13 Oct 2025 17:53:31 GMT  
		Size: 457.3 KB (457271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d021f724a5258839c12e37342dd36675207a4a0433c2b59ed8016304a78ea36e`  
		Last Modified: Mon, 13 Oct 2025 17:53:33 GMT  
		Size: 13.7 MB (13726581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fb97392e7093ca4747dc8b587aaff2c48e7f3b452eba3ac5e1325d5f138f56`  
		Last Modified: Mon, 13 Oct 2025 17:53:31 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d46cc99661e91adce9e188772f760111a40fe2e5615f2afab76427adf415e48`  
		Last Modified: Sat, 22 Nov 2025 22:58:54 GMT  
		Size: 5.5 MB (5545183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:ae0110ead92cfe152f91591a8f5972932dcaf9895efbf406627aaf2fc438ede3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.5 KB (662506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4720b078d9268a9a7ec8958b6e0e2cb2a69026c03e8b6375e0a76132f2782d3a`

```dockerfile
```

-	Layers:
	-	`sha256:edd730f758c08f96b78fc998d12d06518411babe757aa6164b6ec39312b9e55d`  
		Last Modified: Sun, 23 Nov 2025 00:21:03 GMT  
		Size: 653.0 KB (653031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2840f5226e86ee7201a5fefc071278b7b88514d02e89bd45229e20eb3779ac88`  
		Last Modified: Sun, 23 Nov 2025 00:21:04 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:140cd478d70e853b755c3703266519d2b10f79f6269bffceb19ad1ca15d4ed36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23860700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f97ad94fb35e65bd1243968f79902dc3593b502cd9b4fdd70bbeef4ea911321`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 15:49:21 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PYTHON_VERSION=3.12.12
# Thu, 09 Oct 2025 15:49:21 GMT
ENV PYTHON_SHA256=fb85a13414b028c49ba18bbd523c2d055a30b56b18b92ce454ea2c51edc656c4
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 15:49:21 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:43:40 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:43:40 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:43:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:43:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4929a7616ec9e65e89e8fc96cf51868212bfa5dfaa51e5a68686d2f0903e035`  
		Last Modified: Thu, 09 Oct 2025 13:00:09 GMT  
		Size: 457.9 KB (457909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cad96a7c633253553252c05642e5a3fda908a67509b84fddf9ae657b80dd26`  
		Last Modified: Fri, 10 Oct 2025 03:01:09 GMT  
		Size: 14.2 MB (14208759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53be548c8dcb2459f2c3f2996fb4ff5bba2040bc48fef1bd193e6983220ed462`  
		Last Modified: Fri, 10 Oct 2025 03:01:03 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3238534e823733d0bee86bf6c9230cf393d2fbd829a7cb12bc3411d6903fb8df`  
		Last Modified: Thu, 20 Nov 2025 19:43:56 GMT  
		Size: 5.5 MB (5544541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:f331c222ddff104b28beb2e6f555b6c8d4175b9194a6a177567b9b5a84a9c87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.4 KB (662383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f60f731a17d217e98bc24833ef9358dd565a864a9e10740bdeeb4ca8366687`

```dockerfile
```

-	Layers:
	-	`sha256:8ee72984bd9683aeba15dfdeb6fe97dad01d2d43aa71478f93b5e63022b58859`  
		Last Modified: Thu, 20 Nov 2025 21:26:13 GMT  
		Size: 653.0 KB (652977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca79b9b6e14a9f66b6b20a340ae11703c9dc63babfb65c263c1bdad2b57c216c`  
		Last Modified: Thu, 20 Nov 2025 21:26:14 GMT  
		Size: 9.4 KB (9406 bytes)  
		MIME: application/vnd.in-toto+json
