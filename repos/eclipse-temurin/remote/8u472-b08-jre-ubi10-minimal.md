## `eclipse-temurin:8u472-b08-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:b3635264e3767a1cc434afcdd14662d8d078b36b15353f5c32d4f80fbe4809a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u472-b08-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:cb5cb0a3044a323da195ede800f0de3492a4e2b8b42989728c98b841f70fa537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131852435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8badb249f5537d1baa913afa8d50e2b74870500f3f9a7e6ee071882eb1da7ae5`
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
# Mon, 17 Nov 2025 23:15:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:15:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:15:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:15:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:15:57 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Mon, 17 Nov 2025 23:16:00 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 17 Nov 2025 23:16:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:16:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:16:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:655d40851ec137389403231b6dbcbc6498453f87c8529473a95a934d7560b3e6`  
		Last Modified: Mon, 17 Nov 2025 12:13:14 GMT  
		Size: 34.6 MB (34622032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9136b9ae249edbfc8d04b05c492cd2ef86c72b29b416382d2ff77de27b7bf823`  
		Last Modified: Mon, 17 Nov 2025 23:16:32 GMT  
		Size: 55.3 MB (55340303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b37532a9a5849b018541798b5e4a956d5a12c1f08d24c183715072e7ca0b4c`  
		Last Modified: Mon, 17 Nov 2025 23:16:29 GMT  
		Size: 41.9 MB (41887682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff54f616547bab2cb40f3e5af8a5a408e07705aa217b3e5e4d251ac715548b3c`  
		Last Modified: Mon, 17 Nov 2025 23:16:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12976bf8796df109d642250512145ca825ab10bdd24f9a638bb2e7f55a68380c`  
		Last Modified: Mon, 17 Nov 2025 23:16:22 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8b034f61437df13f433b0906e4e274887c7463e04c5d147ea978a218123a14aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5645641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e4aabd7242db218cdf411d440b1ac2e598016aaa917639d3e2896fac51019b`

```dockerfile
```

-	Layers:
	-	`sha256:e73190d3b97b139fdf060adb5cf8cd26bd32b8c2137a8ad4eff3c2732190c653`  
		Last Modified: Tue, 18 Nov 2025 01:19:49 GMT  
		Size: 5.6 MB (5626130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99974fe69601e149724d866e30323d0aaba28acc4827f7cadb7effe68f06ee30`  
		Last Modified: Tue, 18 Nov 2025 01:19:50 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u472-b08-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:4ef25cfa1c49e1da30a80398d27d8b961ebb43a0944a87a9f000ad362efd9452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128623465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de75dcd40af20cc6a69cf5eccc617bf15872310858df22af2f8423f54ce4f0c`
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
# Mon, 17 Nov 2025 23:15:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:15:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:15:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:15:46 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:15:46 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Mon, 17 Nov 2025 23:15:49 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 17 Nov 2025 23:15:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:15:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:15:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:478ab5c6661ea5c0248171ccd1b6894235610fb202e5874f79689086363a2e34`  
		Last Modified: Mon, 17 Nov 2025 12:13:13 GMT  
		Size: 32.6 MB (32592652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eed54b151ccd8e1af7a29dd912e7249faec267d2291b086ad08f34dffb7b702`  
		Last Modified: Mon, 17 Nov 2025 23:16:19 GMT  
		Size: 55.1 MB (55148202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b091c09a9c7e7b4a681f344d6c9901934f6363ea1e65347a9701792e97601`  
		Last Modified: Mon, 17 Nov 2025 23:16:21 GMT  
		Size: 40.9 MB (40880193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823c5aeca7f1a7126da1a1f5740fa0e073b77efc14bff642c9ed5d58f93f417`  
		Last Modified: Mon, 17 Nov 2025 23:16:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e780a9dba7c609c90b82701b3404f845149cacc6fc356a7d89252438a2f9b7`  
		Last Modified: Mon, 17 Nov 2025 23:16:14 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:30832cd274eb75ee5428de9f7c5a15450881f92e92e3beccb4c0b3b56367266b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5645913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aaa5f51aa97a4a7af314bcd9dbb45e5e8d0e4b4fe2433008cbe164d7f95a59`

```dockerfile
```

-	Layers:
	-	`sha256:2c0db735f1fed0df22ccc52b3d849df738d4df45ca4e1d181dab8ed6b1ba57d2`  
		Last Modified: Tue, 18 Nov 2025 01:19:56 GMT  
		Size: 5.6 MB (5626298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfec38c1d4ffd13d6bd27f1fc5af440cba86c3431b869012c2f405aee9d39ccb`  
		Last Modified: Tue, 18 Nov 2025 01:19:58 GMT  
		Size: 19.6 KB (19615 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u472-b08-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:9cbb34b3a16150153def6c62950ad6a487c39c805025c18c5073e99b6bc5afdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137346462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab0c730e9f6a6b047de000f642f2c6b6ff558d2fd6df67e5290a7603d9f628e`
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
# Mon, 17 Nov 2025 23:19:00 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 17 Nov 2025 23:19:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:19:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:19:03 GMT
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
	-	`sha256:4ace61fd33c2d28395f2f46c4023c12fe0b230ea53d9ada1211cd808b72c06ad`  
		Last Modified: Mon, 17 Nov 2025 23:19:51 GMT  
		Size: 41.3 MB (41268883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3769566cbddaaab495b2d28844a077012058eff11ae307ee64546fa26d592000`  
		Last Modified: Mon, 17 Nov 2025 23:19:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0605a6c3c2cd56814e98bf02db8c363af0f0e4352bbda9cdb86927f6b24ad6d5`  
		Last Modified: Mon, 17 Nov 2025 23:19:48 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e3836a7b4517ff8b7a89ffa818eec2d55fc2bf6388b61e0165d8616ab88bf562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5635426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd528430fa0df3035b07232cec431b8d91129cf370e4d385e06d05065c9db956`

```dockerfile
```

-	Layers:
	-	`sha256:e73e99d1869d6e96000a80d05e3f1e28a95f0ab8e12b672d5afa893d87099e02`  
		Last Modified: Tue, 18 Nov 2025 01:20:04 GMT  
		Size: 5.6 MB (5615885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40ff92282996f662745cc395fb6eb85ea1ab5da600fa96e774c4cd81fcf2ac50`  
		Last Modified: Tue, 18 Nov 2025 01:20:05 GMT  
		Size: 19.5 KB (19541 bytes)  
		MIME: application/vnd.in-toto+json
