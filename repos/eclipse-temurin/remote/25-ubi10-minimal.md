## `eclipse-temurin:25-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:7126e1675ef2ba596c3b9705082824a391011f991559f46ccc88110ea169f5c1
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

### `eclipse-temurin:25-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:c1f6b2880390dc17de9bcdfbe8a441430eac7dc162fa5c769a3e5e02ea1b4d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182011508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b76afe015294d64f29fbc7eb17dabdb7e4b9adaafb317f2ad081ed4ca44e90`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-25.0.1+8
# Mon, 17 Nov 2025 23:14:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 17 Nov 2025 23:14:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:14:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:14:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 17 Nov 2025 23:14:56 GMT
CMD ["jshell"]
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
	-	`sha256:b27d52bf7ca80e71e42d0d779522237cac4e8ae4a24d2835d555ed46acfe3219`  
		Last Modified: Mon, 17 Nov 2025 23:15:30 GMT  
		Size: 92.0 MB (92046731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04ca6cf2e547b37febe36d199a6335d0a724c1c8e453e10fdaa8dce6158ae0e`  
		Last Modified: Mon, 17 Nov 2025 23:15:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5188fcad8031483bdaa34a5636fe10fd2b42e35e43d1e61c9b21fed3bc226733`  
		Last Modified: Mon, 17 Nov 2025 23:15:22 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2167ff42860357aff49833a4cf9013c4c76eec53f3bd853984d78e5fd3288939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5652453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e0ae4c11defaefc0891f4ec2558e42ffaeff726c6fe0c93b1b41a5e9617b2b`

```dockerfile
```

-	Layers:
	-	`sha256:ebbd7e493b2925d25156a89ec66a82477956d7f481a148b2eecce178a7fd884d`  
		Last Modified: Tue, 18 Nov 2025 01:18:23 GMT  
		Size: 5.6 MB (5631164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36024f2b4a9ed86389895616e8650e675f8d66e2e3554d3edf69591fe7f2f469`  
		Last Modified: Tue, 18 Nov 2025 01:18:24 GMT  
		Size: 21.3 KB (21289 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:a0ca873fd3a76a42fa907ea36bccbdb2eaf50f33d7eb77dc094dc8dcebad00fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178799563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6360be1d4cc6140c2f4a2722ded81873e0dd9ae2738aee32b2a162388fb1db22`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Mon, 17 Nov 2025 23:18:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:18:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:18:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:18:14 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:18:14 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Mon, 17 Nov 2025 23:18:20 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 17 Nov 2025 23:18:22 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:18:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:18:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 17 Nov 2025 23:18:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:478ab5c6661ea5c0248171ccd1b6894235610fb202e5874f79689086363a2e34`  
		Last Modified: Mon, 17 Nov 2025 12:13:13 GMT  
		Size: 32.6 MB (32592652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590abed54446332fa42d1df6184692b5f3fee1d04a3efe22c9800311afb81cb6`  
		Last Modified: Mon, 17 Nov 2025 23:19:06 GMT  
		Size: 55.1 MB (55148192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c1ecc74f37d29dbf0a109fc53c2c088970c4f6b94e28af9a55b38a44cddae4`  
		Last Modified: Mon, 17 Nov 2025 23:19:09 GMT  
		Size: 91.1 MB (91056299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b916a018fb40f38285a791be7c9469c2d588edc6414aad6870cb93a198ab319c`  
		Last Modified: Mon, 17 Nov 2025 23:18:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25036e6742965911711eee2d2092d28513584ee6346a3cf12da856a47760e45e`  
		Last Modified: Mon, 17 Nov 2025 23:18:57 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:736dcf789596f9c9be4ba5647eb5622729ee0059863cdfc709bd06b4c9d09d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5652056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11011ee4f27d7a0292ea406a7aca21d51d59d176d0a096186c177afd1581a06e`

```dockerfile
```

-	Layers:
	-	`sha256:d8a14b9ac46237b13a62146b6ef250df55a6e7b5cc90e4f7a9be62bdc7ecdd58`  
		Last Modified: Tue, 18 Nov 2025 00:27:03 GMT  
		Size: 5.6 MB (5630651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78cda0765b5682fa3ee4e014288457f61b01ad80f22b6f0a8b70babb3de95856`  
		Last Modified: Tue, 18 Nov 2025 00:27:04 GMT  
		Size: 21.4 KB (21405 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:4ceecd580ec1d94516fa69c5b98bcb44370d6ed4f7835e5d04d0c31ed46461fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187690613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a2a68187df73fd424833e7c8f7661bbc4e1200f6d68b53f9e577bb3c79e52b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-25.0.1+8
# Mon, 17 Nov 2025 23:31:08 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 17 Nov 2025 23:31:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:31:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:31:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 17 Nov 2025 23:31:13 GMT
CMD ["jshell"]
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
	-	`sha256:d2b8eac6e27e7452f425987f3ced134fd828f0597ad2fbbbb9b52c7dc6552aea`  
		Last Modified: Mon, 17 Nov 2025 23:32:21 GMT  
		Size: 91.6 MB (91613033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dd8fb1f259be2ceb0f6678cee4df58a83839537d855f7c0085e25bab781f6a`  
		Last Modified: Mon, 17 Nov 2025 23:32:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbbb6224270a4f71037d992ded42ee2d8ef67f3b93683c3c5c2c2706dbe3dca`  
		Last Modified: Mon, 17 Nov 2025 23:32:05 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9b4abfeec406731ce70db704935401bd5d3bf5eca31b730e72e04280772cbc34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5640937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39654db15a393d53f070bd4acceb93b7fe6c79d22af3912ee57ed550aebac510`

```dockerfile
```

-	Layers:
	-	`sha256:7231f235dc9234b5723a9fcc8366666ae1bd1758fe143d01b5ac7c5c1a119f70`  
		Last Modified: Tue, 18 Nov 2025 00:26:58 GMT  
		Size: 5.6 MB (5619614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1af6e1b95cfc8986acb8869a598f886e7f84f3db5e0d86f45ec9cbae527fb4`  
		Last Modified: Tue, 18 Nov 2025 00:26:59 GMT  
		Size: 21.3 KB (21323 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:164305625bebf0a02e2b391d0c908cfd1d3f48216343cfce51956f6dfac05eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178524025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fb5beee9f294e4136e52cf14b79792123caf0073e447a94301707a45b400cc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Mon, 17 Nov 2025 23:13:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:13:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:13:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:13:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:13:45 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Mon, 17 Nov 2025 23:18:25 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 17 Nov 2025 23:18:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:18:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:18:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 17 Nov 2025 23:18:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2a66ed46dad4e3fa171f22fbb8e4ce06ce8e5891794fb42c5290a350eb241eef`  
		Last Modified: Mon, 17 Nov 2025 12:13:10 GMT  
		Size: 34.4 MB (34366982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ef2d5fa13c529ca5651578802bbbf1107b283eb0c3bed0028a3aed7d77f10a`  
		Last Modified: Mon, 17 Nov 2025 23:14:33 GMT  
		Size: 55.9 MB (55942931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b69fe6e384fc3a640c27ae289e89a69eec5bae1ebbc57450f68c12528c22de2`  
		Last Modified: Mon, 17 Nov 2025 23:19:10 GMT  
		Size: 88.2 MB (88211694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351c2dbb3d7fd10ba250b20ab5efd0149a15a2cd576fd11c38484882057fd280`  
		Last Modified: Mon, 17 Nov 2025 23:19:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8bbb074c7c958821717a1c9b9bb649c4f625b971178482c0cee572c0650403`  
		Last Modified: Mon, 17 Nov 2025 23:19:00 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ba432bc73963452974b42d79a98953be861d6527cdf61c71573c9f6bdd02a6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5640527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f57e424167017c4e2153726d97ec993707c01f3cfcc15526f979392b284fe0`

```dockerfile
```

-	Layers:
	-	`sha256:c9602a9d88710857d2a19f4aa187d615144b68e33e0e90986291d25eb8553f15`  
		Last Modified: Tue, 18 Nov 2025 00:26:54 GMT  
		Size: 5.6 MB (5619238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c22c8af6afd0f67a35ddc427b4cdb6f8ae422af53082ec9f43d52b69723e5d2`  
		Last Modified: Tue, 18 Nov 2025 00:26:55 GMT  
		Size: 21.3 KB (21289 bytes)  
		MIME: application/vnd.in-toto+json
