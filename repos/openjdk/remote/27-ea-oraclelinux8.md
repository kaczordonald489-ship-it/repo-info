## `openjdk:27-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:7987ddc55116e1d561ab78b83e597ac37184cd9bf0b42dd32b069b982e685c16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:27c40448e5c91dfafd2d287de0410890b9f990c44fa40d07c96ee030525deb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.2 MB (295150340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b75c39a63c86019c630f980da8adc52f3baef90a742512ad67d9317ecc3ab9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 26 Jan 2026 22:04:10 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 26 Jan 2026 22:04:10 GMT
CMD ["/bin/bash"]
# Fri, 30 Jan 2026 23:40:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 30 Jan 2026 23:40:53 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 30 Jan 2026 23:40:53 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:53 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:53 GMT
ENV JAVA_VERSION=27-ea+7
# Fri, 30 Jan 2026 23:40:53 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70f5c9ee868f124c508277177dfd78acddb8ada1f704dc8be2b2cdd99836131c`  
		Last Modified: Mon, 26 Jan 2026 22:04:22 GMT  
		Size: 51.5 MB (51467065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad9da4cf8a7b291175879ad383fd24302f057a02a58549e6f12acf53504cc08`  
		Last Modified: Fri, 30 Jan 2026 23:41:14 GMT  
		Size: 15.0 MB (14991127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4aac713ea0201301bbe9c8d8a695018844c56463b03ed4eeb8de4b6b3b8835`  
		Last Modified: Fri, 30 Jan 2026 23:41:18 GMT  
		Size: 228.7 MB (228692148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:52793d85903da86255a917c7d335b2af1c0b5a3432286b3e3db1161b0d194a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e3a44b43aecab047d44282074ab643e8b441488e23f6a26ae4320cac88ab4f`

```dockerfile
```

-	Layers:
	-	`sha256:85fb28c8042b8ea682fb068ae69154455787866d07bdcfba08760580f0d9ea35`  
		Last Modified: Fri, 30 Jan 2026 23:41:13 GMT  
		Size: 2.4 MB (2448060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ffe662a250bc89ef5f512c76fffc4449e27cb3a06549757a8073d50e891687f`  
		Last Modified: Fri, 30 Jan 2026 23:41:13 GMT  
		Size: 15.3 KB (15326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3edef8265551456fd5318233315b68e4acda9cfd46a3758fed230a8a943a756a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292529565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d835c593f609b5965fa83748bb35adbb7db10fb90055463d94bed539871aa39b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 26 Jan 2026 22:07:11 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 26 Jan 2026 22:07:11 GMT
CMD ["/bin/bash"]
# Fri, 30 Jan 2026 23:40:07 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 30 Jan 2026 23:40:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 30 Jan 2026 23:40:20 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:20 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:20 GMT
ENV JAVA_VERSION=27-ea+7
# Fri, 30 Jan 2026 23:40:20 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3e76a047bd66be5e3e8818d893725279bf9a5b8a583db4b258f0d16df8850a42`  
		Last Modified: Mon, 26 Jan 2026 22:07:23 GMT  
		Size: 50.2 MB (50197120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f65e2bd5bdc28f45fa9203a847d612f45ec5f4d17b7eb302b615f2c0d87b1f`  
		Last Modified: Fri, 30 Jan 2026 23:40:42 GMT  
		Size: 15.7 MB (15687659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900a2d3f7773fe62e106b6568ee02221f1f87c59b2ab39a1313ff8bce15f739b`  
		Last Modified: Fri, 30 Jan 2026 23:40:46 GMT  
		Size: 226.6 MB (226644786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:084d1514000d3d4d590c60d5cd6a817b9804eb1d6065d63543215a9a8dc2da77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f923160bc01e9d6c24ec26090a1ba63564c063ba409615a2e1347517741ebb1a`

```dockerfile
```

-	Layers:
	-	`sha256:c0ab2b28c1f37539e7c2f672446712e891175ea3b7758fdbc184d5c48b044452`  
		Last Modified: Fri, 30 Jan 2026 23:40:42 GMT  
		Size: 2.4 MB (2446870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7a72ccda92ed5e640af4c619c163eb8600d35116ac885d5a8f0f15cf8c772d`  
		Last Modified: Fri, 30 Jan 2026 23:40:42 GMT  
		Size: 15.4 KB (15445 bytes)  
		MIME: application/vnd.in-toto+json
