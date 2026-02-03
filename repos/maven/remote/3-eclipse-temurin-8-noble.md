## `maven:3-eclipse-temurin-8-noble`

```console
$ docker pull maven@sha256:f41e3aa8c119f70b29e9b711ab6c343b55aef13236e508e4f13aedf11bf5cb86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-eclipse-temurin-8-noble` - linux; amd64

```console
$ docker pull maven@sha256:60615f0d31517214054e99b05970821d29890d83e7c5f1089ecd1ef4dfd3affb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133295503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f4ec6862911ed3a007d346bcd36cd0998f0ae3c0059b26d5815d98524db318`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:18:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:18:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:18:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:18:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:18:24 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 15 Jan 2026 22:18:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 15 Jan 2026 22:18:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:18:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:18:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 02:42:21 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:42:21 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:42:21 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:42:21 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:42:21 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:42:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:42:21 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:42:21 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:42:21 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:42:21 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:42:21 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:42:21 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:42:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:42:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:42:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a72c85106ae9a2885d2aab3a7c757b40d4b5915c54193b935f37111828dcf3`  
		Last Modified: Thu, 15 Jan 2026 22:18:39 GMT  
		Size: 17.0 MB (16975926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8532bae8ee50cd24b239a6fa063eb19526cff6782f6f74ae026a2178cda0a6e6`  
		Last Modified: Thu, 15 Jan 2026 22:18:40 GMT  
		Size: 54.7 MB (54742663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94376c6c055750f8b9c88f96b456f10b0ae030a3b44755a6e278c38518a9034d`  
		Last Modified: Thu, 15 Jan 2026 22:18:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc7e5b7949d54912db3f6da36540adee01df91f2667cdda51997344cba74339`  
		Last Modified: Thu, 15 Jan 2026 22:18:38 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d017f427a11767d419539a5677d466d9bf16bcfa0406de23deb886fb8221574`  
		Last Modified: Fri, 16 Jan 2026 02:42:33 GMT  
		Size: 22.5 MB (22535195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd25018ee9f8689ffe073f0aace8a7e4ebd952293cccd94429a5ce4a5ba969`  
		Last Modified: Fri, 16 Jan 2026 02:42:33 GMT  
		Size: 9.3 MB (9312235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dda40d310c645b0f399fdbdb565e511dfc4bf24dddeee0f0c4373223628e02`  
		Last Modified: Fri, 16 Jan 2026 02:42:32 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3037dc559031c2f2d16ff97ed02038637eb64cc1f27dd7a915629c6835a83d5`  
		Last Modified: Fri, 16 Jan 2026 02:42:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-noble` - unknown; unknown

```console
$ docker pull maven@sha256:2423222a854c0d5ed7876b3b09583f8892422ccba768757e13ab61cf0ff78678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5034672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d912aef9391eae3f97a573edc1e6435473e8754f2cf16c868ea77d0b20f6d88b`

```dockerfile
```

-	Layers:
	-	`sha256:70f95d19971d40f1cfa9f52f026e8d9df603e66c7734a6737d91ef9a3cf62858`  
		Last Modified: Fri, 16 Jan 2026 02:42:32 GMT  
		Size: 5.0 MB (5014007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc42b4615974eacc3bce546cfc2dc59ee910439673a930d8dd8460d66deba9b7`  
		Last Modified: Fri, 16 Jan 2026 02:42:32 GMT  
		Size: 20.7 KB (20665 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8-noble` - linux; arm variant v7

```console
$ docker pull maven@sha256:aceed04acef57db7f6a054afee28d8cdd8b515c787cfb426c1d9bb8f674fecac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129891240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437c35a05182bd0931acdd3773c14d66f10092ec3e1969cf331dc98fe4d7ed20`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:59 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:02 GMT
ADD file:9e6534a5b837dcbcc4b9596878a4feeb07210fb34c7385aeee0217ff03c2460e in / 
# Tue, 13 Jan 2026 05:40:03 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:09:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:09:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:09:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:09:28 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 15 Jan 2026 22:09:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 15 Jan 2026 22:09:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:35:09 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:35:09 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 15 Jan 2026 23:35:09 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 15 Jan 2026 23:35:09 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 15 Jan 2026 23:35:09 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 15 Jan 2026 23:35:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 15 Jan 2026 23:35:09 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 15 Jan 2026 23:35:09 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:35:09 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 15 Jan 2026 23:35:09 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 15 Jan 2026 23:35:09 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 15 Jan 2026 23:35:09 GMT
ARG USER_HOME_DIR=/root
# Thu, 15 Jan 2026 23:35:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 15 Jan 2026 23:35:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 15 Jan 2026 23:35:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a56277e49d30e9a430d5cefad3038f88470a8681e48b806fff292791ed54f1fc`  
		Last Modified: Tue, 13 Jan 2026 06:35:51 GMT  
		Size: 26.9 MB (26853837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9794ead862662ff877148f78c6a954afced26c3e80c70a689e42810257024568`  
		Last Modified: Thu, 15 Jan 2026 22:09:49 GMT  
		Size: 16.3 MB (16306643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f506d761ce6244c87ee0dfce86be439b17d5c712ef27b8a0a3ac3b4b5104180b`  
		Last Modified: Thu, 15 Jan 2026 22:09:50 GMT  
		Size: 50.1 MB (50144725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437dc824101437c30cc541a61762b87fdec86e527873aef7b68985de95fc7d84`  
		Last Modified: Thu, 15 Jan 2026 22:09:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13345ac4a0f33ab5d5bdf99805b68a8b4aafa373cab3e4997b4c691724de7f75`  
		Last Modified: Thu, 15 Jan 2026 22:09:48 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f0265c23e0e77d86fc03d49a0a2ac4c63dc46b24f1cc3be81e244a3a941aae`  
		Last Modified: Thu, 15 Jan 2026 23:35:20 GMT  
		Size: 27.3 MB (27270325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085fe75fb16cec5e6bf7fb972e0265ebecac61cb96754420e828b15c69bd77ab`  
		Last Modified: Thu, 15 Jan 2026 23:35:20 GMT  
		Size: 9.3 MB (9312237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9594d4142cfb44404bcc5e44e094a03651fcbfb327fa847a9662cba4c5baf4d5`  
		Last Modified: Thu, 15 Jan 2026 23:35:19 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2279a87ee4604c93e1cc30d2710224cc9645e54511885d5e8412fe2c5ec6be16`  
		Last Modified: Thu, 15 Jan 2026 23:35:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-noble` - unknown; unknown

```console
$ docker pull maven@sha256:772146f95bba183f069b657f404bac0a9924a3ba864add0c25e601519a219495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5037549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268dbf522cef2dfed60be0210c7ff9335d9941472fd1dc5c3f20df1814131716`

```dockerfile
```

-	Layers:
	-	`sha256:a2eb069bc7fd7d9318a4fefdd6e2f01aa63ee1e5133a7239fb6be33d147a0a8f`  
		Last Modified: Thu, 15 Jan 2026 23:35:20 GMT  
		Size: 5.0 MB (5016753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5fda9a8371d82c1febde1787a9ed8ffe484f89c798915376a4b75831776ec5e`  
		Last Modified: Thu, 15 Jan 2026 23:35:19 GMT  
		Size: 20.8 KB (20796 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d4dd4cb2bd07fb6b7ae3e38e33120b39811114eb32e15b2d62be2e94635382f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131593960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d2a7a11ee247f4723296effbd34b6d941eb348f571a01c6fc01a0488d4e570`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:18:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:18:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:18:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:18:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:18:09 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 15 Jan 2026 22:18:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 15 Jan 2026 22:18:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:18:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:18:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 03:30:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 03:30:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 03:30:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:30:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:30:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 03:30:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 03:30:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 03:30:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 03:30:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 03:30:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 03:30:26 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 03:30:26 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 03:30:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 03:30:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 03:30:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff97362347d944335e67dc97f791df6e3de56ed1781aa99a4ca33692fa504600`  
		Last Modified: Thu, 15 Jan 2026 22:18:26 GMT  
		Size: 17.0 MB (16991581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e1597199195be99da6ba3699ab0c1d82dd6441832add1d90203ab8145bd747`  
		Last Modified: Thu, 15 Jan 2026 22:18:27 GMT  
		Size: 53.8 MB (53819232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0034ac3de8e3a2a5c5f0abf5c548a847aa72462d18e200fb1171ce8fa46856`  
		Last Modified: Thu, 15 Jan 2026 22:18:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94643a2909473f2e8681911fbea874da9a68313af2222ab7784857c4be37b4c`  
		Last Modified: Thu, 15 Jan 2026 22:18:25 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3cb38441bd272d3edf2bc691fceeabface803f76c99562e3af15571185095d`  
		Last Modified: Fri, 16 Jan 2026 03:30:39 GMT  
		Size: 22.6 MB (22603601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4c0c1d4b41b5a476ede9813dfccfd14a38b2397ec95117fabb4f63e0897cee`  
		Last Modified: Fri, 16 Jan 2026 03:30:38 GMT  
		Size: 9.3 MB (9312253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15dffd1a5d55bc12809bacd0c8661df81355b756901fcab900bd6d1ab2591dd`  
		Last Modified: Fri, 16 Jan 2026 03:30:38 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebac255043c4b0686c01d4f5f962eeb042a1c1e89301626d242352937e44a061`  
		Last Modified: Fri, 16 Jan 2026 03:30:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-noble` - unknown; unknown

```console
$ docker pull maven@sha256:23a23a27b387282198a0160788be5be6c9dfb70d9370a8aff7eb5bbae9af0a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5042086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbed61be44385b91f40acbdd9c60a6f9f2aa280e3533c15abf36f37b726793e2`

```dockerfile
```

-	Layers:
	-	`sha256:d0bc4393810c71efeb3c49c7722b0f84842bf934ea5de20c69d33e1ae3598e75`  
		Last Modified: Fri, 16 Jan 2026 03:30:38 GMT  
		Size: 5.0 MB (5021252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb2df2bae25195f47741e13ecaca72ce672d03621e7559e58dd8c6ec9ad7e4b9`  
		Last Modified: Fri, 16 Jan 2026 03:30:38 GMT  
		Size: 20.8 KB (20834 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:351ed93a9d081dff0aa0eef094b6a3448ba40a7449db1773cc7b79d2512b75cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141200467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3557baf6144da7e4377742fb629843406291fb515046f736d869cd34d7451d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:10:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:10:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:10:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:10:45 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 15 Jan 2026 22:10:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 15 Jan 2026 22:10:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:10:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:10:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 06:13:20 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 06:13:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 06:13:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 06:13:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 06:13:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 06:13:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 06:13:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 06:13:23 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 06:13:24 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 06:13:25 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 06:13:25 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 06:13:25 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 06:13:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 06:13:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 06:13:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ce7f2b7cbaf214ce49ed3c453bb84e28408219a81e2d3ce0e3273159a849c9`  
		Last Modified: Thu, 15 Jan 2026 22:11:22 GMT  
		Size: 18.8 MB (18813960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c731c696bfc6bf5f9b3dda7ce45227d69565f4b34d38f8d8e3b97bddf02265a`  
		Last Modified: Thu, 15 Jan 2026 22:11:23 GMT  
		Size: 52.2 MB (52180265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dcf9a4124246e9878fbda9861c432b60778727de543c7b42110603a8938ff5`  
		Last Modified: Thu, 15 Jan 2026 22:11:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f633c41fe8ab0a9b47045e7f73e8d731d0fea39b5e70b8e86d7dd1e1a6be4160`  
		Last Modified: Thu, 15 Jan 2026 22:11:21 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4df368ff052781db57e7894c833a010121588fd5e3d0b5a4cd02a9d1d1835e`  
		Last Modified: Fri, 16 Jan 2026 06:14:06 GMT  
		Size: 26.6 MB (26584377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf81a85643e5ee91f1064849bb5dec9e238a768f5ea35f56489b87543db2938c`  
		Last Modified: Fri, 16 Jan 2026 06:14:05 GMT  
		Size: 9.3 MB (9312234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecd1f9b5806a33920318676e0daf0dbc4f1ac62f6b2baa82750e561599c12d6`  
		Last Modified: Fri, 16 Jan 2026 06:14:05 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e82abb5870ce3d22e12615b148e9ba05cc0db9555b7d4e945e0d5516c6c39c`  
		Last Modified: Fri, 16 Jan 2026 06:14:05 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-noble` - unknown; unknown

```console
$ docker pull maven@sha256:aba871231b9050cccaf9cd37f39a9fc2679b10d8a2626ecacdd531ac47d39dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5040283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09cde699b9e0e0e9d9106349202c3c6a9672ddc6b839e71656c81707a29c4a7`

```dockerfile
```

-	Layers:
	-	`sha256:b3399f8d050fb00bc6db642d090893bcbaaf5418390f8c5b4795ee4b2caf1b6e`  
		Last Modified: Fri, 16 Jan 2026 06:14:05 GMT  
		Size: 5.0 MB (5019550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b139dfc5b6b3a9eca5d0c81ac2bb0c76f88a43448b40e0c90cf3831c6d97ba7d`  
		Last Modified: Fri, 16 Jan 2026 06:14:04 GMT  
		Size: 20.7 KB (20733 bytes)  
		MIME: application/vnd.in-toto+json
