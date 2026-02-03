## `eclipse-temurin:25-jdk-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:9c9f665be0946f07fd8e6ae99e781d67082b24c630755be54d5b4cb4f77b684b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1a9b972ad5d62396aa43fb650c93f0cb5c8e02d350889c8d233ac47f11cf8f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109098434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98f875fd5943005caf8199de665d399d213c298986a18622b05b95680f273b2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:13:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:13:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:13:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:13:24 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:13:24 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 28 Jan 2026 03:13:35 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 28 Jan 2026 03:13:37 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:13:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:13:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:13:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adb025e1700fa1759332a67655b21cf08b454fa568bbf4dca947f651bce86f1`  
		Last Modified: Wed, 28 Jan 2026 03:13:53 GMT  
		Size: 14.2 MB (14172563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78568e40a591b246c080976f6172390a62d2e3943e4b63a1520caf4069730b37`  
		Last Modified: Wed, 28 Jan 2026 03:13:54 GMT  
		Size: 91.3 MB (91279719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a31c774531abb9d4f74cec728ecfa29df4d2cdcd4d208a4e24cd091fffc59e`  
		Last Modified: Wed, 28 Jan 2026 03:13:52 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65ca921b8424f0fb196d924064875c5cbd6bb1680e1b666631a1cd11ff4505c`  
		Last Modified: Wed, 28 Jan 2026 03:13:52 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:da49cddef0255cf983f48ecd2d2a0780904d94ca0c407d533d6e426e2060620d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **967.1 KB (967122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d70d1932a37cdc2741a76caf1e777add884962136e113f5a866c27457b5d58b`

```dockerfile
```

-	Layers:
	-	`sha256:8b49117762b41609e855b59d61d70bd8b27e3ac0c1e0b85d7b71ed698afa080b`  
		Last Modified: Wed, 28 Jan 2026 03:13:52 GMT  
		Size: 946.6 KB (946603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4f4be5f3f3edc182ed71d5d3bae52868f00dbfb6554cd6bbdd570b486dc4f8b`  
		Last Modified: Wed, 28 Jan 2026 03:13:52 GMT  
		Size: 20.5 KB (20519 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-alpine-3.21` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:bc9d5090f32a395eede1ff4c005cb267d3827c4f9a6fd247a2a86b8cdcf56617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108455400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd654a0fe1a89479ef4763f85e1f37ba2e3ab83dbec5c0a8fdfa0ca258fda0e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:00:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:00:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:00:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:00:30 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:00:30 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 28 Jan 2026 03:00:40 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 28 Jan 2026 03:00:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:00:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:00:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:00:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4745c2ec43805d21f7b5c46152b01f77f500c97377e21d6db29e9bc98b16b1`  
		Last Modified: Wed, 28 Jan 2026 03:00:57 GMT  
		Size: 14.3 MB (14269613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0c8e5d06ed9c384bf53c558700c8744c710578db3dd10af4d016e919f17694`  
		Last Modified: Wed, 28 Jan 2026 03:00:59 GMT  
		Size: 90.2 MB (90190496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e1670c839d6a7a1a0933b5f2d31c0132b6201529bfadcd75f5817f6cf6fcde`  
		Last Modified: Wed, 28 Jan 2026 03:00:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7b3c27e03d5640ed819b2bd17fc8bcf07d4e3dbe3f68c58513bdac1117ccfc`  
		Last Modified: Wed, 28 Jan 2026 03:00:46 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:89dbbd4456325335f2d31622d2edb2e5a3712b322b2a2827e2cb5ffb2e59c5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1117243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0374ee180b98bdd27e7a16af237e4147e9bf2b40db5e4af09d64bb45d97c88be`

```dockerfile
```

-	Layers:
	-	`sha256:55e0f04caa7a4efcf5bdb59b83b5c3c50fdaae8dc1a3ca253a68a931e2a8f528`  
		Last Modified: Wed, 28 Jan 2026 03:00:56 GMT  
		Size: 1.1 MB (1096602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffedd10fda223957b7539b4a28d7338dcb0a18f2e1ecb4f98ee0c9b36be11d19`  
		Last Modified: Wed, 28 Jan 2026 03:01:06 GMT  
		Size: 20.6 KB (20641 bytes)  
		MIME: application/vnd.in-toto+json
