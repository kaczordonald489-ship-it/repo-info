## `swift:jammy`

```console
$ docker pull swift@sha256:0426da184baa96c7a9d9eb48e33d710ac8d028da55428958947a79f0ee27f5eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy` - linux; amd64

```console
$ docker pull swift@sha256:368bed0d61ee61abc0c85a47e301197b1b89646fb1a456a780fc546a6de8bc14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1233569754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d6f1ec782128ae3598c435fd2c259383af5a6249f1dea253dd55196bb8e867`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:49:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 15 Jan 2026 22:49:32 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 15 Jan 2026 22:49:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:49:32 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 15 Jan 2026 22:49:32 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Thu, 15 Jan 2026 22:49:32 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Thu, 15 Jan 2026 22:49:32 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Thu, 15 Jan 2026 22:49:32 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 15 Jan 2026 22:49:32 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 15 Jan 2026 22:50:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Thu, 15 Jan 2026 22:50:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dad709c284593abc70ab038cd9ab2a920a6364c2ef0999757197007b1360e2`  
		Last Modified: Thu, 15 Jan 2026 22:52:23 GMT  
		Size: 175.5 MB (175471835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7087d5f2c161f4a718c1f0db0c811eb7220eb139e0ab975d2d84661aa2f14c58`  
		Last Modified: Thu, 15 Jan 2026 22:52:38 GMT  
		Size: 1.0 GB (1028561078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca7b42dfd18f0847d063e711efc68be8bba9083121bdabb8a03ffdd8d03a223`  
		Last Modified: Thu, 15 Jan 2026 22:52:17 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:f15318ab6327fd87e6e387d9d5707b51d6fde2ab0827c0191c828d960f81fdf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8493403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38671cf2856ddbe089b29d99cc596de047fa8fc7f5730551e747e74662a28c91`

```dockerfile
```

-	Layers:
	-	`sha256:0c6d42d913cefd54190943d842b268a76ce418e8ac531f2e7d769a17a2392900`  
		Last Modified: Thu, 15 Jan 2026 22:52:17 GMT  
		Size: 8.5 MB (8477483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a545306650d8db16a79917ec18bfb155d665fa4ea8630c4bdcb4a86ef75b3e`  
		Last Modified: Thu, 15 Jan 2026 22:52:17 GMT  
		Size: 15.9 KB (15920 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:f56f97b0e6ede00c334fa6d4b405bb6e67c932382c566d59fa1df644e250453e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1222260122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70d65322ccac7c8d15c11b26859b83f4f4c15a5b1630482ba4aca9330322228`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:50:06 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 15 Jan 2026 22:50:06 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 15 Jan 2026 22:50:06 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:50:06 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 15 Jan 2026 22:50:06 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Thu, 15 Jan 2026 22:50:06 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Thu, 15 Jan 2026 22:50:06 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Thu, 15 Jan 2026 22:50:06 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 15 Jan 2026 22:50:06 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 15 Jan 2026 22:50:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Thu, 15 Jan 2026 22:50:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6942530efc7b5a324cbe1d6e9410f3ebcb571fdc5df6d0ff8e3ead3d2abb91`  
		Last Modified: Thu, 15 Jan 2026 22:53:03 GMT  
		Size: 171.8 MB (171802634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf2fc3623307bd356af1dd50b8f306634d5f98345554303a5e28cd70bfce206`  
		Last Modified: Thu, 15 Jan 2026 22:53:18 GMT  
		Size: 1.0 GB (1023073818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5b3ddfd5ac51309331a98c5862debff055dff46c95be739e803f80767b29b1`  
		Last Modified: Thu, 15 Jan 2026 22:52:57 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:b2a840952466853e1eb2e03fff155f8d526f53a3a85335b934a6e69714f7696c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8489211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7bff746f677678faa8da517006244f062c36cbaf88f207b78a815237126cad`

```dockerfile
```

-	Layers:
	-	`sha256:25f6a4099e38f638fa1a65a132b4a53e512b1852ba4d7e8913dfa10614511530`  
		Last Modified: Thu, 15 Jan 2026 22:52:58 GMT  
		Size: 8.5 MB (8473169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d3989fdade603c2f4759854e0fc63afa2b4ed044127c27df5cb8959cb6f0ce8`  
		Last Modified: Thu, 15 Jan 2026 22:52:57 GMT  
		Size: 16.0 KB (16042 bytes)  
		MIME: application/vnd.in-toto+json
