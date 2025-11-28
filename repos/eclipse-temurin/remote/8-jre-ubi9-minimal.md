## `eclipse-temurin:8-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:edb2cc6ece7910902e6d5c4da8a29a006e2cf73f4a4871a1c884371ab79f9a6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2976665cb692097797b0c0b7142ab4c58522bcffd13cebe1893bab319dae4779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109566496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176e4064e6fe6a211f3512d63b4b50b7fb0a467770f42c881e56ebf6544e6ca6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Mon, 17 Nov 2025 23:14:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:14:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:14:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:14:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:14:45 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Mon, 17 Nov 2025 23:14:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 17 Nov 2025 23:14:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:14:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:14:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7d6ca59745ac48971cbc2d72b53fe413144fa5c0c21f2ef1d7aaf1291851e501`  
		Last Modified: Mon, 17 Nov 2025 07:24:40 GMT  
		Size: 40.0 MB (39979464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f9f2d39efc03472d12ef379ccbbff263e4a6f237611887f8c79889ff937b1`  
		Last Modified: Mon, 17 Nov 2025 23:15:09 GMT  
		Size: 27.7 MB (27696981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de21566f23eb1b1c532cee2b821aa23384c94dbc7924dfe847b630f0cccc080f`  
		Last Modified: Mon, 17 Nov 2025 23:15:13 GMT  
		Size: 41.9 MB (41887634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218fae8142f0b5f7e67148253c96fba627d6ead65febed2b2965505d4d93f0ee`  
		Last Modified: Mon, 17 Nov 2025 23:15:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b4ef639259073f8d6a60ff8bb157fee32186bf168615e24a664347ecb96379`  
		Last Modified: Mon, 17 Nov 2025 23:15:08 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5c75eb382c3b174cec8da4fbfade4b6c0263496ea04ecfb7fe658ec1adec0f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8168d11caaef6ca7ecc517f5050dce46a467aae12d115e543b91b7378d36d63`

```dockerfile
```

-	Layers:
	-	`sha256:c5c0bfc75f4823aecc3f34a6b7751b6fcc638882760280c5bbbf5a9a71d3f165`  
		Last Modified: Tue, 18 Nov 2025 01:20:00 GMT  
		Size: 2.4 MB (2435125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f35e62b6a8c06661f0afcdeea6cd194969e3dd51b8f07b13c1c9d56eaf5552a5`  
		Last Modified: Tue, 18 Nov 2025 01:20:01 GMT  
		Size: 19.3 KB (19347 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:e2010c063475d8267657b54b9812d04476670dd6be34859347d4c77dd8ef4763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107212877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c7ce94fb6ef9bf1ddc1b12311744d15f8ab490ca029566aeaebf9db649ed9b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Mon, 17 Nov 2025 23:16:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:16:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:16:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:16:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:16:44 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Mon, 17 Nov 2025 23:16:47 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 17 Nov 2025 23:16:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:16:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:16:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:3c0c9428a7f3bd24ecc53d01a84f8e5daf4cde2806733046039c236a5821dc20`  
		Last Modified: Mon, 17 Nov 2025 07:42:16 GMT  
		Size: 38.2 MB (38200298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffccdcbef89f94cc280dc48ce564109d6b4394a7a60801577ce96eca8d6e2443`  
		Last Modified: Mon, 17 Nov 2025 23:17:08 GMT  
		Size: 28.1 MB (28129993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed52cf09590bc88b2f13b44af738b5fa4c66f4ed73c206653f11cf841a0b5f53`  
		Last Modified: Mon, 17 Nov 2025 23:17:10 GMT  
		Size: 40.9 MB (40880168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcc3610850eef7481a9c3d3bcff776683bd1402fad3a0077dc269c5d7c305bd`  
		Last Modified: Mon, 17 Nov 2025 23:17:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4548eb90771048703fd0facc53588ac139d23bc4455bf6044621d4ae2af99ab2`  
		Last Modified: Mon, 17 Nov 2025 23:17:05 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7cffed053142088f20f0709efb33251812a4bfbb4235a972e5058cf841dafed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fe758b4821d654652065007aa22bf9dc6da1523bd98e7ff4cf74cb4d1f182c`

```dockerfile
```

-	Layers:
	-	`sha256:a87160a61f7b573c8d23051116b847ae29a93d06b683d87006c60fbb91a46a2f`  
		Last Modified: Tue, 18 Nov 2025 01:20:07 GMT  
		Size: 2.4 MB (2435173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dafab83492363118611d7d23aaafc713a0a5723c44af497b72feb1925a084250`  
		Last Modified: Tue, 18 Nov 2025 01:20:08 GMT  
		Size: 19.4 KB (19450 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:328a9f5dd2ff2104f22cd86807da6a942e1d42d1f27fea83e6c84c0fdc8df647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115826711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d94140aed41c767936f25022b8801475ceb53d61c8eebdb44fd7be9c7e3c92d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ENV JAVA_VERSION=jdk8u472-b08
# Mon, 17 Nov 2025 23:20:52 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 17 Nov 2025 23:20:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:21:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:21:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:6e1796eb9fe4c2f4fcec595ad316c9ab9736637f08eaac109b5b15e61b064cec`  
		Last Modified: Mon, 17 Nov 2025 23:21:46 GMT  
		Size: 41.3 MB (41268822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4077ce533e2ccf3a99e3d7a9012960aed66228211ac1c0c397dc3e846a3bed`  
		Last Modified: Mon, 17 Nov 2025 23:21:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b714877c4f78ef20b624172fcf2cc98a3fef3fe1fe81496a32ac6c9bcc9c92`  
		Last Modified: Mon, 17 Nov 2025 23:21:43 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:eedc15228129d29ea9d42a76c907e11d754835d85f0e71fc44bb6e662335c42f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2455197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94665e5a3433b39a617b661269bf37ba388419c733658e1def645693cad9008`

```dockerfile
```

-	Layers:
	-	`sha256:68bbb624bddd6714bbb8c4a04cdd01bbe424803dde84d8d76e25c012b04884cf`  
		Last Modified: Tue, 18 Nov 2025 01:20:12 GMT  
		Size: 2.4 MB (2435820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7375d6e4a434d0560a7db1be14d3115171d714a6704c5fa7fcf676bff4e04596`  
		Last Modified: Tue, 18 Nov 2025 01:20:13 GMT  
		Size: 19.4 KB (19377 bytes)  
		MIME: application/vnd.in-toto+json
