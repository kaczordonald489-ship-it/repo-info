## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:01d3f307558a9b5544e038af8a9ff7a314d4d226bff2b24bf777207b2fec25a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:192a3be24b5161aa5c0eb47f60f84b22528093bacc5dd94fe588ded003ea7597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.2 MB (629208685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7be1133b07324373757b600148399889e8f572a241b0d3fde38c5934440a5f`
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
# Mon, 24 Nov 2025 18:11:53 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 24 Nov 2025 18:11:53 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 24 Nov 2025 18:11:53 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 24 Nov 2025 18:11:53 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 24 Nov 2025 18:11:53 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 24 Nov 2025 18:11:53 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 24 Nov 2025 18:11:53 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 18:11:53 GMT
ENV XWIKI_VERSION=17.10.0
# Mon, 24 Nov 2025 18:11:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.0
# Mon, 24 Nov 2025 18:11:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=7a1942782a74736ec4ebe654ede31a4454cff230bab6818a78db09452a2d1656
# Mon, 24 Nov 2025 18:12:14 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 24 Nov 2025 18:12:14 GMT
ENV POSTGRES_JDBC_VERSION=42.7.8
# Mon, 24 Nov 2025 18:12:14 GMT
ENV POSTGRES_JDBC_SHA256=2a32a9dcbc42d67a50ad3a0de5efd102c8d2be46720045f2cbd6689f160ab7c7
# Mon, 24 Nov 2025 18:12:14 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.8
# Mon, 24 Nov 2025 18:12:14 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.8.jar
# Mon, 24 Nov 2025 18:12:14 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.8.jar
# Mon, 24 Nov 2025 18:12:14 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 24 Nov 2025 18:12:14 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 24 Nov 2025 18:12:14 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 24 Nov 2025 18:12:15 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 24 Nov 2025 18:12:15 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 24 Nov 2025 18:12:15 GMT
VOLUME [/usr/local/xwiki]
# Mon, 24 Nov 2025 18:12:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 18:12:15 GMT
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
	-	`sha256:22869cda807ddc8daf3f84cb45779a3f61df15889c27899fc2383a9d1436cd64`  
		Last Modified: Mon, 24 Nov 2025 18:19:32 GMT  
		Size: 191.2 MB (191180693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57379d8a9633ac3d702e53b189f291acec3b4156448e208217666825e8ddc74`  
		Last Modified: Mon, 24 Nov 2025 18:19:16 GMT  
		Size: 323.0 MB (322968466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787ee4fa07982a2a2c16440b325589e77ef34641e6b049c501d5bebd53da352b`  
		Last Modified: Mon, 24 Nov 2025 18:13:06 GMT  
		Size: 1.0 MB (1043003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d38eba12b1c96c2d5bec90dcbe822edb66712ef6ce91c5a5298ccc4d01f2940`  
		Last Modified: Mon, 24 Nov 2025 18:13:06 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaf357523c24918636192bf112fbfb1303e3bc78f6558c91982983f4dd5f35a`  
		Last Modified: Mon, 24 Nov 2025 18:13:06 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9677836214b21b0974fdf03174b9f1356e284694450e806dcf4b5a23ee0b756`  
		Last Modified: Mon, 24 Nov 2025 18:13:06 GMT  
		Size: 10.7 KB (10673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a22f85b966d4fb0c3c188e29a09b635650317d2383ce3d64e6ba15e961d391`  
		Last Modified: Mon, 24 Nov 2025 18:13:06 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:7113291daef1cc830ac1e244135b6a71658065fd62aa98436a64204020d19a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9209203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3754de08dd93f4160016c1b3fba87244c1cd06f9ca874afde3448bd2c110eb`

```dockerfile
```

-	Layers:
	-	`sha256:26d0d3840439e2b2d0b22315a7690e77ddbcda9170e8531a53d1bdcb83edde74`  
		Last Modified: Mon, 24 Nov 2025 22:07:49 GMT  
		Size: 9.2 MB (9168452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcb01149b88038cc1bc1ec7c78d6bc6cd1ba1f26e537a36e0c21b128af96d858`  
		Last Modified: Mon, 24 Nov 2025 22:07:50 GMT  
		Size: 40.8 KB (40751 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:76dc129add9e37146e94d22ea9056de955dc514dc008cccba7b7cc80097cfb30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.2 MB (625204577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959593f00393f61471aa44ad23b1100f492d34e14bcbb414ca48ebd4adf17ce3`
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
# Mon, 24 Nov 2025 18:53:32 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 24 Nov 2025 18:53:32 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 24 Nov 2025 18:53:32 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 24 Nov 2025 18:53:32 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 24 Nov 2025 18:53:32 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 24 Nov 2025 18:53:32 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 24 Nov 2025 18:53:32 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 18:53:32 GMT
ENV XWIKI_VERSION=17.10.0
# Mon, 24 Nov 2025 18:53:32 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.0
# Mon, 24 Nov 2025 18:53:32 GMT
ENV XWIKI_DOWNLOAD_SHA256=7a1942782a74736ec4ebe654ede31a4454cff230bab6818a78db09452a2d1656
# Mon, 24 Nov 2025 18:53:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 24 Nov 2025 18:53:53 GMT
ENV POSTGRES_JDBC_VERSION=42.7.8
# Mon, 24 Nov 2025 18:53:53 GMT
ENV POSTGRES_JDBC_SHA256=2a32a9dcbc42d67a50ad3a0de5efd102c8d2be46720045f2cbd6689f160ab7c7
# Mon, 24 Nov 2025 18:53:53 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.8
# Mon, 24 Nov 2025 18:53:53 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.8.jar
# Mon, 24 Nov 2025 18:53:53 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.8.jar
# Mon, 24 Nov 2025 18:53:53 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 24 Nov 2025 18:53:53 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 24 Nov 2025 18:53:53 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 24 Nov 2025 18:53:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 24 Nov 2025 18:53:53 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 24 Nov 2025 18:53:53 GMT
VOLUME [/usr/local/xwiki]
# Mon, 24 Nov 2025 18:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 18:53:53 GMT
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
	-	`sha256:f226b300b15007eac4541a956bf3ebbe28cf55549aebf32b73ff4e9ca5330ba8`  
		Last Modified: Mon, 24 Nov 2025 22:10:28 GMT  
		Size: 188.8 MB (188849202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1095e2a0189e084cb8d7f26dc1764876c233ea95ea504d385f2987a748dd164a`  
		Last Modified: Mon, 24 Nov 2025 22:10:31 GMT  
		Size: 323.0 MB (322968467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b906a8d39de62cc13c28c0b41c23c8866d95c6fd5e9017861bb3a4b8452a9f8c`  
		Last Modified: Mon, 24 Nov 2025 18:54:42 GMT  
		Size: 1.0 MB (1043011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221232e67c6f9e77d2a415510e118760fed4c92c1c9f7503699911bed253f8a8`  
		Last Modified: Mon, 24 Nov 2025 18:54:42 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99799c9f256d20379015e452c6aecff11195efc7e9c2571f3f7ce931e2aeaa08`  
		Last Modified: Mon, 24 Nov 2025 18:54:42 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc0d723dd8ddfe9b4a952bed0015ac09ad44ade1cb5d779f21ffe7293c16f94`  
		Last Modified: Mon, 24 Nov 2025 18:54:42 GMT  
		Size: 10.7 KB (10675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c376a24bcf51410584b7e951cc930465a50c19e125b2fd26fec55b28fbcc566`  
		Last Modified: Mon, 24 Nov 2025 18:54:42 GMT  
		Size: 2.4 KB (2419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:c0126dfa18d39e0113a6c4374f2c856b1718adb0a682d17aa80b83c6863726ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9210129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fbc7caf2fc109ff7da811844e666c30dfe6f3bb7c3e16fb8dec940f7ab647e`

```dockerfile
```

-	Layers:
	-	`sha256:a4420226c45c987a515ed02f2464c424b20544046543ef3023ed4ac68427e635`  
		Last Modified: Mon, 24 Nov 2025 22:07:57 GMT  
		Size: 9.2 MB (9169205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:568e6278ed1e8c75e28b3930c5e1d0bdecba49956bcabd9dc691d48912705f03`  
		Last Modified: Mon, 24 Nov 2025 22:07:58 GMT  
		Size: 40.9 KB (40924 bytes)  
		MIME: application/vnd.in-toto+json
