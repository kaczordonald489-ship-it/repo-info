## `openjdk:26-ea-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:66b51aad6e7140f386608b4b81e90bb34f5ddbadfac911266f5606bf150689aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:ae6d526e5a5c45fa79fb25bcede8257cb3a110709a9001a7505ff03de38a0648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260163998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5799655e09e42c625aea714fa64499259ae78a6e2318f7d20be9128c56508f38`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:39:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:40:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 24 Nov 2025 22:40:06 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:40:06 GMT
ENV LANG=C.UTF-8
# Mon, 24 Nov 2025 22:40:06 GMT
ENV JAVA_VERSION=26-ea+25
# Mon, 24 Nov 2025 22:40:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='34a09a42f38d04f223c2c3c3665e4638bcda263c69c38e8e363760be8ceeaffd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='33e9133fcee05a36df65b43ceea8dd2c16ff6fe9c0186acd0a697547c2bd7a42'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 24 Nov 2025 22:40:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64c3e636e8d8e8edd6b158856af9702712a059a3f13fdb195eca3215e96b1c6`  
		Last Modified: Mon, 24 Nov 2025 22:40:45 GMT  
		Size: 2.4 MB (2371028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb572327389f17f25da06ad85ea54eb8923a2ec60953a47fba43237ffbd5fcb`  
		Last Modified: Tue, 25 Nov 2025 01:25:57 GMT  
		Size: 228.0 MB (228016486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:b002213e4fecf774e3ba3e07089bdc90f2c644311db0f2523ea4dd3292520be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b9fc533b25995c3930da111c051dc558e6890608a2dde5759d665d49f3fa17`

```dockerfile
```

-	Layers:
	-	`sha256:0bae08897b01c87bd3b5ac3e06c6e4fde11d9354c4635cd574e31271154946ae`  
		Last Modified: Tue, 25 Nov 2025 01:24:05 GMT  
		Size: 2.3 MB (2278789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cb3c5ba1a42ceb25239099e2ebf56a11d959c462b26337c29074161af454129`  
		Last Modified: Tue, 25 Nov 2025 01:24:06 GMT  
		Size: 18.1 KB (18108 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:21143896cc9e324b0dbc3173d8e801cb9637594f2471d6850cf0f5d02b971b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258324643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981a92ff04f2c39b833dee65c74ee648488104bd5a0df1d1920d1321ce271b4b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:40:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:40:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 24 Nov 2025 22:40:44 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:40:44 GMT
ENV LANG=C.UTF-8
# Mon, 24 Nov 2025 22:40:44 GMT
ENV JAVA_VERSION=26-ea+25
# Mon, 24 Nov 2025 22:40:44 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='34a09a42f38d04f223c2c3c3665e4638bcda263c69c38e8e363760be8ceeaffd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='33e9133fcee05a36df65b43ceea8dd2c16ff6fe9c0186acd0a697547c2bd7a42'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 24 Nov 2025 22:40:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebcd3c2980a32d8d69981cb4954323383f68763439ac02ff39b4be597c9a11b`  
		Last Modified: Mon, 24 Nov 2025 22:41:15 GMT  
		Size: 2.3 MB (2314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805888628673391fe043d79f0d19a3680570d3b91b88aa7c7e1aad0f6ee9a765`  
		Last Modified: Tue, 25 Nov 2025 02:20:27 GMT  
		Size: 225.9 MB (225871934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:76b13c7f6d1768635999e96c12c4ec90a143023092397af185a80bdc2b8d1b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3227a8f52afb7e250682aff14696c0c6c7e23e3c2ff243a84b8604a5b67af41e`

```dockerfile
```

-	Layers:
	-	`sha256:4ce00b94c3034672968cfb13f4de86971b1893cf6493c29f32bc7fde9c26a5e2`  
		Last Modified: Tue, 25 Nov 2025 04:09:43 GMT  
		Size: 2.3 MB (2278475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f1c7df33480b7ea0ad107815533ad48beb57638cbb6dafab76d120e90cf335`  
		Last Modified: Tue, 25 Nov 2025 01:24:11 GMT  
		Size: 18.3 KB (18275 bytes)  
		MIME: application/vnd.in-toto+json
