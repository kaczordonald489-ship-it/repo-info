## `eclipse-temurin:25-jre-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:2d3cd2323c18a9a8073935503f0a1733b6c45b455b94f23294c3df336240fde7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25-jre-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:bcafe5f4865a6e446e594d9b7291228fb821e829d63360a7946c6c2075b99d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75291067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6985e8d0c40d5a8ff55be98d048bb9ebef62e675417b0d0c7707d9f4577f75af`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:14:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:14:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:14:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:14:54 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:14:54 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 28 Jan 2026 03:14:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='0176d4b18047ce6669c451e7293998961340a6720e979adfbfefb7356d21d597';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='46a7eca285957dadb0adacd96fe385bc5512f31b7f90a3dd01f04679d614a420';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Wed, 28 Jan 2026 03:14:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:14:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:14:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68749b27f3260f31302623199f52b49c24a80f2396be8cda8a0a3f3857239e93`  
		Last Modified: Wed, 28 Jan 2026 03:15:10 GMT  
		Size: 9.4 MB (9448670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7884531544f62ceff0d4c024846dd25bc0c1f263186fa6feeef50044c55a01a1`  
		Last Modified: Wed, 28 Jan 2026 03:15:12 GMT  
		Size: 62.0 MB (61978168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479cd42f37e75ae38fa26ba1499a53d2c09c5ec423eab0f25b5ac0e2d6319b9d`  
		Last Modified: Wed, 28 Jan 2026 03:15:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73f2ac35cef4ca3c306cd03f706bb63a4669ec99ef97778f985c3e0c5308f1a`  
		Last Modified: Wed, 28 Jan 2026 03:15:10 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2cc9ddd8996777c7aa544f2b939d45c40250d9f1870daa94fc5e294239c0f220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **821.5 KB (821481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c953932af342806425d22df436950aa4ad3d08e51647f27433ba294ac38d50`

```dockerfile
```

-	Layers:
	-	`sha256:cf8ef97d4c83b0886822cee20d32d99636bf90fcb90944088bb99326871b4429`  
		Last Modified: Wed, 28 Jan 2026 03:15:10 GMT  
		Size: 802.4 KB (802360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03eaa9ac14d1a8ff00a81cce7d9d32d1c6e77ad3e208f362f801414e9a300f0`  
		Last Modified: Wed, 28 Jan 2026 03:15:10 GMT  
		Size: 19.1 KB (19121 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-alpine-3.23` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:2f1805b4202a6f0e5012e214d294b931a0e78485f9c2e4ae37878d7941baa45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74545109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bc3a0e945625b3b174a649fcbf3083d61d6b619f19d71455181e6c3b37b4c9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:02:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:02:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:02:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:02:48 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:02:48 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 28 Jan 2026 03:02:52 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='0176d4b18047ce6669c451e7293998961340a6720e979adfbfefb7356d21d597';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='46a7eca285957dadb0adacd96fe385bc5512f31b7f90a3dd01f04679d614a420';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Wed, 28 Jan 2026 03:02:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:02:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:02:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c83eff7abb4bb59817b7c4042c54c566595552068a329aeeb14a08785b708c2`  
		Last Modified: Wed, 28 Jan 2026 03:03:05 GMT  
		Size: 9.5 MB (9469556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cee1b7e2bef89635d37451aff50b3c3a8892c310b355a302dbf9119b2ec3fa7`  
		Last Modified: Wed, 28 Jan 2026 03:03:06 GMT  
		Size: 60.9 MB (60876054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022035a7b6f8dc789ec30c09f7261deff60c354430ff3908694fc2e606454a3b`  
		Last Modified: Wed, 28 Jan 2026 03:03:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a702ca7d5f8f5cd4d1dec5f8b6ba065dd9026c84bd9aa9229bdcb9a1332d9104`  
		Last Modified: Wed, 28 Jan 2026 03:03:04 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2a288abdac4a075ee729d4a8048be80d1cc391b4a5c5b9682f0c3ca5f7d3b799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **820.4 KB (820352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e29ec497e9ee56c9e3f1b544b90e39a8ac748cc937dd2c455f4190554bec982`

```dockerfile
```

-	Layers:
	-	`sha256:8d3f56f7498b57c3160ff4f6fab0daf514ff18eb50dfec7db9cc873455fd72b6`  
		Last Modified: Wed, 28 Jan 2026 03:03:04 GMT  
		Size: 801.1 KB (801121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d31bc376a1825ab843d1e40101b1d2672075113fccc025a8b2363251e81c1d2`  
		Last Modified: Wed, 28 Jan 2026 03:03:04 GMT  
		Size: 19.2 KB (19231 bytes)  
		MIME: application/vnd.in-toto+json
