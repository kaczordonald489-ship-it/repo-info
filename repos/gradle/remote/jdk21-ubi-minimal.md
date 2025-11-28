## `gradle:jdk21-ubi-minimal`

```console
$ docker pull gradle@sha256:9049dc0698f42c2c1cd5c45a8e8a34f86602e7dd9a217e65da899e5077be3c21
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

### `gradle:jdk21-ubi-minimal` - linux; amd64

```console
$ docker pull gradle@sha256:d8182d8dd88fd697bfce71775d672336b42527b62911747e7a4a210103e5ca0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.1 MB (398116250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa26d0178956dc351d4637066f765ed64ad6848daeb09c2b0c7e70a529eacd53`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 17 Nov 2025 06:51:18 GMT
ENV container oci
# Mon, 17 Nov 2025 06:51:19 GMT
COPY dir:7cf80e1c5cade8bdab1a4d70632d27e8826f968a3bd11979550b2850547e929b in /      
# Mon, 17 Nov 2025 06:51:19 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 06:51:19 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 06:51:19 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 06:51:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 06:51:20 GMT
COPY file:fde1a325755d265b4b09b708d833ef4334fd28d3649fcb5f69929257ca8b0d53 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:51:20 GMT
COPY file:fde1a325755d265b4b09b708d833ef4334fd28d3649fcb5f69929257ca8b0d53 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:51:20 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "org.opencontainers.image.revision"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "build-date"="2025-11-17T06:51:01Z" "release"="1763362218"org.opencontainers.image.revision=f7f5876a3d86ded473c14b11d7491c2b6ddf39ce
# Mon, 17 Nov 2025 23:14:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:14:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:14:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:14:01 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:14:01 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Mon, 17 Nov 2025 23:14:08 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 17 Nov 2025 23:14:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:14:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:14:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 17 Nov 2025 23:14:10 GMT
CMD ["jshell"]
# Tue, 18 Nov 2025 02:43:36 GMT
CMD ["gradle"]
# Tue, 18 Nov 2025 02:43:36 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Nov 2025 02:43:36 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 18 Nov 2025 02:43:36 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Nov 2025 02:43:36 GMT
WORKDIR /home/gradle
# Tue, 18 Nov 2025 02:43:40 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 18 Nov 2025 02:43:40 GMT
ENV GRADLE_VERSION=9.2.1
# Tue, 18 Nov 2025 02:43:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Tue, 18 Nov 2025 02:43:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 18 Nov 2025 02:43:43 GMT
USER gradle
# Tue, 18 Nov 2025 02:43:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 18 Nov 2025 02:43:43 GMT
USER root
```

-	Layers:
	-	`sha256:7d6ca59745ac48971cbc2d72b53fe413144fa5c0c21f2ef1d7aaf1291851e501`  
		Last Modified: Mon, 17 Nov 2025 07:24:40 GMT  
		Size: 40.0 MB (39979464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac35a9086343155326175e8a7ef27bc64f6726ee9dfb02cd366794d8627c2df2`  
		Last Modified: Mon, 17 Nov 2025 23:14:50 GMT  
		Size: 27.7 MB (27696886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac0bd62376d6db417e8b48d48564238aa0eb1932e2ea6a255599ffb1bc3a013`  
		Last Modified: Tue, 18 Nov 2025 01:17:57 GMT  
		Size: 157.8 MB (157828902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416154aa86490b164585bd5573e4dac124faa2505b42cb53159f3b5238e3e358`  
		Last Modified: Mon, 17 Nov 2025 23:14:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005d79bb49ca5bcf33453264cfa5920048e044b63438767d3df68f9081b83b4e`  
		Last Modified: Mon, 17 Nov 2025 23:14:44 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb4bf814e2f815afc420f6f615f546b9b285d3de9ddfea9b253af1323620d9b`  
		Last Modified: Tue, 18 Nov 2025 02:44:11 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc35216898af4194bcb3fb922747ce9f91adff9c7dce4a3135d14221915b53a2`  
		Last Modified: Tue, 18 Nov 2025 02:44:18 GMT  
		Size: 37.0 MB (37029966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0b55d6c7a5d4a55315382fcc80799b5e0a8244a2206ae9c22e24eb260457bd`  
		Last Modified: Tue, 18 Nov 2025 04:55:05 GMT  
		Size: 135.5 MB (135521971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5365396aabf1469ffc4107cf7c66c4c7af80e05faccdebfbe039c225c45ed373`  
		Last Modified: Tue, 18 Nov 2025 02:44:11 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:98e8d066a8e853b6ee2e4c3658ab25fbd4f858c6ab48fd4f9aedc9fd8ff1b232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5425158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d036348cb661eb60b076f812c67e2ce2d8754ae1e4d719b972cdebc4e593c223`

```dockerfile
```

-	Layers:
	-	`sha256:d08e3c5da0792b06323ba89d7ee1479299e0bca054ab8da6ea6b7f7ae96078b8`  
		Last Modified: Tue, 18 Nov 2025 03:27:46 GMT  
		Size: 5.4 MB (5400666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e6cb050c5a02db0479652a10dbc467eb51e985f7dc83ce19fa263cfac1b3c23`  
		Last Modified: Tue, 18 Nov 2025 03:27:47 GMT  
		Size: 24.5 KB (24492 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi-minimal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b5c5bee6e0ad1988e94815bcc1ad01191536e8e306b066b5c89c6ce0b1830ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.4 MB (394442025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dea29548aecf2a37250f614df54b8522bf7b6882ce1cd5116214fdea81d186c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 17 Nov 2025 06:55:56 GMT
ENV container oci
# Mon, 17 Nov 2025 06:55:57 GMT
COPY dir:87932faf9829020ce186f9ca70767f10cf2708680f90badc643a8b214cc3a6f7 in /      
# Mon, 17 Nov 2025 06:55:57 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 06:55:57 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 06:55:57 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 06:55:58 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 06:55:58 GMT
COPY file:9de94f07a9e32b6295a1e34d66c814b476f5c78f9e3d5d56a9c5024309f451a8 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:55:58 GMT
COPY file:9de94f07a9e32b6295a1e34d66c814b476f5c78f9e3d5d56a9c5024309f451a8 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:55:58 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "org.opencontainers.image.revision"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "build-date"="2025-11-17T06:55:41Z" "release"="1763362218"org.opencontainers.image.revision=f7f5876a3d86ded473c14b11d7491c2b6ddf39ce
# Mon, 17 Nov 2025 23:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:14:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:14:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:14:18 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Mon, 17 Nov 2025 23:17:12 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 17 Nov 2025 23:17:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:17:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:17:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 17 Nov 2025 23:17:13 GMT
CMD ["jshell"]
# Mon, 17 Nov 2025 23:29:27 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 23:29:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 23:29:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 23:29:27 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 23:29:27 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 23:29:33 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 17 Nov 2025 23:29:33 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 23:29:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 23:29:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 23:29:35 GMT
USER gradle
# Mon, 17 Nov 2025 23:29:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 23:29:36 GMT
USER root
```

-	Layers:
	-	`sha256:3c0c9428a7f3bd24ecc53d01a84f8e5daf4cde2806733046039c236a5821dc20`  
		Last Modified: Mon, 17 Nov 2025 07:42:16 GMT  
		Size: 38.2 MB (38200298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f2514a047dd3d883e0f12397e04edec140e772c415aaf07e9596a71ad83f32`  
		Last Modified: Mon, 17 Nov 2025 23:14:57 GMT  
		Size: 28.1 MB (28130081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e069df6cc4239010d66cd95363a1a7565557835501702f2c954aa39a222ebad`  
		Last Modified: Mon, 17 Nov 2025 23:29:24 GMT  
		Size: 156.1 MB (156111826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b029e0ec740567e5d5a75e0c570590dad6e252122758eea1e00a8ac2f2067e09`  
		Last Modified: Mon, 17 Nov 2025 23:17:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b0e44cab4dcb89dd0279812371d958cfdfa5fa0e5b5ab5d40ce7eaab9a3949`  
		Last Modified: Mon, 17 Nov 2025 23:17:31 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5ed1b76065c2423fad18206564030ba6e721d0ad64c79ff97c8aacbcbe5dc6`  
		Last Modified: Mon, 17 Nov 2025 23:30:02 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb3748218903b86e16d53eac3afcc1116d3f39c373bb3d029fe71363b443c58`  
		Last Modified: Mon, 17 Nov 2025 23:30:06 GMT  
		Size: 36.4 MB (36414158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07426a4b0f92de054947a8757437ac34e86238addc70d9a0008ee863be04cec`  
		Last Modified: Tue, 18 Nov 2025 02:12:41 GMT  
		Size: 135.5 MB (135521968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb2af99bdfd040c937220c9d2ae7a52c8a99d1925a6613fe377ba35fde747e5`  
		Last Modified: Mon, 17 Nov 2025 23:30:02 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:3f0e20f4969791cdfcb6e9d22583ca42c3ba017b5ec228178da672612dd28aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5424820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376cb6aa4440bb00096a17d460d57d3ed0851b1bf1bd5dcf14d95e31c21e44c6`

```dockerfile
```

-	Layers:
	-	`sha256:cc6082d9f2f611a4b036e269c4a924a4ddf4cf904839e4b3cea294c78fe0d550`  
		Last Modified: Tue, 18 Nov 2025 00:24:04 GMT  
		Size: 5.4 MB (5400096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4250ee52ffda592b6a84247830edc68bda6786dc11d8b19546c42609fcacef82`  
		Last Modified: Tue, 18 Nov 2025 00:24:05 GMT  
		Size: 24.7 KB (24724 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi-minimal` - linux; ppc64le

```console
$ docker pull gradle@sha256:ee4caddf69f5988ceef6dd8f09e5d3e9be90d7083bf31d7c299f0ee96998e351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.4 MB (406367444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16986cd7f4f23ce32623611f18c0186923a1cadc22f1d2fe9736d62b56fa1d9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 17 Nov 2025 06:52:34 GMT
ENV container oci
# Mon, 17 Nov 2025 06:52:35 GMT
COPY dir:9a9add289f1055504c42bfa45e0dd9890598235dacbc2320fb6adf8f7795427f in /      
# Mon, 17 Nov 2025 06:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 06:52:35 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 06:52:35 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 06:52:35 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 06:52:35 GMT
COPY file:df039a12e94c358b58fd977c386a5daf1a5d5ee9447df76db2fd5246917af6b7 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:52:35 GMT
COPY file:df039a12e94c358b58fd977c386a5daf1a5d5ee9447df76db2fd5246917af6b7 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:52:36 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "org.opencontainers.image.revision"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "build-date"="2025-11-17T06:52:24Z" "release"="1763362218"org.opencontainers.image.revision=f7f5876a3d86ded473c14b11d7491c2b6ddf39ce
# Mon, 17 Nov 2025 23:18:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:18:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:18:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:18:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:18:50 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Mon, 17 Nov 2025 23:28:35 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 17 Nov 2025 23:28:37 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:28:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:28:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 17 Nov 2025 23:28:38 GMT
CMD ["jshell"]
# Tue, 18 Nov 2025 00:01:12 GMT
CMD ["gradle"]
# Tue, 18 Nov 2025 00:01:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Nov 2025 00:01:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 18 Nov 2025 00:01:12 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Nov 2025 00:01:13 GMT
WORKDIR /home/gradle
# Tue, 18 Nov 2025 00:01:33 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 18 Nov 2025 00:01:33 GMT
ENV GRADLE_VERSION=9.2.1
# Tue, 18 Nov 2025 00:01:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Tue, 18 Nov 2025 00:01:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 18 Nov 2025 00:01:41 GMT
USER gradle
# Tue, 18 Nov 2025 00:01:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 18 Nov 2025 00:01:42 GMT
USER root
```

-	Layers:
	-	`sha256:6fccaa32330f08c5e0cbe4fb16bd3e3944f9e113abfe46581e3f895ddfc1db49`  
		Last Modified: Mon, 17 Nov 2025 12:10:03 GMT  
		Size: 44.4 MB (44431008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ae5c71fee127db36920f76d71bcf3210a5ea9baf4a783f6ef553746a98cae7`  
		Last Modified: Mon, 17 Nov 2025 23:19:50 GMT  
		Size: 30.1 MB (30124462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fe34e19b835edfa269f0cfeecab66ed2aba4eaf1b914ea9f55e50ad97052c0`  
		Last Modified: Tue, 18 Nov 2025 02:52:14 GMT  
		Size: 157.9 MB (157943397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4737fa5197b40b128aa9715f5deb3510cea6365eba7f8a3c736b7bf01ade6f59`  
		Last Modified: Mon, 17 Nov 2025 23:29:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dc1ac416e958498e7389ce18fdbab2c412c091098b258163283b703b4a339d`  
		Last Modified: Mon, 17 Nov 2025 23:29:29 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e9fac7c2dfb2fa3a78f5b0980b36f6c61c69dff1129b5dd32793b8645b66b2`  
		Last Modified: Tue, 18 Nov 2025 00:02:41 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca9c59a8793d7fca8b05f184e60b2b437d2dcc8eef6db645e91a55d742c4b01`  
		Last Modified: Tue, 18 Nov 2025 00:02:46 GMT  
		Size: 38.3 MB (38307436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29889769a024f91923e7733d3126beae9a120ef83cf90b234b44bb51966494d9`  
		Last Modified: Tue, 18 Nov 2025 20:40:03 GMT  
		Size: 135.5 MB (135521968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6480504002ff9322933510ebd9123e8249888fa9a59c7bd55ebb627b21d8d37`  
		Last Modified: Tue, 18 Nov 2025 00:02:41 GMT  
		Size: 35.0 KB (35006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:cb52a1b6a9bdf116326f4907edad4aded44c4231fc2c4301ff8e619473cac5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621855387b368579f8359815f7b4f97db8bbd90a2612dbe65cc817f9cbd32bd5`

```dockerfile
```

-	Layers:
	-	`sha256:da9e70daf490da67ddb9d324d0778ed0f13a6307fae5ad94d66cfa7e73eff84c`  
		Last Modified: Tue, 18 Nov 2025 00:24:12 GMT  
		Size: 5.4 MB (5398001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa190af4e1cb9f75fbf0e5eb85993d7032959ca35c9dd8a55ba33862d67e9585`  
		Last Modified: Tue, 18 Nov 2025 00:24:12 GMT  
		Size: 24.6 KB (24602 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi-minimal` - linux; s390x

```console
$ docker pull gradle@sha256:8fde1601338372d9853fcab4dc8986ab996383c352bc99d961b3a15d30066730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.1 MB (385134917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77d33f3f43b2e56ac21301e6e838eef4fbe52e69c695763ccea4d8e45ffe586`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 17 Nov 2025 06:55:26 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 06:55:26 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 17 Nov 2025 06:55:27 GMT
ENV container oci
# Mon, 17 Nov 2025 06:55:27 GMT
COPY dir:25054aa4a6c69856b29487af8bbbcbc6cee329e92c8eced671f2e9e1b0cc5041 in /      
# Mon, 17 Nov 2025 06:55:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 06:55:27 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 06:55:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 06:55:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 06:55:27 GMT
COPY file:4b85719f9a6183730ff3a5e6ddd6d5db079cb4351cb42de31d4da99485475023 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:55:27 GMT
COPY file:4b85719f9a6183730ff3a5e6ddd6d5db079cb4351cb42de31d4da99485475023 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:55:28 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "org.opencontainers.image.revision"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "build-date"="2025-11-17T06:55:15Z" "release"="1763362218"org.opencontainers.image.revision=f7f5876a3d86ded473c14b11d7491c2b6ddf39ce
# Mon, 17 Nov 2025 23:13:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:13:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:13:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:13:42 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:13:42 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Mon, 17 Nov 2025 23:17:12 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 17 Nov 2025 23:17:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:17:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:17:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 17 Nov 2025 23:17:13 GMT
CMD ["jshell"]
# Mon, 17 Nov 2025 23:30:16 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 23:30:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 23:30:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 23:30:16 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 23:30:16 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 23:30:26 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 17 Nov 2025 23:30:26 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 23:30:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 23:30:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 23:30:30 GMT
USER gradle
# Mon, 17 Nov 2025 23:30:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 23:30:30 GMT
USER root
```

-	Layers:
	-	`sha256:8a5d6c48cb2c885ab264e85dd244af6174451d4cbdd00e240acc440b771129a5`  
		Last Modified: Mon, 17 Nov 2025 12:09:51 GMT  
		Size: 38.1 MB (38134810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8508eb3307d7668f2c17cc532e5db218f9d047de011dedc4817329dfd7d4842f`  
		Last Modified: Mon, 17 Nov 2025 23:14:25 GMT  
		Size: 27.7 MB (27727867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2cf0a65886b7561537df1449d89d6ee7be515d38bd697e98f08b58390aaeb`  
		Last Modified: Mon, 17 Nov 2025 23:30:14 GMT  
		Size: 147.1 MB (147068473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ce69266f9eeac362ac0bcdf15665a93cad1d1aad0d45001d05dbdb54a17634`  
		Last Modified: Mon, 17 Nov 2025 23:17:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82606cb0ab4d761a0372ac6157008067be4249d7745cd628f0ee77041615def`  
		Last Modified: Mon, 17 Nov 2025 23:17:45 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeadfecf3c85c8a78fd50456964aa8daeb2a903964997442cc2b04fbb7676073`  
		Last Modified: Mon, 17 Nov 2025 23:31:02 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38cfe5c1db093d53c28d3207f324cd5e9ca8c29d76f832f3dcbe9063ebbd6f0e`  
		Last Modified: Mon, 17 Nov 2025 23:31:08 GMT  
		Size: 36.6 MB (36642633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac6ab8bcd6da505035d737f99bb7c627f54e36f4553e59cf0fab2f61655daa1`  
		Last Modified: Tue, 18 Nov 2025 20:40:05 GMT  
		Size: 135.5 MB (135521971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbce073e3301a64859e3606b8923ad3768481250a2d44b7dcc53f0afdba6661e`  
		Last Modified: Mon, 17 Nov 2025 23:31:02 GMT  
		Size: 35.0 KB (35005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:fb337b3aee4cd128dd8fb666a7d9212a364588e1a34325bd07572371acc260b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5411799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa535b3f330d2905aa02722b6fd52aa902b288283cd457ee04ff8f526901c2d`

```dockerfile
```

-	Layers:
	-	`sha256:1a7ac9c552190f9089afe45286ebbd5dd48fbee8923578796769597da78299e7`  
		Last Modified: Tue, 18 Nov 2025 00:24:18 GMT  
		Size: 5.4 MB (5387271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:595e89781f9155f29240f79bcb30b09c35c0f8426bcbedbcd7c9e7f991c0d40f`  
		Last Modified: Tue, 18 Nov 2025 00:24:19 GMT  
		Size: 24.5 KB (24528 bytes)  
		MIME: application/vnd.in-toto+json
