## `eclipse-temurin:11-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:7bb81d3c14101388f39c7800aa3d434123a22bfabe442b58812c2f6f3b7c1186
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e51b80f2e1b028ba8471a6e9909479952f380f775754d94bb327158a38dce0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160806524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6290f225a8289ffa4f09a6c2fef43848b093375d76ca2619216fcf4f2e8e75b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:01:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:01:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:01:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:01:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:01:34 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Wed, 28 Jan 2026 03:03:36 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c7b58655ffde7b5e6fce4a32fdcd21be5745b3bb64ee2bc723fcf55eae720ebe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 03:03:37 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:03:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:03:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:03:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd997c0233305feb28a469161700e1bbb74b5410bb0897a5168f97be4ded910`  
		Last Modified: Wed, 28 Jan 2026 03:01:47 GMT  
		Size: 16.8 MB (16839911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca2f6250f6fdad99102be1f6ed19379666c7b6fed865ddd352f5cdb8a425e62`  
		Last Modified: Wed, 28 Jan 2026 03:03:54 GMT  
		Size: 140.1 MB (140102386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6199d7641cf62a0121147f5d81153f662d441925fe76fb02615468f08931f8`  
		Last Modified: Wed, 28 Jan 2026 03:03:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973d5f47bcc17792d854174aa30df8e3af8c13a0be42929c93850f42c92266a0`  
		Last Modified: Wed, 28 Jan 2026 03:03:51 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:04a226b065ff9a46f9911ea0eab57df757875eb0bc94d866a0bbeea3241ed37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1025825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91da14f0d615232bca295f6c9631f635f59c793faadd8d3d7bf2ef09277d8f1`

```dockerfile
```

-	Layers:
	-	`sha256:e1d8f3fc86f21df4b15144fa8ad96aae4a267368de8dded1cadcd67717b965b3`  
		Last Modified: Wed, 28 Jan 2026 03:03:51 GMT  
		Size: 1.0 MB (1006655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe20ba31ef5dc5f9b3654d328b5f22cc1774e3e37f4cee8f8e75f37a549afb2b`  
		Last Modified: Wed, 28 Jan 2026 03:03:51 GMT  
		Size: 19.2 KB (19170 bytes)  
		MIME: application/vnd.in-toto+json
