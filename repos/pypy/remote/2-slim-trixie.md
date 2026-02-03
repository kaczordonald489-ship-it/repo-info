## `pypy:2-slim-trixie`

```console
$ docker pull pypy@sha256:cb24081f4bbe08dbe7d29e0f78409987af3a63325c9ef3eac5549d14cd329753
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-slim-trixie` - linux; amd64

```console
$ docker pull pypy@sha256:d2edb2254ff1c0587dd564b2a13a64c7f783b72321d529d2c122cd91f8d5d39d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65443524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c002e2567546f99ef2abc25ad6dafae00a5c5d69b244aa5decd9cfe08040ac74`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:01:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:01:26 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:01:26 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:01:26 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 03 Feb 2026 03:01:26 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 03 Feb 2026 03:01:26 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353c1ac466c2163e1b59c491a317a0d1af3aead9ffce7ea6355dab667c4603ea`  
		Last Modified: Tue, 03 Feb 2026 03:01:37 GMT  
		Size: 1.2 MB (1220074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b35b0c016c23f0f3b8841cd0f7c0a9a465b2b04fe5c8d843d51697970b5ea3`  
		Last Modified: Tue, 03 Feb 2026 03:01:38 GMT  
		Size: 34.4 MB (34444854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-trixie` - unknown; unknown

```console
$ docker pull pypy@sha256:dc982ff82a329b3031acfc5ef17efb1c3abac2da81c11784f476cbcbac570a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2830c7ae2743475a1b8a2bb16efb3ffca53e7c63076050a564efa82513777965`

```dockerfile
```

-	Layers:
	-	`sha256:91dd271048dce20500d57a8ec9e5f4dad493a943a73a88229256bdc5c0a683d1`  
		Last Modified: Tue, 03 Feb 2026 03:01:37 GMT  
		Size: 2.1 MB (2131904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83182dad3419528f80b8ca08401a1adb60770653a3047490780a246d61444491`  
		Last Modified: Tue, 03 Feb 2026 03:01:37 GMT  
		Size: 21.2 KB (21215 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:d6cddb0989b876d7fbc58d731d10ef261800c1755a23e6045cbd6b6fedb7156a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63698327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51cde62116d07e8817af67892ee65bcb0d9ef6d13e985a4482910396a88ea476`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:03:51 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:03:51 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:03:51 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 03 Feb 2026 03:03:51 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 03 Feb 2026 03:03:51 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a687490af0aca6103c0172db28dc94c872bb8547aef797479b6143ed6eb9f529`  
		Last Modified: Tue, 03 Feb 2026 03:04:02 GMT  
		Size: 1.2 MB (1201879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3fd7a7f4f5152f12099c2f9a05a71952bcd0c24aa22df7e065cd0211f9d326`  
		Last Modified: Tue, 03 Feb 2026 03:04:03 GMT  
		Size: 32.4 MB (32356384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-trixie` - unknown; unknown

```console
$ docker pull pypy@sha256:97e8d89d5aaad8cf2f8e1dc91c51799f66736197c26f26e03b7833cfc781db4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f2ce8d51bf0fafb2bc87e31f7aeb310ee5273b9325d902dd8f901832a14dad`

```dockerfile
```

-	Layers:
	-	`sha256:63cbcee5dc09e5cc1b6b9b0627075d4cf15ea1e1429c49b587dbe6ab4601f403`  
		Last Modified: Tue, 03 Feb 2026 03:04:02 GMT  
		Size: 2.1 MB (2132311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6f4c2cec2af27aebb1841876e76f756c7c1ab4edb995ff8749fea3bb0f9d71f`  
		Last Modified: Tue, 03 Feb 2026 03:04:02 GMT  
		Size: 21.5 KB (21478 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-trixie` - linux; 386

```console
$ docker pull pypy@sha256:2e43f3b80688a60cda849fd9e1f32d81976ec7f809cacef9a90fbbd54037477a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62521309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be055c92e82bd2153ca0bb063b8c09f772d3f7cdb2ec20a96ad0ed71d7a67e36`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:58:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:58:50 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:58:50 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:58:50 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 03 Feb 2026 02:58:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 03 Feb 2026 02:58:50 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832d0f78f66cc1a366aa7825ccdff0b897e8ddac8e45111ed5c973b40c80d690`  
		Last Modified: Tue, 03 Feb 2026 02:58:59 GMT  
		Size: 1.2 MB (1227823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844ff83a06b17e8f7e619e0079cc17d310c02dca32512659591ced63919b172f`  
		Last Modified: Tue, 03 Feb 2026 02:59:00 GMT  
		Size: 30.0 MB (29999631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-trixie` - unknown; unknown

```console
$ docker pull pypy@sha256:6dd5f856477c10b23931b88987ef5228928f0d34b543e9ecf7f8c52181e007aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ab6ea4362834117c04761d6de67a0c5a9d5715a963f937226507c7fe9de3dc`

```dockerfile
```

-	Layers:
	-	`sha256:769b2326e25296242dbae2275eb97fec5a8da56e755c53fde688c25358953497`  
		Last Modified: Tue, 03 Feb 2026 02:58:59 GMT  
		Size: 2.1 MB (2129031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e1818c31e422f5e32f074eb561be83f782831a98e478ba92935a1c019f4a2d8`  
		Last Modified: Tue, 03 Feb 2026 02:58:59 GMT  
		Size: 21.1 KB (21121 bytes)  
		MIME: application/vnd.in-toto+json
