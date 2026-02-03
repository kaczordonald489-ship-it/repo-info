## `openjdk:26-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:46ff672c8cbd535c1080e3ce4c7a6cd60689b2142bdf9ed149cced743b7ca480
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:b2e2309cba1701086e81177bfb0a7e1a333787d6a84a2d796cff7b48204829ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313480294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9066ae383c3c30fca58e78b9f176b4192f7676bb19464896a7dbe2ef422e2f4`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:12:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:12:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 31 Jan 2026 00:12:37 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 31 Jan 2026 00:12:37 GMT
ENV LANG=C.UTF-8
# Sat, 31 Jan 2026 00:12:37 GMT
ENV JAVA_VERSION=26-ea+33
# Sat, 31 Jan 2026 00:12:37 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 31 Jan 2026 00:12:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e17583089494c0004a8a6d29cd8dee1e937c78a90941033e785c35ff443798`  
		Last Modified: Sat, 31 Jan 2026 00:13:01 GMT  
		Size: 38.3 MB (38297911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa61030c8b1f5865b4d106632166341d13875e933c8e8a8eedb7840a31946d53`  
		Last Modified: Sat, 31 Jan 2026 00:13:06 GMT  
		Size: 227.9 MB (227868575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:11196353163042c105d14b1d7ac16151dc010b0b49077b6f01ac858fe570356f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c258b3a17a0412944a1873a1ccf2c1e41a03126c2ea0ee3e08bbd42300586a6`

```dockerfile
```

-	Layers:
	-	`sha256:f1332ed3e8fee039e8bb00e12ca04caede9e3bc2e8438018a1739d03b07d5fb5`  
		Last Modified: Sat, 31 Jan 2026 00:13:00 GMT  
		Size: 3.7 MB (3655391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9168f1633642457f2e87bb274e9a8e92c5759e8d0ff47f42fb996858ed3473c9`  
		Last Modified: Sat, 31 Jan 2026 00:12:59 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f4baeadc5367b5a5fe3778f6dd876c3427b6ca7ae4c3e7a691036d035e898864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310379910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95daa2ab27f8ad25a3baf7336542c7048dd09b1b5f4725a55d02bb4235d0362f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:12:30 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:12:41 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 31 Jan 2026 00:12:41 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 31 Jan 2026 00:12:41 GMT
ENV LANG=C.UTF-8
# Sat, 31 Jan 2026 00:12:41 GMT
ENV JAVA_VERSION=26-ea+33
# Sat, 31 Jan 2026 00:12:41 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 31 Jan 2026 00:12:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9235c10a46cdf0d1a0979d60b325ded20728f66c0dd28f7ee80374f3fee9c32`  
		Last Modified: Sat, 31 Jan 2026 00:13:04 GMT  
		Size: 38.7 MB (38693764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef027fbf950aadf2db1fa014f00ceb33469ef8a4817392c542a47e4e945575aa`  
		Last Modified: Sat, 31 Jan 2026 00:13:07 GMT  
		Size: 225.8 MB (225784505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:af8071d64d439669c022671449ea357a75f47e03e10c28b1394101d4eb03a829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee5423a82af3b5f492fd987d2b3c56a15f553df7fe8644f078d2e5d99d12914`

```dockerfile
```

-	Layers:
	-	`sha256:2eb23639ed01ae364f976645f7bec05b8af2eb0639ec501c62c0be581732ed22`  
		Last Modified: Sat, 31 Jan 2026 00:13:02 GMT  
		Size: 3.7 MB (3653081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10c995dcb08e45c352e5382e75be2cd2a84dd3b992f11d20f4751c979b15d875`  
		Last Modified: Sat, 31 Jan 2026 00:13:02 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json
