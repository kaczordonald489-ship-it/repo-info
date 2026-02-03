## `eclipse-temurin:17-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:e4b1ffa698e42a55774eed8deab5ff8aa1ff77fe2e864156b1451e446e72a2c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:93e2eca30a9116cfef291b07655fe5ebf158651553d329a24876c35e87e5f342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168347112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cdc391eb995e34c3702082db7ed18bedc47d35cab182da5499527ded6c32eab`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:05:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:05:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:05:46 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:05:46 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 28 Jan 2026 03:05:55 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='4dfea527f66034c5b6f4ca26afe692ae292fd267fd3b295c7f54f6461c65fd33';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 03:05:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:05:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:05:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20855ee35b100477242852e16b31201fe7c4a7887f738d9623541a31f4a01b41`  
		Last Modified: Wed, 28 Jan 2026 03:06:11 GMT  
		Size: 20.7 MB (20727299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7c8f03a4ffe7b3000210838c5ceaa0bfb02b0115747ef674e0cb3a6f9cbabc`  
		Last Modified: Wed, 28 Jan 2026 03:06:14 GMT  
		Size: 144.0 MB (143989538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62231e3217da7f08de4a125662088363e41e26bfcefe5552517b85787795367c`  
		Last Modified: Wed, 28 Jan 2026 03:06:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5b0771acdb8d034f6c9f06f2b51180d55e8551fae0fe67aa6a1b1077397acb`  
		Last Modified: Wed, 28 Jan 2026 03:06:11 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f8a4da82345b1010679fa5cf19051022ada50b455a6ca583b01b916eab0e6d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff1fe642e5c37b5b458264ea47f9b14eb812796adcb92c64d8fd98fe02a54d4`

```dockerfile
```

-	Layers:
	-	`sha256:2fbfe58e543ff7c40a9e2cb37868aa1f40c5d5f5650345a57efe2e0c6eb74bc3`  
		Last Modified: Wed, 28 Jan 2026 03:06:11 GMT  
		Size: 1.1 MB (1070322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e704b05ec234b6770f4f6cdfb62f7f3d21f67cbad96f2d64362be61f8b38bf`  
		Last Modified: Wed, 28 Jan 2026 03:06:10 GMT  
		Size: 19.6 KB (19620 bytes)  
		MIME: application/vnd.in-toto+json
