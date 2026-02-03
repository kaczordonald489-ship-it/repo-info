## `xwiki:postgres-tomcat`

```console
$ docker pull xwiki@sha256:07fc3c5daa47be2add49e2236047645cd9d9b298dd46dbb235d334784afe12b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0fb5f7bcf02697ed9718027ed4c9eb17116e6bd452237d5700fa473cff583312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.4 MB (649421164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6e4cb21a893d5990cfe0377bc53e1e83add2b9c24e4c2fbc4a9b47f56e21e3`
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
# Wed, 28 Jan 2026 21:11:16 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 28 Jan 2026 21:11:16 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 28 Jan 2026 21:11:16 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 28 Jan 2026 21:11:16 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 28 Jan 2026 21:11:16 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 28 Jan 2026 21:11:16 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 28 Jan 2026 21:11:16 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Jan 2026 21:11:16 GMT
ENV XWIKI_VERSION=18.0.0
# Wed, 28 Jan 2026 21:11:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.0.0
# Wed, 28 Jan 2026 21:11:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=ade5891f8ffcb1d62763db7b6a0a9b5b2c6a322bc73d9cd223d06d210a179ac5
# Wed, 28 Jan 2026 21:11:38 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 28 Jan 2026 21:11:38 GMT
ENV POSTGRES_JDBC_VERSION=42.7.9
# Wed, 28 Jan 2026 21:11:38 GMT
ENV POSTGRES_JDBC_SHA256=88f1fc3992e80ec3b048f798030e9a014aa4783c40afb56d3e7a87ee0adf166f
# Wed, 28 Jan 2026 21:11:38 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.9
# Wed, 28 Jan 2026 21:11:38 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.9.jar
# Wed, 28 Jan 2026 21:11:38 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.9.jar
# Wed, 28 Jan 2026 21:11:38 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 28 Jan 2026 21:11:38 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 28 Jan 2026 21:11:38 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 28 Jan 2026 21:11:39 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 28 Jan 2026 21:11:39 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 21:11:39 GMT
VOLUME [/usr/local/xwiki]
# Wed, 28 Jan 2026 21:11:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 21:11:39 GMT
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
	-	`sha256:ef4afe1e5bf529c154bb220bc78a539e5c1c2ebd4d9066b072e2bff3b6e5cb3d`  
		Last Modified: Wed, 28 Jan 2026 21:12:21 GMT  
		Size: 191.2 MB (191176621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4729e96fed9dbe3d17dbee7cffaaf1c12b949bd0df50cfd103a9a8ceeda0a75b`  
		Last Modified: Wed, 28 Jan 2026 21:12:24 GMT  
		Size: 340.2 MB (340176974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f4c4c61b91c9f5c3153848da23735065abaa1f9b7514523527c575c57ed2c`  
		Last Modified: Wed, 28 Jan 2026 21:12:15 GMT  
		Size: 1.1 MB (1055028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e809a2bfbb42ee7e0e16eb81d6bfa5faa6516af8e04d9de3d840343cabaded8`  
		Last Modified: Wed, 28 Jan 2026 21:12:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae3b7f65a1aa5ac9b650da6ad48645281d9cbec7f7cbecc1b8f3dd744c8bf1c`  
		Last Modified: Wed, 28 Jan 2026 21:12:16 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007a938e1491ece81d7c6dd142564ffc6a727107895e21c6e396787114cf5514`  
		Last Modified: Wed, 28 Jan 2026 21:12:16 GMT  
		Size: 10.9 KB (10900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6969cf820aca70993713ca13d94f564000a53a03add9cabaf6866a2bb389a2c1`  
		Last Modified: Wed, 28 Jan 2026 21:12:17 GMT  
		Size: 2.4 KB (2419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:e86afad4a8b48158dd35c787e14e6c7181dd5e01a7210169f77895b7d1b1b425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9230465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0633b5a50b6b0e381229b5b800153ad532b043cbd039ef390560406cd3f1ec88`

```dockerfile
```

-	Layers:
	-	`sha256:bf3e4a095a27181b4e63624633926198e257ed58ac826017088b44b3f373e8c8`  
		Last Modified: Wed, 28 Jan 2026 21:12:15 GMT  
		Size: 9.2 MB (9189716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb5581cd633e23e82584ccdf5fe6042e02a0268eb169fd64891b6d37d9545749`  
		Last Modified: Wed, 28 Jan 2026 21:12:14 GMT  
		Size: 40.7 KB (40749 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b3402f18b22574b68c72c931bc1673b1d47d7969d48b8c607cad1e1d114c19f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.2 MB (645211152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87ff84b79821fae02b36f6ebe582feca47e859bd72eb8649744a466737d18ad`
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
# Wed, 28 Jan 2026 21:22:01 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 28 Jan 2026 21:22:01 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 28 Jan 2026 21:22:01 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 28 Jan 2026 21:22:01 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 28 Jan 2026 21:22:01 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 28 Jan 2026 21:22:01 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 28 Jan 2026 21:22:01 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Jan 2026 21:22:01 GMT
ENV XWIKI_VERSION=18.0.0
# Wed, 28 Jan 2026 21:22:01 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.0.0
# Wed, 28 Jan 2026 21:22:01 GMT
ENV XWIKI_DOWNLOAD_SHA256=ade5891f8ffcb1d62763db7b6a0a9b5b2c6a322bc73d9cd223d06d210a179ac5
# Wed, 28 Jan 2026 21:22:23 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 28 Jan 2026 21:22:23 GMT
ENV POSTGRES_JDBC_VERSION=42.7.9
# Wed, 28 Jan 2026 21:22:23 GMT
ENV POSTGRES_JDBC_SHA256=88f1fc3992e80ec3b048f798030e9a014aa4783c40afb56d3e7a87ee0adf166f
# Wed, 28 Jan 2026 21:22:23 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.9
# Wed, 28 Jan 2026 21:22:23 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.9.jar
# Wed, 28 Jan 2026 21:22:23 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.9.jar
# Wed, 28 Jan 2026 21:22:24 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 28 Jan 2026 21:22:24 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 28 Jan 2026 21:22:24 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 28 Jan 2026 21:22:24 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 28 Jan 2026 21:22:24 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 21:22:24 GMT
VOLUME [/usr/local/xwiki]
# Wed, 28 Jan 2026 21:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 21:22:24 GMT
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
	-	`sha256:ab25f0653e982bb2dcf39308ede4af1e37b5fe71071eacf012a4cdf3655a53f5`  
		Last Modified: Wed, 28 Jan 2026 21:23:04 GMT  
		Size: 188.8 MB (188839879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043c1fe0cb20b59748301087db726a5c7e20cdf7524f92afe2e144ceb75c37e4`  
		Last Modified: Wed, 28 Jan 2026 21:23:08 GMT  
		Size: 340.2 MB (340176974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de5ca7527447e6997ba457d7dabc79e46be3e991158b762555826382f619189`  
		Last Modified: Wed, 28 Jan 2026 21:22:58 GMT  
		Size: 1.1 MB (1055031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3382237343aa77d76bd8a5982024fd3b46034b2a097ed20176d442dfd9b14881`  
		Last Modified: Wed, 28 Jan 2026 21:22:58 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce60269b6dd917bd3b2818f083c4a0b7e4393cdce42866f1f816c7a248f4c59`  
		Last Modified: Wed, 28 Jan 2026 21:22:59 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae7b493e20a5098903e38787e8348f188daa9051a230ddd8471530d977a6e73`  
		Last Modified: Wed, 28 Jan 2026 21:22:59 GMT  
		Size: 10.9 KB (10901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380cd85950ae286cc4df36386b9b56df5257f6b7aec6482108533464037384b8`  
		Last Modified: Wed, 28 Jan 2026 21:23:00 GMT  
		Size: 2.4 KB (2419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:eb8976575095ae6c504ccffb192236d18d2afcf74249dd257c38cb0abef11b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9231391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15da5bee1c3fc6249fb971226f3efb57168745d8c1d43cb0d3bd7a7ad4661edc`

```dockerfile
```

-	Layers:
	-	`sha256:25582e341550577420d3bb78cd3533ca279ee4168cf00523ebb922351ca3e644`  
		Last Modified: Wed, 28 Jan 2026 21:22:58 GMT  
		Size: 9.2 MB (9190469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c85ea6618d65f0ad2a347304dbfc94a6501bf8fd5eb21eaba0845153ace36cf2`  
		Last Modified: Wed, 28 Jan 2026 21:22:57 GMT  
		Size: 40.9 KB (40922 bytes)  
		MIME: application/vnd.in-toto+json
