## `xwiki:lts`

```console
$ docker pull xwiki@sha256:4276f17b69b31af3a3cbbdc67bda1cd4980d16c50111fe20eefcbb9d6e1da6f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts` - linux; amd64

```console
$ docker pull xwiki@sha256:fe90e926ceeb63fab373dd33d6e5ac8a02fb2914de5d83d1632e4ef39680e4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.3 MB (641340498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0049264f59d88dd26a3b2bf0652fed0bcdbbcd3e64f8e78c7c6220f7c594f798`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

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
# Thu, 15 Jan 2026 22:19:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:12 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:20:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:20:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:20:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:20:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 20:10:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jan 2026 20:10:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 20:10:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 28 Jan 2026 20:10:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jan 2026 20:10:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jan 2026 20:10:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jan 2026 20:10:27 GMT
ENV TOMCAT_MAJOR=10
# Wed, 28 Jan 2026 20:10:27 GMT
ENV TOMCAT_VERSION=10.1.52
# Wed, 28 Jan 2026 20:10:27 GMT
ENV TOMCAT_SHA512=241183fe5dec15936205ec495b65e04218117affc10e90c5fbc56bce0b4f031ee944d468c128f0ae484fd1d5bd9bec22b65a95a8cfd94cb7fc1f12c7ef434d99
# Wed, 28 Jan 2026 20:10:27 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 28 Jan 2026 20:10:35 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Jan 2026 20:10:36 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 28 Jan 2026 20:10:36 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 20:10:36 GMT
ENTRYPOINT []
# Wed, 28 Jan 2026 20:10:36 GMT
CMD ["catalina.sh" "run"]
# Mon, 02 Feb 2026 19:27:01 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 02 Feb 2026 19:27:01 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 02 Feb 2026 19:27:01 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 02 Feb 2026 19:27:01 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 02 Feb 2026 19:27:01 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 02 Feb 2026 19:27:01 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 02 Feb 2026 19:27:01 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Feb 2026 19:27:01 GMT
ENV XWIKI_VERSION=17.10.3
# Mon, 02 Feb 2026 19:27:01 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.3
# Mon, 02 Feb 2026 19:27:01 GMT
ENV XWIKI_DOWNLOAD_SHA256=933b524e132bff6ab02bf801a85ac58f676795ab8c1fb3b48fa86023f7cf96fd
# Mon, 02 Feb 2026 19:27:22 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 02 Feb 2026 19:27:22 GMT
ENV MYSQL_JDBC_VERSION=9.5.0
# Mon, 02 Feb 2026 19:27:22 GMT
ENV MYSQL_JDBC_SHA256=f2ca3dfaf00d4aa311470db7ea3051962944ba0cb60005a2f75467549c39f425
# Mon, 02 Feb 2026 19:27:22 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.5.0
# Mon, 02 Feb 2026 19:27:22 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.5.0.jar
# Mon, 02 Feb 2026 19:27:22 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.5.0.jar
# Mon, 02 Feb 2026 19:27:22 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 02 Feb 2026 19:27:22 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 02 Feb 2026 19:27:22 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 02 Feb 2026 19:27:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 02 Feb 2026 19:27:22 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 02 Feb 2026 19:27:22 GMT
VOLUME [/usr/local/xwiki]
# Mon, 02 Feb 2026 19:27:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Feb 2026 19:27:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996467dfb4d0179a2f091bc2a9d9749646d7fc320067d1147a6df2b4833f1c82`  
		Last Modified: Thu, 15 Jan 2026 22:19:34 GMT  
		Size: 17.0 MB (16975950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c9275308302d364422df0f3e02503135621d8a4b49a0c18580cf9220532743`  
		Last Modified: Thu, 15 Jan 2026 22:20:14 GMT  
		Size: 53.0 MB (52978745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac4b4cf16a8ad1b819f8041978350794113eb509aba19c5cd47bd77a053c335`  
		Last Modified: Thu, 15 Jan 2026 22:20:12 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb78f73258bc413aae5281eb128ee526870ba076049a4526b38041362fe99c6`  
		Last Modified: Thu, 15 Jan 2026 22:20:12 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f49bf1a6c6af17f648e8d37d2eb7d3cd4df46a00337ef933f7faa47b34e3b8`  
		Last Modified: Wed, 28 Jan 2026 20:10:45 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8072a5f607737f82131c850f987178bf7056a307f6fb6eab1ba15afb6dfd69`  
		Last Modified: Wed, 28 Jan 2026 20:10:46 GMT  
		Size: 14.3 MB (14284335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842fe3450af8f5d09fe4ed1f9c612cd15f8dcc9546e9f8ada127c5e6842d4b2b`  
		Last Modified: Wed, 28 Jan 2026 20:10:46 GMT  
		Size: 3.0 MB (3027735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570dd0a8f6a7d98ac01062d1dfad8da2db3eb5376ef9f85f490d8e548daf8bf7`  
		Last Modified: Mon, 02 Feb 2026 19:28:03 GMT  
		Size: 191.2 MB (191182059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17b9e807a598c97d8d1ef8c172fc0949c1b73d45dac15087abc0c198ef63cce`  
		Last Modified: Mon, 02 Feb 2026 19:28:05 GMT  
		Size: 330.7 MB (330704691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6931d9d6a6b0fe0233403b6bd9650f420c4b684013159e2e9ba3b738b45b8615`  
		Last Modified: Mon, 02 Feb 2026 19:27:55 GMT  
		Size: 2.4 MB (2441397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0695f926bc9b56b9dc4a2434db1f5dd8e2e9d11fa41f44cae264db188564e3`  
		Last Modified: Mon, 02 Feb 2026 19:27:55 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3f667cc7b73907d0a6c68ec263e1047e4888213565dfcba5019a25934b2dd6`  
		Last Modified: Mon, 02 Feb 2026 19:27:56 GMT  
		Size: 2.4 KB (2373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3bc013a3c6060b832a0eb8d6e60161218141cc40a53c5a754c56c96fb566ed`  
		Last Modified: Mon, 02 Feb 2026 19:27:56 GMT  
		Size: 10.7 KB (10708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc74123a43eb2a3deb62bdf1ad98b89e0a7139005aa4bceb6e71723a9544ade`  
		Last Modified: Mon, 02 Feb 2026 19:27:57 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:40fbe40e0e0b77e07a03eb4b3e74384eb0ad8eb3047da5dfa5ef5c8fb5e9c95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9222379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767fb4f95a9fbc4b3eb526045184eb27767c69875637d38f8ec75b12dd03dfe4`

```dockerfile
```

-	Layers:
	-	`sha256:5c46d39c30f17272b9a0ed80b019fba11d7d51fd97bc8fa30114e4ad0f59a4ac`  
		Last Modified: Mon, 02 Feb 2026 19:27:55 GMT  
		Size: 9.2 MB (9180876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7927435cbe16bd403172ce3b900075b95c18d3441ed0725e58e3da29130e6ca4`  
		Last Modified: Mon, 02 Feb 2026 19:27:55 GMT  
		Size: 41.5 KB (41503 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:e051dc3f42ea81518372d997d4f8970c8b0a1d2f8db7541b125d0858e740a3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.1 MB (637129786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6c15d819c2e56e368c9b3159aaf355265b553805999778b0cc1f2943101eb1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

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
# Thu, 15 Jan 2026 22:21:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:21:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:21:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:21:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:21:25 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:21:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:21:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:21:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:21:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 20:13:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jan 2026 20:13:16 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 20:13:16 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 28 Jan 2026 20:13:16 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jan 2026 20:13:16 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jan 2026 20:13:16 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jan 2026 20:13:16 GMT
ENV TOMCAT_MAJOR=10
# Wed, 28 Jan 2026 20:13:16 GMT
ENV TOMCAT_VERSION=10.1.52
# Wed, 28 Jan 2026 20:13:16 GMT
ENV TOMCAT_SHA512=241183fe5dec15936205ec495b65e04218117affc10e90c5fbc56bce0b4f031ee944d468c128f0ae484fd1d5bd9bec22b65a95a8cfd94cb7fc1f12c7ef434d99
# Wed, 28 Jan 2026 20:13:17 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 28 Jan 2026 20:13:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Jan 2026 20:13:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 28 Jan 2026 20:13:40 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 20:13:40 GMT
ENTRYPOINT []
# Wed, 28 Jan 2026 20:13:40 GMT
CMD ["catalina.sh" "run"]
# Mon, 02 Feb 2026 19:31:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 02 Feb 2026 19:31:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 02 Feb 2026 19:31:23 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 02 Feb 2026 19:31:23 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 02 Feb 2026 19:31:23 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 02 Feb 2026 19:31:23 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 02 Feb 2026 19:31:23 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Feb 2026 19:31:23 GMT
ENV XWIKI_VERSION=17.10.3
# Mon, 02 Feb 2026 19:31:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.3
# Mon, 02 Feb 2026 19:31:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=933b524e132bff6ab02bf801a85ac58f676795ab8c1fb3b48fa86023f7cf96fd
# Mon, 02 Feb 2026 19:31:46 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 02 Feb 2026 19:31:46 GMT
ENV MYSQL_JDBC_VERSION=9.5.0
# Mon, 02 Feb 2026 19:31:46 GMT
ENV MYSQL_JDBC_SHA256=f2ca3dfaf00d4aa311470db7ea3051962944ba0cb60005a2f75467549c39f425
# Mon, 02 Feb 2026 19:31:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.5.0
# Mon, 02 Feb 2026 19:31:46 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.5.0.jar
# Mon, 02 Feb 2026 19:31:46 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.5.0.jar
# Mon, 02 Feb 2026 19:31:46 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 02 Feb 2026 19:31:46 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 02 Feb 2026 19:31:46 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 02 Feb 2026 19:31:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 02 Feb 2026 19:31:47 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 02 Feb 2026 19:31:47 GMT
VOLUME [/usr/local/xwiki]
# Mon, 02 Feb 2026 19:31:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Feb 2026 19:31:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066d9c7316405755c4355dfd9b742623829c8c1c49462c4e6c938a83b810b7c8`  
		Last Modified: Thu, 15 Jan 2026 22:21:41 GMT  
		Size: 17.0 MB (16991549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f94c82a8ac7fd54191a08fd6e2afc54327165fa15aabd600b27aeb40409383`  
		Last Modified: Thu, 15 Jan 2026 22:21:42 GMT  
		Size: 52.1 MB (52148637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb0eb06dfa687a3659cfda05b90257c82298acab510f78e070b4bc6d3286e0a`  
		Last Modified: Thu, 15 Jan 2026 22:21:40 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6456b4703cbd2d5d7bfc1f46fa116f62a97af321aea424d90a4899ad64cdaff1`  
		Last Modified: Thu, 15 Jan 2026 22:21:40 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eace77e2fb5fe257600104e7066e45c1caee1a913af277b77c849ad0bf7977fe`  
		Last Modified: Wed, 28 Jan 2026 20:13:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2320033beab2abf03020ba94c290a6660fc5f35c9ba4205e8fb43eec161fe6f8`  
		Last Modified: Wed, 28 Jan 2026 20:13:50 GMT  
		Size: 14.3 MB (14288038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6279f16e4f2d146f0337c6f295ae35cf6fd99bf23339574090650a74b99edae8`  
		Last Modified: Wed, 28 Jan 2026 20:13:50 GMT  
		Size: 2.8 MB (2827450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fe6d5c75eb6054c9413b657cbc1f8b440a3404833f24d7a82dfb3ce06ff46b`  
		Last Modified: Mon, 02 Feb 2026 19:32:27 GMT  
		Size: 188.8 MB (188844634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3333ffb32c00ac0740794104f2de35b0449e7487108f5683fbabb89be80d22d`  
		Last Modified: Mon, 02 Feb 2026 19:32:29 GMT  
		Size: 330.7 MB (330704679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c9bf707543e35a33a0f84f90ee4ce88348e4f23aa762e72ae938ef6d860428`  
		Last Modified: Mon, 02 Feb 2026 19:32:21 GMT  
		Size: 2.4 MB (2441396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee8598f613584ade499e478178cd9f39ae0ef26aeac17018d34126d212d7e84`  
		Last Modified: Mon, 02 Feb 2026 19:32:21 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e0445c83aacbd20a25d44cd806cbd8f7f7e40013db6ac9ca6d39dc63b7e325`  
		Last Modified: Mon, 02 Feb 2026 19:32:22 GMT  
		Size: 2.4 KB (2374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1b38e5442abcd9384d9fcb018120a46f65ef8fc6477552994bfaadfe80239d`  
		Last Modified: Mon, 02 Feb 2026 19:32:22 GMT  
		Size: 10.7 KB (10706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe14e17dee3f35337eebd942016d3c0262d3c504da7ac38ed1348ca401f3f472`  
		Last Modified: Mon, 02 Feb 2026 19:32:23 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:544033a9f37691da5167740365b240cf2a6f33cb2af1ed0a8b8b714be2c891bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c6df1f7f2a78029e4bb2e6df7e6e4dcf316a61fea4c7195e25e047cbe435de`

```dockerfile
```

-	Layers:
	-	`sha256:14fe9b08c26c8af89d97acd36807f1b9f7b44efe528ac3dc932e21a7845fecb5`  
		Last Modified: Mon, 02 Feb 2026 19:32:21 GMT  
		Size: 9.2 MB (9181665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:344b8eba9ac65f0b0758d920d2918817f9fd485a9a0f17ea116c92ef4b7862b3`  
		Last Modified: Mon, 02 Feb 2026 19:32:20 GMT  
		Size: 41.7 KB (41712 bytes)  
		MIME: application/vnd.in-toto+json
