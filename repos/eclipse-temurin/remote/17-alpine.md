## `eclipse-temurin:17-alpine`

```console
$ docker pull eclipse-temurin@sha256:e2219a46b9e20e3fe8bb303dd851978bb8f9bfb3c54da19e1ea245e326f3b1f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9acc785f69195f092e7b0a2226168061e7edcfbc6ec5ecff46d1f6f821f7bb03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168912267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31e49df7bb010155388aacfd218a1c414801daed21a92a3aa8516e77cb4b04f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:06:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:06:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:06:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:06:56 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:06:56 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 28 Jan 2026 03:07:03 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='4dfea527f66034c5b6f4ca26afe692ae292fd267fd3b295c7f54f6461c65fd33';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 03:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:07:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:07:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc77cdbd7bc1e2f452d8429402632b993034ee6bfccffc10cc8a951d8f9bf6b4`  
		Last Modified: Wed, 28 Jan 2026 03:07:19 GMT  
		Size: 21.1 MB (21115424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db795874e1acc8dcd7dfaa11e545c47a36bd9db774d51cecf4ab0273da86053a`  
		Last Modified: Wed, 28 Jan 2026 03:07:22 GMT  
		Size: 144.0 MB (143989559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4cba3796c63f930fa19b62040f34d6b16b4f7dd6a95896d3e6da8c177eabd7`  
		Last Modified: Wed, 28 Jan 2026 03:07:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357173fc29013c94bdde74c736de14f4dfaf05e42614f5d5346add87083f20f3`  
		Last Modified: Wed, 28 Jan 2026 03:07:18 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e3ee4c02a7ab89311baf8d5a47c2dba647ae0f44a6eec93b281e21018bdf09e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1124392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8a1d3b93bc13e260c876b9eecf5211ed9e9f053c1b73ab6e12ddfe7965331c`

```dockerfile
```

-	Layers:
	-	`sha256:d636009c309294635b54fb56a73fefab8f5ba85af8383f9a89c110fe55f47709`  
		Last Modified: Wed, 28 Jan 2026 03:07:19 GMT  
		Size: 1.1 MB (1103773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad091cc518c7c60966d82b3fa784dcf540ab4a3848758ffa72966999f3b50d4c`  
		Last Modified: Wed, 28 Jan 2026 03:07:18 GMT  
		Size: 20.6 KB (20619 bytes)  
		MIME: application/vnd.in-toto+json
