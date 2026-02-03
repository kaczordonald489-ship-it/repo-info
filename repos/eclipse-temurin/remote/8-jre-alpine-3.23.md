## `eclipse-temurin:8-jre-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:7fb70afe6f6505e0739a399fdb6ad360504b8c745e4d2d46b4e59f65bf242d89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:701e1e3afc0f4b0c72133bc9b2efeb94b014069a353ab81243aae911af10d14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62547005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69cba780cd76c8ec9497ddb5ad343f317b2a1293a4bef896b5cc3e008f2a094`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ENV JAVA_VERSION=jdk8u472-b08
# Wed, 28 Jan 2026 03:01:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='0f169a177121cfd09b43ec5898770717482d02483f07b1b92a2e930dfd32fdb8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 28 Jan 2026 03:01:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:01:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:01:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:0d0ae511feec396ad7d1e90e3a16753e6d79f402fdf9e9727c725a67d07b1143`  
		Last Modified: Wed, 28 Jan 2026 03:01:48 GMT  
		Size: 41.8 MB (41842865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3385d8fab779b149f50a86bb9732efb83a04657d79f9976c62e2f6201ed3c43`  
		Last Modified: Wed, 28 Jan 2026 03:01:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760c81b1664bdc4dd24b79008869e8711ca0f9c5e55265e85aa754cb4ad75c3b`  
		Last Modified: Wed, 28 Jan 2026 03:01:47 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b176c1604586bb539f2be942c38ed901f05295b91694fa4d49eeccf3e9b53b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **952.2 KB (952204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118c142e53ed94cab50b94ebcdbf2c0ea887ea56dc16e7f010de83744cdff073`

```dockerfile
```

-	Layers:
	-	`sha256:8f0d346ecc7b3c647e396bc095440306826de3698aacd3ac29a3c13d8a7400be`  
		Last Modified: Wed, 28 Jan 2026 03:01:47 GMT  
		Size: 934.0 KB (934017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9467d46e42b8c27cdea76352c02daf0144eebe37c92c2d3ff5f64ba9818d49ec`  
		Last Modified: Wed, 28 Jan 2026 03:01:47 GMT  
		Size: 18.2 KB (18187 bytes)  
		MIME: application/vnd.in-toto+json
