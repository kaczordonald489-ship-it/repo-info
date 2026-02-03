## `hylang:pypy3.11-bookworm`

```console
$ docker pull hylang@sha256:8ea39fc19c4c9dcebbb5d57c4e5f65a1114b04693a71d7bc2b42f478beae1b96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:pypy3.11-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:5ec4128aa5bdb59aa6a199d0c38ddd2cdecce18d83522c4c98a266562adf02ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77686531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efbc5fa297fb9d75485119c78b03a807fa178b78c5a426eb0193d4b24f5d57a`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:01:43 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:01:43 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:01:43 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 03 Feb 2026 03:01:43 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 03 Feb 2026 03:01:43 GMT
CMD ["pypy3"]
# Tue, 03 Feb 2026 03:45:05 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Feb 2026 03:45:05 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Feb 2026 03:45:05 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Feb 2026 03:45:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085e2e27e2cb194b5fbecad50af761d212b6ecffe8b43828d02ee975ac7873d8`  
		Last Modified: Tue, 03 Feb 2026 03:01:55 GMT  
		Size: 3.5 MB (3510218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474fcbc51b9a17c1f04829eb57c69702dd3d3254d0412870fb7870d5ca64cd4a`  
		Last Modified: Tue, 03 Feb 2026 03:01:56 GMT  
		Size: 38.2 MB (38206784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297c734f41e5e83278e1fc8dcafb30dfb644ee324cdde60a38689403d50f5653`  
		Last Modified: Tue, 03 Feb 2026 03:45:13 GMT  
		Size: 7.7 MB (7741042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:a2f976fccb032bb392d7c171ffd8ef214e3955c8e3309fa7b8cf001563e26e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc7157aa24721408209f056583f8f82913be2d24ee3907d19d9042060188fe5`

```dockerfile
```

-	Layers:
	-	`sha256:f78d7997faa4eebc3dc0532da8317c13bb0dad607585282a4d80d0d706bae5ab`  
		Last Modified: Tue, 03 Feb 2026 03:45:13 GMT  
		Size: 2.6 MB (2618905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3222f5d1a6b978c4e5d97315472f99920822e5d3f0b65d979d08ad4616d1991c`  
		Last Modified: Tue, 03 Feb 2026 03:45:13 GMT  
		Size: 8.9 KB (8900 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:0e1c727c5ff7907c8193aa8048eabc112123a1850d3f14bfa11cdfd06d006808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75714098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f09089a7a67ce27bb61e5f986ce8977c6c1e04f7a556774ebd9cc51de0e04b`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:04:12 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:04:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:04:12 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 03 Feb 2026 03:04:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 03 Feb 2026 03:04:12 GMT
CMD ["pypy3"]
# Tue, 03 Feb 2026 04:02:48 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Feb 2026 04:02:48 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Feb 2026 04:02:48 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Feb 2026 04:02:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10583e409ce51cb74dfb422bb130bcd49c533639504478f0a6ec7b51e9e5b31`  
		Last Modified: Tue, 03 Feb 2026 03:04:23 GMT  
		Size: 3.3 MB (3341528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ce55a789ea655ebdc101116e002e1918b252770e58fbbc8974ffab7880251`  
		Last Modified: Tue, 03 Feb 2026 03:04:25 GMT  
		Size: 36.5 MB (36523372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8eef221008db3118c805358d67608176dd4cf447e558186380e19c9bf64631`  
		Last Modified: Tue, 03 Feb 2026 04:02:55 GMT  
		Size: 7.7 MB (7741375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:d2ccafdf1e4c376264ff6a3c4037d129db1379b0e9c2dfb9ab70de5485a431dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd175176b16be58724441add85b90fd82415519b2507a9bbfe5b8ffa62f31547`

```dockerfile
```

-	Layers:
	-	`sha256:6f5f34a7bf4500b8d0c5b99b2845959ad3e6ee7c3c049fe72e244d9a4ff45eb4`  
		Last Modified: Tue, 03 Feb 2026 04:02:55 GMT  
		Size: 2.6 MB (2619220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c619b0647c3637d312ae8d352cbdff2daf8e5ab1c5cd0d7f33f4bf9244a42c`  
		Last Modified: Tue, 03 Feb 2026 04:02:55 GMT  
		Size: 9.1 KB (9052 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.11-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:02f52fde62566154b294629fb53c9d550270f7390f2f5e8e650998f998203f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75163368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1824396e0095fc1bf0255b7a8c975c4fbc63ab4ed502c973e2663f46a0fa19de`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:58:39 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:58:39 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:58:39 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 03 Feb 2026 02:58:39 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 03 Feb 2026 02:58:39 GMT
CMD ["pypy3"]
# Tue, 03 Feb 2026 03:39:44 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Feb 2026 03:39:44 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Feb 2026 03:39:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Feb 2026 03:39:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5f93d228262ac8f12d9af5f87a89d9722b3f4d559df30edfa91327db9f457723`  
		Last Modified: Tue, 03 Feb 2026 01:13:52 GMT  
		Size: 29.2 MB (29210015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbe0595d8e83ebc398bba6293210675620a407e356ff81d1547280d3128202a`  
		Last Modified: Tue, 03 Feb 2026 02:58:49 GMT  
		Size: 3.5 MB (3512889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0a4d79139843ffdada8caafa9a6baa9467a349ec1dc82419360050e0c2ad59`  
		Last Modified: Tue, 03 Feb 2026 02:58:50 GMT  
		Size: 34.7 MB (34699312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a0130cd529f81b3170a8978135e878cdfdcc152f433a83a7a01fbd109d0023`  
		Last Modified: Tue, 03 Feb 2026 03:39:52 GMT  
		Size: 7.7 MB (7741152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:9533f064cf98d1edde50fcbabf6426b2dbec80e27bdab14fb10a24891f52cfd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5a7863c2d686205f1ee9ddcc7a698632b5f1d44b7e85459f362df0ebedb41b`

```dockerfile
```

-	Layers:
	-	`sha256:19ef99349f637dd22ff43f020d17accf078324626b19310331a6a3c2f265c7c7`  
		Last Modified: Tue, 03 Feb 2026 03:39:52 GMT  
		Size: 2.6 MB (2616048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db1532d17e36372bb72f7271980936b48d3227ccf6619a3f313743c8115265a`  
		Last Modified: Tue, 03 Feb 2026 03:39:52 GMT  
		Size: 8.8 KB (8848 bytes)  
		MIME: application/vnd.in-toto+json
