## `maven:3-eclipse-temurin-17-alpine`

```console
$ docker pull maven@sha256:bd1dcab89d8d8ccf7583f478d80e1ddd354003e20b7f68f7d6db3860e04b45cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:547018ed3770b90ae52b541a57936eafa8de9c692b06fffc453cadc915b186e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181643023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50cf3fe18ea063c1f6685d6615f6f4931a9c59815e00ce2f7c83eb203a8c6b7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Wed, 28 Jan 2026 04:27:15 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Wed, 28 Jan 2026 04:27:16 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 04:27:16 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:27:16 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:27:16 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 04:27:16 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 04:27:16 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 04:27:16 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 04:27:16 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 04:27:16 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 04:27:16 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 04:27:16 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 04:27:16 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 04:27:16 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 04:27:16 GMT
CMD ["mvn"]
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
	-	`sha256:5a950227e6e92366c82b70f3021bd69da9a0d552bc8f55a6e465424be6c3616c`  
		Last Modified: Wed, 28 Jan 2026 04:27:23 GMT  
		Size: 3.4 MB (3417467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2306e96666422af1ba49b1dfb1e564af3f1b409b8dbcf5ae22461a87147ea7`  
		Last Modified: Wed, 28 Jan 2026 04:27:24 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a1d614b29ae835f6ed6e2c93ba7cb1a9da6c3687342f24da29b1d769632fbd`  
		Last Modified: Wed, 28 Jan 2026 04:27:23 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8290a539c6e78f37f55355010f4d92a5e291f7975526ff33e6c5ce1b42366093`  
		Last Modified: Wed, 28 Jan 2026 04:27:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:cc931f4bcc13f1c65288768485fec93dbd956202bfbf4ff09276d0a60afbfe2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1255081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badfb7d669349142561708421e9f75cb0cc14bd9b8f1c5943d18d56018ea06ab`

```dockerfile
```

-	Layers:
	-	`sha256:7b68eb38cc390c8b080e513f7470769af9e347d76186628d738fe188282f854a`  
		Last Modified: Wed, 28 Jan 2026 04:27:23 GMT  
		Size: 1.2 MB (1235732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a78d94e250edee287c7debd8ed2d9f8525798ad26c835fde6e7b56992dedb9a5`  
		Last Modified: Wed, 28 Jan 2026 04:27:23 GMT  
		Size: 19.3 KB (19349 bytes)  
		MIME: application/vnd.in-toto+json
