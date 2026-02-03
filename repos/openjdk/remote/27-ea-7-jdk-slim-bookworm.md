## `openjdk:27-ea-7-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:7fe66bd77fe27cd9b7146790a16dda30b82d2bf1b9f949e51f858cee8e45b733
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-7-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:7b8f2ec34074c84c53b9f8188c0d0ea87a0a38c4ba5ec7a1c548dd3c1eb1cf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260663033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2824118be95ed1e0ebc9348ff602f11772222b9259f46851952de75d6ece18af`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:50:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 03 Feb 2026 02:50:46 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:50:46 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:50:46 GMT
ENV JAVA_VERSION=27-ea+7
# Tue, 03 Feb 2026 02:50:46 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 03 Feb 2026 02:50:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd34b0de2cfa752d2b6ef8bee598ee1cb9c8773d5be404de698e4c60b6144b81`  
		Last Modified: Tue, 03 Feb 2026 02:51:05 GMT  
		Size: 4.0 MB (4029125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878ca84c9038ec97aeb7b3ae68d678e5519f9ded165266bce108efdab2e277e7`  
		Last Modified: Tue, 03 Feb 2026 02:51:10 GMT  
		Size: 228.4 MB (228405421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-7-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:9a1e26356dcec88b7286cbd295f459e21f37d518866b2adc2d210a147bbff036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab7840233c2725dcdffdbb28f32b2893d008a54a611262bd6a152895c15837e`

```dockerfile
```

-	Layers:
	-	`sha256:becbeb5d8dfa5e2938767d730c64b1a1f21cb4863553f4c39cef6bd3c945c333`  
		Last Modified: Tue, 03 Feb 2026 02:51:05 GMT  
		Size: 2.6 MB (2649170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfb585db58d9577e6fc89ad16f1eec22921f545ffc073e3cbfddbaa1b1c2899d`  
		Last Modified: Tue, 03 Feb 2026 02:51:05 GMT  
		Size: 16.9 KB (16858 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-7-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bf9492f01b20aa3f609c5cc915452740a1a5ab5355dff9ea59a33ee0822abc53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258304314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e58d49b9f35123a43563d5703576b8e077415face83095a0db1016b6f15cc8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:53:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:53:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 03 Feb 2026 02:53:12 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:53:12 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:53:12 GMT
ENV JAVA_VERSION=27-ea+7
# Tue, 03 Feb 2026 02:53:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 03 Feb 2026 02:53:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a944c22a754794a91aad7a209f92c961c852844de930313f3cb8c6dae1bad3`  
		Last Modified: Tue, 03 Feb 2026 02:53:33 GMT  
		Size: 3.9 MB (3851951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02013b402b6dac749bc8ce971fd93867af13bb1b3e01ef18ace7120ebd0b3911`  
		Last Modified: Tue, 03 Feb 2026 02:53:38 GMT  
		Size: 226.3 MB (226344540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-7-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:8f637c6d73d70275fce8dcc15d4bc1188fa196a5608389aef412bff772fd0d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c8ac557345965667f4da0e4db63cc81df0595a2df541058a71110d4da571c9`

```dockerfile
```

-	Layers:
	-	`sha256:6d48ea7f0a82446dab66397fcf76056cb59fa5ca126e1e1dcc0953e64f9be4ce`  
		Last Modified: Tue, 03 Feb 2026 02:53:33 GMT  
		Size: 2.6 MB (2648804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdbf5675b13d0af290b9f0049419c2c41460cc5ff444c635a77e0854cedb91c5`  
		Last Modified: Tue, 03 Feb 2026 02:53:33 GMT  
		Size: 17.0 KB (16976 bytes)  
		MIME: application/vnd.in-toto+json
