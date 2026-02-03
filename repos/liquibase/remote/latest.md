## `liquibase:latest`

```console
$ docker pull liquibase@sha256:cfc2129209c46f5761c0b2e10242d9c3909e30b20a64e56408b0c222dce0760e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:582fb237adcc6bfe24a76e91fc5a85937fafb12470f53e1c50946dd5ee9366e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111101266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ccda79cfd81d9a11e1f7b9f895d924101074308a7c4f179867dd2f3469a1ab`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

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
# Thu, 15 Jan 2026 22:20:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:20:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:20:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:20:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:20:10 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:20:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:20:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:20:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:20:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 00:34:52 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 16 Jan 2026 00:34:52 GMT
WORKDIR /liquibase
# Fri, 16 Jan 2026 00:34:53 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 16 Jan 2026 00:34:53 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 16 Jan 2026 00:34:53 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 16 Jan 2026 00:34:53 GMT
ARG LPM_VERSION=0.2.14
# Fri, 16 Jan 2026 00:34:53 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 16 Jan 2026 00:34:53 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 16 Jan 2026 00:34:53 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 16 Jan 2026 00:34:53 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 16 Jan 2026 00:34:53 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 16 Jan 2026 00:34:53 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 16 Jan 2026 00:34:53 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 16 Jan 2026 00:35:00 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 16 Jan 2026 00:35:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 16 Jan 2026 00:35:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 16 Jan 2026 00:35:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 16 Jan 2026 00:35:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 16 Jan 2026 00:35:00 GMT
USER liquibase:liquibase
# Fri, 16 Jan 2026 00:35:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 00:35:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c302597d98839a67b2d0eb53131fa4ef7965592afa8c476b8a799849d09954c`  
		Last Modified: Thu, 15 Jan 2026 22:20:26 GMT  
		Size: 16.1 MB (16147367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530b8601c1ef3ef81eb5c67cd33025b6798a46aa1e38c5c216c3f27dc893757c`  
		Last Modified: Thu, 15 Jan 2026 22:20:27 GMT  
		Size: 53.0 MB (52978517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa93b68716d37237a828ea6838f2d363ff8db2cebb0701b5a6cc553c1e28a37`  
		Last Modified: Thu, 15 Jan 2026 22:20:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce36aff9df917fee409541f259e7bf51507339b25d86a0bb2eebd24e393aaa4b`  
		Last Modified: Thu, 15 Jan 2026 22:20:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a549396a76b3c938219daea79b77385a2b8b05e065e4a1210042351f19fc648f`  
		Last Modified: Fri, 16 Jan 2026 00:35:09 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a9f9ac0fad4eafbe3e0c81dda8aa0aee009d042368779cda82b637319e72d4`  
		Last Modified: Fri, 16 Jan 2026 00:35:09 GMT  
		Size: 8.7 MB (8665791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cbe5c0fd723ba18cbe2fb5abf15463a59b30d3a0537527e026c820482effd2`  
		Last Modified: Fri, 16 Jan 2026 00:35:09 GMT  
		Size: 3.8 MB (3764543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432e69e7f8a887e94d3d60fa8b18f9f0d9b31b0f7de40bc14e07b74f97860a1f`  
		Last Modified: Fri, 16 Jan 2026 00:35:09 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9d316cdafd94c685d93d465c681f5f015230d91e77c07b56c11f5718f3f8d9`  
		Last Modified: Fri, 16 Jan 2026 00:35:10 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:a593d967f52fc6cad0073d0e4f79243476c95923fdf5b47eceb5b49312ac6e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a186871750905cd53526a1e089dd59f5ed97b05359b629c64041e43ba6e1891e`

```dockerfile
```

-	Layers:
	-	`sha256:649caab800b38204e7f19c87b7c8637e2dd99d2eb596004fd2d26667294938cf`  
		Last Modified: Fri, 16 Jan 2026 00:35:09 GMT  
		Size: 3.9 MB (3897745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c5dac49e3f2470eee7f08dc6dc70713dd6fa1d00ff9077c8015bbd0c1fa0635`  
		Last Modified: Fri, 16 Jan 2026 00:35:08 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:9448799ce0c8d2d4648ce7896ae87f1adae1f56765efa4f3f97b1ebbd1f80538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107713091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00abfb2c8f993c4ad9d9e2824b4fe6e3b1332e23e5b75ca9b80a61cf066d4117`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

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
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:20:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:20:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:20:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:20:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 00:38:26 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 16 Jan 2026 00:38:26 GMT
WORKDIR /liquibase
# Fri, 16 Jan 2026 00:38:27 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 16 Jan 2026 00:38:27 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 16 Jan 2026 00:38:27 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 16 Jan 2026 00:38:27 GMT
ARG LPM_VERSION=0.2.14
# Fri, 16 Jan 2026 00:38:27 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 16 Jan 2026 00:38:27 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 16 Jan 2026 00:38:27 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 16 Jan 2026 00:38:27 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 16 Jan 2026 00:38:27 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 16 Jan 2026 00:38:27 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 16 Jan 2026 00:38:27 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 16 Jan 2026 00:38:37 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 16 Jan 2026 00:38:37 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 16 Jan 2026 00:38:37 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 16 Jan 2026 00:38:37 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 16 Jan 2026 00:38:37 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 16 Jan 2026 00:38:37 GMT
USER liquibase:liquibase
# Fri, 16 Jan 2026 00:38:37 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 00:38:37 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fc3ef6de679ecac0a74cc044dd73825b9e6daa54ab0904bc8e9b9e898d5bdd`  
		Last Modified: Thu, 15 Jan 2026 22:20:05 GMT  
		Size: 16.1 MB (16065656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a219d36f811564c72bb7a6d0857ab0c8d89d075c294126c2b2a475008aa7a9f9`  
		Last Modified: Thu, 15 Jan 2026 22:20:56 GMT  
		Size: 52.1 MB (52148571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e1d55d5d40f3e93a56f24f668a26eea6fa6e5356a993c4e45d8e9953b76df9`  
		Last Modified: Thu, 15 Jan 2026 22:20:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999485e2399b87c1520ab9bc7b8571ffae8afc8ca4ae4945f41f8c3a95c1cf2d`  
		Last Modified: Thu, 15 Jan 2026 22:20:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22339f329ed16bc5f366187b46d1ca874f94bbfefe2d3b247d431ea0d9ed553`  
		Last Modified: Fri, 16 Jan 2026 00:38:46 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f4cb2c9bc55b0157043710c4197f4f449ce7692a8a4eb7de4dde0a06640d66`  
		Last Modified: Fri, 16 Jan 2026 00:38:46 GMT  
		Size: 8.7 MB (8665802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28db09e6a55451e8b949647b1f6e506b0767d3970efff8f37b9e5ef720041e2c`  
		Last Modified: Fri, 16 Jan 2026 00:38:46 GMT  
		Size: 3.4 MB (3441183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ea193430c972e0a857d2fc3bd86bbfc5d433c341fd6a0d7c6c44223d3dd2`  
		Last Modified: Fri, 16 Jan 2026 00:38:46 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b053658a2da6e5ccd5e53c5a6b69c16cc1d7f09b2480460f4d42c3e3825e5ef`  
		Last Modified: Fri, 16 Jan 2026 00:38:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:794295721f42ae19cb6a361a7b98ab0431326a42e2cf4c51ccc4f92ab2f2f83e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda0a1a21e80eb18b426ed1f2622a352fa869c41776d27b6898429975c0e04a`

```dockerfile
```

-	Layers:
	-	`sha256:f1f064fa648f1bec9aa1afe1149562710297f451da24811f23a3b31a0ab3571a`  
		Last Modified: Fri, 16 Jan 2026 00:38:46 GMT  
		Size: 3.9 MB (3897413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:568c19304eecceba457d093ad4154bc1c584c5e53aa9dc439cec5ee1f0a80f8a`  
		Last Modified: Fri, 16 Jan 2026 00:38:46 GMT  
		Size: 24.4 KB (24445 bytes)  
		MIME: application/vnd.in-toto+json
