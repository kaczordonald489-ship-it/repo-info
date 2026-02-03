## `eclipse-temurin:21-jre-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:08eecc477dbe3f2e33daac27f36e41daf7f4ec51d2f3396006e54fa41832c74c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jre-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:ffac82f380c99670c6b02370855fa69ad7a4a9d7609b19cd95b3e180b0b2acfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba49c6e52565f769011b069ba2e3a8bc6c76f9b74b22d3172532e810ac03a09`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:03:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:03:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:03:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:03:00 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:03:00 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Wed, 28 Jan 2026 03:12:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7f8c230ba505b418e4288e2b34758a6e4da32470944740e5ba0cfaae02271c22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='17aca4ecc1600f70ec88ea0f8bf3a06ba6806bdae8c96d03c07683c800f0d4e8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 28 Jan 2026 03:12:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:12:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:12:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a95a7405177abd55077356ffb7a848c87d9ca9c23db8124d028a03a08abbd43`  
		Last Modified: Wed, 28 Jan 2026 03:03:22 GMT  
		Size: 16.3 MB (16294011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d692f84685999cf52a16deb2a62f05a72b23b165370268bb9f84bf2720cbf86f`  
		Last Modified: Wed, 28 Jan 2026 03:12:46 GMT  
		Size: 53.2 MB (53169010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbea5914daf9376671fa3a740cdc4cf83f54bc69c4802edc5123a3224fb2878d`  
		Last Modified: Wed, 28 Jan 2026 03:12:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a0e1e7665e6e529029146a70d0814061dd236331e5b77b0c739c34fd466769`  
		Last Modified: Wed, 28 Jan 2026 03:12:44 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3e28545e27783366cd27ec38d3ecc52a7451e0f877cba1e1eb54d18332224d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **919.9 KB (919920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973e2fb7a2692800ad0da4c2e775454eaab1f5539358bc5cb98db971322b56ee`

```dockerfile
```

-	Layers:
	-	`sha256:967a5cd3457e06a1b48c56dcb0dff47fd1eb0ad4c88b4897b201693d812ce68c`  
		Last Modified: Wed, 28 Jan 2026 03:12:45 GMT  
		Size: 900.2 KB (900221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68b5e2c0d5450f541fbe757f2ee559aa7c44f337ca4ccae68552136e763d4e7d`  
		Last Modified: Wed, 28 Jan 2026 03:12:44 GMT  
		Size: 19.7 KB (19699 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-alpine-3.22` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:8454a719029b75190362aa7b5a3f10c14d5d55494cf485272abd1fa60c3f538d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72626622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d162b865ca65f7c06c2c887fe97b3889158a54ae03f1deb90ad98ee75e84fb82`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:58:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 02:58:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:58:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 02:58:37 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 02:58:37 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Wed, 28 Jan 2026 02:58:40 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7f8c230ba505b418e4288e2b34758a6e4da32470944740e5ba0cfaae02271c22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='17aca4ecc1600f70ec88ea0f8bf3a06ba6806bdae8c96d03c07683c800f0d4e8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 28 Jan 2026 02:58:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 02:58:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:58:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c24115e8411f4d7573c11f391a90280e4d56095cc395d3092b6a130688b6a8d`  
		Last Modified: Wed, 28 Jan 2026 02:58:51 GMT  
		Size: 16.3 MB (16258234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b67ace64d831b85fef838eaaa1fe4f670492e335b3c224aa1dc424897a2fab4`  
		Last Modified: Wed, 28 Jan 2026 02:58:53 GMT  
		Size: 52.2 MB (52226461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03eb363046abe0e3136c465d80392d4c599e6ab1b8c7986e57a303bb02e8a89`  
		Last Modified: Wed, 28 Jan 2026 02:58:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f79a9f2e9a637bcd3b3896f8afa7f5cda80ce104d3d9eef9cb9475b6d9ba06`  
		Last Modified: Wed, 28 Jan 2026 02:58:51 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:898a7454a23ea408c2866d10ada9a6ae5e653f9a9c5d51f92bbe7c44765d2934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **919.5 KB (919492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c0ac29530ef4e387298fdc2910026ea5507e1e971ce662d7f0448759335701`

```dockerfile
```

-	Layers:
	-	`sha256:7ee9f066f2ab3f1ed8951fd893db38a36a366e4668a600b2327ecea38ce4d17e`  
		Last Modified: Wed, 28 Jan 2026 02:58:51 GMT  
		Size: 899.7 KB (899659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a49144bd6363b35cc9696d66c5228ab9581c49c86443e46d76fab04517ffcfe`  
		Last Modified: Wed, 28 Jan 2026 02:58:51 GMT  
		Size: 19.8 KB (19833 bytes)  
		MIME: application/vnd.in-toto+json
