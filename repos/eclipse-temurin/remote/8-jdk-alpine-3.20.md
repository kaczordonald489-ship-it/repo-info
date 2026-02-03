## `eclipse-temurin:8-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:413c9f243aa5ecca021fbeca5905db95fe4532a08a21d319ce1bed00edd00fa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4a92c60d72115aabb2ff26dcdda6fafa34a386b69acbc810b6c663cb1c06ecda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72349257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6577f73387dcce1e6ab8c51394650edbf8ab8d79481929a229f065cb73cb25`
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
# Wed, 28 Jan 2026 02:56:25 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2ded87ce3a1f912ac7263f7df526fb0a2ccbc09a2a0124e0b35e22c3decb9bc5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
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
	-	`sha256:4670988b528641c13717ecdc16865084560306fff1c7dd96a9fde30f3583a7b9`  
		Last Modified: Wed, 28 Jan 2026 02:56:37 GMT  
		Size: 52.6 MB (52637504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8134229cf416656b2476bbbe0708f656a066ed1198d1e9bca14b3da64e5c48`  
		Last Modified: Wed, 28 Jan 2026 02:56:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e5a15f317fce02fc1d2b0283e6b52efb904c5229b94b0b67d5a2289b6e733b`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:68c8959b44c45d5be43c1eb0713c23bafe96dec98919fbe5567499b6b2dcd0b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1113040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee009abb201357ab28aab791cfd1e0690c8be8fa7846a602691e942cf9693e1`

```dockerfile
```

-	Layers:
	-	`sha256:bb0c37c1bfaf9e6d79d03729dff0c3f3bec4b8b3242d47f7def924be19bf61c8`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 1.1 MB (1094329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e4ca8f637afaf1e3cc68a11d1ff7f80930b96888296c5d0fbb4feff8f99c2dd`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 18.7 KB (18711 bytes)  
		MIME: application/vnd.in-toto+json
