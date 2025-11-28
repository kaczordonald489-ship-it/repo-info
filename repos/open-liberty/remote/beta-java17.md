## `open-liberty:beta-java17`

```console
$ docker pull open-liberty@sha256:9ac6a03181f2da2cfd2c2b4b5659e357c23eb5a317caee0871714f45fa9865fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `open-liberty:beta-java17` - linux; amd64

```console
$ docker pull open-liberty@sha256:05bc6feb73ae86000f938000c1577037ca33cd1a9b82f5e571e446e41972be84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.8 MB (484828418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ac42d05a78283e9ebda3c0d365bf52aef8621d1261c7760f1b9dd09b33512f`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:26:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:26:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:26:12 GMT
ENV JAVA_VERSION=jdk-17.0.17+10_openj9-0.56.0
# Thu, 13 Nov 2025 23:26:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='56f11335a3c67f96f0dc8ca4ebe02239fa300fd871ab46de27103666998b2aec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cc9ac62b665c1c61860dbfe8d06f2f30d1f0439f1e93f6ae09770ca91949feb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='13c8bbbb9ffa57b33a48ca018fd281e69dd6fdbb4e96ca7df72a49db614d899c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='bc147228dc80b3add4a64b441cf3fe69e06b0b8ad3cd86444d7de2fd7c0fea86';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Nov 2025 23:26:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:26:15 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Nov 2025 23:26:47 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 14 Nov 2025 00:30:44 GMT
USER root
# Fri, 14 Nov 2025 00:30:44 GMT
ARG LIBERTY_VERSION=25.0.0.12-beta
# Fri, 14 Nov 2025 00:30:44 GMT
ARG LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5
# Fri, 14 Nov 2025 00:30:44 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip
# Fri, 14 Nov 2025 00:30:44 GMT
ARG LIBERTY_BUILD_LABEL=cl251120251020-0302
# Fri, 14 Nov 2025 00:30:44 GMT
ARG OPENJ9_SCC=true
# Fri, 14 Nov 2025 00:30:44 GMT
ARG VERBOSE=false
# Fri, 14 Nov 2025 00:30:44 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251120251020-0302 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.12-beta liberty.version=25.0.0.12-beta io.openliberty.version=25.0.0.12-beta
# Fri, 14 Nov 2025 00:30:44 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 14 Nov 2025 00:30:44 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 14 Nov 2025 00:30:44 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 14 Nov 2025 00:30:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 14 Nov 2025 00:31:01 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 14 Nov 2025 00:31:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 14 Nov 2025 00:31:01 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 14 Nov 2025 00:31:01 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 14 Nov 2025 00:31:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 14 Nov 2025 00:31:23 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 14 Nov 2025 00:31:23 GMT
USER 1001
# Fri, 14 Nov 2025 00:31:23 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 14 Nov 2025 00:31:23 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 14 Nov 2025 00:31:23 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed758cc5553a37ce8cad94f4b107e110a36e826b5877bddfb2f3c141f783dfa`  
		Last Modified: Thu, 13 Nov 2025 23:27:08 GMT  
		Size: 12.2 MB (12171706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b84bbca0fa33b311d0fb6c24ada2d6cbe1ecc53dfa141d8ef7fc04019138145`  
		Last Modified: Thu, 13 Nov 2025 23:27:17 GMT  
		Size: 55.2 MB (55190794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7aec9a786568cfd3ea9f2580ed8a458a099ef0e8d833b422f82ab29971be740`  
		Last Modified: Thu, 13 Nov 2025 23:27:07 GMT  
		Size: 5.1 MB (5093596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5164ca182152d3a64fdbe2dca4bd1628272242a9abe536701b683825f2c33d45`  
		Last Modified: Fri, 14 Nov 2025 00:32:00 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a60779c8351ec40417630135e901c9738422a28d4c19f98b6295a755c14efd3`  
		Last Modified: Fri, 14 Nov 2025 00:32:00 GMT  
		Size: 12.3 KB (12289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3f83fdf81a66a335b92ccab55326d8a1aa5f5888fb5792c650a3d7244a49b3`  
		Last Modified: Fri, 14 Nov 2025 00:32:00 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a58f9d99bb9ec95454aae3fe0447b21e60acf1d40a7193cc24aac7c6fc638ab`  
		Last Modified: Fri, 14 Nov 2025 00:32:01 GMT  
		Size: 31.7 KB (31747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f9863d1a0b2c030392bf4fc1dde21a6f8b98e6bccdc5bb9392dde1729e36be`  
		Last Modified: Fri, 14 Nov 2025 09:07:14 GMT  
		Size: 368.0 MB (367995136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a46f54997af3dfa1efdafc5f785cf776049067682fc4a6b7654f8d710c50a55`  
		Last Modified: Fri, 14 Nov 2025 00:32:01 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8147277938f72246b1645c7379122404aa26723ae79642ec146767aa73d158f2`  
		Last Modified: Fri, 14 Nov 2025 00:32:01 GMT  
		Size: 13.7 KB (13718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a5595d76b9b24699c18fece37b9fac78a441dcc2f2685b82efc7a1ae307b2d`  
		Last Modified: Fri, 14 Nov 2025 00:32:02 GMT  
		Size: 14.8 MB (14780285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:d258e20113e27b3a69fddd0eab93010ca4d62c31c94c39f0555fca8400d8c50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5830939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5370c7393fd0e14a609cbf2b21e7bb7f04c0d903a20d6ab397a45d65f116bbfa`

```dockerfile
```

-	Layers:
	-	`sha256:aaf4c0ea0f241c6e49bf56f21602c7da49cd32d2f5fe7981a8df05ee1f5dec19`  
		Last Modified: Fri, 14 Nov 2025 03:51:36 GMT  
		Size: 5.8 MB (5791452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67849ef45e0094bbe9a3215db5c2c4b593920a14442343bcf128c51f7346a1eb`  
		Last Modified: Fri, 14 Nov 2025 03:51:37 GMT  
		Size: 39.5 KB (39487 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:7bdba5c9eac579fd0b10e268ca1fec4086ea6469060da3bdfa53bc092f9ac162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.2 MB (480172297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b746926470d747b7f372337893b2bb4dd1b39f191b724193ad6f3eac6dee636`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:26:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:26:04 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:26:04 GMT
ENV JAVA_VERSION=jdk-17.0.17+10_openj9-0.56.0
# Thu, 13 Nov 2025 23:26:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='56f11335a3c67f96f0dc8ca4ebe02239fa300fd871ab46de27103666998b2aec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cc9ac62b665c1c61860dbfe8d06f2f30d1f0439f1e93f6ae09770ca91949feb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='13c8bbbb9ffa57b33a48ca018fd281e69dd6fdbb4e96ca7df72a49db614d899c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='bc147228dc80b3add4a64b441cf3fe69e06b0b8ad3cd86444d7de2fd7c0fea86';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Nov 2025 23:26:07 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:26:07 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Nov 2025 23:26:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 14 Nov 2025 00:30:55 GMT
USER root
# Fri, 14 Nov 2025 00:30:55 GMT
ARG LIBERTY_VERSION=25.0.0.12-beta
# Fri, 14 Nov 2025 00:30:55 GMT
ARG LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5
# Fri, 14 Nov 2025 00:30:55 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip
# Fri, 14 Nov 2025 00:30:55 GMT
ARG LIBERTY_BUILD_LABEL=cl251120251020-0302
# Fri, 14 Nov 2025 00:30:55 GMT
ARG OPENJ9_SCC=true
# Fri, 14 Nov 2025 00:30:55 GMT
ARG VERBOSE=false
# Fri, 14 Nov 2025 00:30:55 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251120251020-0302 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.12-beta liberty.version=25.0.0.12-beta io.openliberty.version=25.0.0.12-beta
# Fri, 14 Nov 2025 00:30:55 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 14 Nov 2025 00:30:55 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 14 Nov 2025 00:30:55 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 14 Nov 2025 00:30:55 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 14 Nov 2025 00:31:16 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 14 Nov 2025 00:31:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 14 Nov 2025 00:31:16 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 14 Nov 2025 00:31:16 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 14 Nov 2025 00:31:42 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 14 Nov 2025 00:31:42 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 14 Nov 2025 00:31:42 GMT
USER 1001
# Fri, 14 Nov 2025 00:31:42 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 14 Nov 2025 00:31:42 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 14 Nov 2025 00:31:42 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4de0508d820199870bd9526fb7971ba639e12c5e59240c4d7b46465d9d9e77e`  
		Last Modified: Thu, 13 Nov 2025 23:26:59 GMT  
		Size: 12.1 MB (12130079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dbbc93653a34e268180a5212893ca6e44b9fa969e008d682881a08cf5abf94`  
		Last Modified: Thu, 13 Nov 2025 23:27:03 GMT  
		Size: 53.5 MB (53468115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9b00cfd87167f3c6d245a23ce981920902247b97461fa0cda28922bda8c871`  
		Last Modified: Thu, 13 Nov 2025 23:26:58 GMT  
		Size: 4.8 MB (4847896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3088d10e951f39badb2b7738b24ef5bbd0307bf97e81dad46738e8e442ba01af`  
		Last Modified: Fri, 14 Nov 2025 00:32:24 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb926cdabd860f89b0aac15f5e66a3c8076675d27a625087a6fe125dcdf0aa97`  
		Last Modified: Fri, 14 Nov 2025 00:32:24 GMT  
		Size: 12.3 KB (12285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee9db9d2ffcbc63447c1593e4a6667a1d17418ab53a61664ffd7d4f89ba6c3`  
		Last Modified: Fri, 14 Nov 2025 00:32:24 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b5dab7fdef9ed2a7c6ea8b2718aca7fe9516b3e50c2c48974fa811167db419`  
		Last Modified: Fri, 14 Nov 2025 00:32:24 GMT  
		Size: 42.3 KB (42321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98404bf2a6a438ad94fdc299a9a2d244e97bd07abfef4f93b040d62f372c8dac`  
		Last Modified: Fri, 14 Nov 2025 23:38:08 GMT  
		Size: 368.0 MB (367995295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a32bee34d908af323ed6ec33828e7995e09ceb6a661261b1f91a5bfaada235`  
		Last Modified: Fri, 14 Nov 2025 00:32:25 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba765de42208893e07889abe74eff50abc5ba6124cf6b539a6987b4e9ba59edb`  
		Last Modified: Fri, 14 Nov 2025 00:32:25 GMT  
		Size: 13.7 KB (13724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fad0499fa4f3a18211ed242caba4005334cc4e0342c7cad4b02df4db223120`  
		Last Modified: Fri, 14 Nov 2025 00:32:26 GMT  
		Size: 14.3 MB (14276359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:3a790f9f2099af91387988806ceb626ee4d31a75676977eb34a96b6e78dd8d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5829427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6cdd67fd3bccbea10a800bfd118329c6cb840bafd755fbdf9c52cca6cb41de`

```dockerfile
```

-	Layers:
	-	`sha256:5614cf657c56fb90c93a4ae435dca7d4ec140bbbb957d775fc6b8183d8090981`  
		Last Modified: Fri, 14 Nov 2025 03:51:43 GMT  
		Size: 5.8 MB (5789812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d7f9b2a7dfdfa5bd500e7c639e6fb54836b7cea7f65a78e8ac6413d6a28ffe6`  
		Last Modified: Fri, 14 Nov 2025 03:51:44 GMT  
		Size: 39.6 KB (39615 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:3e53b359f58c8823276da3a6e6989d22827ce1aecf792ae8e0f3b96a33664bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.3 MB (489279839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ddbaf247d4ca7bed1cb79821ac8b15f757fa7f7e44cae9fc174a364e9fec1f`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:37:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:37:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:19 GMT
ENV JAVA_VERSION=jdk-17.0.17+10_openj9-0.56.0
# Thu, 13 Nov 2025 23:53:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='56f11335a3c67f96f0dc8ca4ebe02239fa300fd871ab46de27103666998b2aec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cc9ac62b665c1c61860dbfe8d06f2f30d1f0439f1e93f6ae09770ca91949feb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='13c8bbbb9ffa57b33a48ca018fd281e69dd6fdbb4e96ca7df72a49db614d899c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='bc147228dc80b3add4a64b441cf3fe69e06b0b8ad3cd86444d7de2fd7c0fea86';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Nov 2025 23:53:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:53:22 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Nov 2025 23:53:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 14 Nov 2025 03:38:10 GMT
USER root
# Fri, 14 Nov 2025 03:38:10 GMT
ARG LIBERTY_VERSION=25.0.0.12-beta
# Fri, 14 Nov 2025 03:38:10 GMT
ARG LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5
# Fri, 14 Nov 2025 03:38:10 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip
# Fri, 14 Nov 2025 03:38:10 GMT
ARG LIBERTY_BUILD_LABEL=cl251120251020-0302
# Fri, 14 Nov 2025 03:38:10 GMT
ARG OPENJ9_SCC=true
# Fri, 14 Nov 2025 03:38:10 GMT
ARG VERBOSE=false
# Fri, 14 Nov 2025 03:38:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251120251020-0302 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.12-beta liberty.version=25.0.0.12-beta io.openliberty.version=25.0.0.12-beta
# Fri, 14 Nov 2025 03:38:10 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 14 Nov 2025 03:38:10 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 14 Nov 2025 03:38:11 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 14 Nov 2025 03:38:12 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 14 Nov 2025 03:38:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 14 Nov 2025 03:38:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 14 Nov 2025 03:38:39 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 14 Nov 2025 03:38:39 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 14 Nov 2025 03:39:21 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 14 Nov 2025 03:39:21 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 14 Nov 2025 03:39:21 GMT
USER 1001
# Fri, 14 Nov 2025 03:39:21 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 14 Nov 2025 03:39:21 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 14 Nov 2025 03:39:21 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28828c4219e6f91b491a0cc4ec95ce76d6f124150bfb43bfd907147824beaf5e`  
		Last Modified: Thu, 13 Nov 2025 23:38:45 GMT  
		Size: 12.9 MB (12893989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f50a314e72fb5b20233bc2f7d9fb05fc53a11f1b4a153f9395ea3eab20bfa1`  
		Last Modified: Thu, 13 Nov 2025 23:54:32 GMT  
		Size: 57.0 MB (57019156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1cd15e3d4895a47c9982c1564dab8dd580d0c5621bd457671bcc859a829614`  
		Last Modified: Thu, 13 Nov 2025 23:54:28 GMT  
		Size: 3.8 MB (3847115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b4de214901cd102a6662c9be503c5fe18a84ad72383b86007c2cd12590c6e0`  
		Last Modified: Fri, 14 Nov 2025 03:40:39 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f429ace2d30a4051c1862beac27a7e41d5b9279665e58713ca69314a9d90c20e`  
		Last Modified: Fri, 14 Nov 2025 03:40:39 GMT  
		Size: 12.3 KB (12280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b267ac8dfb4b5e287b7c6c88e60850b56846632d16faf8c3f447d8a6db084f`  
		Last Modified: Fri, 14 Nov 2025 03:40:39 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c82a6c40df64bf4bd386bac2026d96508b8e442feff8fa749f87939828408a5`  
		Last Modified: Fri, 14 Nov 2025 03:40:39 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2360c1c5fd9892b03b63c19ba336ea9e4030f359497a65dc5d54156f1d6fbdfd`  
		Last Modified: Fri, 14 Nov 2025 23:33:44 GMT  
		Size: 368.0 MB (367995625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4c0d7114b48ef4bce402d884b1214f98bb9f8c57123c27b4f9dc2719330e60`  
		Last Modified: Fri, 14 Nov 2025 03:40:39 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b4d4bf4b905ce2c1aa522753178b94ea45742dd7195bf1d879e5fee8adf1ea`  
		Last Modified: Fri, 14 Nov 2025 03:40:40 GMT  
		Size: 13.7 KB (13724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286616365b260da028cec14900f5936ad509f1b1e0168c295f6ca131ff98473f`  
		Last Modified: Fri, 14 Nov 2025 03:40:41 GMT  
		Size: 13.0 MB (13012392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:15a7902a9d168a352036547c0a8f3f15f0402554ec6fcb4d07c86619308db1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5835594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11488db66c1d8862be34bea9214fd0e9befae6f2128c220a2013ee0a549ece05`

```dockerfile
```

-	Layers:
	-	`sha256:28f1df5c30930c76de010dde24e9935cfb0237cb4834a70de7261b159bebee1f`  
		Last Modified: Fri, 14 Nov 2025 06:48:24 GMT  
		Size: 5.8 MB (5796073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:785d4c505aea90fab4ee9f1c3e9f57495165decb409719fded965d9d55017776`  
		Last Modified: Fri, 14 Nov 2025 06:48:25 GMT  
		Size: 39.5 KB (39521 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; s390x

```console
$ docker pull open-liberty@sha256:d6f4013931dc22462c96bbd3428623348ded012624893a019875cb12d63ce0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.6 MB (482555022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2609e8e938ecffe92806ad730fbcfd6f04e438969cf7c26883e774e16aa248a4`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:13:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:13:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:13:26 GMT
ENV JAVA_VERSION=jdk-17.0.17+10_openj9-0.56.0
# Thu, 13 Nov 2025 23:17:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='56f11335a3c67f96f0dc8ca4ebe02239fa300fd871ab46de27103666998b2aec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cc9ac62b665c1c61860dbfe8d06f2f30d1f0439f1e93f6ae09770ca91949feb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='13c8bbbb9ffa57b33a48ca018fd281e69dd6fdbb4e96ca7df72a49db614d899c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='bc147228dc80b3add4a64b441cf3fe69e06b0b8ad3cd86444d7de2fd7c0fea86';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Nov 2025 23:17:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:17:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Nov 2025 23:17:34 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 14 Nov 2025 00:23:59 GMT
USER root
# Fri, 14 Nov 2025 00:23:59 GMT
ARG LIBERTY_VERSION=25.0.0.12-beta
# Fri, 14 Nov 2025 00:23:59 GMT
ARG LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5
# Fri, 14 Nov 2025 00:23:59 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip
# Fri, 14 Nov 2025 00:23:59 GMT
ARG LIBERTY_BUILD_LABEL=cl251120251020-0302
# Fri, 14 Nov 2025 00:23:59 GMT
ARG OPENJ9_SCC=true
# Fri, 14 Nov 2025 00:23:59 GMT
ARG VERBOSE=false
# Fri, 14 Nov 2025 00:23:59 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251120251020-0302 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.12-beta liberty.version=25.0.0.12-beta io.openliberty.version=25.0.0.12-beta
# Fri, 14 Nov 2025 00:23:59 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 14 Nov 2025 00:23:59 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 14 Nov 2025 00:23:59 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 14 Nov 2025 00:23:59 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 14 Nov 2025 00:24:14 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 14 Nov 2025 00:24:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 14 Nov 2025 00:24:14 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 14 Nov 2025 00:24:14 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 14 Nov 2025 00:24:39 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 14 Nov 2025 00:24:39 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 14 Nov 2025 00:24:39 GMT
USER 1001
# Fri, 14 Nov 2025 00:24:39 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 14 Nov 2025 00:24:39 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 14 Nov 2025 00:24:39 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ebf2f3fd42b59c867dbc8ee4d6fb881babedba503d35eec208ade18e4a3820`  
		Last Modified: Thu, 13 Nov 2025 23:14:34 GMT  
		Size: 12.2 MB (12219661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643db97244a4b9ad00c155561851c5bf7707bc724245c4e578ee9b8832a3bb3b`  
		Last Modified: Thu, 13 Nov 2025 23:18:04 GMT  
		Size: 54.2 MB (54201914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36379231f1f7cacfe784fdcb94367c6d6edd366528b4f5fcae5d3164a89bbca`  
		Last Modified: Thu, 13 Nov 2025 23:18:01 GMT  
		Size: 5.2 MB (5197553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24848187883f0192c6fdcc13ec9f0187bfe46e44b1067d46b6a7387333c77c6c`  
		Last Modified: Fri, 14 Nov 2025 00:25:23 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c0c80974e77ffc5b7d1b574b9f5d6048ac7fd5fea4a612139316c4731ae2c3`  
		Last Modified: Fri, 14 Nov 2025 00:25:23 GMT  
		Size: 12.3 KB (12280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b36b94909a7a67110b2a44f45916573f2916132ffdf12c46ae9c7cf0d06e210`  
		Last Modified: Fri, 14 Nov 2025 00:25:23 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536361166e7526d5d6ceff299474d705d3289cfd138a628a86c33819b9d99dfd`  
		Last Modified: Fri, 14 Nov 2025 00:25:23 GMT  
		Size: 33.1 KB (33111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d509797e0b15c7caefd39153122ba0fa55ab41a64743331e38ef2acbebc629`  
		Last Modified: Thu, 27 Nov 2025 21:23:33 GMT  
		Size: 368.0 MB (367994804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7641bbe946bdd93fec32bfe765dc3621bee034a1ea888d6af1073fd9aceb8ad1`  
		Last Modified: Fri, 14 Nov 2025 00:25:24 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72fbb7c4057a5e018e5a206d5ad1e71250b218c95321e431aba2cfaa08d8b67`  
		Last Modified: Fri, 14 Nov 2025 00:25:24 GMT  
		Size: 13.7 KB (13719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c7ddcb6d72decd414508ecf0cee47b37fce3e37a3ebf0ff1277578f4e83d04`  
		Last Modified: Fri, 14 Nov 2025 00:25:25 GMT  
		Size: 14.9 MB (14876350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:9cda2028053b3c22ed14e6805a23c928a6601f7d9d352277b401c77b9e09dcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5831956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3f620c95fab9ea6f26c0b91c223fdcfeee3f1e38ff6ad7efa3e7c51804483a`

```dockerfile
```

-	Layers:
	-	`sha256:9e84c82886e5d428fa0ce62c257a5f9a101a95cda557a5549100a9e8a8871b95`  
		Last Modified: Fri, 14 Nov 2025 03:51:55 GMT  
		Size: 5.8 MB (5792469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa457f4c5b4f7214db6562c6712b3fc777b2c96f985777843f42e81837f42527`  
		Last Modified: Fri, 14 Nov 2025 03:51:55 GMT  
		Size: 39.5 KB (39487 bytes)  
		MIME: application/vnd.in-toto+json
