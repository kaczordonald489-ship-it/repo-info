## `eclipse-temurin:8-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:b16b2f89f5c469b0c5c2e52065fede2117dd63a8cb2346943a230004acaa2dd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6a1c800df687d46c98649037a9a1e6b481a741fed4b8848e26babb8b12484ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113844488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe55adee30e61be8541b7db354026c96b2b7804ef901dcc019501f832a0082f`
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
# Thu, 29 Jan 2026 19:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jan 2026 19:04:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 19:04:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jan 2026 19:04:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 29 Jan 2026 19:04:47 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 29 Jan 2026 19:04:50 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 29 Jan 2026 19:04:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 29 Jan 2026 19:04:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:04:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:438bf0ef7bf7d9e54cbea537827e1b65c9de6ea0f4486cbdeaa845a0a9e70190`  
		Last Modified: Thu, 29 Jan 2026 10:51:29 GMT  
		Size: 34.6 MB (34577419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435a1924bc947fdc4e37af91336e874f9f1f41f0cdd36cd26c1eed355312aa61`  
		Last Modified: Thu, 29 Jan 2026 19:05:04 GMT  
		Size: 37.4 MB (37376973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e817901de648ce4e9e3430d057a3f12a05229329275d9c4918308a10b7afd40f`  
		Last Modified: Thu, 29 Jan 2026 19:05:04 GMT  
		Size: 41.9 MB (41887679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5ba2c4f86c5efc5e4e3ce67204d08c96c7944419b544df4be2ce3cac8fc00f`  
		Last Modified: Thu, 29 Jan 2026 19:05:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0466b9f6c4977806f97beb4d43becf9cdf73a26edfc7b0e6a7c0a92f8cfec0`  
		Last Modified: Thu, 29 Jan 2026 19:05:02 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d2776b560917835f1497a6130722bd491d8fa1bf464691b6348ab57de274c8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3753591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5bb64d2433648da632c5bfcdbedff2336add721e958adca0b0f1254100b1c35`

```dockerfile
```

-	Layers:
	-	`sha256:892e5c4b125ab91fbd005f0dcb054e5a6ab2ae28d4341ca5a64b6c974b154957`  
		Last Modified: Thu, 29 Jan 2026 19:05:02 GMT  
		Size: 3.7 MB (3734081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:badc36d030def1f14022a3c5d7b273a66b1b0e6df88ea680d7cffa598ef876c1`  
		Last Modified: Thu, 29 Jan 2026 19:05:02 GMT  
		Size: 19.5 KB (19510 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:40e8b417c9d718acd10597fa9c5d3d4afa528f8926fae4abbf3639f8b81688ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110832498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9243451b76d38a65123836364c864a2c13e4fa0ac51483f066de1d7abe43dbee`
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
# Thu, 29 Jan 2026 19:03:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jan 2026 19:03:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 19:03:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jan 2026 19:03:46 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 29 Jan 2026 19:03:46 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 29 Jan 2026 19:03:50 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 29 Jan 2026 19:03:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 29 Jan 2026 19:03:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:03:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0aaa6d534ca2cd2a0028481caedba14f5f3893da8f6d1ba86fb068a9ba044c3e`  
		Last Modified: Thu, 29 Jan 2026 12:10:31 GMT  
		Size: 32.6 MB (32628824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8b1c754f4d2fb39f5f43aadb492fe51d586c5b43afdf796514569f8d67faf7`  
		Last Modified: Thu, 29 Jan 2026 19:04:04 GMT  
		Size: 37.3 MB (37321046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2cbe1a746ff1a781534851e969e06ccf0596c2ef875127a5c501f56ecbce02`  
		Last Modified: Thu, 29 Jan 2026 19:04:04 GMT  
		Size: 40.9 MB (40880208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae34820bb7a8a288884eda646e49da66eeb7d620212bea2769a570cf83328a5`  
		Last Modified: Thu, 29 Jan 2026 19:04:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43743916858030d253e7d31c0c5f37188bf0ec708a898c164b91e969fd4a790`  
		Last Modified: Thu, 29 Jan 2026 19:04:03 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2825c1d028bcfd1bcf5c1b64c94335dea7d45fbecd3f312e5d15a3294b34db7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3753800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e576c8d83c2403057edc4fd29d02022e68089449906fbe743ee267bed3e47feb`

```dockerfile
```

-	Layers:
	-	`sha256:f0e800dca07dab5391a2a6ca2507dc4856a4d001fee522e52978061a56491992`  
		Last Modified: Thu, 29 Jan 2026 19:04:02 GMT  
		Size: 3.7 MB (3734185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f3e69292d92f5c4013e5de568f45950fbf6b0a1edfc3f04164801606c55b534`  
		Last Modified: Thu, 29 Jan 2026 19:04:02 GMT  
		Size: 19.6 KB (19615 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:4c6ff255cf59ff0adf09bb23f6963a02dfb8c4b0617443b102381da7ac5c5c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119079523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1661860ed86410e5f7cc70a4141f9add3f8e732a6053a77a41a174588acfe3d0`
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
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 29 Jan 2026 19:28:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 29 Jan 2026 19:28:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:28:34 GMT
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
	-	`sha256:d3be9f259ec737d70c116096785f441152bebd64beb419ef0a01ca5441ac550d`  
		Last Modified: Thu, 29 Jan 2026 19:29:12 GMT  
		Size: 41.3 MB (41268876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f57a0829d210a141de4bd2c754662604ff91584a668e6173af3891a39954ee5`  
		Last Modified: Thu, 29 Jan 2026 19:29:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e925b2020cb57e54c4cde8c889277edecd468363194304a5eaf237fa29ccf8`  
		Last Modified: Thu, 29 Jan 2026 19:29:11 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e8dfe2148d1278d292b79ff607ae50464db68ef1a4ea8ddc8e1922f3dfd2777e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93adeb0110e6c8b43723e667396baac6ec046421aa066f8ca34dff657a3cf7ac`

```dockerfile
```

-	Layers:
	-	`sha256:b564790e6002215efe94aa872b480270edf037624338b3b01de9247b9a129db9`  
		Last Modified: Thu, 29 Jan 2026 19:29:10 GMT  
		Size: 3.7 MB (3723516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d583e9ff4b42da6176136d88b9059a838b751903ec081326a80da2b2a50d45`  
		Last Modified: Thu, 29 Jan 2026 19:29:10 GMT  
		Size: 19.5 KB (19541 bytes)  
		MIME: application/vnd.in-toto+json
