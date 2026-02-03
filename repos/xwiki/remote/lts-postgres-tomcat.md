## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:d0d4ba459aeb772904405770f78dca33f07127b1d021b82f78f8b79d813fcf21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:b36d8ddb04fa3cbd5fd261feff90c41f05b365bc0e8f3c43c0613d2f76091477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 MB (639953175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f89a23abaa1e301cfc78f77d636c05817d365be2c17dc545dfd643ff1a63cc5`
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
# Mon, 02 Feb 2026 19:27:08 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 02 Feb 2026 19:27:08 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 02 Feb 2026 19:27:08 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 02 Feb 2026 19:27:08 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 02 Feb 2026 19:27:08 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 02 Feb 2026 19:27:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 02 Feb 2026 19:27:08 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Feb 2026 19:27:08 GMT
ENV XWIKI_VERSION=17.10.3
# Mon, 02 Feb 2026 19:27:08 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.3
# Mon, 02 Feb 2026 19:27:08 GMT
ENV XWIKI_DOWNLOAD_SHA256=933b524e132bff6ab02bf801a85ac58f676795ab8c1fb3b48fa86023f7cf96fd
# Mon, 02 Feb 2026 19:27:30 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 02 Feb 2026 19:27:30 GMT
ENV POSTGRES_JDBC_VERSION=42.7.9
# Mon, 02 Feb 2026 19:27:30 GMT
ENV POSTGRES_JDBC_SHA256=88f1fc3992e80ec3b048f798030e9a014aa4783c40afb56d3e7a87ee0adf166f
# Mon, 02 Feb 2026 19:27:30 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.9
# Mon, 02 Feb 2026 19:27:30 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.9.jar
# Mon, 02 Feb 2026 19:27:30 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.9.jar
# Mon, 02 Feb 2026 19:27:30 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 02 Feb 2026 19:27:30 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 02 Feb 2026 19:27:31 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 02 Feb 2026 19:27:31 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 02 Feb 2026 19:27:31 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 02 Feb 2026 19:27:31 GMT
VOLUME [/usr/local/xwiki]
# Mon, 02 Feb 2026 19:27:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Feb 2026 19:27:31 GMT
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
	-	`sha256:b405baf874493557d5465a39bb9624deebfa2eaa4fe52d33494948b462abf02c`  
		Last Modified: Mon, 02 Feb 2026 19:28:15 GMT  
		Size: 191.2 MB (191181150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada091d97d665857c09bae6feedd5ccf9b6676e17edd8178e10175c548b2e2de`  
		Last Modified: Mon, 02 Feb 2026 19:28:17 GMT  
		Size: 330.7 MB (330704648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3edd9eabf58b400cf0d8553714c5ce59f7d50ac34de807126b8f1bfafd28093`  
		Last Modified: Mon, 02 Feb 2026 19:28:08 GMT  
		Size: 1.1 MB (1055028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e905c15894d8d41572dcdd3542dda6055b04a4664f9f35839209754d5f3aba9`  
		Last Modified: Mon, 02 Feb 2026 19:28:08 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb82f976f85f3d5902b21ad3094ef55f3b3e1472247dc8d585a9c9e056b70870`  
		Last Modified: Mon, 02 Feb 2026 19:28:09 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bf1ce78369f98e88a26312ce0ca472f3976010b1bcf8520943c9e598698a34`  
		Last Modified: Mon, 02 Feb 2026 19:28:10 GMT  
		Size: 10.7 KB (10706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9791c3468fb1e39f6aa8b0ba10b25f21e58346054f4ac8fcc3707c739f40286`  
		Last Modified: Mon, 02 Feb 2026 19:28:11 GMT  
		Size: 2.4 KB (2419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:43c000a82fcf16bf36af9b7af7cb9a65b7d236122e5cc8fb585c8612436514aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9220103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c94434d442beaf0d6909690e7baa5d5501e905f96d4778f88f5ec6d1d4b24e`

```dockerfile
```

-	Layers:
	-	`sha256:c27aaee31c50f2de4df2a584246a0a1a35590af8c6da985900f3727a790ee68b`  
		Last Modified: Mon, 02 Feb 2026 19:28:09 GMT  
		Size: 9.2 MB (9179670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7b52c52a566152623aabf37da8712f0c431f345bf06d3f5ac27e787fd24373f`  
		Last Modified: Mon, 02 Feb 2026 19:28:08 GMT  
		Size: 40.4 KB (40433 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:e84bf8297080d6e5922470e527ae9edf36fcff234068134618a12c0bb2c9d307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.7 MB (635743470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040feb51dc75a9164adff7bee9d2054ddb56f10af2829e1987422211272118b1`
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
# Mon, 02 Feb 2026 19:31:31 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 02 Feb 2026 19:31:31 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 02 Feb 2026 19:31:31 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 02 Feb 2026 19:31:31 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 02 Feb 2026 19:31:31 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 02 Feb 2026 19:31:31 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 02 Feb 2026 19:31:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Feb 2026 19:31:31 GMT
ENV XWIKI_VERSION=17.10.3
# Mon, 02 Feb 2026 19:31:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.3
# Mon, 02 Feb 2026 19:31:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=933b524e132bff6ab02bf801a85ac58f676795ab8c1fb3b48fa86023f7cf96fd
# Mon, 02 Feb 2026 19:31:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 02 Feb 2026 19:31:53 GMT
ENV POSTGRES_JDBC_VERSION=42.7.9
# Mon, 02 Feb 2026 19:31:53 GMT
ENV POSTGRES_JDBC_SHA256=88f1fc3992e80ec3b048f798030e9a014aa4783c40afb56d3e7a87ee0adf166f
# Mon, 02 Feb 2026 19:31:53 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.9
# Mon, 02 Feb 2026 19:31:53 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.9.jar
# Mon, 02 Feb 2026 19:31:53 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.9.jar
# Mon, 02 Feb 2026 19:31:53 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 02 Feb 2026 19:31:53 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 02 Feb 2026 19:31:53 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 02 Feb 2026 19:31:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 02 Feb 2026 19:31:53 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 02 Feb 2026 19:31:53 GMT
VOLUME [/usr/local/xwiki]
# Mon, 02 Feb 2026 19:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Feb 2026 19:31:53 GMT
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
	-	`sha256:ae42ca55b9e1be2c739d4b8daad5d8744e87144ba05e0b681f6aecbf3551f36e`  
		Last Modified: Mon, 02 Feb 2026 19:32:33 GMT  
		Size: 188.8 MB (188844670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5b58f88578d616d2c2fd97e99219a5888e33544f30d89cc2325b17736ecbca`  
		Last Modified: Mon, 02 Feb 2026 19:32:36 GMT  
		Size: 330.7 MB (330704706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544df6ecac6ad8bf75c1e26cb39b34c986d81eeab040eb09bd22da3f2fb71fbd`  
		Last Modified: Mon, 02 Feb 2026 19:32:26 GMT  
		Size: 1.1 MB (1055029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb648fc2932232636b2e35e53c433b0475883d7d8c1d3b334e49e432a13d26b`  
		Last Modified: Mon, 02 Feb 2026 19:32:26 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0beb593d3c55d736c397e276b6415d79e1339f4736dc45e0d00eb43553dda484`  
		Last Modified: Mon, 02 Feb 2026 19:32:27 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffce5fa532ebb6d1b896b0647fcfdd2cfe866adc620d797cf4a363d3169569c`  
		Last Modified: Mon, 02 Feb 2026 19:32:28 GMT  
		Size: 10.7 KB (10707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b3f3b8ec0e004deb265fb45b9a3ecf404c432476da5699f2bac7e2947711c9`  
		Last Modified: Mon, 02 Feb 2026 19:32:29 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:1141a7a6ba3eb94e8e788b7445c5f0e89564d5a354e2ffa8781100d64eab9892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9221005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3c622b2ca302c776c30d75883bbd1ca3db9613420fc3b9a92184cdfb78799c`

```dockerfile
```

-	Layers:
	-	`sha256:035ddb406be884680a17b2806c44ef9abb4d9cf23b471dbf00e0042a51f2a6b0`  
		Last Modified: Mon, 02 Feb 2026 19:32:27 GMT  
		Size: 9.2 MB (9180411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8482b6dfb192b8969fb65a38d1eaad61540ee18e4040e0eb6bb76ea1c84b7d93`  
		Last Modified: Mon, 02 Feb 2026 19:32:26 GMT  
		Size: 40.6 KB (40594 bytes)  
		MIME: application/vnd.in-toto+json
