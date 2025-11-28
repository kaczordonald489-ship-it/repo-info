## `pypy:2-7-slim-bookworm`

```console
$ docker pull pypy@sha256:a50a4dc9ebbc273b95d690a3f870f8b24e48f5f86fc4e9c6638809b015dfce9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-7-slim-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:c67731bb55896f2b21108206afd332887fb6c8ee515134b45285d5be1b5b6533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66137908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3541c86fa4377da31c9f6a157e4dcd426aa6013c854b4249b170de42e68b04`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:48:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:48:51 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:48:51 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:48:51 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 18 Nov 2025 05:48:51 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 18 Nov 2025 05:48:51 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e9f53f51cdaedb4440ec9c48114c0515e04e4beb77ac9204e0e549954fa36`  
		Last Modified: Tue, 18 Nov 2025 05:49:08 GMT  
		Size: 3.5 MB (3509692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9af490138d10fbcde1111884ddf176cb55ddc6e8e4cf0f85a510fab365d10b2`  
		Last Modified: Tue, 18 Nov 2025 05:49:11 GMT  
		Size: 34.4 MB (34399767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:7332158a8432d1f0529cdc5f371448d6bdcc94f4dbe24f7137130d5211ab3ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2536984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2c2d036bef980a8065cdc84d26075cd4b46ea27910918ef31eb4b0fa94f2f7`

```dockerfile
```

-	Layers:
	-	`sha256:1cf2e8ce3a6b2fb72e32f966a06c5839f7dbd55a976a4e60b575518dc99e9b73`  
		Last Modified: Tue, 18 Nov 2025 07:39:54 GMT  
		Size: 2.5 MB (2518151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a8c747d34ec7df32048a5b0851f69dba7e2d5dd15a5edd92be8b8db426a5a1a`  
		Last Modified: Tue, 18 Nov 2025 07:39:55 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:42377cf7a61664b5d7afccb380784b4937c5c80f2655325fff45453a08ca3f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63752188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe009c848c3342d390745f0a71e84516f5413e083b115bcccd58b3a82411efe`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:29:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:29:27 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:29:27 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:29:27 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 18 Nov 2025 04:29:27 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 18 Nov 2025 04:29:27 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ddde99a68a452105708c6700d2435433dcfab48c2fd8d63850cb0082c61685`  
		Last Modified: Tue, 18 Nov 2025 04:29:44 GMT  
		Size: 3.3 MB (3340682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac18e8540f50d1ba146b1718394f6abb777bff798784c4b3814581556fc9ffc7`  
		Last Modified: Tue, 18 Nov 2025 04:29:47 GMT  
		Size: 32.3 MB (32309299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:7f03fcfed246f211e3e0fe3467ca0a1f68554619e38abdf7a18379dd40059e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2537460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5b0a23fd7d5fb0275a31c035f1633c681daa414df56ad0d4497a76ed96c71f`

```dockerfile
```

-	Layers:
	-	`sha256:b641fdff19f00ffee521a335d9b49907c9032badea606786815b724d9cb23c68`  
		Last Modified: Tue, 18 Nov 2025 07:39:59 GMT  
		Size: 2.5 MB (2518461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee80d1798940e7d2e988b33877fcb0066f5599662e9a6de148a19ce32f90e6c3`  
		Last Modified: Tue, 18 Nov 2025 07:40:00 GMT  
		Size: 19.0 KB (18999 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:efec8a89b684f71a4c98c50119a5b1210da3b050d0399ad25cd8dee8a3164ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62683047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f96180e973669d7ec6ddd84e38c382ae52d490350a265815373a7dd92b9018`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:22:59 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 03:22:59 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:22:59 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 18 Nov 2025 03:22:59 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 18 Nov 2025 03:22:59 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7204b6848e47deb5cde149bba830ab2cc9d2d043413f90aa32821b0a670dc487`  
		Last Modified: Tue, 18 Nov 2025 03:23:16 GMT  
		Size: 3.5 MB (3511046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457475d7e021f1a3e894c7ea1bf7e0457fadf281291d13b86366405a5f617092`  
		Last Modified: Tue, 18 Nov 2025 03:23:19 GMT  
		Size: 30.0 MB (29962297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:eb299d20e7a00e34d2b767025a6e2d225aac76d247bbfb2f6db5b7582ea6a6f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2534083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b40ffdbe2904b8ab6d6ebc439f580dd03dbc832f29a8bf751e87fdb2d1d034`

```dockerfile
```

-	Layers:
	-	`sha256:eda7d2aef77d655a0d536687b636d8c47307583ba674cdf319a47b2c1ba02690`  
		Last Modified: Tue, 18 Nov 2025 04:41:46 GMT  
		Size: 2.5 MB (2515304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abd769f3672eceee9b7cb2ab755c68687cb88b2dbabb8c548eece5475b6bd937`  
		Last Modified: Tue, 18 Nov 2025 04:41:47 GMT  
		Size: 18.8 KB (18779 bytes)  
		MIME: application/vnd.in-toto+json
