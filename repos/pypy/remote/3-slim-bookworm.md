## `pypy:3-slim-bookworm`

```console
$ docker pull pypy@sha256:c40f00b45649ccef15d9e648f9cc990908ff55f6adf7b295971ff10baf677843
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:3-slim-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:da0dc014f71af7babe1b58917ceda45252ef3c003cf8478449a7a135f95fc2ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69944738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda33c7796b54cc7522f763da6d1e85a5e1c9d205830825ae537410c2759f9bf`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:48:58 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:48:58 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:48:58 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 18 Nov 2025 05:48:58 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 18 Nov 2025 05:48:58 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fc313e20a207e946666c121291078680f0f2037a6686ff2341074b6048c472`  
		Last Modified: Tue, 18 Nov 2025 05:49:16 GMT  
		Size: 3.5 MB (3509686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886229f7b171c7c460366cb614634497e8e68d70a39490d20aa3cb2bb6fc3ce4`  
		Last Modified: Tue, 18 Nov 2025 05:49:18 GMT  
		Size: 38.2 MB (38206603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:3c0757c7fe3288990e8b02f3ace2b0752ba8d57e787d34ea184d66650cabe48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbfa1c48a7209689321974201d3c34ec0ad3284db9cf95cce59bc8f27207809`

```dockerfile
```

-	Layers:
	-	`sha256:1070f7f4eb390b8137713f82d92222c415ae9684bfd256b5f9030eb3ce2e7b7d`  
		Last Modified: Tue, 18 Nov 2025 07:42:08 GMT  
		Size: 2.6 MB (2611634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d2a87fc87d3a466724708880e60b31a6e948058041a7f893f03d75cb26af67`  
		Last Modified: Tue, 18 Nov 2025 07:42:09 GMT  
		Size: 22.0 KB (21957 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:829a7e1597814f7ff333aad8bd234c25419e9681a72fbf50ebdf4f515465d9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67965722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9560d291db18ebf0abc7044e6e26fea885e72bda7b86f81639a9221e8ab1eac8`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:28:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:28:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:28:44 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:28:44 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 18 Nov 2025 04:28:44 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 18 Nov 2025 04:28:44 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80700ce6d9b1f19e39f821587f57456956e0b54394bed6fdcef5b85f39cebea0`  
		Last Modified: Tue, 18 Nov 2025 04:29:04 GMT  
		Size: 3.3 MB (3340642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd052863aa6232674cd841237cd572deeaac6d7da3bd18afd47e8193073139b`  
		Last Modified: Tue, 18 Nov 2025 04:29:09 GMT  
		Size: 36.5 MB (36522873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:d9ff178c290dd20500810a6e55820724bc384baa410d44cf68f76b817c987ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e36665a140fef325881051b070a26c1ad7db6d9ecf92b2a54e3b3c4fffd9401`

```dockerfile
```

-	Layers:
	-	`sha256:babf6f39a5e02b3cde8446522241e6ad207f20b283e8f36fe0b1654373f7cb62`  
		Last Modified: Tue, 18 Nov 2025 07:42:13 GMT  
		Size: 2.6 MB (2611961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d41520005b65200c2657e51b03fb1eec5089f9d9ceb4759e5ecba9021ff6c2b2`  
		Last Modified: Tue, 18 Nov 2025 07:42:14 GMT  
		Size: 22.1 KB (22136 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:1ffb901fe48d6eb13d03410cce0c93161529a89979c035f63a5ff9697c16b4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67419199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11884d5efb1ece2d3719602ed1c1cb3cc6aac27608d1803da5c15d9388f20362`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:20:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:21:24 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 03:21:24 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:21:24 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 18 Nov 2025 03:21:24 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 18 Nov 2025 03:21:24 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0dc128ee4ca9cf8501fba9f1824fa09e66e3ca9fe3d0daf72cd8121589a8a7`  
		Last Modified: Tue, 18 Nov 2025 03:21:41 GMT  
		Size: 3.5 MB (3511013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3efa51985cf56c4c4105d5383fd2fa83872e39d30c70aa0c2912f6e5956208`  
		Last Modified: Tue, 18 Nov 2025 03:21:44 GMT  
		Size: 34.7 MB (34698482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:7a686d4a973569856ab99cc828d90fc2b050ac5bd0deba5cfcf5198fd97cecb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2630670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e392fb1a900d6f927b76e494183d6bb8bb2cfe747d8a8c66f0a9fbecf55589`

```dockerfile
```

-	Layers:
	-	`sha256:cef3df2f56040515813872ad11e0938142814b2c7ffe494ad0e12c64e47b00f0`  
		Last Modified: Tue, 18 Nov 2025 04:43:08 GMT  
		Size: 2.6 MB (2608772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b34dce00c8179d685fba2dccccb608c72da0254fa6244c25d3dcb10d69fc0946`  
		Last Modified: Tue, 18 Nov 2025 04:43:08 GMT  
		Size: 21.9 KB (21898 bytes)  
		MIME: application/vnd.in-toto+json
