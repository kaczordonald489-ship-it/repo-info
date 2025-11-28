## `xwiki:lts-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:ad07fa8ef0572e8da28656d4be4b8f5b18465c01f6e66f29976b0643d16f9d73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:9c2f8bc4eb295d5ea7a514601f22086ef680cc31039b7a48303bbceaf23bf1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.2 MB (623188318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b497e1d9c334011e97abc9e3cfa8454ee28b41b2905f77b61e8adbe3f037b601`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

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
# Thu, 13 Nov 2025 23:20:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:24:38 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 14 Nov 2025 01:24:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:24:38 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 14 Nov 2025 01:24:38 GMT
WORKDIR /usr/local/tomcat
# Fri, 14 Nov 2025 01:24:38 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:24:38 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:24:38 GMT
ENV TOMCAT_MAJOR=9
# Fri, 14 Nov 2025 01:24:38 GMT
ENV TOMCAT_VERSION=9.0.112
# Fri, 14 Nov 2025 01:24:38 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Fri, 14 Nov 2025 01:24:38 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 14 Nov 2025 01:24:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:24:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 14 Nov 2025 01:24:45 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 01:24:45 GMT
ENTRYPOINT []
# Fri, 14 Nov 2025 01:24:45 GMT
CMD ["catalina.sh" "run"]
# Fri, 14 Nov 2025 02:22:12 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 14 Nov 2025 02:22:12 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 14 Nov 2025 02:22:12 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 14 Nov 2025 02:22:12 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 14 Nov 2025 02:22:12 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 14 Nov 2025 02:22:12 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 14 Nov 2025 02:22:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 02:22:12 GMT
ENV XWIKI_VERSION=16.10.14
# Fri, 14 Nov 2025 02:22:12 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.14
# Fri, 14 Nov 2025 02:22:12 GMT
ENV XWIKI_DOWNLOAD_SHA256=2d617d4f05206866187f60098d3f7e4116d83659d89f7b266d1b635ddc32f0fc
# Fri, 14 Nov 2025 02:22:32 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 14 Nov 2025 02:22:32 GMT
ENV MARIADB_JDBC_VERSION=3.5.6
# Fri, 14 Nov 2025 02:22:32 GMT
ENV MARIADB_JDBC_SHA256=a129703efd7b0f334564d46753de999f09b3a361489a2eb647e6020390981cc9
# Fri, 14 Nov 2025 02:22:32 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.6
# Fri, 14 Nov 2025 02:22:32 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.6.jar
# Fri, 14 Nov 2025 02:22:32 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.6.jar
# Fri, 14 Nov 2025 02:22:32 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 14 Nov 2025 02:22:32 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 14 Nov 2025 02:22:32 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 14 Nov 2025 02:22:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 14 Nov 2025 02:22:32 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 02:22:32 GMT
VOLUME [/usr/local/xwiki]
# Fri, 14 Nov 2025 02:22:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 02:22:32 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f878172f1ac3121519dd1795c821097cda557a10d8ac4526d248f9fe1738b942`  
		Last Modified: Thu, 13 Nov 2025 23:21:35 GMT  
		Size: 17.0 MB (16972399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b92fa77023f1881e077b68fb149d30aade157324fdc1181dacf19b57e1313b9`  
		Last Modified: Thu, 13 Nov 2025 23:22:21 GMT  
		Size: 53.0 MB (52978772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1321ce5b3e3ab111f1a88d34df69fbf748e96e3338e9f3d403b062e3e26d99d9`  
		Last Modified: Thu, 13 Nov 2025 23:22:07 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0e444f3c26062a0908ef59f39a3b8894225b2faef3d5b877c11441d3a52713`  
		Last Modified: Thu, 13 Nov 2025 23:22:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbea165fc4ff35146a8adaa801544eedc2fcf0f1d703505de0850ab9b1bb227`  
		Last Modified: Fri, 14 Nov 2025 01:25:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfca27531378f413da530fbbc6091094dfca85a6098450b921bae0110a5bd9d`  
		Last Modified: Fri, 14 Nov 2025 01:25:00 GMT  
		Size: 13.7 MB (13731896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2da11d900d8bf5c88d6309f7a33318bc006a9518a019c65afef83404d618bc0`  
		Last Modified: Fri, 14 Nov 2025 01:24:59 GMT  
		Size: 224.7 KB (224725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cc2a1af2b5a2a0f647cb6545b073f9b831bdb0401f4d7a2d4c766495c3bf03`  
		Last Modified: Fri, 14 Nov 2025 07:44:56 GMT  
		Size: 191.2 MB (191182071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911712c21c09105f739aebba74e1bbb5c9f88613851da5812bbff43e8f261227`  
		Last Modified: Fri, 14 Nov 2025 07:45:12 GMT  
		Size: 317.7 MB (317653414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2986a46f1eca0f1c283ea6e57208bef5dd26a2d9c86bab190537faac349f9630`  
		Last Modified: Fri, 14 Nov 2025 02:23:18 GMT  
		Size: 705.0 KB (704960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b784e1270c1928be93c51b6de454353f3c782499bc047670f3852be1332a143`  
		Last Modified: Fri, 14 Nov 2025 02:23:18 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4507320279f39cbf5e163b275fba33bdfd2b9ecb1c08cb453f7175a6de005c8c`  
		Last Modified: Fri, 14 Nov 2025 02:23:18 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2741f145d99674a6433c2710e5f66747ebdf4281ed2f9d9fc40d6c29a0f966`  
		Last Modified: Fri, 14 Nov 2025 02:23:18 GMT  
		Size: 6.6 KB (6624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7bc7397dbc2eb009f9eeb605f00b3e9a7ac7d817ab72c8badc5b68586ed8cc`  
		Last Modified: Fri, 14 Nov 2025 02:23:19 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:ad8c2d43d345fcc556c3eaf093a95393e68de812ca202c17fd9a192af510b97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9150002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052c571de3c6fad46d2c852072907870240d2f81a6142bebfd8118808cce9b14`

```dockerfile
```

-	Layers:
	-	`sha256:40d62ad33b27024643de29c4bf39c27cf5021ace2a222710b1da6d58b27c5807`  
		Last Modified: Fri, 14 Nov 2025 04:07:36 GMT  
		Size: 9.1 MB (9109553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b93b6e2e917388ddd9427fd4f896d5b06c4088e9b6c699cb9f734a9babeec374`  
		Last Modified: Fri, 14 Nov 2025 04:07:37 GMT  
		Size: 40.4 KB (40449 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:337dfb734df3a6e2d2cf5cf74f572d353cca72a51d48fdee90274ba18d7c9bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.2 MB (619188250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c9f9040b5b88fd4b34c76eb15abf99590010cceba50e6e3d157f25ac84ca70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

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
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:41:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 14 Nov 2025 01:41:09 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:41:09 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 14 Nov 2025 01:41:09 GMT
WORKDIR /usr/local/tomcat
# Fri, 14 Nov 2025 01:41:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:41:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:41:09 GMT
ENV TOMCAT_MAJOR=9
# Fri, 14 Nov 2025 01:41:09 GMT
ENV TOMCAT_VERSION=9.0.112
# Fri, 14 Nov 2025 01:41:09 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Fri, 14 Nov 2025 01:41:11 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 14 Nov 2025 01:41:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:41:22 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 14 Nov 2025 01:41:22 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 01:41:22 GMT
ENTRYPOINT []
# Fri, 14 Nov 2025 01:41:22 GMT
CMD ["catalina.sh" "run"]
# Fri, 14 Nov 2025 02:26:16 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 14 Nov 2025 02:26:16 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 14 Nov 2025 02:26:16 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 14 Nov 2025 02:26:16 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 14 Nov 2025 02:26:16 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 14 Nov 2025 02:26:16 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 14 Nov 2025 02:26:16 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 02:26:16 GMT
ENV XWIKI_VERSION=16.10.14
# Fri, 14 Nov 2025 02:26:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.14
# Fri, 14 Nov 2025 02:26:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=2d617d4f05206866187f60098d3f7e4116d83659d89f7b266d1b635ddc32f0fc
# Fri, 14 Nov 2025 02:26:36 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 14 Nov 2025 02:26:36 GMT
ENV MARIADB_JDBC_VERSION=3.5.6
# Fri, 14 Nov 2025 02:26:36 GMT
ENV MARIADB_JDBC_SHA256=a129703efd7b0f334564d46753de999f09b3a361489a2eb647e6020390981cc9
# Fri, 14 Nov 2025 02:26:36 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.6
# Fri, 14 Nov 2025 02:26:36 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.6.jar
# Fri, 14 Nov 2025 02:26:36 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.6.jar
# Fri, 14 Nov 2025 02:26:36 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 14 Nov 2025 02:26:36 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 14 Nov 2025 02:26:36 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 14 Nov 2025 02:26:37 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 14 Nov 2025 02:26:37 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 02:26:37 GMT
VOLUME [/usr/local/xwiki]
# Fri, 14 Nov 2025 02:26:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 02:26:37 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e052f7b40adf3e6b8172dd9f3385e9469f4dcfbea63c3518933c4239901bcc`  
		Last Modified: Thu, 13 Nov 2025 23:21:05 GMT  
		Size: 17.0 MB (16989179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07df04fa133324a49bb96c54d2b02e9d4463a8a2ba701459d09aac3d20984431`  
		Last Modified: Thu, 13 Nov 2025 23:21:47 GMT  
		Size: 52.1 MB (52148635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3225358e001b3b4abaaa7eddcf1179402e80dd7e5627430be9ec054cf2e309`  
		Last Modified: Thu, 13 Nov 2025 23:21:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Thu, 13 Nov 2025 23:21:42 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d0874a2b3978833b9ffcbd93fd9270f7311b8ed83f76d0f52485dd4424f96`  
		Last Modified: Fri, 14 Nov 2025 01:41:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4b7077ce17e0a1b9281156f6a644fa9a8e5e38797e44d0a0dd1aaeb12bce98`  
		Last Modified: Fri, 14 Nov 2025 01:41:44 GMT  
		Size: 13.7 MB (13740078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5491fceb91f2532aadb2d169c4176e6237efcc85178e19ee3bb52037f924c6f`  
		Last Modified: Fri, 14 Nov 2025 01:41:38 GMT  
		Size: 225.2 KB (225176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab59b70ff3ac9bdf4eb34f609bfecb17e37abdb743ffc1185cd7fae853ceaa5`  
		Last Modified: Sun, 16 Nov 2025 05:21:55 GMT  
		Size: 188.8 MB (188849396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5475d3daa28d75c57b780d54414fff11c4c2beda19492f673a8b77fe888eab89`  
		Last Modified: Sun, 16 Nov 2025 05:22:39 GMT  
		Size: 317.7 MB (317653495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdbf2cbe4f4addf0900418884d1e02f8d03c996b33048d6409944fcfa71853c`  
		Last Modified: Fri, 14 Nov 2025 02:27:29 GMT  
		Size: 705.0 KB (704954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d594f4fb3d443f920d522807772ddd30c1aaee982c9b2096eb18ad67fa0bb158`  
		Last Modified: Fri, 14 Nov 2025 02:27:29 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b210748b14b6012ff816b2b9d1e291b2784408716b903c59bf6d4513f82e84`  
		Last Modified: Fri, 14 Nov 2025 02:27:29 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe80096347ab6717b6c87f25cb270944520f13e28d26b52266197253ec31438f`  
		Last Modified: Fri, 14 Nov 2025 02:27:29 GMT  
		Size: 6.6 KB (6623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9c7dc2a926299b9b61130b85acd7391bfdd79965b5ece4595f89a79343e82d`  
		Last Modified: Fri, 14 Nov 2025 02:27:29 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:83060faeccbc49d204fb39b220de62260e1ea566bfa7266a05c89c8d94b58e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9150906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a985fc379894f58f8300a3d13ac571566f2c914c743e194416408b16b13c9bae`

```dockerfile
```

-	Layers:
	-	`sha256:e3a7ef06d1440a9c4f06ccdc4d44c823ab78d90a0519a1913a4659fbbe1f9690`  
		Last Modified: Fri, 14 Nov 2025 04:07:44 GMT  
		Size: 9.1 MB (9110294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7dfbd75e7035ec21a6aa72a5ee46ff1186d4330d0db761abe93f53eef90c3f7`  
		Last Modified: Fri, 14 Nov 2025 04:07:45 GMT  
		Size: 40.6 KB (40612 bytes)  
		MIME: application/vnd.in-toto+json
