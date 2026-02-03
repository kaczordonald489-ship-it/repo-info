## `eclipse-temurin:11-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:702889447adf4d1ae8fd0daceeff1acba4636638177a75ec1935d667bbf03ad2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0d3fb63e97c902897c87572f3d6252a2deecf404e3b135c5267c0aa22dea14aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159814082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b670b6a524f23892168089989fa79c9ba83527c7a3ca8dff1556cf9a00301048`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:01:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:01:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:01:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:01:55 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:01:55 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Wed, 28 Jan 2026 03:02:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c7b58655ffde7b5e6fce4a32fdcd21be5745b3bb64ee2bc723fcf55eae720ebe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 03:02:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:02:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:02:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:02:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0c7c73d405bc71c22f0a011d7ee9e9ac1092f59d6da2bf39f6fde41ce84cde`  
		Last Modified: Wed, 28 Jan 2026 03:02:22 GMT  
		Size: 16.1 MB (16081464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff09436fb44e18e2345a14da0a36d3978c2b9efd016ecd84dd99b88d562712e`  
		Last Modified: Wed, 28 Jan 2026 03:02:24 GMT  
		Size: 140.1 MB (140102344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762e069fdb73da931a26d1f0418beadcdf3e708a680c0513d0d1115be16b7242`  
		Last Modified: Wed, 28 Jan 2026 03:02:21 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c64989395d63074dfe07422d745d01df55b27217b14d4f9336b3c719fdc3edf`  
		Last Modified: Wed, 28 Jan 2026 03:02:21 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:101953e8df26382f5bfdd6e5e49a47ac1b0ff76c459ff0800c409f682b4c991d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df09eaca59f19ec39d39927ed8889ae38d00fe904c2f683c38a3d1467a74068d`

```dockerfile
```

-	Layers:
	-	`sha256:f5d9384dfb5eb655a801402c4acf4153aa21258c7d1bc990a051c8c4cb3dadb0`  
		Last Modified: Wed, 28 Jan 2026 03:02:21 GMT  
		Size: 993.0 KB (993009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1759aae9da5efac9886a72b765ced1c14ec8ad6b63ec355ed85da135842940ce`  
		Last Modified: Wed, 28 Jan 2026 03:02:21 GMT  
		Size: 19.2 KB (19170 bytes)  
		MIME: application/vnd.in-toto+json
