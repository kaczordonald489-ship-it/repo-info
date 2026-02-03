## `eclipse-temurin:8u472-b08-jdk-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:7cf580bd042c694f973f5e9ba20afd44b0eb606aff2392813993cf063ed10c7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u472-b08-jdk-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:26c9880fe23bb59b56bd37461b01baae053406f84fc295d16cffa89e760a2d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73341717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b290285c277c143ad7f067d88153004feaf6301ca6bca9cf017e455399da04`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:58:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 02:58:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:58:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 02:58:26 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 02:58:26 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Wed, 28 Jan 2026 02:58:30 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2ded87ce3a1f912ac7263f7df526fb0a2ccbc09a2a0124e0b35e22c3decb9bc5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 28 Jan 2026 02:58:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 02:58:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:58:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebb88d94ebe4bae471da80ffe1eca7993559248bd0e1920ab2d7237cf26ab03`  
		Last Modified: Wed, 28 Jan 2026 02:58:42 GMT  
		Size: 16.8 MB (16839938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdc257f8fb43da7b05d6b688d0c3f115fbeaf206ee6f63a61fec0ed88c08724`  
		Last Modified: Wed, 28 Jan 2026 02:58:42 GMT  
		Size: 52.6 MB (52637526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df81e2781748341009b4e5ae1676276af168920ce3f241e377dfa7fb6f8b7f8`  
		Last Modified: Wed, 28 Jan 2026 02:58:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e094d13c996e34e1bd1640ae26c84acca7c33e9232d31cd0d1608ee9a357a1e9`  
		Last Modified: Wed, 28 Jan 2026 02:58:41 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jdk-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4ad4a3255731721715f5976913c11a211c18a0cb8cce8e7fd7a263ce53c8a44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1126686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fb37f40822e5f3e4b90b2e2cf00917bd9f1f39db76327750e1d4610135bc7a`

```dockerfile
```

-	Layers:
	-	`sha256:e8f55b6dee40fe7e98147922a039b60a9fcaa320424b5ca7e4bd5ac7c2e0a74c`  
		Last Modified: Wed, 28 Jan 2026 02:58:41 GMT  
		Size: 1.1 MB (1107975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed74e0c96d3b619345e68b2f2a461646b31c324465a3901d75f0eaa8a1bf2bb`  
		Last Modified: Wed, 28 Jan 2026 02:58:41 GMT  
		Size: 18.7 KB (18711 bytes)  
		MIME: application/vnd.in-toto+json
