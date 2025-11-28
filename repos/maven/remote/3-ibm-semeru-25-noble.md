## `maven:3-ibm-semeru-25-noble`

```console
$ docker pull maven@sha256:79ad1c380b25b622d81643f6d47fcb55ee6281977320d69b3efb50d0982fe9ef
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

### `maven:3-ibm-semeru-25-noble` - linux; amd64

```console
$ docker pull maven@sha256:9cafdfff98fac4a42468096af74ab3872625321a0ed4436ea7708e2e0d881af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328404142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54380a0b0c58c1b6ad6c5a6acc1335580aa599b840da48591eb97a826054c93d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Thu, 13 Nov 2025 23:26:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:26:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:26:11 GMT
ENV JAVA_VERSION=jdk-25.0.1+8_openj9-0.56.0
# Thu, 13 Nov 2025 23:27:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a646d2925bff9772aea6ed7aa88ca8e7a44c79ea8ac8432a6eb9239c3ddc78ea';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.1%2B8_openj9-0.56.0/ibm-semeru-open-jdk_aarch64_linux_25.0.1_8_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='827cd477c672b8280646ef5d52421fef8d0c8f24bf43c2a83031fadaf28dad19';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.1%2B8_openj9-0.56.0/ibm-semeru-open-jdk_x64_linux_25.0.1_8_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='eb14a211581c88e83912296794aec6efe8946c491db3190131b9ce9da587f43d';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.1%2B8_openj9-0.56.0/ibm-semeru-open-jdk_ppc64le_linux_25.0.1_8_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='4d2131798cf1589adce52f7c2f7afe17951430bee04165ff4d6a90e24b057426';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.1%2B8_openj9-0.56.0/ibm-semeru-open-jdk_s390x_linux_25.0.1_8_openj9-0.56.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Nov 2025 23:27:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:27:26 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Nov 2025 23:27:57 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 13 Nov 2025 23:27:57 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 01:41:42 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:41:43 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:41:43 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:41:43 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:41:43 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:41:43 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:41:43 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:41:43 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:41:43 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:41:43 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:41:43 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:41:43 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:41:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:41:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:41:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2037978b1357168ade07a7e5caded43d9c65bc80bb7e096c0ce346a859a402`  
		Last Modified: Thu, 13 Nov 2025 23:27:05 GMT  
		Size: 12.8 MB (12796512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527a3258c8f093151240cece6847f47afb735c34550da84e59ebaf8601d163c8`  
		Last Modified: Fri, 14 Nov 2025 01:41:28 GMT  
		Size: 247.2 MB (247184651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92dacd27ff4438938976af52f567439fedf4f2f5a47faf43fb3668f4a764844`  
		Last Modified: Thu, 13 Nov 2025 23:28:29 GMT  
		Size: 6.9 MB (6888265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7a6eb0d530c0ab54f024990ff15ac0253a664ac6c6979b7f97a3ec21f03742`  
		Last Modified: Fri, 14 Nov 2025 01:42:04 GMT  
		Size: 22.6 MB (22566413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f36e3b683992968e5db4649352d4795d1f95c33468ae05eae9dd594d539ae11`  
		Last Modified: Fri, 14 Nov 2025 01:42:03 GMT  
		Size: 9.2 MB (9242572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affc0de97c34373dff80613cca2d966d879f8a055c0c61a67b10c68ddb3afebb`  
		Last Modified: Fri, 14 Nov 2025 01:42:02 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f426f07aa196c4f26c51fb72290c501dbb69700e411dccb7295365133b2b90`  
		Last Modified: Fri, 14 Nov 2025 01:42:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-25-noble` - unknown; unknown

```console
$ docker pull maven@sha256:e8e5c15df853bf8353cb9aed40b2be287f01d2c3fa99555734d6bd9756669885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4802148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a3bb76969caace41a5ce2251f62f5f865f699228c97fe32f784ccc46cf41e5`

```dockerfile
```

-	Layers:
	-	`sha256:602deb2880be0ff2fc0461cb3fcfd072383f75e4d52a425e812400848adfb572`  
		Last Modified: Fri, 14 Nov 2025 03:32:06 GMT  
		Size: 4.8 MB (4783094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c276459596a4be1f92fec9dfc69eaf9167a4bf72d8cf02a55761f912d0e86634`  
		Last Modified: Fri, 14 Nov 2025 03:32:07 GMT  
		Size: 19.1 KB (19054 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-25-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:482743fe00a80023422a1c9bb43777242b406b84f500c45eeda6d0c7c4a9c8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.5 MB (323541052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb30e830af98ad77e040323f12a32949a0cc42877f64c4f72f2644fa08f78dde`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Thu, 13 Nov 2025 23:25:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:25:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:25:43 GMT
ENV JAVA_VERSION=jdk-25.0.1+8_openj9-0.56.0
# Thu, 13 Nov 2025 23:27:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a646d2925bff9772aea6ed7aa88ca8e7a44c79ea8ac8432a6eb9239c3ddc78ea';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.1%2B8_openj9-0.56.0/ibm-semeru-open-jdk_aarch64_linux_25.0.1_8_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='827cd477c672b8280646ef5d52421fef8d0c8f24bf43c2a83031fadaf28dad19';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.1%2B8_openj9-0.56.0/ibm-semeru-open-jdk_x64_linux_25.0.1_8_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='eb14a211581c88e83912296794aec6efe8946c491db3190131b9ce9da587f43d';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.1%2B8_openj9-0.56.0/ibm-semeru-open-jdk_ppc64le_linux_25.0.1_8_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='4d2131798cf1589adce52f7c2f7afe17951430bee04165ff4d6a90e24b057426';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.1%2B8_openj9-0.56.0/ibm-semeru-open-jdk_s390x_linux_25.0.1_8_openj9-0.56.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Nov 2025 23:27:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:27:09 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Nov 2025 23:27:41 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 13 Nov 2025 23:27:41 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 01:59:07 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:59:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:59:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:59:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:59:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:59:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:59:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:59:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:59:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:59:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:59:07 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:59:07 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:59:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:59:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:59:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f9cd44c03f1237cd9710d8fa5fb29c4209986d06e959446c3ae80833e6a780`  
		Last Modified: Thu, 13 Nov 2025 23:26:51 GMT  
		Size: 12.8 MB (12831484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfe5b4209878ba9d415cec80040c143bcec033b20b94f99a2569e4f2bea391f`  
		Last Modified: Fri, 14 Nov 2025 01:58:51 GMT  
		Size: 243.4 MB (243398151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03cff8df418c63402fa7790e444605ca620bb7d454b6540a4ea7cb869206f41`  
		Last Modified: Thu, 13 Nov 2025 23:28:14 GMT  
		Size: 6.6 MB (6570605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917d516c9982fde119abdeca2dc932e3b1fea103d9303caff23e28ff9bf77cbd`  
		Last Modified: Fri, 14 Nov 2025 01:59:29 GMT  
		Size: 22.6 MB (22635245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30d8f08db683e626008cdeec6ac04d86b1a92ed69e54fa0db05dc60180f59d6`  
		Last Modified: Fri, 14 Nov 2025 01:59:29 GMT  
		Size: 9.2 MB (9242571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ede76717a05121cb97a8633bb6588a14424463eee6dfb8da41234667056bac`  
		Last Modified: Fri, 14 Nov 2025 01:59:28 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad489c951398ba4e1c7fcb2dc4f1cbfd3433c718e79e49b3357b03cdaa9d618`  
		Last Modified: Fri, 14 Nov 2025 01:59:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-25-noble` - unknown; unknown

```console
$ docker pull maven@sha256:0e34c7ce95200495c78899bfdd6e0e0dcab88dc7f09200836faa4f5b5e77a237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4807510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c20f55e80499efa556e3ed378428ed752c4035b7425174a66deba359fd00d5e`

```dockerfile
```

-	Layers:
	-	`sha256:24fdf6d4dc3d9ab5e4c31e3b9dfd544a7e11f42d7ccaaab5b7a32d7788ba7c48`  
		Last Modified: Fri, 14 Nov 2025 03:32:11 GMT  
		Size: 4.8 MB (4788323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b46c0af9a513d4bc7f27153d82efe1929e5d0a0143f7451971619bc618231389`  
		Last Modified: Fri, 14 Nov 2025 03:32:12 GMT  
		Size: 19.2 KB (19187 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-25-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:411a971854b4689a65d863fcbbc2e08a68a82a3ae9c3d6b43609ae33e4e3a218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340524090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c70c399b046d363f3443f6d809c1884df3d5bf5c98c45992c44e7505813b5d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Thu, 13 Nov 2025 23:39:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:39:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:39:21 GMT
ENV JAVA_VERSION=jdk-25.0.1+8_openj9-0.56.0
# Fri, 14 Nov 2025 00:04:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a646d2925bff9772aea6ed7aa88ca8e7a44c79ea8ac8432a6eb9239c3ddc78ea';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.1%2B8_openj9-0.56.0/ibm-semeru-open-jdk_aarch64_linux_25.0.1_8_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='827cd477c672b8280646ef5d52421fef8d0c8f24bf43c2a83031fadaf28dad19';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.1%2B8_openj9-0.56.0/ibm-semeru-open-jdk_x64_linux_25.0.1_8_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='eb14a211581c88e83912296794aec6efe8946c491db3190131b9ce9da587f43d';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.1%2B8_openj9-0.56.0/ibm-semeru-open-jdk_ppc64le_linux_25.0.1_8_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='4d2131798cf1589adce52f7c2f7afe17951430bee04165ff4d6a90e24b057426';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.1%2B8_openj9-0.56.0/ibm-semeru-open-jdk_s390x_linux_25.0.1_8_openj9-0.56.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 14 Nov 2025 00:04:56 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:04:56 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 14 Nov 2025 00:05:29 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 14 Nov 2025 00:05:29 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 14:36:21 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 14:36:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 14:36:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 14:36:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 14:36:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 14:36:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 14:36:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 14:36:23 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 14:36:23 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 14:36:23 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 14:36:23 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 14:36:23 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 14:36:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 14:36:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 14:36:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a76c425c79bf766b59c998d5db4eb2aa18eff8ad07eb7fc0177fa2aa73a414`  
		Last Modified: Thu, 13 Nov 2025 23:40:42 GMT  
		Size: 13.8 MB (13795716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8eafa6413031c9ace17c4b0cc6ba1fc67c0171e015a951a78ac76619f464e0`  
		Last Modified: Fri, 14 Nov 2025 23:32:55 GMT  
		Size: 251.1 MB (251071629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46b6951d5064e10d79bb89be14ea7d087f29c8f7023acbd2f96017804aff1cf`  
		Last Modified: Fri, 14 Nov 2025 00:06:25 GMT  
		Size: 5.5 MB (5496704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f2cc45597d6c83b506571654e82f2f99ef04a369e2adc78bd132a2af3ae61c`  
		Last Modified: Fri, 14 Nov 2025 14:37:08 GMT  
		Size: 26.6 MB (26612002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c452f30569cdfa251ca3f0e2982c6fbb5ed72303c018eb839bce7574e9473fe9`  
		Last Modified: Fri, 14 Nov 2025 14:37:07 GMT  
		Size: 9.2 MB (9242574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2090cacce936bcddc2ae10b336a7835e1e925220ecb8b2a77dc4c0818631ed8`  
		Last Modified: Fri, 14 Nov 2025 14:37:05 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7309c70a878f79e5bab1db566407b43331816e5cbf3d77de3f648cbdb4dfbdb2`  
		Last Modified: Fri, 14 Nov 2025 14:37:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-25-noble` - unknown; unknown

```console
$ docker pull maven@sha256:50a286d096d0ed7bd1a0f0c1e85d24171375f15daf30e26ff4d5f01427300ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4809621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2b0d252e2b10e248810f14ee82a129ce4e189e9c1f1c2bdede507dcdf8aaab`

```dockerfile
```

-	Layers:
	-	`sha256:7532872afa18c2bc709f39fad85bea64a2a699959b0ea03a242fa04c6420f68c`  
		Last Modified: Fri, 14 Nov 2025 15:28:45 GMT  
		Size: 4.8 MB (4790517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5745e7942b2880ec2e87def8b5bde6d37c7077bb600a82d846d6fa65a61147db`  
		Last Modified: Fri, 14 Nov 2025 15:28:46 GMT  
		Size: 19.1 KB (19104 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-25-noble` - linux; s390x

```console
$ docker pull maven@sha256:b6d7cefc9e0902cb87a159cfe706ec88fe7c42e5a82735ef1f5cafea931d9d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.9 MB (327860041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651db9c7130260550dd4c613ed496c2a536ffab59ece8b6603bf21fc8aaf51bf`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Thu, 13 Nov 2025 23:14:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:14:28 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:14:28 GMT
ENV JAVA_VERSION=jdk-25.0.1+8_openj9-0.56.0
# Thu, 13 Nov 2025 23:20:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a646d2925bff9772aea6ed7aa88ca8e7a44c79ea8ac8432a6eb9239c3ddc78ea';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.1%2B8_openj9-0.56.0/ibm-semeru-open-jdk_aarch64_linux_25.0.1_8_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='827cd477c672b8280646ef5d52421fef8d0c8f24bf43c2a83031fadaf28dad19';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.1%2B8_openj9-0.56.0/ibm-semeru-open-jdk_x64_linux_25.0.1_8_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='eb14a211581c88e83912296794aec6efe8946c491db3190131b9ce9da587f43d';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.1%2B8_openj9-0.56.0/ibm-semeru-open-jdk_ppc64le_linux_25.0.1_8_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='4d2131798cf1589adce52f7c2f7afe17951430bee04165ff4d6a90e24b057426';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.1%2B8_openj9-0.56.0/ibm-semeru-open-jdk_s390x_linux_25.0.1_8_openj9-0.56.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Nov 2025 23:20:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Nov 2025 23:20:35 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 13 Nov 2025 23:20:35 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 02:32:57 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 02:32:57 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 02:32:57 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 02:32:57 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 02:32:57 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 02:32:57 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 02:32:57 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 02:32:57 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 02:32:57 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 02:32:57 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 02:32:57 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 02:32:57 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 02:32:57 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 02:32:57 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 02:32:57 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7d5b0205a5ff16c2b58f20a113b5eb9a80393a644df077beab5d90635153dc66`  
		Last Modified: Thu, 16 Oct 2025 21:17:39 GMT  
		Size: 29.9 MB (29907597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3489841bfd89671b4443c187c254bddeaa7431d89f7c42e83eed1c8b7587e15c`  
		Last Modified: Thu, 13 Nov 2025 23:15:25 GMT  
		Size: 13.1 MB (13120792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa93b8b5308306627e6fc41b39ef9067dae78f32c4fa6b153b75b803743178a`  
		Last Modified: Fri, 14 Nov 2025 02:32:54 GMT  
		Size: 244.9 MB (244899892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f57f40e84e6922064427df3406f18ff9b4eb076a0903c99518bbee2c20ceca`  
		Last Modified: Thu, 13 Nov 2025 23:21:14 GMT  
		Size: 7.0 MB (6992329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bece97213ed60c35f62879cee574604f95267ccb31cf6c36395f0e4a58e3b6d`  
		Last Modified: Fri, 14 Nov 2025 02:33:23 GMT  
		Size: 23.7 MB (23695812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe97fdcd214929e688b3c419999f666b9c847b57cb7613d36a29b2e469b18cb`  
		Last Modified: Fri, 14 Nov 2025 02:33:22 GMT  
		Size: 9.2 MB (9242580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65d7ef5339618fb24c43e5b8e5fb119503c9470cdabf8bc4ede5952f21eea87`  
		Last Modified: Fri, 14 Nov 2025 02:33:20 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6169fdb43a31e5b725cbc8ed8b8c9598dd9f3f33fea6a685ed040e2948b73f`  
		Last Modified: Fri, 14 Nov 2025 02:33:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-25-noble` - unknown; unknown

```console
$ docker pull maven@sha256:42975314a56574e4a0fae858c3d0b73b718cff9e12abdd61ccb482495d93cfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4804561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18d605512789c381341cd243518c79f481f33c30f0768ec6ee118dc040b16d0`

```dockerfile
```

-	Layers:
	-	`sha256:3a68d59f0c735ae6301c5707950fd3659a6159d4db237b2672fdb88c698ea6c6`  
		Last Modified: Fri, 14 Nov 2025 03:32:20 GMT  
		Size: 4.8 MB (4785507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c13a6b37022e514be276bb171374dd855543c03eec4f5b8ea1f74ad876c3fe7f`  
		Last Modified: Fri, 14 Nov 2025 03:32:21 GMT  
		Size: 19.1 KB (19054 bytes)  
		MIME: application/vnd.in-toto+json
