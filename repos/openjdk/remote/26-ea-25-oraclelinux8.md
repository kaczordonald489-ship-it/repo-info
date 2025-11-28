## `openjdk:26-ea-25-oraclelinux8`

```console
$ docker pull openjdk@sha256:ee9ce2b9f5821450d48d9374e54211eeb69e5fda058066a586bf25486fa1ec2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-25-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:937353e6699f5b1d4b8ab95a9cc7a840c91c38875bda3d172ed33edb641bbd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294682429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42fbd95b3edb68ecfc797e924082c9cf3ad105f013d7544fcd8e1f7023aaf4c8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Nov 2025 23:50:37 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 25 Nov 2025 23:50:37 GMT
CMD ["/bin/bash"]
# Wed, 26 Nov 2025 00:10:31 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 26 Nov 2025 00:10:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Wed, 26 Nov 2025 00:10:40 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Nov 2025 00:10:40 GMT
ENV LANG=C.UTF-8
# Wed, 26 Nov 2025 00:10:40 GMT
ENV JAVA_VERSION=26-ea+25
# Wed, 26 Nov 2025 00:10:40 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='34a09a42f38d04f223c2c3c3665e4638bcda263c69c38e8e363760be8ceeaffd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='33e9133fcee05a36df65b43ceea8dd2c16ff6fe9c0186acd0a697547c2bd7a42'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 26 Nov 2025 00:10:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b436d89f13c92f9703618820d992b4e1f2b38ba243024b251c81a610f04c67b1`  
		Last Modified: Tue, 25 Nov 2025 23:51:01 GMT  
		Size: 51.4 MB (51378078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7b6176c8d2abedc29877c99714b84dfbc9ae9dde46a5e38924ba5ffa3e960c`  
		Last Modified: Wed, 26 Nov 2025 00:11:39 GMT  
		Size: 15.0 MB (14999271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005a473d700de3ee5e97ad0e80119c5a0f4d12a46dc9d9cd60bd4989ee74914c`  
		Last Modified: Wed, 26 Nov 2025 01:58:34 GMT  
		Size: 228.3 MB (228305080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-25-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:c84f68b07d4190e67da2175e6b2a9aa16de6dbfa0277c2e98e2901bb39a32b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c7294bed9717724f74bf9bf4c389cc53343440afc352a32f91b708dc015b1c`

```dockerfile
```

-	Layers:
	-	`sha256:34a04a88a72458071f047b255bdcd0ad2f606959a65ab224facd78c24ed469c6`  
		Last Modified: Wed, 26 Nov 2025 01:23:24 GMT  
		Size: 2.4 MB (2448013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade2441449bcc9b44f5571b0eb303481d78e5d5199cf028b9bfb0eff4f65bca4`  
		Last Modified: Wed, 26 Nov 2025 01:23:25 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-25-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4e9dd9d8e87e2a896f800d3d041fe3f764d46a525a28507e91c78882d7175912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291970964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf71d92d3a5e4d88d6e799ab4c46d51384944a9459c3f6446299e76d3ecd525`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Nov 2025 23:37:54 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 25 Nov 2025 23:37:54 GMT
CMD ["/bin/bash"]
# Tue, 25 Nov 2025 23:52:26 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 25 Nov 2025 23:52:36 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 25 Nov 2025 23:52:36 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Nov 2025 23:52:36 GMT
ENV LANG=C.UTF-8
# Tue, 25 Nov 2025 23:52:36 GMT
ENV JAVA_VERSION=26-ea+25
# Tue, 25 Nov 2025 23:52:36 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='34a09a42f38d04f223c2c3c3665e4638bcda263c69c38e8e363760be8ceeaffd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='33e9133fcee05a36df65b43ceea8dd2c16ff6fe9c0186acd0a697547c2bd7a42'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 25 Nov 2025 23:52:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:674388ef21c06396c4d40407ba2af1c3a42c30a5cb162fd4355950be7600edf7`  
		Last Modified: Tue, 25 Nov 2025 23:38:20 GMT  
		Size: 50.1 MB (50103076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ebc4ac017a2ee9edd01b3a38686678bea037bba65265b046387588dc249748`  
		Last Modified: Tue, 25 Nov 2025 23:53:09 GMT  
		Size: 15.7 MB (15691578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519abd1d69554bbe95f7ad6c537930e08ee21506eb923b8de8219b080471bc87`  
		Last Modified: Wed, 26 Nov 2025 00:12:43 GMT  
		Size: 226.2 MB (226176310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-25-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:83533cf917f9f09b28b48d1e22dc4eebe8b53b04a34cfb717ce69c7255705b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a790a4fc1bd693950826916a7076c53ef5a501dc048d9a6df85cb08c0c0a280c`

```dockerfile
```

-	Layers:
	-	`sha256:b6373c71fb947e724845b12312e9c4133b9d9e4021f19504b9ae2c6024195799`  
		Last Modified: Wed, 26 Nov 2025 01:23:29 GMT  
		Size: 2.4 MB (2446823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9becab9e8e135c3cfa68bc05a1f35183fc6b1d28c1e8ee8efb05edbac6f2b28e`  
		Last Modified: Wed, 26 Nov 2025 01:23:30 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
