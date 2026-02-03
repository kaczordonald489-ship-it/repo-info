## `clojure:temurin-21-tools-deps-1.12.4.1602-alpine`

```console
$ docker pull clojure@sha256:93480cf9e020ab0bb9416f54d60be0aa06aa4dc7dbb6dc8bff21ea8a837846ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1602-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:61940701c4aa53cac8063f5819ccac5b2f47dd46593bbd9fbd2ef0857bcc675f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208149348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bc8ae34a949d6efd7731b7be9bf03049d495af75517919d9e615449fb0d1e7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:11:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:11:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:11:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:11:08 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:11:08 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Wed, 28 Jan 2026 03:11:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 03:11:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:11:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:11:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:11:16 GMT
CMD ["jshell"]
# Wed, 28 Jan 2026 18:05:14 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:05:14 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:05:18 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 28 Jan 2026 18:05:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:05:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:05:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:05:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec9d6adc0e2666316744526b3e6b46024e14d211d934176cc82f480f88468a4`  
		Last Modified: Wed, 28 Jan 2026 03:11:33 GMT  
		Size: 21.1 MB (21115198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c077e7f5dd48795d611a90c0aeeabe7b837252b56c8406aac46577cdbcd6bd93`  
		Last Modified: Wed, 28 Jan 2026 03:11:36 GMT  
		Size: 158.1 MB (158102925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654728b92e1362ff81920038e72b4daebd48183a298e8e2a566bc42aad73110c`  
		Last Modified: Wed, 28 Jan 2026 03:11:32 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362be48a2be2658e4295069ddce05198f142098bc57a82f27d2da35698afdc81`  
		Last Modified: Wed, 28 Jan 2026 03:11:32 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d252e69a8240e1256ab13224ec4d7e165f53d9fdc899519aa36b8e48aa6b838`  
		Last Modified: Wed, 28 Jan 2026 18:05:28 GMT  
		Size: 25.1 MB (25122890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffa9fc74f78a5b97d3d3d49eeb99e1ed15c7ca62ea949fd39f60b7b61fab22b`  
		Last Modified: Wed, 28 Jan 2026 18:05:28 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66361119ee72406a34fe483382f85dc8e16c0b1532b9e2b91b9172f03503a16`  
		Last Modified: Wed, 28 Jan 2026 18:05:28 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:7fcf5f030772b62977933cf5b72e80ab0ece5d6ef8f52b782478fd3ff576dbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1316393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d833663ec55596a7066c8a5e5182b89ab5a9fd3524cc9401c25d44f2e2cb74`

```dockerfile
```

-	Layers:
	-	`sha256:41b1ba2ee1ecbecd9de75b9be3236195a9dfd8f0f0dc5a9bf0f09cebe18a8516`  
		Last Modified: Wed, 28 Jan 2026 18:05:28 GMT  
		Size: 1.3 MB (1300962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c76eaca6a4951284c672d1c60c1a3732a603fe422d0d576f291ca08945d4075c`  
		Last Modified: Wed, 28 Jan 2026 18:05:28 GMT  
		Size: 15.4 KB (15431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:81c461fe6aac6b4eb767c03b1615a3f51bde9d267c434827aa1f660a8c5aaebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.6 MB (206645986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a2c0c481cbd482ef0cf35085a493b80348363eb83fb21b279e01a5bba39e34`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 02:56:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:56:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 02:56:37 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 02:56:37 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Wed, 28 Jan 2026 02:56:45 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 02:56:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 02:56:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:56:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:47 GMT
CMD ["jshell"]
# Wed, 28 Jan 2026 18:04:47 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:04:47 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:04:50 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 28 Jan 2026 18:04:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:04:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:04:50 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:04:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d237401997b4e6d77e1a6cbf3006b196170369b2872d0a2fba9f845ce7cfeeb5`  
		Last Modified: Wed, 28 Jan 2026 02:57:03 GMT  
		Size: 21.2 MB (21166024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bf8a9ded26681fc49549c27c20edd4b88472a3ca476e9a7c4ebf9d58174315`  
		Last Modified: Wed, 28 Jan 2026 02:57:06 GMT  
		Size: 156.1 MB (156097479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9c000864d8ab5dc2884668139fc08c3b2e6cc3aaa69eacd03144943b90354f`  
		Last Modified: Wed, 28 Jan 2026 02:57:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e39acec808282ee08cd7b6292bf85d7b6775f69ca5e3bb0eb617e09e97bb94d`  
		Last Modified: Wed, 28 Jan 2026 02:57:02 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725150d481053e108d3392e8ae0cf8c2d0afca154aeeb1e3767387a5d176b92a`  
		Last Modified: Wed, 28 Jan 2026 18:05:00 GMT  
		Size: 25.2 MB (25239505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26e2a14500d4cc43b4dbc32672166400a24473f8715ae831d6a2fd6ce66bc6`  
		Last Modified: Wed, 28 Jan 2026 18:05:00 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa16eaefac1637dc48cdd775c0a252a41d0c4f38bc1333d67afeea978a741181`  
		Last Modified: Wed, 28 Jan 2026 18:05:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:185bba784b73c9af6201718a583e60643919ffe6f6d36e00930e8adc219860d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 MB (1466487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcba5a82cf4a4c82c9fdfe218280981ee82e7ff888401e156f4e5a5662a20863`

```dockerfile
```

-	Layers:
	-	`sha256:dd7a643c7b635f8c8d62d0ab721378cb293f6e3ad32664186493a3e426212304`  
		Last Modified: Wed, 28 Jan 2026 18:05:00 GMT  
		Size: 1.5 MB (1450964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca4a865ef5200646216905a6fee6a48eb230238a15855bd0dde650f53015d7e`  
		Last Modified: Wed, 28 Jan 2026 18:05:00 GMT  
		Size: 15.5 KB (15523 bytes)  
		MIME: application/vnd.in-toto+json
