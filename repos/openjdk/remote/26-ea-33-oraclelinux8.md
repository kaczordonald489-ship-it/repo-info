## `openjdk:26-ea-33-oraclelinux8`

```console
$ docker pull openjdk@sha256:b0e0656e5f0443cc24f04e205ffc4fdd2a4ee59cad2479b6a7cd1b3ba51e4ebf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-33-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:f5398d8ea33f45a7aaa5d7ace3ba34f7cad082fa081aea571d90e2c352dab5c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294782978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2243fc6228ae9e56c9ce0321812a7295a54bd408c0263d73a27ff7e3416eb5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 26 Jan 2026 22:04:10 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 26 Jan 2026 22:04:10 GMT
CMD ["/bin/bash"]
# Fri, 30 Jan 2026 23:40:34 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 30 Jan 2026 23:40:48 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 30 Jan 2026 23:40:48 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:48 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:48 GMT
ENV JAVA_VERSION=26-ea+33
# Fri, 30 Jan 2026 23:40:48 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70f5c9ee868f124c508277177dfd78acddb8ada1f704dc8be2b2cdd99836131c`  
		Last Modified: Mon, 26 Jan 2026 22:04:22 GMT  
		Size: 51.5 MB (51467065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b154aaa0d54736e86daf2782771e3ceda77d2c3da0ef30d600860f3087435f89`  
		Last Modified: Fri, 30 Jan 2026 23:41:09 GMT  
		Size: 15.0 MB (14991443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f09f282264395e038fd83fee51ec3a7f962034bf76d831c15cdb04a9ab2a461`  
		Last Modified: Fri, 30 Jan 2026 23:41:14 GMT  
		Size: 228.3 MB (228324470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:fff0d92f65288febb0dd63971af2a2b43f3097ba43e44ca945f38eb5258f1914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8005e535a2b5e447365391b88a0d8ce11469b5d26c38cc43d18991ab4ada946c`

```dockerfile
```

-	Layers:
	-	`sha256:c8d88b600d4349cc6da04fd4ee9ba875f0c06af5add4b57152097c9aead53344`  
		Last Modified: Fri, 30 Jan 2026 23:41:09 GMT  
		Size: 2.4 MB (2448688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b7fa3a838e92e4b7f094bb1bb284fa0ac73f3a78971c5aa3ef0038996b821eb`  
		Last Modified: Fri, 30 Jan 2026 23:41:09 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-33-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fc23b28d6ca00cbd849fe9c91c4b997fef7b72ed7a8faaab4e330793b6323de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292144100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4989b5e5cc5e6806c6733890b9e2b17a5a8819978d557fdad5197987ae6a55c9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 26 Jan 2026 22:07:11 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 26 Jan 2026 22:07:11 GMT
CMD ["/bin/bash"]
# Fri, 30 Jan 2026 23:39:58 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 30 Jan 2026 23:40:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 30 Jan 2026 23:40:14 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:14 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:14 GMT
ENV JAVA_VERSION=26-ea+33
# Fri, 30 Jan 2026 23:40:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3e76a047bd66be5e3e8818d893725279bf9a5b8a583db4b258f0d16df8850a42`  
		Last Modified: Mon, 26 Jan 2026 22:07:23 GMT  
		Size: 50.2 MB (50197120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca19fb09e0f199895dc8cfaaf7fc857b0f4e2cbe76de34edaf49454dac77654`  
		Last Modified: Fri, 30 Jan 2026 23:40:35 GMT  
		Size: 15.7 MB (15687673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f34051cde834a55da4f1393c5238f3ce80d9f149a785c6b1e89fc196e8cfc5`  
		Last Modified: Fri, 30 Jan 2026 23:40:40 GMT  
		Size: 226.3 MB (226259307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:7f86b4051b21370d5e1f44b704b1a074b0f6d1ee1c4868cdaf70dcc76fd26376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64e500bfcc5a22ef952677099dfcc0f455535b8685378d3f231a2d8014e96f1`

```dockerfile
```

-	Layers:
	-	`sha256:d14d4ac6c9ee3c0ff1b0e2d0a875b5bb3041a27e9663fd75948f9dcf54c04632`  
		Last Modified: Fri, 30 Jan 2026 23:40:35 GMT  
		Size: 2.4 MB (2447498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf050e06b9a9ad9d0df8d6ff8461acdf3ce23060c6412457e1cf2acede8d3cab`  
		Last Modified: Fri, 30 Jan 2026 23:40:35 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
