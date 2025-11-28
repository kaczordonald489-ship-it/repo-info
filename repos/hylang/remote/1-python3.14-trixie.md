## `hylang:1-python3.14-trixie`

```console
$ docker pull hylang@sha256:0ed7b23b21a8de17cecf6115d9b56eb38b5bb295284939c7dac25ee8ef95347d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `hylang:1-python3.14-trixie` - linux; amd64

```console
$ docker pull hylang@sha256:365eb8b77f9978d459d1858ac732c4c46970359b9df679ecf8b06ae28cb41994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48945631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07a6e425fed5e5d9a22049a70afeb15f27cb941ecd93c5742e4cd7671d018d3`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:49:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:49:12 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 18 Nov 2025 05:49:12 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Tue, 18 Nov 2025 05:54:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 18 Nov 2025 05:54:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 18 Nov 2025 05:54:37 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:40:15 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:40:15 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:40:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:40:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebd987125d414f355d50710ebe2c8c1ef82be7f9b295a56c5a75f8a0c4246ea`  
		Last Modified: Tue, 18 Nov 2025 05:54:50 GMT  
		Size: 1.3 MB (1292747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a580af6aa213e326f6c625b68adba4affedcee7ed5002f13160db623e69497`  
		Last Modified: Tue, 18 Nov 2025 05:54:51 GMT  
		Size: 12.2 MB (12172554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec80ae14678f10e720bc3837c21cd58c485f01d08c008d31702a3961595057c5`  
		Last Modified: Tue, 18 Nov 2025 05:54:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1abb58562d4503a3a9fa30006cc53a8525138e7ef8decdd7bbaa921bb3c9034`  
		Last Modified: Thu, 20 Nov 2025 19:41:26 GMT  
		Size: 5.7 MB (5703596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:5c9a9b17578a9f4b2912a6d4e737de5d049e5e965950359007f91d8490ad35f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04039d844dc83e8dc67b8e8c8270a2328de9e31416d0458a139bdbb74460d5f`

```dockerfile
```

-	Layers:
	-	`sha256:b2173b637b501be6b6a62f76d11845dfd301b32dd5da889e7d7dd8cd50b19993`  
		Last Modified: Thu, 20 Nov 2025 21:20:10 GMT  
		Size: 2.2 MB (2157284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b972bbb886c9e3f6a453e7c08109ed7c0fe76a91432bda2449fae362b83f74fa`  
		Last Modified: Thu, 20 Nov 2025 21:20:11 GMT  
		Size: 11.6 KB (11643 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-trixie` - linux; arm variant v5

```console
$ docker pull hylang@sha256:f334f2b43aa4bb4ed7d996751ceab09126b994a97a5a0511a64004d61a68271e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46775606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433183601b353d18e316ba33d807787bd89fba001d654b669f7e2394f243dd5f`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:57:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:57:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 03:57:14 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 18 Nov 2025 03:57:14 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Tue, 18 Nov 2025 04:07:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 18 Nov 2025 04:07:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 18 Nov 2025 04:07:37 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:40:10 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:40:10 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:40:10 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:40:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d758926d2ef621253c118c9edb9c47434e936423766ca76611f221b5357268`  
		Last Modified: Tue, 18 Nov 2025 04:07:50 GMT  
		Size: 1.3 MB (1275891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77858c34053206a749a49c3687311f8aab824a2d87c14af9d197df2a7e0a186c`  
		Last Modified: Tue, 18 Nov 2025 04:07:51 GMT  
		Size: 11.9 MB (11851579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4b002170ae852a7d4f762966ad59816e1934f7d07fa8ca1afaaedd8f2252da`  
		Last Modified: Tue, 18 Nov 2025 04:07:50 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eddf0a371419f57f8e74006a9d92e2d74a86a78a688d3e87f29d9df62cd5b2b`  
		Last Modified: Thu, 20 Nov 2025 19:40:24 GMT  
		Size: 5.7 MB (5703740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:846e2b0b79ac85952d64e808e39dd0f8991d4d9765c972f5dd628d00d77fdc51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909babeaffc7caa1575935bc660d8f2053180a9d7822ade4c591d623d02e352f`

```dockerfile
```

-	Layers:
	-	`sha256:587e590ee7da2380dfd26a47bf95a08b8501f73868e811e89f8dd41d71a1ddf6`  
		Last Modified: Thu, 20 Nov 2025 21:20:16 GMT  
		Size: 2.2 MB (2160349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23108e5f6bce471a45dbae35fe375872ed75378079c675a3d7186321a28b726`  
		Last Modified: Thu, 20 Nov 2025 21:20:17 GMT  
		Size: 11.8 KB (11819 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-trixie` - linux; arm variant v7

```console
$ docker pull hylang@sha256:d34fa8af0166c5519ef1df7d05f74adc2e3bfe28107720b8b72f78339a2f7337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44709579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d6af2a6df167a6d621e4ea736fc5ea7a162d1bda6f6f817e5395ff30b88b75`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:38:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:38:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:38:52 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 18 Nov 2025 04:38:52 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Tue, 18 Nov 2025 04:47:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 18 Nov 2025 04:47:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 18 Nov 2025 04:47:39 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:40:40 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:40:40 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:40:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:40:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab112a4afe944ecd54744c2219e37461568855fea5bcf8e1a3f253e0915fc795`  
		Last Modified: Tue, 18 Nov 2025 04:47:53 GMT  
		Size: 1.2 MB (1248499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ab3c55d37458f210404c46162b057e43ad1ff4b97c2318dfc6070fcb5f0916`  
		Last Modified: Tue, 18 Nov 2025 04:47:53 GMT  
		Size: 11.5 MB (11547231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de42d5ada8a5c362fe3658cf7ac1743303a13628830d6679e88e5a488d1cb7a`  
		Last Modified: Tue, 18 Nov 2025 04:47:52 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf867f450398bedfa45df09ea18576415c359fe8789bba0cb4570ed3da5436dc`  
		Last Modified: Thu, 20 Nov 2025 19:40:56 GMT  
		Size: 5.7 MB (5703640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:239e67a84b96243ba651796d6ef177ccc9561abd02d51e1f355ce6abf94776b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2170621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57451ad7b0d94d87dea549a0b8dc10f045d7c84db41e268ace80466016233c4e`

```dockerfile
```

-	Layers:
	-	`sha256:5a92e93680e550642ee0d3d5e2b5d9a4e308663639e25bcb7e6ac831f3048034`  
		Last Modified: Thu, 20 Nov 2025 21:20:21 GMT  
		Size: 2.2 MB (2158802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e205560504dec2ff9640d602ebb39b57c67da9418f377d4a98b3f90800349e2c`  
		Last Modified: Thu, 20 Nov 2025 21:20:22 GMT  
		Size: 11.8 KB (11819 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:b74d439cabcd847267fc46365b613eca4a2dde4b23db1de8707e0bb8ade77212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49199299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83f23dca1cb7966cd4521d84a94bf4527fcc5aa762fa1cea75b5ff906ea4346`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:31:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:31:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:31:13 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 18 Nov 2025 04:31:13 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Tue, 18 Nov 2025 04:36:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 18 Nov 2025 04:36:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 18 Nov 2025 04:36:59 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:40:07 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:40:07 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:40:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:40:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff97b433249fa541dddf15b078e27b908592207c632eefd05a467148c8108915`  
		Last Modified: Tue, 18 Nov 2025 04:37:12 GMT  
		Size: 1.3 MB (1273764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c6c2370ffd920c53bbf447eba1694e5d20c5ffbf8fbbc15a1191eb924938da`  
		Last Modified: Tue, 18 Nov 2025 04:37:16 GMT  
		Size: 12.1 MB (12083040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07e1971e2bde777c69ef9be622e6e392814501ac8171c4fbc8d351dc0e7a7c`  
		Last Modified: Tue, 18 Nov 2025 04:37:12 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ff9a0c9755af8e6b738717931294e4e3e7a5d66c448bf6d87d4cb8f3aeb45d`  
		Last Modified: Thu, 20 Nov 2025 19:41:58 GMT  
		Size: 5.7 MB (5703635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:b95d2afc11d71f09ac2c013bf5e5b1ad9ad4de36f86262bf1a3ae94a309967cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77609b1197c15f0cc2fa44f60de33d2d541dc55bea62faaecab53cb8a981cd5b`

```dockerfile
```

-	Layers:
	-	`sha256:c4854ad8adbd5a77ad6d2e5bde89fb43f826463c49c721f76d4eb471cf5bcc1d`  
		Last Modified: Thu, 20 Nov 2025 21:20:26 GMT  
		Size: 2.2 MB (2157694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdca54c11b84eabb0fd95e43d742bb390fc8e9877496f8aa536d47ba54dac6aa`  
		Last Modified: Thu, 20 Nov 2025 21:20:27 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-trixie` - linux; 386

```console
$ docker pull hylang@sha256:5633406b578496fd8b04e64cf0908b910a6e1ef07e35d2f254a90d0fc46465a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50589864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784dde94f959ca80c032a79610b8ccdf551950de543d0bdd0e8d378b516aee6d`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:26:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 03:26:05 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 18 Nov 2025 03:26:05 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Tue, 18 Nov 2025 03:32:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 18 Nov 2025 03:32:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 18 Nov 2025 03:32:11 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:39:28 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:39:28 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:39:28 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:39:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab1da9f34dfc855da6f31b525acd9b377ba2159d0727bb1a93d343a6bd2f28d`  
		Last Modified: Tue, 18 Nov 2025 03:32:25 GMT  
		Size: 1.3 MB (1296818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027eb8964e605589f9bc4b4f4027f23a7374367dadcf09232eef29795b4150d9`  
		Last Modified: Tue, 18 Nov 2025 03:32:28 GMT  
		Size: 12.3 MB (12295977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddcb606a1bd4a355b7af9c090a3c46a8aa38cc4e76b78edb8b6b47ca8643e30`  
		Last Modified: Tue, 18 Nov 2025 03:32:25 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c3e986c3dd7741e9b438392c8ba48be02cf47e2bfd1683482f98d392926e9b`  
		Last Modified: Thu, 20 Nov 2025 19:40:31 GMT  
		Size: 5.7 MB (5703751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:d0138a2fb99b08653ad0defcac724e36953df24d45cf484ecdb8c034b7cf7f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a15ae4946b3003970c44a62d4ebfd654d8fea27452d2628bbbeac6ae98e6c38`

```dockerfile
```

-	Layers:
	-	`sha256:d79b2df755cfd61502832519b2dd73d52075370c3f8eda93c7621e1fb5a4c6f2`  
		Last Modified: Thu, 20 Nov 2025 21:20:30 GMT  
		Size: 2.2 MB (2154405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:960d6f9903b2593f185ac738d5e1cc9b9f190c77d691c55375b812db7a227337`  
		Last Modified: Thu, 20 Nov 2025 21:20:31 GMT  
		Size: 11.6 KB (11551 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-trixie` - linux; ppc64le

```console
$ docker pull hylang@sha256:158bc563983e176ab71fe6279624467d45e13551cc89e5ffee5e1078e8d838ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53204948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f267c8643a0fd3e12ebcafa60fb979096d8c16738821c0fff1e05818530435`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 18:24:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 18:24:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 18:24:03 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 18 Nov 2025 18:24:03 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Tue, 18 Nov 2025 18:48:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 18 Nov 2025 18:48:18 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 18 Nov 2025 18:48:18 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:38:28 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:38:28 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:38:28 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:38:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbcef8c770c0643674380f6787c6d13d11479fccd2e5a398f9584e6028aacd51`  
		Last Modified: Tue, 18 Nov 2025 18:32:41 GMT  
		Size: 1.3 MB (1320551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bea2dd589c4cb54e611b1581b871e058d6cfdc882c3d4b45b4f419482b605b`  
		Last Modified: Tue, 18 Nov 2025 18:49:15 GMT  
		Size: 12.6 MB (12583694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f431ea69f3eb03542ac3615a261573af297286b99def73b9733da0d922c0e0a`  
		Last Modified: Tue, 18 Nov 2025 18:49:12 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d06115b87465f611686a9e5192bd623f2e28333d760261b81528f60763d0b3`  
		Last Modified: Thu, 20 Nov 2025 19:39:15 GMT  
		Size: 5.7 MB (5703594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:98c6103296c80630e4902865b1decbb0e3b9b6b85aa928b33247acc99e85a21f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e56bdb8118c200682fe9645cbc19c1b3f67efc5cef94a884d57392a43a4a3c`

```dockerfile
```

-	Layers:
	-	`sha256:161098193d7de80ce011ebc60e3b6bdb962c855fa6c691ce41737daae434dce6`  
		Last Modified: Thu, 20 Nov 2025 21:20:35 GMT  
		Size: 2.2 MB (2160923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2efeccbdd02d5d2a046b719c66b40c82c4b7a164b4b83a426c1b670af1e204`  
		Last Modified: Thu, 20 Nov 2025 21:20:36 GMT  
		Size: 11.8 KB (11759 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-trixie` - linux; riscv64

```console
$ docker pull hylang@sha256:58c50a2eb7a5a7b6cfd3179cd47d0e2725ef8d03dc25bb53295f5da6349d0060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47416867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517434fc90dbdc54a3c9d6f5220d7c4ab8efaa252691b0c08d8b12cf2dd69e17`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 05:15:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 05:15:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 05:15:00 GMT
ENV PYTHON_VERSION=3.14.0
# Thu, 20 Nov 2025 05:15:00 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Thu, 20 Nov 2025 07:03:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 20 Nov 2025 07:03:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 20 Nov 2025 07:03:07 GMT
CMD ["python3"]
# Sat, 22 Nov 2025 22:29:13 GMT
ENV HY_VERSION=1.1.0
# Sat, 22 Nov 2025 22:29:13 GMT
ENV HYRULE_VERSION=1.0.1
# Sat, 22 Nov 2025 22:29:13 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 22 Nov 2025 22:29:13 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca3c6622d839fd6b48607097e5c05e3cd8aa90969f85bdcac54be852f3e3e2d`  
		Last Modified: Thu, 20 Nov 2025 07:04:33 GMT  
		Size: 1.3 MB (1259913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad8ff91ecad8acc4440983fe2a01a28c48b17acc81281e0c223c72d780df1a4`  
		Last Modified: Thu, 20 Nov 2025 07:04:40 GMT  
		Size: 12.2 MB (12178806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1de5383a13a768cf2494279956f1df2d371c3e752c7549f1111238a87a46da`  
		Last Modified: Thu, 20 Nov 2025 07:04:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b94527b6f8ce349620a872d3fa576dc9e0a03e570fffd050bc320b3a74ecc1`  
		Last Modified: Sat, 22 Nov 2025 22:30:19 GMT  
		Size: 5.7 MB (5704772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:2ad1f9d0e796e55bef11d64740159bbff8f5598e82a7e1d9d507ef0615ba75c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c0a62900ef8c7cbba970e2446d4002f5f2152ab26c621312bfebb61707b035`

```dockerfile
```

-	Layers:
	-	`sha256:1892c0f8f011f45c9822b292fc775785fa800774c04ebe836474050b303314fd`  
		Last Modified: Sun, 23 Nov 2025 00:17:42 GMT  
		Size: 2.2 MB (2151294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2590179189d1865e02234f2e3c6ff6c9f77338922fabd2906ac2b907372213f4`  
		Last Modified: Sun, 23 Nov 2025 00:17:43 GMT  
		Size: 11.8 KB (11756 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-trixie` - linux; s390x

```console
$ docker pull hylang@sha256:a5088fee3f050c1398b443b424cddbe4a12ae3b4258deafe33238cae8eb34534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49066708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6eea2ed540b7fc04098485de712f3f5179a8f09a94f2104229d362920107e77`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:35:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:35:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:35:55 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 18 Nov 2025 04:35:55 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Tue, 18 Nov 2025 04:49:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 18 Nov 2025 04:49:03 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 18 Nov 2025 04:49:03 GMT
CMD ["python3"]
# Thu, 20 Nov 2025 19:38:20 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:38:20 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:38:20 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:38:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2ec73b573bfd8c07a3b96dd47b7f4ce3c774842548af03bc814087653d3370`  
		Last Modified: Tue, 18 Nov 2025 04:44:23 GMT  
		Size: 1.3 MB (1305175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bc54e0e957194ad2d8c784df29323c62717ed9b62c45dbdc700ae44e1e8716`  
		Last Modified: Tue, 18 Nov 2025 04:49:19 GMT  
		Size: 12.2 MB (12223276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfde95c00bfb2d62cfc6fbdb5ac2cc3fadf4bb5d451e7f4bacc6e2085b5b748`  
		Last Modified: Tue, 18 Nov 2025 04:49:19 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c069f5f0a8dfb62f4defa5407bc403e9869eac72825a5ac251c6fffe0dce9f6`  
		Last Modified: Thu, 20 Nov 2025 19:39:11 GMT  
		Size: 5.7 MB (5703635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:0eb9edeb60278abdbd6fd29ad72693ad82764dc2c33a285ba917708c17c708c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2170366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa78a0283a84af03c46e3398fc708eb74b5ad6ba284d161bdd90536f3bd4fb6b`

```dockerfile
```

-	Layers:
	-	`sha256:22eb8335088aacd7a648632ea23738af4cecfc7ff1b8505626b51a0b825cab6b`  
		Last Modified: Thu, 20 Nov 2025 21:20:43 GMT  
		Size: 2.2 MB (2158723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7b6bff06b3cc9180f3d6084f72e9041085b1d2597cb8215213e55950206f024`  
		Last Modified: Thu, 20 Nov 2025 21:20:44 GMT  
		Size: 11.6 KB (11643 bytes)  
		MIME: application/vnd.in-toto+json
