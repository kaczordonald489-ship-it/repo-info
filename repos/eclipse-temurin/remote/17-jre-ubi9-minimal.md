## `eclipse-temurin:17-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:4f0f6bf8f67e7dcc1a56afc19e7ddfee7ea6963adb9f23fbbacff76a9b209cd2
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

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1e89ca6e32aabe143fd4fe04e0d75c855c27381dae1cdc31215433882dba15d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114733265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6565bfdc0384cb99ec774926990ddc0dc3268d3b344598aff899eceec816d663`
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
ENV JAVA_VERSION=jdk-17.0.17+10
# Mon, 17 Nov 2025 23:17:24 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 17 Nov 2025 23:17:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:17:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:17:24 GMT
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
	-	`sha256:109be7ae139216029c66ad93fbd845b59aea4279a27c647a0861e25ea6f6ee4a`  
		Last Modified: Mon, 17 Nov 2025 23:17:48 GMT  
		Size: 47.1 MB (47054402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a8bf8d82403a6c26eafa26a3dc41ee01d0965625dbcd8bc71f142c352c09dc`  
		Last Modified: Mon, 17 Nov 2025 23:17:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889060ed274f1bf64913e3f68bba3de31810de5754cf25002350c5f05e6f5c21`  
		Last Modified: Mon, 17 Nov 2025 23:17:43 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6c09b8f61bd6db80e8757e8409af80cc6be239bf7b72e566d82df9471025b46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df058e80d8841853854aefd50f9cdea0c836b628fc8f14e87ca0ee69009991ff`

```dockerfile
```

-	Layers:
	-	`sha256:07ee0a7db8b47d5d9124feb9a57567522cd5d48ea973c757d1a388964d3f3c3f`  
		Last Modified: Tue, 18 Nov 2025 01:15:54 GMT  
		Size: 2.4 MB (2405018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019b25b2a46d8dd6c1a3d4866ef9c7b530adca6f476c7d1e22788e847d9c0c80`  
		Last Modified: Tue, 18 Nov 2025 01:15:55 GMT  
		Size: 20.2 KB (20210 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:d9e323fcb91f56561b2112affc8cad9663b484e1ee68e382b8fb056e115738d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112867364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1dc6eb11f759b21eb0fc83fccb2ebde531cb0dd277aad9fc87e79964c5fcdfe`
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
# Mon, 17 Nov 2025 23:17:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:17:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:17:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:17:09 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:17:09 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Mon, 17 Nov 2025 23:17:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 17 Nov 2025 23:17:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:17:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:17:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:3c0c9428a7f3bd24ecc53d01a84f8e5daf4cde2806733046039c236a5821dc20`  
		Last Modified: Mon, 17 Nov 2025 07:42:16 GMT  
		Size: 38.2 MB (38200298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a22257553b3802c6596eb2e8a386f6ec5fa8d2d2cb07b09334c277a7d4e628`  
		Last Modified: Mon, 17 Nov 2025 23:17:35 GMT  
		Size: 28.1 MB (28130148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185e493e59aae33ad4d89b939c95bf18b49214cb7ffeb662ee987f39fcd62cb7`  
		Last Modified: Mon, 17 Nov 2025 23:17:37 GMT  
		Size: 46.5 MB (46534501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ce69266f9eeac362ac0bcdf15665a93cad1d1aad0d45001d05dbdb54a17634`  
		Last Modified: Mon, 17 Nov 2025 23:17:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b0e44cab4dcb89dd0279812371d958cfdfa5fa0e5b5ab5d40ce7eaab9a3949`  
		Last Modified: Mon, 17 Nov 2025 23:17:31 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:50cea4b26a10f0e44fd6748fc49fe05dd90012669b95cf9dbfb6c41ad2c4cd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2424688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385731c23c52b0c3e0fc6a0d0e31936bb31e56993d1fb422d70f63cc5c5ec64e`

```dockerfile
```

-	Layers:
	-	`sha256:aec681d9bddefe520d85205a89230e356867859c9a24489d12347fb15147d040`  
		Last Modified: Tue, 18 Nov 2025 01:16:00 GMT  
		Size: 2.4 MB (2404376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d90db413e5e4f86b46e050b5b6e0c71b71d4e5d1fff07ca85142590bb27d45a`  
		Last Modified: Tue, 18 Nov 2025 01:16:01 GMT  
		Size: 20.3 KB (20312 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:04a02146aa6232eb5d43fb06f32b178f67e92cd7d686ccc77601f27faed9f97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121450845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d3afb71db44add1039ae849a932b1c45a927d4aac7be85692e87610b40757e`
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
ENV JAVA_VERSION=jdk-17.0.17+10
# Mon, 17 Nov 2025 23:27:18 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 17 Nov 2025 23:27:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:27:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:27:19 GMT
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
	-	`sha256:a60ec9b487aa6ac83d5fe09461afe8673df5725190f60433d98187c6d0293c82`  
		Last Modified: Mon, 17 Nov 2025 23:28:13 GMT  
		Size: 46.9 MB (46892959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ceeac0897f8e6cafbbbb4bd06b9ee44ffbbbcda88d55f371d668f336197066`  
		Last Modified: Mon, 17 Nov 2025 23:28:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffb8b7fdeb957dca4e2871b47730a07676b6a52f2ca608e5878ff88bbd5c9f3`  
		Last Modified: Mon, 17 Nov 2025 23:28:07 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:be242075a6c05edabcba0105000ec9d344244867abe9ee3f3520d3cda67ec691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca3153b127edcfaca319a1c73e5938fbd0b4045f0a78a0f025bdccdea329d76`

```dockerfile
```

-	Layers:
	-	`sha256:c106a9ce2496eb5ad49cb31c75b772af70cbe61302d8d51fa5e9350bc7e2dc48`  
		Last Modified: Tue, 18 Nov 2025 01:16:05 GMT  
		Size: 2.4 MB (2405023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48a2c5dbd16ef7a7b099f3643ba731f33eed2a11842638efda053591b032f417`  
		Last Modified: Tue, 18 Nov 2025 01:16:06 GMT  
		Size: 20.2 KB (20240 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:4e6bc818d8742c978cd76cc147b962e461e7135e6d2f6145a139c515f035a73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109891065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce789883b6248f73fb9828dafa8e72695abde3dab9fcc7866279bc90b37aa165`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 17 Nov 2025 06:55:26 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 06:55:26 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 06:55:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 17 Nov 2025 06:55:27 GMT
ENV container oci
# Mon, 17 Nov 2025 06:55:27 GMT
COPY dir:25054aa4a6c69856b29487af8bbbcbc6cee329e92c8eced671f2e9e1b0cc5041 in /      
# Mon, 17 Nov 2025 06:55:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 06:55:27 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 06:55:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 06:55:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 06:55:27 GMT
COPY file:4b85719f9a6183730ff3a5e6ddd6d5db079cb4351cb42de31d4da99485475023 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:55:27 GMT
COPY file:4b85719f9a6183730ff3a5e6ddd6d5db079cb4351cb42de31d4da99485475023 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:55:28 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "org.opencontainers.image.revision"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "build-date"="2025-11-17T06:55:15Z" "release"="1763362218"org.opencontainers.image.revision=f7f5876a3d86ded473c14b11d7491c2b6ddf39ce
# Mon, 17 Nov 2025 23:14:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:14:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:14:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:14:10 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:14:10 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Mon, 17 Nov 2025 23:15:37 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 17 Nov 2025 23:15:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:15:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:15:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8a5d6c48cb2c885ab264e85dd244af6174451d4cbdd00e240acc440b771129a5`  
		Last Modified: Mon, 17 Nov 2025 12:09:51 GMT  
		Size: 38.1 MB (38134810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57e774d711a58b879c6ccc775c62083a02983cfc56f05d852055b27aa227635`  
		Last Modified: Mon, 17 Nov 2025 23:14:42 GMT  
		Size: 27.7 MB (27727846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a022e5298b865addb4b2901316cbde4843359b3cb6bc7ba16daa222adc16773c`  
		Last Modified: Mon, 17 Nov 2025 23:16:03 GMT  
		Size: 44.0 MB (44025990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd051ed7d0364b661056648f8f948c11c91753547642b3ab728ed5cc2caa65`  
		Last Modified: Mon, 17 Nov 2025 23:15:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7949fe37f980ecf14b8ff72d13cfe9b9594fc9e116b23eb7ef342d5c70bfab59`  
		Last Modified: Mon, 17 Nov 2025 23:15:59 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7a3c2209663e62f89cdaca5361577a1c32fdb9900d802bdfd4cc8378379c28d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2417020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c9082625e08f1ab02fdac3ac1b90f28badf966e35ccec15293c5a50c6de2e8`

```dockerfile
```

-	Layers:
	-	`sha256:e8511507489fdbc48cbd1d39d6d2940f96a56b76582c4f126628df2bc26427cf`  
		Last Modified: Tue, 18 Nov 2025 01:16:11 GMT  
		Size: 2.4 MB (2396810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b6ac5d41805e1158d8f88b80934b3c59b9b1c9d999545237b5d27b71f2ac951`  
		Last Modified: Tue, 18 Nov 2025 01:16:12 GMT  
		Size: 20.2 KB (20210 bytes)  
		MIME: application/vnd.in-toto+json
