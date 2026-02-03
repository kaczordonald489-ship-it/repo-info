## `eclipse-temurin:25-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:bea3f108bfdeb549579a4b6546e7309bc754e30cfbc6fc328124740b3c30e774
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

### `eclipse-temurin:25-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0390463f22b5b32c6fd763355ab99ac8d2ff104e40b8d58a9bcf114125e0ba2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164003509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1905c3e4b61b990b799d9216af81c7345516eced1e11d01c711c071d2ba3bedb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 29 Jan 2026 19:05:31 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 29 Jan 2026 19:05:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jan 2026 19:05:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:05:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jan 2026 19:05:33 GMT
CMD ["jshell"]
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
	-	`sha256:20a98c3118c933599abac14dd67c0e5a5b89bfef7b03de4872e5174c68e6d47a`  
		Last Modified: Thu, 29 Jan 2026 19:05:50 GMT  
		Size: 92.0 MB (92046696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9885b38140f1bf3a75acee13b326d7ae7e3b7eb48b59743c88066cf06b36bffa`  
		Last Modified: Thu, 29 Jan 2026 19:05:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2716e005aaabcc65ddcd8486d999846787a638b1eef32dc3cbdd01642d906a`  
		Last Modified: Thu, 29 Jan 2026 19:05:48 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ab475f4246621d9ed7ab6855a1140ecdc0c0563fa9e52a1ccef9c24c9b5d1da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e3ab0f0f5e51ff042007cf148ea5dee5a88b8d54ea00d1c404dc328a225365`

```dockerfile
```

-	Layers:
	-	`sha256:a95fec6978f7fe00416c3ce6ab5db7913f11dbead45b4e24b896c79d17428522`  
		Last Modified: Thu, 29 Jan 2026 19:05:48 GMT  
		Size: 3.7 MB (3739115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e325542bacc86fd68b595b18146f811d47f396dceaadf5e80c223328b17e92d8`  
		Last Modified: Thu, 29 Jan 2026 19:05:47 GMT  
		Size: 21.3 KB (21289 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:daae0fff54c8afb6a372dd2ea45367357b436e68492f0d1a68be1305de3596e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161008590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33eabbb367d020ee50f40e247bc14bae0cfe7b6f31257fcef12892472f00842b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 29 Jan 2026 19:04:47 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 29 Jan 2026 19:04:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jan 2026 19:04:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:04:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jan 2026 19:04:48 GMT
CMD ["jshell"]
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
	-	`sha256:361f6722e0a71ece37dfec2238c01729a9370f35e1110e8bb767b3486721225d`  
		Last Modified: Thu, 29 Jan 2026 19:05:08 GMT  
		Size: 91.1 MB (91056300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7dc76a5cb5feb8b0d90fca5ce17510920a268ef7738d2c0b46f57e117d0603`  
		Last Modified: Thu, 29 Jan 2026 19:05:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0466b9f6c4977806f97beb4d43becf9cdf73a26edfc7b0e6a7c0a92f8cfec0`  
		Last Modified: Thu, 29 Jan 2026 19:05:02 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f42c16fb8a4828a7a654fbc6eadf44b0367ca32ca7ac3ab60929506f3b838c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86f86bb36b04ec360a8ba92269f6ce84c9da07cadc42803074f42a7b638fc31`

```dockerfile
```

-	Layers:
	-	`sha256:267f518763229c4d7e046bba468a6caf5bf99cd20518681c903a0268f0838e61`  
		Last Modified: Thu, 29 Jan 2026 19:05:05 GMT  
		Size: 3.7 MB (3738538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bba7acdf9e104b2a2eeeb451a8786638a96d096c1822386cb157929a0e720f4`  
		Last Modified: Thu, 29 Jan 2026 19:05:05 GMT  
		Size: 21.4 KB (21404 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:bed7f6f5a4c9bc5770f8d10e9e9d1fbf42ce14dd2c4c42e0f897ddcca3e33d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169423681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6155e31caf66e256702125b81b5eee2dea569d1ec9edc93deb733f4ca5285a4c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 29 Jan 2026 19:33:04 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 29 Jan 2026 19:33:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jan 2026 19:33:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:33:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jan 2026 19:33:07 GMT
CMD ["jshell"]
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
	-	`sha256:41e48be4498ada486ca869cac8fb4fbbcb9890560b6babcc217d728516fbb799`  
		Last Modified: Thu, 29 Jan 2026 19:33:49 GMT  
		Size: 91.6 MB (91613031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f09291ef4b05efda4f42a4cd82dcbb1775ab4a644a7e6e85fd5afcedd0f514`  
		Last Modified: Thu, 29 Jan 2026 19:33:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14cbec368ba0049f2c820701d24c28ddf2b41ed350e8e303a33c07e9bf76388`  
		Last Modified: Thu, 29 Jan 2026 19:33:46 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6170ff6c23fc2f4bf3b3f2750502765d760c95bee754ede8121303e3b8ee1c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01c395a0859f64ae68c8583c0b8ea03c9a13b1f2eb0f855093a6da40b7145f1`

```dockerfile
```

-	Layers:
	-	`sha256:16a3a011b7f971fedd44d3cfd810075a06b22c7527b3efef4985539ac60f2533`  
		Last Modified: Thu, 29 Jan 2026 19:33:47 GMT  
		Size: 3.7 MB (3727245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f8a37621bb40af67492cbc459eaf7e526004708283ddd1155d9f131950f4c23`  
		Last Modified: Thu, 29 Jan 2026 19:33:46 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:9cb8a3d834475bfb359312a310f6babc0a3a9161ea9fcf1b477a065b522cfca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160329722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497b9a0a4b8778ad5e4296e332290257ee36e2637c6e824399ac047dc5e08c89`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 29 Jan 2026 09:56:50 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Jan 2026 09:56:50 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 29 Jan 2026 09:56:50 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 29 Jan 2026 09:56:50 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 29 Jan 2026 09:56:50 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Jan 2026 09:56:50 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 29 Jan 2026 09:56:50 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Jan 2026 09:56:50 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Jan 2026 09:56:50 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 29 Jan 2026 09:56:50 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Jan 2026 09:56:50 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 29 Jan 2026 09:56:50 GMT
ENV container oci
# Thu, 29 Jan 2026 09:56:51 GMT
COPY dir:327471521892cd34c1da1b0c08146334e1a52fc96d00977ec2c4716a805926be in /      
# Thu, 29 Jan 2026 09:56:51 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 29 Jan 2026 09:56:51 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 09:56:51 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 29 Jan 2026 09:56:51 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 29 Jan 2026 09:56:51 GMT
COPY file:507254a3916ae8a3d0da81ab0e311fbbbd0af5c49efaabdd888ea88769ed073c in /usr/share/buildinfo/labels.json      
# Thu, 29 Jan 2026 09:56:51 GMT
COPY file:507254a3916ae8a3d0da81ab0e311fbbbd0af5c49efaabdd888ea88769ed073c in /root/buildinfo/labels.json      
# Thu, 29 Jan 2026 09:56:52 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="24312baa53bef28621c8f52f140c638d591e1d71" "org.opencontainers.image.revision"="24312baa53bef28621c8f52f140c638d591e1d71" "build-date"="2026-01-29T09:54:31Z" "org.opencontainers.image.created"="2026-01-29T09:54:31Z" "release"="1769677092"org.opencontainers.image.revision=24312baa53bef28621c8f52f140c638d591e1d71,org.opencontainers.image.created=2026-01-29T09:54:31Z
# Thu, 29 Jan 2026 19:07:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jan 2026 19:07:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 19:07:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jan 2026 19:07:20 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 29 Jan 2026 19:07:20 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 29 Jan 2026 19:08:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 29 Jan 2026 19:08:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jan 2026 19:08:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:08:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jan 2026 19:08:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d8ee08a58910c5c5149bb0ea01f46100abfda005d1c4e44af7de63358967442`  
		Last Modified: Thu, 29 Jan 2026 12:10:39 GMT  
		Size: 34.4 MB (34355699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fac79be9396898c75970a01f5081befd0c69910a0195a3bef5e7144742c54b`  
		Last Modified: Thu, 29 Jan 2026 19:07:52 GMT  
		Size: 37.8 MB (37759880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b97278208582d932d9e8016201d3d40607aac9203353b6e3f4f87615bdaca10`  
		Last Modified: Thu, 29 Jan 2026 19:09:00 GMT  
		Size: 88.2 MB (88211724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f02165b9a2708e99ab637e9ef1791b42a9277e59981a0c4cfb28fb29296bb09`  
		Last Modified: Thu, 29 Jan 2026 19:08:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43cb9a31746881ec70a9ef59c8e4382ee1afbef0eed5bdefd970b98c4f62645`  
		Last Modified: Thu, 29 Jan 2026 19:08:58 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a8fca3187e81f9a9a074ae92a7e4758bb15df7bacdf29194fe027642a818f944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a858813e3a641f63e3cd40a47981708bdadc15f8cb6204ed9abe3e8c9d520df`

```dockerfile
```

-	Layers:
	-	`sha256:4b3984b021ff78b040412297f17232243d6c07d60add089e99f612e764812005`  
		Last Modified: Thu, 29 Jan 2026 19:08:58 GMT  
		Size: 3.7 MB (3727253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e13a244a536f9769341052ca8522fbf43f204a28029a880f4e0308c7b55b04`  
		Last Modified: Thu, 29 Jan 2026 19:08:58 GMT  
		Size: 21.3 KB (21289 bytes)  
		MIME: application/vnd.in-toto+json
