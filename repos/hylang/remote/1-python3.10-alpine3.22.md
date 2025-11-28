## `hylang:1-python3.10-alpine3.22`

```console
$ docker pull hylang@sha256:8bb12c7cff8190909801148cc600647f7fbb9bc6a1e9c18f5f2a64367e57a9eb
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

### `hylang:1-python3.10-alpine3.22` - linux; amd64

```console
$ docker pull hylang@sha256:5a4d1f68cf369fc6d8d78b10b5ce8bf8ef3919bc4d081231a91fe39a403e3b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24925333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e797d7de63e7131d985527c419de22439677920ec565ac8e801afe120d92c43`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 21:44:07 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_VERSION=3.10.19
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:44:22 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:44:22 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:44:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:44:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6919b1d38e53ccdc8cbb29e0abc43a8479d26bda83c438c3d88edfed60f3372`  
		Last Modified: Thu, 09 Oct 2025 22:42:31 GMT  
		Size: 456.9 KB (456922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7714f75ddfc2be8cf74030a638884b5a2255a05dfafb8f6b1a00a29c8db44863`  
		Last Modified: Thu, 09 Oct 2025 22:45:33 GMT  
		Size: 15.4 MB (15386896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9463c33f02cb04bbc185fc1084b80cdda25a6d998debeda9819947253e5c1b48`  
		Last Modified: Thu, 09 Oct 2025 22:45:30 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123d0301de79d357ed4d37813195787b8689690e93d953bd989eeddffd37bb6c`  
		Last Modified: Thu, 20 Nov 2025 19:44:36 GMT  
		Size: 5.3 MB (5278813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:48f7152900cd71d345d031f763f92e1078a9ade8b278da66ae99925c4cbc9b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.4 KB (709378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9d630c4b2b1af03fc83b607672e340383612295864694f1dcc8b3dd2a8722d`

```dockerfile
```

-	Layers:
	-	`sha256:ef6ccc8337f3677b082f867257667db9d976fa14ae3ba55333df19b749535439`  
		Last Modified: Thu, 20 Nov 2025 21:22:42 GMT  
		Size: 700.0 KB (699971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51cdf1df1d333a27633afca2f6e104715c0e2c11a5f7f616374106272f2f4323`  
		Last Modified: Thu, 20 Nov 2025 21:22:43 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:d93654d9ac93c9bcdbcd26c5415392212729bd30e15b859eddcd9df0c3530798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24207263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355ce33c699aceb032bc22af4fb1530ee5e61f11eb78db8469ba524fead90c8d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 21:44:07 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_VERSION=3.10.19
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:43:27 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:43:27 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:43:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:43:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4520e26c4d6c143e67ba3e19216f0e624eeb3daa7c50276dd03168cdd933f09c`  
		Last Modified: Thu, 09 Oct 2025 22:52:01 GMT  
		Size: 457.7 KB (457737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f6ad5c9e5312665da4b2af58fab290c37df2256774c0beb3fb3c1dc2619b32`  
		Last Modified: Thu, 09 Oct 2025 22:52:02 GMT  
		Size: 15.0 MB (14966384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc7fe700b60fa68f219db460b2bd4d0db5c5fbb041996c3a7844077e7512d44`  
		Last Modified: Thu, 09 Oct 2025 22:52:01 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2317f593c6514977727ac7620efa87dce9e3018b669c66fafb0faccdba7365`  
		Last Modified: Thu, 20 Nov 2025 19:43:37 GMT  
		Size: 5.3 MB (5278813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:383897adee708b828302f79f88fd662eb37d93122d943b8b78bc7f4024a1a5ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0a48e1971f6e8126124aa03b8c665bc800860e398d93ef129472345c305bcc`

```dockerfile
```

-	Layers:
	-	`sha256:a3b89656ac2d9021a65df85add5892b337f0982b79b42aa8ad236449ad4ba9a4`  
		Last Modified: Thu, 20 Nov 2025 21:22:46 GMT  
		Size: 9.3 KB (9304 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:4782d6f175e481c5ea8c0da1ca7f5d7a6906ba3084fff64ae304ef85a9e00d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23522509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1af1b0615bb2c390da6092923f8e657eb7b8bd6a895bae79e0615c418b1dd5c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 21:44:07 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_VERSION=3.10.19
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:44:39 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:44:39 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:44:39 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:44:39 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897ce543693bd5e087e24f84349c4333e07c996591bab9754fb042fb2c94dda7`  
		Last Modified: Thu, 09 Oct 2025 23:21:02 GMT  
		Size: 456.9 KB (456931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20944f87593f31ae289df49927ac635b3e92c25fc1b6210aada9bddedb5298a`  
		Last Modified: Thu, 09 Oct 2025 23:21:04 GMT  
		Size: 14.6 MB (14565062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225f60df7475bedca555fbc548c3c4aa7c86c4365128e23266decbb16c5a7a86`  
		Last Modified: Thu, 09 Oct 2025 23:21:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7ab46371ba43c866710e0b4c294f8443711eee09a482ec31de59c475ccd130`  
		Last Modified: Thu, 20 Nov 2025 19:44:51 GMT  
		Size: 5.3 MB (5278713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:1643aeadaf0e7799e21c26420b0a1b46a9a1756eabcab89841dddef7b285d753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.5 KB (712548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562fb43df2b747d29c4d0afae84eb2c8827c3280d69293e334b225a0d05ccb22`

```dockerfile
```

-	Layers:
	-	`sha256:43e0899f04c02333ec1316ff17336518dfecb99a83e2b515af74c561cb0b8d36`  
		Last Modified: Thu, 20 Nov 2025 21:22:49 GMT  
		Size: 703.0 KB (703029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09a01dfd5323fce8e44cfcb7073f803410a06096220c5a82bc8b4722cd0a0c67`  
		Last Modified: Thu, 20 Nov 2025 21:22:50 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:fa1d5f186146dbe70f054adc2773cde79096206de046b837c7580d85d7e95ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25319560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80dc4ff11e17b4b167fb661b5cd0fed343ba8a840295107435435467fb08c36a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 21:44:07 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_VERSION=3.10.19
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:44:21 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:44:21 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:44:21 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:44:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5767682a7f5ada1bbc82a32ed7452f6ace6f5aabfc82ec197c2fcfd2238dc525`  
		Last Modified: Thu, 09 Oct 2025 22:49:15 GMT  
		Size: 459.0 KB (459007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115d3fa080d3ab57202dcf15333cbb02db8dfa71cb4d79ff7251e5879269843d`  
		Last Modified: Thu, 09 Oct 2025 23:15:52 GMT  
		Size: 15.4 MB (15443428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec6c3ed91d8b004b1c3416b006bf0f6d3299171b57b2ef58cdd20dc7581734a`  
		Last Modified: Thu, 09 Oct 2025 22:49:15 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0956a219c05488879653858f7ea48de669d926063296e41fa844e862387455ea`  
		Last Modified: Thu, 20 Nov 2025 19:44:33 GMT  
		Size: 5.3 MB (5278808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:06fb48965dae4950a8aa3e0c300a99a3e1e7ccdd1175a8a3fe80e81ea43b767f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.6 KB (709633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87257c8810fef834511daf25eac73cfb0a963e22cb1e45b023db4240ce666ab1`

```dockerfile
```

-	Layers:
	-	`sha256:a37d868ed021cb8ccde1fed0d0ceeeaf326482cdd84010efd5305c66fd5b8468`  
		Last Modified: Thu, 20 Nov 2025 21:22:54 GMT  
		Size: 700.1 KB (700075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16b58168f391bdac2ec1877822382df20ceb332a23100355e02c3880e3c63b76`  
		Last Modified: Thu, 20 Nov 2025 21:22:55 GMT  
		Size: 9.6 KB (9558 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:f3eebb0bf363003909003ebf112027f1272d74b2b05c318d42d13ec6067f1d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24981404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699f3d91e2a888396c8951f84385327a16649703e02e4bea9ba7e0b1afa52f54`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 21:44:07 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_VERSION=3.10.19
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:44:37 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:44:37 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:44:37 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:44:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435956c4a76f6a0ceacdf8cd884d1786b8d5410b2690ad525a2f9546449b122b`  
		Last Modified: Thu, 09 Oct 2025 22:49:01 GMT  
		Size: 457.4 KB (457374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c509e173ea6f5b8661cc72fa9f728788fe309b7f27760ab86acb4cd48a1a06`  
		Last Modified: Thu, 09 Oct 2025 22:49:02 GMT  
		Size: 15.6 MB (15626157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd955eaccb9bb1823e76329bff2a277313b336bb566cc80adeb06e58176bf55`  
		Last Modified: Thu, 09 Oct 2025 22:49:00 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a39cbbcf8bb706bad13af255c29d5b9d0c505eb3aa2c75de0209abb3862f97d`  
		Last Modified: Thu, 20 Nov 2025 19:44:49 GMT  
		Size: 5.3 MB (5278692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:e31ea08fbcd9721f4924581822800bb247a1d4230236862400c7f4039eabc011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.3 KB (709281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9382ac1ad72b5c7b12d13294e6c5bb8b7caff19430c40a47e54173ae88a4b1`

```dockerfile
```

-	Layers:
	-	`sha256:d1e0413ac392aa86c5327f0073e49bb659fc1676be19ae7c92673d19ecea1db4`  
		Last Modified: Thu, 20 Nov 2025 21:22:59 GMT  
		Size: 699.9 KB (699926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68549d041688cdaa7473b492496dc047638eabbfd146f33ec6287f63f3cc8edb`  
		Last Modified: Thu, 20 Nov 2025 21:23:00 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:48cd18e1edb34e5005adfc4bff2757d7d8e6078511e27d236c47e85f652022aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25555250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7628c67173a3ccc19e426ba0597185704bb73d066ac53d2fdcd64be54c9583`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 21:44:07 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_VERSION=3.10.19
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:49:53 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:49:53 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:49:53 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:49:53 GMT
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
	-	`sha256:6bc6099de0aa36de5487e974a3bfbb5628f7f7b602483bdcd38e47235345bb98`  
		Last Modified: Fri, 10 Oct 2025 04:09:05 GMT  
		Size: 16.1 MB (16084467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb995851c32d392bd0b216e109af3e115b840aca397cc59291e7aba1b0e4fddf`  
		Last Modified: Fri, 10 Oct 2025 04:09:04 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce70ef4515309a336b932781f0d5a4897b630e60531a12223c9b44b6b953cb3`  
		Last Modified: Thu, 20 Nov 2025 19:51:15 GMT  
		Size: 5.3 MB (5278858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:014337f30887cf5a3e57b3007847d629a126517a9345e2e4a23fe995091ccf2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.6 KB (707553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056397ed29ff66ed59921ae646c7dff6166636b2117bb574e54fdd8d50183f0f`

```dockerfile
```

-	Layers:
	-	`sha256:00021bd49a399358581aec0af9ea7f006aa71884b2cd77226a91d88aaa66366c`  
		Last Modified: Thu, 20 Nov 2025 21:23:04 GMT  
		Size: 698.1 KB (698078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:635189e125c91e0fc71f4ea9bcffa444e22eea111998390eecf0e5816c9422d3`  
		Last Modified: Thu, 20 Nov 2025 21:23:05 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:cb2b7fec4e41a4e3d5d9130d348b29e7b73b61c73a56df38de50a943f8965ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24649808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a9002dc8ad10a08f0b6560015bf0f29c6201f5f05cfb3eebd89d22722224dc`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 21:44:07 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_VERSION=3.10.19
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
CMD ["python3"]
# Sat, 22 Nov 2025 23:22:12 GMT
ENV HY_VERSION=1.1.0
# Sat, 22 Nov 2025 23:22:12 GMT
ENV HYRULE_VERSION=1.0.1
# Sat, 22 Nov 2025 23:22:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 22 Nov 2025 23:22:12 GMT
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
	-	`sha256:6a4dc7ef6d9a1e223056ee4cb7e98ce6f17549cf217e94f7710d9ff0ab8f54cc`  
		Last Modified: Tue, 14 Oct 2025 09:26:11 GMT  
		Size: 15.4 MB (15397340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b834f7edc24ff071efdc807f769a04b98da622282387384aa29cbca534e44102`  
		Last Modified: Tue, 14 Oct 2025 09:26:10 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a135d42664728e6b54cfad21271a1e893008be6468e35c0609812622c88c5df`  
		Last Modified: Sat, 22 Nov 2025 23:23:00 GMT  
		Size: 5.3 MB (5279707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:94ce548e87a5feef10e555b884748e3986ac45f6bc496db2484a5ffcd5efa88a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.5 KB (707549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec755beaa66fcb9d8c0dbf794544a5a3f16a11fcfa1fef72d109d41ce9c20f1`

```dockerfile
```

-	Layers:
	-	`sha256:7613e069b276816a7a000077273f03db10b1c50405c7d61f9ee6f9eb1442918d`  
		Last Modified: Sun, 23 Nov 2025 00:18:13 GMT  
		Size: 698.1 KB (698074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84d12af858960821712498a7dc296b6c0da1d79e6cbd8060c6029205d5b95791`  
		Last Modified: Sun, 23 Nov 2025 00:18:13 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:c8c75b39f67858542d9af9ccded1840dff344c735d4780d7f1b242e01aad3f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25184069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ed74f1bb225b81c2d5c28eda27f7807bf9839696ced82894903ae84c70c924`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 21:44:07 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_VERSION=3.10.19
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:45:34 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:45:34 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:45:34 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:45:34 GMT
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
	-	`sha256:894c40495d120caf4fa7d68aa78849cb6b41de7dcdadab7f4f3df83b78336b9b`  
		Last Modified: Fri, 10 Oct 2025 04:54:21 GMT  
		Size: 15.8 MB (15797949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595c845ea3e91fd188d4afeb767557a097b17e817779fbaca7c5b429789834df`  
		Last Modified: Fri, 10 Oct 2025 04:54:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c57eedd2236823033cb9873964d6eab2a312bd311a2d4ba11801ca0eb7695e`  
		Last Modified: Fri, 21 Nov 2025 04:44:23 GMT  
		Size: 5.3 MB (5278719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:43d1dd9d9f89a981be344e8409251c4e7a1feb1dbb82d53bf33be1b6e8a0a5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.4 KB (707427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f033adef776579bfc30f0341206e9a8dd0fa8cfaa25732f3d7c463475d215af2`

```dockerfile
```

-	Layers:
	-	`sha256:926ad45606e66125e1c81511a2e3513507a676c81180c3d1830407e6feb0580a`  
		Last Modified: Thu, 20 Nov 2025 21:23:11 GMT  
		Size: 698.0 KB (698020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc6fa92e8ed76f51bdbbd4e2c6bc69257456be8abfa196fd9559d8ebedc23509`  
		Last Modified: Thu, 20 Nov 2025 21:23:12 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json
