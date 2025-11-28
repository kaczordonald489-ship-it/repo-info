## `tomcat:10-jre25-temurin-noble`

```console
$ docker pull tomcat@sha256:db18f9e1232891a13dc74d02577b8fceaa7d1fcc8152fa18f1b649e68dc6c801
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:10-jre25-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:0a989a87d074154d27c08bf187c2814af440746d68b5e890b94c12e3c3506205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118226367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265f4ee1189fdfb47a0ff49cf199e94e684c350c6c4b6e1cd6f526bc8f8e1ad3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:22:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:22:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:22:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:22:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:22:15 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 13 Nov 2025 23:22:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        riscv64)          ESUM='31af8beb1071d499bf4d55d4709aef49055e854c3f6b505d01296f947fde3b8f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:22:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:22:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:22:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:22:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 14 Nov 2025 01:22:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:22:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 14 Nov 2025 01:22:57 GMT
WORKDIR /usr/local/tomcat
# Fri, 14 Nov 2025 01:22:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:22:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:22:57 GMT
ENV TOMCAT_MAJOR=10
# Fri, 14 Nov 2025 01:22:57 GMT
ENV TOMCAT_VERSION=10.1.49
# Fri, 14 Nov 2025 01:22:57 GMT
ENV TOMCAT_SHA512=a46c8e37d4767b56a16dbdd8e81b80f25ad2edd5fba68b5099b9165cfffbe32bc923a601db8bb5cba50e8b1047a7906eb8c30ca176e1c0b8dfd85fbb9c54c6c2
# Fri, 14 Nov 2025 01:23:58 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 14 Nov 2025 01:24:04 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:24:04 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 14 Nov 2025 01:24:04 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 01:24:04 GMT
ENTRYPOINT []
# Fri, 14 Nov 2025 01:24:04 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb04f8b15cf295a8c19ea7266cea595263d427367c21fff5945243e2dbadb7f`  
		Last Modified: Thu, 13 Nov 2025 23:22:54 GMT  
		Size: 11.5 MB (11475255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62e45ce99cf84344c8584d913b5e93f8c44f0e2078db9c0c365d9e3bc17ac7f`  
		Last Modified: Thu, 13 Nov 2025 23:23:00 GMT  
		Size: 62.7 MB (62719763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b71810e376dd30df27d0d1b5bc7477690109fdcf871ed098d51ba389ce04d2`  
		Last Modified: Thu, 13 Nov 2025 23:22:52 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d7067fe9af1414daf78bcc31a7ae57cc0556901dd0258dd5c5f42bf7b137b5`  
		Last Modified: Fri, 14 Nov 2025 01:23:17 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5026335c9a8717904a4413afc69bafa4bbeaef9e6b9ddddf182a41e45a6a89`  
		Last Modified: Fri, 14 Nov 2025 01:24:18 GMT  
		Size: 14.1 MB (14096618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0755b3a77288e7fc9210049d233abdd26cdb9b1d1662ded936d87dea53580dda`  
		Last Modified: Fri, 14 Nov 2025 01:24:17 GMT  
		Size: 207.5 KB (207526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:95c84b68434e534dcf243915547d75c5487fac85278f0999807596adbe797f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb482949d967da09f273731df66217950e44c341b60c6a54fbd4c078402d314d`

```dockerfile
```

-	Layers:
	-	`sha256:61c490bc978e0497f0b7759f2742e7901bd9646099ee66cc5bc8037abea0a3e6`  
		Last Modified: Fri, 14 Nov 2025 03:32:43 GMT  
		Size: 3.1 MB (3129168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d7307db8239e69846cbb281406ffba6b5511f6190075e5b34a041767a95fb82`  
		Last Modified: Fri, 14 Nov 2025 03:32:44 GMT  
		Size: 23.1 KB (23098 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre25-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:81673fbe1e7c699f17f078f0442a54435083704b64d099aab22586b15ed0ac4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116310886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f596e8c73b870ec0da9b2edcf259824a5d85e077400d8b499e12aa861067f75c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:44 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 13 Nov 2025 23:22:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        riscv64)          ESUM='31af8beb1071d499bf4d55d4709aef49055e854c3f6b505d01296f947fde3b8f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:22:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:22:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:22:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:39:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 14 Nov 2025 01:39:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:39:50 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 14 Nov 2025 01:39:50 GMT
WORKDIR /usr/local/tomcat
# Fri, 14 Nov 2025 01:39:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:39:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:39:50 GMT
ENV TOMCAT_MAJOR=10
# Fri, 14 Nov 2025 01:39:50 GMT
ENV TOMCAT_VERSION=10.1.49
# Fri, 14 Nov 2025 01:39:50 GMT
ENV TOMCAT_SHA512=a46c8e37d4767b56a16dbdd8e81b80f25ad2edd5fba68b5099b9165cfffbe32bc923a601db8bb5cba50e8b1047a7906eb8c30ca176e1c0b8dfd85fbb9c54c6c2
# Fri, 14 Nov 2025 01:39:50 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 14 Nov 2025 01:39:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:39:57 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 14 Nov 2025 01:39:57 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 01:39:57 GMT
ENTRYPOINT []
# Fri, 14 Nov 2025 01:39:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610462493f8365c1c50dc1e88be08516bacca1bf3951a94bd438b3f5a433bd80`  
		Last Modified: Thu, 13 Nov 2025 23:22:25 GMT  
		Size: 11.5 MB (11469621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e2c5c245a804374ef8046978fc5268ef7cb3d113fb59d8fb954217f0f62e6`  
		Last Modified: Thu, 13 Nov 2025 23:22:27 GMT  
		Size: 61.7 MB (61670007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435f2e942c2099b67bb826915c859b97f9b227a2209b4fa3e4ad1c47daf2fbe3`  
		Last Modified: Thu, 13 Nov 2025 23:22:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65388ba42c324ee417a49166b4ed4e2ee0c4a5ed8804f1b9d887844bdbe52826`  
		Last Modified: Fri, 14 Nov 2025 01:40:11 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a95c53ed35ffeab76bc8a3a7b9696f3824d052d5b031aebf3a9d47734578ce`  
		Last Modified: Fri, 14 Nov 2025 01:40:12 GMT  
		Size: 14.1 MB (14099595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eb09b5da7bebc3eacebf5915a54745dfceff15ada03932f31fc2bee8681ac6`  
		Last Modified: Fri, 14 Nov 2025 01:40:11 GMT  
		Size: 207.2 KB (207189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:a99820b6c6f01d80b118ca56e364225bd88b64772f76c2cea2fdc158947345e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b46e6975fea9edb44199ef8be91e50d2d71c57fa4b7b0ea0be8d86b88c407e3`

```dockerfile
```

-	Layers:
	-	`sha256:fbf58dcfc16f80c69f999ec29e26a28554f5d1ebeb27d8fcb55cc1c031c2910a`  
		Last Modified: Fri, 14 Nov 2025 03:32:48 GMT  
		Size: 3.1 MB (3129678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdc80bd91ff32edd0e8cb61ac62505e433257fc7eeb81e12d967305c44a0c314`  
		Last Modified: Fri, 14 Nov 2025 03:32:49 GMT  
		Size: 23.3 KB (23318 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre25-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:05a5d52ce181922a8e224f640f617dce4afb16aff7df31ff4b5ac2dcc61d8fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122864850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb57ba18b9856c0f763a3c68bd772eec3c6fa787069abbe9700010e3a854735c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:35:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:35:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:35:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:42 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 13 Nov 2025 23:36:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        riscv64)          ESUM='31af8beb1071d499bf4d55d4709aef49055e854c3f6b505d01296f947fde3b8f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:36:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:36:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:36:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 08:17:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 14 Nov 2025 08:17:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 08:17:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 14 Nov 2025 08:17:39 GMT
WORKDIR /usr/local/tomcat
# Fri, 14 Nov 2025 08:17:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 08:17:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 08:17:39 GMT
ENV TOMCAT_MAJOR=10
# Fri, 14 Nov 2025 08:17:39 GMT
ENV TOMCAT_VERSION=10.1.49
# Fri, 14 Nov 2025 08:17:39 GMT
ENV TOMCAT_SHA512=a46c8e37d4767b56a16dbdd8e81b80f25ad2edd5fba68b5099b9165cfffbe32bc923a601db8bb5cba50e8b1047a7906eb8c30ca176e1c0b8dfd85fbb9c54c6c2
# Fri, 14 Nov 2025 08:23:43 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 14 Nov 2025 08:23:50 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 08:23:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 14 Nov 2025 08:23:51 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 08:23:51 GMT
ENTRYPOINT []
# Fri, 14 Nov 2025 08:23:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8edbdc2eb6ad00fa254d7f0d96005b9ef7826fc43f9d27ce0d4f43a523e9f9d`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 12.1 MB (12051474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618687c61ca530302b8b6ccfced53e64007eb3efbdcc3cdb4c6a635e1b919d65`  
		Last Modified: Thu, 13 Nov 2025 23:36:58 GMT  
		Size: 62.2 MB (62155111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cdace3c43abbe478c395bcd7d9c69f4a68a04222287a5c4f24adb525af42e3`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b49c20bc56dd35536fc76dc0b0cabc87df6fef841087227859d69a3889c049`  
		Last Modified: Fri, 14 Nov 2025 08:18:16 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd64e524fd6d76d7698e55aa19e050249a3d758229c99d451125e423a2cc20f`  
		Last Modified: Fri, 14 Nov 2025 08:24:18 GMT  
		Size: 14.1 MB (14112583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd4b2235298f3f99cbfdb30fbe866f0d0da8bd69924e81a4b7cbb46ee3d17ef`  
		Last Modified: Fri, 14 Nov 2025 08:24:17 GMT  
		Size: 238.7 KB (238740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:4982414f3a33d5db826410f0352a18a226e34e283680fd34d7a9c2c2960b2326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10230caa1ffd197062b119792596986cc829c1bc80b8272c0fbcbaadaf1d7d42`

```dockerfile
```

-	Layers:
	-	`sha256:a4c27871ebc11635d503e7d74419b7151f69efe2b3036bc473d92c6985f07bce`  
		Last Modified: Fri, 14 Nov 2025 09:29:36 GMT  
		Size: 3.1 MB (3132495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:872ed602e980a325440c28832e9fd1d69b0f1754e137604b85858065e9a03e55`  
		Last Modified: Fri, 14 Nov 2025 09:29:37 GMT  
		Size: 23.2 KB (23186 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre25-temurin-noble` - linux; riscv64

```console
$ docker pull tomcat@sha256:a8b6c1b4d815d8c0cd8cf8c0d4b98f7f4f80452ebb397623180f6878d90b8c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118461856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286193b76723a012278b2339147d556aabfc36ed9999dc77cb6ced1154ecec09`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 16 Oct 2025 19:53:04 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:53:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:53:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:53:05 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:53:45 GMT
ADD file:6c2a12ec42d9e6c7e02041a8483a3a93ab9b91131ca66ecb93506ba161a4909d in / 
# Thu, 16 Oct 2025 19:53:49 GMT
CMD ["/bin/bash"]
# Sat, 15 Nov 2025 13:35:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 15 Nov 2025 13:35:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 13:35:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 15 Nov 2025 13:35:58 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Nov 2025 13:35:58 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 15 Nov 2025 13:38:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        riscv64)          ESUM='31af8beb1071d499bf4d55d4709aef49055e854c3f6b505d01296f947fde3b8f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 15 Nov 2025 13:38:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 15 Nov 2025 13:38:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 15 Nov 2025 13:38:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 15 Nov 2025 23:33:30 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 15 Nov 2025 23:33:30 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 23:33:30 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 15 Nov 2025 23:33:30 GMT
WORKDIR /usr/local/tomcat
# Sat, 15 Nov 2025 23:33:30 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 15 Nov 2025 23:33:30 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 15 Nov 2025 23:33:30 GMT
ENV TOMCAT_MAJOR=10
# Sat, 15 Nov 2025 23:33:30 GMT
ENV TOMCAT_VERSION=10.1.49
# Sat, 15 Nov 2025 23:33:30 GMT
ENV TOMCAT_SHA512=a46c8e37d4767b56a16dbdd8e81b80f25ad2edd5fba68b5099b9165cfffbe32bc923a601db8bb5cba50e8b1047a7906eb8c30ca176e1c0b8dfd85fbb9c54c6c2
# Sat, 15 Nov 2025 23:42:52 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 15 Nov 2025 23:43:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Nov 2025 23:43:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 15 Nov 2025 23:43:39 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 15 Nov 2025 23:43:39 GMT
ENTRYPOINT []
# Sat, 15 Nov 2025 23:43:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4f36e1b0a2cc427e5979b49608ef4e52795313f083fdc941cab616d5ab2b861b`  
		Last Modified: Sat, 15 Nov 2025 10:03:37 GMT  
		Size: 31.0 MB (30952148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad30e666e522c77c634be22adbcd51d11d506e0ff46a96bf14acfb7730528b3`  
		Last Modified: Sat, 15 Nov 2025 13:41:09 GMT  
		Size: 11.6 MB (11570222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264da94fe7b5871246212863f61001aa2a1a4ea4918261b96a2f744c1b24448e`  
		Last Modified: Sat, 15 Nov 2025 13:41:11 GMT  
		Size: 61.4 MB (61443925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dd40c61993805a82d0724c36ff75fded841293a43e53fa9ba51a606881eed3`  
		Last Modified: Sat, 15 Nov 2025 13:41:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a4ff0cdeb0b1d886482822b55b00b78718757afec502043c163ea8d0c63942`  
		Last Modified: Sat, 15 Nov 2025 23:36:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89adaedcd6e6a3737500e38bb6ac264eb1d3fd4ee74be55051b82679f14923`  
		Last Modified: Sat, 15 Nov 2025 23:45:32 GMT  
		Size: 14.3 MB (14282874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb56000d72cc044d5277db00873ec238a7fd958f84e1541e278ad8f4d3a71d06`  
		Last Modified: Sat, 15 Nov 2025 23:45:31 GMT  
		Size: 210.2 KB (210170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:257f25ca6e95d256a849a43c6ceeacc097f44402fabcdfae557ebac4d7b881f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3144377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8154d221a2416b34692d96d1a06c4636764bc2670510b8794dcf1db50ca207ec`

```dockerfile
```

-	Layers:
	-	`sha256:9d47e5d618bf49e18d5d44f089155bcdfdd51d2a780839b7b25b37aa3696b9ca`  
		Last Modified: Sun, 16 Nov 2025 00:29:12 GMT  
		Size: 3.1 MB (3121191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60ada6bcd8b83441d0b61671313b80152faa19e1ac9089cb698873221fd4cc5`  
		Last Modified: Sun, 16 Nov 2025 00:29:13 GMT  
		Size: 23.2 KB (23186 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre25-temurin-noble` - linux; s390x

```console
$ docker pull tomcat@sha256:aad1795a5c9c8347a44a1ba942bf0c1066ae22f09fd42767ddddb935f6f01368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116339805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f417367b4bc5764dbb643b8f565f44505c03b07d117dbe073a61478126d833eb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:14 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:16 GMT
ADD file:f7335d462150d31c3c91b13ccd3e927bc9a1b9c6664fa8905ccf68bbe3d86cd3 in / 
# Thu, 16 Oct 2025 19:25:16 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:12:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:12:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:12:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:12:30 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 13 Nov 2025 23:12:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        riscv64)          ESUM='31af8beb1071d499bf4d55d4709aef49055e854c3f6b505d01296f947fde3b8f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:12:44 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:12:44 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:12:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:43:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 14 Nov 2025 01:43:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:43:15 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 14 Nov 2025 01:43:15 GMT
WORKDIR /usr/local/tomcat
# Fri, 14 Nov 2025 01:43:15 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:43:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:43:15 GMT
ENV TOMCAT_MAJOR=10
# Fri, 14 Nov 2025 01:43:15 GMT
ENV TOMCAT_VERSION=10.1.49
# Fri, 14 Nov 2025 01:43:15 GMT
ENV TOMCAT_SHA512=a46c8e37d4767b56a16dbdd8e81b80f25ad2edd5fba68b5099b9165cfffbe32bc923a601db8bb5cba50e8b1047a7906eb8c30ca176e1c0b8dfd85fbb9c54c6c2
# Fri, 14 Nov 2025 01:44:55 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 14 Nov 2025 01:44:58 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:44:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 14 Nov 2025 01:44:59 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 01:44:59 GMT
ENTRYPOINT []
# Fri, 14 Nov 2025 01:44:59 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7d5b0205a5ff16c2b58f20a113b5eb9a80393a644df077beab5d90635153dc66`  
		Last Modified: Thu, 16 Oct 2025 21:17:39 GMT  
		Size: 29.9 MB (29907597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ae3655c49748dd7586f4e8197b4096b5d7761475686d6724d5820fa897fde1`  
		Last Modified: Thu, 13 Nov 2025 23:13:10 GMT  
		Size: 11.8 MB (11768275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c2f211da77423ed978b6d442ea015da5f18d05e20c7d8e017728cd862cbccd`  
		Last Modified: Thu, 13 Nov 2025 23:13:15 GMT  
		Size: 60.3 MB (60340591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb78c2802ebfd84ea2a01ff1c27c1759a20e174b87839d9afb9d2c0ed76a7c4`  
		Last Modified: Thu, 13 Nov 2025 23:13:07 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab77246e523184b742d665bf7b577e5cfabd54fc6c3bd402c8ff8a447772e622`  
		Last Modified: Fri, 14 Nov 2025 01:43:40 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebd40f0c2c34994d7e16cb1bf5b0dabc89d341bc63b6e23bd3a074e0b9a68c1`  
		Last Modified: Fri, 14 Nov 2025 01:45:16 GMT  
		Size: 14.1 MB (14105773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2665bb53dffd4a5dd36e9e46d0db5f82f56b5f4bacb43af4f2553995302d742`  
		Last Modified: Fri, 14 Nov 2025 01:45:15 GMT  
		Size: 215.1 KB (215052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:c589cff66655635097ee87b9cac56061f0e61a9e11e0b60a9598481d3852cb84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1cd8c521cb73d21511865628007e5ab61fde56fd245ee84f464af444f41413d`

```dockerfile
```

-	Layers:
	-	`sha256:ece14fbf11c00cf458fd7039ec340896a24b36f818243e959514aeecea03a952`  
		Last Modified: Fri, 14 Nov 2025 03:33:01 GMT  
		Size: 3.1 MB (3130765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e79b75d5d9a64ed2df4f4f95e95c747d442dfc8e108bc0e3402297662f442768`  
		Last Modified: Fri, 14 Nov 2025 03:33:02 GMT  
		Size: 23.1 KB (23098 bytes)  
		MIME: application/vnd.in-toto+json
