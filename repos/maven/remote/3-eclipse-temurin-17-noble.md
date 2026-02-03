## `maven:3-eclipse-temurin-17-noble`

```console
$ docker pull maven@sha256:ad60c60f9cafc2ad2181a419dea6440a64669876b0c3fd35a6f5657701d13fff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `maven:3-eclipse-temurin-17-noble` - linux; amd64

```console
$ docker pull maven@sha256:85fa4d79dbe2d662ad861ae2938c70a923d5f106dd04e4be9ec892558b19d14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229395574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7787045d71260881de0c397762bf3efad015d5ba89bd93ae59072b3bcad971`
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
# Thu, 15 Jan 2026 22:19:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:44 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='fba21763f6553efb65d774f51ab6a347e67a69eb2bb2d26980cdf2ee0f35a6db';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:51 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:51 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 02:08:21 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:08:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:08:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:08:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:08:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:08:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:08:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:08:27 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:08:27 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Fri, 16 Jan 2026 02:08:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:08:27 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:08:27 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:08:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:08:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:08:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f0f1ec9ea380a6af4a85e594cff7bccbe1c7d5311177ebdc52d3e6d2f04b7`  
		Last Modified: Thu, 15 Jan 2026 22:20:07 GMT  
		Size: 23.0 MB (22961250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3404c492510be2396378b473c5470243eb685ac3c2fdcef9fbb84ee599ddc259`  
		Last Modified: Thu, 15 Jan 2026 22:20:10 GMT  
		Size: 144.9 MB (144851725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682d1a3197c6ea11de7df99dd2f999e6acfbca27646f512103d6a81c3d3994cf`  
		Last Modified: Thu, 15 Jan 2026 22:20:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c940cc503ed4660889aab5fe6ab7b4e7f6f5668ee17a74fb1b5918d33e645f92`  
		Last Modified: Thu, 15 Jan 2026 22:20:06 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863408270529aa04152055412a0cc16659262e1582c94d82ce87f40d28c413c5`  
		Last Modified: Fri, 16 Jan 2026 02:08:40 GMT  
		Size: 22.5 MB (22540774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56559f60d03b75798ef8c2d5819479246113f25a989651c81e22d43862b50763`  
		Last Modified: Fri, 16 Jan 2026 02:08:40 GMT  
		Size: 9.3 MB (9312016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaeb52b7a4a9472abd60dddab4cf453289209f171f5127e75e0be499c842913`  
		Last Modified: Fri, 16 Jan 2026 02:08:40 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1aa553afb458605dae29563f06c5c1580dac87519bee2923224a580788afe9`  
		Last Modified: Fri, 16 Jan 2026 02:08:40 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42bb9482ac1eeb662e4b72e82cb5b27d44844bc7966b8f0f72eb2e9b38c5c44`  
		Last Modified: Fri, 16 Jan 2026 02:08:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:4f5276e048e4cc85162dacf54ddf70b9f83e79e646b2f55a42bb730708d77f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5070866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7391eb396d90f782fbcb9d986c7fecf384a9f35fffdc0f97fc49a683284794`

```dockerfile
```

-	Layers:
	-	`sha256:dbd430b3ebf299229cb134f899f853f1b6e527672fa18b3468399cb4d0e7772e`  
		Last Modified: Fri, 16 Jan 2026 02:08:40 GMT  
		Size: 5.0 MB (5044756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0199a2ac9d2d8f52f8ab9bc496701b867f6db2ac5c99fb09f44a78227700dacf`  
		Last Modified: Fri, 16 Jan 2026 02:08:39 GMT  
		Size: 26.1 KB (26110 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; arm variant v7

```console
$ docker pull maven@sha256:553dd8c9a66be80b0777a701a7b3f5803efcbfa59a9b3678034eef2399b168b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227160431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4e0c865809e37badd2977b1b5f97e06991030600d759c1abc9b588412a7b20`
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
# Thu, 15 Jan 2026 22:10:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:10:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:10:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:10:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:10:20 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:10:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='fba21763f6553efb65d774f51ab6a347e67a69eb2bb2d26980cdf2ee0f35a6db';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:10:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:10:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:10:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:10:32 GMT
CMD ["jshell"]
# Thu, 15 Jan 2026 22:43:44 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 15 Jan 2026 22:43:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 15 Jan 2026 22:43:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 15 Jan 2026 22:43:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 15 Jan 2026 22:43:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 15 Jan 2026 22:43:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 15 Jan 2026 22:43:48 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:43:48 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Thu, 15 Jan 2026 22:43:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 15 Jan 2026 22:43:48 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 15 Jan 2026 22:43:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 15 Jan 2026 22:43:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 15 Jan 2026 22:43:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 15 Jan 2026 22:43:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a56277e49d30e9a430d5cefad3038f88470a8681e48b806fff292791ed54f1fc`  
		Last Modified: Tue, 13 Jan 2026 06:35:51 GMT  
		Size: 26.9 MB (26853837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30a8db371624c07cd68d5c2a7bd7b64fe8e3fa4cb0f47455d6e8f5a26b5fbf`  
		Last Modified: Thu, 15 Jan 2026 22:10:49 GMT  
		Size: 21.4 MB (21386795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b8a9f0a1fbf7e6143507c1a6a537a1fc297f009965285eef03a76da4f33f62`  
		Last Modified: Thu, 15 Jan 2026 22:10:51 GMT  
		Size: 142.3 MB (142329797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23e9463f5118738fefcc93d49999fbc0b285aac9835c7d3944af6347fc7272c`  
		Last Modified: Thu, 15 Jan 2026 22:10:47 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf8ae01510bc04c2d4b113e5d1d1f1d6ff5462d99e73c27e10411cad69ac781`  
		Last Modified: Thu, 15 Jan 2026 22:10:16 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a63a52d3c2011a4a42b093628f61377c5e05469942b16ec2bd04b8dcfc3467`  
		Last Modified: Thu, 15 Jan 2026 22:44:00 GMT  
		Size: 27.3 MB (27274184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a18f912fae0e2f8074820368e8bb6eead3a73f4ddb800ad76f5a135049fd70`  
		Last Modified: Thu, 15 Jan 2026 22:44:00 GMT  
		Size: 9.3 MB (9312012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c479beb933a0f1eb5bf3ec02d81dd05fca79b017ae59afb7b4c6800d0f66b060`  
		Last Modified: Thu, 15 Jan 2026 22:43:59 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c461fb9d70bbd1393d2e87739f81409ddc3d0553e74b462cc427d437c85d82e8`  
		Last Modified: Thu, 15 Jan 2026 22:43:59 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7619f575f3936c1766fb83da191eb9894a37475513df9873ddd8696a2900f35`  
		Last Modified: Thu, 15 Jan 2026 22:44:00 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:e426c0b6ba10501710aba1ec0e4f35e8fff7e1fb91983f6e4cf53dc64176da75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5009278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f90e6cd04815822523cd1615b1432fa0d54500ed869a20319340dff64552e14`

```dockerfile
```

-	Layers:
	-	`sha256:7b65c23aecee0065b9f6705ad0d356f733885f1f0b51829dd986a37a1176e1e8`  
		Last Modified: Thu, 15 Jan 2026 22:43:59 GMT  
		Size: 5.0 MB (4983005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d651fe74cb0695224ed45e656df72a01abb5353e041d517d23317db306a152d5`  
		Last Modified: Thu, 15 Jan 2026 22:43:59 GMT  
		Size: 26.3 KB (26273 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:005022239023fe3ee57dfe91bf9232305543c0104d83f76d85f0071ae678b3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228636682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7ca7e19b57ec67f0280d0d126f8557d5706d8b7348f111ec4a9e9c7e586f09`
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
# Thu, 15 Jan 2026 22:19:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='fba21763f6553efb65d774f51ab6a347e67a69eb2bb2d26980cdf2ee0f35a6db';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:54 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 02:13:42 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:13:47 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:13:47 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:13:47 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:13:47 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:13:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:13:47 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:13:47 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:13:47 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Fri, 16 Jan 2026 02:13:47 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:13:47 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:13:47 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:13:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:13:47 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:13:47 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e4116d8d6e5320d366443942067a43834d0d58389a0a501596650d87012ed7`  
		Last Modified: Thu, 15 Jan 2026 22:20:11 GMT  
		Size: 24.2 MB (24166525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bab40ec88938a4a1cc05ed8925309e6b395efb6617566b2c9235d71354c7ac`  
		Last Modified: Thu, 15 Jan 2026 22:20:14 GMT  
		Size: 143.7 MB (143681454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d730e5bb3a1e94cebc5dae0690d86ef0d17491e9584717f3318d280ac9bc0012`  
		Last Modified: Thu, 15 Jan 2026 22:20:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b4b65fc380fc87df9d7a19c5abf67e22e913f6f0b56b870b1ee5ca46f5cdf5`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47246db20d86c0080424d7b4de27f68b306395f7c95b5f5a2d5760e3fc20542`  
		Last Modified: Fri, 16 Jan 2026 02:14:00 GMT  
		Size: 22.6 MB (22609065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da2bfbbd308c1ec21e0dff927d400e651b31ef1e7cfe7444d0ffece5cc074f`  
		Last Modified: Fri, 16 Jan 2026 02:14:01 GMT  
		Size: 9.3 MB (9312014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb19f12b4db90e1da26b5db28da75b870be5fb5c4117470665716521a8f56a51`  
		Last Modified: Fri, 16 Jan 2026 02:13:59 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8f4a702e35603c3b96b3bcef89a52b140ff33de3760ab7473749ad5ce91a94`  
		Last Modified: Fri, 16 Jan 2026 02:13:59 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6ca1adbbf2421917f39267e62225bbbfc0b8cea61295ffa0af506c70f8cffa`  
		Last Modified: Fri, 16 Jan 2026 02:14:00 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:29e852a2366e6059880da6ca859eccda3e2d812665729f2add2b4ccade914ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b626b0a219e6f692207e280e16cc62d4efcdcdc9105eaf14136edaf937f3ce`

```dockerfile
```

-	Layers:
	-	`sha256:1779433a3b5be3f171e24c12756aa891625cae82e474501898cf57deb9dab6d3`  
		Last Modified: Fri, 16 Jan 2026 02:13:59 GMT  
		Size: 5.2 MB (5182353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44428ee7f1521ad9f0108e8cfba9a4240b702c3a1f7db670de75e9f2fa6f30d8`  
		Last Modified: Fri, 16 Jan 2026 02:13:59 GMT  
		Size: 26.3 KB (26315 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:9d528debc5cf09f37c215e7a99a2f8616a3fbe6f5635f5566043c69fe70e7eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.8 MB (238847111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c963954bba1342711873fc0731b80da93bd6ed9103fa8b662358d5b4525e62ee`
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
# Thu, 15 Jan 2026 22:15:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:15:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:15:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:15:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:15:19 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:15:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='fba21763f6553efb65d774f51ab6a347e67a69eb2bb2d26980cdf2ee0f35a6db';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:15:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:15:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:15:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:15:36 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 03:51:47 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 03:51:58 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 03:51:58 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:51:58 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:51:58 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 03:51:58 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 03:51:58 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 03:51:58 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 03:51:59 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Fri, 16 Jan 2026 03:52:00 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 03:52:00 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 03:52:00 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 03:52:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 03:52:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 03:52:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935fc6b67e53753b7fd4310688a6745a6f3dc91379aa280218a4dad865d583ec`  
		Last Modified: Thu, 15 Jan 2026 22:16:17 GMT  
		Size: 24.1 MB (24102276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532ae8b10857cc7b1b82413e29e054b1e0b084c932171117faf0e362eef7cd5b`  
		Last Modified: Thu, 15 Jan 2026 22:16:20 GMT  
		Size: 144.5 MB (144534045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd118092dd0ac79e37619e91a13eb24c81776ba95b53b1d5e7afd0a2ecb72f7`  
		Last Modified: Thu, 15 Jan 2026 22:16:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaaabed2317e2357db6deb7b9bbd1c8bbb90968b0f80578ad7fbe536bf1d84f`  
		Last Modified: Thu, 15 Jan 2026 22:16:16 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe142850f28f46a03e5740bdb5e17e7ec171290f31e1f0a760b65102e6c121d`  
		Last Modified: Fri, 16 Jan 2026 03:52:41 GMT  
		Size: 26.6 MB (26588799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64b9bb424f835b8505ddbe526b6be2186008fc2eb09674093d920a1033e1aa8`  
		Last Modified: Fri, 16 Jan 2026 03:52:40 GMT  
		Size: 9.3 MB (9312025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e0583de4ce54359aec5729e0210e7c299faa580e645d0defa2906c77b516dc`  
		Last Modified: Fri, 16 Jan 2026 03:52:40 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612d258641cd1e4b1cf73319b5d538af30ce8fec462d9165c247515ad45acaea`  
		Last Modified: Fri, 16 Jan 2026 03:52:40 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ee202e624a38ca1e565971ea6f1c2e61d0c3300f776ac9c8b20655011ece14`  
		Last Modified: Fri, 16 Jan 2026 03:52:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:518d861a93a8566101a24463f28a5b875d686ac592dc6a3b20b50acd4a47a096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5121509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0901f1a83f26961d4a5407fdb5a55154f9258fb15eea564e23b9c68925dd6dc`

```dockerfile
```

-	Layers:
	-	`sha256:146b258961ed98dbea1944bb06c69d2cfc7f3074f0573b24ba1bf6dd36349954`  
		Last Modified: Fri, 16 Jan 2026 03:52:40 GMT  
		Size: 5.1 MB (5095331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d920113e0e64f275e9ea192b45e3b2690fcf38c7ea71f1d5736075a02b62bf30`  
		Last Modified: Fri, 16 Jan 2026 03:52:40 GMT  
		Size: 26.2 KB (26178 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; riscv64

```console
$ docker pull maven@sha256:06b99c2bab1f82f88894f6d743d496e209fea41572a5b4b04461018f88c47902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233309198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e451e8fa5c2841de151fc4dc7eb7be2fb0503fc5677160b0cf64c2a499dde49`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 06:14:56 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:14:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:14:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:14:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:15:46 GMT
ADD file:8d0655de001e92042901c645c76202ac355acb6fa186561e7344a0829ffd983d in / 
# Tue, 13 Jan 2026 06:15:51 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 18:08:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 19 Jan 2026 18:08:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Jan 2026 18:08:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 19 Jan 2026 18:08:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Jan 2026 18:08:38 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Mon, 19 Jan 2026 18:09:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='fba21763f6553efb65d774f51ab6a347e67a69eb2bb2d26980cdf2ee0f35a6db';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 19 Jan 2026 18:09:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 19 Jan 2026 18:09:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 19 Jan 2026 18:09:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 19 Jan 2026 18:09:45 GMT
CMD ["jshell"]
# Thu, 22 Jan 2026 05:03:02 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Jan 2026 05:03:13 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 22 Jan 2026 05:03:13 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 22 Jan 2026 05:03:13 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 22 Jan 2026 05:03:13 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 22 Jan 2026 05:03:13 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 22 Jan 2026 05:03:13 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 22 Jan 2026 05:03:14 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 22 Jan 2026 05:03:14 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Thu, 22 Jan 2026 05:03:14 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 22 Jan 2026 05:03:14 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 22 Jan 2026 05:03:14 GMT
ARG USER_HOME_DIR=/root
# Thu, 22 Jan 2026 05:03:14 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 22 Jan 2026 05:03:14 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 22 Jan 2026 05:03:14 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f151392858868452ec0f1f8d2947624e8dcdecf23bce587cfbd7c38a3264f9df`  
		Last Modified: Tue, 13 Jan 2026 06:36:06 GMT  
		Size: 31.0 MB (30953090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70a79886c4402a76ef90814a79e96c424cf0e215bb8c0b7d7f29e0d0acc7bd0`  
		Last Modified: Mon, 19 Jan 2026 18:13:27 GMT  
		Size: 20.1 MB (20146747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a8c295fe1c3a29911cd50dce0da34e3d5dc2d7e618f3b8cd6c831d5c381978`  
		Last Modified: Mon, 19 Jan 2026 18:13:45 GMT  
		Size: 141.9 MB (141894150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa31de1d37e05d22a78ed1852d107df54e32c69d609a2fe243bb9cbdfa68b7`  
		Last Modified: Mon, 19 Jan 2026 18:13:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d780e8a0077b6f8e0142791e8bee314e001fc128c3fd04cac1b86f6ca6299231`  
		Last Modified: Mon, 19 Jan 2026 18:13:21 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd0a3bcd4b61c3f5c2a7893c353fd162c0d7f40529e9a3bc7609736947ef652`  
		Last Modified: Thu, 22 Jan 2026 05:06:23 GMT  
		Size: 31.0 MB (30999379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f389f815f64590c4a4105fa07ccb4901a6d2352882046064d473e7bcc7ff28`  
		Last Modified: Thu, 22 Jan 2026 05:06:20 GMT  
		Size: 9.3 MB (9312024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c48339260902842db576c752830847bb960a8b95a612a776b3e2d667de8338c`  
		Last Modified: Thu, 22 Jan 2026 05:06:17 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ff48922fe49772c52823f0d48894c35a63650b4f0adb09a275436426161601`  
		Last Modified: Thu, 22 Jan 2026 05:06:17 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb243bda87757cdd8e009dcc6319ba6447768faae2f9091ee6dd0f461bf146e`  
		Last Modified: Thu, 22 Jan 2026 05:06:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:e0731fc5a1ac31fbfc3ff6bfcae0630028d4b8ba05d4c38f1114ec765afc9c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11b17b4efd013b0126362d098d069a92cdf61d1cab274336e01443e459bd9e7`

```dockerfile
```

-	Layers:
	-	`sha256:283cc7525d01e1946592ff3dbf59db2e527dfad4fe37ddec7022acf1b472fe09`  
		Last Modified: Thu, 22 Jan 2026 05:06:18 GMT  
		Size: 5.1 MB (5146477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5293f685bee7d1d37dbf9d27773f3ce56820f547d65580870dd65a1e5875713e`  
		Last Modified: Thu, 22 Jan 2026 05:06:17 GMT  
		Size: 26.2 KB (26178 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; s390x

```console
$ docker pull maven@sha256:c192c25c028b69941a3c471c21b6ee2e306adeb4636fc3157a609264cda2b929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219885226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16714ee1f607135879dc3ee9a730d18df2d0d532c4e3bfe322a44bcfc93f491`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 06:29:20 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:29:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:29:22 GMT
ADD file:55a7874afa0094b7b4c6edc68b58164a34177fa761bc6e673ddb0c846b91f26f in / 
# Tue, 13 Jan 2026 06:29:22 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:08:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:08:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:08:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:08:50 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:08:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='fba21763f6553efb65d774f51ab6a347e67a69eb2bb2d26980cdf2ee0f35a6db';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:08:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:08:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:08:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:08:55 GMT
CMD ["jshell"]
# Thu, 15 Jan 2026 23:24:34 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:24:37 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 15 Jan 2026 23:24:37 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 15 Jan 2026 23:24:37 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 15 Jan 2026 23:24:37 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 15 Jan 2026 23:24:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 15 Jan 2026 23:24:37 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 15 Jan 2026 23:24:37 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:24:37 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Thu, 15 Jan 2026 23:24:37 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 15 Jan 2026 23:24:37 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 15 Jan 2026 23:24:37 GMT
ARG USER_HOME_DIR=/root
# Thu, 15 Jan 2026 23:24:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 15 Jan 2026 23:24:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 15 Jan 2026 23:24:37 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:88318e41cf944fd93c8b2fdfaeb1378b17ed0e2440ef9811f9820449bf19a6ad`  
		Last Modified: Tue, 13 Jan 2026 06:36:13 GMT  
		Size: 29.9 MB (29909204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf594db9e0a61709897c7efb4b65db2a8edccb2aab36b7a813871b3428f2f62`  
		Last Modified: Thu, 15 Jan 2026 22:09:18 GMT  
		Size: 22.1 MB (22129350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3965cca5a0f76297b56734385760b667704e44243caf5723b423e822f7b4e80`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 134.9 MB (134864285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1347e3bbe0f58930ad0ebd82545acc81a2fe5ab7e1cd5d9658d9f46d6942cff7`  
		Last Modified: Thu, 15 Jan 2026 22:09:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc739c61af7d1eea46106081a4a43dbb9dcb8c553aa956f65b47aca3fa455bc1`  
		Last Modified: Thu, 15 Jan 2026 22:09:17 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa203711ec37c6b12d5dbeb66dab4d88217491267280cb32dbc53f5bcd7b680`  
		Last Modified: Thu, 15 Jan 2026 23:24:56 GMT  
		Size: 23.7 MB (23666566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d47ebcdc357ae8da459e1d7d4516bc1e6868da94fa58f03fcf4685ed593f3ac`  
		Last Modified: Thu, 15 Jan 2026 23:24:56 GMT  
		Size: 9.3 MB (9312016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add40c410c9aac90847b6f6a10196e0d2720c5224d8a9f6673c9234712b00ac8`  
		Last Modified: Thu, 15 Jan 2026 23:24:55 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3757b26dbe067deb0ec8b71f55d74572f9d91b59a57944ca69274f52f6bc4b`  
		Last Modified: Thu, 15 Jan 2026 23:24:56 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc8379cec650e44878ec2bf2bdab501f3bb05b940af14b7e16b7c0218c082c2`  
		Last Modified: Thu, 15 Jan 2026 23:24:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:b1c5b7368b7de16acda0f4301e1fd5d7a29614ca331c2aa2fe33ba7ac757d520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5016268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf896c3dbb7052762b6fa7a64dbd13a6b5d1c75158f8b16bea1ff2b6da6e130`

```dockerfile
```

-	Layers:
	-	`sha256:02a24a37fa80f3c0243b0e638de7ed178d51d9b73ff1b44daa7b9ac2a05f9314`  
		Last Modified: Thu, 15 Jan 2026 23:24:56 GMT  
		Size: 5.0 MB (4990158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0294d89c743ae31ff4be315ba3cd489b77bdfdf336f7e6bc165d79a4b7d004e`  
		Last Modified: Thu, 15 Jan 2026 23:24:55 GMT  
		Size: 26.1 KB (26110 bytes)  
		MIME: application/vnd.in-toto+json
