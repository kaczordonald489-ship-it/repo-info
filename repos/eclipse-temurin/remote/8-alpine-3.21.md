## `eclipse-temurin:8-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:762836d0ca8810b9d9d65bccc11488b8ce9328562cdd434f9c0b8bc8e4b45e38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:96438b36bf70985d0a47732c6bb6e160602694ca78fd703553766703a2d33bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72458352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e102bbd7fcaae6b0aebbcccef00e0b68085431c24f9ee76902033d689a1d4295`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:57:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 02:57:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:57:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 02:57:14 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 02:57:14 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Wed, 28 Jan 2026 02:57:18 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2ded87ce3a1f912ac7263f7df526fb0a2ccbc09a2a0124e0b35e22c3decb9bc5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 28 Jan 2026 02:57:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 02:57:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:57:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3d6e7b00765ea59e5f54c1fe5701692042fd7d4a4c8e05d86695da80f2e594`  
		Last Modified: Wed, 28 Jan 2026 02:57:29 GMT  
		Size: 16.2 MB (16174636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28dced71935ce22bed08e72960a1591c22ceb0b31ab876520e13eea161fa17d`  
		Last Modified: Wed, 28 Jan 2026 02:57:31 GMT  
		Size: 52.6 MB (52637540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9948c8aa501d38a2ac60a0508bc4fd2fa57679b9ff42f780180040c6dae8dc`  
		Last Modified: Wed, 28 Jan 2026 02:57:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51864de0de19846fc330433ad37ff6dd578354cca27a6a986fe0cd5b9b8ab8ba`  
		Last Modified: Wed, 28 Jan 2026 02:57:29 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7fbc01d2f73ee175f9800742b71f3e11c3205ee24b50f38b325179d2c529810e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1119516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1743a183463452030c2960d2e4a7b2d48a2fa7445b06ced53336aacc49c932`

```dockerfile
```

-	Layers:
	-	`sha256:d0fa11599435203f2585be09b65c45e24fed4c4d85a7d16113198ef442393a92`  
		Last Modified: Wed, 28 Jan 2026 02:57:28 GMT  
		Size: 1.1 MB (1100805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcc3f6537271305094c48ba9f13603e5ca6084b64151495deb66927f18fcaec5`  
		Last Modified: Wed, 28 Jan 2026 02:57:28 GMT  
		Size: 18.7 KB (18711 bytes)  
		MIME: application/vnd.in-toto+json
