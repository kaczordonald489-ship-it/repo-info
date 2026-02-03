## `openjdk:26-ea-slim-trixie`

```console
$ docker pull openjdk@sha256:90e9a99e4eb86436c9956284c651896c470b582d0399af2a42ac6a40dd5135ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:b92688d80b91feb45f69d4f7040fc8b1c556ad6c9064da4ad6abf7422e0ea4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260185257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf3175e64f02f8e11a21b2c788b750ec9bf68bec4819e1b3b428dd268d8bf3a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:50:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 03 Feb 2026 02:50:24 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:50:24 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:50:24 GMT
ENV JAVA_VERSION=26-ea+33
# Tue, 03 Feb 2026 02:50:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 03 Feb 2026 02:50:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416de081c3e53e64716f8e3fd3a8d98047c718c3ec77b493a712e6b9901e3de4`  
		Last Modified: Tue, 03 Feb 2026 02:50:44 GMT  
		Size: 2.4 MB (2370964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2766eead1fc19b54afb7c7999a3b04631d2ca6a4c6c456ac38f1ed03fecaff`  
		Last Modified: Tue, 03 Feb 2026 02:50:49 GMT  
		Size: 228.0 MB (228035697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:9da2d292ebcc914f0e4a3ddeaece3c2c978e675112d0bba4f7876fd607094e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599159520e4f158c2799258f9f1d5e1c9a32172b4355713e9df95b14e5276d8e`

```dockerfile
```

-	Layers:
	-	`sha256:833559b307e2cece059a3d848f7760956cc7d419e266f2062ad87e9f86083882`  
		Last Modified: Tue, 03 Feb 2026 02:50:44 GMT  
		Size: 2.3 MB (2278851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7916eacfd3001a81240730f3c2fb42bf8bc69b943d896d0fec0f17c6dcee6a43`  
		Last Modified: Tue, 03 Feb 2026 02:50:44 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f399ea69916b2c376fadceb50d139ac1fc42cdd4c4a7a9fe87cb0f9541c60cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258405767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20678c452dbbe8db5dd2bda7dd01e58b8577d9f69ebaf57be459f33c27aa6f0b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:53:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 03 Feb 2026 02:53:06 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:53:06 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:53:06 GMT
ENV JAVA_VERSION=26-ea+33
# Tue, 03 Feb 2026 02:53:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 03 Feb 2026 02:53:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2773d010414a660c371754c0d9d4eabbf9822334b8affc51b35c5bb39cdeccb5`  
		Last Modified: Tue, 03 Feb 2026 02:53:26 GMT  
		Size: 2.3 MB (2314422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c075c750d62f328c332924f73936135011f491d24f0541383618b1cb4a030950`  
		Last Modified: Tue, 03 Feb 2026 02:53:30 GMT  
		Size: 226.0 MB (225951281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:94ab176af8295dd46adb9c7261afc70872b96e3c2960953bbd3e7b811240f9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c0a63ccb1988088607a9070f29488d539390ca5734a14b647c74d01a0ae542`

```dockerfile
```

-	Layers:
	-	`sha256:66d4f9d8a6454a2f85c8752ac01e3b5d1775c2acade90665aff451f7265caeec`  
		Last Modified: Tue, 03 Feb 2026 02:53:26 GMT  
		Size: 2.3 MB (2278537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3cde2d2cbd50faa4b835f55d9f1e20d913117766dac2806b27715c3231bdb7d`  
		Last Modified: Tue, 03 Feb 2026 02:53:26 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
