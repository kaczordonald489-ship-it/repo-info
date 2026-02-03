## `eclipse-temurin:8-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:279d542301ebacc5c572e7e9787fdc08b6f5d2478520dea89c83314810e52247
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:5375340f564bb96c3eaabcce27c3d747900df8decf07fb8c3d49fad0d5a28cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72738810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4603f9b08a32ed1286510258d4951af7c4b3a9a41d5e32a95424797ed82286`
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
# Wed, 28 Jan 2026 02:57:48 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2ded87ce3a1f912ac7263f7df526fb0a2ccbc09a2a0124e0b35e22c3decb9bc5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 28 Jan 2026 02:57:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 02:57:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:57:48 GMT
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
	-	`sha256:c1df43779a3c57a87747db20a005169860188285eceb9220b03b87ed7683041a`  
		Last Modified: Wed, 28 Jan 2026 02:58:00 GMT  
		Size: 52.6 MB (52637515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0d01f26b972e85867dd19b874203219c73d3801767fb8f02b00df47115cf35`  
		Last Modified: Wed, 28 Jan 2026 02:57:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1459b165f5168e1049b1396a4b89efa67519664e53ef8cf4c4211958e960ec`  
		Last Modified: Wed, 28 Jan 2026 02:57:58 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:75fc0fb97c4bb48d2ed7e0c018891d6fb0b2adfe4dd67ca548278cca9c550dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1123057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65537758a68cd3f2895d977baf5e57abc450670086fa1984ba8afa3dbf5a1d8c`

```dockerfile
```

-	Layers:
	-	`sha256:bfdd5081c2b3a1b31cbd31a2576cce260f1ed1a9eb52274a904dccc8892cf448`  
		Last Modified: Wed, 28 Jan 2026 02:57:58 GMT  
		Size: 1.1 MB (1103354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6179724ffd3ee9a483cf29fc5b6d241d327aaccc1128dcc1de50e1c5270906f8`  
		Last Modified: Wed, 28 Jan 2026 02:57:58 GMT  
		Size: 19.7 KB (19703 bytes)  
		MIME: application/vnd.in-toto+json
