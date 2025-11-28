## `pypy:3-slim-trixie`

```console
$ docker pull pypy@sha256:90a80839199f3035525a8b9f5caa568f95fcb57dc8c704b60395dd060b728fbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:3-slim-trixie` - linux; amd64

```console
$ docker pull pypy@sha256:a994222df21ad95ae339b5e8e68c7937466ace1bfb71a00369292bd5060b845d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68835107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ee49a04f069f14842143b635495375d34514d955ebf8e63fedb9fbacb11ff5`
-	Default Command: `["pypy3"]`

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

### `pypy:3-slim-trixie` - unknown; unknown

```console
$ docker pull pypy@sha256:51c307e791e7baa9fbf4bae0965d2453f1c88742aedc062c0de9f8f383b4d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cedd509386cd9b89636faddde3ecbd3b059d6bc1c7ed5efcd0e64ee556ce98`

```dockerfile
```

-	Layers:
	-	`sha256:9710d4218b4bf0cd3a3137f81c88fc1a51f278641f222ded4258c9a1cc4eea4a`  
		Last Modified: Tue, 18 Nov 2025 07:42:02 GMT  
		Size: 2.2 MB (2231863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0266502deea577ca12ba98d7c5d5ca2203e03f257f8416e2a3c68ad7e2ddb08b`  
		Last Modified: Tue, 18 Nov 2025 07:42:03 GMT  
		Size: 24.6 KB (24633 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:bd318c677d9a8bab3bdd4476c6d9c48d57ae6a152af8594da34ce4cd4d0d03f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67497392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4435b1ff0747596c65c052b8af6abc47c182e12514bbcbddae1e848d291e4999`
-	Default Command: `["pypy3"]`

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

### `pypy:3-slim-trixie` - unknown; unknown

```console
$ docker pull pypy@sha256:bddea581e97adc3ebbb88fb62ef50f342c12c52c05608b2096e5bcb0bbec9617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2000de8319db3915fbde8610b53da2257261173ba00b968f414dec17657b04b1`

```dockerfile
```

-	Layers:
	-	`sha256:c1fe3e33c8ebd5bd9ada7dace320e887fc61d513d8b19f9321b93be900c5a270`  
		Last Modified: Tue, 18 Nov 2025 07:42:07 GMT  
		Size: 2.2 MB (2232298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d948a62ff72d02577fbac6403e6cc71cfe62d5fb6bb1ba75e6b6d22db7793d`  
		Last Modified: Tue, 18 Nov 2025 07:42:08 GMT  
		Size: 24.9 KB (24919 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-slim-trixie` - linux; 386

```console
$ docker pull pypy@sha256:63bc7774677ec2be22179e0d4ef61741ec697f4284d3f47baf78282d8a8948f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66757654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c7f661ff2bf9746acca8c9b630eac47da359cb26a3f00e33d00e602c58d0e3`
-	Default Command: `["pypy3"]`

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

### `pypy:3-slim-trixie` - unknown; unknown

```console
$ docker pull pypy@sha256:b3eb384d5ce5dfdb48ee950cd59c4499a5c5eac77238b3f0d71b0bbb1a67e870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af30e63a240e792be950a619a305b52b4b6233ce8225c792fcf94e26850f394`

```dockerfile
```

-	Layers:
	-	`sha256:81f65d6d7b24936254b52338554e7cd96a2c63557c242cd50e843742d1e07ec5`  
		Last Modified: Tue, 18 Nov 2025 04:43:00 GMT  
		Size: 2.2 MB (2228972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee2bc5087a4748a38d79dbdc57ccf59f717d343a37f738316b7ebb906c646b1`  
		Last Modified: Tue, 18 Nov 2025 04:43:01 GMT  
		Size: 24.5 KB (24529 bytes)  
		MIME: application/vnd.in-toto+json
