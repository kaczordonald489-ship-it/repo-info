## `xwiki:17-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:97738fc0a230cff56641082caab6b03dfb63f5b6a55ac0de4c11c5f2485204a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:17-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:462cd239c06785682581eceb68f12f3cfd30b44432e732be823f0016e1dc0c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.9 MB (628869844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945138697c1f384a98ecac9e4cd1f3c367e6ec2d0e4865515e9ef612903acc37`
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
# Fri, 14 Nov 2025 02:21:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 14 Nov 2025 02:21:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 02:21:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 14 Nov 2025 02:21:19 GMT
WORKDIR /usr/local/tomcat
# Fri, 14 Nov 2025 02:21:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 02:21:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 02:21:19 GMT
ENV TOMCAT_MAJOR=10
# Fri, 14 Nov 2025 02:21:19 GMT
ENV TOMCAT_VERSION=10.1.49
# Fri, 14 Nov 2025 02:21:19 GMT
ENV TOMCAT_SHA512=a46c8e37d4767b56a16dbdd8e81b80f25ad2edd5fba68b5099b9165cfffbe32bc923a601db8bb5cba50e8b1047a7906eb8c30ca176e1c0b8dfd85fbb9c54c6c2
# Fri, 14 Nov 2025 02:21:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 14 Nov 2025 02:21:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 02:21:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 14 Nov 2025 02:21:25 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 02:21:25 GMT
ENTRYPOINT []
# Fri, 14 Nov 2025 02:21:25 GMT
CMD ["catalina.sh" "run"]
# Mon, 24 Nov 2025 18:10:42 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 24 Nov 2025 18:10:42 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 24 Nov 2025 18:10:42 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 24 Nov 2025 18:10:42 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 24 Nov 2025 18:10:42 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 24 Nov 2025 18:10:42 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 24 Nov 2025 18:10:42 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 18:10:42 GMT
ENV XWIKI_VERSION=17.10.0
# Mon, 24 Nov 2025 18:10:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.0
# Mon, 24 Nov 2025 18:10:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=7a1942782a74736ec4ebe654ede31a4454cff230bab6818a78db09452a2d1656
# Mon, 24 Nov 2025 18:11:03 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 24 Nov 2025 18:11:03 GMT
ENV MARIADB_JDBC_VERSION=3.5.6
# Mon, 24 Nov 2025 18:11:03 GMT
ENV MARIADB_JDBC_SHA256=a129703efd7b0f334564d46753de999f09b3a361489a2eb647e6020390981cc9
# Mon, 24 Nov 2025 18:11:03 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.6
# Mon, 24 Nov 2025 18:11:03 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.6.jar
# Mon, 24 Nov 2025 18:11:03 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.6.jar
# Mon, 24 Nov 2025 18:12:00 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 24 Nov 2025 18:12:00 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 24 Nov 2025 18:12:00 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 24 Nov 2025 18:12:00 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 24 Nov 2025 18:12:00 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 24 Nov 2025 18:12:00 GMT
VOLUME [/usr/local/xwiki]
# Mon, 24 Nov 2025 18:12:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 18:12:00 GMT
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
	-	`sha256:3b2a8227e000a2d12d21934eacf073d426c9006f3f853061a3c4f6a476e9f8a0`  
		Last Modified: Fri, 14 Nov 2025 02:21:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5caa722c7f17a8ad9d921f9322fb085a69b501b10e8d315cf194f7cd3614bc5`  
		Last Modified: Fri, 14 Nov 2025 02:21:40 GMT  
		Size: 14.1 MB (14096370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f930fae56746693faec57b1589c11f24eda665dfe92a7babb677ef9e8ef90a1`  
		Last Modified: Fri, 14 Nov 2025 02:21:39 GMT  
		Size: 224.8 KB (224758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb9a62f2b8865a787870ad5f257b24b5766523114dbdf5acf2c9f5c51183303`  
		Last Modified: Mon, 24 Nov 2025 18:28:27 GMT  
		Size: 191.2 MB (191180022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745c67ed4fbcf6d1a7da8aed2b53210dcd8394e9373ec8a7dd094adec40ff01b`  
		Last Modified: Mon, 24 Nov 2025 18:28:26 GMT  
		Size: 323.0 MB (322968429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ccbb82c1fd190e78a142d6236d97958dd0c8bfb47f3743b9f54b5b8e3aaece`  
		Last Modified: Mon, 24 Nov 2025 18:12:21 GMT  
		Size: 705.0 KB (704957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8c0938a341c779b64d90b7afdb38c47a7198f30b5d29f4491227a215d32be5`  
		Last Modified: Mon, 24 Nov 2025 18:12:21 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f19247526beba8850512918b6313acbb757cc95b5ca69a6d8f481b810ec45e`  
		Last Modified: Mon, 24 Nov 2025 18:12:21 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9155a012ece1f1860e90dd394f0c49d07b218c9a15f4aa3ee5db6b3495506cd`  
		Last Modified: Mon, 24 Nov 2025 18:12:21 GMT  
		Size: 10.7 KB (10678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015b2c71b17724e25a73bd09f29b83832f5cc16d5fdc53cb40e6b1a6207625c5`  
		Last Modified: Mon, 24 Nov 2025 18:12:21 GMT  
		Size: 2.5 KB (2475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:35c36daf456e28b90eaf851dde3282e4668d428c9dd172c845a4b71e350e53e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9209209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff0d6f0acddc49d606954de51e79e9af6e9c662ca0c65bc941adda6ec27f4ab`

```dockerfile
```

-	Layers:
	-	`sha256:3525b7f96b547fc5c0af635825412ba26296092fd1e565beff4b1dad3daf3a9c`  
		Last Modified: Mon, 24 Nov 2025 22:07:35 GMT  
		Size: 9.2 MB (9168435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096cc5e430cf48a803928d0067d6ca49c95ae3186342f08da9b1dfa6033a9a88`  
		Last Modified: Mon, 24 Nov 2025 22:07:36 GMT  
		Size: 40.8 KB (40774 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:17-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:074dbb03a19ae5d94d8fc18f77f8d3e21ba27a8a1168e2ca505f8efe516ab44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.9 MB (624866634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52744d33f10506eb2f83c39ba5584d38c0fb7a66c8062ebcaed5f9c7253e8fc`
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
# Fri, 14 Nov 2025 01:40:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 14 Nov 2025 01:40:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:40:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 14 Nov 2025 01:40:24 GMT
WORKDIR /usr/local/tomcat
# Fri, 14 Nov 2025 01:40:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:40:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:40:24 GMT
ENV TOMCAT_MAJOR=10
# Fri, 14 Nov 2025 01:40:24 GMT
ENV TOMCAT_VERSION=10.1.49
# Fri, 14 Nov 2025 01:40:24 GMT
ENV TOMCAT_SHA512=a46c8e37d4767b56a16dbdd8e81b80f25ad2edd5fba68b5099b9165cfffbe32bc923a601db8bb5cba50e8b1047a7906eb8c30ca176e1c0b8dfd85fbb9c54c6c2
# Fri, 14 Nov 2025 01:40:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 14 Nov 2025 01:40:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:40:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 14 Nov 2025 01:40:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 01:40:34 GMT
ENTRYPOINT []
# Fri, 14 Nov 2025 01:40:34 GMT
CMD ["catalina.sh" "run"]
# Mon, 24 Nov 2025 18:52:24 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 24 Nov 2025 18:52:24 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 24 Nov 2025 18:52:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 24 Nov 2025 18:52:24 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 24 Nov 2025 18:52:24 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 24 Nov 2025 18:52:24 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 24 Nov 2025 18:52:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 18:52:24 GMT
ENV XWIKI_VERSION=17.10.0
# Mon, 24 Nov 2025 18:52:24 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.0
# Mon, 24 Nov 2025 18:52:24 GMT
ENV XWIKI_DOWNLOAD_SHA256=7a1942782a74736ec4ebe654ede31a4454cff230bab6818a78db09452a2d1656
# Mon, 24 Nov 2025 18:52:45 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 24 Nov 2025 18:52:45 GMT
ENV MARIADB_JDBC_VERSION=3.5.6
# Mon, 24 Nov 2025 18:52:45 GMT
ENV MARIADB_JDBC_SHA256=a129703efd7b0f334564d46753de999f09b3a361489a2eb647e6020390981cc9
# Mon, 24 Nov 2025 18:52:45 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.6
# Mon, 24 Nov 2025 18:52:45 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.6.jar
# Mon, 24 Nov 2025 18:52:45 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.6.jar
# Mon, 24 Nov 2025 18:53:35 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 24 Nov 2025 18:53:35 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 24 Nov 2025 18:53:35 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 24 Nov 2025 18:53:35 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 24 Nov 2025 18:53:35 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 24 Nov 2025 18:53:35 GMT
VOLUME [/usr/local/xwiki]
# Mon, 24 Nov 2025 18:53:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 18:53:35 GMT
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
	-	`sha256:6cc54f22ff7be481d07fbc5563fa78622b485d16a8399546cb598cd4116d3fb6`  
		Last Modified: Fri, 14 Nov 2025 01:40:48 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796431cd390aaf24c6f9076bf17f54d840b43c2bc40b53c454e8aebb59cc538d`  
		Last Modified: Fri, 14 Nov 2025 01:40:49 GMT  
		Size: 14.1 MB (14099378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b6fa534208a2149ad3fd01edcd3758353690a78f52f6acd10f60d8572246e2`  
		Last Modified: Fri, 14 Nov 2025 01:40:48 GMT  
		Size: 225.2 KB (225203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44544d3e5943a9c8e34c988e722647e4c1b6a2f2c57f42c41caef7e4c7b09fee`  
		Last Modified: Tue, 25 Nov 2025 10:19:13 GMT  
		Size: 188.8 MB (188849437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abea921988ae8a948d53d9d320255f576ca6780c1ef984b97bf635d91b001642`  
		Last Modified: Tue, 25 Nov 2025 00:46:53 GMT  
		Size: 323.0 MB (322968449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc682494ae61922731ba08e7c37fc59cd8e21de6ee6bf6116c90ac72227d348a`  
		Last Modified: Mon, 24 Nov 2025 18:54:02 GMT  
		Size: 705.0 KB (704960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e990736fad1104dcad7aca8f361d141c2be0c8bd324b5d56b9de11fab3c6da6f`  
		Last Modified: Mon, 24 Nov 2025 18:54:02 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db3a487b46dbda2eced689ced8fb57f7e49f90bb34a64cd59c65ea208ea3d02`  
		Last Modified: Mon, 24 Nov 2025 18:54:02 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7856b696aa3f98f7329d16aa0f70d1a88f8e9e976f2d641c68dcb6daf0fecebc`  
		Last Modified: Mon, 24 Nov 2025 18:54:02 GMT  
		Size: 10.7 KB (10676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39f92eb89d611c27003a522e8b8af51b0295259196d98da43f8c292d93ee3cb`  
		Last Modified: Mon, 24 Nov 2025 18:54:02 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:17f1bfd5551ad690fa737592321f15e77fe189b71309fac8bed04a6d78a6d86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9210135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d8c374bb55802ade44fefa231f07219b8a69ccb5c9efba35f509ac27b47752`

```dockerfile
```

-	Layers:
	-	`sha256:48b611ba89dbe3e9159d391bf1091d9869254b071aeb443d5a704836becfd71a`  
		Last Modified: Mon, 24 Nov 2025 22:07:45 GMT  
		Size: 9.2 MB (9169188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a80eec561ceff9335d2b2bd71ec417a9d90769b019064e98ad066e5a2c9bae68`  
		Last Modified: Mon, 24 Nov 2025 22:07:45 GMT  
		Size: 40.9 KB (40947 bytes)  
		MIME: application/vnd.in-toto+json
