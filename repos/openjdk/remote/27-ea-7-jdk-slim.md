## `openjdk:27-ea-7-jdk-slim`

```console
$ docker pull openjdk@sha256:71b31d18f958a9d99e2fb4fd7b8be74846690f257c4180dc68c9b226b723a997
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-7-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:3b156a025256bfc7114392dfb90c1f38511b333592a10a13712d7576affc0878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.6 MB (260559934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7121a0acd535b6423643170515427707cf7a4aa5aab72f2416ed4796446639`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:50:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 03 Feb 2026 02:50:29 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:50:29 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:50:29 GMT
ENV JAVA_VERSION=27-ea+7
# Tue, 03 Feb 2026 02:50:29 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 03 Feb 2026 02:50:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4d8fde36bca18731512372edd74ad8d29046e1b61adf27de2ed7b9f6423780`  
		Last Modified: Tue, 03 Feb 2026 02:50:49 GMT  
		Size: 2.4 MB (2371009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b52157b33c201fcf3f0e868836b965f1af3ba328bd54e7cc3a59406c0de8298`  
		Last Modified: Tue, 03 Feb 2026 02:50:54 GMT  
		Size: 228.4 MB (228410329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-7-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:368f2bb2d6bb8b048a29d56f1cb2580e760d7dd1df029116dc075b117e152e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9fbf8f97a3d224752f4693f81283c6a89c9942d261cbb59fda0fdbc841785c`

```dockerfile
```

-	Layers:
	-	`sha256:4b041f650c6ae96c48b2f1f0b4a478e6a42e5af3bb99bc4384228b2744f2b3e2`  
		Last Modified: Tue, 03 Feb 2026 02:50:49 GMT  
		Size: 2.3 MB (2278218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a74fad9f922ed3832c62013617b548b74e82ec904eebb3326ce927fd771db0a`  
		Last Modified: Tue, 03 Feb 2026 02:50:49 GMT  
		Size: 18.1 KB (18088 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-7-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a2e46a33b9facf7a37734919227f045e13aa98cc40f1eea6992924d316fe943a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258796408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70dbff37ba3d8d1a5977c7ac11ba5cf0fb4172327adf09902a3dd3469d98c48f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:52:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:53:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 03 Feb 2026 02:53:10 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:53:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:53:10 GMT
ENV JAVA_VERSION=27-ea+7
# Tue, 03 Feb 2026 02:53:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 03 Feb 2026 02:53:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07207917b0e83ff47ab13f37ba84c0dbfaab3bdef8b9557699b05102ae34db0a`  
		Last Modified: Tue, 03 Feb 2026 02:53:30 GMT  
		Size: 2.3 MB (2314434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373f9acf5ab79e5dd7e4fc5f5110a8352c8f3a41cda24ff47075ae3a866829da`  
		Last Modified: Tue, 03 Feb 2026 02:53:35 GMT  
		Size: 226.3 MB (226341910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-7-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:59b8eb85d3c05f71d80e61bcdf6983e2e6993082c0283432950930f7cf65e645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc2f4210dd846f1f450bb778e7e23574f4f33df6e7b7e2dbc5e39243bbc725c`

```dockerfile
```

-	Layers:
	-	`sha256:21f3519460a981864617942e106ded99c6a9d69f63bdc6882b5a84661081f088`  
		Last Modified: Tue, 03 Feb 2026 02:53:30 GMT  
		Size: 2.3 MB (2277904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb822a3dae0d34aec5a5940d5fa2f5424b2dbeae6c8d8fe1ccc5c41db74a69bb`  
		Last Modified: Tue, 03 Feb 2026 02:53:30 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
