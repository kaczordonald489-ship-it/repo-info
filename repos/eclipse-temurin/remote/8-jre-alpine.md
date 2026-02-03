## `eclipse-temurin:8-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:03500d0d064c414268c986bb23dd19badea448da5552fcf7a78e284463a141c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:676cf36ba6fcb36a9c3539ac95f101d9b40ec782a97e3000d0611c9609c6f12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61944096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122395fcf98b7f19999445d61cbd9812b22f451c82258f835a0164f817f4b44c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:57:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 02:57:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:57:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 02:57:45 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 02:57:45 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Wed, 28 Jan 2026 03:00:31 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='0f169a177121cfd09b43ec5898770717482d02483f07b1b92a2e930dfd32fdb8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 28 Jan 2026 03:00:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:00:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:00:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712170bbbcf08e7e6d5fdc5e77492f5ee689ccc346dfd3323e70ed3cd4ce6391`  
		Last Modified: Wed, 28 Jan 2026 02:57:59 GMT  
		Size: 16.3 MB (16293985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0403c81f746edc7d8819538d867c2f9bd63f12a8a63c6b4889b0a54018da7073`  
		Last Modified: Wed, 28 Jan 2026 03:00:42 GMT  
		Size: 41.8 MB (41842827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2130c333ba237d10bb71f06e32cf81da898f38e3028ce7bbfae439fdb5f279`  
		Last Modified: Wed, 28 Jan 2026 03:00:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7b3c27e03d5640ed819b2bd17fc8bcf07d4e3dbe3f68c58513bdac1117ccfc`  
		Last Modified: Wed, 28 Jan 2026 03:00:46 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5fa9757b1d068caf6ab7b70c0d434052d53e2ed0dfc62e8edf323b2201fcd87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **947.9 KB (947935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb03147f0e67c358ac1e15f5f913856f495fdcd23848a7d44193912e5f2a559`

```dockerfile
```

-	Layers:
	-	`sha256:ca77a82d432c6f46b182ea2c775fc16714e27170b8ade483dce1e3a5cecc1d9b`  
		Last Modified: Wed, 28 Jan 2026 03:00:41 GMT  
		Size: 929.1 KB (929076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f48c0f50fb027ef906e78dc75f552acb2db88589f9acbeb18830118c0498db60`  
		Last Modified: Wed, 28 Jan 2026 03:00:40 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.in-toto+json
