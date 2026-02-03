## `eclipse-temurin:25-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:7ace075f29555df6696750ee3caffea4fb542a1db8a5b1e7578129162f071c03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:259338b5fce51035b85bbac235bf9558bb17e25347c3d3e3db66d5b22cf7e8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109333651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6781eae841edcce71860661d83c0daea11df54596ae9f2d30b6794aed83aebcb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:13:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:13:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:13:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:13:48 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:13:48 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 28 Jan 2026 03:13:54 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 28 Jan 2026 03:13:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:13:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:13:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:13:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c82c37cc1e371eead2dc58300215ff956e7c66f7a9be860363938c03e5c76da`  
		Last Modified: Wed, 28 Jan 2026 03:14:10 GMT  
		Size: 14.2 MB (14246382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a31aa63af3fdb098e136e53cb2a136db5e58d0d583a45a29aa0f688e2b0c3b3`  
		Last Modified: Wed, 28 Jan 2026 03:14:13 GMT  
		Size: 91.3 MB (91279981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e456b61d1dd1581cd1136ee74763eedb7bf7af1158ecad882564104548359d1`  
		Last Modified: Wed, 28 Jan 2026 03:14:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331024c35ae2ab78ba266cd395ff3155e7a3135687cde5017449ef802da8d926`  
		Last Modified: Wed, 28 Jan 2026 03:14:10 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f3eb342d53019aa53d246d5347a0fcb6fb4b1e8d0d52625b54a439409734f695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **969.9 KB (969879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537c7ee68da9914fa457cc2b56f4d4ba67943c7d5476bea8b9e4e280fc9bcd45`

```dockerfile
```

-	Layers:
	-	`sha256:7f3f65b4fb35bd126dc70a68310c2441573ee3b52e2318d82c7ef9c91ce8ddc0`  
		Last Modified: Wed, 28 Jan 2026 03:14:10 GMT  
		Size: 948.4 KB (948366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcbe5ca072f3fa1f98e89df40f505c0e4f7d8d97f0fd7836ff96a626c317f205`  
		Last Modified: Wed, 28 Jan 2026 03:14:10 GMT  
		Size: 21.5 KB (21513 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:5fab6278c863efd7cf9e418bc645ab1ee3a08c0451a7991f3de662fd80365bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108685134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f88d2a9ca50226369d26b6bcf087e96f4f50141e3ea8eaced2403ba16bc0719`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:00:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:00:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:00:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:00:45 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:00:45 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 28 Jan 2026 03:00:53 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 28 Jan 2026 03:00:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:00:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:00:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:00:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5288573acdcd1544c20a13292ab18c2f63bfc25bd67e4ff7fda45bcd6ff95602`  
		Last Modified: Wed, 28 Jan 2026 03:01:09 GMT  
		Size: 14.4 MB (14352508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59a6d58393b4efd9f9346f830fb5d4b12d5abe806a5efe2b15f408c79a26081`  
		Last Modified: Wed, 28 Jan 2026 03:01:11 GMT  
		Size: 90.2 MB (90190699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9452efb31da7be8de7a686fffee1b06489e32b6b26a07b4b1108bee8041a3e12`  
		Last Modified: Wed, 28 Jan 2026 03:01:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a8435556e3b5786f56d544bb393ce6a392d6617de1793d08481767d196bd9d`  
		Last Modified: Wed, 28 Jan 2026 03:01:12 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:91e5e5eb94cdc0ca46f366d8f3211f970a8d523ad47cc6410c80ccd2d60c9436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1120072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6f164ce9fcd769b0fea4b51c8052eb493c65766f2199f70a5741c80000bc4d`

```dockerfile
```

-	Layers:
	-	`sha256:0547c691764168c744df7ebacbd8de5432b036ee1b1d2be80046505f7db0629c`  
		Last Modified: Wed, 28 Jan 2026 03:01:09 GMT  
		Size: 1.1 MB (1098401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04101185f5ac4fe6b76bfbc914c841551881618e214046b36ade24f97dcaa166`  
		Last Modified: Wed, 28 Jan 2026 03:01:10 GMT  
		Size: 21.7 KB (21671 bytes)  
		MIME: application/vnd.in-toto+json
