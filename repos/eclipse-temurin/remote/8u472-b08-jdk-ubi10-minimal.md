## `eclipse-temurin:8u472-b08-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:476952c636e7d8b63a993f6eab99cd364b8e794db5226ee03986ed2f3e3882a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u472-b08-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1b69f580f0be0988703a2f4f80dc100918f9ae211392b360c8603793d1488d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144698768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d70f07ab71f5fdb1809ebc7b40ed2714c6bc0f6bbaa525af536b8338c16f220`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 17 Nov 2025 07:01:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 07:01:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 07:01:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 07:01:07 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 17 Nov 2025 07:01:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 07:01:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 17 Nov 2025 07:01:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 07:01:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 07:01:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 17 Nov 2025 07:01:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 07:01:08 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 17 Nov 2025 07:01:08 GMT
ENV container oci
# Mon, 17 Nov 2025 07:01:09 GMT
COPY dir:6f102d5d0a81427532060e899f002b6c279a2bdfa663565eb4d68240cd4deb2a in /      
# Mon, 17 Nov 2025 07:01:09 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 07:01:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 07:01:09 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 07:01:10 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 07:01:10 GMT
COPY file:42c1a5fe3a98108cbf4ea734a78ed48ceae9786bdcb72b488a4915deb55aebb5 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 07:01:10 GMT
COPY file:42c1a5fe3a98108cbf4ea734a78ed48ceae9786bdcb72b488a4915deb55aebb5 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 07:01:10 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "org.opencontainers.image.revision"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "build-date"="2025-11-17T07:00:51Z" "release"="1763362715"org.opencontainers.image.revision=f3ce7416a648177fb2c54fd1c28cc0dab0304a68
# Mon, 17 Nov 2025 23:15:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:15:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:15:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:15:04 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:15:04 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Mon, 17 Nov 2025 23:15:07 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 17 Nov 2025 23:15:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:15:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:15:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:655d40851ec137389403231b6dbcbc6498453f87c8529473a95a934d7560b3e6`  
		Last Modified: Mon, 17 Nov 2025 12:13:14 GMT  
		Size: 34.6 MB (34622032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c694ede4b104b8dc806929f4e66e269dc204374b4b0140faa89eb3609a3eddc6`  
		Last Modified: Mon, 17 Nov 2025 23:15:38 GMT  
		Size: 55.3 MB (55340382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cbe25590812c250d1b7f04a18187baf0cdb81b0bbbe00d8530da7dc51ffcf1`  
		Last Modified: Mon, 17 Nov 2025 23:15:50 GMT  
		Size: 54.7 MB (54733912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475e92b4861450e3421a104e246819e5f3dca6c2f23d809196450df41d7968a4`  
		Last Modified: Mon, 17 Nov 2025 23:15:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4271c5a71c054556ca7881d8e77414b44122245bc90e9a0d1e0d87405befa0`  
		Last Modified: Mon, 17 Nov 2025 23:15:32 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f667fa4822328de2ad0ed7ede899f07b9b77d660e1150c49c576d9d3dfd8e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5822152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9950ccfde57c37984f2493c5b63efbd60ee37b597e15dd1c1d8bae0c5688aa`

```dockerfile
```

-	Layers:
	-	`sha256:ddedb3e48d625f23cff44d318ec8b5c66c29ab0bb087d513c6cc99ab0f42ed70`  
		Last Modified: Tue, 18 Nov 2025 01:19:23 GMT  
		Size: 5.8 MB (5802114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc421ea03ac94466c523b9a1e8bdb679a7accdaf0c4df33f15fe7b95e3b9721`  
		Last Modified: Tue, 18 Nov 2025 01:19:24 GMT  
		Size: 20.0 KB (20038 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u472-b08-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:5ed1d0c9a57fdaf942c4387d5afdf102db3e373fde3aada4fe510fd12aeff496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141558708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1876e2a751c2dc17a283c6004333f6175c88a57427a5ddace0d3e7228f1b888`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 17 Nov 2025 07:05:20 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 07:05:20 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 07:05:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 07:05:20 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 17 Nov 2025 07:05:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 07:05:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 17 Nov 2025 07:05:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 07:05:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 07:05:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 17 Nov 2025 07:05:21 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 07:05:21 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 17 Nov 2025 07:05:21 GMT
ENV container oci
# Mon, 17 Nov 2025 07:05:21 GMT
COPY dir:71c88713509dd6b0b5837b8d1a56e982242f9588ee4f21c026f7f78f90f1a386 in /      
# Mon, 17 Nov 2025 07:05:21 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 07:05:21 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 07:05:22 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 07:05:22 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 07:05:22 GMT
COPY file:1adfb0cb6d42f20dcbe21ac6ef5900c488572e79486c9bd342365e6ac328e720 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 07:05:22 GMT
COPY file:1adfb0cb6d42f20dcbe21ac6ef5900c488572e79486c9bd342365e6ac328e720 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 07:05:22 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "org.opencontainers.image.revision"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "build-date"="2025-11-17T07:05:00Z" "release"="1763362715"org.opencontainers.image.revision=f3ce7416a648177fb2c54fd1c28cc0dab0304a68
# Mon, 17 Nov 2025 23:14:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:14:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:14:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:14:04 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:14:04 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Mon, 17 Nov 2025 23:15:14 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 17 Nov 2025 23:15:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:15:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:15:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:478ab5c6661ea5c0248171ccd1b6894235610fb202e5874f79689086363a2e34`  
		Last Modified: Mon, 17 Nov 2025 12:13:13 GMT  
		Size: 32.6 MB (32592652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e419e505db8a310e855e0426f766cd3f4597d6aae71e0e2723b32cb43289d970`  
		Last Modified: Mon, 17 Nov 2025 23:14:51 GMT  
		Size: 55.1 MB (55148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34c2fb5f89d0a5674a167c82a079edccbf7d44368e37926209f68ee359fcc7f`  
		Last Modified: Mon, 17 Nov 2025 23:15:43 GMT  
		Size: 53.8 MB (53815589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20ebb454f26f8f9c158f5ae7d132b1d35bda3db54a7793e81d3ce4d972e6d11`  
		Last Modified: Mon, 17 Nov 2025 23:15:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189916dd525d60c1ec95dac52e9d81421f291ce1ee1e2374f1a38dd477d44ace`  
		Last Modified: Mon, 17 Nov 2025 23:15:36 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cfeb8246e19eb1e0cac977368046861d6c45d3d068269b5a5d662e5dffca6567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5822457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf1f6ba7209f143cc610f780f64aa726e0aff2daa2442f5bfc96da3f2200b00`

```dockerfile
```

-	Layers:
	-	`sha256:820d9b0ec68865949f8a87b9dc3536df86507f0f9cb26a1e1ce2d1cb64918a44`  
		Last Modified: Tue, 18 Nov 2025 01:19:30 GMT  
		Size: 5.8 MB (5802302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a8b9c6e65b24ebf07c84852ffb89028bd822d05f2ef15dd802114c9b5416b96`  
		Last Modified: Tue, 18 Nov 2025 01:19:31 GMT  
		Size: 20.2 KB (20155 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u472-b08-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:62a2a3d9f51d9d004680015d73313896ba4d7d102297536f15b0bafca3478ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148253455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e8b84c42a9c4598a422c57540fa068aa24850b5f54880eb671058454ecbcc1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 17 Nov 2025 07:03:31 GMT
ENV container oci
# Mon, 17 Nov 2025 07:03:32 GMT
COPY dir:3f836289fcb5e4834914ff52d15c42d6b925906d318eaeb6e7ece83b813f7798 in /      
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 07:03:32 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:040b4789124c20d56e0f81f37d756e271408963b29b2b4b1e2a7e2c073e4ad50 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:040b4789124c20d56e0f81f37d756e271408963b29b2b4b1e2a7e2c073e4ad50 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 07:03:33 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "org.opencontainers.image.revision"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "build-date"="2025-11-17T07:03:20Z" "release"="1763362715"org.opencontainers.image.revision=f3ce7416a648177fb2c54fd1c28cc0dab0304a68
# Mon, 17 Nov 2025 23:14:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:14:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:14:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:14:49 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:14:49 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Mon, 17 Nov 2025 23:15:04 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 17 Nov 2025 23:15:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:15:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:15:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6e24e81139d30a463716e63229e1184a2b4250bb139ff88e3682c9e552661b81`  
		Last Modified: Mon, 17 Nov 2025 12:13:13 GMT  
		Size: 38.7 MB (38721761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106e259b55af997c3f2efc1cf8633c914cd06061615b03cbef4967d4541d920a`  
		Last Modified: Mon, 17 Nov 2025 23:16:28 GMT  
		Size: 57.4 MB (57353400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c98c25f59b323b4b9b1d817a982443c1f1ac73552b7dce037be4ce51467092`  
		Last Modified: Mon, 17 Nov 2025 23:16:30 GMT  
		Size: 52.2 MB (52175851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087db38746d7fe31248758e28d4c5501b5dd6a93d3d4fc580a804aaf37434f97`  
		Last Modified: Mon, 17 Nov 2025 23:15:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44eb1f3890e10788f3681e62f9ecd6ef3eab7ddba47e3bc0aee9d094f3c09a94`  
		Last Modified: Mon, 17 Nov 2025 23:16:20 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c8ae1b5d9625a1c7261d42a527ddc360b1e33dd465390787c5d2b1028c566228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5809934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bffcc40884215789b9df39957199ccddacca65a9b1f7253ee6379a89a2384c`

```dockerfile
```

-	Layers:
	-	`sha256:b9864a36a4b7f06055401e382c9b2d625ea4f1f36844871a5bfe2b31b964a45e`  
		Last Modified: Tue, 18 Nov 2025 01:19:37 GMT  
		Size: 5.8 MB (5789859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14fd4ad5cb70853c24cdf8e404ea7118cada007483df20e3c261a6b7edc786d9`  
		Last Modified: Tue, 18 Nov 2025 01:19:38 GMT  
		Size: 20.1 KB (20075 bytes)  
		MIME: application/vnd.in-toto+json
