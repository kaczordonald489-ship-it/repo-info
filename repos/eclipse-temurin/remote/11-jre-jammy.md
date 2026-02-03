## `eclipse-temurin:11-jre-jammy`

```console
$ docker pull eclipse-temurin@sha256:88f8545b78c72f0233157a6a36d63dfb8a448891cff38f661ee0fe38ccb53d4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-temurin:11-jre-jammy` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:5173e55d3394668981e971609f94d7829f7fb2b73b6683aa3140e9f04d1c62b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92570203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536c7e0b704af4f34e953f831d8696f4f3f07ee9872d2edafb45a49451d20acb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:13 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 15 Jan 2026 22:19:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f72bbf49e53cd7abbf0a1938937550baad6a61278e830b27dc7ac0b1237056`  
		Last Modified: Thu, 15 Jan 2026 22:19:27 GMT  
		Size: 16.1 MB (16147450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52334a3339e5917bdaae310909a684a6d33f493ac029ad7bbb3d4d45bdf6a2d7`  
		Last Modified: Thu, 15 Jan 2026 22:19:28 GMT  
		Size: 46.9 MB (46883643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbb3186e79f54c1c8bc93b2e4ac17c88d0719c0662caf3c8f5fee1e4068afb8`  
		Last Modified: Thu, 15 Jan 2026 22:19:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d704164306ad1ff78584a292668f38506a0e6ff418351bfd0e4678c81a02bfb`  
		Last Modified: Thu, 15 Jan 2026 22:19:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:985fccf821ecb09e90cd1d5f9ab046ed05b42f78d5dad38e66d3d9caf857e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3914977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274174088732e120c66c5dab0d87bcf7c5e93acd44520a8131439e6b4491e452`

```dockerfile
```

-	Layers:
	-	`sha256:bf74a6cec14d2cfbbcc65d4ccc21577af1d6ce66d967bcd7fb135fd350c52713`  
		Last Modified: Thu, 15 Jan 2026 22:19:27 GMT  
		Size: 3.9 MB (3892484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c0d1ad9426d4af3714a47f92979cf8c9667d1ef69a1a3626fa91ad1b7c1b22d`  
		Last Modified: Thu, 15 Jan 2026 22:19:27 GMT  
		Size: 22.5 KB (22493 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-jammy` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:0eeffe9149330815ce5eb1957eff30c1c6d124e980f1b5a42943239d9a19586f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87583251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e272f9ec76fce96eaf5f35e98d58292c582358de04def548087645f3b66296f6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:02:38 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:02:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:02:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:02:38 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:02:42 GMT
ADD file:c6e8dc9cf610f17d4ed912b48dc43aef299146d67e62f2248ccd0e2cca210a77 in / 
# Fri, 09 Jan 2026 07:02:42 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:10:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:10:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:10:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:10:21 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 15 Jan 2026 22:10:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:10:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:10:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:10:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:83d1a597d0ed11bf60c1ab8ef65516448b87de3790f14ee8336174b7f9a56d82`  
		Last Modified: Fri, 09 Jan 2026 07:36:09 GMT  
		Size: 26.6 MB (26643402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dbfe0e4a3e1b55426985b0e755d33abe06266bf8cd68733654fa59e5e27c75`  
		Last Modified: Thu, 15 Jan 2026 22:10:37 GMT  
		Size: 15.9 MB (15890632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30468d2c90f924c1a9519afa4b9ca96ecfaf94c54580d548352fc47832c9bfdc`  
		Last Modified: Thu, 15 Jan 2026 22:10:38 GMT  
		Size: 45.0 MB (45046779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8a0937243e305f098425ab4fed456d847c7a20a93270b126a59dc736076e7e`  
		Last Modified: Thu, 15 Jan 2026 22:10:37 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf8ae01510bc04c2d4b113e5d1d1f1d6ff5462d99e73c27e10411cad69ac781`  
		Last Modified: Thu, 15 Jan 2026 22:10:16 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3b5cffa9c18d031a6cb3ca2d09cb8245dfeca5eb30de1cc5f9de4a6f5d988b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3918654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba896aef47db94921836d49a36494febf930bcb829bbcf63d145c4b6630ea411`

```dockerfile
```

-	Layers:
	-	`sha256:811871197e47cc2a10c669a5a80bd9300b3ba55b7da6d3908f30ee7000a6c94f`  
		Last Modified: Thu, 15 Jan 2026 22:10:37 GMT  
		Size: 3.9 MB (3896071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:691fc66cc64ac91deaf74564ea9270d35fae06b1995f7d92fb437710b6dd6de9`  
		Last Modified: Thu, 15 Jan 2026 22:10:37 GMT  
		Size: 22.6 KB (22583 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:55a189016e4199808a7a3438680bce8c3582d714638399ba040e102a9f073f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88672425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25905d3d566c6e37e85f8c7919814fbebdaa0156d6fccc8249cb483e521dd7fd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:05 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 15 Jan 2026 22:19:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e7c78b270fc977bd807e23019ea3b57ca39734f8ba060d62ef10d6f99e9d0c`  
		Last Modified: Thu, 15 Jan 2026 22:19:22 GMT  
		Size: 16.1 MB (16065931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b729da86244bc5e1a1e48c9acd85dc2d7a5f2456ae786c69f178857b683ec59f`  
		Last Modified: Thu, 15 Jan 2026 22:19:23 GMT  
		Size: 45.2 MB (45220556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dff9cf0162ae7bc52165e6958c57d5974c45f73dc204dfff761910068efcd1`  
		Last Modified: Thu, 15 Jan 2026 22:19:21 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb954ce4c40c8ba7cb4d1b301537c9468fbdb35dc33337742e5163bb52cb3c0f`  
		Last Modified: Thu, 15 Jan 2026 22:19:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:42f14625fbbdec9e3d25bce0b072de53756203b86f580e9b03bdccd4d0c653ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6debe2e46bb454fc34914d4776ebb662afbeb3acaae5b19780b1ba911807d601`

```dockerfile
```

-	Layers:
	-	`sha256:dfdfd601d1e1ac361f4db0a6d2cd57bb111bd6322ace2b4e223e01e8a444d37d`  
		Last Modified: Thu, 15 Jan 2026 22:19:21 GMT  
		Size: 3.9 MB (3892758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14eab02ff47b3e9ce28e814d8d0635e6747fb71d4cf5bb8f7e2acfdb79e4e0fb`  
		Last Modified: Thu, 15 Jan 2026 22:19:21 GMT  
		Size: 22.6 KB (22603 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:b2c65c2f91d3c0173a90d2685e1326c0809bc0d619fe4fac4a9b7a24b2704558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94359164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b9c30d70fa55101a2e4fe47aa67e4373b9e93b647c13bc7d16844250acb674`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:09:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:09:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:09:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 15 Jan 2026 22:13:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:13:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:13:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:13:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183556a79e45cd164d41dfffcf9da5a4846b19eb406b8300431457b5010ff3f3`  
		Last Modified: Thu, 15 Jan 2026 22:09:41 GMT  
		Size: 17.6 MB (17619200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b293ecafd630063bcb5186267efa589f780b852b7f4ae4f6161fc21b368d64`  
		Last Modified: Thu, 15 Jan 2026 22:13:44 GMT  
		Size: 42.3 MB (42290561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4efca18364173dfd2388d2503fc6932286ff0d015e2f28b9e09194042f4b1e`  
		Last Modified: Thu, 15 Jan 2026 22:13:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262e22cdecd7e1c54b3ecf1d2ca9016d4abcf373561c9bbab60a3823ccf7129e`  
		Last Modified: Thu, 15 Jan 2026 22:13:41 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:55ea933007a8841b2e5e163dafb145b085a77911c20707a4fccb02486cbbc1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd57dd39271e5a34ddcdc78a0a2bd9f47882136e4208c9da9c1c8b7aa5cdd754`

```dockerfile
```

-	Layers:
	-	`sha256:8b673b34348f4ba4c19925ab97a9f89af4191f9ae14a55d43352305067d78f08`  
		Last Modified: Thu, 15 Jan 2026 22:13:42 GMT  
		Size: 3.9 MB (3896563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f3b9b3517c924613649bcf8d4386e6ad76f5ce2de8ab31eae17a3f142c781e2`  
		Last Modified: Thu, 15 Jan 2026 22:13:41 GMT  
		Size: 22.5 KB (22529 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-jammy` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:501f10c512f2a746db275f5c18e382b87186afa64b8b3e633555f0734b00a9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85032592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf6b34f02547a40bcf2bbf2c8db1183fe319f7978f8c9bcb74858a56d00326a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 15 Jan 2026 22:07:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:07:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:07:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:07:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Fri, 09 Jan 2026 07:36:31 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:07 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5756fabaef1b7457ab960f2aa94d20ec15c3df6ec7fef1bc4fcc286452731bf8`  
		Last Modified: Thu, 15 Jan 2026 22:08:08 GMT  
		Size: 40.9 MB (40880653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c93407051451d97f5b77b799507f6e56cf6e8af23ee883a6ff564cf52afcdf1`  
		Last Modified: Thu, 15 Jan 2026 22:08:07 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db9d6aa879ded96abfcbf210b06cb8e8df22a13e843c05d8bf2fc6099a54903`  
		Last Modified: Thu, 15 Jan 2026 22:08:07 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3032f5a3f96762da2c45604907e8aca1490e713e51a2d4a4f89f1480b664c610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d963cbc01783cd8e23ba93c9c0588561c5250d23587dd69006a549b672151c0`

```dockerfile
```

-	Layers:
	-	`sha256:b880c8b6ae88da1fe90551f9a090ac29c400735898c86a10e7bc83d912151955`  
		Last Modified: Thu, 15 Jan 2026 22:08:07 GMT  
		Size: 3.9 MB (3894082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f446eb7501bf09d36fbec47a1c038173078cfb2c5e6ffad34ad808a099da7cbf`  
		Last Modified: Thu, 15 Jan 2026 22:08:07 GMT  
		Size: 22.5 KB (22493 bytes)  
		MIME: application/vnd.in-toto+json
