## `eclipse-temurin:8-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:ca5ba018cf3decbf7293cfc6916249fb86fc1a5b694e361c66618574e3194b6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:564164c5dc6e1a28f844041957b393b3624af1e9b4a700616e84edd8ffca977c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126690702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f887d1ff199572fc8efe14f06c1acb15020afb3c08a124f5c1a7c7c867a61fa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Jan 2026 09:02:29 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 29 Jan 2026 09:02:30 GMT
ENV container oci
# Thu, 29 Jan 2026 09:02:30 GMT
COPY dir:fd123199d2aa564f8f0592613ffa5ec1622b80265ee6073edb50ec5ee7520e92 in /      
# Thu, 29 Jan 2026 09:02:30 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 29 Jan 2026 09:02:30 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 09:02:31 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 29 Jan 2026 09:02:31 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 29 Jan 2026 09:02:31 GMT
COPY file:449edb9408a04a948eac072a18a188bbaa8b86d792fecd68574017d6afe608e1 in /usr/share/buildinfo/labels.json      
# Thu, 29 Jan 2026 09:02:31 GMT
COPY file:449edb9408a04a948eac072a18a188bbaa8b86d792fecd68574017d6afe608e1 in /root/buildinfo/labels.json      
# Thu, 29 Jan 2026 09:02:31 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="24312baa53bef28621c8f52f140c638d591e1d71" "org.opencontainers.image.revision"="24312baa53bef28621c8f52f140c638d591e1d71" "build-date"="2026-01-29T09:01:57Z" "org.opencontainers.image.created"="2026-01-29T09:01:57Z" "release"="1769677092"org.opencontainers.image.revision=24312baa53bef28621c8f52f140c638d591e1d71,org.opencontainers.image.created=2026-01-29T09:01:57Z
# Thu, 29 Jan 2026 19:04:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jan 2026 19:04:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 19:04:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jan 2026 19:04:37 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 29 Jan 2026 19:04:37 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 29 Jan 2026 19:04:41 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 29 Jan 2026 19:04:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 29 Jan 2026 19:04:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:04:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:438bf0ef7bf7d9e54cbea537827e1b65c9de6ea0f4486cbdeaa845a0a9e70190`  
		Last Modified: Thu, 29 Jan 2026 10:51:29 GMT  
		Size: 34.6 MB (34577419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c10805bc1753cf762b2c67f0cce4d5e060e1a344ceb882d9bdeb54ded9ae45`  
		Last Modified: Thu, 29 Jan 2026 19:04:56 GMT  
		Size: 37.4 MB (37376914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472eead2924ceb236f2fdf5788cfb52af85870297dc7bc26f205bb477d078e36`  
		Last Modified: Thu, 29 Jan 2026 19:04:56 GMT  
		Size: 54.7 MB (54733927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147e561eecb24df79176b849fdf19b98882a38565eece84839373b800fe3652e`  
		Last Modified: Thu, 29 Jan 2026 19:04:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d9f48b0dde68f948d0d7b0c758dba30d0f7855eb12e65d44750e65b5993e0f`  
		Last Modified: Thu, 29 Jan 2026 19:04:54 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e7c6c5cbd364c6e0ac29a7782602aa4f7b7ea6773cab9a6fe52ad306dce156db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e6c458061d2517cd0c1cea4d377d89d1d45177eebefda71bce1f3e6d1a1c85`

```dockerfile
```

-	Layers:
	-	`sha256:8d359cbddc33b19d81d48342a2e15556696baad87074c2d3e0b3a05e7262b517`  
		Last Modified: Thu, 29 Jan 2026 19:04:54 GMT  
		Size: 3.9 MB (3910065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1901deef45b42cf098f5c1bf1ac09cd34bb0aa001d692fc5eef13cd2523aef1b`  
		Last Modified: Thu, 29 Jan 2026 19:04:53 GMT  
		Size: 20.0 KB (20038 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:d35cbd2a57a7a486fd1673dee885a73b4243b58437ec5a7000edc6c9f234ab2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123767897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6247d1ebaa4c519fc5737b3b6fe23b829a3e7e62d2eb95377b18f13431c33b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 29 Jan 2026 09:05:12 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Jan 2026 09:05:12 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 29 Jan 2026 09:05:12 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 29 Jan 2026 09:05:12 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 29 Jan 2026 09:05:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Jan 2026 09:05:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 29 Jan 2026 09:05:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Jan 2026 09:05:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Jan 2026 09:05:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 29 Jan 2026 09:05:12 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Jan 2026 09:05:12 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 29 Jan 2026 09:05:12 GMT
ENV container oci
# Thu, 29 Jan 2026 09:05:13 GMT
COPY dir:f04a14441fcd212e5d0214a121dec2a1bc6d2c5d21cfbaf83a8d433e3a4b847e in /      
# Thu, 29 Jan 2026 09:05:13 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 29 Jan 2026 09:05:13 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 09:05:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 29 Jan 2026 09:05:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 29 Jan 2026 09:05:14 GMT
COPY file:a32ea0360b7828c576362304234412573437731fb955216e7f74f48b0b670488 in /usr/share/buildinfo/labels.json      
# Thu, 29 Jan 2026 09:05:14 GMT
COPY file:a32ea0360b7828c576362304234412573437731fb955216e7f74f48b0b670488 in /root/buildinfo/labels.json      
# Thu, 29 Jan 2026 09:05:14 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="24312baa53bef28621c8f52f140c638d591e1d71" "org.opencontainers.image.revision"="24312baa53bef28621c8f52f140c638d591e1d71" "build-date"="2026-01-29T09:04:51Z" "org.opencontainers.image.created"="2026-01-29T09:04:51Z" "release"="1769677092"org.opencontainers.image.revision=24312baa53bef28621c8f52f140c638d591e1d71,org.opencontainers.image.created=2026-01-29T09:04:51Z
# Thu, 29 Jan 2026 19:03:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jan 2026 19:03:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 19:03:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jan 2026 19:03:43 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 29 Jan 2026 19:03:43 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 29 Jan 2026 19:03:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 29 Jan 2026 19:03:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 29 Jan 2026 19:03:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:03:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0aaa6d534ca2cd2a0028481caedba14f5f3893da8f6d1ba86fb068a9ba044c3e`  
		Last Modified: Thu, 29 Jan 2026 12:10:31 GMT  
		Size: 32.6 MB (32628824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb6d71f3d7291f3ff35712c92caed2aa3ef15125567725e60a4455c52f67f12`  
		Last Modified: Thu, 29 Jan 2026 19:04:04 GMT  
		Size: 37.3 MB (37321000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1877f48f5cde0641bada3c7f84d61c558bcb800d29803df8384635e0875258`  
		Last Modified: Thu, 29 Jan 2026 19:04:04 GMT  
		Size: 53.8 MB (53815628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11244de0ee6a2fb1b20f872fb16ff20af44c00842a2e35e8e2c657025b0029f4`  
		Last Modified: Thu, 29 Jan 2026 19:04:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cedf1a872e754e9de5005209d8dceaa762a6f3d28601dd28038899f49b0b2ad`  
		Last Modified: Thu, 29 Jan 2026 19:04:03 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2d385cce9af73e08fa2aec8fd885b529604eb4b428dc11fdbbc180963ec1583d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c76bbd85980a032a508089411191c0e1e841a853ae4a1ffb22c49e5355ddb5f`

```dockerfile
```

-	Layers:
	-	`sha256:7aa039bfbc0fa1261533e7c5cbe03bf349de94b398e3277bd257df9b6a41fd4e`  
		Last Modified: Thu, 29 Jan 2026 19:04:01 GMT  
		Size: 3.9 MB (3910189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a28f0bba937a3bacdd2fb71e3a61b100fb86996c3cfad1dee71464f587a288e7`  
		Last Modified: Thu, 29 Jan 2026 19:04:01 GMT  
		Size: 20.2 KB (20155 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:5281c291c44c7c732809cae0a80bc885d55fe2a0f25ac094b7c0b409321af48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129986525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6926540a4257c208ad1d5541e8b1b120e2984829981a682260ea6adbad6f6cb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Jan 2026 09:43:39 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 29 Jan 2026 09:43:39 GMT
ENV container oci
# Thu, 29 Jan 2026 09:43:40 GMT
COPY dir:9f05c03fd98385ca667703832b015e247b162c40641da4bfafae12b451fb75f8 in /      
# Thu, 29 Jan 2026 09:43:40 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 29 Jan 2026 09:43:40 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 09:43:40 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 29 Jan 2026 09:43:40 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 29 Jan 2026 09:43:40 GMT
COPY file:53726944e41cc90bd970a2878ac432c863bd39ac879813f59a75e5ef00cb4ae2 in /usr/share/buildinfo/labels.json      
# Thu, 29 Jan 2026 09:43:40 GMT
COPY file:53726944e41cc90bd970a2878ac432c863bd39ac879813f59a75e5ef00cb4ae2 in /root/buildinfo/labels.json      
# Thu, 29 Jan 2026 09:43:40 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="24312baa53bef28621c8f52f140c638d591e1d71" "org.opencontainers.image.revision"="24312baa53bef28621c8f52f140c638d591e1d71" "build-date"="2026-01-29T09:43:27Z" "org.opencontainers.image.created"="2026-01-29T09:43:27Z" "release"="1769677092"org.opencontainers.image.revision=24312baa53bef28621c8f52f140c638d591e1d71,org.opencontainers.image.created=2026-01-29T09:43:27Z
# Thu, 29 Jan 2026 19:28:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jan 2026 19:28:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 19:28:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jan 2026 19:28:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 29 Jan 2026 19:28:25 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 29 Jan 2026 19:28:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 29 Jan 2026 19:28:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 29 Jan 2026 19:28:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:28:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:a8e4c90395db70569d5d34c1b72c9a955f03527f82047f5ff481b9771e26f723`  
		Last Modified: Thu, 29 Jan 2026 12:10:46 GMT  
		Size: 38.7 MB (38665536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a847da3c495b4477c38c514638ee54d51d2e0860a704b7879a5c13e9d797ec8d`  
		Last Modified: Thu, 29 Jan 2026 19:29:12 GMT  
		Size: 39.1 MB (39142692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3b4e8a9520ddd79ab2ff8373b574793b6ad69e097a40f0a2dfaaf2468eae6f`  
		Last Modified: Thu, 29 Jan 2026 19:29:13 GMT  
		Size: 52.2 MB (52175853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f57a0829d210a141de4bd2c754662604ff91584a668e6173af3891a39954ee5`  
		Last Modified: Thu, 29 Jan 2026 19:29:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64687754566bd588cf941ca533d3b6865d91f26951256cfca11a3bcf4c0af920`  
		Last Modified: Thu, 29 Jan 2026 19:29:11 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9ae4dc7523657a00b624958ad3037c987fc09db18c5b0bf769d071484bbbaab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35450a45b672cd4d2d55d4afead4c173dc2221d3ef77405e3aaf04fef1cd8c4`

```dockerfile
```

-	Layers:
	-	`sha256:ab7354e0543b567508f70e500755f4b7d46f90e89e1a96d7a72854a1d9d2122f`  
		Last Modified: Thu, 29 Jan 2026 19:29:10 GMT  
		Size: 3.9 MB (3897490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01d97bc7a9e7bc788754f3956b68a8d172e0def4726ca266c58167a2ad123956`  
		Last Modified: Thu, 29 Jan 2026 19:29:09 GMT  
		Size: 20.1 KB (20075 bytes)  
		MIME: application/vnd.in-toto+json
