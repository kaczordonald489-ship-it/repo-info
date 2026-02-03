## `maven:3-eclipse-temurin-11-alpine`

```console
$ docker pull maven@sha256:0bf160595f3e6cb1bffc274e915118d0a0ff0493143bb21282ad53770b0a176d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:0a9d4e2408698e582b41351787945ae602d8237cb6a079a71ddd4601082751a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173320120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd09ec04e00d392521e9daf0d8f0ea3638ffff9cf4af2223d7c75316df8eea0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
ENV JAVA_VERSION=jdk-11.0.29+7
# Wed, 28 Jan 2026 03:03:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c7b58655ffde7b5e6fce4a32fdcd21be5745b3bb64ee2bc723fcf55eae720ebe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 03:03:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:03:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:03:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:03:08 GMT
CMD ["jshell"]
# Wed, 28 Jan 2026 04:27:06 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Wed, 28 Jan 2026 04:27:10 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 04:27:10 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:27:10 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:27:10 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 04:27:10 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 04:27:10 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 04:27:10 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 04:27:10 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 04:27:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 04:27:11 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 04:27:11 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 04:27:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 04:27:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 04:27:11 GMT
CMD ["mvn"]
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
	-	`sha256:fa6a695983e73627cb4159100da7fbc662b3727706c392e8ffd27d64bf481c2b`  
		Last Modified: Wed, 28 Jan 2026 03:03:26 GMT  
		Size: 140.1 MB (140102382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea14b20ff7de2eebe5038d26444bbb80a02022f13817302f2fe29c8cd0628cda`  
		Last Modified: Wed, 28 Jan 2026 03:03:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7aeb83382b9b7198bf601d2ec81a192e153f4aa03d11277731a45d81e1f902`  
		Last Modified: Wed, 28 Jan 2026 03:03:22 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9742d3668caecd8b1da7623f5df750e3fa503a258d3ab87c18b439acbab3db1`  
		Last Modified: Wed, 28 Jan 2026 04:27:18 GMT  
		Size: 3.8 MB (3803153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb87d67e84097f571b93bc8fad52d214404c59db58550c7ac3c37e2478034eab`  
		Last Modified: Wed, 28 Jan 2026 04:27:18 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e722e7b52f1284ff1cac0a0ec0d0136406c3f8a98d9357fb5dc9925e188372b3`  
		Last Modified: Wed, 28 Jan 2026 04:27:18 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4677c550a32936c51a4eb04d1995a03c2da389f120af6aef73cddd07b8e83a08`  
		Last Modified: Wed, 28 Jan 2026 04:27:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:acf9228e20814c3d709243914cc307c8e716c326e30b069fc23642ddf210d20b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1156401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a804980bbd9d8872fbeebf79cd94428c6c295b6a9ee1149e748710618a3eca`

```dockerfile
```

-	Layers:
	-	`sha256:1745e33ae9c068f264c72fb7078536455e626cff414904b71ae4fa57e6dfe000`  
		Last Modified: Wed, 28 Jan 2026 04:27:18 GMT  
		Size: 1.1 MB (1137054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eb2753c06e5d89f9122b9cf4063d43597dcb1c42e8cd17c5c721ce95d548983`  
		Last Modified: Wed, 28 Jan 2026 04:27:18 GMT  
		Size: 19.3 KB (19347 bytes)  
		MIME: application/vnd.in-toto+json
