## `hylang:1-pypy3.11-trixie`

```console
$ docker pull hylang@sha256:c020d490f0e4d9cc53d9b8be3c3e28f0f1fe4a3136e4f40050b9ebc1c5a48af4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:1-pypy3.11-trixie` - linux; amd64

```console
$ docker pull hylang@sha256:f949618081e1f7873f3deecab7739a8155b93cce44fd98fb5491fff3baf81a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76702788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb6e7cd43de721801ef017bdcc3accf96e116e24ecb15edb94e4dd0a97b3265`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:47:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:47:50 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:47:50 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:47:50 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 18 Nov 2025 05:47:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 18 Nov 2025 05:47:50 GMT
CMD ["pypy3"]
# Thu, 20 Nov 2025 19:44:48 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:44:48 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:44:48 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:44:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74122f6d503ccf7e5125158f5a1a78a159ede42c422430768b93f227a31be44`  
		Last Modified: Tue, 18 Nov 2025 05:48:07 GMT  
		Size: 1.2 MB (1220116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30e3eeef6192e60f421dcb1608041742081203da0c9a7de10235e0e37731ec6`  
		Last Modified: Tue, 18 Nov 2025 05:48:11 GMT  
		Size: 37.8 MB (37838507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58baacdb204a8e6a2e0253e33e2f92bc3d121e7a19ff76e3eff79826ed718d8a`  
		Last Modified: Thu, 20 Nov 2025 19:45:01 GMT  
		Size: 7.9 MB (7867681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:aad24a6692214a65e33ce02aba75915e1afabed327ecfd7af218081cd50c52d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7ca5bae9a9fa293852b723c8ab3aae83ed7d62751db24197c3fad644073bba`

```dockerfile
```

-	Layers:
	-	`sha256:92d0cce099010173cee191db361112706fbb390286ebcc79323c1e4afc8e72b2`  
		Last Modified: Thu, 20 Nov 2025 21:21:44 GMT  
		Size: 2.2 MB (2238806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df1549d5306ad5e31575a4b9bedd6540cd6f7c0e9922ed564e4a0a44a737c7fb`  
		Last Modified: Thu, 20 Nov 2025 21:21:45 GMT  
		Size: 11.3 KB (11290 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:36134b0205dac84b61e836a613c3f505130ab46480a6dfc4bb74406f4668e052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75365093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c3cdc3abe206c357d75da741254fc662839e2f71264341cf4b0075505e1698`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:27:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:28:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:28:14 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:28:14 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 18 Nov 2025 04:28:14 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 18 Nov 2025 04:28:14 GMT
CMD ["pypy3"]
# Thu, 20 Nov 2025 19:44:54 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:44:54 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:44:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:44:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0cc1b8e6e005029a07250ce17f8659d9d8edb69eac949adc84243741e455c2`  
		Last Modified: Tue, 18 Nov 2025 04:28:32 GMT  
		Size: 1.2 MB (1202324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c7d8e62b742a93f0590b5eb19b32db7153059d269aadf03d82591267c3d219`  
		Last Modified: Tue, 18 Nov 2025 04:28:36 GMT  
		Size: 36.2 MB (36156458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715ad77bded06caf89691daf3711f690f72ee70f40260fdfa096efbca72d189a`  
		Last Modified: Thu, 20 Nov 2025 19:45:11 GMT  
		Size: 7.9 MB (7867701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:7a08fb36b923d3b33272bd8e4d4e63cc193272512d1ab33df23159bfdab31bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f406e1cc8fd69361616975892321021e88357ba88f1ce000bcddef8dd1944a7b`

```dockerfile
```

-	Layers:
	-	`sha256:f85270664c1607fae4ea89185ee8d316ed1790e1515694f664d4e4de82d4afde`  
		Last Modified: Thu, 20 Nov 2025 21:21:49 GMT  
		Size: 2.2 MB (2239217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a511c21f611ace1cc804903be8a2f5327eac5719cae89a90dc28774dc3bab09f`  
		Last Modified: Thu, 20 Nov 2025 21:21:50 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11-trixie` - linux; 386

```console
$ docker pull hylang@sha256:1d0de9d9d3f58fe1402450e39e69f6e2ff19a8ef98326731eb0362d783e4195a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74625270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6cb173beb6527d317a3c5e8c177f3bae0771d7bebcdc3c6f34595bf471f7e9`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:21:32 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 03:21:32 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:21:32 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 18 Nov 2025 03:21:32 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 18 Nov 2025 03:21:32 GMT
CMD ["pypy3"]
# Thu, 20 Nov 2025 19:45:05 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:45:05 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:45:05 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 20 Nov 2025 19:45:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6823324682842ec1bf2ad33450d5f12e7c468c1fc4fa38f3a049bc41506b0e22`  
		Last Modified: Tue, 18 Nov 2025 03:21:47 GMT  
		Size: 1.2 MB (1227777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188e534a50347ffef95298aa1459a2910aa407d2013b11d05f48ca22b9a7c326`  
		Last Modified: Tue, 18 Nov 2025 03:21:50 GMT  
		Size: 34.2 MB (34236809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448be1aa7ab0f5c581825bbc1aa8d9d245236925afd062e36201a0cd781d438e`  
		Last Modified: Thu, 20 Nov 2025 19:45:19 GMT  
		Size: 7.9 MB (7867616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:67f17b735bde0c2aa28632c27a9399490568eeb233df6683559f9cc40e0f18f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608118813db8429b513471a8f218f1d62546282476c9dd2e83821867f4b157d1`

```dockerfile
```

-	Layers:
	-	`sha256:0a5b71a1bf48305071c3c747662d51db280330436f90acc4273403eabc80cb75`  
		Last Modified: Thu, 20 Nov 2025 21:21:54 GMT  
		Size: 2.2 MB (2235925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d703d698406aa70e33956e19beeb3013177e3d0a3aa91d4091cab1c89b5dd02`  
		Last Modified: Thu, 20 Nov 2025 21:21:54 GMT  
		Size: 11.2 KB (11198 bytes)  
		MIME: application/vnd.in-toto+json
