## `hylang:1-python3.11-alpine3.21`

```console
$ docker pull hylang@sha256:416f7efca8c6f8503d4baac8b97c40f86e0e78c6bc91ea915c7384bdfbc23d86
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

### `hylang:1-python3.11-alpine3.21` - linux; amd64

```console
$ docker pull hylang@sha256:2cfe8ff1bb3a741678165c46736e44592f846b48c78bf6bb0a51fe8384903c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27143102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b1ffee85e5b7362a399ed268991e5629f607f15d02117089040fa89edda77c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
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
ENV PYTHON_VERSION=3.11.14
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:43:42 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:43:42 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:43:42 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:43:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3ebd1ba813a1621555a6bdc18e809b8a5d0796a99ba8c4301bc7360dd33cf5`  
		Last Modified: Thu, 09 Oct 2025 22:43:20 GMT  
		Size: 456.9 KB (456884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785198da0926470a6594d5313507ec774462044ec1bdb979157fe8820e7ae3b5`  
		Last Modified: Thu, 09 Oct 2025 22:43:22 GMT  
		Size: 15.9 MB (15939602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce055d5792e4f0b5502dc6523fefecc00e214f20b6a849d84388d3af87c43e95`  
		Last Modified: Thu, 09 Oct 2025 22:43:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f53a43cdf7f705acee11edae306ad57f758f7aa49bf653a2e8b6e199dc14441`  
		Last Modified: Thu, 20 Nov 2025 19:44:02 GMT  
		Size: 7.1 MB (7103801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:3b7f18b753feafc0c1493ae6b9cffc64f2e4b11b53e90c5def219ec72004e11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.2 KB (705203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458efb5283b98857ebc432b460bfb8f93e5101d048250f5571e11972c29900a3`

```dockerfile
```

-	Layers:
	-	`sha256:45a373b20ebf419efdd53d166b5fcda0408eddf15a830b222aabfd5b04d75c18`  
		Last Modified: Thu, 20 Nov 2025 21:24:34 GMT  
		Size: 697.1 KB (697100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a9b11176caea9edf93ef15bb44d97042d9e32f54bcba61354788828616dd4cc`  
		Last Modified: Thu, 20 Nov 2025 21:24:35 GMT  
		Size: 8.1 KB (8103 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.21` - linux; arm variant v6

```console
$ docker pull hylang@sha256:884403d5702b8840dc8723d17d3b207d4b378c5e6979c6a258c394acb346c592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26407691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf09124c37aab596a7d385898072ab4c5a47ad34470c6ed8ed648580b6008ae`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
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
ENV PYTHON_VERSION=3.11.14
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:42:22 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:42:22 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:42:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:42:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a354d4eda470b43231cbf360a76cdb7d0ba148fa93e4cf4d4b530e71891d9c`  
		Last Modified: Thu, 09 Oct 2025 22:41:22 GMT  
		Size: 457.7 KB (457683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d8d1c4154262c8a6963f80720f54f36252f17e8e7a20e6db2323f1afdd49a0`  
		Last Modified: Thu, 09 Oct 2025 22:48:13 GMT  
		Size: 15.5 MB (15480534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bba80edf81b3f968dc3b25901f21382e8bec92bf01fbd0511647101184ac6f`  
		Last Modified: Thu, 09 Oct 2025 22:48:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921bca2382ba16d4e556a5d65469f0e318ed1e7d38c6be1ce1f6e8565108d182`  
		Last Modified: Thu, 20 Nov 2025 19:42:34 GMT  
		Size: 7.1 MB (7103758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:b90293cef7abe5744fadf53d3a6de72a7d36901bb41299133876d076d30b4e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 KB (7968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68389af51351a72a514da389b536c93dbfb657d1ae2c2df31d1bcec7e725835`

```dockerfile
```

-	Layers:
	-	`sha256:a8737909ef6b0b27a68301d2dea596dfe91ddda91d9c18b51563bf3f8f6a1551`  
		Last Modified: Thu, 20 Nov 2025 21:24:38 GMT  
		Size: 8.0 KB (7968 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.21` - linux; arm variant v7

```console
$ docker pull hylang@sha256:7e56fd3ad18b375e09014e4defe1aed5eced697a90a6360ffe7bba14ea1fab57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25739140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4473572636152f06491f8de0b3f1adb155f9ef0e9b4beb1ab31eecab64fe70d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
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
ENV PYTHON_VERSION=3.11.14
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:43:36 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:43:36 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:43:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:43:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f767143e1a5a9f1fe4b0bb8a4aee64af49886238581e51c8a7942ff60577ce1a`  
		Last Modified: Thu, 09 Oct 2025 23:17:10 GMT  
		Size: 456.9 KB (456884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc14269504a0a54c27439a3f2d849a3b5e9bf36eb14c47ec4b6060822568ba7d`  
		Last Modified: Thu, 09 Oct 2025 23:17:11 GMT  
		Size: 15.1 MB (15079625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69ce804968a85bb40b010d989f742890f00909a86730af7c34830112085a211`  
		Last Modified: Thu, 09 Oct 2025 23:17:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907c3cf6f58c79483b922e1fc73b3b7d0b69cc10d11547143034f548952df2c7`  
		Last Modified: Thu, 20 Nov 2025 19:43:48 GMT  
		Size: 7.1 MB (7103772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:7ca32c82139b1ddee0a9d138bd76cca0cc9212dc762682dede2d9780ea851c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.3 KB (708309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d40f3150040ddac1236b590ebbb4f681097d841326546ea489c4897aab059b4`

```dockerfile
```

-	Layers:
	-	`sha256:1eaa7dc95b8a301f1a34dd3fc43c9df38d877f40345dbc79bcee724a76924c3a`  
		Last Modified: Thu, 20 Nov 2025 21:24:41 GMT  
		Size: 700.1 KB (700126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc1e7fac434483e385a4f661ce2bc990efc730b99a69b46c8178ab8eef98948e`  
		Last Modified: Thu, 20 Nov 2025 21:24:42 GMT  
		Size: 8.2 KB (8183 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:5d000ff637f93afd3e533dd64eb13630d9b7d5af03a34b2f26e87635a734ca39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27572331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf3107609d203d131d8be4bca1ea5a3e325e275947e3cb3873a26e5848cac47`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
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
ENV PYTHON_VERSION=3.11.14
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:43:33 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:43:33 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:43:33 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:43:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8993f3b8a7bfec7a84525bfccc40205867214442502184ea0914489e986a8d3f`  
		Last Modified: Thu, 09 Oct 2025 22:46:07 GMT  
		Size: 459.0 KB (458981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88230c87240f0a21e2a390a275bab932da9ac46e0e362e73e5ca23e882f5d0c1`  
		Last Modified: Thu, 09 Oct 2025 22:46:12 GMT  
		Size: 16.0 MB (16017027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787d785bdfd305b4db5915c306c59e7a62818b720388d879fcfa62276bff03c4`  
		Last Modified: Thu, 09 Oct 2025 22:46:07 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe4984c62238f10dab9cc89e5b18b2eaaef73061d764694effdf48d3d5121be`  
		Last Modified: Thu, 20 Nov 2025 19:43:45 GMT  
		Size: 7.1 MB (7103722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:b26cecceba6d0c753747a29a8c02a575c14232e343dd2cd3f5dd59f11dfdc418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.4 KB (705363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a483c8f3ae63bffa54ce95e52c901aa887b0521251d647c0c65c720dfd6063ca`

```dockerfile
```

-	Layers:
	-	`sha256:36e85ae41f8105d04da54a69023027d7101bfa064d83330c0a90143225297bba`  
		Last Modified: Thu, 20 Nov 2025 21:24:46 GMT  
		Size: 697.2 KB (697156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cae1fd72a807e201ae422d448464668ec5931bc329c36b828b6777bc86d361e9`  
		Last Modified: Thu, 20 Nov 2025 21:24:47 GMT  
		Size: 8.2 KB (8207 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.21` - linux; 386

```console
$ docker pull hylang@sha256:3af61a85e369559091129fa41caf63fd8a3e40bb99d08499b497b3295d013968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27187711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a8f3b9621ac7f3f9c7eea34d5ee9a7742fc690d359f5cb08cf99b52de42ede`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
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
ENV PYTHON_VERSION=3.11.14
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:44:04 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:44:04 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:44:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:44:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c65d663be7744df6357a0e4f20b46994d37f846ccbf8bfe2b1a0d3171223ff`  
		Last Modified: Thu, 09 Oct 2025 22:40:59 GMT  
		Size: 457.3 KB (457336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d9973d3b20d9be2631b01b151c44a6a20ff8569d08b55e1e28b46ab528a671`  
		Last Modified: Thu, 09 Oct 2025 23:13:03 GMT  
		Size: 16.2 MB (16161708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4ad72491b2c6026fdda93ef5ad1af31774edeef348d3f8101f8f6f8f196a77`  
		Last Modified: Thu, 09 Oct 2025 22:45:38 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0acf0ea81f7ffc52d306ba728c11fee6c7eb5cd982a648796f5d41cbc4aa9f`  
		Last Modified: Thu, 20 Nov 2025 19:44:18 GMT  
		Size: 7.1 MB (7103712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:6d6d47bf8c9d75a94fd69d7c87a9222d407b12627fd4a36a942508fceb427d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.1 KB (705146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1973d4d1a2ce6f8fb5ccf39081c8390c77b3e17adc96845929dcab579a5534`

```dockerfile
```

-	Layers:
	-	`sha256:8c67e96f8bf6b77ab5ac9f9ebe2aa02b0c7459d24aed18b1203c37592ee1898e`  
		Last Modified: Thu, 20 Nov 2025 21:24:51 GMT  
		Size: 697.1 KB (697075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3f0a8fcbe07d0db81b25ce8ffa90d7072a7673aecea4db4e862cf0b2f09b1d7`  
		Last Modified: Thu, 20 Nov 2025 21:24:52 GMT  
		Size: 8.1 KB (8071 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.21` - linux; ppc64le

```console
$ docker pull hylang@sha256:97996ae3df3932a6a29433abde814522a79707836d3ddb3d3f839c543be038f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27797965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d324914f6e9e60eaf38762539d3fcea4047484c1c21346a52d6fa17e5c0ac4c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
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
ENV PYTHON_VERSION=3.11.14
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:47:53 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:47:53 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:47:53 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:47:53 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0026c7dc43c0a7255a1ad9f4da34ccbef2597f65b422a86bda4c70ee1f6cbd4`  
		Last Modified: Thu, 09 Oct 2025 08:37:20 GMT  
		Size: 459.4 KB (459409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c467a7cfa1dad0fe6e4044aba238e1625c9bf8c7ee963c91c7d43fa429dba03c`  
		Last Modified: Fri, 10 Oct 2025 02:32:40 GMT  
		Size: 16.7 MB (16660520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bf039aff031686020bba4f77bc1c37ac8b11ef5afe9d00d6500e3a53ba1cee`  
		Last Modified: Fri, 10 Oct 2025 02:32:39 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b21353707253561dd703d09d1299490550e3c68a9d29bb3bdd3cbc70782112`  
		Last Modified: Thu, 20 Nov 2025 19:48:26 GMT  
		Size: 7.1 MB (7103715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:e9ab3b5c17e7fe92909d8c4c731d3593e8d546e77149c5745da06f1944bbcfcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.3 KB (703330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdca4581c667caf70841aac10e22da573aa1d10f52ec90a985c656cffb5215bd`

```dockerfile
```

-	Layers:
	-	`sha256:0e583d2cadb718d4d49f1c78424374b6a2b70a80593ba4b3a6173f1bf02e2ca7`  
		Last Modified: Thu, 20 Nov 2025 21:24:55 GMT  
		Size: 695.2 KB (695183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f9225b40157972e9d87b2ca28976d37548177905192b4b8a477833577ca2474`  
		Last Modified: Thu, 20 Nov 2025 21:24:56 GMT  
		Size: 8.1 KB (8147 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.21` - linux; riscv64

```console
$ docker pull hylang@sha256:aa7b10adcb16a3c4d3ba4b5b7a068cac6a7f4a037e54ff2ed66f0a4422f9355f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26789287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc440081d7dc3eea6efae3039fb47cc5a12a2172e4b4c1a91fc9959cac950ef9`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
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
ENV PYTHON_VERSION=3.11.14
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
CMD ["python3"]
# Sat, 22 Nov 2025 23:14:10 GMT
ENV HY_VERSION=1.1.0
# Sat, 22 Nov 2025 23:14:10 GMT
ENV HYRULE_VERSION=1.0.1
# Sat, 22 Nov 2025 23:14:10 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 22 Nov 2025 23:14:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f874295bfcd01a87ee99265d45f0786d35242cd9d53bc2744cb330bf3be277f5`  
		Last Modified: Wed, 08 Oct 2025 21:19:05 GMT  
		Size: 3.4 MB (3351001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4666486ae2b3de4262dd119500cb4aed261920d55a1e4598d541bd3462e2414`  
		Last Modified: Mon, 13 Oct 2025 18:26:13 GMT  
		Size: 457.2 KB (457225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b450e75209f641fb5e5ca9f43f11795608fc1741c791bd32b78837a6ecc5ab2`  
		Last Modified: Tue, 14 Oct 2025 06:27:11 GMT  
		Size: 15.9 MB (15876341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be94242698e23d7a82ae92e825a0176aa54afbf3d81a5765a1b5390e35621eb`  
		Last Modified: Tue, 14 Oct 2025 06:27:10 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b22c2f91993dfe4feddf14bd0e28fb660947622bcb5ad6f09211fe19f71eec`  
		Last Modified: Sat, 22 Nov 2025 23:15:01 GMT  
		Size: 7.1 MB (7104470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:a7c49f089aa99bd139aeafe2a6ce6efaed3a5d7d6b82b902f077d3c4173df063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.3 KB (703325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3ac2ba6133f9eb9f27b8917a7911032706e83c16fa716804ba0ebb4e23c575`

```dockerfile
```

-	Layers:
	-	`sha256:9f98a68d02a23594d50ef9a0a4dcb94b2e4040cbbd412ebcaf77fff3a253cf3c`  
		Last Modified: Sun, 23 Nov 2025 00:20:50 GMT  
		Size: 695.2 KB (695179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4797c087a2bebae01a63c8099d422c5140700e661287424aab5f7e3a626bfba0`  
		Last Modified: Sun, 23 Nov 2025 00:20:50 GMT  
		Size: 8.1 KB (8146 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.21` - linux; s390x

```console
$ docker pull hylang@sha256:22cb54f1e744c1a94a7730a6814b94c6667b8bef1e3d7313b9f06cabc5168b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27442420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa03bb8fbdd82d9945d3c012a7d036c441746d165c8f8411352b3f7a9a14502e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
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
ENV PYTHON_VERSION=3.11.14
# Thu, 09 Oct 2025 21:44:07 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 21:44:07 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:44:40 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:44:40 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:44:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:44:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d403476d77f3c6d174042f0a35c75c77af9283be8ed3f5fdc93ad0cd153034`  
		Last Modified: Thu, 09 Oct 2025 13:06:21 GMT  
		Size: 457.9 KB (457870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e69ef0aa4288fc8ec4f3a05567b6c2a542f655e8d7a0828c1f8b77c21aa8d6`  
		Last Modified: Fri, 10 Oct 2025 04:16:07 GMT  
		Size: 16.4 MB (16414197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92073bcf16bc3fb561e5036e117313e83e4e1cd6de8be6d1886229ab159b3bf`  
		Last Modified: Fri, 10 Oct 2025 04:16:06 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ca4e8f6791ab574725d781a4e77eba3be3d6aff7459a022d220a37f4b076ef`  
		Last Modified: Thu, 20 Nov 2025 19:44:55 GMT  
		Size: 7.1 MB (7103671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:234f392236b3ee29d4dcae0062eeb416cdd3e8cde1bb53c69f503414d5491982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.3 KB (703252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28a018b0efd66db48c8c6455a6e6a47b1a243ca02513ebf28399f0e4f8c87ba`

```dockerfile
```

-	Layers:
	-	`sha256:a7194333a34a41742a4107ba948447f69cf48b48727f9dbcedc07b25670d87ff`  
		Last Modified: Thu, 20 Nov 2025 21:25:03 GMT  
		Size: 695.1 KB (695149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c968627464b655a271c2b0580d9ea188a33b49e6d4a6c68482de60256df715a`  
		Last Modified: Thu, 20 Nov 2025 21:25:04 GMT  
		Size: 8.1 KB (8103 bytes)  
		MIME: application/vnd.in-toto+json
