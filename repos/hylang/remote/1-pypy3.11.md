## `hylang:1-pypy3.11`

```console
$ docker pull hylang@sha256:79b9967007da56fa5e144aff7d8fbef443b4f1e5b46b622bf0a50686a2db8a2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `hylang:1-pypy3.11` - linux; amd64

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

### `hylang:1-pypy3.11` - unknown; unknown

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

### `hylang:1-pypy3.11` - linux; arm64 variant v8

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

### `hylang:1-pypy3.11` - unknown; unknown

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

### `hylang:1-pypy3.11` - linux; 386

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

### `hylang:1-pypy3.11` - unknown; unknown

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

### `hylang:1-pypy3.11` - windows version 10.0.26100.32230; amd64

```console
$ docker pull hylang@sha256:13d913e72399713f3bc01abea4b4986d231f488e429a992b97ce121b705f5744
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1551192951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc10342980d50751ff96cb47b46eccbb37a087e1a6ff4ae1d5352ec40723477b`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:01:06 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:01:15 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:01:15 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 13 Jan 2026 23:01:50 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:01:52 GMT
CMD ["pypy"]
# Wed, 14 Jan 2026 22:03:56 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 22:03:57 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 22:05:07 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 Jan 2026 22:05:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efa37c091ab5ec4869e2ab85fd61db9ffc02e5ee0f087000562c7b74d0ace95`  
		Last Modified: Tue, 13 Jan 2026 22:54:55 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811f9956f15897d4609b84a7a598d1b6af09c6095cffb78e1eb3bd7cca1dfb89`  
		Last Modified: Tue, 13 Jan 2026 23:01:56 GMT  
		Size: 383.8 KB (383812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a237c7c700c6a65c03052392f2bca636915dea66276acda9f090e4f6708b532b`  
		Last Modified: Tue, 13 Jan 2026 23:01:58 GMT  
		Size: 15.6 MB (15560688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cf56576cf098e66e238684e1d61a9bfd768a06d5c5e0ac7d7addbf8411633b`  
		Last Modified: Tue, 13 Jan 2026 23:01:56 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50569a64d765a7719bc9198243edd1db5e9cadd60d603c4f6607f08aa6fc5b72`  
		Last Modified: Tue, 13 Jan 2026 23:02:00 GMT  
		Size: 30.7 MB (30693687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f699ce7062aa7938a793d08a8845e1869af2ff8402c5336f6df0cf2f161cc2`  
		Last Modified: Tue, 13 Jan 2026 23:01:56 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f25fcde554117b23b433b580406795ae989e447e738bee07df39de68766d6ad`  
		Last Modified: Wed, 14 Jan 2026 22:05:12 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7046cbefdba9fcf1c9568e8d16ad7660e1cd9610ecd97ade65b3908caa6289`  
		Last Modified: Wed, 14 Jan 2026 22:05:12 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903bdf01a771d51c073c6227eedab7f15d00ad4eea1de4895d581a3bf9a0359f`  
		Last Modified: Wed, 14 Jan 2026 22:05:14 GMT  
		Size: 8.8 MB (8786569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd57a5ba11baf90c0ab1dfc4ae5dd694d71b75356e45d469e6cf87d32889e99c`  
		Last Modified: Wed, 14 Jan 2026 22:05:12 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-pypy3.11` - windows version 10.0.20348.4648; amd64

```console
$ docker pull hylang@sha256:38ae998d113556f54c5efebd61d0b2e43b9626ebd4788de1a1d10579bf53672b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1891098369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0652ad8522bca333246be72ce814e810cfcbc613b89c78bab9a3dbd4f2406e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:54:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:11:56 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:12:05 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:12:06 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 13 Jan 2026 23:12:42 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:12:42 GMT
CMD ["pypy"]
# Wed, 14 Jan 2026 22:03:34 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 22:03:35 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 22:04:28 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 Jan 2026 22:04:29 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f08760e06519dd29e9a52391dac11e5952f68046c79c4bdea23cb54196c9897`  
		Last Modified: Tue, 13 Jan 2026 22:59:44 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27312a9f7bf9397d877f52fa65cc2a37431648e3defc89630bd9b9ffe4828206`  
		Last Modified: Tue, 13 Jan 2026 23:12:47 GMT  
		Size: 486.1 KB (486093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35263fd2f63c29340963f82cb88e73ee7e4cc3e5c91c06dd678d444d1b88f0d9`  
		Last Modified: Tue, 13 Jan 2026 23:12:49 GMT  
		Size: 15.5 MB (15528198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ec3d1f7c2afb3e7f80fe185d930a03fd99911031e8521616817190b1e4228c`  
		Last Modified: Tue, 13 Jan 2026 23:12:47 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47515769f526c0f3652f708639ecaa989b6e48dd5eb642bb48dfd548f5af7d7`  
		Last Modified: Tue, 13 Jan 2026 23:12:51 GMT  
		Size: 30.7 MB (30664641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a30789d9bbf357e1d8e8941e629b59f6266af5c945c580c412b034567a046b3`  
		Last Modified: Tue, 13 Jan 2026 23:12:47 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c613227aa92be1086d56c3212b415b0d519ca5a46bcbd7bec43f3b9fea7074`  
		Last Modified: Wed, 14 Jan 2026 22:04:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a5c36dbda7b4062faf5af7aa7f4afd62529dd1672f7265695a045724154d42`  
		Last Modified: Wed, 14 Jan 2026 22:04:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12a219e1ef69a8eeb4b27fd400d6f7ec23f1f0faaaa8ac92b14e1e09be319a6`  
		Last Modified: Wed, 14 Jan 2026 22:04:35 GMT  
		Size: 8.8 MB (8752447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f9fe6cddf0512da31eba94cb858503c09f0a11f79a9bab19e3aa3a4a1395ec`  
		Last Modified: Wed, 14 Jan 2026 22:04:34 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
