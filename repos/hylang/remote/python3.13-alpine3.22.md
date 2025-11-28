## `hylang:python3.13-alpine3.22`

```console
$ docker pull hylang@sha256:a1feead48e7ab3ee0469196b4a241932a442ebd6b18b690e90b7c0244962b884
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

### `hylang:python3.13-alpine3.22` - linux; amd64

```console
$ docker pull hylang@sha256:63c8c1746bf7881866399541bd2b2d005a3b6ebe875b57adf9b241ea6512d542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22131961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fa6dff085ec62cad362ef56945fdd659b48316ae351793c1b674d8dfe9522a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:41:12 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:41:12 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:41:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:41:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24e45344b415b3025bddd3c7795b3b3f9883beea1dc700ee52587c432184eba`  
		Last Modified: Wed, 15 Oct 2025 17:11:24 GMT  
		Size: 456.9 KB (456923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1a564c7d4a34452712d895e8047635d9a6ba701e9f526f403907ed67d7c780`  
		Last Modified: Wed, 15 Oct 2025 17:11:25 GMT  
		Size: 12.4 MB (12379126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6fa290b4c73bf1d47f30315e9949e2fbfc992ad584f6318856c72555b253db`  
		Last Modified: Wed, 15 Oct 2025 17:11:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017cccdd3a3720fe2043ff1c33ce957cc4556d4ac04269c9646e6f1a48b473f9`  
		Last Modified: Thu, 20 Nov 2025 19:41:27 GMT  
		Size: 5.5 MB (5493212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:da9afaf7e98d448be21172ab5f9b7d3dd6cdf96a5680598977994194aa448bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.8 KB (632767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697f366763ca3ed4c8259208e352b211f508d1938f69bef41c533a3651456083`

```dockerfile
```

-	Layers:
	-	`sha256:5c06fb55f7c2b90f81645c6dbb1db81e0562dfc6b083f96d68f7d2d298ea14e6`  
		Last Modified: Thu, 20 Nov 2025 21:27:22 GMT  
		Size: 623.4 KB (623376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec15afcf5669b96c72aec9a72a642822432d5f29aa613ada2d00429ee794ea4`  
		Last Modified: Thu, 20 Nov 2025 21:27:23 GMT  
		Size: 9.4 KB (9391 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:c7cfec2a45d1f74d1ac0f55a2d5164be12157d27ac5ac39082e51dd7a672c1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 MB (21452921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02cdd8ed392cc789b4804f4c9415aedc7e7d6906520c2cb1fe4a353fe6582095`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:39:50 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:39:50 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:39:50 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:39:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02e4f3cc3a4565fdc6d682b29ff1086172ec601449ffc64ff35a5ec7180a85`  
		Last Modified: Wed, 15 Oct 2025 16:49:37 GMT  
		Size: 457.7 KB (457746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf2697a8cd57899655b1f12b5240de1679df2f3af8262e1bf9cb246077e1211`  
		Last Modified: Wed, 15 Oct 2025 16:49:38 GMT  
		Size: 12.0 MB (11997565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f5f8f921b37496f0e5be4773922e5634bb1b910bf7be6590e5d04d6fe24e6b`  
		Last Modified: Wed, 15 Oct 2025 16:49:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3ba29888f51209782cb2180ccdd7353bde4a6f5d545d6feed49557f4d6baf`  
		Last Modified: Thu, 20 Nov 2025 19:40:01 GMT  
		Size: 5.5 MB (5493282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:933269c7dc24b43b5c833db9e11a1e4747cdded9381c79b9acf03a3e618d1b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443470593e74bd3784326fd9b917ddccda760bd798714e902fe6f5c82e0b1bcf`

```dockerfile
```

-	Layers:
	-	`sha256:64f30fe2c1286255f58e0fd5796d864f56c0f1349fb1d3df3464390e96c020fc`  
		Last Modified: Thu, 20 Nov 2025 21:27:29 GMT  
		Size: 9.3 KB (9288 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:4cda84ffd8fe22832a9e8ca96392fc9c9b72d01790ebf04c7782db47f4ee3f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20846064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5aa3e9a07f260f5beeee0db4e34652dd949fe717e668b2fdef7825abc3aa8c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:42:24 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:42:24 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:42:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:42:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dae11c7ce712c3188f32a226f09e34ce659930bb9a74419bf4af9616329f62`  
		Last Modified: Wed, 15 Oct 2025 16:57:32 GMT  
		Size: 456.9 KB (456927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e1e247a2a02da52add9d5e26dc2d2baddf4acada7748fe6a03498ef2d0e41b`  
		Last Modified: Wed, 15 Oct 2025 16:57:33 GMT  
		Size: 11.7 MB (11674057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d314d7266a9f081fdcfbdc2b51e3151abf866e95a4df136913586c3553a44fa7`  
		Last Modified: Wed, 15 Oct 2025 16:57:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee0e7e2109ab7e428131a0eb339cd1b04804f15d4679e6e20e8a757bc55a44c`  
		Last Modified: Thu, 20 Nov 2025 19:42:38 GMT  
		Size: 5.5 MB (5493277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:d3643768f5ea2e189e51cbdd5ddc045c3ece8e8e57c17d1ea12965c891b341c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.9 KB (635936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ab68263a8596cd32053930023e0a8ff2cef3bfbb9ad20de6c6795ee0dd57e7`

```dockerfile
```

-	Layers:
	-	`sha256:8ea83b19d95f2a2798e7e38cd2859c9e2af2346a6be0f4441f0fb73c1576cee8`  
		Last Modified: Thu, 20 Nov 2025 21:27:32 GMT  
		Size: 626.4 KB (626434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7e91ed5f90078ad5a38b8736ff6912e773203917834d8ecf0c57e15f99e15a3`  
		Last Modified: Thu, 20 Nov 2025 21:27:33 GMT  
		Size: 9.5 KB (9502 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:80e591e5ac5a2d4283f042e5012c9ed2504708f3fc4ebc48ffdaee2ec164d650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22484586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73605a4ab8b64d23406aadd786ea9ca8909c6e87fb798565309450dd21f64a1`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:41:42 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:41:42 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:41:42 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:41:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71263fa570a63eb3dfff44620561237a401f3196cb998cefa48b23c32c0f4abf`  
		Last Modified: Wed, 15 Oct 2025 16:53:49 GMT  
		Size: 459.0 KB (459011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e82d8615442035e9072f7ebebbfdc82f06194b454d313168e5ff21f02bcb14`  
		Last Modified: Wed, 15 Oct 2025 16:53:50 GMT  
		Size: 12.4 MB (12394016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a365b55c38e78952efffd43d7cd4a850e08c2651eee738ae437bb5e8599df70f`  
		Last Modified: Wed, 15 Oct 2025 16:53:49 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0073c5fa086f8b723ff7e1ed821f96eea20bc0c8ba2d171815734fcddb0c6c51`  
		Last Modified: Thu, 20 Nov 2025 19:41:59 GMT  
		Size: 5.5 MB (5493242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:cb3fcb6d1f3207c3b0ac6faa71df77021902317d73c801baf48ad370c67f2549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.0 KB (633023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c33e7be16c1b3f10982ac85ab80a1f7cd48d95b36d4c78bbd833794eead9071`

```dockerfile
```

-	Layers:
	-	`sha256:4e7936c6c266aa0a4ab7483a8b37c67205ff29807a575cf290c95a610c949ccc`  
		Last Modified: Thu, 20 Nov 2025 21:27:37 GMT  
		Size: 623.5 KB (623480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89aedd8d8ab665eadc3e3362f71b14a630bf62aaf581abb815603cd3dd2579fc`  
		Last Modified: Thu, 20 Nov 2025 21:27:37 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:fe39e3d37f5b8f8f628a8685c8441ebbca3923cbe0be2e5f3e0f62e9b7e98bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22204358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613edcec4fdf8e2cf3f186dbcca9d1392e3d985d773766f7f1d69fb48562529a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:42:32 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:42:32 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:42:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:42:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7cf655b6483b0826a9217a18f518ce3f101d68c7d578c33e94c53155341d4e`  
		Last Modified: Wed, 15 Oct 2025 16:51:10 GMT  
		Size: 457.4 KB (457373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d017901a61343661e85de32cc65ee8097bb4ffbc6c26e6fe7db57ca98c02b0`  
		Last Modified: Wed, 15 Oct 2025 16:51:14 GMT  
		Size: 12.6 MB (12634549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8788d4a5dbec5607a987af531f4ea1030e25153c167071eb709b6de3395d488`  
		Last Modified: Wed, 15 Oct 2025 16:51:10 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25d3d528617f67e814563c86bc9d3727bfb19877b7dc47c430a4293dac501c6`  
		Last Modified: Thu, 20 Nov 2025 19:42:45 GMT  
		Size: 5.5 MB (5493255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:d3a46de0d5a07e513f31a853413121291162d12818fcceb0907cb93745d1d3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.7 KB (632670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cedd7a49194c3f08e1e1a1617813f5869b9ba9bef3c3f0be19f8e5f6526559`

```dockerfile
```

-	Layers:
	-	`sha256:7c58a748a31a8ff92b944deb3964a68303da9b364e3ddc145ed7390f61e45a75`  
		Last Modified: Thu, 20 Nov 2025 21:27:41 GMT  
		Size: 623.3 KB (623331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5bfebaa87089cafd3dc4d707858a5423b96712ca4127e1005557ba9b420c921`  
		Last Modified: Thu, 20 Nov 2025 21:27:42 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:2ed97c8d7fe2546dbc75c33c8e19b2451f4a86874f7a218313f6c33633fd0706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22788334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3a9ca2ac34ad5200fd69b836cca7134e57f1dca9e49f3e909efe2c0c20ed70`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:43:04 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:43:04 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:43:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:43:04 GMT
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
	-	`sha256:0fb18a53c63bd02893e5f5137cc66f1ec4c8fd6c5486c04a700b762f8564c6a3`  
		Last Modified: Wed, 15 Oct 2025 18:11:15 GMT  
		Size: 13.1 MB (13103071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3d21d6f7e75f52bfcf1ddedad4146ace35b88a4e53485ade69bc15f158e810`  
		Last Modified: Wed, 15 Oct 2025 18:11:14 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df02ee096d11da6f26214faaa0f7fa50f5281f49dec0e652c9346cb8b1466abc`  
		Last Modified: Thu, 20 Nov 2025 19:43:23 GMT  
		Size: 5.5 MB (5493345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:61c6cfc1c4fc0ee161ddd45559daad928c2725df71d84ff6b30c6e886b8ec9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.9 KB (630942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6fa3875212e4a3a0c9b035a59690e81932ebc3b7f3cbf52f3cb2b8bc41c972`

```dockerfile
```

-	Layers:
	-	`sha256:708ad81e004b6aa4d689cd2d8f22902d881cf82a3a184c37005e948f7a0335ad`  
		Last Modified: Thu, 20 Nov 2025 21:27:46 GMT  
		Size: 621.5 KB (621483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b969913317803023d00d944487e215299d5463e33640a987357074e83834e5e`  
		Last Modified: Thu, 20 Nov 2025 21:27:47 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:a1ed57e077ad2ba70ec160f3f24772e049568023272739e7a57c0db2368ce8a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21913496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad12e77688a7e50b5257c0ebb9d613211defd5845b886f5c776f035f5789ce88`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
CMD ["python3"]
# Sat, 22 Nov 2025 22:45:32 GMT
ENV HY_VERSION=1.1.0
# Sat, 22 Nov 2025 22:45:32 GMT
ENV HYRULE_VERSION=1.0.1
# Sat, 22 Nov 2025 22:45:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 22 Nov 2025 22:45:32 GMT
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
	-	`sha256:0c9817292eb1fc9ec1536cf82a879cea516580480c3a4201a6bcc9b4d79af838`  
		Last Modified: Thu, 16 Oct 2025 05:32:13 GMT  
		Size: 12.4 MB (12446747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f0b3d2bf84076c840e7b2c23315ef8b51370c7805efbeb66d2e0416aba27a`  
		Last Modified: Thu, 16 Oct 2025 05:32:12 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013450a654ee977f89c70cd172e2488261bc077d84464cb6750ad0f1a5723f35`  
		Last Modified: Sat, 22 Nov 2025 22:46:17 GMT  
		Size: 5.5 MB (5493996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:2f462281fdada7acd991570108dd92e12444ff6c1b6aebf6bc55ea3117b8d5aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.9 KB (630937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869af4bad084d3c835abc1c9860b07c84244c57d254a20d471ab2f22503d1856`

```dockerfile
```

-	Layers:
	-	`sha256:8a20226ef6c62e818f93f5891a278ddd939b0b9c78be442b4a542f981ab748a7`  
		Last Modified: Sun, 23 Nov 2025 00:19:38 GMT  
		Size: 621.5 KB (621479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51fdace5fd21ba6e067d1c81f30450bbdb822db7ca81197e680a30d28f288b1f`  
		Last Modified: Sun, 23 Nov 2025 00:19:39 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:7741a1e0a636128afeecdee6fc90201a81967470561ca00d5e76a5c260cb07c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 MB (22439534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a3d2a259a5d28b79b295f1c679c3635c7fe7666d85a9fc24ab00e99360a098`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 14 Oct 2025 21:49:24 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 14 Oct 2025 21:49:24 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:40:48 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:40:48 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:40:48 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:40:48 GMT
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
	-	`sha256:ec98d65865fba049469fe400b5d69c38e507f010f68d29af057b36553b3be2b7`  
		Last Modified: Wed, 15 Oct 2025 17:46:13 GMT  
		Size: 12.8 MB (12838780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ffb40dcde2104cc8ae4166057fc3ace80f7a0f79c06a790d89d13029b642a8`  
		Last Modified: Wed, 15 Oct 2025 17:46:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f79edaa6094c2056b480cc36eee338194f3494507cea2b7361f87fd4d1f9`  
		Last Modified: Thu, 20 Nov 2025 19:41:03 GMT  
		Size: 5.5 MB (5493358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:e903f3ef6715346f27ece96e274a63495cc9d109da22eaa6535a4445aafe9193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.8 KB (630816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0180ad86ed84fc84a527ed91ab0b0730af3e6e870ce90a14423cea16c1e0595`

```dockerfile
```

-	Layers:
	-	`sha256:e49ef77ff4cf97c7afcb00a26a535463aa16b9cb88f7dfde44edb0440180ba44`  
		Last Modified: Thu, 20 Nov 2025 21:27:54 GMT  
		Size: 621.4 KB (621425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be5d13dc1a0ab7fd06a3e570a433d6660170d34c4090a5f0d5a2808a970b2b2`  
		Last Modified: Thu, 20 Nov 2025 21:27:55 GMT  
		Size: 9.4 KB (9391 bytes)  
		MIME: application/vnd.in-toto+json
