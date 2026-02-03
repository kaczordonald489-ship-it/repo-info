<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.16`](#varnish6016)
-	[`varnish:7.7`](#varnish77)
-	[`varnish:7.7-alpine`](#varnish77-alpine)
-	[`varnish:7.7.3`](#varnish773)
-	[`varnish:7.7.3-alpine`](#varnish773-alpine)
-	[`varnish:8`](#varnish8)
-	[`varnish:8-alpine`](#varnish8-alpine)
-	[`varnish:8.0`](#varnish80)
-	[`varnish:8.0-alpine`](#varnish80-alpine)
-	[`varnish:8.0.0`](#varnish800)
-	[`varnish:8.0.0-alpine`](#varnish800-alpine)
-	[`varnish:alpine`](#varnishalpine)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:fresh-alpine`](#varnishfresh-alpine)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:old`](#varnishold)
-	[`varnish:old-alpine`](#varnishold-alpine)
-	[`varnish:stable`](#varnishstable)

## `varnish:6.0`

```console
$ docker pull varnish@sha256:1ab688fc4ebddba39ef6a74e99216684e746eff0652450de0735b6bd65440a30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:ab873f9d6297aaf704e15c51082019a134f631eb3b1ce2a6667ce9776efff91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103549435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508454c11eef459eec1b24838fa146a92adf53177227c945433a94468dc8ef44`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:00 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 03 Feb 2026 02:43:00 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 03 Feb 2026 02:43:00 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 03 Feb 2026 02:43:00 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:43:00 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 03 Feb 2026 02:43:00 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:43:00 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:43:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:43:00 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:43:00 GMT
CMD []
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50561126bf2cc22facca3f7e3ae51518979813418f5824a39315a68d373f3530`  
		Last Modified: Tue, 03 Feb 2026 02:43:13 GMT  
		Size: 75.3 MB (75320192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab38f1120f1568d0b995b108553d91294c0a2538896178541b022b92de4aa82`  
		Last Modified: Tue, 03 Feb 2026 02:43:10 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:2fb567482b26431d7cab1dea2bf8da1dfb603459c5191ec50f1ab027bfbfe6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a173684a3089cd0110283ed9a05ff14f4d3edbe4c3c773cca369c84113fb766`

```dockerfile
```

-	Layers:
	-	`sha256:b4be3cd8fb2c42686018dad38803faae9885b789a83d4280fda0be7baf5c2f09`  
		Last Modified: Tue, 03 Feb 2026 02:43:10 GMT  
		Size: 12.7 KB (12656 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7a6c8173f7aa5404e58ed29e4745bceb42846de891b7e618f23f57bc28572be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98409279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59626750601c1f20862e364508d4d8fc3fa142ff758288f26a51d4106297436`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:45:58 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 03 Feb 2026 02:45:58 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 03 Feb 2026 02:45:58 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 03 Feb 2026 02:45:58 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:45:58 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 03 Feb 2026 02:45:58 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:45:58 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:45:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:45:58 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:45:58 GMT
CMD []
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0f6557bfcc6f23ce7e667a0ce3c4c4192c63b3bf041e192ec03f7f5bb4d2dc`  
		Last Modified: Tue, 03 Feb 2026 02:46:10 GMT  
		Size: 70.3 MB (70300699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8ba01b6da17f8bec0293d3ce5cb5d987d71179980075c132bf8d1ef9db4290`  
		Last Modified: Tue, 03 Feb 2026 02:46:08 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:410f1c52f38ce61afeebfde3cd901ba6f37bc179c6f2931d4853512e50e652e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38856403b71349f8a9f6565a7c08213d684010a327fb87fa2f2ef6cc564a715`

```dockerfile
```

-	Layers:
	-	`sha256:a12c2993cd26360dd6a72b78b348c569b69edb05fdc680e97a2faada87050704`  
		Last Modified: Tue, 03 Feb 2026 02:46:08 GMT  
		Size: 12.7 KB (12749 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.16`

```console
$ docker pull varnish@sha256:1ab688fc4ebddba39ef6a74e99216684e746eff0652450de0735b6bd65440a30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0.16` - linux; amd64

```console
$ docker pull varnish@sha256:ab873f9d6297aaf704e15c51082019a134f631eb3b1ce2a6667ce9776efff91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103549435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508454c11eef459eec1b24838fa146a92adf53177227c945433a94468dc8ef44`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:00 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 03 Feb 2026 02:43:00 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 03 Feb 2026 02:43:00 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 03 Feb 2026 02:43:00 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:43:00 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 03 Feb 2026 02:43:00 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:43:00 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:43:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:43:00 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:43:00 GMT
CMD []
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50561126bf2cc22facca3f7e3ae51518979813418f5824a39315a68d373f3530`  
		Last Modified: Tue, 03 Feb 2026 02:43:13 GMT  
		Size: 75.3 MB (75320192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab38f1120f1568d0b995b108553d91294c0a2538896178541b022b92de4aa82`  
		Last Modified: Tue, 03 Feb 2026 02:43:10 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:2fb567482b26431d7cab1dea2bf8da1dfb603459c5191ec50f1ab027bfbfe6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a173684a3089cd0110283ed9a05ff14f4d3edbe4c3c773cca369c84113fb766`

```dockerfile
```

-	Layers:
	-	`sha256:b4be3cd8fb2c42686018dad38803faae9885b789a83d4280fda0be7baf5c2f09`  
		Last Modified: Tue, 03 Feb 2026 02:43:10 GMT  
		Size: 12.7 KB (12656 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7a6c8173f7aa5404e58ed29e4745bceb42846de891b7e618f23f57bc28572be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98409279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59626750601c1f20862e364508d4d8fc3fa142ff758288f26a51d4106297436`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:45:58 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 03 Feb 2026 02:45:58 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 03 Feb 2026 02:45:58 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 03 Feb 2026 02:45:58 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:45:58 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 03 Feb 2026 02:45:58 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:45:58 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:45:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:45:58 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:45:58 GMT
CMD []
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0f6557bfcc6f23ce7e667a0ce3c4c4192c63b3bf041e192ec03f7f5bb4d2dc`  
		Last Modified: Tue, 03 Feb 2026 02:46:10 GMT  
		Size: 70.3 MB (70300699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8ba01b6da17f8bec0293d3ce5cb5d987d71179980075c132bf8d1ef9db4290`  
		Last Modified: Tue, 03 Feb 2026 02:46:08 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:410f1c52f38ce61afeebfde3cd901ba6f37bc179c6f2931d4853512e50e652e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38856403b71349f8a9f6565a7c08213d684010a327fb87fa2f2ef6cc564a715`

```dockerfile
```

-	Layers:
	-	`sha256:a12c2993cd26360dd6a72b78b348c569b69edb05fdc680e97a2faada87050704`  
		Last Modified: Tue, 03 Feb 2026 02:46:08 GMT  
		Size: 12.7 KB (12749 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7`

```console
$ docker pull varnish@sha256:fbcfe0d9eecf40eb5a16381d7605237f4d6e7188b99d556f503923e2eb4e2155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:7.7` - linux; amd64

```console
$ docker pull varnish@sha256:88bced2b343bab9b233dff35c42eb529e4e982a017e3624aa524151c4f3c5ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116346186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb0514cc7fb6bd6c70385fa61c4ddd976f3428283882296246734e07d1fc2c4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:47:07 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 03 Feb 2026 03:47:07 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 03 Feb 2026 03:47:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 03 Feb 2026 03:47:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 03 Feb 2026 03:47:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 03:47:07 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 03:47:07 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 03:47:07 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 03:47:07 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:47:07 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 03:47:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 03:47:07 GMT
USER varnish
# Tue, 03 Feb 2026 03:47:07 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 03:47:07 GMT
CMD []
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78d5cb1bba1feacb6362d4014b338d3e9c025e5028144a2005ee8929a5127c2`  
		Last Modified: Tue, 03 Feb 2026 03:47:22 GMT  
		Size: 86.6 MB (86565545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73003d45cacff21c1022a462a7cb84f58eb827b7fd5700aa489f8e4eda8fe3ca`  
		Last Modified: Tue, 03 Feb 2026 03:47:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222ebdf0dda00e72527e9458a718979edaf63cec3413338d2b8b2084f310e64d`  
		Last Modified: Tue, 03 Feb 2026 03:47:19 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:f2794fd830479d9cd6cd7e3bb2d3378558618386e5407eaf115f38aacde2ff0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4349af5775296e1a8561e2dd9e8c10df40a4e2bff82de672cf08ebdca8c7ba`

```dockerfile
```

-	Layers:
	-	`sha256:aad51e36ff0df4b53cf9ac4ad53f25f3ff02382bea98e6eab560caff9307a41a`  
		Last Modified: Tue, 03 Feb 2026 03:47:19 GMT  
		Size: 19.1 KB (19053 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8aaaa04e878ae972934d9be59b6572128e5582dc248173ca484de4dcc476797d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110527705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96367711e92e07d47a4f94f00f6f9412e44745900894f5a5f8abdacee5e52d16`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:28 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 03 Feb 2026 02:46:28 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 03 Feb 2026 02:46:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 03 Feb 2026 02:46:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 03 Feb 2026 02:46:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:46:28 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 02:46:28 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 02:46:29 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:46:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:46:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:46:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:46:29 GMT
USER varnish
# Tue, 03 Feb 2026 02:46:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:46:29 GMT
CMD []
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc96d349d263ff12e47f8954a315c622c6884059baa940d9459de0f365a989b`  
		Last Modified: Tue, 03 Feb 2026 02:46:41 GMT  
		Size: 80.4 MB (80385593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfceea4e1c6f838873a5ec8d3723a7db7dcbdfaab3d32ff6355c7acb562c196`  
		Last Modified: Tue, 03 Feb 2026 02:46:39 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1ff5558ad5eca044452183365b8668a746f335ea6215af14fe6aedb2f8a34b`  
		Last Modified: Tue, 03 Feb 2026 02:46:39 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:5821f3408fb4a85ebc4fa033459d119f01b6d2603af27971c7faba368c7ee923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2113d13c12567f525dacd6b8996978ebea79ce7205da225db606c24f342d0a7`

```dockerfile
```

-	Layers:
	-	`sha256:d1debaf1ed2c15b3234a6b5e5924c1d8c0cf094b882a64d5b588a7be88ac7a0c`  
		Last Modified: Tue, 03 Feb 2026 02:46:39 GMT  
		Size: 19.1 KB (19144 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7-alpine`

```console
$ docker pull varnish@sha256:95deada23d0ef0cd1005cfe32463f3390f31a63f13682996bccdb5b01ea7f291
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:7.7-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:8aa05c32b87720c21201f23664c14e58218e6a8bf2d240192d61ddf7cbda1543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80549045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4b3a4a43c039fde71b875c7d203b302d8f539cf7d6ea66bd68203662cfd84c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:08 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_VERSION=7.7.3
# Wed, 28 Jan 2026 02:40:08 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Wed, 28 Jan 2026 02:40:08 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 02:40:08 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 02:40:08 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 02:40:08 GMT
USER varnish
# Wed, 28 Jan 2026 02:40:08 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 02:40:08 GMT
CMD []
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a04f2c14282af7f7e529680683c4281801fe0d25060b1f1849b5b10ce75207`  
		Last Modified: Wed, 28 Jan 2026 02:40:21 GMT  
		Size: 76.7 MB (76742117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431ff28a6f82e4f8ababee51c3cba66677a5d436c027f202cff74cdfaa22b2fa`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e3640c70635b2fb032b6853f07c74fea52315c1157b90d728b171a25b855a6`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:fdbfb5b2598b29dc6fcc4576ff7054763636eb08b994d768f3b662e46af7cada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70f4eca00c39ae1979c06ee1adef5eba46dbea1c6b4bb8dddc0c9da233cf6a7`

```dockerfile
```

-	Layers:
	-	`sha256:af700eba3659b121f6e7f4f91bec07eb72c5b17f00d6e85559d34eae8c6939a5`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 18.8 KB (18840 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e08f69115921e2084edfdc49c70244ca6e2c2830f7cd882ce3fc68302320e795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77534209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68875f332b81c8a9f0b8157adf6aca453c9ce66478997f3899c83048bee86613`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:14 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_VERSION=7.7.3
# Wed, 28 Jan 2026 02:40:14 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Wed, 28 Jan 2026 02:40:14 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 02:40:14 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 02:40:14 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 02:40:14 GMT
USER varnish
# Wed, 28 Jan 2026 02:40:14 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 02:40:14 GMT
CMD []
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf710ef050705257a3b1ccc4556cc95fed48da6153f9dee22ff258bd3f4a2704`  
		Last Modified: Wed, 28 Jan 2026 02:40:27 GMT  
		Size: 73.4 MB (73392634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed23c78500b776f154686015e0536a78e6cbcf306c95ed7a6dab1769067fbaa5`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9086e9e0255e2a3935f436f74da42da55a0fa0de25ce1aaee7c10dfba1a1882b`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:b3342940e958392acaafe6dc63153ff912a0c9ef8b4d773520b8d0e57c4f8910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d64f6ef49b079355c29686ebba4c3599233207673cca81322e56af6cf83e9fb`

```dockerfile
```

-	Layers:
	-	`sha256:14078e9f50c83d2b5b9d2201394b09e185e22d9f12db3c8385b168e27f1b5679`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 18.9 KB (18933 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7.3`

```console
$ docker pull varnish@sha256:fbcfe0d9eecf40eb5a16381d7605237f4d6e7188b99d556f503923e2eb4e2155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:7.7.3` - linux; amd64

```console
$ docker pull varnish@sha256:88bced2b343bab9b233dff35c42eb529e4e982a017e3624aa524151c4f3c5ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116346186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb0514cc7fb6bd6c70385fa61c4ddd976f3428283882296246734e07d1fc2c4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:47:07 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 03 Feb 2026 03:47:07 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 03 Feb 2026 03:47:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 03 Feb 2026 03:47:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 03 Feb 2026 03:47:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 03:47:07 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 03:47:07 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 03:47:07 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 03:47:07 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:47:07 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 03:47:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 03:47:07 GMT
USER varnish
# Tue, 03 Feb 2026 03:47:07 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 03:47:07 GMT
CMD []
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78d5cb1bba1feacb6362d4014b338d3e9c025e5028144a2005ee8929a5127c2`  
		Last Modified: Tue, 03 Feb 2026 03:47:22 GMT  
		Size: 86.6 MB (86565545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73003d45cacff21c1022a462a7cb84f58eb827b7fd5700aa489f8e4eda8fe3ca`  
		Last Modified: Tue, 03 Feb 2026 03:47:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222ebdf0dda00e72527e9458a718979edaf63cec3413338d2b8b2084f310e64d`  
		Last Modified: Tue, 03 Feb 2026 03:47:19 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:f2794fd830479d9cd6cd7e3bb2d3378558618386e5407eaf115f38aacde2ff0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4349af5775296e1a8561e2dd9e8c10df40a4e2bff82de672cf08ebdca8c7ba`

```dockerfile
```

-	Layers:
	-	`sha256:aad51e36ff0df4b53cf9ac4ad53f25f3ff02382bea98e6eab560caff9307a41a`  
		Last Modified: Tue, 03 Feb 2026 03:47:19 GMT  
		Size: 19.1 KB (19053 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8aaaa04e878ae972934d9be59b6572128e5582dc248173ca484de4dcc476797d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110527705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96367711e92e07d47a4f94f00f6f9412e44745900894f5a5f8abdacee5e52d16`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:28 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 03 Feb 2026 02:46:28 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 03 Feb 2026 02:46:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 03 Feb 2026 02:46:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 03 Feb 2026 02:46:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:46:28 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 02:46:28 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 02:46:29 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:46:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:46:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:46:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:46:29 GMT
USER varnish
# Tue, 03 Feb 2026 02:46:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:46:29 GMT
CMD []
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc96d349d263ff12e47f8954a315c622c6884059baa940d9459de0f365a989b`  
		Last Modified: Tue, 03 Feb 2026 02:46:41 GMT  
		Size: 80.4 MB (80385593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfceea4e1c6f838873a5ec8d3723a7db7dcbdfaab3d32ff6355c7acb562c196`  
		Last Modified: Tue, 03 Feb 2026 02:46:39 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1ff5558ad5eca044452183365b8668a746f335ea6215af14fe6aedb2f8a34b`  
		Last Modified: Tue, 03 Feb 2026 02:46:39 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:5821f3408fb4a85ebc4fa033459d119f01b6d2603af27971c7faba368c7ee923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2113d13c12567f525dacd6b8996978ebea79ce7205da225db606c24f342d0a7`

```dockerfile
```

-	Layers:
	-	`sha256:d1debaf1ed2c15b3234a6b5e5924c1d8c0cf094b882a64d5b588a7be88ac7a0c`  
		Last Modified: Tue, 03 Feb 2026 02:46:39 GMT  
		Size: 19.1 KB (19144 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7.3-alpine`

```console
$ docker pull varnish@sha256:95deada23d0ef0cd1005cfe32463f3390f31a63f13682996bccdb5b01ea7f291
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:7.7.3-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:8aa05c32b87720c21201f23664c14e58218e6a8bf2d240192d61ddf7cbda1543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80549045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4b3a4a43c039fde71b875c7d203b302d8f539cf7d6ea66bd68203662cfd84c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:08 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_VERSION=7.7.3
# Wed, 28 Jan 2026 02:40:08 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Wed, 28 Jan 2026 02:40:08 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 02:40:08 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 02:40:08 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 02:40:08 GMT
USER varnish
# Wed, 28 Jan 2026 02:40:08 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 02:40:08 GMT
CMD []
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a04f2c14282af7f7e529680683c4281801fe0d25060b1f1849b5b10ce75207`  
		Last Modified: Wed, 28 Jan 2026 02:40:21 GMT  
		Size: 76.7 MB (76742117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431ff28a6f82e4f8ababee51c3cba66677a5d436c027f202cff74cdfaa22b2fa`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e3640c70635b2fb032b6853f07c74fea52315c1157b90d728b171a25b855a6`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:fdbfb5b2598b29dc6fcc4576ff7054763636eb08b994d768f3b662e46af7cada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70f4eca00c39ae1979c06ee1adef5eba46dbea1c6b4bb8dddc0c9da233cf6a7`

```dockerfile
```

-	Layers:
	-	`sha256:af700eba3659b121f6e7f4f91bec07eb72c5b17f00d6e85559d34eae8c6939a5`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 18.8 KB (18840 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e08f69115921e2084edfdc49c70244ca6e2c2830f7cd882ce3fc68302320e795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77534209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68875f332b81c8a9f0b8157adf6aca453c9ce66478997f3899c83048bee86613`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:14 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_VERSION=7.7.3
# Wed, 28 Jan 2026 02:40:14 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Wed, 28 Jan 2026 02:40:14 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 02:40:14 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 02:40:14 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 02:40:14 GMT
USER varnish
# Wed, 28 Jan 2026 02:40:14 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 02:40:14 GMT
CMD []
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf710ef050705257a3b1ccc4556cc95fed48da6153f9dee22ff258bd3f4a2704`  
		Last Modified: Wed, 28 Jan 2026 02:40:27 GMT  
		Size: 73.4 MB (73392634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed23c78500b776f154686015e0536a78e6cbcf306c95ed7a6dab1769067fbaa5`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9086e9e0255e2a3935f436f74da42da55a0fa0de25ce1aaee7c10dfba1a1882b`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:b3342940e958392acaafe6dc63153ff912a0c9ef8b4d773520b8d0e57c4f8910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d64f6ef49b079355c29686ebba4c3599233207673cca81322e56af6cf83e9fb`

```dockerfile
```

-	Layers:
	-	`sha256:14078e9f50c83d2b5b9d2201394b09e185e22d9f12db3c8385b168e27f1b5679`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 18.9 KB (18933 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8`

```console
$ docker pull varnish@sha256:226a23129ecf7c69d670e409fc8be49d1c1bfc2fad8557f66f62dd8dbdcc3fe1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8` - linux; amd64

```console
$ docker pull varnish@sha256:d352c9681d9a8ba5e56689cafcdeaf13be9b4f3eb50702e8cdf60aa2462e8211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121962336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d60cea63dbf0bfb59e087cd0da723866bb4b226c32f3e2bde8235fed975db9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:21 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 03 Feb 2026 02:42:21 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-4
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 03 Feb 2026 02:42:21 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 02:42:21 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.0-4 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         if [ "$(dpkg --print-architecture)" = "amd64" ]; then         EXTRA_VMODS="vmod-cfg=${VARNISH_VERSION}";     else         EXTRA_VMODS= ;     fi;     apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				${EXTRA_VMODS} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:42:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:42:21 GMT
USER varnish
# Tue, 03 Feb 2026 02:42:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:42:21 GMT
CMD []
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96ce5385998e16a6fb7ef0226d1f20b45298bed9dc060e1bf28d50b55ab6b44`  
		Last Modified: Tue, 03 Feb 2026 02:42:36 GMT  
		Size: 92.2 MB (92180627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d975aae4b8d991a67a2469a23763d6acfdf59ac627560c2f790c080c24018d71`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850971c09b6d0682278837f5c6a4e9d01b30dccf52df0692fdf7a668c729420a`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f107400f6a38a9314a93b12c9392f94b30b5f795125cf51885a1dbe8c0c49a`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:362009b8c48f6e6c1df889fed612bea5e9606c328aa1844be7840919bae04d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 KB (21545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6e6c2c755a94af44f9b0afc723c139b2357ebdcd63288ebae6773749f97cdf`

```dockerfile
```

-	Layers:
	-	`sha256:d5d34eb7eddcf079b45cf5c06eebd4f2d4f2e58f53d5cd95788bbd42eb37fb80`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 21.5 KB (21545 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:cf120eda11e2042d4d3b042a843ba90d71839f7ea5da41b44631b161444b5138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114675943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12599516796d11291cda900c5d30ad79d4ffb66b35e6a2cdb49dac94423d3a43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:45:15 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 03 Feb 2026 02:45:15 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-4
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 03 Feb 2026 02:45:15 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 02:45:15 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.0-4 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         if [ "$(dpkg --print-architecture)" = "amd64" ]; then         EXTRA_VMODS="vmod-cfg=${VARNISH_VERSION}";     else         EXTRA_VMODS= ;     fi;     apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				${EXTRA_VMODS} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:45:15 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:45:15 GMT
USER varnish
# Tue, 03 Feb 2026 02:45:15 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:45:15 GMT
CMD []
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bd55ca0600e6a3e876c49088103397b7b05e6094487e7a60107919cd3051bd`  
		Last Modified: Tue, 03 Feb 2026 02:45:29 GMT  
		Size: 84.5 MB (84532762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66978ff33f084ea694488f026f19a130f485eb75eb669ee030fb8248faef72af`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad63af1ab6603e791221ce68a695341b32ed14e8a5be37150f8c6a65a50df61`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c278d8bcf8a98fe62140fe7ddf9d61e65feef87d547df1c78ea939529cf33bb3`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:c782dfe175af659dbef2371903f4af0180af017bc4eb89ea45965a4f385f8b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44de953c67739aa87eb699753315560c3e5f898d721b253a78ee9b0bece90d32`

```dockerfile
```

-	Layers:
	-	`sha256:76d12f419243f487cfd1893ef954181ed8dbeaeb13f0ff1923e98d6f37cf3ad0`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 21.7 KB (21661 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8-alpine`

```console
$ docker pull varnish@sha256:a84e1d4adb58b1f0594efbc95b9854c37040aafbbb990fa4889d6520a2feea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:313c1e39011cd7ad60a797012574cf43ec9b3f652368766eb8f658134c798e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91772446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2dd9ec648dcf29eb5e73fb988e6337591e92a9cd3dc40566579e5dfc69a0b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:32:53 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:32:53 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:32:53 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:32:53 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:32:53 GMT
USER varnish
# Wed, 28 Jan 2026 18:32:53 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:32:53 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a023c28f50298fde5fdebfb9183a14c01add9e56dbd5e465fbb5f20091e66b26`  
		Last Modified: Wed, 28 Jan 2026 18:33:06 GMT  
		Size: 87.9 MB (87907492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43ab80124716fd6fd1dea26c10cb19d9956f00e9310f54b211bedf51903d0a8`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed37e8718e0c2f976041d5825a05251d01a2cccd7ea651e4faba3892a74a3c7`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3e6fd73e1c2d4af26c7e5621e4317be18bcfc94308e5b6beb6a72cd170854`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f5a6df222303ec11afdd7aba8e6ce117da6dca249c39fcb4c7bf80666ffa4e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e35f19446543c684a63b0d3e4df83aadc77b84dbd5ba27017204e16548e5cf`

```dockerfile
```

-	Layers:
	-	`sha256:2472b92b11950f0ccd3dac0294bf9c31e2174882ccbec33de210089fab5ec428`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 20.7 KB (20687 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:5012ddbf256e65054b99e3f27bae23f4973c3427d3e69882536053454ae033dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83538388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6858c7d69f1ef19e0c93fe2588a96b69e65e9c3918e563a55fbb19e09a0b33`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:45:55 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:45:55 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:45:55 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:45:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:45:55 GMT
USER varnish
# Wed, 28 Jan 2026 18:45:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da24d757c3e5486bd934e3ed2ab115041c3cd5eeca9bf88d5e0fe5e73f1c01bd`  
		Last Modified: Wed, 28 Jan 2026 18:46:07 GMT  
		Size: 79.3 MB (79338167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76a29fb6864bfa14adb7c64c7cd4a92ae6740e89da8dc5544e4032c5670f7d1`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ca8d9ee0017ec696497e5afaafe59a065eb02feac3a273c07d5ec27b56fd34`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d83ce2d813532284a2265d0ea39dfcbd5a65dc2b4b6c09af121ab8edd31c46b`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5cb09b7c875b608f6488d947d4fae3713abeb40a55f44b7ce5e011b5bdfb77cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c3dbcb1e49cbee0a8f8b985cb8f495cd814543ff07752a680cb0d5cb573948`

```dockerfile
```

-	Layers:
	-	`sha256:7b786c97ea1f2e5b349e6674dcdbee3e869393e0ba482f7be67c9bab7fd4be22`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0`

```console
$ docker pull varnish@sha256:226a23129ecf7c69d670e409fc8be49d1c1bfc2fad8557f66f62dd8dbdcc3fe1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0` - linux; amd64

```console
$ docker pull varnish@sha256:d352c9681d9a8ba5e56689cafcdeaf13be9b4f3eb50702e8cdf60aa2462e8211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121962336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d60cea63dbf0bfb59e087cd0da723866bb4b226c32f3e2bde8235fed975db9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:21 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 03 Feb 2026 02:42:21 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-4
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 03 Feb 2026 02:42:21 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 02:42:21 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.0-4 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         if [ "$(dpkg --print-architecture)" = "amd64" ]; then         EXTRA_VMODS="vmod-cfg=${VARNISH_VERSION}";     else         EXTRA_VMODS= ;     fi;     apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				${EXTRA_VMODS} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:42:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:42:21 GMT
USER varnish
# Tue, 03 Feb 2026 02:42:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:42:21 GMT
CMD []
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96ce5385998e16a6fb7ef0226d1f20b45298bed9dc060e1bf28d50b55ab6b44`  
		Last Modified: Tue, 03 Feb 2026 02:42:36 GMT  
		Size: 92.2 MB (92180627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d975aae4b8d991a67a2469a23763d6acfdf59ac627560c2f790c080c24018d71`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850971c09b6d0682278837f5c6a4e9d01b30dccf52df0692fdf7a668c729420a`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f107400f6a38a9314a93b12c9392f94b30b5f795125cf51885a1dbe8c0c49a`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:362009b8c48f6e6c1df889fed612bea5e9606c328aa1844be7840919bae04d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 KB (21545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6e6c2c755a94af44f9b0afc723c139b2357ebdcd63288ebae6773749f97cdf`

```dockerfile
```

-	Layers:
	-	`sha256:d5d34eb7eddcf079b45cf5c06eebd4f2d4f2e58f53d5cd95788bbd42eb37fb80`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 21.5 KB (21545 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:cf120eda11e2042d4d3b042a843ba90d71839f7ea5da41b44631b161444b5138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114675943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12599516796d11291cda900c5d30ad79d4ffb66b35e6a2cdb49dac94423d3a43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:45:15 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 03 Feb 2026 02:45:15 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-4
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 03 Feb 2026 02:45:15 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 02:45:15 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.0-4 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         if [ "$(dpkg --print-architecture)" = "amd64" ]; then         EXTRA_VMODS="vmod-cfg=${VARNISH_VERSION}";     else         EXTRA_VMODS= ;     fi;     apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				${EXTRA_VMODS} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:45:15 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:45:15 GMT
USER varnish
# Tue, 03 Feb 2026 02:45:15 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:45:15 GMT
CMD []
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bd55ca0600e6a3e876c49088103397b7b05e6094487e7a60107919cd3051bd`  
		Last Modified: Tue, 03 Feb 2026 02:45:29 GMT  
		Size: 84.5 MB (84532762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66978ff33f084ea694488f026f19a130f485eb75eb669ee030fb8248faef72af`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad63af1ab6603e791221ce68a695341b32ed14e8a5be37150f8c6a65a50df61`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c278d8bcf8a98fe62140fe7ddf9d61e65feef87d547df1c78ea939529cf33bb3`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:c782dfe175af659dbef2371903f4af0180af017bc4eb89ea45965a4f385f8b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44de953c67739aa87eb699753315560c3e5f898d721b253a78ee9b0bece90d32`

```dockerfile
```

-	Layers:
	-	`sha256:76d12f419243f487cfd1893ef954181ed8dbeaeb13f0ff1923e98d6f37cf3ad0`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 21.7 KB (21661 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0-alpine`

```console
$ docker pull varnish@sha256:a84e1d4adb58b1f0594efbc95b9854c37040aafbbb990fa4889d6520a2feea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:313c1e39011cd7ad60a797012574cf43ec9b3f652368766eb8f658134c798e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91772446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2dd9ec648dcf29eb5e73fb988e6337591e92a9cd3dc40566579e5dfc69a0b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:32:53 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:32:53 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:32:53 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:32:53 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:32:53 GMT
USER varnish
# Wed, 28 Jan 2026 18:32:53 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:32:53 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a023c28f50298fde5fdebfb9183a14c01add9e56dbd5e465fbb5f20091e66b26`  
		Last Modified: Wed, 28 Jan 2026 18:33:06 GMT  
		Size: 87.9 MB (87907492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43ab80124716fd6fd1dea26c10cb19d9956f00e9310f54b211bedf51903d0a8`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed37e8718e0c2f976041d5825a05251d01a2cccd7ea651e4faba3892a74a3c7`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3e6fd73e1c2d4af26c7e5621e4317be18bcfc94308e5b6beb6a72cd170854`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f5a6df222303ec11afdd7aba8e6ce117da6dca249c39fcb4c7bf80666ffa4e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e35f19446543c684a63b0d3e4df83aadc77b84dbd5ba27017204e16548e5cf`

```dockerfile
```

-	Layers:
	-	`sha256:2472b92b11950f0ccd3dac0294bf9c31e2174882ccbec33de210089fab5ec428`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 20.7 KB (20687 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:5012ddbf256e65054b99e3f27bae23f4973c3427d3e69882536053454ae033dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83538388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6858c7d69f1ef19e0c93fe2588a96b69e65e9c3918e563a55fbb19e09a0b33`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:45:55 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:45:55 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:45:55 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:45:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:45:55 GMT
USER varnish
# Wed, 28 Jan 2026 18:45:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da24d757c3e5486bd934e3ed2ab115041c3cd5eeca9bf88d5e0fe5e73f1c01bd`  
		Last Modified: Wed, 28 Jan 2026 18:46:07 GMT  
		Size: 79.3 MB (79338167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76a29fb6864bfa14adb7c64c7cd4a92ae6740e89da8dc5544e4032c5670f7d1`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ca8d9ee0017ec696497e5afaafe59a065eb02feac3a273c07d5ec27b56fd34`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d83ce2d813532284a2265d0ea39dfcbd5a65dc2b4b6c09af121ab8edd31c46b`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5cb09b7c875b608f6488d947d4fae3713abeb40a55f44b7ce5e011b5bdfb77cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c3dbcb1e49cbee0a8f8b985cb8f495cd814543ff07752a680cb0d5cb573948`

```dockerfile
```

-	Layers:
	-	`sha256:7b786c97ea1f2e5b349e6674dcdbee3e869393e0ba482f7be67c9bab7fd4be22`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0.0`

```console
$ docker pull varnish@sha256:226a23129ecf7c69d670e409fc8be49d1c1bfc2fad8557f66f62dd8dbdcc3fe1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0.0` - linux; amd64

```console
$ docker pull varnish@sha256:d352c9681d9a8ba5e56689cafcdeaf13be9b4f3eb50702e8cdf60aa2462e8211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121962336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d60cea63dbf0bfb59e087cd0da723866bb4b226c32f3e2bde8235fed975db9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:21 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 03 Feb 2026 02:42:21 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-4
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 03 Feb 2026 02:42:21 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 02:42:21 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.0-4 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         if [ "$(dpkg --print-architecture)" = "amd64" ]; then         EXTRA_VMODS="vmod-cfg=${VARNISH_VERSION}";     else         EXTRA_VMODS= ;     fi;     apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				${EXTRA_VMODS} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:42:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:42:21 GMT
USER varnish
# Tue, 03 Feb 2026 02:42:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:42:21 GMT
CMD []
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96ce5385998e16a6fb7ef0226d1f20b45298bed9dc060e1bf28d50b55ab6b44`  
		Last Modified: Tue, 03 Feb 2026 02:42:36 GMT  
		Size: 92.2 MB (92180627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d975aae4b8d991a67a2469a23763d6acfdf59ac627560c2f790c080c24018d71`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850971c09b6d0682278837f5c6a4e9d01b30dccf52df0692fdf7a668c729420a`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f107400f6a38a9314a93b12c9392f94b30b5f795125cf51885a1dbe8c0c49a`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0` - unknown; unknown

```console
$ docker pull varnish@sha256:362009b8c48f6e6c1df889fed612bea5e9606c328aa1844be7840919bae04d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 KB (21545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6e6c2c755a94af44f9b0afc723c139b2357ebdcd63288ebae6773749f97cdf`

```dockerfile
```

-	Layers:
	-	`sha256:d5d34eb7eddcf079b45cf5c06eebd4f2d4f2e58f53d5cd95788bbd42eb37fb80`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 21.5 KB (21545 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:cf120eda11e2042d4d3b042a843ba90d71839f7ea5da41b44631b161444b5138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114675943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12599516796d11291cda900c5d30ad79d4ffb66b35e6a2cdb49dac94423d3a43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:45:15 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 03 Feb 2026 02:45:15 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-4
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 03 Feb 2026 02:45:15 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 02:45:15 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.0-4 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         if [ "$(dpkg --print-architecture)" = "amd64" ]; then         EXTRA_VMODS="vmod-cfg=${VARNISH_VERSION}";     else         EXTRA_VMODS= ;     fi;     apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				${EXTRA_VMODS} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:45:15 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:45:15 GMT
USER varnish
# Tue, 03 Feb 2026 02:45:15 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:45:15 GMT
CMD []
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bd55ca0600e6a3e876c49088103397b7b05e6094487e7a60107919cd3051bd`  
		Last Modified: Tue, 03 Feb 2026 02:45:29 GMT  
		Size: 84.5 MB (84532762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66978ff33f084ea694488f026f19a130f485eb75eb669ee030fb8248faef72af`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad63af1ab6603e791221ce68a695341b32ed14e8a5be37150f8c6a65a50df61`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c278d8bcf8a98fe62140fe7ddf9d61e65feef87d547df1c78ea939529cf33bb3`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0` - unknown; unknown

```console
$ docker pull varnish@sha256:c782dfe175af659dbef2371903f4af0180af017bc4eb89ea45965a4f385f8b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44de953c67739aa87eb699753315560c3e5f898d721b253a78ee9b0bece90d32`

```dockerfile
```

-	Layers:
	-	`sha256:76d12f419243f487cfd1893ef954181ed8dbeaeb13f0ff1923e98d6f37cf3ad0`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 21.7 KB (21661 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0.0-alpine`

```console
$ docker pull varnish@sha256:a84e1d4adb58b1f0594efbc95b9854c37040aafbbb990fa4889d6520a2feea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:313c1e39011cd7ad60a797012574cf43ec9b3f652368766eb8f658134c798e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91772446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2dd9ec648dcf29eb5e73fb988e6337591e92a9cd3dc40566579e5dfc69a0b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:32:53 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:32:53 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:32:53 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:32:53 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:32:53 GMT
USER varnish
# Wed, 28 Jan 2026 18:32:53 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:32:53 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a023c28f50298fde5fdebfb9183a14c01add9e56dbd5e465fbb5f20091e66b26`  
		Last Modified: Wed, 28 Jan 2026 18:33:06 GMT  
		Size: 87.9 MB (87907492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43ab80124716fd6fd1dea26c10cb19d9956f00e9310f54b211bedf51903d0a8`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed37e8718e0c2f976041d5825a05251d01a2cccd7ea651e4faba3892a74a3c7`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3e6fd73e1c2d4af26c7e5621e4317be18bcfc94308e5b6beb6a72cd170854`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f5a6df222303ec11afdd7aba8e6ce117da6dca249c39fcb4c7bf80666ffa4e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e35f19446543c684a63b0d3e4df83aadc77b84dbd5ba27017204e16548e5cf`

```dockerfile
```

-	Layers:
	-	`sha256:2472b92b11950f0ccd3dac0294bf9c31e2174882ccbec33de210089fab5ec428`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 20.7 KB (20687 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:5012ddbf256e65054b99e3f27bae23f4973c3427d3e69882536053454ae033dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83538388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6858c7d69f1ef19e0c93fe2588a96b69e65e9c3918e563a55fbb19e09a0b33`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:45:55 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:45:55 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:45:55 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:45:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:45:55 GMT
USER varnish
# Wed, 28 Jan 2026 18:45:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da24d757c3e5486bd934e3ed2ab115041c3cd5eeca9bf88d5e0fe5e73f1c01bd`  
		Last Modified: Wed, 28 Jan 2026 18:46:07 GMT  
		Size: 79.3 MB (79338167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76a29fb6864bfa14adb7c64c7cd4a92ae6740e89da8dc5544e4032c5670f7d1`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ca8d9ee0017ec696497e5afaafe59a065eb02feac3a273c07d5ec27b56fd34`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d83ce2d813532284a2265d0ea39dfcbd5a65dc2b4b6c09af121ab8edd31c46b`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5cb09b7c875b608f6488d947d4fae3713abeb40a55f44b7ce5e011b5bdfb77cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c3dbcb1e49cbee0a8f8b985cb8f495cd814543ff07752a680cb0d5cb573948`

```dockerfile
```

-	Layers:
	-	`sha256:7b786c97ea1f2e5b349e6674dcdbee3e869393e0ba482f7be67c9bab7fd4be22`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:alpine`

```console
$ docker pull varnish@sha256:a84e1d4adb58b1f0594efbc95b9854c37040aafbbb990fa4889d6520a2feea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:alpine` - linux; amd64

```console
$ docker pull varnish@sha256:313c1e39011cd7ad60a797012574cf43ec9b3f652368766eb8f658134c798e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91772446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2dd9ec648dcf29eb5e73fb988e6337591e92a9cd3dc40566579e5dfc69a0b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:32:53 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:32:53 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:32:53 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:32:53 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:32:53 GMT
USER varnish
# Wed, 28 Jan 2026 18:32:53 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:32:53 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a023c28f50298fde5fdebfb9183a14c01add9e56dbd5e465fbb5f20091e66b26`  
		Last Modified: Wed, 28 Jan 2026 18:33:06 GMT  
		Size: 87.9 MB (87907492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43ab80124716fd6fd1dea26c10cb19d9956f00e9310f54b211bedf51903d0a8`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed37e8718e0c2f976041d5825a05251d01a2cccd7ea651e4faba3892a74a3c7`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3e6fd73e1c2d4af26c7e5621e4317be18bcfc94308e5b6beb6a72cd170854`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f5a6df222303ec11afdd7aba8e6ce117da6dca249c39fcb4c7bf80666ffa4e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e35f19446543c684a63b0d3e4df83aadc77b84dbd5ba27017204e16548e5cf`

```dockerfile
```

-	Layers:
	-	`sha256:2472b92b11950f0ccd3dac0294bf9c31e2174882ccbec33de210089fab5ec428`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 20.7 KB (20687 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:5012ddbf256e65054b99e3f27bae23f4973c3427d3e69882536053454ae033dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83538388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6858c7d69f1ef19e0c93fe2588a96b69e65e9c3918e563a55fbb19e09a0b33`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:45:55 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:45:55 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:45:55 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:45:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:45:55 GMT
USER varnish
# Wed, 28 Jan 2026 18:45:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da24d757c3e5486bd934e3ed2ab115041c3cd5eeca9bf88d5e0fe5e73f1c01bd`  
		Last Modified: Wed, 28 Jan 2026 18:46:07 GMT  
		Size: 79.3 MB (79338167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76a29fb6864bfa14adb7c64c7cd4a92ae6740e89da8dc5544e4032c5670f7d1`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ca8d9ee0017ec696497e5afaafe59a065eb02feac3a273c07d5ec27b56fd34`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d83ce2d813532284a2265d0ea39dfcbd5a65dc2b4b6c09af121ab8edd31c46b`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5cb09b7c875b608f6488d947d4fae3713abeb40a55f44b7ce5e011b5bdfb77cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c3dbcb1e49cbee0a8f8b985cb8f495cd814543ff07752a680cb0d5cb573948`

```dockerfile
```

-	Layers:
	-	`sha256:7b786c97ea1f2e5b349e6674dcdbee3e869393e0ba482f7be67c9bab7fd4be22`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh`

```console
$ docker pull varnish@sha256:226a23129ecf7c69d670e409fc8be49d1c1bfc2fad8557f66f62dd8dbdcc3fe1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:d352c9681d9a8ba5e56689cafcdeaf13be9b4f3eb50702e8cdf60aa2462e8211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121962336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d60cea63dbf0bfb59e087cd0da723866bb4b226c32f3e2bde8235fed975db9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:21 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 03 Feb 2026 02:42:21 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-4
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 03 Feb 2026 02:42:21 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 02:42:21 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.0-4 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         if [ "$(dpkg --print-architecture)" = "amd64" ]; then         EXTRA_VMODS="vmod-cfg=${VARNISH_VERSION}";     else         EXTRA_VMODS= ;     fi;     apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				${EXTRA_VMODS} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:42:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:42:21 GMT
USER varnish
# Tue, 03 Feb 2026 02:42:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:42:21 GMT
CMD []
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96ce5385998e16a6fb7ef0226d1f20b45298bed9dc060e1bf28d50b55ab6b44`  
		Last Modified: Tue, 03 Feb 2026 02:42:36 GMT  
		Size: 92.2 MB (92180627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d975aae4b8d991a67a2469a23763d6acfdf59ac627560c2f790c080c24018d71`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850971c09b6d0682278837f5c6a4e9d01b30dccf52df0692fdf7a668c729420a`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f107400f6a38a9314a93b12c9392f94b30b5f795125cf51885a1dbe8c0c49a`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:362009b8c48f6e6c1df889fed612bea5e9606c328aa1844be7840919bae04d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 KB (21545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6e6c2c755a94af44f9b0afc723c139b2357ebdcd63288ebae6773749f97cdf`

```dockerfile
```

-	Layers:
	-	`sha256:d5d34eb7eddcf079b45cf5c06eebd4f2d4f2e58f53d5cd95788bbd42eb37fb80`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 21.5 KB (21545 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:cf120eda11e2042d4d3b042a843ba90d71839f7ea5da41b44631b161444b5138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114675943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12599516796d11291cda900c5d30ad79d4ffb66b35e6a2cdb49dac94423d3a43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:45:15 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 03 Feb 2026 02:45:15 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-4
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 03 Feb 2026 02:45:15 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 02:45:15 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.0-4 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         if [ "$(dpkg --print-architecture)" = "amd64" ]; then         EXTRA_VMODS="vmod-cfg=${VARNISH_VERSION}";     else         EXTRA_VMODS= ;     fi;     apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				${EXTRA_VMODS} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:45:15 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:45:15 GMT
USER varnish
# Tue, 03 Feb 2026 02:45:15 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:45:15 GMT
CMD []
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bd55ca0600e6a3e876c49088103397b7b05e6094487e7a60107919cd3051bd`  
		Last Modified: Tue, 03 Feb 2026 02:45:29 GMT  
		Size: 84.5 MB (84532762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66978ff33f084ea694488f026f19a130f485eb75eb669ee030fb8248faef72af`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad63af1ab6603e791221ce68a695341b32ed14e8a5be37150f8c6a65a50df61`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c278d8bcf8a98fe62140fe7ddf9d61e65feef87d547df1c78ea939529cf33bb3`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:c782dfe175af659dbef2371903f4af0180af017bc4eb89ea45965a4f385f8b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44de953c67739aa87eb699753315560c3e5f898d721b253a78ee9b0bece90d32`

```dockerfile
```

-	Layers:
	-	`sha256:76d12f419243f487cfd1893ef954181ed8dbeaeb13f0ff1923e98d6f37cf3ad0`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 21.7 KB (21661 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:a84e1d4adb58b1f0594efbc95b9854c37040aafbbb990fa4889d6520a2feea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:fresh-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:313c1e39011cd7ad60a797012574cf43ec9b3f652368766eb8f658134c798e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91772446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2dd9ec648dcf29eb5e73fb988e6337591e92a9cd3dc40566579e5dfc69a0b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:32:53 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:32:53 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:32:53 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:32:53 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:32:53 GMT
USER varnish
# Wed, 28 Jan 2026 18:32:53 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:32:53 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a023c28f50298fde5fdebfb9183a14c01add9e56dbd5e465fbb5f20091e66b26`  
		Last Modified: Wed, 28 Jan 2026 18:33:06 GMT  
		Size: 87.9 MB (87907492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43ab80124716fd6fd1dea26c10cb19d9956f00e9310f54b211bedf51903d0a8`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed37e8718e0c2f976041d5825a05251d01a2cccd7ea651e4faba3892a74a3c7`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3e6fd73e1c2d4af26c7e5621e4317be18bcfc94308e5b6beb6a72cd170854`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f5a6df222303ec11afdd7aba8e6ce117da6dca249c39fcb4c7bf80666ffa4e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e35f19446543c684a63b0d3e4df83aadc77b84dbd5ba27017204e16548e5cf`

```dockerfile
```

-	Layers:
	-	`sha256:2472b92b11950f0ccd3dac0294bf9c31e2174882ccbec33de210089fab5ec428`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 20.7 KB (20687 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:5012ddbf256e65054b99e3f27bae23f4973c3427d3e69882536053454ae033dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83538388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6858c7d69f1ef19e0c93fe2588a96b69e65e9c3918e563a55fbb19e09a0b33`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:45:55 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:45:55 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:45:55 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:45:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:45:55 GMT
USER varnish
# Wed, 28 Jan 2026 18:45:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da24d757c3e5486bd934e3ed2ab115041c3cd5eeca9bf88d5e0fe5e73f1c01bd`  
		Last Modified: Wed, 28 Jan 2026 18:46:07 GMT  
		Size: 79.3 MB (79338167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76a29fb6864bfa14adb7c64c7cd4a92ae6740e89da8dc5544e4032c5670f7d1`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ca8d9ee0017ec696497e5afaafe59a065eb02feac3a273c07d5ec27b56fd34`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d83ce2d813532284a2265d0ea39dfcbd5a65dc2b4b6c09af121ab8edd31c46b`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5cb09b7c875b608f6488d947d4fae3713abeb40a55f44b7ce5e011b5bdfb77cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c3dbcb1e49cbee0a8f8b985cb8f495cd814543ff07752a680cb0d5cb573948`

```dockerfile
```

-	Layers:
	-	`sha256:7b786c97ea1f2e5b349e6674dcdbee3e869393e0ba482f7be67c9bab7fd4be22`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:latest`

```console
$ docker pull varnish@sha256:226a23129ecf7c69d670e409fc8be49d1c1bfc2fad8557f66f62dd8dbdcc3fe1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:d352c9681d9a8ba5e56689cafcdeaf13be9b4f3eb50702e8cdf60aa2462e8211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121962336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d60cea63dbf0bfb59e087cd0da723866bb4b226c32f3e2bde8235fed975db9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:21 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 03 Feb 2026 02:42:21 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-4
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 03 Feb 2026 02:42:21 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 02:42:21 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.0-4 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         if [ "$(dpkg --print-architecture)" = "amd64" ]; then         EXTRA_VMODS="vmod-cfg=${VARNISH_VERSION}";     else         EXTRA_VMODS= ;     fi;     apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				${EXTRA_VMODS} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:42:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:42:21 GMT
USER varnish
# Tue, 03 Feb 2026 02:42:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:42:21 GMT
CMD []
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96ce5385998e16a6fb7ef0226d1f20b45298bed9dc060e1bf28d50b55ab6b44`  
		Last Modified: Tue, 03 Feb 2026 02:42:36 GMT  
		Size: 92.2 MB (92180627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d975aae4b8d991a67a2469a23763d6acfdf59ac627560c2f790c080c24018d71`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850971c09b6d0682278837f5c6a4e9d01b30dccf52df0692fdf7a668c729420a`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f107400f6a38a9314a93b12c9392f94b30b5f795125cf51885a1dbe8c0c49a`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:362009b8c48f6e6c1df889fed612bea5e9606c328aa1844be7840919bae04d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 KB (21545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6e6c2c755a94af44f9b0afc723c139b2357ebdcd63288ebae6773749f97cdf`

```dockerfile
```

-	Layers:
	-	`sha256:d5d34eb7eddcf079b45cf5c06eebd4f2d4f2e58f53d5cd95788bbd42eb37fb80`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 21.5 KB (21545 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:cf120eda11e2042d4d3b042a843ba90d71839f7ea5da41b44631b161444b5138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114675943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12599516796d11291cda900c5d30ad79d4ffb66b35e6a2cdb49dac94423d3a43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:45:15 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 03 Feb 2026 02:45:15 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-4
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 03 Feb 2026 02:45:15 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 02:45:15 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.0-4 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         if [ "$(dpkg --print-architecture)" = "amd64" ]; then         EXTRA_VMODS="vmod-cfg=${VARNISH_VERSION}";     else         EXTRA_VMODS= ;     fi;     apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				${EXTRA_VMODS} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:45:15 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:45:15 GMT
USER varnish
# Tue, 03 Feb 2026 02:45:15 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:45:15 GMT
CMD []
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bd55ca0600e6a3e876c49088103397b7b05e6094487e7a60107919cd3051bd`  
		Last Modified: Tue, 03 Feb 2026 02:45:29 GMT  
		Size: 84.5 MB (84532762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66978ff33f084ea694488f026f19a130f485eb75eb669ee030fb8248faef72af`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad63af1ab6603e791221ce68a695341b32ed14e8a5be37150f8c6a65a50df61`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c278d8bcf8a98fe62140fe7ddf9d61e65feef87d547df1c78ea939529cf33bb3`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:c782dfe175af659dbef2371903f4af0180af017bc4eb89ea45965a4f385f8b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44de953c67739aa87eb699753315560c3e5f898d721b253a78ee9b0bece90d32`

```dockerfile
```

-	Layers:
	-	`sha256:76d12f419243f487cfd1893ef954181ed8dbeaeb13f0ff1923e98d6f37cf3ad0`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 21.7 KB (21661 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old`

```console
$ docker pull varnish@sha256:fbcfe0d9eecf40eb5a16381d7605237f4d6e7188b99d556f503923e2eb4e2155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:88bced2b343bab9b233dff35c42eb529e4e982a017e3624aa524151c4f3c5ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116346186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb0514cc7fb6bd6c70385fa61c4ddd976f3428283882296246734e07d1fc2c4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:47:07 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 03 Feb 2026 03:47:07 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 03 Feb 2026 03:47:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 03 Feb 2026 03:47:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 03 Feb 2026 03:47:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 03 Feb 2026 03:47:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 03:47:07 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 03:47:07 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 03:47:07 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 03:47:07 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:47:07 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 03:47:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 03:47:07 GMT
USER varnish
# Tue, 03 Feb 2026 03:47:07 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 03:47:07 GMT
CMD []
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78d5cb1bba1feacb6362d4014b338d3e9c025e5028144a2005ee8929a5127c2`  
		Last Modified: Tue, 03 Feb 2026 03:47:22 GMT  
		Size: 86.6 MB (86565545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73003d45cacff21c1022a462a7cb84f58eb827b7fd5700aa489f8e4eda8fe3ca`  
		Last Modified: Tue, 03 Feb 2026 03:47:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222ebdf0dda00e72527e9458a718979edaf63cec3413338d2b8b2084f310e64d`  
		Last Modified: Tue, 03 Feb 2026 03:47:19 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:f2794fd830479d9cd6cd7e3bb2d3378558618386e5407eaf115f38aacde2ff0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4349af5775296e1a8561e2dd9e8c10df40a4e2bff82de672cf08ebdca8c7ba`

```dockerfile
```

-	Layers:
	-	`sha256:aad51e36ff0df4b53cf9ac4ad53f25f3ff02382bea98e6eab560caff9307a41a`  
		Last Modified: Tue, 03 Feb 2026 03:47:19 GMT  
		Size: 19.1 KB (19053 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8aaaa04e878ae972934d9be59b6572128e5582dc248173ca484de4dcc476797d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110527705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96367711e92e07d47a4f94f00f6f9412e44745900894f5a5f8abdacee5e52d16`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:28 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 03 Feb 2026 02:46:28 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 03 Feb 2026 02:46:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 03 Feb 2026 02:46:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 03 Feb 2026 02:46:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 03 Feb 2026 02:46:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:46:28 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 02:46:28 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 02:46:29 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:46:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:46:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:46:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:46:29 GMT
USER varnish
# Tue, 03 Feb 2026 02:46:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:46:29 GMT
CMD []
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc96d349d263ff12e47f8954a315c622c6884059baa940d9459de0f365a989b`  
		Last Modified: Tue, 03 Feb 2026 02:46:41 GMT  
		Size: 80.4 MB (80385593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfceea4e1c6f838873a5ec8d3723a7db7dcbdfaab3d32ff6355c7acb562c196`  
		Last Modified: Tue, 03 Feb 2026 02:46:39 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1ff5558ad5eca044452183365b8668a746f335ea6215af14fe6aedb2f8a34b`  
		Last Modified: Tue, 03 Feb 2026 02:46:39 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:5821f3408fb4a85ebc4fa033459d119f01b6d2603af27971c7faba368c7ee923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2113d13c12567f525dacd6b8996978ebea79ce7205da225db606c24f342d0a7`

```dockerfile
```

-	Layers:
	-	`sha256:d1debaf1ed2c15b3234a6b5e5924c1d8c0cf094b882a64d5b588a7be88ac7a0c`  
		Last Modified: Tue, 03 Feb 2026 02:46:39 GMT  
		Size: 19.1 KB (19144 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:95deada23d0ef0cd1005cfe32463f3390f31a63f13682996bccdb5b01ea7f291
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:8aa05c32b87720c21201f23664c14e58218e6a8bf2d240192d61ddf7cbda1543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80549045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4b3a4a43c039fde71b875c7d203b302d8f539cf7d6ea66bd68203662cfd84c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:08 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_VERSION=7.7.3
# Wed, 28 Jan 2026 02:40:08 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Wed, 28 Jan 2026 02:40:08 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 02:40:08 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 02:40:08 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 02:40:08 GMT
USER varnish
# Wed, 28 Jan 2026 02:40:08 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 02:40:08 GMT
CMD []
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a04f2c14282af7f7e529680683c4281801fe0d25060b1f1849b5b10ce75207`  
		Last Modified: Wed, 28 Jan 2026 02:40:21 GMT  
		Size: 76.7 MB (76742117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431ff28a6f82e4f8ababee51c3cba66677a5d436c027f202cff74cdfaa22b2fa`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e3640c70635b2fb032b6853f07c74fea52315c1157b90d728b171a25b855a6`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:fdbfb5b2598b29dc6fcc4576ff7054763636eb08b994d768f3b662e46af7cada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70f4eca00c39ae1979c06ee1adef5eba46dbea1c6b4bb8dddc0c9da233cf6a7`

```dockerfile
```

-	Layers:
	-	`sha256:af700eba3659b121f6e7f4f91bec07eb72c5b17f00d6e85559d34eae8c6939a5`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 18.8 KB (18840 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e08f69115921e2084edfdc49c70244ca6e2c2830f7cd882ce3fc68302320e795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77534209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68875f332b81c8a9f0b8157adf6aca453c9ce66478997f3899c83048bee86613`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:14 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_VERSION=7.7.3
# Wed, 28 Jan 2026 02:40:14 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Wed, 28 Jan 2026 02:40:14 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 02:40:14 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 02:40:14 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 02:40:14 GMT
USER varnish
# Wed, 28 Jan 2026 02:40:14 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 02:40:14 GMT
CMD []
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf710ef050705257a3b1ccc4556cc95fed48da6153f9dee22ff258bd3f4a2704`  
		Last Modified: Wed, 28 Jan 2026 02:40:27 GMT  
		Size: 73.4 MB (73392634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed23c78500b776f154686015e0536a78e6cbcf306c95ed7a6dab1769067fbaa5`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9086e9e0255e2a3935f436f74da42da55a0fa0de25ce1aaee7c10dfba1a1882b`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:b3342940e958392acaafe6dc63153ff912a0c9ef8b4d773520b8d0e57c4f8910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d64f6ef49b079355c29686ebba4c3599233207673cca81322e56af6cf83e9fb`

```dockerfile
```

-	Layers:
	-	`sha256:14078e9f50c83d2b5b9d2201394b09e185e22d9f12db3c8385b168e27f1b5679`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 18.9 KB (18933 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:stable`

```console
$ docker pull varnish@sha256:1ab688fc4ebddba39ef6a74e99216684e746eff0652450de0735b6bd65440a30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:ab873f9d6297aaf704e15c51082019a134f631eb3b1ce2a6667ce9776efff91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103549435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508454c11eef459eec1b24838fa146a92adf53177227c945433a94468dc8ef44`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:00 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 03 Feb 2026 02:43:00 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 03 Feb 2026 02:43:00 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 03 Feb 2026 02:43:00 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:43:00 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 03 Feb 2026 02:43:00 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:43:00 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:43:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:43:00 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:43:00 GMT
CMD []
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50561126bf2cc22facca3f7e3ae51518979813418f5824a39315a68d373f3530`  
		Last Modified: Tue, 03 Feb 2026 02:43:13 GMT  
		Size: 75.3 MB (75320192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab38f1120f1568d0b995b108553d91294c0a2538896178541b022b92de4aa82`  
		Last Modified: Tue, 03 Feb 2026 02:43:10 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:2fb567482b26431d7cab1dea2bf8da1dfb603459c5191ec50f1ab027bfbfe6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a173684a3089cd0110283ed9a05ff14f4d3edbe4c3c773cca369c84113fb766`

```dockerfile
```

-	Layers:
	-	`sha256:b4be3cd8fb2c42686018dad38803faae9885b789a83d4280fda0be7baf5c2f09`  
		Last Modified: Tue, 03 Feb 2026 02:43:10 GMT  
		Size: 12.7 KB (12656 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7a6c8173f7aa5404e58ed29e4745bceb42846de891b7e618f23f57bc28572be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98409279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59626750601c1f20862e364508d4d8fc3fa142ff758288f26a51d4106297436`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:45:58 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 03 Feb 2026 02:45:58 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 03 Feb 2026 02:45:58 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 03 Feb 2026 02:45:58 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:45:58 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 03 Feb 2026 02:45:58 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:45:58 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:45:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:45:58 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:45:58 GMT
CMD []
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0f6557bfcc6f23ce7e667a0ce3c4c4192c63b3bf041e192ec03f7f5bb4d2dc`  
		Last Modified: Tue, 03 Feb 2026 02:46:10 GMT  
		Size: 70.3 MB (70300699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8ba01b6da17f8bec0293d3ce5cb5d987d71179980075c132bf8d1ef9db4290`  
		Last Modified: Tue, 03 Feb 2026 02:46:08 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:410f1c52f38ce61afeebfde3cd901ba6f37bc179c6f2931d4853512e50e652e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38856403b71349f8a9f6565a7c08213d684010a327fb87fa2f2ef6cc564a715`

```dockerfile
```

-	Layers:
	-	`sha256:a12c2993cd26360dd6a72b78b348c569b69edb05fdc680e97a2faada87050704`  
		Last Modified: Tue, 03 Feb 2026 02:46:08 GMT  
		Size: 12.7 KB (12749 bytes)  
		MIME: application/vnd.in-toto+json
