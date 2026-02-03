## `hylang:pypy3.11-trixie`

```console
$ docker pull hylang@sha256:5a048e9cbcf6f5e357e8a3a1e5c1d6c47d48120756bc5f45ee50f6c068bb3460
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:pypy3.11-trixie` - linux; amd64

```console
$ docker pull hylang@sha256:470bd08d08c777c067e62e13d56900f8b3a72049a74020477280282f71265597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76578725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167a7309b8cfe1f8ed9269f89bbd48324d6172e7b51c8143f981ede33f1999bb`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:00:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:01:03 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:01:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:01:03 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 03 Feb 2026 03:01:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 03 Feb 2026 03:01:03 GMT
CMD ["pypy3"]
# Tue, 03 Feb 2026 03:45:04 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Feb 2026 03:45:04 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Feb 2026 03:45:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Feb 2026 03:45:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3628c889dd4b011ed269ecb9f0a3c0088ef913f738dade7ca0309291282ecae9`  
		Last Modified: Tue, 03 Feb 2026 03:01:14 GMT  
		Size: 1.2 MB (1220080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abe45a7245626f7dbb428a8b1287bc11333f5084240c87892d046baf534d2f1`  
		Last Modified: Tue, 03 Feb 2026 03:01:15 GMT  
		Size: 37.8 MB (37839136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d8cc4010430e5751e851364643f0aeb32c35b6b61c03a06e91769d4ddb1f3b`  
		Last Modified: Tue, 03 Feb 2026 03:45:12 GMT  
		Size: 7.7 MB (7740913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:88e7bd0dd17b5d7dda1f793f65d976d6285afa7f6976251071b26c17a9aabb57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5abbed0f7a032c2a1702be5244175cfc30a904299064ea028a95e5a71bbfbf2`

```dockerfile
```

-	Layers:
	-	`sha256:1312e067fc9d3b3b7d441f0c3963fd8f441eb4ef244b16a1b5697e57b9848e07`  
		Last Modified: Tue, 03 Feb 2026 03:45:12 GMT  
		Size: 2.2 MB (2238904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47767e0b2963cc71090ac9fbc35bfb01da99802be9e4dde18a61aa1eeea1b453`  
		Last Modified: Tue, 03 Feb 2026 03:45:12 GMT  
		Size: 11.3 KB (11290 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.11-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:d2c42ddc4c7e5c8a5aba61a2e457c06219e6441532349c6e5228d46ea3beae79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75239817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aba989311e2edb70392dd4879bef56aeace279cc317d3393543f66f37e3b86`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:04:13 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:04:13 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:04:13 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 03 Feb 2026 03:04:13 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 03 Feb 2026 03:04:13 GMT
CMD ["pypy3"]
# Tue, 03 Feb 2026 04:02:44 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Feb 2026 04:02:44 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Feb 2026 04:02:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Feb 2026 04:02:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ec0b1646c2a46e24147c99e4250d7536ebd7b5f6a891a0a19b335280bfcc94`  
		Last Modified: Tue, 03 Feb 2026 03:04:25 GMT  
		Size: 1.2 MB (1201882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d7e035f885b09e79fb5c888aeec90bcc9b62582231e6e884db524719e66e50`  
		Last Modified: Tue, 03 Feb 2026 03:04:26 GMT  
		Size: 36.2 MB (36156592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918d8923fe0cad7857b0793f4d7d72e4c1758988e7b9392063de7d75af809780`  
		Last Modified: Tue, 03 Feb 2026 04:02:52 GMT  
		Size: 7.7 MB (7741279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:89d4ce423f93f1a7e3b2160337b151d015fefdc58567c11c2aaee4a1a1b6a611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800f767aae05ff3dfea1f5c88d971bc3bb181e15b536fa6d84a0096912c8922b`

```dockerfile
```

-	Layers:
	-	`sha256:0284b10952e25e2a497d555ca69751eac4df6ba6878fb001c0796bdc39efadb8`  
		Last Modified: Tue, 03 Feb 2026 04:02:51 GMT  
		Size: 2.2 MB (2239315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89d0d1adb132d1b073eb8e57f272b13496b3a9e6c34b9c635e86a135f47422a7`  
		Last Modified: Tue, 03 Feb 2026 04:02:51 GMT  
		Size: 11.5 KB (11538 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.11-trixie` - linux; 386

```console
$ docker pull hylang@sha256:503aaaaa4598cd6a96df55ab81f9cfaf3505005c788c6674e8235cfac80dcf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74500008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bba71dba43a13801461e678c14c9fc53f5e54bdd3c4a2dca35e2460ccec48c1`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:57:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:57:49 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:57:49 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:57:49 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 03 Feb 2026 02:57:49 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 03 Feb 2026 02:57:49 GMT
CMD ["pypy3"]
# Tue, 03 Feb 2026 03:39:41 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Feb 2026 03:39:41 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Feb 2026 03:39:41 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Feb 2026 03:39:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cab89acd8aa0bbdef5c314dc4d99d1268362e2b61fe64c250ecdc9ea8e74dd`  
		Last Modified: Tue, 03 Feb 2026 02:57:58 GMT  
		Size: 1.2 MB (1227825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b824557a751dc2c06db1420a2bfd6040085d33d9ff594a5762d3bf6a48e3a7`  
		Last Modified: Tue, 03 Feb 2026 02:57:59 GMT  
		Size: 34.2 MB (34237379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa23f1f926e7c0e43f831875c101c7971e161aac0661713728088d5b16fe9e1`  
		Last Modified: Tue, 03 Feb 2026 03:39:48 GMT  
		Size: 7.7 MB (7740949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:c3072ad7c8ecbd3f27c3d4cc6328b89678351e66240238bccaf211a694e83eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfe15a5ef43b60f3645b550a860bef3807da6ed590051a50c3f1e34d93c23a9`

```dockerfile
```

-	Layers:
	-	`sha256:c97d122bbd24f1ba92d8231a888f6de613af12650e44b37f81f4135ad8b33b78`  
		Last Modified: Tue, 03 Feb 2026 03:39:48 GMT  
		Size: 2.2 MB (2236023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89cf5345b8e3efcd8d61c756d2d45f89dea5d29b1b4788301b6fb4d34395c96f`  
		Last Modified: Tue, 03 Feb 2026 03:39:48 GMT  
		Size: 11.2 KB (11198 bytes)  
		MIME: application/vnd.in-toto+json
