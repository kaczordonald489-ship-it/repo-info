## `eclipse-temurin:8-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:8fa724afe68880126b33dc267dcd3566e894b488d1702354013ed04edab54138
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4bb7279b2579da46fd2db4485e989b1af462d0dc9ba31126a2e6cc76b2e42286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61554585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12e11a3648d173779482a2cf1e67a6cde0209a5fdce3d3bfc90644ce1859e8f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 02:56:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:56:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 02:56:19 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 02:56:19 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Wed, 28 Jan 2026 02:59:10 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='0f169a177121cfd09b43ec5898770717482d02483f07b1b92a2e930dfd32fdb8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 28 Jan 2026 02:59:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 02:59:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:59:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf41906f75cbf579942c86038e2fa35270f037e8552f6fcb4d338a279cab3331`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 16.1 MB (16081455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5a9b80c8ad521355986e8b91b560d9ad8c3636f9d2e44ee51b665399806685`  
		Last Modified: Wed, 28 Jan 2026 02:59:20 GMT  
		Size: 41.8 MB (41842859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92360374097109cb7762ed2599b92527fcff4b821affcb1c97d1e7aa9a025f0c`  
		Last Modified: Wed, 28 Jan 2026 02:59:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a23c080d114a4650f729f24c45917c9c4cc22d7d2232a5e9bd91aaf8dc4629`  
		Last Modified: Wed, 28 Jan 2026 02:59:19 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e04b79f8a308a52bd3f81f4037076d6f1ab3f463a28e6e1a3d376c307b54ec69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **938.6 KB (938558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f601f3620429b30ac6ac21e9a178bcc2f88ef245f7d471f5e9c5a90409f193b`

```dockerfile
```

-	Layers:
	-	`sha256:e74484d2e8d5f9b520abd5f7bfc5c9defbdfbf9704a07f139f618e4d342b6abf`  
		Last Modified: Wed, 28 Jan 2026 02:59:19 GMT  
		Size: 920.4 KB (920371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b86d27641aff26c7cbf229f581ff2cb63916529e2d201bc090ba7d79630d674d`  
		Last Modified: Wed, 28 Jan 2026 02:59:19 GMT  
		Size: 18.2 KB (18187 bytes)  
		MIME: application/vnd.in-toto+json
