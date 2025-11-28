## `hylang:pypy-bookworm`

```console
$ docker pull hylang@sha256:021beb64be7f8dd32ec698ae81543d7e99cb9ef71cb007eb0430aeca5afc5bea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:pypy-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:2630fb1eb0404975feb2837a97e2c2e2aa4d9428fae071d2b4c9a402c14026b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77812306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772d178219e220d1227f1ce652d7ee83fa3e7c3f98d76886c8a138d34af07eba`
-	Default Command: `["hy"]`

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
# Thu, 20 Nov 2025 19:44:59 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:44:59 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:44:59 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:44:59 GMT
CMD ["hy"]
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
	-	`sha256:2cadc695d1a2dca151f4104e48db4f23e339b7c9cbe8e749ceec6a65171cf6e8`  
		Last Modified: Thu, 20 Nov 2025 19:45:14 GMT  
		Size: 7.9 MB (7867568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:b3e7c335b146187d745d96edfbb0965537c18d9a1293ec0686cd1eff4076944e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb0ab85ff1ebe5b6ded9fe532148e37f78a01f2be46f8ce19a990c40e9b5887`

```dockerfile
```

-	Layers:
	-	`sha256:0f3af5ff47b27f67c785c846a6596bfe9c28ce0922f2cb24f19cc206b9bca9f4`  
		Last Modified: Thu, 20 Nov 2025 21:21:44 GMT  
		Size: 2.6 MB (2618859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9e1257b3d0fecf12379b2c942f3875695051d5482a468f23a21f1c25747d3de`  
		Last Modified: Thu, 20 Nov 2025 21:21:45 GMT  
		Size: 8.9 KB (8900 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:60cfb9c2d685698c0f4e67d3133106c3e6400fcc13ec2c258c74a32d57aea872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75833463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758b10e9c5cc1912fc48740e83c06f02df40a9f70b1685d5d47c0cb07b88c73f`
-	Default Command: `["hy"]`

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
# Thu, 20 Nov 2025 19:45:08 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:45:08 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:45:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:45:08 GMT
CMD ["hy"]
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
	-	`sha256:6f9d3642ed134e45a6b5f72fe0401bb75c9b4a177f98bff634887e042d1e360a`  
		Last Modified: Thu, 20 Nov 2025 19:45:23 GMT  
		Size: 7.9 MB (7867741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:017eb184e84147d504418bbf9c82ffd1e6cf84ef301bd4d761fd045a264bacbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2766b96ef8f47d43000beea2336d6870504597b3e041072aa7aaa871dd8f8548`

```dockerfile
```

-	Layers:
	-	`sha256:c639643f2a96b905ca06fdbaa6a6432ff4c6f019b2bb9a2deef0341ca3c8e20d`  
		Last Modified: Thu, 20 Nov 2025 21:21:50 GMT  
		Size: 2.6 MB (2619174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43d16a2fb00b6f74549e5d01f7ffbfc9b47034374677f397e0870bf0be811e2e`  
		Last Modified: Thu, 20 Nov 2025 21:21:51 GMT  
		Size: 9.1 KB (9052 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:fc5f36ea0749a48a9193ed9ccf99cdddc5b273db9ed57df56beb31ed6963ab5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75286896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6257f2cb2f3663ab13d9bd559a3c8b57ba2430b56be3d495436bccd1a39cca8e`
-	Default Command: `["hy"]`

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
# Thu, 20 Nov 2025 19:45:14 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:45:14 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:45:14 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:45:14 GMT
CMD ["hy"]
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
	-	`sha256:72840ba0a4ce3fccd6629b4bf53aa76395b84a6d935f369725ee201342a2c43d`  
		Last Modified: Thu, 20 Nov 2025 19:45:27 GMT  
		Size: 7.9 MB (7867697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:b3e7a61045dc12665da5b9c90418b38c131ae3eadcd8f64b7c342073afa0f323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244d7fc335b33a835a16dac5774ded426c2c2b0928cf26adbefe903927c980b9`

```dockerfile
```

-	Layers:
	-	`sha256:2a32f1bdb17f3e12dd70de2671949bec55d8e6af40076d391c5677a29db64d76`  
		Last Modified: Thu, 20 Nov 2025 21:21:55 GMT  
		Size: 2.6 MB (2616002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba2a3fa47dd3e3253baf483a4489b9222ef8ca55f9d499a744f1c7d7d2559a32`  
		Last Modified: Thu, 20 Nov 2025 21:21:56 GMT  
		Size: 8.8 KB (8847 bytes)  
		MIME: application/vnd.in-toto+json
