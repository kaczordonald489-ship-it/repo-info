## `openjdk:26-ea-33-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:afe905e46f48c166c287b9cab37b487653fb4a77049a71dc5df43fbe736f7c45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-33-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:996be21f0082df57d3dfc38b4a2edb05b761a78523f7efc3455dc2b4b224c16e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260293285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb7be9df0013455644166b94cc4ea019aa09b9024a9227c2d2e8c1ca722e152`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:50:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 03 Feb 2026 02:50:22 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:50:22 GMT
ENV JAVA_VERSION=26-ea+33
# Tue, 03 Feb 2026 02:50:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 03 Feb 2026 02:50:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b304cf855f0f33d07bafba36074f0735d768ec43586c9a75eba5c46d57dfe15`  
		Last Modified: Tue, 03 Feb 2026 02:50:41 GMT  
		Size: 4.0 MB (4029225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb57181e6f7c2ff0ca3c2929ff279c843006d81558bdb72215b8323cc01c4c4`  
		Last Modified: Tue, 03 Feb 2026 02:50:45 GMT  
		Size: 228.0 MB (228035573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0ad3318b4e624169ae87797ccc07c6a800baf0eabb13a7e3f19b1d8fc843e639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df15ce4deec9a0dc55d0653a6228fd25d8891c83e5806117c92f09b536a713b7`

```dockerfile
```

-	Layers:
	-	`sha256:8c7aa62a1c6c849dda8423b08bd657b88c8e070540f8f04cc1d17a6f5dd63dec`  
		Last Modified: Tue, 03 Feb 2026 02:50:41 GMT  
		Size: 2.6 MB (2649799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aec39b311cb729607c18ec490679e617b9f73680d8cf4fbebaedfef110eb6c21`  
		Last Modified: Tue, 03 Feb 2026 02:50:41 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-33-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:75ae69e374347659db98d03cae1779d87a051eb84bf372fae4e524db6238ac15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257907666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a798988f1645ba1f2a66485d6b5d80cd10cd5e04035994b23f4a2948a869c6ad`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:53:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 03 Feb 2026 02:53:05 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:53:05 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:53:05 GMT
ENV JAVA_VERSION=26-ea+33
# Tue, 03 Feb 2026 02:53:05 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 03 Feb 2026 02:53:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a51c6792840209bc00f1aea87608ff785735fd0f04efc072ae6d15e0726b94`  
		Last Modified: Tue, 03 Feb 2026 02:53:26 GMT  
		Size: 3.9 MB (3851961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38be8a6489838a6554746a836bcf3156a028d210b879ec453ac93775882b1532`  
		Last Modified: Tue, 03 Feb 2026 02:53:31 GMT  
		Size: 225.9 MB (225947882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:cf428df2fec50cfb096faf3df2e22f8edf51c6662efaf031bf3ba769b093ebce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b763f87a4d9aef2e42c6fabe8cb486df963f7a2f0f9ca20154bc3642a21b1fd5`

```dockerfile
```

-	Layers:
	-	`sha256:34c5db32ce18fa26ae24326eff74bb8c91d8183741befa2fd4ba6053af9a2178`  
		Last Modified: Tue, 03 Feb 2026 02:53:26 GMT  
		Size: 2.6 MB (2649433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37a69f88b13d7627be24212aa9bab0f2db18e6baec6257a49ee18f5a8f70f78`  
		Last Modified: Tue, 03 Feb 2026 02:53:26 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
