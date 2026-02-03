## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:6b258bca0976715bc66d944a48d8dde214770d63c5ca37bd21218b8b876c1259
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:14f8d51573734f5d2a7102c8bfb1d415b407184c4bb8e06a0fe7c73eb3cd21ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136397138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbcb8c87a312ebd5071582e3c5fccc8802f257f151d5b4fbdc719c4c79bb824d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jan 2026 08:58:27 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 26 Jan 2026 08:58:27 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 26 Jan 2026 08:58:28 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 26 Jan 2026 08:58:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 26 Jan 2026 08:58:28 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 26 Jan 2026 08:58:28 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 26 Jan 2026 08:58:28 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 26 Jan 2026 08:58:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 26 Jan 2026 08:58:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 26 Jan 2026 08:58:28 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 26 Jan 2026 08:58:28 GMT
ENV container oci
# Mon, 26 Jan 2026 08:58:29 GMT
COPY dir:01e64492bab95c9bb50415bb71c9d9af08d45cfa4202a0dced536614910ad969 in /      
# Mon, 26 Jan 2026 08:58:30 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 26 Jan 2026 08:58:30 GMT
CMD ["/bin/bash"]
# Mon, 26 Jan 2026 08:58:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 26 Jan 2026 08:58:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 26 Jan 2026 08:58:30 GMT
COPY file:3470321d029d513b81b4a742114d348fdf5a38e37806c6a8c9c4312f5537eee6 in /usr/share/buildinfo/labels.json      
# Mon, 26 Jan 2026 08:58:30 GMT
COPY file:3470321d029d513b81b4a742114d348fdf5a38e37806c6a8c9c4312f5537eee6 in /root/buildinfo/labels.json      
# Mon, 26 Jan 2026 08:58:31 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3c890e2f809f541b3b3eeac850c684f63b5a6b17" "org.opencontainers.image.revision"="3c890e2f809f541b3b3eeac850c684f63b5a6b17" "build-date"="2026-01-26T08:58:06Z" "org.opencontainers.image.created"="2026-01-26T08:58:06Z" "release"="1769417801"org.opencontainers.image.revision=3c890e2f809f541b3b3eeac850c684f63b5a6b17,org.opencontainers.image.created=2026-01-26T08:58:06Z
# Mon, 26 Jan 2026 22:12:24 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 26 Jan 2026 22:12:24 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 26 Jan 2026 22:12:24 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 26 Jan 2026 22:12:24 GMT
ARG SWIFT_PLATFORM=ubi9
# Mon, 26 Jan 2026 22:12:24 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Mon, 26 Jan 2026 22:12:24 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Mon, 26 Jan 2026 22:12:24 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 26 Jan 2026 22:12:24 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 26 Jan 2026 22:12:24 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:ed05ec7380a9ee435dfa899685fe7c2d7ac9c107c0a0c266a72521d623ef15e1`  
		Last Modified: Mon, 26 Jan 2026 10:06:05 GMT  
		Size: 80.0 MB (79975561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d60459bff3b9398cfeecb8a4d979339249e85c8b26ed87f8826d9528ee49c65`  
		Last Modified: Mon, 26 Jan 2026 22:12:40 GMT  
		Size: 56.4 MB (56421577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:94c2ce8698bef1fb724fa8a9bf7d7af13a0d5e89f5f52077a1c103e40742f3b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6417724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a265679475ba1836eda2b8238ecbeb6a24175ffbdc16d62d162b2dbc7a4e71`

```dockerfile
```

-	Layers:
	-	`sha256:6497ba97fc69ddd469a183523e4b60c87ef093f90f0651a91f90ee610dd8c7e4`  
		Last Modified: Mon, 26 Jan 2026 22:12:37 GMT  
		Size: 6.4 MB (6406256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb68f55700c23d4596da85c7c5ab60273ecb04adc14143a513ed8bb0d1044abd`  
		Last Modified: Mon, 26 Jan 2026 22:12:37 GMT  
		Size: 11.5 KB (11468 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:32a12d70e765bf93c931b58ac22445945a77fd4ee9f81608fdea35cc467490ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132687440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5797e5a781bbe7ef4cda13f6cf09f3763bb12342efba9f84b6829def3c42c28`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jan 2026 09:01:12 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 26 Jan 2026 09:01:12 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 26 Jan 2026 09:01:12 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 26 Jan 2026 09:01:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 26 Jan 2026 09:01:12 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 26 Jan 2026 09:01:12 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 26 Jan 2026 09:01:12 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 26 Jan 2026 09:01:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 26 Jan 2026 09:01:12 GMT
LABEL io.openshift.expose-services=""
# Mon, 26 Jan 2026 09:01:12 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 26 Jan 2026 09:01:12 GMT
ENV container oci
# Mon, 26 Jan 2026 09:01:15 GMT
COPY dir:22ad6c8479e720c0647f296efd652c954a8909c2b62a5e4799881d394d89895a in /      
# Mon, 26 Jan 2026 09:01:15 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 26 Jan 2026 09:01:15 GMT
CMD ["/bin/bash"]
# Mon, 26 Jan 2026 09:01:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 26 Jan 2026 09:01:16 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 26 Jan 2026 09:01:16 GMT
COPY file:e6ff405a24b5ac53dfa3fa24f4edeef55d95514be581f026049c11e5b11570c1 in /usr/share/buildinfo/labels.json      
# Mon, 26 Jan 2026 09:01:16 GMT
COPY file:e6ff405a24b5ac53dfa3fa24f4edeef55d95514be581f026049c11e5b11570c1 in /root/buildinfo/labels.json      
# Mon, 26 Jan 2026 09:01:16 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3c890e2f809f541b3b3eeac850c684f63b5a6b17" "org.opencontainers.image.revision"="3c890e2f809f541b3b3eeac850c684f63b5a6b17" "build-date"="2026-01-26T09:00:48Z" "org.opencontainers.image.created"="2026-01-26T09:00:48Z" "release"="1769417801"org.opencontainers.image.revision=3c890e2f809f541b3b3eeac850c684f63b5a6b17,org.opencontainers.image.created=2026-01-26T09:00:48Z
# Mon, 26 Jan 2026 22:11:34 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 26 Jan 2026 22:11:34 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 26 Jan 2026 22:11:34 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 26 Jan 2026 22:11:34 GMT
ARG SWIFT_PLATFORM=ubi9
# Mon, 26 Jan 2026 22:11:34 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Mon, 26 Jan 2026 22:11:34 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Mon, 26 Jan 2026 22:11:34 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 26 Jan 2026 22:11:34 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 26 Jan 2026 22:11:34 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:78a409151699ae26a49dbbd110b057aebf76392031c3bae976851c4dc6a53d2e`  
		Last Modified: Mon, 26 Jan 2026 10:11:52 GMT  
		Size: 77.7 MB (77716951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782705f3f1ecf61a54758b726d57904d6d5a677c6eacf398cdb348a4b0f66adb`  
		Last Modified: Mon, 26 Jan 2026 22:11:50 GMT  
		Size: 55.0 MB (54970489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:4afa4470ea0165fc99f1fcc62cf593845724d8aea2f2267fb2ad2b91beca1b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6413608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f203775b3fa30701c3aa17ca43fcae095f452e5864a77668e56a486a346f270`

```dockerfile
```

-	Layers:
	-	`sha256:7fc82f2443bee8a2cc5631ac5c08ae9919cc9e453ac8e9c40676a03a43d42c20`  
		Last Modified: Mon, 26 Jan 2026 22:11:48 GMT  
		Size: 6.4 MB (6402055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc56bdc42f4a07b78658a06e784be5f8862d223256f351a1d57c1a2ca52de971`  
		Last Modified: Mon, 26 Jan 2026 22:11:47 GMT  
		Size: 11.6 KB (11553 bytes)  
		MIME: application/vnd.in-toto+json
