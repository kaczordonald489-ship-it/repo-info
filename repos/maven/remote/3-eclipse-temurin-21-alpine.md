## `maven:3-eclipse-temurin-21-alpine`

```console
$ docker pull maven@sha256:1ce8199c546899ac4083356d593c73065173c3987fd02041dd981402c1ddbfbb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:c4fff1164b5ee8e2e626f70bc73a5bc8b4733ba5b341ba45a367f5a71274c9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195756199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b198bec798ba47fddb4cb3671ed7219138d38dc9154a0ba7925ba27f36d0ac41`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:11:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:11:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:11:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:11:08 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:11:08 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Wed, 28 Jan 2026 03:11:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 03:11:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:11:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:11:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:11:16 GMT
CMD ["jshell"]
# Wed, 28 Jan 2026 04:25:50 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Wed, 28 Jan 2026 04:25:54 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 04:25:54 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:25:54 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:25:54 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 04:25:54 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 04:25:54 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 04:25:54 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 04:25:54 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 04:25:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 04:25:55 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 04:25:55 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 04:25:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 04:25:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 04:25:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec9d6adc0e2666316744526b3e6b46024e14d211d934176cc82f480f88468a4`  
		Last Modified: Wed, 28 Jan 2026 03:11:33 GMT  
		Size: 21.1 MB (21115198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c077e7f5dd48795d611a90c0aeeabe7b837252b56c8406aac46577cdbcd6bd93`  
		Last Modified: Wed, 28 Jan 2026 03:11:36 GMT  
		Size: 158.1 MB (158102925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654728b92e1362ff81920038e72b4daebd48183a298e8e2a566bc42aad73110c`  
		Last Modified: Wed, 28 Jan 2026 03:11:32 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362be48a2be2658e4295069ddce05198f142098bc57a82f27d2da35698afdc81`  
		Last Modified: Wed, 28 Jan 2026 03:11:32 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46d38c06408b954acb6ce9198c27aef82a260dc2f19408f177ef40b3f8fa24d`  
		Last Modified: Wed, 28 Jan 2026 04:26:01 GMT  
		Size: 3.4 MB (3417502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749d45c969eadd0f47b3c021c38242b0b8378972d6a12e950bde0a3ce23f590d`  
		Last Modified: Wed, 28 Jan 2026 04:26:01 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68785fd36d867873520041fda22babcbe08050674ab685d7332c53481fd38915`  
		Last Modified: Wed, 28 Jan 2026 04:26:01 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c4dd94ff1e3f9eebae8c7efc4d4f44866e2e68b1d3fceba709f84b9aed8be4`  
		Last Modified: Wed, 28 Jan 2026 04:26:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:f19f1c35c685c9c7741e7b54e0b670663000217b0e619ebf725cc831100e13ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1258181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232aeedb6d6ffef75c8cf5120073bca56480f5833dc6ec8f2b1801642e024614`

```dockerfile
```

-	Layers:
	-	`sha256:378aa34e53d84b4933ee7cd6e0a5c14bc3926a5aa843e7d6760dee8505bc8a23`  
		Last Modified: Wed, 28 Jan 2026 04:26:01 GMT  
		Size: 1.2 MB (1238834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d291ca29e5b14bd0c6ee62087c4de07ba09cf9a118fa563cf057ebae7fb23fe`  
		Last Modified: Wed, 28 Jan 2026 04:26:01 GMT  
		Size: 19.3 KB (19347 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a426355ec4906101fdc07fcf3e724bb3d964d0f58097b96648bd27a8f9fbb524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 MB (194195660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb186cbd41a0fa65c3406e45d9ccf310c4db699c940960a19baa05f2b959e96`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 02:56:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:56:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 02:56:37 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 02:56:37 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Wed, 28 Jan 2026 02:56:45 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 02:56:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 02:56:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:56:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:47 GMT
CMD ["jshell"]
# Wed, 28 Jan 2026 04:52:00 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Wed, 28 Jan 2026 04:52:00 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 04:52:00 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:52:00 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:52:00 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 04:52:00 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 04:52:00 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 04:52:00 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 04:52:00 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 04:52:00 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 04:52:00 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 04:52:00 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 04:52:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 04:52:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 04:52:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d237401997b4e6d77e1a6cbf3006b196170369b2872d0a2fba9f845ce7cfeeb5`  
		Last Modified: Wed, 28 Jan 2026 02:57:03 GMT  
		Size: 21.2 MB (21166024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bf8a9ded26681fc49549c27c20edd4b88472a3ca476e9a7c4ebf9d58174315`  
		Last Modified: Wed, 28 Jan 2026 02:57:06 GMT  
		Size: 156.1 MB (156097479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9c000864d8ab5dc2884668139fc08c3b2e6cc3aaa69eacd03144943b90354f`  
		Last Modified: Wed, 28 Jan 2026 02:57:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e39acec808282ee08cd7b6292bf85d7b6775f69ca5e3bb0eb617e09e97bb94d`  
		Last Modified: Wed, 28 Jan 2026 02:57:02 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1614c0aca7bef95dc3a482487482c2ae71aa6184eb31a9fc85a3cdbb21cca26`  
		Last Modified: Wed, 28 Jan 2026 04:52:08 GMT  
		Size: 3.5 MB (3476940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77d30146d620550ce267e45bc3da44f4e582b1a53c7e46a9aff655f289a05fa`  
		Last Modified: Wed, 28 Jan 2026 04:52:08 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1485bbcf25b635306d8ea9ab754f681c289bf017a8e94f23e32278d0a24b032e`  
		Last Modified: Wed, 28 Jan 2026 04:52:08 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3779edeb592b69c53d847ac0b84dc264150a3c869bb344bed6edb752ddad79`  
		Last Modified: Wed, 28 Jan 2026 04:52:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:baa1a8349d58fab04c34c2197851823902e7e16b0ea12bd1f250580c89556546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1408316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1fffb5e761736af37b57473087cccb421b291a6ac563e3cf6855ebc8d9dcf5`

```dockerfile
```

-	Layers:
	-	`sha256:32dcac52d7dd64ababc62ae7d60b9680360f252570078aeae3ee64cca47d1b11`  
		Last Modified: Wed, 28 Jan 2026 04:52:08 GMT  
		Size: 1.4 MB (1388836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2423771ff31bec75e9d7c4e68e1c41b007a011270a936dcfd9bf6a32cafb03f7`  
		Last Modified: Wed, 28 Jan 2026 04:52:08 GMT  
		Size: 19.5 KB (19480 bytes)  
		MIME: application/vnd.in-toto+json
