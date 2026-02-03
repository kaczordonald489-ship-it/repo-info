## `eclipse-temurin:21-jdk-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:e77121c67822672d9213162682dba8be5449a92904ee9e92f98fe593dfc1bfbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:15f701e28e7e67b141743ee22d92f3ea57acd75b8bf3e047f87bf7bfaafec2b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182698936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9433ad8efcc7281167bca7acf096809bc94d9a815e6f7c2c6561eb92960c0e4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:10:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:10:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:10:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:10:17 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:10:17 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Wed, 28 Jan 2026 03:10:24 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 03:10:25 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:10:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:10:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:10:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c37ebf6450e154c3d2b8e85a53d6a68517fa4a2b544dbf2db751cbe1f706d1`  
		Last Modified: Wed, 28 Jan 2026 03:10:42 GMT  
		Size: 20.9 MB (20949857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc5d0cc55d9ae993bf3def98c54f1b704bb17543b25572ada8f5f3324b79ef0`  
		Last Modified: Wed, 28 Jan 2026 03:10:45 GMT  
		Size: 158.1 MB (158102929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cdbc2409efff6789306384fb3c1e2d5d7f7a548575ef7e1a53284392f155f5`  
		Last Modified: Wed, 28 Jan 2026 03:10:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d8072e2c39f7c154e19e7fcc1cf714a0f2f6ccd8f1959585943050d82cb5a8`  
		Last Modified: Wed, 28 Jan 2026 03:10:41 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:672aecb853d81c9ed4604d35a9d71f2cea16035538fe809217da8ea449855e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1124744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29f2e066364264ed3f516a652e29596d331cf55e73f2121ae58706c3812345e`

```dockerfile
```

-	Layers:
	-	`sha256:a7d712e618c6835d138cd08ac7107551bec93cc2ce5d681e3a706ccfd099304f`  
		Last Modified: Wed, 28 Jan 2026 03:10:41 GMT  
		Size: 1.1 MB (1104322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ee8f8fc5a6afcb6ad5eb5cfc15374ba8739f79680f12f5c8722b8e5225576e9`  
		Last Modified: Wed, 28 Jan 2026 03:10:41 GMT  
		Size: 20.4 KB (20422 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-alpine-3.21` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:cebb705ef33b0a704017573c6e8b358a3b09e9ba754f379297f3c2bfd4681a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.1 MB (181098942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e62608d38cf192a0ed1c3e4e0f82af464379d1b4cf9c5650a349e96a3749c7a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 02:55:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:55:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 02:55:23 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 02:55:23 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Wed, 28 Jan 2026 02:55:30 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 02:55:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 02:55:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b96c1a71d1473746d06b1f65be592353943441da6b95dd97f8a9771952c7b8b`  
		Last Modified: Wed, 28 Jan 2026 02:55:48 GMT  
		Size: 21.0 MB (21006302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798b750f97901e80666a23bbae4f7bb989f36314526d73813f11fe00c596b5f7`  
		Last Modified: Wed, 28 Jan 2026 02:55:51 GMT  
		Size: 156.1 MB (156097349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6eb88585ec255ff1ca3354c0e1fc03074a46da11ee5428ead0808abf1473423`  
		Last Modified: Wed, 28 Jan 2026 02:55:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a694ed2d487a358b5619fdcfefbb02b3cc67e0d5b483b413c9fbdc7aa8da8f`  
		Last Modified: Wed, 28 Jan 2026 02:55:47 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cb3f55a86f59657da88c464779bd57e4915ba401bd93a0e443064f07ff53b508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1274868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5ba43e65cdc01f287147733dfc1b5202b54abcf722a42768a7d1df1d79699d`

```dockerfile
```

-	Layers:
	-	`sha256:2dedf04fd65a2d72d553f9e569ad5fbf51a8ac3b9a239e808050f59664963278`  
		Last Modified: Wed, 28 Jan 2026 02:55:47 GMT  
		Size: 1.3 MB (1254324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3fd55825fd09e4ed1c1e28eec3427f01d44a4e47749cef0f5f874450900f82d`  
		Last Modified: Wed, 28 Jan 2026 02:55:47 GMT  
		Size: 20.5 KB (20544 bytes)  
		MIME: application/vnd.in-toto+json
