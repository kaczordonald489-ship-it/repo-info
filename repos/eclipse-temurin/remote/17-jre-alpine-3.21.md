## `eclipse-temurin:17-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:2775d6e7fb2852e571fa214964811fd520779a02c8c7893ad833a22f137d47c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e7a624df5755e1f91877f4cb9cd3664afbfd089588e1d63652f9ebae222ce341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66539753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe668fd93293a786c6b7c23025623485e299b7aaaf77040e5e0790b9c50c2a96`
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
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 28 Jan 2026 03:08:53 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='6c3047e8edd3878e8d2a1cee95c04606042c6a55954ad365d20b58f88cc9ecd5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 28 Jan 2026 03:08:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:08:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:08:54 GMT
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
	-	`sha256:7cacf4032b2f467231bd860ce5e77c8a7933a563a0d105e9afe7949c1ddce449`  
		Last Modified: Wed, 28 Jan 2026 03:09:05 GMT  
		Size: 46.7 MB (46718967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35297c9e392bfb68c151cae55472d29df8db40b852a14483df69f73417d4d6b`  
		Last Modified: Wed, 28 Jan 2026 03:09:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598c53817a36ce583c4a8b4c8283d905b4ba91a664368bdd53bf0f77f7ef3518`  
		Last Modified: Wed, 28 Jan 2026 03:09:04 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:096a57bb6a03166ca372408053310f53541f51b28bd6ceb1341b09b344e8ceec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **913.7 KB (913718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc7a5552840d204069da5a430a52d6e68523b24ee3278150efd3b62136ec80d`

```dockerfile
```

-	Layers:
	-	`sha256:581f60c48d6ba888588691e0af1bd3d6a08f7892bc2da6c747b61cc625351231`  
		Last Modified: Wed, 28 Jan 2026 03:09:04 GMT  
		Size: 895.5 KB (895494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4260bc1b07249157f2167d50a0a0dd4b6860f2a614ab18320170515877dd4dd`  
		Last Modified: Wed, 28 Jan 2026 03:09:04 GMT  
		Size: 18.2 KB (18224 bytes)  
		MIME: application/vnd.in-toto+json
