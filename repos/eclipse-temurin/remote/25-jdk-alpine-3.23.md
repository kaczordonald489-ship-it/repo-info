## `eclipse-temurin:25-jdk-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:39a68e9e668d660d97465c7059171be0fee6e900f768c729f11f59e2ea6850d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25-jdk-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:af8a39b2850fd0d59c4070cc7ad8233ad23a833bac892636ab068b8df5bef38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109451895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f1d681f2e18d429e013a512412c00201de8722f37ce3c13b89c79e491f6e8e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:14:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:14:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:14:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:14:01 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:14:01 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 28 Jan 2026 03:14:13 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 28 Jan 2026 03:14:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:14:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:14:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:14:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b3071f8dda2c9887c8ab035661134d359c2e8c5e830638ab7b49698a030580`  
		Last Modified: Wed, 28 Jan 2026 03:14:29 GMT  
		Size: 14.3 MB (14303803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d73955785c7cb41d752474fc886a4da7c0a8b1aec825334eb75c818a08db765`  
		Last Modified: Wed, 28 Jan 2026 03:14:31 GMT  
		Size: 91.3 MB (91283861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb462d63230065bc153d5a367590bdac34ee4b048df7fecb645dd3398523fab`  
		Last Modified: Wed, 28 Jan 2026 03:14:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a4c857b97aad7ff0a745a4aa2d2a627b26c1f32231465d6a9a2afb941d3471`  
		Last Modified: Wed, 28 Jan 2026 03:14:28 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:43cc569867143b01c7b031ae414defd3985add47cc3f003cb44e4952be407eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **970.4 KB (970449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18f7f030a7eddaccb7a5cbd30d7d5c201135a96707c5315321c62e1cf01e396`

```dockerfile
```

-	Layers:
	-	`sha256:ab06e9f0c60043c0c99505e9d5ddbedbc1a6dd12db3b859e5f96a639baf7c05b`  
		Last Modified: Wed, 28 Jan 2026 03:14:28 GMT  
		Size: 949.9 KB (949930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e601f32ddcf9098f40c030801e43c28d29417886637c2b302574faed29678b65`  
		Last Modified: Wed, 28 Jan 2026 03:14:28 GMT  
		Size: 20.5 KB (20519 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-alpine-3.23` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:a70da129daed17a5c5245b9067167f8c4b992f3fef18119ab7cf8b7c31b0e635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108767580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b24e36213452ccc3b8cc9580b2dc1375bc7b17fb94eb8ad70267477ed7ef9a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:01:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:01:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:01:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:01:35 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:01:35 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 28 Jan 2026 03:01:42 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 28 Jan 2026 03:01:44 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:01:44 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:01:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:01:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4476ae2c4d993302d4b997814b39c54da97513a5487fff3e94a5d574d1a09f`  
		Last Modified: Wed, 28 Jan 2026 03:01:59 GMT  
		Size: 14.4 MB (14373013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1a65717c4b03d5c4a8f96caf0dae59a007f13e3c20c4528bbdc1fc798a218e`  
		Last Modified: Wed, 28 Jan 2026 03:02:00 GMT  
		Size: 90.2 MB (90195065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47956e68d96e58f8ea32c54e85540c7abc8aba80c08331b613a2937cecefb03`  
		Last Modified: Wed, 28 Jan 2026 03:01:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760c81b1664bdc4dd24b79008869e8711ca0f9c5e55265e85aa754cb4ad75c3b`  
		Last Modified: Wed, 28 Jan 2026 03:01:47 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4760779b71ef6ab4039446f9172a2e122fac05007f674223f0706a7d755b0a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1119920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e43af5cdbc33c07f43ac7556e7bad8a79c05febc0a53e39f463d3e7760c9c8c`

```dockerfile
```

-	Layers:
	-	`sha256:829dabdd14b8adab5217f9173c6f1248cf88f42d1aa2d80c245652ba86832d22`  
		Last Modified: Wed, 28 Jan 2026 03:01:58 GMT  
		Size: 1.1 MB (1099279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9179a1648ed98760490abac9d11d9aa728806e23968f24dd1ccf876c9362150c`  
		Last Modified: Wed, 28 Jan 2026 03:01:58 GMT  
		Size: 20.6 KB (20641 bytes)  
		MIME: application/vnd.in-toto+json
