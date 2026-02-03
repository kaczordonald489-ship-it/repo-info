## `openjdk:27-ea-7-oracle`

```console
$ docker pull openjdk@sha256:94290770a42479059c592fe8ff484b10910baf27ced2cf04eb1e2b2d31f341a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-7-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:a581c650b5edf2d035bf5a6a87d94a2fb9b03cbdbdd9c82713b2db97d9146e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313848043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c77c6cde56eb7e35bbf27bd2baeb81c2025d26400cfecbfb09de5000c76409`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:12:28 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:12:50 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 31 Jan 2026 00:12:50 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 31 Jan 2026 00:12:50 GMT
ENV LANG=C.UTF-8
# Sat, 31 Jan 2026 00:12:50 GMT
ENV JAVA_VERSION=27-ea+7
# Sat, 31 Jan 2026 00:12:50 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 31 Jan 2026 00:12:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d69407aa64a6860c247aa0265f83fc435733f0785c7ef7c35a6608bed0b6b49`  
		Last Modified: Sat, 31 Jan 2026 00:13:12 GMT  
		Size: 38.3 MB (38297759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7462813dde3aab69e35961a87dedca9822934981578e263edfd2be0b94367de8`  
		Last Modified: Sat, 31 Jan 2026 00:13:17 GMT  
		Size: 228.2 MB (228236476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-7-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:d4474c220741e3a2184a28012c6ad8daa46db3454c609fcd58d13fbb02e3dbe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36bf298b63d2dc73cbf5fca4502f6ac0373b094a32d952288d0eca03390659b`

```dockerfile
```

-	Layers:
	-	`sha256:b328ee88b9b9f7cf875e33221412347f3d3180c2c635f17835df93bf3def7f78`  
		Last Modified: Sat, 31 Jan 2026 00:13:11 GMT  
		Size: 3.7 MB (3654755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8abd46a5a8fdcbd8d6d12cd1a43504f3bbf80898c1db508b02da559d659f451a`  
		Last Modified: Sat, 31 Jan 2026 00:13:10 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-7-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fb8d837f7913f9f5885bd228cafb0179fb665133cbf229fb0b8aa2cea47ed209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310766563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e45f481b9646392c304203cb1609232e20a0ac2f83929ded0d6e9f464beb556`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:12:34 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:12:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 31 Jan 2026 00:12:44 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 31 Jan 2026 00:12:44 GMT
ENV LANG=C.UTF-8
# Sat, 31 Jan 2026 00:12:44 GMT
ENV JAVA_VERSION=27-ea+7
# Sat, 31 Jan 2026 00:12:44 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 31 Jan 2026 00:12:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b344e939556ac85f80437fec0c5974715c9884ffb1d433d36cd7427511c50e`  
		Last Modified: Sat, 31 Jan 2026 00:13:08 GMT  
		Size: 38.7 MB (38693924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b0d3bbbbd65f0361be1fb1522f91d7209a344289b7ad16a8046ca14dc1526b`  
		Last Modified: Sat, 31 Jan 2026 00:13:11 GMT  
		Size: 226.2 MB (226170998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-7-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:81e0e39c8df834986d662b764bf069f2e22ac2f455a57a37c5e07e962a19c9d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dffff593f23fffa2174d443fdb628ca3e2cff574b9ff78eb671f96e4f3fcea2f`

```dockerfile
```

-	Layers:
	-	`sha256:282943a27e963d76a4c185bd6830f484e12863afe0ca48830b859ad0927c9634`  
		Last Modified: Sat, 31 Jan 2026 00:13:06 GMT  
		Size: 3.7 MB (3652445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e70c94fd07de9acd091504eab0eb87568676c0c7cb6bd40eaec3fbd60883fbd9`  
		Last Modified: Sat, 31 Jan 2026 00:13:06 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json
