## `eclipse-temurin:17-jdk-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:45e3b48219b3ec3477d91e87544b56d7dab1f0a3574de126bdba3064f609bdd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jdk-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2845765cc4e1d77c265a33ca66862f1726bb7cb64f0290ba832b1e2991559254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.2 MB (169168941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5327c6a52a3401c7fcbbddf30de5c941a4c2918b42e192343ccac6369fbd1d88`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:07:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:07:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:07:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:07:53 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:07:53 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 28 Jan 2026 03:08:00 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='4dfea527f66034c5b6f4ca26afe692ae292fd267fd3b295c7f54f6461c65fd33';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 03:08:01 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:08:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:08:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:08:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33270a0a6f7d5cd140ef90e251143575f46698b49aa2f2b4bfa7e857dd5272e4`  
		Last Modified: Wed, 28 Jan 2026 03:08:16 GMT  
		Size: 21.3 MB (21315128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b855dcfe91d881aa30e6e448ad0a640290146d0aa271575970fa60cc3f7d1cf`  
		Last Modified: Wed, 28 Jan 2026 03:08:18 GMT  
		Size: 144.0 MB (143989583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3476dfaa0e8da46bce2ffed8445fb6e17cde73607d05b6b7ba1be475f8ded37`  
		Last Modified: Wed, 28 Jan 2026 03:08:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9314c63076121775c5c3c36b7e709d59a552c38d4a0deb4d676b616173c39253`  
		Last Modified: Wed, 28 Jan 2026 03:08:04 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4ba0de5acb2189c4c7190f28cbf23b5eb83d271e4010102f1b569abfa0d7dfb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1124964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cdc4d7458df40a42572ddd183a1d300e105007b711795e12cc0f6e1f034714`

```dockerfile
```

-	Layers:
	-	`sha256:b4bf165a1973ebc3633dcace18736628b92bc978dd7b69834bbc47fae7e5fab8`  
		Last Modified: Wed, 28 Jan 2026 03:08:15 GMT  
		Size: 1.1 MB (1105343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3170a8675a3c1e1a95b3b124aa08ed955724eb888bf35622022dbb602cb802f9`  
		Last Modified: Wed, 28 Jan 2026 03:08:15 GMT  
		Size: 19.6 KB (19621 bytes)  
		MIME: application/vnd.in-toto+json
