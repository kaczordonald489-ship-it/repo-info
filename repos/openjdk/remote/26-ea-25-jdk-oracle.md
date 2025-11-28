## `openjdk:26-ea-25-jdk-oracle`

```console
$ docker pull openjdk@sha256:761277f3c97038d24f1c38f9a948c5b5d5dfe4e5062af2a9374ec4babc94f5d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-25-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:d7f8e7d6ced9e379cc58ce4b25968e46c124962d6d492db98ea5a9322481ce6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315418147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f339c65ef7c59b42314e9fefb8c0093633f6e89e894bf03d8fae9b18623e8e24`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 22:39:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 24 Nov 2025 22:39:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 24 Nov 2025 22:39:27 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:27 GMT
ENV LANG=C.UTF-8
# Mon, 24 Nov 2025 22:39:27 GMT
ENV JAVA_VERSION=26-ea+25
# Mon, 24 Nov 2025 22:39:27 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='34a09a42f38d04f223c2c3c3665e4638bcda263c69c38e8e363760be8ceeaffd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='33e9133fcee05a36df65b43ceea8dd2c16ff6fe9c0186acd0a697547c2bd7a42'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 24 Nov 2025 22:39:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf608a82e295979461fe541a79070109962c5869f1fe35083b1fe2bd71a153d`  
		Last Modified: Mon, 24 Nov 2025 22:40:23 GMT  
		Size: 38.1 MB (38078851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f0d45bffe88cdd52c3bd60e1dda18a2873756e0bebe641183fc84e4ad6ee8d`  
		Last Modified: Mon, 24 Nov 2025 23:14:18 GMT  
		Size: 227.8 MB (227842791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-25-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:6e2789c9e7fd2a60924e6bbabd6ca1ef8e82f7f57b7eac50a40813f827c08184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3654201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1debfe8ee451fb593385bdb127bbaaa6266b04ac401c2a432339d662ac5930d`

```dockerfile
```

-	Layers:
	-	`sha256:92425cc5a6392d0aebc9bcc54d6e2fbdc1a83cba831b60f2902a71c8acba22ab`  
		Last Modified: Tue, 25 Nov 2025 01:23:24 GMT  
		Size: 3.6 MB (3636362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f78e8773813ee6399dba81bf636ca87a731263b93f59d30a0a5b33200f4530`  
		Last Modified: Tue, 25 Nov 2025 01:23:25 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-25-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3e24e6869416124d2a55cb96f6e32542136c7bc546089f410b86131a46636440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 MB (312281189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d437f0f138c9b2faf99211a929c07dcb00392f2f621ee1c27690b15116e7d5b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 22:39:31 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 24 Nov 2025 22:39:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 24 Nov 2025 22:39:58 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:58 GMT
ENV LANG=C.UTF-8
# Mon, 24 Nov 2025 22:39:58 GMT
ENV JAVA_VERSION=26-ea+25
# Mon, 24 Nov 2025 22:39:58 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='34a09a42f38d04f223c2c3c3665e4638bcda263c69c38e8e363760be8ceeaffd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='33e9133fcee05a36df65b43ceea8dd2c16ff6fe9c0186acd0a697547c2bd7a42'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 24 Nov 2025 22:39:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fdc07cdc69e066e027a8a95055506d4df85a5edd717dea8f572fe4a3c54407`  
		Last Modified: Mon, 24 Nov 2025 22:40:53 GMT  
		Size: 38.5 MB (38494079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd7f442426fecfe67511da3a4ace0a8faff14ce244eeb3d153be1d005eaec81`  
		Last Modified: Mon, 24 Nov 2025 23:29:17 GMT  
		Size: 225.7 MB (225700209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-25-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:32c63e0718f78e1f2fa5083420687231cfb71a09f499a05a090a4c7af48a97dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3652105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a696c90de054319fdd19d504a5404ff308be4e61ab19f9e442c8f64a3324983`

```dockerfile
```

-	Layers:
	-	`sha256:e7ffe5b99c26bb0dbf371c60805e5b1a578b07ac0b7a65d138b8393f3173b47e`  
		Last Modified: Tue, 25 Nov 2025 01:23:58 GMT  
		Size: 3.6 MB (3634052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a56227f0581e64ec4e1fda5a13f7b0860b00fae711005874a9dd1da5c9058d70`  
		Last Modified: Tue, 25 Nov 2025 01:23:58 GMT  
		Size: 18.1 KB (18053 bytes)  
		MIME: application/vnd.in-toto+json
