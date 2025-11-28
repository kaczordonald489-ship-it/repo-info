## `openjdk:26-ea-jdk-trixie`

```console
$ docker pull openjdk@sha256:736a7f10a36cc9a8532d51a6a88541124dda28bbbf09ef00af28cf8d671ea01d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:b9bae5fbd7c02a841752e03c9de9b256d22c942035f6832807854686e2e3f0d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.7 MB (386712290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:292739983d1c05c35d0f5e2bf0a4123ae5a8f9612772afbcaa2637b63f7eff05`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 24 Nov 2025 22:38:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 24 Nov 2025 22:39:08 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:08 GMT
ENV LANG=C.UTF-8
# Mon, 24 Nov 2025 22:39:08 GMT
ENV JAVA_VERSION=26-ea+25
# Mon, 24 Nov 2025 22:39:08 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='34a09a42f38d04f223c2c3c3665e4638bcda263c69c38e8e363760be8ceeaffd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='33e9133fcee05a36df65b43ceea8dd2c16ff6fe9c0186acd0a697547c2bd7a42'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 24 Nov 2025 22:39:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae668646f447b181fe300ae6756351b6167aa2578be449b167ba79ed4926798`  
		Last Modified: Tue, 18 Nov 2025 05:11:30 GMT  
		Size: 25.6 MB (25613858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2e6e687b6ce78177a4cac678dd533c8e72b97469f030783b6bb491f681fd4c`  
		Last Modified: Tue, 18 Nov 2025 06:39:26 GMT  
		Size: 67.8 MB (67779054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cdb87ec97a58b10b4e784cb80e7ee0d3990932d0350fecb7be33d797919e14`  
		Last Modified: Mon, 24 Nov 2025 22:39:49 GMT  
		Size: 16.1 MB (16061688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce117efd5845710a38cd160e8b377e718c63e20ce34a28618745d4ffb7a1abf`  
		Last Modified: Tue, 25 Nov 2025 01:59:36 GMT  
		Size: 228.0 MB (227968143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:5aac1086a189127399f45930cd7bd34b129e2e27db73694d0d0c6621a50a4e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9286c2c2ea127b5612de1c3e008e2ea3f59d936556af609fdca7ed6ba26ab3`

```dockerfile
```

-	Layers:
	-	`sha256:f3d262d0659553a83768e42c9e50b738799f06f42bbc0e3e3b8a7aaf9b6128f9`  
		Last Modified: Tue, 25 Nov 2025 01:24:30 GMT  
		Size: 8.5 MB (8509943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fb23be0288bcef2db14d4e993681c71153043d7af08a52adb72dc9b53253f3c`  
		Last Modified: Tue, 25 Nov 2025 01:24:31 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:171e97d29fc5b891d0aeb90c44b3c8c30352d121fa8ea34718283b43629a1828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384151116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6fa4de0040e13d86afde40e0ed8dab57ca244372fb5d549755c39fbc99ffd3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 24 Nov 2025 22:40:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:40:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 24 Nov 2025 22:40:40 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:40:40 GMT
ENV LANG=C.UTF-8
# Mon, 24 Nov 2025 22:40:40 GMT
ENV JAVA_VERSION=26-ea+25
# Mon, 24 Nov 2025 22:40:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='34a09a42f38d04f223c2c3c3665e4638bcda263c69c38e8e363760be8ceeaffd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='33e9133fcee05a36df65b43ceea8dd2c16ff6fe9c0186acd0a697547c2bd7a42'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 24 Nov 2025 22:40:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14656e63ca309d8cfd09d01a9dbb3d1ea2d59a5efe7d40b9716f822e821385ab`  
		Last Modified: Tue, 18 Nov 2025 03:27:58 GMT  
		Size: 25.0 MB (25021011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9898fed0b4a62008cd3a65adf14beaff9f7a6dbe46176b901f31b3a21db4c6ab`  
		Last Modified: Tue, 18 Nov 2025 05:39:53 GMT  
		Size: 67.6 MB (67584762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af827b2e1d044a98ef36d605b5d1b13432f44b27f3ec942a74a70043a19e5877`  
		Last Modified: Mon, 24 Nov 2025 22:41:21 GMT  
		Size: 16.1 MB (16070882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6bfcd5e7a372e9690856138f5845f6e3cc2d6be82a3e5dea39f218c797bc14`  
		Last Modified: Tue, 25 Nov 2025 02:19:28 GMT  
		Size: 225.8 MB (225824229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:4aa6323dda32151739036137b22613b3a98f6bcc5c0ebc7f6c8e47175e5d0510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5dcac4c5ffa329eabef59e077a161f6f77286b4c9cb32ba75b98bd1cb75d61a`

```dockerfile
```

-	Layers:
	-	`sha256:575c98751d272d17fc26f17ff4f23025779302e2988b2c8d4f2ec68f80e334ca`  
		Last Modified: Tue, 25 Nov 2025 01:24:38 GMT  
		Size: 8.7 MB (8704733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08ce93a7f206d7db285f871cb33c7a6149b5db83629f16e488759044bbe72df7`  
		Last Modified: Tue, 25 Nov 2025 01:24:39 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
