## `eclipse-temurin:17-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:8ae884ff6c0df54ed7dc142a82b5384f44c1c9b800958aa23d351ec771ac063f
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

### `eclipse-temurin:17-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:c6d584fee134fd0a04bc4a2ef204f9cffcc8b2185c570a420eedde0581c41974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234817687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370c9995069ca6431257a064a1e93ae62a5c560535e153d1987b35892f858e3c`
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
# Mon, 17 Nov 2025 23:16:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:16:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:16:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:16:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:16:50 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Mon, 17 Nov 2025 23:16:56 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 17 Nov 2025 23:16:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:16:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:16:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 17 Nov 2025 23:16:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:655d40851ec137389403231b6dbcbc6498453f87c8529473a95a934d7560b3e6`  
		Last Modified: Mon, 17 Nov 2025 12:13:14 GMT  
		Size: 34.6 MB (34622032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1aaf0bde5f30b57fd304cbc53f6587b7d73d52af5227f0c973fe55c69e1e21`  
		Last Modified: Tue, 18 Nov 2025 04:28:29 GMT  
		Size: 55.3 MB (55340339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927c46f92daa702db38a83ba38cf2bcd8dc9bc02da58b4de8481f35ab9e550f7`  
		Last Modified: Tue, 18 Nov 2025 04:28:39 GMT  
		Size: 144.9 MB (144852896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb8cef85646c06ae137420193ab5ac2ca09273186e682213a0cbff08e61ff42`  
		Last Modified: Mon, 17 Nov 2025 23:17:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6b31f3d23c4fa02c8f486b9999e2a24eded07e022a85a884a6dadf525b14a6`  
		Last Modified: Mon, 17 Nov 2025 23:17:25 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bf591320dca6d27669168327212241949132f7651c0a85ae85e679cd70ab0070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5701846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a4bac6b0c1cc5ed357c0cf1fa020cf2b3cb0d26a97b889f56d303b1d9127ce`

```dockerfile
```

-	Layers:
	-	`sha256:13861618b499f9dbec9e3eafdfd46476efd051b862a6ce3d66cd607e30f410c4`  
		Last Modified: Tue, 18 Nov 2025 01:15:09 GMT  
		Size: 5.7 MB (5680506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a516a5a5edbb02ef257da0e8aef566a19b016c5588483d8269bf08aa7918666`  
		Last Modified: Tue, 18 Nov 2025 01:15:10 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:14ab2dcfbbfc3635588e7f4ff8b198ce02b01fa0df42f87d7a7fab5197aad655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231428608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0abacbfc00afcae2ca38013bc8ce5d15e4bb7bb7df50c7d4c121f64431fff0c`
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
# Mon, 17 Nov 2025 23:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:17:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:17:11 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:17:11 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Mon, 17 Nov 2025 23:17:17 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 17 Nov 2025 23:17:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:17:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:17:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 17 Nov 2025 23:17:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:478ab5c6661ea5c0248171ccd1b6894235610fb202e5874f79689086363a2e34`  
		Last Modified: Mon, 17 Nov 2025 12:13:13 GMT  
		Size: 32.6 MB (32592652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22810bfd2c6d478a8bf8e7fd81848c42e841cca2ebf13b9ceb096901f74fe3`  
		Last Modified: Mon, 17 Nov 2025 23:17:57 GMT  
		Size: 55.1 MB (55148152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe5c0fcd6a4019174117ed67c18fb655fa5178b1272047802c248e27284878f`  
		Last Modified: Tue, 18 Nov 2025 07:33:17 GMT  
		Size: 143.7 MB (143685386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e07ad6e79801e8bc8e2dd6dc17dd1e1ac9a49756789c419a2c127fc634b944`  
		Last Modified: Mon, 17 Nov 2025 23:17:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f744a3c990eee2960b78f547c46a3f3ed2c87d7aa57c4b3d433ab10d923fd54`  
		Last Modified: Mon, 17 Nov 2025 23:17:50 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b38bcc8f49fc5ba408603a8a3b40d3e99f6cccd259e13811cb313a6437d01519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5701451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68945d2ea402cba8f03afd7134d75350652fc26194131670c1d0a214e74f6b3f`

```dockerfile
```

-	Layers:
	-	`sha256:63344a06d364121ca06ed13d621d3b61f1cf0ebbfacf402dafddfe26cff1a8bf`  
		Last Modified: Tue, 18 Nov 2025 01:15:17 GMT  
		Size: 5.7 MB (5679996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3097e6540d69eb40e33153c7540e14c3bb0096b2e8f5f70b0cbe4c9c06273b17`  
		Last Modified: Tue, 18 Nov 2025 01:15:18 GMT  
		Size: 21.5 KB (21455 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:91c3914117b8b9a84214811681d6e65daeaaf625fb2830a7ab2a2d321cea602f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240625427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6afefee1f14bf38069aab0f5e976dad2f539d0763273569c2e6a04304b1e9b`
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
ENV JAVA_VERSION=jdk-17.0.17+10
# Mon, 17 Nov 2025 23:24:30 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 17 Nov 2025 23:24:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:24:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:24:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 17 Nov 2025 23:24:39 GMT
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
	-	`sha256:acd0a5326b179764eb4da106035397b55fdf50795eaa1440d2035d03da646991`  
		Last Modified: Tue, 18 Nov 2025 09:21:53 GMT  
		Size: 144.5 MB (144547849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9aa648f85474e7273500ecab419725b13a6e4f2007ba9d259154b97944d6a7`  
		Last Modified: Mon, 17 Nov 2025 23:25:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf78dac091a00c8cedba75cb893716b76c30a1c198decd72f0ea5ee705895b2`  
		Last Modified: Mon, 17 Nov 2025 23:25:40 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4ff0ddd8ee5c9bc9f33319427674491d40df053722bda3350cb36df6b60e801b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5689034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacd42de4ec9897248f2f23c5a7d229843621e4eacb7f61e07ad37a8ec7168ab`

```dockerfile
```

-	Layers:
	-	`sha256:0088ee1a8862be9236a457512ef637c29042a1804f0fc46275d02687b386d8ab`  
		Last Modified: Tue, 18 Nov 2025 01:15:24 GMT  
		Size: 5.7 MB (5667658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4a570d51a72bb134d0ca9d38bd6330da33a41494f0eb8f8f29291a5823bdacb`  
		Last Modified: Tue, 18 Nov 2025 01:15:25 GMT  
		Size: 21.4 KB (21376 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:3f4b7cd12de6a73e22aa7b58650f00d901f74e89ee3658e6ff9a1a58567d9c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225174379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34637f4a2e45a9a5e79bec537c33591a55aebf54994b76b6221d7031c5bea8f8`
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
# Mon, 17 Nov 2025 23:13:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:13:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:13:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:13:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:13:48 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Mon, 17 Nov 2025 23:15:07 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 17 Nov 2025 23:15:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:15:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:15:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 17 Nov 2025 23:15:08 GMT
CMD ["jshell"]
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
	-	`sha256:a20a9eb5004862666dff6a56782cc395eb39694985b2ff47bfcde886b983a1b5`  
		Last Modified: Tue, 18 Nov 2025 09:22:05 GMT  
		Size: 134.9 MB (134862198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dfa48dcfd9940b907ffa24f0202e00e0890d41490c77694378cf7ae3f7d997`  
		Last Modified: Mon, 17 Nov 2025 23:15:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70c6d5c72f65c9dc4d4bd0e6b3a0397d4961d83e097b64c88da57abb7873db7`  
		Last Modified: Mon, 17 Nov 2025 23:15:32 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e589434445e4da564a7181198cf71d869efe971f4a1a26ce4d5ffb76786676d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5687372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a337d92f89932e865169b6d93e4ed84165f797e600fda8e651747e3dff8d3ae8`

```dockerfile
```

-	Layers:
	-	`sha256:cf2c696fd3078aa7c9a8c5158123192b71aab2f4043e93f724f2fba8b3127810`  
		Last Modified: Tue, 18 Nov 2025 01:15:31 GMT  
		Size: 5.7 MB (5666032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d03db870f82d2221d9ec00241a3d8065ff32bc34ba867b36aed41e4585472d09`  
		Last Modified: Tue, 18 Nov 2025 01:15:33 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json
