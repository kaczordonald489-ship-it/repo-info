## `eclipse-temurin:8-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:15f103b2256871c82adfbbaa52f7a4d73af14d0be5cad27a4defa8d416e8b2c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:a4be3e2e436725444fbf3a42ba633cd61fe13aa3900ff705dd3d002c4635c2c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61663611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b69985785907927ac94caa4fe6e4518eda582c3843e82de41967f273f094da`
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
# Wed, 28 Jan 2026 03:00:10 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='0f169a177121cfd09b43ec5898770717482d02483f07b1b92a2e930dfd32fdb8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 28 Jan 2026 03:00:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:00:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:00:10 GMT
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
	-	`sha256:487ef254fb1a2f9b188459582546833b43dbfe1248f8cdd7d64dd198f952ffbd`  
		Last Modified: Wed, 28 Jan 2026 03:00:21 GMT  
		Size: 41.8 MB (41842825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e426fe160da02c99897aac9ab1effc530498fe6bcac6c1b30a6f83fd19d3e9`  
		Last Modified: Wed, 28 Jan 2026 03:00:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32434197ec68c038d367ea88a5de9ddc7680db3f7715a3e8eca3df2b923facc6`  
		Last Modified: Wed, 28 Jan 2026 03:00:20 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a3873eb0f3fdef71345aea6392e50f92d43e78562ace97e85b00873f52c5314d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.0 KB (945034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f52ceaf20c18a07ca6524e80ec3eba694724006bd96b011424a34da500e284`

```dockerfile
```

-	Layers:
	-	`sha256:94071caf24dfd63f6aaae18b90f1a43a248cc1b9e6cd671eb7c372dd77ebfde8`  
		Last Modified: Wed, 28 Jan 2026 03:00:20 GMT  
		Size: 926.8 KB (926847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:404d4b0eb306e1c82c543971d8189159542022d7ab060e009e446e239d993323`  
		Last Modified: Wed, 28 Jan 2026 03:00:20 GMT  
		Size: 18.2 KB (18187 bytes)  
		MIME: application/vnd.in-toto+json
