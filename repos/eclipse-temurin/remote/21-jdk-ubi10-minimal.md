## `eclipse-temurin:21-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:23708f308767a8b81e9fa6f3f57580aad7101bbf9b74fba94c87ecb88fcb2c54
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

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:658d5610f6481c89cfb74ad1af142fbe5385773b9e5b63d57b446e188f673b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229785800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7008322253bc7d9b9f5696e52df42a5c2cfe7aa69f23ec61f19953be6197b10`
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
# Thu, 29 Jan 2026 19:05:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jan 2026 19:05:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 19:05:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jan 2026 19:05:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 29 Jan 2026 19:05:25 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 29 Jan 2026 19:05:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 29 Jan 2026 19:05:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jan 2026 19:05:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:05:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jan 2026 19:05:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:438bf0ef7bf7d9e54cbea537827e1b65c9de6ea0f4486cbdeaa845a0a9e70190`  
		Last Modified: Thu, 29 Jan 2026 10:51:29 GMT  
		Size: 34.6 MB (34577419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfd31423199dbfd4fd08effdf3b4a9fcb4d9fc2ba01f4d3fec09d9b88d2ea1b`  
		Last Modified: Thu, 29 Jan 2026 19:05:54 GMT  
		Size: 37.4 MB (37377014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0471a2c619ce444eed364b1c53cd4b7e91dfadf874fba539f5151d618c1f7ecf`  
		Last Modified: Thu, 29 Jan 2026 19:05:57 GMT  
		Size: 157.8 MB (157828949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6969496e8dfdd48167376cb4d93a7a1d7955bb7e66ac4cf64f9ff404a6449180`  
		Last Modified: Thu, 29 Jan 2026 19:05:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21273d9233a90c81a26171972af3dc88500e81d654d63785f99948b413de419f`  
		Last Modified: Thu, 29 Jan 2026 19:05:53 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:48bc89f9f744a1285d5749991c9f7627431f86cdd74dc2183f4292f411decb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3812873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fdf7f3706bbd0c4de6def4f9dc40845df38c7c5a1b4a3b64fa8b3c2368585ac`

```dockerfile
```

-	Layers:
	-	`sha256:6deb6716b74437c7d9b2121229b8972a7fa80f8442d5e1e21401ebaad112aed6`  
		Last Modified: Thu, 29 Jan 2026 19:05:53 GMT  
		Size: 3.8 MB (3791557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eefca2f297dc946432564887c2b004c3ec677d46593691b283fae2983310bd0e`  
		Last Modified: Thu, 29 Jan 2026 19:05:53 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:605a0a3db83900fcd53fcc34b7998ac126d2c2bcbd1f98d2ab91bdadecbb738c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226064125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0149ceffe0297b513753c1a81eac1facd45a306f5f92460b624c6eb6a7c82b33`
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
# Thu, 29 Jan 2026 19:03:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jan 2026 19:03:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 19:03:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jan 2026 19:03:43 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 29 Jan 2026 19:03:43 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 29 Jan 2026 19:04:28 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 29 Jan 2026 19:04:30 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jan 2026 19:04:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:04:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jan 2026 19:04:30 GMT
CMD ["jshell"]
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
	-	`sha256:64f5780ec8c5c8f5a9a90afcbe2f9967bb236fb540023a2cda2bb0850fb3dcd0`  
		Last Modified: Thu, 29 Jan 2026 19:04:50 GMT  
		Size: 156.1 MB (156111879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77ac2dec8d25326c4f1ff56e8a39ccb4ef68be5beeb659c40a71a34134edc3b`  
		Last Modified: Thu, 29 Jan 2026 19:04:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd1d712266103c7f32b59149bf9445982d2a5dd5bd3637a160da4b70dd073d7`  
		Last Modified: Thu, 29 Jan 2026 19:04:47 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6ceaa5d092565909e6f293acb8c77d01bd8f95cbd3b91eb12707a17e885f793b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3812415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c956bc1a9b97e8a16c67bf0d4c013ef2a0e9881b626a2e02bd7e3200e276379b`

```dockerfile
```

-	Layers:
	-	`sha256:a47e276af6c2f28d78062747ff0a8f447c7674a6b4a8fb95d1a28f80bb442434`  
		Last Modified: Thu, 29 Jan 2026 19:04:47 GMT  
		Size: 3.8 MB (3790983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65a8b6d0d846f7c79ad06cb55fa4d71d63f7e40b05ada3788d009c0b91f5df6d`  
		Last Modified: Thu, 29 Jan 2026 19:04:47 GMT  
		Size: 21.4 KB (21432 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:f0b07bb7facac3c124c37d48f77645552195709b5f24b7199951bd0efc213647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235754136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44e89add132ebf2d36d5f5e6799ccea90f9b2a07bed8be3fee38575cf97cda2`
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
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 29 Jan 2026 19:32:06 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 29 Jan 2026 19:32:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jan 2026 19:32:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:32:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jan 2026 19:32:10 GMT
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
	-	`sha256:94944bfbf4fa2cd46c889d473062739b66d7e95ba63948bcb1efae9516fa4f03`  
		Last Modified: Thu, 29 Jan 2026 19:32:51 GMT  
		Size: 157.9 MB (157943487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9652a75255a1883e80787d72ead620b6d9d297038189fb1071d3b3f3c16b5e9c`  
		Last Modified: Thu, 29 Jan 2026 19:32:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc931eb4ff49333b8da7e374214e8290549ecd8aa084da8bd6a39dd8340dd44`  
		Last Modified: Thu, 29 Jan 2026 19:32:48 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1dd649805f2a1cc02349115a76f6cd6250e960a22cd99950f837428d9e1033f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b882893445b449a024f8bdceefb5e0a39e8c01a71fb93a1c9446be317261d644`

```dockerfile
```

-	Layers:
	-	`sha256:c420b04dfb8a5468daf56c7825e6433aae457314a59a885738b49207f93a389a`  
		Last Modified: Thu, 29 Jan 2026 19:32:48 GMT  
		Size: 3.8 MB (3778389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9a89e705759a6b75f1916ce9db5ed8979d3d810666d725e8dc88ebaf4341c3d`  
		Last Modified: Thu, 29 Jan 2026 19:32:47 GMT  
		Size: 21.4 KB (21352 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:b00d2f50b206c8e6cba787cbc3c6a971a62527db0e065b62d73a744485318d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219186611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e4a214efb80e0829f0c62fedbe54bb6aae25cd0977828e2f8d6bcf7c98b052`
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
# Thu, 29 Jan 2026 19:07:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jan 2026 19:07:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 19:07:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jan 2026 19:07:19 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 29 Jan 2026 19:07:19 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 29 Jan 2026 19:08:19 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 29 Jan 2026 19:08:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jan 2026 19:08:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:08:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jan 2026 19:08:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d8ee08a58910c5c5149bb0ea01f46100abfda005d1c4e44af7de63358967442`  
		Last Modified: Thu, 29 Jan 2026 12:10:39 GMT  
		Size: 34.4 MB (34355699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91c67f3455e131bede0017b40f4e5fb73926b62632ac0b9d7f1aba6e461fea7`  
		Last Modified: Thu, 29 Jan 2026 19:07:44 GMT  
		Size: 37.8 MB (37759987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea77e82bfe4f59597dab97a7cb8b5b5154cc986812be74ed78e9fa5e944e31c`  
		Last Modified: Thu, 29 Jan 2026 19:08:49 GMT  
		Size: 147.1 MB (147068505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7116e7337b4364ad8575ab8c6fa8e96c18bc9e053c11eff7e44c7e9d2050fca`  
		Last Modified: Thu, 29 Jan 2026 19:08:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211bf8117859ecd949786761ef1b3af0464f93a98ba7fea25506ff3ea2f0fdc2`  
		Last Modified: Thu, 29 Jan 2026 19:08:46 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bbe04f09c3b8281c80cddc0bf167c05eb1bc23aefc77ecc218bd3baa2807adfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3798463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d3399957d0bd5948f69893a74ffe4d200614da9ea3ebe84de42dc3f3ccdab5`

```dockerfile
```

-	Layers:
	-	`sha256:4b6a56d2dae7db20d0a689036d16b26ed1435be442cb692387498ced2aa447db`  
		Last Modified: Thu, 29 Jan 2026 19:08:46 GMT  
		Size: 3.8 MB (3777147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d223b4b68275f6414cec6c72f4f7a65acc4156460f440ae69050eff8e38baea`  
		Last Modified: Thu, 29 Jan 2026 19:08:46 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json
