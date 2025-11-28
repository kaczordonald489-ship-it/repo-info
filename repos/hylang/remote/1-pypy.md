## `hylang:1-pypy`

```console
$ docker pull hylang@sha256:59a8a998fc6efdbd12f0079698c3db106e4d221260ab762a36879d64e4847066
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `hylang:1-pypy` - linux; amd64

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

### `hylang:1-pypy` - unknown; unknown

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

### `hylang:1-pypy` - linux; arm64 variant v8

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

### `hylang:1-pypy` - unknown; unknown

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

### `hylang:1-pypy` - linux; 386

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

### `hylang:1-pypy` - unknown; unknown

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

### `hylang:1-pypy` - windows version 10.0.26100.7171; amd64

```console
$ docker pull hylang@sha256:2117ef1239da2e8e10bc068251d78a0b181446d24274c277e8c4f5b69da3c0a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3290863173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bc71b90ea4ba0f084a9903e063d35667844706c41778542f27d0ffe0529b00`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:27:14 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:27:23 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:27:23 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 11 Nov 2025 19:28:06 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:28:07 GMT
CMD ["pypy"]
# Thu, 20 Nov 2025 19:44:30 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:44:31 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:45:30 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 20 Nov 2025 19:45:30 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8285ac56aa8dfc6927624dc14fae2bfc7d25d53da7342eb169af1b4433e08d02`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3946b48a3a8e69231ebe93558658226c6e53f281d568fd74b5e2fda8d16fc17`  
		Last Modified: Tue, 11 Nov 2025 19:28:24 GMT  
		Size: 358.9 KB (358917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ce9f865a1fbb63ea6ed95fd2f3ea88bbf38551e91515451f0636e5b698aae1`  
		Last Modified: Tue, 11 Nov 2025 19:28:25 GMT  
		Size: 15.5 MB (15529573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f628114af2eda98472aa5ec10fdc837f8ec8a924a4c0306bb2b28686529694cb`  
		Last Modified: Tue, 11 Nov 2025 19:28:24 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6b8c56e76c031cbd1e553f2eb5d1e8af9cb75b0b1d6046d6c87d0b6daa2c95`  
		Last Modified: Tue, 11 Nov 2025 19:28:27 GMT  
		Size: 30.7 MB (30670943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fbf78de2bbdb6d3dd6712af6b8568aa09ef6135c1639945a7e3c8ac78b4739`  
		Last Modified: Tue, 11 Nov 2025 19:28:24 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51553d7ef7b6784ddc172b974527503ebabc753edc57bf3361523c780584aa5`  
		Last Modified: Thu, 20 Nov 2025 19:45:42 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f44ddd8e5847c59fe60403e4b67008529261dd26ef36456416f412cb053a04`  
		Last Modified: Thu, 20 Nov 2025 19:45:42 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea642060bf8e61750450bf45ba4d0ede87d1eda3807058a426b2e0411ab548db`  
		Last Modified: Thu, 20 Nov 2025 19:45:43 GMT  
		Size: 8.8 MB (8840144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84de9dcbad826db5b329fe417c0cbc2bbcc82be7edf6353f2b5b29ca70ec7e2e`  
		Last Modified: Thu, 20 Nov 2025 19:45:42 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-pypy` - windows version 10.0.20348.4405; amd64

```console
$ docker pull hylang@sha256:df129f6d66851e1c2a1891c8af3744975af058b0769e6d4097289225ed31635c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1825488411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de3ae1bceeb233fe69db5c032d1690a72765a0a90ab61847d9270042ab9e382`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:28:14 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:28:24 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:28:25 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 11 Nov 2025 19:29:03 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:29:03 GMT
CMD ["pypy"]
# Thu, 20 Nov 2025 19:42:32 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:42:32 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:43:28 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 20 Nov 2025 19:43:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442760c8d26f9c34d441d655bfed0213774e9ee1491b0a9d451ba3951353bd99`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d80c29a0842a34f8c512d7c99d3ec6a50bc0da8baa6234281af26593606c756`  
		Last Modified: Tue, 11 Nov 2025 19:29:21 GMT  
		Size: 487.9 KB (487935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c736ff67c1729815898cab1f0ce89d5cc7b38c9928a3fea417d6ad98d67de66`  
		Last Modified: Tue, 11 Nov 2025 19:29:22 GMT  
		Size: 15.5 MB (15529843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3ced131808af1789c74f41256a2ab4d8e46d6013f7e28cfdb0bb2633dc4b8f`  
		Last Modified: Tue, 11 Nov 2025 19:29:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9685518121426f07f379bea6b65794018f09c0c737b442db076d9db44acc80c1`  
		Last Modified: Tue, 11 Nov 2025 19:29:25 GMT  
		Size: 30.7 MB (30672291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea916fe33d8d87609385929be1936f8ca3934e23cec287a7b788a7fc5badf25`  
		Last Modified: Tue, 11 Nov 2025 19:29:21 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a788febd4647e53bca83411bacc17e560fbd0e54ed9b76a66879585bf81c30da`  
		Last Modified: Thu, 20 Nov 2025 19:43:40 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a675be48786f954763d72d3a128348086b736ba6950c7385816eac1388858a2c`  
		Last Modified: Thu, 20 Nov 2025 19:43:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde02c42db77134fc27b0ba615febed876dbc24b01f8c36f50c5dc0af14eda9e`  
		Last Modified: Thu, 20 Nov 2025 19:43:41 GMT  
		Size: 8.8 MB (8829029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2be63de21791d6f9c102c011e9fe8497ee4e74fa5db9710254ed31a90cddd40`  
		Last Modified: Thu, 20 Nov 2025 19:43:40 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
