## `eclipse-temurin:21-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:f73ceb8f044d6dd94ad441ee3402d75ade7efd6e55022059ee370c455585c22b
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

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:eb517bda078909ed4180eb126ad9ef48f95adacc4876633c2fdc0c37e34f28b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142941045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80af074cf1884d6bb840a8a21ca2423402d33230c04e5ff1c81ed1d5a07c9bea`
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
# Mon, 17 Nov 2025 23:14:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:14:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:14:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:14:49 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:14:49 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Mon, 17 Nov 2025 23:17:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 17 Nov 2025 23:17:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:17:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:17:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:655d40851ec137389403231b6dbcbc6498453f87c8529473a95a934d7560b3e6`  
		Last Modified: Mon, 17 Nov 2025 12:13:14 GMT  
		Size: 34.6 MB (34622032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e85cea4469f691bb37232896ae484f8072a0b24e091fdc90e608e8de37d0f8`  
		Last Modified: Mon, 17 Nov 2025 23:15:33 GMT  
		Size: 55.3 MB (55340324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa50902c0cfc5a660b92d7b9b1a3b5363fa199155a9ac7602538d4ab5b06cff9`  
		Last Modified: Mon, 17 Nov 2025 23:18:05 GMT  
		Size: 53.0 MB (52976271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e753a97138726478621e8923f20bd2714dd2595f0c8a2d646451b7dd65196f19`  
		Last Modified: Mon, 17 Nov 2025 23:18:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56270b2b1ff777987a2ef9748dc79d35e2dc1b9d7157199b569ecd14687ac03`  
		Last Modified: Mon, 17 Nov 2025 23:18:00 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e16e1e9601db7bac2dd6764acaa3015886e79df8c3d0e5f1c50c4c712852642b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5618873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a8f0088f1fc17705606ed056ae53250b64717c95a69c06fcf77eb491ed2b51`

```dockerfile
```

-	Layers:
	-	`sha256:b218576afa2cefb446e595555e7225a63a184364f3ca7a2fe9b00f19ddb77b6e`  
		Last Modified: Tue, 18 Nov 2025 01:17:18 GMT  
		Size: 5.6 MB (5598519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00bb4a0ca38a2b3790f41b88f7437cb37268ebe23bc8f3a2c49d91ecbb905c74`  
		Last Modified: Tue, 18 Nov 2025 01:17:19 GMT  
		Size: 20.4 KB (20354 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:54dd73264298c05d3c58ae6bf65d2f78ffde164e4e586b72b6775a711465e9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139884300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac6728c7c0f54d619dd28005e62ca332a45bcdf02cc89d0fc56e627677c120d`
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
ENV JAVA_VERSION=jdk-21.0.9+10
# Mon, 17 Nov 2025 23:17:52 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 17 Nov 2025 23:17:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:17:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:17:52 GMT
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
	-	`sha256:f5152467f83110aaa1ae4326448a76d9bbb90a3b0c041ea4743b54485e62f33c`  
		Last Modified: Mon, 17 Nov 2025 23:18:19 GMT  
		Size: 52.1 MB (52141207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b17ac1242d35d65d755b13a41e47dd309d5ad5f7347d29e6cfd39c1a29f8f82`  
		Last Modified: Mon, 17 Nov 2025 23:18:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf47e1c3fe78762e3be5a8a8092b70cb4518e3ee95ba6ce4170f3bd5af6ec8d`  
		Last Modified: Mon, 17 Nov 2025 23:18:13 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:897cacb30ce9a14e96254cc658a8fe3ac1d1811934d631bfc13e85d7a696d06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5618455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e936ed1cc283896ff26067c472f051a3780957ac77ecee4c571f6d781c1d75`

```dockerfile
```

-	Layers:
	-	`sha256:c7d6063f547bfdd739f8a742974905fb6c47f659c7ec7d305d5522acbb6fd53d`  
		Last Modified: Tue, 18 Nov 2025 01:17:25 GMT  
		Size: 5.6 MB (5597997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a180fed76f91942c10bac0cce4f4a3865010c099b1b2b9a8ab0b078a54dfbc`  
		Last Modified: Tue, 18 Nov 2025 01:17:26 GMT  
		Size: 20.5 KB (20458 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:82cabddbed21b9328b5fe18c5afa2e9c465dfca1ba844da6d6376e39cf357e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149055325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7467e74ed9af8a0651206cd6ff062ccc2a6d8e3bfc879f5cd9314dc2ba8cbb3c`
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
ENV JAVA_VERSION=jdk-21.0.9+10
# Mon, 17 Nov 2025 23:29:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 17 Nov 2025 23:29:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:29:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:29:38 GMT
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
	-	`sha256:57f2567fc79458c7818b5bcf33eee8b10059b60a0baa0474e9f99999cdd891c3`  
		Last Modified: Mon, 17 Nov 2025 23:30:30 GMT  
		Size: 53.0 MB (52977747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b91fc0ac0c429d83cfc961aecdf183a86fc5142bcea9ac8ede8c9d7687a795d`  
		Last Modified: Mon, 17 Nov 2025 23:30:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c233598419e5ed940ea6eddd342dc62a93ea9de66edf9e6cfff2ec09463377b9`  
		Last Modified: Mon, 17 Nov 2025 23:30:25 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:da4730c0745e38e25ab717c48d188c8ad7ec387ea614147ec671b9739a966ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830c6dc3554055128e690c5098fbb8d96d6c10286204e747381b8151e66bac14`

```dockerfile
```

-	Layers:
	-	`sha256:e9931c5c09a9624caa81f5329ed223a43a6e5cd3615aae44d58e36d10dddb696`  
		Last Modified: Tue, 18 Nov 2025 01:17:31 GMT  
		Size: 5.6 MB (5587584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae1cdc8b44b4b67650c9dab451b4a33d4567c67c182ee7252d6f69343433b89`  
		Last Modified: Tue, 18 Nov 2025 01:17:32 GMT  
		Size: 20.4 KB (20384 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:3a714c1b33131d641168031022215d2895dffbe79120b9c4c7ebf5eab6756243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139828141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312fe673ede4bbf210a5cb2f29042a83b8a768e9b97922fe73aeb1e43d5ed2ae`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 17 Nov 2025 07:10:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 07:10:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 07:10:17 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 07:10:17 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 17 Nov 2025 07:10:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 07:10:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 17 Nov 2025 07:10:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 07:10:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 07:10:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 17 Nov 2025 07:10:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 07:10:17 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 17 Nov 2025 07:10:17 GMT
ENV container oci
# Mon, 17 Nov 2025 07:10:17 GMT
COPY dir:76a6336bcfe979f4363ab4e270e094c8022e34df72e324a083a12c2d85f8216c in /      
# Mon, 17 Nov 2025 07:10:17 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 07:10:17 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 07:10:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 07:10:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 07:10:18 GMT
COPY file:722fbb47feca83759f23f8dfff0d3c846a19a0b2fd67a93ddc9c6f485a86ce74 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 07:10:18 GMT
COPY file:722fbb47feca83759f23f8dfff0d3c846a19a0b2fd67a93ddc9c6f485a86ce74 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 07:10:18 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "org.opencontainers.image.revision"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "build-date"="2025-11-17T07:08:03Z" "release"="1763362715"org.opencontainers.image.revision=f3ce7416a648177fb2c54fd1c28cc0dab0304a68
# Mon, 17 Nov 2025 23:13:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:13:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:13:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:13:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:13:48 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Mon, 17 Nov 2025 23:17:10 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 17 Nov 2025 23:17:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:17:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:17:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2a66ed46dad4e3fa171f22fbb8e4ce06ce8e5891794fb42c5290a350eb241eef`  
		Last Modified: Mon, 17 Nov 2025 12:13:10 GMT  
		Size: 34.4 MB (34366982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f812c55e7e93a758eec59955278cb14eb59e41427aedb44630ae8bfa61613ad9`  
		Last Modified: Mon, 17 Nov 2025 23:14:37 GMT  
		Size: 55.9 MB (55942783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a86d1a6ba3d0843eabf2a4f131c5b9db8495f15b7a2c94f93055f905d5f7fd5`  
		Last Modified: Mon, 17 Nov 2025 23:17:48 GMT  
		Size: 49.5 MB (49515957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7219e3a433f52883ffe96f3828a78b5c0ef561b8e20c59f8073a8d6eaaba2`  
		Last Modified: Mon, 17 Nov 2025 23:17:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2e708fe55758ab077c0e8e86b0e66fb32b7a903029b9e0c0d4de9721f47a05`  
		Last Modified: Mon, 17 Nov 2025 23:17:39 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bb58c5a4b28c6f66b6f5fe0698e5c1656fda1276126709ded9f31e337cf4a01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1975ec96592074732023998730ddfe16ca19448c2cc1a1e328da33288e50e21e`

```dockerfile
```

-	Layers:
	-	`sha256:fef043b5bd1d79f457418bd9d23f7cca0e2fb686e2afd5b48319c728d6c35c30`  
		Last Modified: Tue, 18 Nov 2025 01:17:38 GMT  
		Size: 5.6 MB (5588445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6dd95e0e5bd3bd35cdd483eec893f15ace248307fcab8614b0efb2116e62a71`  
		Last Modified: Tue, 18 Nov 2025 01:17:40 GMT  
		Size: 20.4 KB (20354 bytes)  
		MIME: application/vnd.in-toto+json
