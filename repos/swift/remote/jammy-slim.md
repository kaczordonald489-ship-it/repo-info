## `swift:jammy-slim`

```console
$ docker pull swift@sha256:d9b374970f26016011ab376e0a6f42c4293fc1c71164777a28857eb76d2e546e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy-slim` - linux; amd64

```console
$ docker pull swift@sha256:867abca8c25ee8235e97e62b41f909633b30c87a48dacb798edc54d7b09be324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98832462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6c6c882adc73d0dc1879a7ee29bb85fad7e5da144e765727ae87925a85e5d7`
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
# Thu, 15 Jan 2026 22:49:18 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 15 Jan 2026 22:49:18 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 15 Jan 2026 22:49:18 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:49:18 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 15 Jan 2026 22:49:18 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Thu, 15 Jan 2026 22:49:18 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Thu, 15 Jan 2026 22:49:18 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Thu, 15 Jan 2026 22:49:18 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 15 Jan 2026 22:49:18 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 15 Jan 2026 22:49:59 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f32d365e0c2c984c81eb51ec59f820f4a8dd493d76d3dd912c64434e5c0d6d`  
		Last Modified: Thu, 15 Jan 2026 22:50:12 GMT  
		Size: 19.2 MB (19223685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ada2a8fee7fba8632d8a7a885a576ba329a481736e51174a9e86cc656049a24`  
		Last Modified: Thu, 15 Jan 2026 22:50:13 GMT  
		Size: 50.1 MB (50072110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:7b6b8b44bd1ab925c063e287da249056bf3c1c9c3d906fdab170e45e919bb715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3069421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0c49cb417394e166b060c2476a5128862cc43aff68bff1fd743e4ec267c4e2`

```dockerfile
```

-	Layers:
	-	`sha256:fe65a5c22e9ffa862035017794c80e5a47ed81f08b33cfe7b9bacbcdcbc3fa9b`  
		Last Modified: Thu, 15 Jan 2026 22:50:11 GMT  
		Size: 3.1 MB (3055481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd6b772c4e6faf8c216063b120accb793442cb91f6f3f4a3e14270d7c35e81e0`  
		Last Modified: Thu, 15 Jan 2026 22:50:11 GMT  
		Size: 13.9 KB (13940 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:90de4b8e79357f1f3f6978914c01d82b2c70de4ee3ab059b76d7dc865125f9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95960661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e656d57434b47bd07162fee188454dad174f6cd4ac79c4ae0db45e0a427fcc`
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
# Thu, 15 Jan 2026 22:50:05 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 15 Jan 2026 22:50:05 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 15 Jan 2026 22:50:05 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:50:05 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 15 Jan 2026 22:50:05 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Thu, 15 Jan 2026 22:50:05 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Thu, 15 Jan 2026 22:50:05 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Thu, 15 Jan 2026 22:50:05 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 15 Jan 2026 22:50:05 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 15 Jan 2026 22:50:47 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c0f593b886bec68bc45e300fd38f95daf35159d16bca35318a6ee4f5edfa3`  
		Last Modified: Thu, 15 Jan 2026 22:51:00 GMT  
		Size: 19.1 MB (19100182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b760f092010f4144648c788d1787bbc5fe20999aebe456877790b31b72398053`  
		Last Modified: Thu, 15 Jan 2026 22:51:01 GMT  
		Size: 49.5 MB (49476982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:291ddca5a06f65e5e9c065357527201526bbdbbe45592cfb8650def571082c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3069815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a71bd21d8f934c96802da5c283ae479e1d0778a189d4a79aba5ba8d32add2c7`

```dockerfile
```

-	Layers:
	-	`sha256:6ec06bb968dc50c0292fc659db5c8261d05201e1eedff1427c87a68cd012c322`  
		Last Modified: Thu, 15 Jan 2026 22:51:00 GMT  
		Size: 3.1 MB (3055768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8bccbfe1f81798fc4d67218d2199b77bbb8cab24b03cd0209394c2467c29ad7`  
		Last Modified: Thu, 15 Jan 2026 22:50:59 GMT  
		Size: 14.0 KB (14047 bytes)  
		MIME: application/vnd.in-toto+json
