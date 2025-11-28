## `openjdk:26-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:6366f3374c92eb98aa429b3181b3a55385b8951b00534f0c51f4bd8f5a998e38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:d06767f188d9d1d968d3be62aecba9828cb8289727234dbaadf33fd2450705d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260270619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e66e7726ac3c9eb30e4ada375ed26321c2c7657fe7d08c6807062a010dbee04`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Mon, 24 Nov 2025 22:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:40:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 24 Nov 2025 22:40:22 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:40:22 GMT
ENV LANG=C.UTF-8
# Mon, 24 Nov 2025 22:40:22 GMT
ENV JAVA_VERSION=26-ea+25
# Mon, 24 Nov 2025 22:40:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='34a09a42f38d04f223c2c3c3665e4638bcda263c69c38e8e363760be8ceeaffd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='33e9133fcee05a36df65b43ceea8dd2c16ff6fe9c0186acd0a697547c2bd7a42'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 24 Nov 2025 22:40:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdae031af776803c54bf3a5ccb1916357d1245b76ce38573f82ef158ba246e4c`  
		Last Modified: Mon, 24 Nov 2025 22:40:55 GMT  
		Size: 4.0 MB (4027343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189d76c3e7d624c8956a6b7ec6ac55a1504d9f8da566045ebfc6563f60bd7a83`  
		Last Modified: Tue, 25 Nov 2025 01:53:11 GMT  
		Size: 228.0 MB (228014827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ba07de2fc7dc97d468ea76ca919db0c7ecd85cc4f6ec1546fd8bf10937b893b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c02d9da943cdef9480d40053c8312973d35853d0f805d5c0e50aaf21c6c189`

```dockerfile
```

-	Layers:
	-	`sha256:d78e35fe85b6eb940f163a0bdf989f386dc0428cd1c750dd31c3329e91ee8cd1`  
		Last Modified: Tue, 25 Nov 2025 01:24:13 GMT  
		Size: 2.6 MB (2649789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d84dc24cecc716dfa073da08e41e8870dbc99ad532c74d1f58197b80d3df2e`  
		Last Modified: Tue, 25 Nov 2025 01:24:14 GMT  
		Size: 16.9 KB (16870 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e7974e14f162c8dff95b15fa48c0b4605d2df52b1dfbf7a93fcad4cb420baa6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257827831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8206d1e3001be747733b6e1652a8a5bb65afd3e26767d458933574a401eedd9b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Mon, 24 Nov 2025 22:40:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:40:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 24 Nov 2025 22:40:50 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:40:50 GMT
ENV LANG=C.UTF-8
# Mon, 24 Nov 2025 22:40:50 GMT
ENV JAVA_VERSION=26-ea+25
# Mon, 24 Nov 2025 22:40:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='34a09a42f38d04f223c2c3c3665e4638bcda263c69c38e8e363760be8ceeaffd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='33e9133fcee05a36df65b43ceea8dd2c16ff6fe9c0186acd0a697547c2bd7a42'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 24 Nov 2025 22:40:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f12e6861ba0d370b7b61311773877082c9c2417b0d00048588fabc4cad2156`  
		Last Modified: Mon, 24 Nov 2025 22:41:20 GMT  
		Size: 3.9 MB (3851397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd5bb0296b6909a2afb258969712bcbcdebe8ac49a071471b0197fc3256b684`  
		Last Modified: Tue, 25 Nov 2025 02:20:37 GMT  
		Size: 225.9 MB (225874227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f5d959a29c5bc9326ca6be4e4ac7365a5e22ed646d8a3c072010b221241d66bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98d9267cdfbf2f6310b0e95687e59e4fa87bf57f43811a3b885ebb21f5ca805`

```dockerfile
```

-	Layers:
	-	`sha256:ed623d25d2c99d1f99acf44621ac6fce89007dfd33158a2fd1a6fad75997bc68`  
		Last Modified: Tue, 25 Nov 2025 01:24:18 GMT  
		Size: 2.6 MB (2649423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:009bae76d7c77fc3ce03eb22dd4662a968fdc04790752012159011d67c211bb5`  
		Last Modified: Tue, 25 Nov 2025 01:24:19 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
