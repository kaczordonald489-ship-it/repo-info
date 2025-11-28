<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `irssi`

-	[`irssi:1`](#irssi1)
-	[`irssi:1-alpine`](#irssi1-alpine)
-	[`irssi:1-alpine3.22`](#irssi1-alpine322)
-	[`irssi:1-trixie`](#irssi1-trixie)
-	[`irssi:1.4`](#irssi14)
-	[`irssi:1.4-alpine`](#irssi14-alpine)
-	[`irssi:1.4-alpine3.22`](#irssi14-alpine322)
-	[`irssi:1.4-trixie`](#irssi14-trixie)
-	[`irssi:1.4.5`](#irssi145)
-	[`irssi:1.4.5-alpine`](#irssi145-alpine)
-	[`irssi:1.4.5-alpine3.22`](#irssi145-alpine322)
-	[`irssi:1.4.5-trixie`](#irssi145-trixie)
-	[`irssi:alpine`](#irssialpine)
-	[`irssi:alpine3.22`](#irssialpine322)
-	[`irssi:latest`](#irssilatest)
-	[`irssi:trixie`](#irssitrixie)

## `irssi:1`

```console
$ docker pull irssi@sha256:f16b9ab6967270a5b2d0745b7f6b9233f6226b9866de8e46ab3f67f20167dde3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1` - linux; amd64

```console
$ docker pull irssi@sha256:1c3ad0c692729985069dc605f6970c498536ff77cdc28731957a9981bb5cc69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8b5071dd14f9cc7babdbbb92be355488770afbb4baa1dd4193f835544e54d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:18:09 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 04:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 04:18:46 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 04:18:46 GMT
USER user
# Tue, 18 Nov 2025 04:18:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3defe69b9d42ee331ee4997997e0b6950a228ac42a28acb744b2a217802984`  
		Last Modified: Tue, 18 Nov 2025 04:19:08 GMT  
		Size: 19.2 MB (19222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d261d2d2be0daf5812e199043e646cd3b38c72c6a85a46d1aa2664afbbfdab`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb0ce4ebcc67d4eb7b0fd5a6f142adedb46b4a4b5c9f752bb3663092160fd4`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 4.9 MB (4866605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:22bdb7c49ddfaba85497f04c9d268938716f3b3352fe24378d933a7732e8d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d4070dfa4342b3ae917c1f765452b8b31cbfe6c04864d806db24d761ba3c65`

```dockerfile
```

-	Layers:
	-	`sha256:5234daf2a71968c25322c71bfea4cdc75082624fc15fcfa85f68596c0e1e8722`  
		Last Modified: Tue, 18 Nov 2025 06:01:31 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6a5104b772e5ddb76df8ed09e14d2aaf8f4757fd03c65a00ce68904337b081`  
		Last Modified: Tue, 18 Nov 2025 06:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3bfeabfea3f173a6eef66224244f7c8ab79162e4b3e3454b5d7b951b699e6d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce561de65d9ced729b270243f33a9fe650e7088512ea128954c48a408518f61`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:22:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:23:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:23:21 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:23:21 GMT
USER user
# Tue, 18 Nov 2025 02:23:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e77346f90948edf43f33edec1b3c918cc8196b58e71fc74d47eb901d26a7c88`  
		Last Modified: Tue, 18 Nov 2025 02:23:39 GMT  
		Size: 18.3 MB (18286955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20fff4d4c2bb97e0fc743edd41339f9e7f2db5706f958f8419de0227c19fa9`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deede23e33150dccc8ce32f23f864d2a100697bb5c3f5f0d51414ec4913c97f`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 4.7 MB (4709653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:92486d0301f23f7f5fef04e23a1038f9c9c424a3a47ade435591fdd52853f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1456fb2be5b0b7cdc491b833efa2a0ceb4796c5c761a82e6ef643577401e6`

```dockerfile
```

-	Layers:
	-	`sha256:6273392ed72e310ca2593fd6731c533c6f636ed1289f29f728e45fc25e8d45b3`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c338421356fba9d226382ee2864822813fdd13c90654bd98562c53392aa9884f`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6206945589cb5f70880eb627ea43ce5e83dc6b09e69ad976fc69ec0a8a671e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e2dfadf9b6f72f29f6e28ff5885e16008ea991da97c386c12c6effd41ef773`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:24:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:24:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:24:41 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:24:41 GMT
USER user
# Tue, 18 Nov 2025 02:24:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07012b32f4cdf9145076ab6689e96bf750c40d6358ddc6b3d983ed86522093b2`  
		Last Modified: Tue, 18 Nov 2025 02:25:00 GMT  
		Size: 17.9 MB (17909541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317eec7c88d4aa0563b4acdfa018d18e2244d1cd4faaa808233aad6ed8c4eef`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e397c097f4a4f9d07fc0ad13a259eb1c5dc9952ad435619e84f81acd7aa5a`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 4.6 MB (4558582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:2807406dbaf53bd4128387747c9380192177098c869b02c4fbc0e079734b4a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912225e9dca4300bbd0be1c71db46f637c20bb0ae39dd56905152d9fd37712e7`

```dockerfile
```

-	Layers:
	-	`sha256:826b1dd7affc3defc30e532bafe21b81af9274fe59f9cb13bc8880b266566410`  
		Last Modified: Tue, 18 Nov 2025 06:01:49 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caba9a457c37510c70d5629f0b91ebfec1b4e1fddabcf69e4581cc62b8efbdf9`  
		Last Modified: Tue, 18 Nov 2025 06:01:51 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0ca154f240d8e55d9139562ed162f6d09ed917369e5d3ac0ef11f4277868a144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494da41086e91ed2e2a5b5a81ed84f81af0313ded1a6a19ca4935a9ed697e260`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:19:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:20:13 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:20:13 GMT
USER user
# Tue, 18 Nov 2025 02:20:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619a9a2c5679b92c7e4905e08f05810e02f68d89d06b10524e21d2583f4ab16`  
		Last Modified: Tue, 18 Nov 2025 02:20:32 GMT  
		Size: 19.0 MB (19049113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494e61b822c7885405295c0e02e3d6f750e57594294fe2d8b997a0632065745d`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84635b25a37fcbf6ec3700e051e040f70178ad0e6880c9c76aeef1ebcfdf275`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 4.8 MB (4781743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:6b955f8723ba03a2a30061c1a89c6af489d1442317213524c5594663f9d28695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b845fa96792ab508c1cabce079cc6822b4d3ed51f4ff9cc1486fb4becdb2b9`

```dockerfile
```

-	Layers:
	-	`sha256:1e1288c631711328c43fbd795987044f9c19d6d7ca488586f7d48b2d1bbf9fc9`  
		Last Modified: Tue, 18 Nov 2025 06:01:56 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3627aff8962b25f0eb1a595d760c047d53573e5a83de81ffd5ee43ffde3e283f`  
		Last Modified: Tue, 18 Nov 2025 06:01:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:9ca8e0716038e4dbc489c402c36d6bdc49bb1c6dc80a6050371e0ebb63798b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afefadafe5f8e789fb22f477834b8855758beefa989deb19c7f4e79699e5e89`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:17:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:17:16 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:17:16 GMT
USER user
# Tue, 18 Nov 2025 02:17:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2fb43e1b281a402bf774cd8bde6070d229add5d03c870cbfe7c8e16f2cbb7`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 18.7 MB (18740862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6997edee7df4e50b70fa845f324ec76992912dec560143cbead27a7aec43803b`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a3e4cae20c6dc7e982f2a19aa8de8e2b641b6bcc81e72f1bef2930dca363d`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 4.9 MB (4868298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:59d4050c0c1cd29128be910eccf5ea2a035052b836f46e045244c9f64fa4298c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1003b498f9e79e27d0402d3e70dfc68a8d4f2e5fb76327ddf0d269848f164933`

```dockerfile
```

-	Layers:
	-	`sha256:dae334eb70cbeb2210f0f00af9826de6e0af19a4045d45c351ccd063c967c44c`  
		Last Modified: Tue, 18 Nov 2025 06:02:04 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f17fc2c6b6001ffa3a573775d2cbcfc57f6836267cf4f7578260842ada1b7`  
		Last Modified: Tue, 18 Nov 2025 06:02:05 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:459fe708abbb929ace6e5502ac492cb132f84c0e1b80e5a3dd662a7d98b6470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72533238806364f21d117ef1051d9f72e86e6063d9c6683bc210cea47127bda`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 15:03:14 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 15:03:14 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 15:04:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 15:04:50 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 15:04:50 GMT
USER user
# Tue, 18 Nov 2025 15:04:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f858dd24ce7b2766334f11cb720c162ec10dcc1115c24b7c5a2cb933f4732e`  
		Last Modified: Tue, 18 Nov 2025 15:05:24 GMT  
		Size: 19.5 MB (19542803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e87e68a0f54b41f554a220560c01fae4bca1b4bb4b83336d6c6110f750186`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab575b18effe508097b5d8936201a72cd903f95c5c055af70a652fee9591f15f`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 5.1 MB (5097211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:43823b3c76d194b48bf19fd79dde879a47f65352dc638bc93f743de8b5863b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b0fd9dbba87f1d0495d3f376c23a11766edc9e180c9c6afddfacb7df1cbe76`

```dockerfile
```

-	Layers:
	-	`sha256:ebbbdb938672f1b98a9abf9c0267764349f2261c7295ea777971571c28ac293f`  
		Last Modified: Tue, 18 Nov 2025 18:00:17 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae083b6d0624ff996d976b7dfead8f215b20de9aedc3bef84697341f367a4d3`  
		Last Modified: Tue, 18 Nov 2025 18:00:18 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; riscv64

```console
$ docker pull irssi@sha256:0a17bc9dc7f1ede0aae4d4035aa269c39fdd3ad059158a3c6a569fa2bf7da8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6a1bc4c5ae216cf035ec48b010768259be2a066ee4ef066bcb9c32d445e4d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 10:01:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:01:44 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 10:08:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 10:08:36 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 10:08:36 GMT
USER user
# Tue, 18 Nov 2025 10:08:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afef2a7493fa326b06e464e36f2a79568e4c5c265515366e193165f0b4d284e`  
		Last Modified: Tue, 18 Nov 2025 10:10:42 GMT  
		Size: 18.5 MB (18549074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026bbe28877d1917f647dacffd37172e95435e1c7e9fbe30a62986bb72cd62b`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 3.3 KB (3337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3d248f54be38451080b4d25093d9df5c1c9efe1175c3cf58494a7e0fd7fe62`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 4.9 MB (4860627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:7b01cdd2258dc9fd9266a05e6cbd264f72886699285f27da4dcfa624dcb82f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb4ae2e3561846a1f14e41a61390911210a0c9ea6b4f9bace7ef57ca7a1303`

```dockerfile
```

-	Layers:
	-	`sha256:5044523627d968ee0b87912ad5e86b6f374ff85ef9a7878ae77c52dcf5581421`  
		Last Modified: Tue, 18 Nov 2025 18:00:24 GMT  
		Size: 5.6 MB (5579680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43863609ed306f6a1f2ac385d2c41ef9efb115640066a4bb3b02043bb96f7158`  
		Last Modified: Tue, 18 Nov 2025 18:00:25 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:da93e9283b14d1092e451a797eb231f916c62509d64042a7ed65617b6ab9c487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b5c6cf33fd166afa65862c57464a7a99d44516a592d7093c9c71058d5008c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:17:58 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:18:33 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:18:33 GMT
USER user
# Tue, 18 Nov 2025 02:18:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce4907214a18511e7c1676f0b93794fa538b6672045daa187e1c681bbd9019`  
		Last Modified: Tue, 18 Nov 2025 02:18:55 GMT  
		Size: 19.8 MB (19759415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dca431fe704652eca13f122842a6232de3a88619e75b4585c55d73ab6784b33`  
		Last Modified: Tue, 18 Nov 2025 02:18:52 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12fa892c886e7110c8b36d26e5b06c87bdfad4dab6e9bf9b746c2887bce206f`  
		Last Modified: Tue, 18 Nov 2025 02:18:53 GMT  
		Size: 4.9 MB (4905870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:9921bed642cdddc5b883e960fbb4efa54a43817af46e8c05c8c59611062a6056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babbc467c5248e09f8d3d0710512a06a92fbd5173a81414b551f82cab3d5d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:a1fee033f27a53ca8a99d5789a2cf1a16782bef7f265384856e2f9c62104fc55`  
		Last Modified: Tue, 18 Nov 2025 06:02:18 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd54ab02d147f06764006021d0881cd166981d03206bbcbfdca3215249d036e1`  
		Last Modified: Tue, 18 Nov 2025 06:02:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:1e663ae10149c0b4d9df663b9da7bb650a58deea6cb49343c8191884eb0ec8ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1-alpine` - linux; amd64

```console
$ docker pull irssi@sha256:faf9e4f6be7260cc0682ec1445c6826e0bdcdc63f4a064eb8a981701bb709594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8798df3f4b34c7e6f52a3727072b2c410704453c6794f69663ce299680c47d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e11827177f1c189b726b09341a9159227f1bfd85f6bfa5e738af089ccd47cc`  
		Last Modified: Wed, 08 Oct 2025 22:39:07 GMT  
		Size: 10.4 MB (10396003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6644b44e4c465f7087dbb97380180e75f01380c552303d8a2486f385aad34f35`  
		Last Modified: Wed, 08 Oct 2025 22:39:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b031546d04685e49a4d43b8482a34aaa0e6a3a6d75e947a09671aaf238e1ffc`  
		Last Modified: Wed, 08 Oct 2025 22:39:05 GMT  
		Size: 6.0 MB (5973981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:60dc002a8263e274525a471186038e9a631be6a5c61c1fd9e0ec2accade632f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be809ef2f20f547ecb812fc7251645454e581cc3d872627c003659069a74285e`

```dockerfile
```

-	Layers:
	-	`sha256:7def044fb5b5a27bb8a83fe2e1f6903b88c7090d91d03cc25c2be92d2b115084`  
		Last Modified: Thu, 09 Oct 2025 01:59:25 GMT  
		Size: 1.3 MB (1270668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d745c2ae7ce01c7631e58d7cf581615e9c45ca2b8d31cccaa988c9e5257205`  
		Last Modified: Thu, 09 Oct 2025 01:59:26 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:8dfb08ad7779ab00246287f396771e855c5271e8e67f8fcb68229714505701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4ac8e569bab3223b4cbc8f2ffb5137d951b2efa8fbca448cdef1d3e4925de`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b352b3151cd505887f05e68a9791f679acceebf79736c8050c72db1b5191a`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 9.6 MB (9619615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8386f23106fb9eeab59f6f1e82d6fda32cd5130f7e9240952ab361424133835`  
		Last Modified: Wed, 08 Oct 2025 21:42:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5176e22c73a447407c118250d8b7084c947461ad88e0f8ffba848633ef457d1`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 5.8 MB (5802239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3529f2221a487a696afdfab5dd8793069c4e5153fdd0bbc77b1a10ed59976e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402305c7b183a88a4427e0caf1314f408323bb659aab78e52073f5d4946a814`

```dockerfile
```

-	Layers:
	-	`sha256:40cb74de7dde3071930d2507974b11b96e2a2fcf0dd4cc4063ea7658469d44d0`  
		Last Modified: Wed, 08 Oct 2025 22:59:36 GMT  
		Size: 17.5 KB (17462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1c77198ac74e17d59093ac465b9d5cb18f5cf9b495d394dc7fe1757c6cd43c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18234853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e381f20e12f748a613e6b9d046d4f23726de50b2d6209ee706e26cdc81cd9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355e9f8d23dd7df754d0fc9b69cb593d77843421e4fdc90e0999ac63d910671`  
		Last Modified: Wed, 08 Oct 2025 21:42:22 GMT  
		Size: 9.4 MB (9449582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d327d03f3716120871e15d8a53213e2201fb4c543cff4cfda89d44a362924f5b`  
		Last Modified: Wed, 08 Oct 2025 21:42:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7bac72cbbe13e0d2ca93a7e2045c3cee7af4a9a99e4f4a137d438a669963e`  
		Last Modified: Wed, 08 Oct 2025 21:42:21 GMT  
		Size: 5.6 MB (5562729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:a538097b3d9e95fd66c681e163119ee4fda34648e1138be1471be07765e086b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1291403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd05d16ceb8c11139b6c2e140bdd3f2ff4d48d4eeae0c78b36653e7f2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:66532285c363d95627518c5ee59b11b1d8179d0e9a5459c633c0d02618fed06d`  
		Last Modified: Wed, 08 Oct 2025 22:59:39 GMT  
		Size: 1.3 MB (1273726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f81d5bd314d48e57ad6439aa665accb301d8fa90cf9cfbc734e80cc3932d07`  
		Last Modified: Wed, 08 Oct 2025 22:59:40 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6312b888a6893a7c5bcbfa3b983ab38749f99778b44a99530ef47a5fa8afe92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6748a647916da83e7b32a7fc1af7248d48c18b28e2c35d2403a1aeaba48783`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d53dd86b6f70255a46f81ded3715200f2293ef56b5b5e4a9bd208fe73a5a4`  
		Last Modified: Wed, 08 Oct 2025 21:28:34 GMT  
		Size: 10.4 MB (10358145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35b8acbeb2e8727c286447b6769cf3d016bb4864c5ad35e2e295e2f173749a`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb455678cd1949819acffee4a71aa2ae7f91c1aae58a696c6666455cd9924e53`  
		Last Modified: Wed, 08 Oct 2025 21:28:35 GMT  
		Size: 5.8 MB (5847748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:816e238d7fee6ac073eb8bd4ed99e37a650f1d462c391ae4ae546450436b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f33b353f49dad9739f03717967b6ed81661089b4a5f7503a731715f3f4e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:d1eb3ee699a52f4b20f4604d2e59b51c391ac02eb535317009268ef8a4fc45df`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 1.3 MB (1270772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309170da33d1e1e4b4a1a75c21c0120ff197fc0e4fb56a433d3097dd47cdb44b`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:e66bdc96a17047cd31d803681e0c481fef6963c4d0120511222702e892610149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19616013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9546217ea8e23f6143afa741cd4e2050c708ad5ad67102826bac0bd4e68e070`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ef0d9eddfed06ea09466e4f959f424bd4487ea48914b239e32d9a01ae664b`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 9.9 MB (9940223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1546130b809d653b7ffb8056fabb7cde5c59816ee611d191515f665953378af9`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05246638c115aace0ae244236cec9016bac4501e4699e0b5761e13d518f3aa7`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 6.1 MB (6055871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b12b29108acc7caee0ab23ab7c1191d2861b6bf4761b820569a0bb5519120cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3cccb44b653f9d355429131978d3190d1b78b70f94e13b2cc06e9f7997a5e`

```dockerfile
```

-	Layers:
	-	`sha256:3ae7b6184d4abc32aca3718238c88832fa852fc8a1b082f050f7d291dfde1737`  
		Last Modified: Wed, 08 Oct 2025 22:59:48 GMT  
		Size: 1.3 MB (1270623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7720d5b50178fd0c79f8f0d50307c9837e7c9413280ecc69217fdc55705d6b3f`  
		Last Modified: Wed, 08 Oct 2025 22:59:49 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:11ec21937e624e10112a9366a2e39f63804c250cd288519f31d38458aa0c9d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20560595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dfe8eb30ae660e9f6b618bd8acba1eb372978247dff8685fcdb0393231e246`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c17d61a4d1554d280ba28d7252c2f305090eeac61b357dd6b76bd73c43c63`  
		Last Modified: Thu, 09 Oct 2025 00:45:13 GMT  
		Size: 10.6 MB (10595397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26efea3de5b42df966c34855cef32948787b76acb851a4084e3e3ad212766f3`  
		Last Modified: Thu, 09 Oct 2025 00:45:11 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa99ddfbbb8375b453f006a945c8fa07c1ce170fda8448f7b653f0ac29d72c7b`  
		Last Modified: Thu, 09 Oct 2025 00:45:07 GMT  
		Size: 6.2 MB (6231972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:9c4cef9155fe22476444ceb17f379012b0c8b3e5e05a7c96919fa63eff2fdfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179a2005edd691213f7786f101a4bd63364292c1882766e726e961190a7a7a47`

```dockerfile
```

-	Layers:
	-	`sha256:33a5c683cc42bda4a70c31f9d11afeffee44599ee508e945b64f8f0f007364b0`  
		Last Modified: Thu, 09 Oct 2025 01:59:38 GMT  
		Size: 1.3 MB (1268775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ee5b46b5c6c2bdcc6f69f3de81a1779cddf19f1c547cb5807d97cd7e0429e`  
		Last Modified: Thu, 09 Oct 2025 01:59:39 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:af936cabadda0c93ca3a229f630f7a5f4888f182b0cbb68edba78dbfaf1dd897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19342220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6546997bb677e945cd6914f29dcdd5d93b42fce0ffcc5b7109c0829285bcea25`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90056e842713293c53c6dce4290bfbd298df758358806bd5d3bec46230a89716`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 9.8 MB (9840947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c83cc5e93d426e4646d9cce9fdd7a659215fc178d82320a85f6c6e13ce0939`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486e128aa6ab32a4665c7cdcb3ed936f18c1e8bf06a7a4d7414222f0a89ac9`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 6.0 MB (5985049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:7bdbcb1c990676d35120b16117a0adacceb673203918e2e310ce5e5bb9f8ef01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1819ad33d43cee11f7584b364a2e91ced1b9b8229dea8fc4e7bf7cad969bfe7`

```dockerfile
```

-	Layers:
	-	`sha256:0191fc70832b0a543dfdac6c4787f835b7dd8fd57d9e0b7c1a864173c00c5b5a`  
		Last Modified: Thu, 09 Oct 2025 07:59:31 GMT  
		Size: 1.3 MB (1268771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101fedb5dfade0a1d32aed1260a2c4e061defe2886d8bccdd1cabcc4f65ab848`  
		Last Modified: Thu, 09 Oct 2025 07:59:32 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:f3623b26ebb6e5ca70e89646c7b5dc3cc4923efff13fcf40e13603205b1d2c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20728269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc9af67d43ea3efb18b38b4dd936194a56cde8d7cedf49529c2085f844b996`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a35a93027b47a44ea544d9fee84d01ab7be35185d9c512211141ce9d358b9c`  
		Last Modified: Thu, 09 Oct 2025 00:42:42 GMT  
		Size: 11.0 MB (10953642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054cb0439f6b75b07dcf89d2ae109ef474c8c1ca0e6748b16768e98125bfadd4`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439f567e83e96d3eb1406d4ffb34da86c733b3fc27798542727ad6be641a537`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 6.1 MB (6124398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:033679be33af045692166464cde309c06c55d1e3c2f0f70ff8f5a32a40c138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3b68e4209308a841644a418b0f59ac60f7f2626e13c308ee01fa66528b5f4b`

```dockerfile
```

-	Layers:
	-	`sha256:874c4b424a680cfa6457999c0ce435d96b02cffc5203fa3f92b393d5811628a1`  
		Last Modified: Thu, 09 Oct 2025 01:59:58 GMT  
		Size: 1.3 MB (1268717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586c45ea22dc49613e4d853a8c98ede4e76cc44653d06cf317710f979f305a99`  
		Last Modified: Thu, 09 Oct 2025 01:59:59 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.22`

```console
$ docker pull irssi@sha256:1e663ae10149c0b4d9df663b9da7bb650a58deea6cb49343c8191884eb0ec8ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1-alpine3.22` - linux; amd64

```console
$ docker pull irssi@sha256:faf9e4f6be7260cc0682ec1445c6826e0bdcdc63f4a064eb8a981701bb709594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8798df3f4b34c7e6f52a3727072b2c410704453c6794f69663ce299680c47d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e11827177f1c189b726b09341a9159227f1bfd85f6bfa5e738af089ccd47cc`  
		Last Modified: Wed, 08 Oct 2025 22:39:07 GMT  
		Size: 10.4 MB (10396003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6644b44e4c465f7087dbb97380180e75f01380c552303d8a2486f385aad34f35`  
		Last Modified: Wed, 08 Oct 2025 22:39:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b031546d04685e49a4d43b8482a34aaa0e6a3a6d75e947a09671aaf238e1ffc`  
		Last Modified: Wed, 08 Oct 2025 22:39:05 GMT  
		Size: 6.0 MB (5973981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:60dc002a8263e274525a471186038e9a631be6a5c61c1fd9e0ec2accade632f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be809ef2f20f547ecb812fc7251645454e581cc3d872627c003659069a74285e`

```dockerfile
```

-	Layers:
	-	`sha256:7def044fb5b5a27bb8a83fe2e1f6903b88c7090d91d03cc25c2be92d2b115084`  
		Last Modified: Thu, 09 Oct 2025 01:59:25 GMT  
		Size: 1.3 MB (1270668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d745c2ae7ce01c7631e58d7cf581615e9c45ca2b8d31cccaa988c9e5257205`  
		Last Modified: Thu, 09 Oct 2025 01:59:26 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; arm variant v6

```console
$ docker pull irssi@sha256:8dfb08ad7779ab00246287f396771e855c5271e8e67f8fcb68229714505701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4ac8e569bab3223b4cbc8f2ffb5137d951b2efa8fbca448cdef1d3e4925de`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b352b3151cd505887f05e68a9791f679acceebf79736c8050c72db1b5191a`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 9.6 MB (9619615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8386f23106fb9eeab59f6f1e82d6fda32cd5130f7e9240952ab361424133835`  
		Last Modified: Wed, 08 Oct 2025 21:42:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5176e22c73a447407c118250d8b7084c947461ad88e0f8ffba848633ef457d1`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 5.8 MB (5802239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:3529f2221a487a696afdfab5dd8793069c4e5153fdd0bbc77b1a10ed59976e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402305c7b183a88a4427e0caf1314f408323bb659aab78e52073f5d4946a814`

```dockerfile
```

-	Layers:
	-	`sha256:40cb74de7dde3071930d2507974b11b96e2a2fcf0dd4cc4063ea7658469d44d0`  
		Last Modified: Wed, 08 Oct 2025 22:59:36 GMT  
		Size: 17.5 KB (17462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1c77198ac74e17d59093ac465b9d5cb18f5cf9b495d394dc7fe1757c6cd43c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18234853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e381f20e12f748a613e6b9d046d4f23726de50b2d6209ee706e26cdc81cd9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355e9f8d23dd7df754d0fc9b69cb593d77843421e4fdc90e0999ac63d910671`  
		Last Modified: Wed, 08 Oct 2025 21:42:22 GMT  
		Size: 9.4 MB (9449582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d327d03f3716120871e15d8a53213e2201fb4c543cff4cfda89d44a362924f5b`  
		Last Modified: Wed, 08 Oct 2025 21:42:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7bac72cbbe13e0d2ca93a7e2045c3cee7af4a9a99e4f4a137d438a669963e`  
		Last Modified: Wed, 08 Oct 2025 21:42:21 GMT  
		Size: 5.6 MB (5562729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:a538097b3d9e95fd66c681e163119ee4fda34648e1138be1471be07765e086b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1291403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd05d16ceb8c11139b6c2e140bdd3f2ff4d48d4eeae0c78b36653e7f2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:66532285c363d95627518c5ee59b11b1d8179d0e9a5459c633c0d02618fed06d`  
		Last Modified: Wed, 08 Oct 2025 22:59:39 GMT  
		Size: 1.3 MB (1273726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f81d5bd314d48e57ad6439aa665accb301d8fa90cf9cfbc734e80cc3932d07`  
		Last Modified: Wed, 08 Oct 2025 22:59:40 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6312b888a6893a7c5bcbfa3b983ab38749f99778b44a99530ef47a5fa8afe92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6748a647916da83e7b32a7fc1af7248d48c18b28e2c35d2403a1aeaba48783`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d53dd86b6f70255a46f81ded3715200f2293ef56b5b5e4a9bd208fe73a5a4`  
		Last Modified: Wed, 08 Oct 2025 21:28:34 GMT  
		Size: 10.4 MB (10358145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35b8acbeb2e8727c286447b6769cf3d016bb4864c5ad35e2e295e2f173749a`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb455678cd1949819acffee4a71aa2ae7f91c1aae58a696c6666455cd9924e53`  
		Last Modified: Wed, 08 Oct 2025 21:28:35 GMT  
		Size: 5.8 MB (5847748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:816e238d7fee6ac073eb8bd4ed99e37a650f1d462c391ae4ae546450436b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f33b353f49dad9739f03717967b6ed81661089b4a5f7503a731715f3f4e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:d1eb3ee699a52f4b20f4604d2e59b51c391ac02eb535317009268ef8a4fc45df`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 1.3 MB (1270772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309170da33d1e1e4b4a1a75c21c0120ff197fc0e4fb56a433d3097dd47cdb44b`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; 386

```console
$ docker pull irssi@sha256:e66bdc96a17047cd31d803681e0c481fef6963c4d0120511222702e892610149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19616013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9546217ea8e23f6143afa741cd4e2050c708ad5ad67102826bac0bd4e68e070`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ef0d9eddfed06ea09466e4f959f424bd4487ea48914b239e32d9a01ae664b`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 9.9 MB (9940223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1546130b809d653b7ffb8056fabb7cde5c59816ee611d191515f665953378af9`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05246638c115aace0ae244236cec9016bac4501e4699e0b5761e13d518f3aa7`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 6.1 MB (6055871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:b12b29108acc7caee0ab23ab7c1191d2861b6bf4761b820569a0bb5519120cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3cccb44b653f9d355429131978d3190d1b78b70f94e13b2cc06e9f7997a5e`

```dockerfile
```

-	Layers:
	-	`sha256:3ae7b6184d4abc32aca3718238c88832fa852fc8a1b082f050f7d291dfde1737`  
		Last Modified: Wed, 08 Oct 2025 22:59:48 GMT  
		Size: 1.3 MB (1270623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7720d5b50178fd0c79f8f0d50307c9837e7c9413280ecc69217fdc55705d6b3f`  
		Last Modified: Wed, 08 Oct 2025 22:59:49 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; ppc64le

```console
$ docker pull irssi@sha256:11ec21937e624e10112a9366a2e39f63804c250cd288519f31d38458aa0c9d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20560595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dfe8eb30ae660e9f6b618bd8acba1eb372978247dff8685fcdb0393231e246`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c17d61a4d1554d280ba28d7252c2f305090eeac61b357dd6b76bd73c43c63`  
		Last Modified: Thu, 09 Oct 2025 00:45:13 GMT  
		Size: 10.6 MB (10595397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26efea3de5b42df966c34855cef32948787b76acb851a4084e3e3ad212766f3`  
		Last Modified: Thu, 09 Oct 2025 00:45:11 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa99ddfbbb8375b453f006a945c8fa07c1ce170fda8448f7b653f0ac29d72c7b`  
		Last Modified: Thu, 09 Oct 2025 00:45:07 GMT  
		Size: 6.2 MB (6231972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:9c4cef9155fe22476444ceb17f379012b0c8b3e5e05a7c96919fa63eff2fdfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179a2005edd691213f7786f101a4bd63364292c1882766e726e961190a7a7a47`

```dockerfile
```

-	Layers:
	-	`sha256:33a5c683cc42bda4a70c31f9d11afeffee44599ee508e945b64f8f0f007364b0`  
		Last Modified: Thu, 09 Oct 2025 01:59:38 GMT  
		Size: 1.3 MB (1268775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ee5b46b5c6c2bdcc6f69f3de81a1779cddf19f1c547cb5807d97cd7e0429e`  
		Last Modified: Thu, 09 Oct 2025 01:59:39 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; riscv64

```console
$ docker pull irssi@sha256:af936cabadda0c93ca3a229f630f7a5f4888f182b0cbb68edba78dbfaf1dd897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19342220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6546997bb677e945cd6914f29dcdd5d93b42fce0ffcc5b7109c0829285bcea25`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90056e842713293c53c6dce4290bfbd298df758358806bd5d3bec46230a89716`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 9.8 MB (9840947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c83cc5e93d426e4646d9cce9fdd7a659215fc178d82320a85f6c6e13ce0939`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486e128aa6ab32a4665c7cdcb3ed936f18c1e8bf06a7a4d7414222f0a89ac9`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 6.0 MB (5985049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:7bdbcb1c990676d35120b16117a0adacceb673203918e2e310ce5e5bb9f8ef01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1819ad33d43cee11f7584b364a2e91ced1b9b8229dea8fc4e7bf7cad969bfe7`

```dockerfile
```

-	Layers:
	-	`sha256:0191fc70832b0a543dfdac6c4787f835b7dd8fd57d9e0b7c1a864173c00c5b5a`  
		Last Modified: Thu, 09 Oct 2025 07:59:31 GMT  
		Size: 1.3 MB (1268771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101fedb5dfade0a1d32aed1260a2c4e061defe2886d8bccdd1cabcc4f65ab848`  
		Last Modified: Thu, 09 Oct 2025 07:59:32 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; s390x

```console
$ docker pull irssi@sha256:f3623b26ebb6e5ca70e89646c7b5dc3cc4923efff13fcf40e13603205b1d2c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20728269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc9af67d43ea3efb18b38b4dd936194a56cde8d7cedf49529c2085f844b996`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a35a93027b47a44ea544d9fee84d01ab7be35185d9c512211141ce9d358b9c`  
		Last Modified: Thu, 09 Oct 2025 00:42:42 GMT  
		Size: 11.0 MB (10953642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054cb0439f6b75b07dcf89d2ae109ef474c8c1ca0e6748b16768e98125bfadd4`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439f567e83e96d3eb1406d4ffb34da86c733b3fc27798542727ad6be641a537`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 6.1 MB (6124398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:033679be33af045692166464cde309c06c55d1e3c2f0f70ff8f5a32a40c138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3b68e4209308a841644a418b0f59ac60f7f2626e13c308ee01fa66528b5f4b`

```dockerfile
```

-	Layers:
	-	`sha256:874c4b424a680cfa6457999c0ce435d96b02cffc5203fa3f92b393d5811628a1`  
		Last Modified: Thu, 09 Oct 2025 01:59:58 GMT  
		Size: 1.3 MB (1268717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586c45ea22dc49613e4d853a8c98ede4e76cc44653d06cf317710f979f305a99`  
		Last Modified: Thu, 09 Oct 2025 01:59:59 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-trixie`

```console
$ docker pull irssi@sha256:f16b9ab6967270a5b2d0745b7f6b9233f6226b9866de8e46ab3f67f20167dde3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1-trixie` - linux; amd64

```console
$ docker pull irssi@sha256:1c3ad0c692729985069dc605f6970c498536ff77cdc28731957a9981bb5cc69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8b5071dd14f9cc7babdbbb92be355488770afbb4baa1dd4193f835544e54d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:18:09 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 04:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 04:18:46 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 04:18:46 GMT
USER user
# Tue, 18 Nov 2025 04:18:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3defe69b9d42ee331ee4997997e0b6950a228ac42a28acb744b2a217802984`  
		Last Modified: Tue, 18 Nov 2025 04:19:08 GMT  
		Size: 19.2 MB (19222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d261d2d2be0daf5812e199043e646cd3b38c72c6a85a46d1aa2664afbbfdab`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb0ce4ebcc67d4eb7b0fd5a6f142adedb46b4a4b5c9f752bb3663092160fd4`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 4.9 MB (4866605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:22bdb7c49ddfaba85497f04c9d268938716f3b3352fe24378d933a7732e8d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d4070dfa4342b3ae917c1f765452b8b31cbfe6c04864d806db24d761ba3c65`

```dockerfile
```

-	Layers:
	-	`sha256:5234daf2a71968c25322c71bfea4cdc75082624fc15fcfa85f68596c0e1e8722`  
		Last Modified: Tue, 18 Nov 2025 06:01:31 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6a5104b772e5ddb76df8ed09e14d2aaf8f4757fd03c65a00ce68904337b081`  
		Last Modified: Tue, 18 Nov 2025 06:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3bfeabfea3f173a6eef66224244f7c8ab79162e4b3e3454b5d7b951b699e6d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce561de65d9ced729b270243f33a9fe650e7088512ea128954c48a408518f61`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:22:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:23:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:23:21 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:23:21 GMT
USER user
# Tue, 18 Nov 2025 02:23:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e77346f90948edf43f33edec1b3c918cc8196b58e71fc74d47eb901d26a7c88`  
		Last Modified: Tue, 18 Nov 2025 02:23:39 GMT  
		Size: 18.3 MB (18286955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20fff4d4c2bb97e0fc743edd41339f9e7f2db5706f958f8419de0227c19fa9`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deede23e33150dccc8ce32f23f864d2a100697bb5c3f5f0d51414ec4913c97f`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 4.7 MB (4709653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:92486d0301f23f7f5fef04e23a1038f9c9c424a3a47ade435591fdd52853f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1456fb2be5b0b7cdc491b833efa2a0ceb4796c5c761a82e6ef643577401e6`

```dockerfile
```

-	Layers:
	-	`sha256:6273392ed72e310ca2593fd6731c533c6f636ed1289f29f728e45fc25e8d45b3`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c338421356fba9d226382ee2864822813fdd13c90654bd98562c53392aa9884f`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6206945589cb5f70880eb627ea43ce5e83dc6b09e69ad976fc69ec0a8a671e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e2dfadf9b6f72f29f6e28ff5885e16008ea991da97c386c12c6effd41ef773`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:24:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:24:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:24:41 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:24:41 GMT
USER user
# Tue, 18 Nov 2025 02:24:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07012b32f4cdf9145076ab6689e96bf750c40d6358ddc6b3d983ed86522093b2`  
		Last Modified: Tue, 18 Nov 2025 02:25:00 GMT  
		Size: 17.9 MB (17909541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317eec7c88d4aa0563b4acdfa018d18e2244d1cd4faaa808233aad6ed8c4eef`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e397c097f4a4f9d07fc0ad13a259eb1c5dc9952ad435619e84f81acd7aa5a`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 4.6 MB (4558582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2807406dbaf53bd4128387747c9380192177098c869b02c4fbc0e079734b4a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912225e9dca4300bbd0be1c71db46f637c20bb0ae39dd56905152d9fd37712e7`

```dockerfile
```

-	Layers:
	-	`sha256:826b1dd7affc3defc30e532bafe21b81af9274fe59f9cb13bc8880b266566410`  
		Last Modified: Tue, 18 Nov 2025 06:01:49 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caba9a457c37510c70d5629f0b91ebfec1b4e1fddabcf69e4581cc62b8efbdf9`  
		Last Modified: Tue, 18 Nov 2025 06:01:51 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0ca154f240d8e55d9139562ed162f6d09ed917369e5d3ac0ef11f4277868a144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494da41086e91ed2e2a5b5a81ed84f81af0313ded1a6a19ca4935a9ed697e260`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:19:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:20:13 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:20:13 GMT
USER user
# Tue, 18 Nov 2025 02:20:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619a9a2c5679b92c7e4905e08f05810e02f68d89d06b10524e21d2583f4ab16`  
		Last Modified: Tue, 18 Nov 2025 02:20:32 GMT  
		Size: 19.0 MB (19049113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494e61b822c7885405295c0e02e3d6f750e57594294fe2d8b997a0632065745d`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84635b25a37fcbf6ec3700e051e040f70178ad0e6880c9c76aeef1ebcfdf275`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 4.8 MB (4781743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6b955f8723ba03a2a30061c1a89c6af489d1442317213524c5594663f9d28695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b845fa96792ab508c1cabce079cc6822b4d3ed51f4ff9cc1486fb4becdb2b9`

```dockerfile
```

-	Layers:
	-	`sha256:1e1288c631711328c43fbd795987044f9c19d6d7ca488586f7d48b2d1bbf9fc9`  
		Last Modified: Tue, 18 Nov 2025 06:01:56 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3627aff8962b25f0eb1a595d760c047d53573e5a83de81ffd5ee43ffde3e283f`  
		Last Modified: Tue, 18 Nov 2025 06:01:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; 386

```console
$ docker pull irssi@sha256:9ca8e0716038e4dbc489c402c36d6bdc49bb1c6dc80a6050371e0ebb63798b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afefadafe5f8e789fb22f477834b8855758beefa989deb19c7f4e79699e5e89`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:17:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:17:16 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:17:16 GMT
USER user
# Tue, 18 Nov 2025 02:17:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2fb43e1b281a402bf774cd8bde6070d229add5d03c870cbfe7c8e16f2cbb7`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 18.7 MB (18740862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6997edee7df4e50b70fa845f324ec76992912dec560143cbead27a7aec43803b`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a3e4cae20c6dc7e982f2a19aa8de8e2b641b6bcc81e72f1bef2930dca363d`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 4.9 MB (4868298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:59d4050c0c1cd29128be910eccf5ea2a035052b836f46e045244c9f64fa4298c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1003b498f9e79e27d0402d3e70dfc68a8d4f2e5fb76327ddf0d269848f164933`

```dockerfile
```

-	Layers:
	-	`sha256:dae334eb70cbeb2210f0f00af9826de6e0af19a4045d45c351ccd063c967c44c`  
		Last Modified: Tue, 18 Nov 2025 06:02:04 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f17fc2c6b6001ffa3a573775d2cbcfc57f6836267cf4f7578260842ada1b7`  
		Last Modified: Tue, 18 Nov 2025 06:02:05 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:459fe708abbb929ace6e5502ac492cb132f84c0e1b80e5a3dd662a7d98b6470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72533238806364f21d117ef1051d9f72e86e6063d9c6683bc210cea47127bda`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 15:03:14 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 15:03:14 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 15:04:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 15:04:50 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 15:04:50 GMT
USER user
# Tue, 18 Nov 2025 15:04:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f858dd24ce7b2766334f11cb720c162ec10dcc1115c24b7c5a2cb933f4732e`  
		Last Modified: Tue, 18 Nov 2025 15:05:24 GMT  
		Size: 19.5 MB (19542803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e87e68a0f54b41f554a220560c01fae4bca1b4bb4b83336d6c6110f750186`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab575b18effe508097b5d8936201a72cd903f95c5c055af70a652fee9591f15f`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 5.1 MB (5097211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:43823b3c76d194b48bf19fd79dde879a47f65352dc638bc93f743de8b5863b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b0fd9dbba87f1d0495d3f376c23a11766edc9e180c9c6afddfacb7df1cbe76`

```dockerfile
```

-	Layers:
	-	`sha256:ebbbdb938672f1b98a9abf9c0267764349f2261c7295ea777971571c28ac293f`  
		Last Modified: Tue, 18 Nov 2025 18:00:17 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae083b6d0624ff996d976b7dfead8f215b20de9aedc3bef84697341f367a4d3`  
		Last Modified: Tue, 18 Nov 2025 18:00:18 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:0a17bc9dc7f1ede0aae4d4035aa269c39fdd3ad059158a3c6a569fa2bf7da8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6a1bc4c5ae216cf035ec48b010768259be2a066ee4ef066bcb9c32d445e4d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 10:01:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:01:44 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 10:08:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 10:08:36 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 10:08:36 GMT
USER user
# Tue, 18 Nov 2025 10:08:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afef2a7493fa326b06e464e36f2a79568e4c5c265515366e193165f0b4d284e`  
		Last Modified: Tue, 18 Nov 2025 10:10:42 GMT  
		Size: 18.5 MB (18549074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026bbe28877d1917f647dacffd37172e95435e1c7e9fbe30a62986bb72cd62b`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 3.3 KB (3337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3d248f54be38451080b4d25093d9df5c1c9efe1175c3cf58494a7e0fd7fe62`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 4.9 MB (4860627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:7b01cdd2258dc9fd9266a05e6cbd264f72886699285f27da4dcfa624dcb82f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb4ae2e3561846a1f14e41a61390911210a0c9ea6b4f9bace7ef57ca7a1303`

```dockerfile
```

-	Layers:
	-	`sha256:5044523627d968ee0b87912ad5e86b6f374ff85ef9a7878ae77c52dcf5581421`  
		Last Modified: Tue, 18 Nov 2025 18:00:24 GMT  
		Size: 5.6 MB (5579680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43863609ed306f6a1f2ac385d2c41ef9efb115640066a4bb3b02043bb96f7158`  
		Last Modified: Tue, 18 Nov 2025 18:00:25 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:da93e9283b14d1092e451a797eb231f916c62509d64042a7ed65617b6ab9c487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b5c6cf33fd166afa65862c57464a7a99d44516a592d7093c9c71058d5008c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:17:58 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:18:33 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:18:33 GMT
USER user
# Tue, 18 Nov 2025 02:18:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce4907214a18511e7c1676f0b93794fa538b6672045daa187e1c681bbd9019`  
		Last Modified: Tue, 18 Nov 2025 02:18:55 GMT  
		Size: 19.8 MB (19759415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dca431fe704652eca13f122842a6232de3a88619e75b4585c55d73ab6784b33`  
		Last Modified: Tue, 18 Nov 2025 02:18:52 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12fa892c886e7110c8b36d26e5b06c87bdfad4dab6e9bf9b746c2887bce206f`  
		Last Modified: Tue, 18 Nov 2025 02:18:53 GMT  
		Size: 4.9 MB (4905870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:9921bed642cdddc5b883e960fbb4efa54a43817af46e8c05c8c59611062a6056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babbc467c5248e09f8d3d0710512a06a92fbd5173a81414b551f82cab3d5d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:a1fee033f27a53ca8a99d5789a2cf1a16782bef7f265384856e2f9c62104fc55`  
		Last Modified: Tue, 18 Nov 2025 06:02:18 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd54ab02d147f06764006021d0881cd166981d03206bbcbfdca3215249d036e1`  
		Last Modified: Tue, 18 Nov 2025 06:02:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:f16b9ab6967270a5b2d0745b7f6b9233f6226b9866de8e46ab3f67f20167dde3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4` - linux; amd64

```console
$ docker pull irssi@sha256:1c3ad0c692729985069dc605f6970c498536ff77cdc28731957a9981bb5cc69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8b5071dd14f9cc7babdbbb92be355488770afbb4baa1dd4193f835544e54d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:18:09 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 04:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 04:18:46 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 04:18:46 GMT
USER user
# Tue, 18 Nov 2025 04:18:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3defe69b9d42ee331ee4997997e0b6950a228ac42a28acb744b2a217802984`  
		Last Modified: Tue, 18 Nov 2025 04:19:08 GMT  
		Size: 19.2 MB (19222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d261d2d2be0daf5812e199043e646cd3b38c72c6a85a46d1aa2664afbbfdab`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb0ce4ebcc67d4eb7b0fd5a6f142adedb46b4a4b5c9f752bb3663092160fd4`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 4.9 MB (4866605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:22bdb7c49ddfaba85497f04c9d268938716f3b3352fe24378d933a7732e8d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d4070dfa4342b3ae917c1f765452b8b31cbfe6c04864d806db24d761ba3c65`

```dockerfile
```

-	Layers:
	-	`sha256:5234daf2a71968c25322c71bfea4cdc75082624fc15fcfa85f68596c0e1e8722`  
		Last Modified: Tue, 18 Nov 2025 06:01:31 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6a5104b772e5ddb76df8ed09e14d2aaf8f4757fd03c65a00ce68904337b081`  
		Last Modified: Tue, 18 Nov 2025 06:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3bfeabfea3f173a6eef66224244f7c8ab79162e4b3e3454b5d7b951b699e6d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce561de65d9ced729b270243f33a9fe650e7088512ea128954c48a408518f61`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:22:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:23:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:23:21 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:23:21 GMT
USER user
# Tue, 18 Nov 2025 02:23:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e77346f90948edf43f33edec1b3c918cc8196b58e71fc74d47eb901d26a7c88`  
		Last Modified: Tue, 18 Nov 2025 02:23:39 GMT  
		Size: 18.3 MB (18286955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20fff4d4c2bb97e0fc743edd41339f9e7f2db5706f958f8419de0227c19fa9`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deede23e33150dccc8ce32f23f864d2a100697bb5c3f5f0d51414ec4913c97f`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 4.7 MB (4709653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:92486d0301f23f7f5fef04e23a1038f9c9c424a3a47ade435591fdd52853f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1456fb2be5b0b7cdc491b833efa2a0ceb4796c5c761a82e6ef643577401e6`

```dockerfile
```

-	Layers:
	-	`sha256:6273392ed72e310ca2593fd6731c533c6f636ed1289f29f728e45fc25e8d45b3`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c338421356fba9d226382ee2864822813fdd13c90654bd98562c53392aa9884f`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6206945589cb5f70880eb627ea43ce5e83dc6b09e69ad976fc69ec0a8a671e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e2dfadf9b6f72f29f6e28ff5885e16008ea991da97c386c12c6effd41ef773`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:24:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:24:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:24:41 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:24:41 GMT
USER user
# Tue, 18 Nov 2025 02:24:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07012b32f4cdf9145076ab6689e96bf750c40d6358ddc6b3d983ed86522093b2`  
		Last Modified: Tue, 18 Nov 2025 02:25:00 GMT  
		Size: 17.9 MB (17909541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317eec7c88d4aa0563b4acdfa018d18e2244d1cd4faaa808233aad6ed8c4eef`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e397c097f4a4f9d07fc0ad13a259eb1c5dc9952ad435619e84f81acd7aa5a`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 4.6 MB (4558582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:2807406dbaf53bd4128387747c9380192177098c869b02c4fbc0e079734b4a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912225e9dca4300bbd0be1c71db46f637c20bb0ae39dd56905152d9fd37712e7`

```dockerfile
```

-	Layers:
	-	`sha256:826b1dd7affc3defc30e532bafe21b81af9274fe59f9cb13bc8880b266566410`  
		Last Modified: Tue, 18 Nov 2025 06:01:49 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caba9a457c37510c70d5629f0b91ebfec1b4e1fddabcf69e4581cc62b8efbdf9`  
		Last Modified: Tue, 18 Nov 2025 06:01:51 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0ca154f240d8e55d9139562ed162f6d09ed917369e5d3ac0ef11f4277868a144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494da41086e91ed2e2a5b5a81ed84f81af0313ded1a6a19ca4935a9ed697e260`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:19:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:20:13 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:20:13 GMT
USER user
# Tue, 18 Nov 2025 02:20:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619a9a2c5679b92c7e4905e08f05810e02f68d89d06b10524e21d2583f4ab16`  
		Last Modified: Tue, 18 Nov 2025 02:20:32 GMT  
		Size: 19.0 MB (19049113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494e61b822c7885405295c0e02e3d6f750e57594294fe2d8b997a0632065745d`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84635b25a37fcbf6ec3700e051e040f70178ad0e6880c9c76aeef1ebcfdf275`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 4.8 MB (4781743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:6b955f8723ba03a2a30061c1a89c6af489d1442317213524c5594663f9d28695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b845fa96792ab508c1cabce079cc6822b4d3ed51f4ff9cc1486fb4becdb2b9`

```dockerfile
```

-	Layers:
	-	`sha256:1e1288c631711328c43fbd795987044f9c19d6d7ca488586f7d48b2d1bbf9fc9`  
		Last Modified: Tue, 18 Nov 2025 06:01:56 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3627aff8962b25f0eb1a595d760c047d53573e5a83de81ffd5ee43ffde3e283f`  
		Last Modified: Tue, 18 Nov 2025 06:01:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:9ca8e0716038e4dbc489c402c36d6bdc49bb1c6dc80a6050371e0ebb63798b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afefadafe5f8e789fb22f477834b8855758beefa989deb19c7f4e79699e5e89`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:17:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:17:16 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:17:16 GMT
USER user
# Tue, 18 Nov 2025 02:17:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2fb43e1b281a402bf774cd8bde6070d229add5d03c870cbfe7c8e16f2cbb7`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 18.7 MB (18740862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6997edee7df4e50b70fa845f324ec76992912dec560143cbead27a7aec43803b`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a3e4cae20c6dc7e982f2a19aa8de8e2b641b6bcc81e72f1bef2930dca363d`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 4.9 MB (4868298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:59d4050c0c1cd29128be910eccf5ea2a035052b836f46e045244c9f64fa4298c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1003b498f9e79e27d0402d3e70dfc68a8d4f2e5fb76327ddf0d269848f164933`

```dockerfile
```

-	Layers:
	-	`sha256:dae334eb70cbeb2210f0f00af9826de6e0af19a4045d45c351ccd063c967c44c`  
		Last Modified: Tue, 18 Nov 2025 06:02:04 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f17fc2c6b6001ffa3a573775d2cbcfc57f6836267cf4f7578260842ada1b7`  
		Last Modified: Tue, 18 Nov 2025 06:02:05 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:459fe708abbb929ace6e5502ac492cb132f84c0e1b80e5a3dd662a7d98b6470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72533238806364f21d117ef1051d9f72e86e6063d9c6683bc210cea47127bda`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 15:03:14 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 15:03:14 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 15:04:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 15:04:50 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 15:04:50 GMT
USER user
# Tue, 18 Nov 2025 15:04:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f858dd24ce7b2766334f11cb720c162ec10dcc1115c24b7c5a2cb933f4732e`  
		Last Modified: Tue, 18 Nov 2025 15:05:24 GMT  
		Size: 19.5 MB (19542803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e87e68a0f54b41f554a220560c01fae4bca1b4bb4b83336d6c6110f750186`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab575b18effe508097b5d8936201a72cd903f95c5c055af70a652fee9591f15f`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 5.1 MB (5097211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:43823b3c76d194b48bf19fd79dde879a47f65352dc638bc93f743de8b5863b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b0fd9dbba87f1d0495d3f376c23a11766edc9e180c9c6afddfacb7df1cbe76`

```dockerfile
```

-	Layers:
	-	`sha256:ebbbdb938672f1b98a9abf9c0267764349f2261c7295ea777971571c28ac293f`  
		Last Modified: Tue, 18 Nov 2025 18:00:17 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae083b6d0624ff996d976b7dfead8f215b20de9aedc3bef84697341f367a4d3`  
		Last Modified: Tue, 18 Nov 2025 18:00:18 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; riscv64

```console
$ docker pull irssi@sha256:0a17bc9dc7f1ede0aae4d4035aa269c39fdd3ad059158a3c6a569fa2bf7da8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6a1bc4c5ae216cf035ec48b010768259be2a066ee4ef066bcb9c32d445e4d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 10:01:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:01:44 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 10:08:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 10:08:36 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 10:08:36 GMT
USER user
# Tue, 18 Nov 2025 10:08:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afef2a7493fa326b06e464e36f2a79568e4c5c265515366e193165f0b4d284e`  
		Last Modified: Tue, 18 Nov 2025 10:10:42 GMT  
		Size: 18.5 MB (18549074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026bbe28877d1917f647dacffd37172e95435e1c7e9fbe30a62986bb72cd62b`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 3.3 KB (3337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3d248f54be38451080b4d25093d9df5c1c9efe1175c3cf58494a7e0fd7fe62`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 4.9 MB (4860627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:7b01cdd2258dc9fd9266a05e6cbd264f72886699285f27da4dcfa624dcb82f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb4ae2e3561846a1f14e41a61390911210a0c9ea6b4f9bace7ef57ca7a1303`

```dockerfile
```

-	Layers:
	-	`sha256:5044523627d968ee0b87912ad5e86b6f374ff85ef9a7878ae77c52dcf5581421`  
		Last Modified: Tue, 18 Nov 2025 18:00:24 GMT  
		Size: 5.6 MB (5579680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43863609ed306f6a1f2ac385d2c41ef9efb115640066a4bb3b02043bb96f7158`  
		Last Modified: Tue, 18 Nov 2025 18:00:25 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:da93e9283b14d1092e451a797eb231f916c62509d64042a7ed65617b6ab9c487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b5c6cf33fd166afa65862c57464a7a99d44516a592d7093c9c71058d5008c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:17:58 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:18:33 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:18:33 GMT
USER user
# Tue, 18 Nov 2025 02:18:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce4907214a18511e7c1676f0b93794fa538b6672045daa187e1c681bbd9019`  
		Last Modified: Tue, 18 Nov 2025 02:18:55 GMT  
		Size: 19.8 MB (19759415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dca431fe704652eca13f122842a6232de3a88619e75b4585c55d73ab6784b33`  
		Last Modified: Tue, 18 Nov 2025 02:18:52 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12fa892c886e7110c8b36d26e5b06c87bdfad4dab6e9bf9b746c2887bce206f`  
		Last Modified: Tue, 18 Nov 2025 02:18:53 GMT  
		Size: 4.9 MB (4905870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:9921bed642cdddc5b883e960fbb4efa54a43817af46e8c05c8c59611062a6056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babbc467c5248e09f8d3d0710512a06a92fbd5173a81414b551f82cab3d5d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:a1fee033f27a53ca8a99d5789a2cf1a16782bef7f265384856e2f9c62104fc55`  
		Last Modified: Tue, 18 Nov 2025 06:02:18 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd54ab02d147f06764006021d0881cd166981d03206bbcbfdca3215249d036e1`  
		Last Modified: Tue, 18 Nov 2025 06:02:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:1e663ae10149c0b4d9df663b9da7bb650a58deea6cb49343c8191884eb0ec8ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4-alpine` - linux; amd64

```console
$ docker pull irssi@sha256:faf9e4f6be7260cc0682ec1445c6826e0bdcdc63f4a064eb8a981701bb709594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8798df3f4b34c7e6f52a3727072b2c410704453c6794f69663ce299680c47d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e11827177f1c189b726b09341a9159227f1bfd85f6bfa5e738af089ccd47cc`  
		Last Modified: Wed, 08 Oct 2025 22:39:07 GMT  
		Size: 10.4 MB (10396003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6644b44e4c465f7087dbb97380180e75f01380c552303d8a2486f385aad34f35`  
		Last Modified: Wed, 08 Oct 2025 22:39:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b031546d04685e49a4d43b8482a34aaa0e6a3a6d75e947a09671aaf238e1ffc`  
		Last Modified: Wed, 08 Oct 2025 22:39:05 GMT  
		Size: 6.0 MB (5973981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:60dc002a8263e274525a471186038e9a631be6a5c61c1fd9e0ec2accade632f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be809ef2f20f547ecb812fc7251645454e581cc3d872627c003659069a74285e`

```dockerfile
```

-	Layers:
	-	`sha256:7def044fb5b5a27bb8a83fe2e1f6903b88c7090d91d03cc25c2be92d2b115084`  
		Last Modified: Thu, 09 Oct 2025 01:59:25 GMT  
		Size: 1.3 MB (1270668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d745c2ae7ce01c7631e58d7cf581615e9c45ca2b8d31cccaa988c9e5257205`  
		Last Modified: Thu, 09 Oct 2025 01:59:26 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:8dfb08ad7779ab00246287f396771e855c5271e8e67f8fcb68229714505701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4ac8e569bab3223b4cbc8f2ffb5137d951b2efa8fbca448cdef1d3e4925de`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b352b3151cd505887f05e68a9791f679acceebf79736c8050c72db1b5191a`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 9.6 MB (9619615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8386f23106fb9eeab59f6f1e82d6fda32cd5130f7e9240952ab361424133835`  
		Last Modified: Wed, 08 Oct 2025 21:42:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5176e22c73a447407c118250d8b7084c947461ad88e0f8ffba848633ef457d1`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 5.8 MB (5802239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3529f2221a487a696afdfab5dd8793069c4e5153fdd0bbc77b1a10ed59976e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402305c7b183a88a4427e0caf1314f408323bb659aab78e52073f5d4946a814`

```dockerfile
```

-	Layers:
	-	`sha256:40cb74de7dde3071930d2507974b11b96e2a2fcf0dd4cc4063ea7658469d44d0`  
		Last Modified: Wed, 08 Oct 2025 22:59:36 GMT  
		Size: 17.5 KB (17462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1c77198ac74e17d59093ac465b9d5cb18f5cf9b495d394dc7fe1757c6cd43c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18234853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e381f20e12f748a613e6b9d046d4f23726de50b2d6209ee706e26cdc81cd9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355e9f8d23dd7df754d0fc9b69cb593d77843421e4fdc90e0999ac63d910671`  
		Last Modified: Wed, 08 Oct 2025 21:42:22 GMT  
		Size: 9.4 MB (9449582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d327d03f3716120871e15d8a53213e2201fb4c543cff4cfda89d44a362924f5b`  
		Last Modified: Wed, 08 Oct 2025 21:42:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7bac72cbbe13e0d2ca93a7e2045c3cee7af4a9a99e4f4a137d438a669963e`  
		Last Modified: Wed, 08 Oct 2025 21:42:21 GMT  
		Size: 5.6 MB (5562729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:a538097b3d9e95fd66c681e163119ee4fda34648e1138be1471be07765e086b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1291403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd05d16ceb8c11139b6c2e140bdd3f2ff4d48d4eeae0c78b36653e7f2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:66532285c363d95627518c5ee59b11b1d8179d0e9a5459c633c0d02618fed06d`  
		Last Modified: Wed, 08 Oct 2025 22:59:39 GMT  
		Size: 1.3 MB (1273726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f81d5bd314d48e57ad6439aa665accb301d8fa90cf9cfbc734e80cc3932d07`  
		Last Modified: Wed, 08 Oct 2025 22:59:40 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6312b888a6893a7c5bcbfa3b983ab38749f99778b44a99530ef47a5fa8afe92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6748a647916da83e7b32a7fc1af7248d48c18b28e2c35d2403a1aeaba48783`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d53dd86b6f70255a46f81ded3715200f2293ef56b5b5e4a9bd208fe73a5a4`  
		Last Modified: Wed, 08 Oct 2025 21:28:34 GMT  
		Size: 10.4 MB (10358145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35b8acbeb2e8727c286447b6769cf3d016bb4864c5ad35e2e295e2f173749a`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb455678cd1949819acffee4a71aa2ae7f91c1aae58a696c6666455cd9924e53`  
		Last Modified: Wed, 08 Oct 2025 21:28:35 GMT  
		Size: 5.8 MB (5847748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:816e238d7fee6ac073eb8bd4ed99e37a650f1d462c391ae4ae546450436b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f33b353f49dad9739f03717967b6ed81661089b4a5f7503a731715f3f4e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:d1eb3ee699a52f4b20f4604d2e59b51c391ac02eb535317009268ef8a4fc45df`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 1.3 MB (1270772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309170da33d1e1e4b4a1a75c21c0120ff197fc0e4fb56a433d3097dd47cdb44b`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:e66bdc96a17047cd31d803681e0c481fef6963c4d0120511222702e892610149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19616013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9546217ea8e23f6143afa741cd4e2050c708ad5ad67102826bac0bd4e68e070`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ef0d9eddfed06ea09466e4f959f424bd4487ea48914b239e32d9a01ae664b`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 9.9 MB (9940223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1546130b809d653b7ffb8056fabb7cde5c59816ee611d191515f665953378af9`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05246638c115aace0ae244236cec9016bac4501e4699e0b5761e13d518f3aa7`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 6.1 MB (6055871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b12b29108acc7caee0ab23ab7c1191d2861b6bf4761b820569a0bb5519120cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3cccb44b653f9d355429131978d3190d1b78b70f94e13b2cc06e9f7997a5e`

```dockerfile
```

-	Layers:
	-	`sha256:3ae7b6184d4abc32aca3718238c88832fa852fc8a1b082f050f7d291dfde1737`  
		Last Modified: Wed, 08 Oct 2025 22:59:48 GMT  
		Size: 1.3 MB (1270623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7720d5b50178fd0c79f8f0d50307c9837e7c9413280ecc69217fdc55705d6b3f`  
		Last Modified: Wed, 08 Oct 2025 22:59:49 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:11ec21937e624e10112a9366a2e39f63804c250cd288519f31d38458aa0c9d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20560595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dfe8eb30ae660e9f6b618bd8acba1eb372978247dff8685fcdb0393231e246`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c17d61a4d1554d280ba28d7252c2f305090eeac61b357dd6b76bd73c43c63`  
		Last Modified: Thu, 09 Oct 2025 00:45:13 GMT  
		Size: 10.6 MB (10595397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26efea3de5b42df966c34855cef32948787b76acb851a4084e3e3ad212766f3`  
		Last Modified: Thu, 09 Oct 2025 00:45:11 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa99ddfbbb8375b453f006a945c8fa07c1ce170fda8448f7b653f0ac29d72c7b`  
		Last Modified: Thu, 09 Oct 2025 00:45:07 GMT  
		Size: 6.2 MB (6231972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:9c4cef9155fe22476444ceb17f379012b0c8b3e5e05a7c96919fa63eff2fdfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179a2005edd691213f7786f101a4bd63364292c1882766e726e961190a7a7a47`

```dockerfile
```

-	Layers:
	-	`sha256:33a5c683cc42bda4a70c31f9d11afeffee44599ee508e945b64f8f0f007364b0`  
		Last Modified: Thu, 09 Oct 2025 01:59:38 GMT  
		Size: 1.3 MB (1268775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ee5b46b5c6c2bdcc6f69f3de81a1779cddf19f1c547cb5807d97cd7e0429e`  
		Last Modified: Thu, 09 Oct 2025 01:59:39 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:af936cabadda0c93ca3a229f630f7a5f4888f182b0cbb68edba78dbfaf1dd897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19342220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6546997bb677e945cd6914f29dcdd5d93b42fce0ffcc5b7109c0829285bcea25`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90056e842713293c53c6dce4290bfbd298df758358806bd5d3bec46230a89716`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 9.8 MB (9840947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c83cc5e93d426e4646d9cce9fdd7a659215fc178d82320a85f6c6e13ce0939`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486e128aa6ab32a4665c7cdcb3ed936f18c1e8bf06a7a4d7414222f0a89ac9`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 6.0 MB (5985049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:7bdbcb1c990676d35120b16117a0adacceb673203918e2e310ce5e5bb9f8ef01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1819ad33d43cee11f7584b364a2e91ced1b9b8229dea8fc4e7bf7cad969bfe7`

```dockerfile
```

-	Layers:
	-	`sha256:0191fc70832b0a543dfdac6c4787f835b7dd8fd57d9e0b7c1a864173c00c5b5a`  
		Last Modified: Thu, 09 Oct 2025 07:59:31 GMT  
		Size: 1.3 MB (1268771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101fedb5dfade0a1d32aed1260a2c4e061defe2886d8bccdd1cabcc4f65ab848`  
		Last Modified: Thu, 09 Oct 2025 07:59:32 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:f3623b26ebb6e5ca70e89646c7b5dc3cc4923efff13fcf40e13603205b1d2c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20728269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc9af67d43ea3efb18b38b4dd936194a56cde8d7cedf49529c2085f844b996`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a35a93027b47a44ea544d9fee84d01ab7be35185d9c512211141ce9d358b9c`  
		Last Modified: Thu, 09 Oct 2025 00:42:42 GMT  
		Size: 11.0 MB (10953642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054cb0439f6b75b07dcf89d2ae109ef474c8c1ca0e6748b16768e98125bfadd4`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439f567e83e96d3eb1406d4ffb34da86c733b3fc27798542727ad6be641a537`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 6.1 MB (6124398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:033679be33af045692166464cde309c06c55d1e3c2f0f70ff8f5a32a40c138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3b68e4209308a841644a418b0f59ac60f7f2626e13c308ee01fa66528b5f4b`

```dockerfile
```

-	Layers:
	-	`sha256:874c4b424a680cfa6457999c0ce435d96b02cffc5203fa3f92b393d5811628a1`  
		Last Modified: Thu, 09 Oct 2025 01:59:58 GMT  
		Size: 1.3 MB (1268717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586c45ea22dc49613e4d853a8c98ede4e76cc44653d06cf317710f979f305a99`  
		Last Modified: Thu, 09 Oct 2025 01:59:59 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.22`

```console
$ docker pull irssi@sha256:1e663ae10149c0b4d9df663b9da7bb650a58deea6cb49343c8191884eb0ec8ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4-alpine3.22` - linux; amd64

```console
$ docker pull irssi@sha256:faf9e4f6be7260cc0682ec1445c6826e0bdcdc63f4a064eb8a981701bb709594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8798df3f4b34c7e6f52a3727072b2c410704453c6794f69663ce299680c47d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e11827177f1c189b726b09341a9159227f1bfd85f6bfa5e738af089ccd47cc`  
		Last Modified: Wed, 08 Oct 2025 22:39:07 GMT  
		Size: 10.4 MB (10396003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6644b44e4c465f7087dbb97380180e75f01380c552303d8a2486f385aad34f35`  
		Last Modified: Wed, 08 Oct 2025 22:39:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b031546d04685e49a4d43b8482a34aaa0e6a3a6d75e947a09671aaf238e1ffc`  
		Last Modified: Wed, 08 Oct 2025 22:39:05 GMT  
		Size: 6.0 MB (5973981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:60dc002a8263e274525a471186038e9a631be6a5c61c1fd9e0ec2accade632f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be809ef2f20f547ecb812fc7251645454e581cc3d872627c003659069a74285e`

```dockerfile
```

-	Layers:
	-	`sha256:7def044fb5b5a27bb8a83fe2e1f6903b88c7090d91d03cc25c2be92d2b115084`  
		Last Modified: Thu, 09 Oct 2025 01:59:25 GMT  
		Size: 1.3 MB (1270668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d745c2ae7ce01c7631e58d7cf581615e9c45ca2b8d31cccaa988c9e5257205`  
		Last Modified: Thu, 09 Oct 2025 01:59:26 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; arm variant v6

```console
$ docker pull irssi@sha256:8dfb08ad7779ab00246287f396771e855c5271e8e67f8fcb68229714505701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4ac8e569bab3223b4cbc8f2ffb5137d951b2efa8fbca448cdef1d3e4925de`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b352b3151cd505887f05e68a9791f679acceebf79736c8050c72db1b5191a`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 9.6 MB (9619615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8386f23106fb9eeab59f6f1e82d6fda32cd5130f7e9240952ab361424133835`  
		Last Modified: Wed, 08 Oct 2025 21:42:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5176e22c73a447407c118250d8b7084c947461ad88e0f8ffba848633ef457d1`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 5.8 MB (5802239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:3529f2221a487a696afdfab5dd8793069c4e5153fdd0bbc77b1a10ed59976e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402305c7b183a88a4427e0caf1314f408323bb659aab78e52073f5d4946a814`

```dockerfile
```

-	Layers:
	-	`sha256:40cb74de7dde3071930d2507974b11b96e2a2fcf0dd4cc4063ea7658469d44d0`  
		Last Modified: Wed, 08 Oct 2025 22:59:36 GMT  
		Size: 17.5 KB (17462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1c77198ac74e17d59093ac465b9d5cb18f5cf9b495d394dc7fe1757c6cd43c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18234853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e381f20e12f748a613e6b9d046d4f23726de50b2d6209ee706e26cdc81cd9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355e9f8d23dd7df754d0fc9b69cb593d77843421e4fdc90e0999ac63d910671`  
		Last Modified: Wed, 08 Oct 2025 21:42:22 GMT  
		Size: 9.4 MB (9449582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d327d03f3716120871e15d8a53213e2201fb4c543cff4cfda89d44a362924f5b`  
		Last Modified: Wed, 08 Oct 2025 21:42:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7bac72cbbe13e0d2ca93a7e2045c3cee7af4a9a99e4f4a137d438a669963e`  
		Last Modified: Wed, 08 Oct 2025 21:42:21 GMT  
		Size: 5.6 MB (5562729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:a538097b3d9e95fd66c681e163119ee4fda34648e1138be1471be07765e086b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1291403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd05d16ceb8c11139b6c2e140bdd3f2ff4d48d4eeae0c78b36653e7f2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:66532285c363d95627518c5ee59b11b1d8179d0e9a5459c633c0d02618fed06d`  
		Last Modified: Wed, 08 Oct 2025 22:59:39 GMT  
		Size: 1.3 MB (1273726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f81d5bd314d48e57ad6439aa665accb301d8fa90cf9cfbc734e80cc3932d07`  
		Last Modified: Wed, 08 Oct 2025 22:59:40 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6312b888a6893a7c5bcbfa3b983ab38749f99778b44a99530ef47a5fa8afe92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6748a647916da83e7b32a7fc1af7248d48c18b28e2c35d2403a1aeaba48783`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d53dd86b6f70255a46f81ded3715200f2293ef56b5b5e4a9bd208fe73a5a4`  
		Last Modified: Wed, 08 Oct 2025 21:28:34 GMT  
		Size: 10.4 MB (10358145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35b8acbeb2e8727c286447b6769cf3d016bb4864c5ad35e2e295e2f173749a`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb455678cd1949819acffee4a71aa2ae7f91c1aae58a696c6666455cd9924e53`  
		Last Modified: Wed, 08 Oct 2025 21:28:35 GMT  
		Size: 5.8 MB (5847748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:816e238d7fee6ac073eb8bd4ed99e37a650f1d462c391ae4ae546450436b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f33b353f49dad9739f03717967b6ed81661089b4a5f7503a731715f3f4e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:d1eb3ee699a52f4b20f4604d2e59b51c391ac02eb535317009268ef8a4fc45df`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 1.3 MB (1270772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309170da33d1e1e4b4a1a75c21c0120ff197fc0e4fb56a433d3097dd47cdb44b`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; 386

```console
$ docker pull irssi@sha256:e66bdc96a17047cd31d803681e0c481fef6963c4d0120511222702e892610149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19616013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9546217ea8e23f6143afa741cd4e2050c708ad5ad67102826bac0bd4e68e070`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ef0d9eddfed06ea09466e4f959f424bd4487ea48914b239e32d9a01ae664b`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 9.9 MB (9940223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1546130b809d653b7ffb8056fabb7cde5c59816ee611d191515f665953378af9`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05246638c115aace0ae244236cec9016bac4501e4699e0b5761e13d518f3aa7`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 6.1 MB (6055871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:b12b29108acc7caee0ab23ab7c1191d2861b6bf4761b820569a0bb5519120cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3cccb44b653f9d355429131978d3190d1b78b70f94e13b2cc06e9f7997a5e`

```dockerfile
```

-	Layers:
	-	`sha256:3ae7b6184d4abc32aca3718238c88832fa852fc8a1b082f050f7d291dfde1737`  
		Last Modified: Wed, 08 Oct 2025 22:59:48 GMT  
		Size: 1.3 MB (1270623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7720d5b50178fd0c79f8f0d50307c9837e7c9413280ecc69217fdc55705d6b3f`  
		Last Modified: Wed, 08 Oct 2025 22:59:49 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; ppc64le

```console
$ docker pull irssi@sha256:11ec21937e624e10112a9366a2e39f63804c250cd288519f31d38458aa0c9d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20560595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dfe8eb30ae660e9f6b618bd8acba1eb372978247dff8685fcdb0393231e246`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c17d61a4d1554d280ba28d7252c2f305090eeac61b357dd6b76bd73c43c63`  
		Last Modified: Thu, 09 Oct 2025 00:45:13 GMT  
		Size: 10.6 MB (10595397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26efea3de5b42df966c34855cef32948787b76acb851a4084e3e3ad212766f3`  
		Last Modified: Thu, 09 Oct 2025 00:45:11 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa99ddfbbb8375b453f006a945c8fa07c1ce170fda8448f7b653f0ac29d72c7b`  
		Last Modified: Thu, 09 Oct 2025 00:45:07 GMT  
		Size: 6.2 MB (6231972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:9c4cef9155fe22476444ceb17f379012b0c8b3e5e05a7c96919fa63eff2fdfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179a2005edd691213f7786f101a4bd63364292c1882766e726e961190a7a7a47`

```dockerfile
```

-	Layers:
	-	`sha256:33a5c683cc42bda4a70c31f9d11afeffee44599ee508e945b64f8f0f007364b0`  
		Last Modified: Thu, 09 Oct 2025 01:59:38 GMT  
		Size: 1.3 MB (1268775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ee5b46b5c6c2bdcc6f69f3de81a1779cddf19f1c547cb5807d97cd7e0429e`  
		Last Modified: Thu, 09 Oct 2025 01:59:39 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; riscv64

```console
$ docker pull irssi@sha256:af936cabadda0c93ca3a229f630f7a5f4888f182b0cbb68edba78dbfaf1dd897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19342220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6546997bb677e945cd6914f29dcdd5d93b42fce0ffcc5b7109c0829285bcea25`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90056e842713293c53c6dce4290bfbd298df758358806bd5d3bec46230a89716`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 9.8 MB (9840947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c83cc5e93d426e4646d9cce9fdd7a659215fc178d82320a85f6c6e13ce0939`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486e128aa6ab32a4665c7cdcb3ed936f18c1e8bf06a7a4d7414222f0a89ac9`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 6.0 MB (5985049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:7bdbcb1c990676d35120b16117a0adacceb673203918e2e310ce5e5bb9f8ef01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1819ad33d43cee11f7584b364a2e91ced1b9b8229dea8fc4e7bf7cad969bfe7`

```dockerfile
```

-	Layers:
	-	`sha256:0191fc70832b0a543dfdac6c4787f835b7dd8fd57d9e0b7c1a864173c00c5b5a`  
		Last Modified: Thu, 09 Oct 2025 07:59:31 GMT  
		Size: 1.3 MB (1268771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101fedb5dfade0a1d32aed1260a2c4e061defe2886d8bccdd1cabcc4f65ab848`  
		Last Modified: Thu, 09 Oct 2025 07:59:32 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; s390x

```console
$ docker pull irssi@sha256:f3623b26ebb6e5ca70e89646c7b5dc3cc4923efff13fcf40e13603205b1d2c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20728269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc9af67d43ea3efb18b38b4dd936194a56cde8d7cedf49529c2085f844b996`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a35a93027b47a44ea544d9fee84d01ab7be35185d9c512211141ce9d358b9c`  
		Last Modified: Thu, 09 Oct 2025 00:42:42 GMT  
		Size: 11.0 MB (10953642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054cb0439f6b75b07dcf89d2ae109ef474c8c1ca0e6748b16768e98125bfadd4`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439f567e83e96d3eb1406d4ffb34da86c733b3fc27798542727ad6be641a537`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 6.1 MB (6124398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:033679be33af045692166464cde309c06c55d1e3c2f0f70ff8f5a32a40c138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3b68e4209308a841644a418b0f59ac60f7f2626e13c308ee01fa66528b5f4b`

```dockerfile
```

-	Layers:
	-	`sha256:874c4b424a680cfa6457999c0ce435d96b02cffc5203fa3f92b393d5811628a1`  
		Last Modified: Thu, 09 Oct 2025 01:59:58 GMT  
		Size: 1.3 MB (1268717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586c45ea22dc49613e4d853a8c98ede4e76cc44653d06cf317710f979f305a99`  
		Last Modified: Thu, 09 Oct 2025 01:59:59 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-trixie`

```console
$ docker pull irssi@sha256:f16b9ab6967270a5b2d0745b7f6b9233f6226b9866de8e46ab3f67f20167dde3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4-trixie` - linux; amd64

```console
$ docker pull irssi@sha256:1c3ad0c692729985069dc605f6970c498536ff77cdc28731957a9981bb5cc69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8b5071dd14f9cc7babdbbb92be355488770afbb4baa1dd4193f835544e54d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:18:09 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 04:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 04:18:46 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 04:18:46 GMT
USER user
# Tue, 18 Nov 2025 04:18:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3defe69b9d42ee331ee4997997e0b6950a228ac42a28acb744b2a217802984`  
		Last Modified: Tue, 18 Nov 2025 04:19:08 GMT  
		Size: 19.2 MB (19222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d261d2d2be0daf5812e199043e646cd3b38c72c6a85a46d1aa2664afbbfdab`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb0ce4ebcc67d4eb7b0fd5a6f142adedb46b4a4b5c9f752bb3663092160fd4`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 4.9 MB (4866605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:22bdb7c49ddfaba85497f04c9d268938716f3b3352fe24378d933a7732e8d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d4070dfa4342b3ae917c1f765452b8b31cbfe6c04864d806db24d761ba3c65`

```dockerfile
```

-	Layers:
	-	`sha256:5234daf2a71968c25322c71bfea4cdc75082624fc15fcfa85f68596c0e1e8722`  
		Last Modified: Tue, 18 Nov 2025 06:01:31 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6a5104b772e5ddb76df8ed09e14d2aaf8f4757fd03c65a00ce68904337b081`  
		Last Modified: Tue, 18 Nov 2025 06:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3bfeabfea3f173a6eef66224244f7c8ab79162e4b3e3454b5d7b951b699e6d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce561de65d9ced729b270243f33a9fe650e7088512ea128954c48a408518f61`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:22:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:23:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:23:21 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:23:21 GMT
USER user
# Tue, 18 Nov 2025 02:23:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e77346f90948edf43f33edec1b3c918cc8196b58e71fc74d47eb901d26a7c88`  
		Last Modified: Tue, 18 Nov 2025 02:23:39 GMT  
		Size: 18.3 MB (18286955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20fff4d4c2bb97e0fc743edd41339f9e7f2db5706f958f8419de0227c19fa9`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deede23e33150dccc8ce32f23f864d2a100697bb5c3f5f0d51414ec4913c97f`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 4.7 MB (4709653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:92486d0301f23f7f5fef04e23a1038f9c9c424a3a47ade435591fdd52853f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1456fb2be5b0b7cdc491b833efa2a0ceb4796c5c761a82e6ef643577401e6`

```dockerfile
```

-	Layers:
	-	`sha256:6273392ed72e310ca2593fd6731c533c6f636ed1289f29f728e45fc25e8d45b3`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c338421356fba9d226382ee2864822813fdd13c90654bd98562c53392aa9884f`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6206945589cb5f70880eb627ea43ce5e83dc6b09e69ad976fc69ec0a8a671e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e2dfadf9b6f72f29f6e28ff5885e16008ea991da97c386c12c6effd41ef773`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:24:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:24:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:24:41 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:24:41 GMT
USER user
# Tue, 18 Nov 2025 02:24:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07012b32f4cdf9145076ab6689e96bf750c40d6358ddc6b3d983ed86522093b2`  
		Last Modified: Tue, 18 Nov 2025 02:25:00 GMT  
		Size: 17.9 MB (17909541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317eec7c88d4aa0563b4acdfa018d18e2244d1cd4faaa808233aad6ed8c4eef`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e397c097f4a4f9d07fc0ad13a259eb1c5dc9952ad435619e84f81acd7aa5a`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 4.6 MB (4558582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2807406dbaf53bd4128387747c9380192177098c869b02c4fbc0e079734b4a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912225e9dca4300bbd0be1c71db46f637c20bb0ae39dd56905152d9fd37712e7`

```dockerfile
```

-	Layers:
	-	`sha256:826b1dd7affc3defc30e532bafe21b81af9274fe59f9cb13bc8880b266566410`  
		Last Modified: Tue, 18 Nov 2025 06:01:49 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caba9a457c37510c70d5629f0b91ebfec1b4e1fddabcf69e4581cc62b8efbdf9`  
		Last Modified: Tue, 18 Nov 2025 06:01:51 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0ca154f240d8e55d9139562ed162f6d09ed917369e5d3ac0ef11f4277868a144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494da41086e91ed2e2a5b5a81ed84f81af0313ded1a6a19ca4935a9ed697e260`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:19:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:20:13 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:20:13 GMT
USER user
# Tue, 18 Nov 2025 02:20:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619a9a2c5679b92c7e4905e08f05810e02f68d89d06b10524e21d2583f4ab16`  
		Last Modified: Tue, 18 Nov 2025 02:20:32 GMT  
		Size: 19.0 MB (19049113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494e61b822c7885405295c0e02e3d6f750e57594294fe2d8b997a0632065745d`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84635b25a37fcbf6ec3700e051e040f70178ad0e6880c9c76aeef1ebcfdf275`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 4.8 MB (4781743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6b955f8723ba03a2a30061c1a89c6af489d1442317213524c5594663f9d28695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b845fa96792ab508c1cabce079cc6822b4d3ed51f4ff9cc1486fb4becdb2b9`

```dockerfile
```

-	Layers:
	-	`sha256:1e1288c631711328c43fbd795987044f9c19d6d7ca488586f7d48b2d1bbf9fc9`  
		Last Modified: Tue, 18 Nov 2025 06:01:56 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3627aff8962b25f0eb1a595d760c047d53573e5a83de81ffd5ee43ffde3e283f`  
		Last Modified: Tue, 18 Nov 2025 06:01:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; 386

```console
$ docker pull irssi@sha256:9ca8e0716038e4dbc489c402c36d6bdc49bb1c6dc80a6050371e0ebb63798b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afefadafe5f8e789fb22f477834b8855758beefa989deb19c7f4e79699e5e89`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:17:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:17:16 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:17:16 GMT
USER user
# Tue, 18 Nov 2025 02:17:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2fb43e1b281a402bf774cd8bde6070d229add5d03c870cbfe7c8e16f2cbb7`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 18.7 MB (18740862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6997edee7df4e50b70fa845f324ec76992912dec560143cbead27a7aec43803b`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a3e4cae20c6dc7e982f2a19aa8de8e2b641b6bcc81e72f1bef2930dca363d`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 4.9 MB (4868298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:59d4050c0c1cd29128be910eccf5ea2a035052b836f46e045244c9f64fa4298c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1003b498f9e79e27d0402d3e70dfc68a8d4f2e5fb76327ddf0d269848f164933`

```dockerfile
```

-	Layers:
	-	`sha256:dae334eb70cbeb2210f0f00af9826de6e0af19a4045d45c351ccd063c967c44c`  
		Last Modified: Tue, 18 Nov 2025 06:02:04 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f17fc2c6b6001ffa3a573775d2cbcfc57f6836267cf4f7578260842ada1b7`  
		Last Modified: Tue, 18 Nov 2025 06:02:05 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:459fe708abbb929ace6e5502ac492cb132f84c0e1b80e5a3dd662a7d98b6470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72533238806364f21d117ef1051d9f72e86e6063d9c6683bc210cea47127bda`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 15:03:14 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 15:03:14 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 15:04:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 15:04:50 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 15:04:50 GMT
USER user
# Tue, 18 Nov 2025 15:04:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f858dd24ce7b2766334f11cb720c162ec10dcc1115c24b7c5a2cb933f4732e`  
		Last Modified: Tue, 18 Nov 2025 15:05:24 GMT  
		Size: 19.5 MB (19542803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e87e68a0f54b41f554a220560c01fae4bca1b4bb4b83336d6c6110f750186`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab575b18effe508097b5d8936201a72cd903f95c5c055af70a652fee9591f15f`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 5.1 MB (5097211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:43823b3c76d194b48bf19fd79dde879a47f65352dc638bc93f743de8b5863b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b0fd9dbba87f1d0495d3f376c23a11766edc9e180c9c6afddfacb7df1cbe76`

```dockerfile
```

-	Layers:
	-	`sha256:ebbbdb938672f1b98a9abf9c0267764349f2261c7295ea777971571c28ac293f`  
		Last Modified: Tue, 18 Nov 2025 18:00:17 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae083b6d0624ff996d976b7dfead8f215b20de9aedc3bef84697341f367a4d3`  
		Last Modified: Tue, 18 Nov 2025 18:00:18 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:0a17bc9dc7f1ede0aae4d4035aa269c39fdd3ad059158a3c6a569fa2bf7da8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6a1bc4c5ae216cf035ec48b010768259be2a066ee4ef066bcb9c32d445e4d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 10:01:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:01:44 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 10:08:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 10:08:36 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 10:08:36 GMT
USER user
# Tue, 18 Nov 2025 10:08:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afef2a7493fa326b06e464e36f2a79568e4c5c265515366e193165f0b4d284e`  
		Last Modified: Tue, 18 Nov 2025 10:10:42 GMT  
		Size: 18.5 MB (18549074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026bbe28877d1917f647dacffd37172e95435e1c7e9fbe30a62986bb72cd62b`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 3.3 KB (3337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3d248f54be38451080b4d25093d9df5c1c9efe1175c3cf58494a7e0fd7fe62`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 4.9 MB (4860627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:7b01cdd2258dc9fd9266a05e6cbd264f72886699285f27da4dcfa624dcb82f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb4ae2e3561846a1f14e41a61390911210a0c9ea6b4f9bace7ef57ca7a1303`

```dockerfile
```

-	Layers:
	-	`sha256:5044523627d968ee0b87912ad5e86b6f374ff85ef9a7878ae77c52dcf5581421`  
		Last Modified: Tue, 18 Nov 2025 18:00:24 GMT  
		Size: 5.6 MB (5579680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43863609ed306f6a1f2ac385d2c41ef9efb115640066a4bb3b02043bb96f7158`  
		Last Modified: Tue, 18 Nov 2025 18:00:25 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:da93e9283b14d1092e451a797eb231f916c62509d64042a7ed65617b6ab9c487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b5c6cf33fd166afa65862c57464a7a99d44516a592d7093c9c71058d5008c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:17:58 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:18:33 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:18:33 GMT
USER user
# Tue, 18 Nov 2025 02:18:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce4907214a18511e7c1676f0b93794fa538b6672045daa187e1c681bbd9019`  
		Last Modified: Tue, 18 Nov 2025 02:18:55 GMT  
		Size: 19.8 MB (19759415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dca431fe704652eca13f122842a6232de3a88619e75b4585c55d73ab6784b33`  
		Last Modified: Tue, 18 Nov 2025 02:18:52 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12fa892c886e7110c8b36d26e5b06c87bdfad4dab6e9bf9b746c2887bce206f`  
		Last Modified: Tue, 18 Nov 2025 02:18:53 GMT  
		Size: 4.9 MB (4905870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:9921bed642cdddc5b883e960fbb4efa54a43817af46e8c05c8c59611062a6056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babbc467c5248e09f8d3d0710512a06a92fbd5173a81414b551f82cab3d5d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:a1fee033f27a53ca8a99d5789a2cf1a16782bef7f265384856e2f9c62104fc55`  
		Last Modified: Tue, 18 Nov 2025 06:02:18 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd54ab02d147f06764006021d0881cd166981d03206bbcbfdca3215249d036e1`  
		Last Modified: Tue, 18 Nov 2025 06:02:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:f16b9ab6967270a5b2d0745b7f6b9233f6226b9866de8e46ab3f67f20167dde3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4.5` - linux; amd64

```console
$ docker pull irssi@sha256:1c3ad0c692729985069dc605f6970c498536ff77cdc28731957a9981bb5cc69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8b5071dd14f9cc7babdbbb92be355488770afbb4baa1dd4193f835544e54d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:18:09 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 04:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 04:18:46 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 04:18:46 GMT
USER user
# Tue, 18 Nov 2025 04:18:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3defe69b9d42ee331ee4997997e0b6950a228ac42a28acb744b2a217802984`  
		Last Modified: Tue, 18 Nov 2025 04:19:08 GMT  
		Size: 19.2 MB (19222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d261d2d2be0daf5812e199043e646cd3b38c72c6a85a46d1aa2664afbbfdab`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb0ce4ebcc67d4eb7b0fd5a6f142adedb46b4a4b5c9f752bb3663092160fd4`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 4.9 MB (4866605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:22bdb7c49ddfaba85497f04c9d268938716f3b3352fe24378d933a7732e8d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d4070dfa4342b3ae917c1f765452b8b31cbfe6c04864d806db24d761ba3c65`

```dockerfile
```

-	Layers:
	-	`sha256:5234daf2a71968c25322c71bfea4cdc75082624fc15fcfa85f68596c0e1e8722`  
		Last Modified: Tue, 18 Nov 2025 06:01:31 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6a5104b772e5ddb76df8ed09e14d2aaf8f4757fd03c65a00ce68904337b081`  
		Last Modified: Tue, 18 Nov 2025 06:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3bfeabfea3f173a6eef66224244f7c8ab79162e4b3e3454b5d7b951b699e6d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce561de65d9ced729b270243f33a9fe650e7088512ea128954c48a408518f61`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:22:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:23:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:23:21 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:23:21 GMT
USER user
# Tue, 18 Nov 2025 02:23:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e77346f90948edf43f33edec1b3c918cc8196b58e71fc74d47eb901d26a7c88`  
		Last Modified: Tue, 18 Nov 2025 02:23:39 GMT  
		Size: 18.3 MB (18286955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20fff4d4c2bb97e0fc743edd41339f9e7f2db5706f958f8419de0227c19fa9`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deede23e33150dccc8ce32f23f864d2a100697bb5c3f5f0d51414ec4913c97f`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 4.7 MB (4709653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:92486d0301f23f7f5fef04e23a1038f9c9c424a3a47ade435591fdd52853f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1456fb2be5b0b7cdc491b833efa2a0ceb4796c5c761a82e6ef643577401e6`

```dockerfile
```

-	Layers:
	-	`sha256:6273392ed72e310ca2593fd6731c533c6f636ed1289f29f728e45fc25e8d45b3`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c338421356fba9d226382ee2864822813fdd13c90654bd98562c53392aa9884f`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6206945589cb5f70880eb627ea43ce5e83dc6b09e69ad976fc69ec0a8a671e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e2dfadf9b6f72f29f6e28ff5885e16008ea991da97c386c12c6effd41ef773`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:24:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:24:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:24:41 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:24:41 GMT
USER user
# Tue, 18 Nov 2025 02:24:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07012b32f4cdf9145076ab6689e96bf750c40d6358ddc6b3d983ed86522093b2`  
		Last Modified: Tue, 18 Nov 2025 02:25:00 GMT  
		Size: 17.9 MB (17909541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317eec7c88d4aa0563b4acdfa018d18e2244d1cd4faaa808233aad6ed8c4eef`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e397c097f4a4f9d07fc0ad13a259eb1c5dc9952ad435619e84f81acd7aa5a`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 4.6 MB (4558582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:2807406dbaf53bd4128387747c9380192177098c869b02c4fbc0e079734b4a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912225e9dca4300bbd0be1c71db46f637c20bb0ae39dd56905152d9fd37712e7`

```dockerfile
```

-	Layers:
	-	`sha256:826b1dd7affc3defc30e532bafe21b81af9274fe59f9cb13bc8880b266566410`  
		Last Modified: Tue, 18 Nov 2025 06:01:49 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caba9a457c37510c70d5629f0b91ebfec1b4e1fddabcf69e4581cc62b8efbdf9`  
		Last Modified: Tue, 18 Nov 2025 06:01:51 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0ca154f240d8e55d9139562ed162f6d09ed917369e5d3ac0ef11f4277868a144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494da41086e91ed2e2a5b5a81ed84f81af0313ded1a6a19ca4935a9ed697e260`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:19:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:20:13 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:20:13 GMT
USER user
# Tue, 18 Nov 2025 02:20:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619a9a2c5679b92c7e4905e08f05810e02f68d89d06b10524e21d2583f4ab16`  
		Last Modified: Tue, 18 Nov 2025 02:20:32 GMT  
		Size: 19.0 MB (19049113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494e61b822c7885405295c0e02e3d6f750e57594294fe2d8b997a0632065745d`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84635b25a37fcbf6ec3700e051e040f70178ad0e6880c9c76aeef1ebcfdf275`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 4.8 MB (4781743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:6b955f8723ba03a2a30061c1a89c6af489d1442317213524c5594663f9d28695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b845fa96792ab508c1cabce079cc6822b4d3ed51f4ff9cc1486fb4becdb2b9`

```dockerfile
```

-	Layers:
	-	`sha256:1e1288c631711328c43fbd795987044f9c19d6d7ca488586f7d48b2d1bbf9fc9`  
		Last Modified: Tue, 18 Nov 2025 06:01:56 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3627aff8962b25f0eb1a595d760c047d53573e5a83de81ffd5ee43ffde3e283f`  
		Last Modified: Tue, 18 Nov 2025 06:01:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:9ca8e0716038e4dbc489c402c36d6bdc49bb1c6dc80a6050371e0ebb63798b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afefadafe5f8e789fb22f477834b8855758beefa989deb19c7f4e79699e5e89`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:17:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:17:16 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:17:16 GMT
USER user
# Tue, 18 Nov 2025 02:17:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2fb43e1b281a402bf774cd8bde6070d229add5d03c870cbfe7c8e16f2cbb7`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 18.7 MB (18740862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6997edee7df4e50b70fa845f324ec76992912dec560143cbead27a7aec43803b`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a3e4cae20c6dc7e982f2a19aa8de8e2b641b6bcc81e72f1bef2930dca363d`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 4.9 MB (4868298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:59d4050c0c1cd29128be910eccf5ea2a035052b836f46e045244c9f64fa4298c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1003b498f9e79e27d0402d3e70dfc68a8d4f2e5fb76327ddf0d269848f164933`

```dockerfile
```

-	Layers:
	-	`sha256:dae334eb70cbeb2210f0f00af9826de6e0af19a4045d45c351ccd063c967c44c`  
		Last Modified: Tue, 18 Nov 2025 06:02:04 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f17fc2c6b6001ffa3a573775d2cbcfc57f6836267cf4f7578260842ada1b7`  
		Last Modified: Tue, 18 Nov 2025 06:02:05 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:459fe708abbb929ace6e5502ac492cb132f84c0e1b80e5a3dd662a7d98b6470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72533238806364f21d117ef1051d9f72e86e6063d9c6683bc210cea47127bda`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 15:03:14 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 15:03:14 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 15:04:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 15:04:50 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 15:04:50 GMT
USER user
# Tue, 18 Nov 2025 15:04:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f858dd24ce7b2766334f11cb720c162ec10dcc1115c24b7c5a2cb933f4732e`  
		Last Modified: Tue, 18 Nov 2025 15:05:24 GMT  
		Size: 19.5 MB (19542803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e87e68a0f54b41f554a220560c01fae4bca1b4bb4b83336d6c6110f750186`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab575b18effe508097b5d8936201a72cd903f95c5c055af70a652fee9591f15f`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 5.1 MB (5097211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:43823b3c76d194b48bf19fd79dde879a47f65352dc638bc93f743de8b5863b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b0fd9dbba87f1d0495d3f376c23a11766edc9e180c9c6afddfacb7df1cbe76`

```dockerfile
```

-	Layers:
	-	`sha256:ebbbdb938672f1b98a9abf9c0267764349f2261c7295ea777971571c28ac293f`  
		Last Modified: Tue, 18 Nov 2025 18:00:17 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae083b6d0624ff996d976b7dfead8f215b20de9aedc3bef84697341f367a4d3`  
		Last Modified: Tue, 18 Nov 2025 18:00:18 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; riscv64

```console
$ docker pull irssi@sha256:0a17bc9dc7f1ede0aae4d4035aa269c39fdd3ad059158a3c6a569fa2bf7da8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6a1bc4c5ae216cf035ec48b010768259be2a066ee4ef066bcb9c32d445e4d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 10:01:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:01:44 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 10:08:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 10:08:36 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 10:08:36 GMT
USER user
# Tue, 18 Nov 2025 10:08:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afef2a7493fa326b06e464e36f2a79568e4c5c265515366e193165f0b4d284e`  
		Last Modified: Tue, 18 Nov 2025 10:10:42 GMT  
		Size: 18.5 MB (18549074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026bbe28877d1917f647dacffd37172e95435e1c7e9fbe30a62986bb72cd62b`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 3.3 KB (3337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3d248f54be38451080b4d25093d9df5c1c9efe1175c3cf58494a7e0fd7fe62`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 4.9 MB (4860627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:7b01cdd2258dc9fd9266a05e6cbd264f72886699285f27da4dcfa624dcb82f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb4ae2e3561846a1f14e41a61390911210a0c9ea6b4f9bace7ef57ca7a1303`

```dockerfile
```

-	Layers:
	-	`sha256:5044523627d968ee0b87912ad5e86b6f374ff85ef9a7878ae77c52dcf5581421`  
		Last Modified: Tue, 18 Nov 2025 18:00:24 GMT  
		Size: 5.6 MB (5579680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43863609ed306f6a1f2ac385d2c41ef9efb115640066a4bb3b02043bb96f7158`  
		Last Modified: Tue, 18 Nov 2025 18:00:25 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:da93e9283b14d1092e451a797eb231f916c62509d64042a7ed65617b6ab9c487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b5c6cf33fd166afa65862c57464a7a99d44516a592d7093c9c71058d5008c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:17:58 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:18:33 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:18:33 GMT
USER user
# Tue, 18 Nov 2025 02:18:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce4907214a18511e7c1676f0b93794fa538b6672045daa187e1c681bbd9019`  
		Last Modified: Tue, 18 Nov 2025 02:18:55 GMT  
		Size: 19.8 MB (19759415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dca431fe704652eca13f122842a6232de3a88619e75b4585c55d73ab6784b33`  
		Last Modified: Tue, 18 Nov 2025 02:18:52 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12fa892c886e7110c8b36d26e5b06c87bdfad4dab6e9bf9b746c2887bce206f`  
		Last Modified: Tue, 18 Nov 2025 02:18:53 GMT  
		Size: 4.9 MB (4905870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:9921bed642cdddc5b883e960fbb4efa54a43817af46e8c05c8c59611062a6056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babbc467c5248e09f8d3d0710512a06a92fbd5173a81414b551f82cab3d5d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:a1fee033f27a53ca8a99d5789a2cf1a16782bef7f265384856e2f9c62104fc55`  
		Last Modified: Tue, 18 Nov 2025 06:02:18 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd54ab02d147f06764006021d0881cd166981d03206bbcbfdca3215249d036e1`  
		Last Modified: Tue, 18 Nov 2025 06:02:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:1e663ae10149c0b4d9df663b9da7bb650a58deea6cb49343c8191884eb0ec8ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4.5-alpine` - linux; amd64

```console
$ docker pull irssi@sha256:faf9e4f6be7260cc0682ec1445c6826e0bdcdc63f4a064eb8a981701bb709594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8798df3f4b34c7e6f52a3727072b2c410704453c6794f69663ce299680c47d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e11827177f1c189b726b09341a9159227f1bfd85f6bfa5e738af089ccd47cc`  
		Last Modified: Wed, 08 Oct 2025 22:39:07 GMT  
		Size: 10.4 MB (10396003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6644b44e4c465f7087dbb97380180e75f01380c552303d8a2486f385aad34f35`  
		Last Modified: Wed, 08 Oct 2025 22:39:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b031546d04685e49a4d43b8482a34aaa0e6a3a6d75e947a09671aaf238e1ffc`  
		Last Modified: Wed, 08 Oct 2025 22:39:05 GMT  
		Size: 6.0 MB (5973981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:60dc002a8263e274525a471186038e9a631be6a5c61c1fd9e0ec2accade632f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be809ef2f20f547ecb812fc7251645454e581cc3d872627c003659069a74285e`

```dockerfile
```

-	Layers:
	-	`sha256:7def044fb5b5a27bb8a83fe2e1f6903b88c7090d91d03cc25c2be92d2b115084`  
		Last Modified: Thu, 09 Oct 2025 01:59:25 GMT  
		Size: 1.3 MB (1270668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d745c2ae7ce01c7631e58d7cf581615e9c45ca2b8d31cccaa988c9e5257205`  
		Last Modified: Thu, 09 Oct 2025 01:59:26 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:8dfb08ad7779ab00246287f396771e855c5271e8e67f8fcb68229714505701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4ac8e569bab3223b4cbc8f2ffb5137d951b2efa8fbca448cdef1d3e4925de`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b352b3151cd505887f05e68a9791f679acceebf79736c8050c72db1b5191a`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 9.6 MB (9619615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8386f23106fb9eeab59f6f1e82d6fda32cd5130f7e9240952ab361424133835`  
		Last Modified: Wed, 08 Oct 2025 21:42:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5176e22c73a447407c118250d8b7084c947461ad88e0f8ffba848633ef457d1`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 5.8 MB (5802239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3529f2221a487a696afdfab5dd8793069c4e5153fdd0bbc77b1a10ed59976e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402305c7b183a88a4427e0caf1314f408323bb659aab78e52073f5d4946a814`

```dockerfile
```

-	Layers:
	-	`sha256:40cb74de7dde3071930d2507974b11b96e2a2fcf0dd4cc4063ea7658469d44d0`  
		Last Modified: Wed, 08 Oct 2025 22:59:36 GMT  
		Size: 17.5 KB (17462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1c77198ac74e17d59093ac465b9d5cb18f5cf9b495d394dc7fe1757c6cd43c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18234853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e381f20e12f748a613e6b9d046d4f23726de50b2d6209ee706e26cdc81cd9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355e9f8d23dd7df754d0fc9b69cb593d77843421e4fdc90e0999ac63d910671`  
		Last Modified: Wed, 08 Oct 2025 21:42:22 GMT  
		Size: 9.4 MB (9449582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d327d03f3716120871e15d8a53213e2201fb4c543cff4cfda89d44a362924f5b`  
		Last Modified: Wed, 08 Oct 2025 21:42:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7bac72cbbe13e0d2ca93a7e2045c3cee7af4a9a99e4f4a137d438a669963e`  
		Last Modified: Wed, 08 Oct 2025 21:42:21 GMT  
		Size: 5.6 MB (5562729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:a538097b3d9e95fd66c681e163119ee4fda34648e1138be1471be07765e086b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1291403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd05d16ceb8c11139b6c2e140bdd3f2ff4d48d4eeae0c78b36653e7f2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:66532285c363d95627518c5ee59b11b1d8179d0e9a5459c633c0d02618fed06d`  
		Last Modified: Wed, 08 Oct 2025 22:59:39 GMT  
		Size: 1.3 MB (1273726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f81d5bd314d48e57ad6439aa665accb301d8fa90cf9cfbc734e80cc3932d07`  
		Last Modified: Wed, 08 Oct 2025 22:59:40 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6312b888a6893a7c5bcbfa3b983ab38749f99778b44a99530ef47a5fa8afe92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6748a647916da83e7b32a7fc1af7248d48c18b28e2c35d2403a1aeaba48783`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d53dd86b6f70255a46f81ded3715200f2293ef56b5b5e4a9bd208fe73a5a4`  
		Last Modified: Wed, 08 Oct 2025 21:28:34 GMT  
		Size: 10.4 MB (10358145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35b8acbeb2e8727c286447b6769cf3d016bb4864c5ad35e2e295e2f173749a`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb455678cd1949819acffee4a71aa2ae7f91c1aae58a696c6666455cd9924e53`  
		Last Modified: Wed, 08 Oct 2025 21:28:35 GMT  
		Size: 5.8 MB (5847748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:816e238d7fee6ac073eb8bd4ed99e37a650f1d462c391ae4ae546450436b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f33b353f49dad9739f03717967b6ed81661089b4a5f7503a731715f3f4e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:d1eb3ee699a52f4b20f4604d2e59b51c391ac02eb535317009268ef8a4fc45df`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 1.3 MB (1270772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309170da33d1e1e4b4a1a75c21c0120ff197fc0e4fb56a433d3097dd47cdb44b`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:e66bdc96a17047cd31d803681e0c481fef6963c4d0120511222702e892610149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19616013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9546217ea8e23f6143afa741cd4e2050c708ad5ad67102826bac0bd4e68e070`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ef0d9eddfed06ea09466e4f959f424bd4487ea48914b239e32d9a01ae664b`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 9.9 MB (9940223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1546130b809d653b7ffb8056fabb7cde5c59816ee611d191515f665953378af9`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05246638c115aace0ae244236cec9016bac4501e4699e0b5761e13d518f3aa7`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 6.1 MB (6055871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b12b29108acc7caee0ab23ab7c1191d2861b6bf4761b820569a0bb5519120cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3cccb44b653f9d355429131978d3190d1b78b70f94e13b2cc06e9f7997a5e`

```dockerfile
```

-	Layers:
	-	`sha256:3ae7b6184d4abc32aca3718238c88832fa852fc8a1b082f050f7d291dfde1737`  
		Last Modified: Wed, 08 Oct 2025 22:59:48 GMT  
		Size: 1.3 MB (1270623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7720d5b50178fd0c79f8f0d50307c9837e7c9413280ecc69217fdc55705d6b3f`  
		Last Modified: Wed, 08 Oct 2025 22:59:49 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:11ec21937e624e10112a9366a2e39f63804c250cd288519f31d38458aa0c9d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20560595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dfe8eb30ae660e9f6b618bd8acba1eb372978247dff8685fcdb0393231e246`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c17d61a4d1554d280ba28d7252c2f305090eeac61b357dd6b76bd73c43c63`  
		Last Modified: Thu, 09 Oct 2025 00:45:13 GMT  
		Size: 10.6 MB (10595397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26efea3de5b42df966c34855cef32948787b76acb851a4084e3e3ad212766f3`  
		Last Modified: Thu, 09 Oct 2025 00:45:11 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa99ddfbbb8375b453f006a945c8fa07c1ce170fda8448f7b653f0ac29d72c7b`  
		Last Modified: Thu, 09 Oct 2025 00:45:07 GMT  
		Size: 6.2 MB (6231972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:9c4cef9155fe22476444ceb17f379012b0c8b3e5e05a7c96919fa63eff2fdfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179a2005edd691213f7786f101a4bd63364292c1882766e726e961190a7a7a47`

```dockerfile
```

-	Layers:
	-	`sha256:33a5c683cc42bda4a70c31f9d11afeffee44599ee508e945b64f8f0f007364b0`  
		Last Modified: Thu, 09 Oct 2025 01:59:38 GMT  
		Size: 1.3 MB (1268775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ee5b46b5c6c2bdcc6f69f3de81a1779cddf19f1c547cb5807d97cd7e0429e`  
		Last Modified: Thu, 09 Oct 2025 01:59:39 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:af936cabadda0c93ca3a229f630f7a5f4888f182b0cbb68edba78dbfaf1dd897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19342220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6546997bb677e945cd6914f29dcdd5d93b42fce0ffcc5b7109c0829285bcea25`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90056e842713293c53c6dce4290bfbd298df758358806bd5d3bec46230a89716`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 9.8 MB (9840947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c83cc5e93d426e4646d9cce9fdd7a659215fc178d82320a85f6c6e13ce0939`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486e128aa6ab32a4665c7cdcb3ed936f18c1e8bf06a7a4d7414222f0a89ac9`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 6.0 MB (5985049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:7bdbcb1c990676d35120b16117a0adacceb673203918e2e310ce5e5bb9f8ef01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1819ad33d43cee11f7584b364a2e91ced1b9b8229dea8fc4e7bf7cad969bfe7`

```dockerfile
```

-	Layers:
	-	`sha256:0191fc70832b0a543dfdac6c4787f835b7dd8fd57d9e0b7c1a864173c00c5b5a`  
		Last Modified: Thu, 09 Oct 2025 07:59:31 GMT  
		Size: 1.3 MB (1268771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101fedb5dfade0a1d32aed1260a2c4e061defe2886d8bccdd1cabcc4f65ab848`  
		Last Modified: Thu, 09 Oct 2025 07:59:32 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:f3623b26ebb6e5ca70e89646c7b5dc3cc4923efff13fcf40e13603205b1d2c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20728269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc9af67d43ea3efb18b38b4dd936194a56cde8d7cedf49529c2085f844b996`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a35a93027b47a44ea544d9fee84d01ab7be35185d9c512211141ce9d358b9c`  
		Last Modified: Thu, 09 Oct 2025 00:42:42 GMT  
		Size: 11.0 MB (10953642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054cb0439f6b75b07dcf89d2ae109ef474c8c1ca0e6748b16768e98125bfadd4`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439f567e83e96d3eb1406d4ffb34da86c733b3fc27798542727ad6be641a537`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 6.1 MB (6124398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:033679be33af045692166464cde309c06c55d1e3c2f0f70ff8f5a32a40c138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3b68e4209308a841644a418b0f59ac60f7f2626e13c308ee01fa66528b5f4b`

```dockerfile
```

-	Layers:
	-	`sha256:874c4b424a680cfa6457999c0ce435d96b02cffc5203fa3f92b393d5811628a1`  
		Last Modified: Thu, 09 Oct 2025 01:59:58 GMT  
		Size: 1.3 MB (1268717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586c45ea22dc49613e4d853a8c98ede4e76cc44653d06cf317710f979f305a99`  
		Last Modified: Thu, 09 Oct 2025 01:59:59 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.22`

```console
$ docker pull irssi@sha256:1e663ae10149c0b4d9df663b9da7bb650a58deea6cb49343c8191884eb0ec8ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4.5-alpine3.22` - linux; amd64

```console
$ docker pull irssi@sha256:faf9e4f6be7260cc0682ec1445c6826e0bdcdc63f4a064eb8a981701bb709594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8798df3f4b34c7e6f52a3727072b2c410704453c6794f69663ce299680c47d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e11827177f1c189b726b09341a9159227f1bfd85f6bfa5e738af089ccd47cc`  
		Last Modified: Wed, 08 Oct 2025 22:39:07 GMT  
		Size: 10.4 MB (10396003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6644b44e4c465f7087dbb97380180e75f01380c552303d8a2486f385aad34f35`  
		Last Modified: Wed, 08 Oct 2025 22:39:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b031546d04685e49a4d43b8482a34aaa0e6a3a6d75e947a09671aaf238e1ffc`  
		Last Modified: Wed, 08 Oct 2025 22:39:05 GMT  
		Size: 6.0 MB (5973981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:60dc002a8263e274525a471186038e9a631be6a5c61c1fd9e0ec2accade632f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be809ef2f20f547ecb812fc7251645454e581cc3d872627c003659069a74285e`

```dockerfile
```

-	Layers:
	-	`sha256:7def044fb5b5a27bb8a83fe2e1f6903b88c7090d91d03cc25c2be92d2b115084`  
		Last Modified: Thu, 09 Oct 2025 01:59:25 GMT  
		Size: 1.3 MB (1270668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d745c2ae7ce01c7631e58d7cf581615e9c45ca2b8d31cccaa988c9e5257205`  
		Last Modified: Thu, 09 Oct 2025 01:59:26 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; arm variant v6

```console
$ docker pull irssi@sha256:8dfb08ad7779ab00246287f396771e855c5271e8e67f8fcb68229714505701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4ac8e569bab3223b4cbc8f2ffb5137d951b2efa8fbca448cdef1d3e4925de`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b352b3151cd505887f05e68a9791f679acceebf79736c8050c72db1b5191a`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 9.6 MB (9619615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8386f23106fb9eeab59f6f1e82d6fda32cd5130f7e9240952ab361424133835`  
		Last Modified: Wed, 08 Oct 2025 21:42:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5176e22c73a447407c118250d8b7084c947461ad88e0f8ffba848633ef457d1`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 5.8 MB (5802239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:3529f2221a487a696afdfab5dd8793069c4e5153fdd0bbc77b1a10ed59976e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402305c7b183a88a4427e0caf1314f408323bb659aab78e52073f5d4946a814`

```dockerfile
```

-	Layers:
	-	`sha256:40cb74de7dde3071930d2507974b11b96e2a2fcf0dd4cc4063ea7658469d44d0`  
		Last Modified: Wed, 08 Oct 2025 22:59:36 GMT  
		Size: 17.5 KB (17462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1c77198ac74e17d59093ac465b9d5cb18f5cf9b495d394dc7fe1757c6cd43c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18234853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e381f20e12f748a613e6b9d046d4f23726de50b2d6209ee706e26cdc81cd9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355e9f8d23dd7df754d0fc9b69cb593d77843421e4fdc90e0999ac63d910671`  
		Last Modified: Wed, 08 Oct 2025 21:42:22 GMT  
		Size: 9.4 MB (9449582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d327d03f3716120871e15d8a53213e2201fb4c543cff4cfda89d44a362924f5b`  
		Last Modified: Wed, 08 Oct 2025 21:42:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7bac72cbbe13e0d2ca93a7e2045c3cee7af4a9a99e4f4a137d438a669963e`  
		Last Modified: Wed, 08 Oct 2025 21:42:21 GMT  
		Size: 5.6 MB (5562729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:a538097b3d9e95fd66c681e163119ee4fda34648e1138be1471be07765e086b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1291403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd05d16ceb8c11139b6c2e140bdd3f2ff4d48d4eeae0c78b36653e7f2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:66532285c363d95627518c5ee59b11b1d8179d0e9a5459c633c0d02618fed06d`  
		Last Modified: Wed, 08 Oct 2025 22:59:39 GMT  
		Size: 1.3 MB (1273726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f81d5bd314d48e57ad6439aa665accb301d8fa90cf9cfbc734e80cc3932d07`  
		Last Modified: Wed, 08 Oct 2025 22:59:40 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6312b888a6893a7c5bcbfa3b983ab38749f99778b44a99530ef47a5fa8afe92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6748a647916da83e7b32a7fc1af7248d48c18b28e2c35d2403a1aeaba48783`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d53dd86b6f70255a46f81ded3715200f2293ef56b5b5e4a9bd208fe73a5a4`  
		Last Modified: Wed, 08 Oct 2025 21:28:34 GMT  
		Size: 10.4 MB (10358145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35b8acbeb2e8727c286447b6769cf3d016bb4864c5ad35e2e295e2f173749a`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb455678cd1949819acffee4a71aa2ae7f91c1aae58a696c6666455cd9924e53`  
		Last Modified: Wed, 08 Oct 2025 21:28:35 GMT  
		Size: 5.8 MB (5847748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:816e238d7fee6ac073eb8bd4ed99e37a650f1d462c391ae4ae546450436b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f33b353f49dad9739f03717967b6ed81661089b4a5f7503a731715f3f4e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:d1eb3ee699a52f4b20f4604d2e59b51c391ac02eb535317009268ef8a4fc45df`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 1.3 MB (1270772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309170da33d1e1e4b4a1a75c21c0120ff197fc0e4fb56a433d3097dd47cdb44b`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; 386

```console
$ docker pull irssi@sha256:e66bdc96a17047cd31d803681e0c481fef6963c4d0120511222702e892610149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19616013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9546217ea8e23f6143afa741cd4e2050c708ad5ad67102826bac0bd4e68e070`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ef0d9eddfed06ea09466e4f959f424bd4487ea48914b239e32d9a01ae664b`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 9.9 MB (9940223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1546130b809d653b7ffb8056fabb7cde5c59816ee611d191515f665953378af9`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05246638c115aace0ae244236cec9016bac4501e4699e0b5761e13d518f3aa7`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 6.1 MB (6055871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:b12b29108acc7caee0ab23ab7c1191d2861b6bf4761b820569a0bb5519120cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3cccb44b653f9d355429131978d3190d1b78b70f94e13b2cc06e9f7997a5e`

```dockerfile
```

-	Layers:
	-	`sha256:3ae7b6184d4abc32aca3718238c88832fa852fc8a1b082f050f7d291dfde1737`  
		Last Modified: Wed, 08 Oct 2025 22:59:48 GMT  
		Size: 1.3 MB (1270623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7720d5b50178fd0c79f8f0d50307c9837e7c9413280ecc69217fdc55705d6b3f`  
		Last Modified: Wed, 08 Oct 2025 22:59:49 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; ppc64le

```console
$ docker pull irssi@sha256:11ec21937e624e10112a9366a2e39f63804c250cd288519f31d38458aa0c9d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20560595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dfe8eb30ae660e9f6b618bd8acba1eb372978247dff8685fcdb0393231e246`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c17d61a4d1554d280ba28d7252c2f305090eeac61b357dd6b76bd73c43c63`  
		Last Modified: Thu, 09 Oct 2025 00:45:13 GMT  
		Size: 10.6 MB (10595397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26efea3de5b42df966c34855cef32948787b76acb851a4084e3e3ad212766f3`  
		Last Modified: Thu, 09 Oct 2025 00:45:11 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa99ddfbbb8375b453f006a945c8fa07c1ce170fda8448f7b653f0ac29d72c7b`  
		Last Modified: Thu, 09 Oct 2025 00:45:07 GMT  
		Size: 6.2 MB (6231972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:9c4cef9155fe22476444ceb17f379012b0c8b3e5e05a7c96919fa63eff2fdfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179a2005edd691213f7786f101a4bd63364292c1882766e726e961190a7a7a47`

```dockerfile
```

-	Layers:
	-	`sha256:33a5c683cc42bda4a70c31f9d11afeffee44599ee508e945b64f8f0f007364b0`  
		Last Modified: Thu, 09 Oct 2025 01:59:38 GMT  
		Size: 1.3 MB (1268775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ee5b46b5c6c2bdcc6f69f3de81a1779cddf19f1c547cb5807d97cd7e0429e`  
		Last Modified: Thu, 09 Oct 2025 01:59:39 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; riscv64

```console
$ docker pull irssi@sha256:af936cabadda0c93ca3a229f630f7a5f4888f182b0cbb68edba78dbfaf1dd897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19342220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6546997bb677e945cd6914f29dcdd5d93b42fce0ffcc5b7109c0829285bcea25`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90056e842713293c53c6dce4290bfbd298df758358806bd5d3bec46230a89716`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 9.8 MB (9840947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c83cc5e93d426e4646d9cce9fdd7a659215fc178d82320a85f6c6e13ce0939`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486e128aa6ab32a4665c7cdcb3ed936f18c1e8bf06a7a4d7414222f0a89ac9`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 6.0 MB (5985049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:7bdbcb1c990676d35120b16117a0adacceb673203918e2e310ce5e5bb9f8ef01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1819ad33d43cee11f7584b364a2e91ced1b9b8229dea8fc4e7bf7cad969bfe7`

```dockerfile
```

-	Layers:
	-	`sha256:0191fc70832b0a543dfdac6c4787f835b7dd8fd57d9e0b7c1a864173c00c5b5a`  
		Last Modified: Thu, 09 Oct 2025 07:59:31 GMT  
		Size: 1.3 MB (1268771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101fedb5dfade0a1d32aed1260a2c4e061defe2886d8bccdd1cabcc4f65ab848`  
		Last Modified: Thu, 09 Oct 2025 07:59:32 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; s390x

```console
$ docker pull irssi@sha256:f3623b26ebb6e5ca70e89646c7b5dc3cc4923efff13fcf40e13603205b1d2c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20728269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc9af67d43ea3efb18b38b4dd936194a56cde8d7cedf49529c2085f844b996`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a35a93027b47a44ea544d9fee84d01ab7be35185d9c512211141ce9d358b9c`  
		Last Modified: Thu, 09 Oct 2025 00:42:42 GMT  
		Size: 11.0 MB (10953642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054cb0439f6b75b07dcf89d2ae109ef474c8c1ca0e6748b16768e98125bfadd4`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439f567e83e96d3eb1406d4ffb34da86c733b3fc27798542727ad6be641a537`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 6.1 MB (6124398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:033679be33af045692166464cde309c06c55d1e3c2f0f70ff8f5a32a40c138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3b68e4209308a841644a418b0f59ac60f7f2626e13c308ee01fa66528b5f4b`

```dockerfile
```

-	Layers:
	-	`sha256:874c4b424a680cfa6457999c0ce435d96b02cffc5203fa3f92b393d5811628a1`  
		Last Modified: Thu, 09 Oct 2025 01:59:58 GMT  
		Size: 1.3 MB (1268717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586c45ea22dc49613e4d853a8c98ede4e76cc44653d06cf317710f979f305a99`  
		Last Modified: Thu, 09 Oct 2025 01:59:59 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-trixie`

```console
$ docker pull irssi@sha256:f16b9ab6967270a5b2d0745b7f6b9233f6226b9866de8e46ab3f67f20167dde3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4.5-trixie` - linux; amd64

```console
$ docker pull irssi@sha256:1c3ad0c692729985069dc605f6970c498536ff77cdc28731957a9981bb5cc69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8b5071dd14f9cc7babdbbb92be355488770afbb4baa1dd4193f835544e54d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:18:09 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 04:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 04:18:46 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 04:18:46 GMT
USER user
# Tue, 18 Nov 2025 04:18:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3defe69b9d42ee331ee4997997e0b6950a228ac42a28acb744b2a217802984`  
		Last Modified: Tue, 18 Nov 2025 04:19:08 GMT  
		Size: 19.2 MB (19222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d261d2d2be0daf5812e199043e646cd3b38c72c6a85a46d1aa2664afbbfdab`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb0ce4ebcc67d4eb7b0fd5a6f142adedb46b4a4b5c9f752bb3663092160fd4`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 4.9 MB (4866605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:22bdb7c49ddfaba85497f04c9d268938716f3b3352fe24378d933a7732e8d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d4070dfa4342b3ae917c1f765452b8b31cbfe6c04864d806db24d761ba3c65`

```dockerfile
```

-	Layers:
	-	`sha256:5234daf2a71968c25322c71bfea4cdc75082624fc15fcfa85f68596c0e1e8722`  
		Last Modified: Tue, 18 Nov 2025 06:01:31 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6a5104b772e5ddb76df8ed09e14d2aaf8f4757fd03c65a00ce68904337b081`  
		Last Modified: Tue, 18 Nov 2025 06:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3bfeabfea3f173a6eef66224244f7c8ab79162e4b3e3454b5d7b951b699e6d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce561de65d9ced729b270243f33a9fe650e7088512ea128954c48a408518f61`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:22:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:23:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:23:21 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:23:21 GMT
USER user
# Tue, 18 Nov 2025 02:23:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e77346f90948edf43f33edec1b3c918cc8196b58e71fc74d47eb901d26a7c88`  
		Last Modified: Tue, 18 Nov 2025 02:23:39 GMT  
		Size: 18.3 MB (18286955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20fff4d4c2bb97e0fc743edd41339f9e7f2db5706f958f8419de0227c19fa9`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deede23e33150dccc8ce32f23f864d2a100697bb5c3f5f0d51414ec4913c97f`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 4.7 MB (4709653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:92486d0301f23f7f5fef04e23a1038f9c9c424a3a47ade435591fdd52853f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1456fb2be5b0b7cdc491b833efa2a0ceb4796c5c761a82e6ef643577401e6`

```dockerfile
```

-	Layers:
	-	`sha256:6273392ed72e310ca2593fd6731c533c6f636ed1289f29f728e45fc25e8d45b3`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c338421356fba9d226382ee2864822813fdd13c90654bd98562c53392aa9884f`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6206945589cb5f70880eb627ea43ce5e83dc6b09e69ad976fc69ec0a8a671e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e2dfadf9b6f72f29f6e28ff5885e16008ea991da97c386c12c6effd41ef773`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:24:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:24:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:24:41 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:24:41 GMT
USER user
# Tue, 18 Nov 2025 02:24:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07012b32f4cdf9145076ab6689e96bf750c40d6358ddc6b3d983ed86522093b2`  
		Last Modified: Tue, 18 Nov 2025 02:25:00 GMT  
		Size: 17.9 MB (17909541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317eec7c88d4aa0563b4acdfa018d18e2244d1cd4faaa808233aad6ed8c4eef`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e397c097f4a4f9d07fc0ad13a259eb1c5dc9952ad435619e84f81acd7aa5a`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 4.6 MB (4558582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2807406dbaf53bd4128387747c9380192177098c869b02c4fbc0e079734b4a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912225e9dca4300bbd0be1c71db46f637c20bb0ae39dd56905152d9fd37712e7`

```dockerfile
```

-	Layers:
	-	`sha256:826b1dd7affc3defc30e532bafe21b81af9274fe59f9cb13bc8880b266566410`  
		Last Modified: Tue, 18 Nov 2025 06:01:49 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caba9a457c37510c70d5629f0b91ebfec1b4e1fddabcf69e4581cc62b8efbdf9`  
		Last Modified: Tue, 18 Nov 2025 06:01:51 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0ca154f240d8e55d9139562ed162f6d09ed917369e5d3ac0ef11f4277868a144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494da41086e91ed2e2a5b5a81ed84f81af0313ded1a6a19ca4935a9ed697e260`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:19:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:20:13 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:20:13 GMT
USER user
# Tue, 18 Nov 2025 02:20:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619a9a2c5679b92c7e4905e08f05810e02f68d89d06b10524e21d2583f4ab16`  
		Last Modified: Tue, 18 Nov 2025 02:20:32 GMT  
		Size: 19.0 MB (19049113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494e61b822c7885405295c0e02e3d6f750e57594294fe2d8b997a0632065745d`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84635b25a37fcbf6ec3700e051e040f70178ad0e6880c9c76aeef1ebcfdf275`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 4.8 MB (4781743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6b955f8723ba03a2a30061c1a89c6af489d1442317213524c5594663f9d28695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b845fa96792ab508c1cabce079cc6822b4d3ed51f4ff9cc1486fb4becdb2b9`

```dockerfile
```

-	Layers:
	-	`sha256:1e1288c631711328c43fbd795987044f9c19d6d7ca488586f7d48b2d1bbf9fc9`  
		Last Modified: Tue, 18 Nov 2025 06:01:56 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3627aff8962b25f0eb1a595d760c047d53573e5a83de81ffd5ee43ffde3e283f`  
		Last Modified: Tue, 18 Nov 2025 06:01:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; 386

```console
$ docker pull irssi@sha256:9ca8e0716038e4dbc489c402c36d6bdc49bb1c6dc80a6050371e0ebb63798b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afefadafe5f8e789fb22f477834b8855758beefa989deb19c7f4e79699e5e89`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:17:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:17:16 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:17:16 GMT
USER user
# Tue, 18 Nov 2025 02:17:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2fb43e1b281a402bf774cd8bde6070d229add5d03c870cbfe7c8e16f2cbb7`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 18.7 MB (18740862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6997edee7df4e50b70fa845f324ec76992912dec560143cbead27a7aec43803b`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a3e4cae20c6dc7e982f2a19aa8de8e2b641b6bcc81e72f1bef2930dca363d`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 4.9 MB (4868298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:59d4050c0c1cd29128be910eccf5ea2a035052b836f46e045244c9f64fa4298c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1003b498f9e79e27d0402d3e70dfc68a8d4f2e5fb76327ddf0d269848f164933`

```dockerfile
```

-	Layers:
	-	`sha256:dae334eb70cbeb2210f0f00af9826de6e0af19a4045d45c351ccd063c967c44c`  
		Last Modified: Tue, 18 Nov 2025 06:02:04 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f17fc2c6b6001ffa3a573775d2cbcfc57f6836267cf4f7578260842ada1b7`  
		Last Modified: Tue, 18 Nov 2025 06:02:05 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:459fe708abbb929ace6e5502ac492cb132f84c0e1b80e5a3dd662a7d98b6470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72533238806364f21d117ef1051d9f72e86e6063d9c6683bc210cea47127bda`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 15:03:14 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 15:03:14 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 15:04:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 15:04:50 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 15:04:50 GMT
USER user
# Tue, 18 Nov 2025 15:04:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f858dd24ce7b2766334f11cb720c162ec10dcc1115c24b7c5a2cb933f4732e`  
		Last Modified: Tue, 18 Nov 2025 15:05:24 GMT  
		Size: 19.5 MB (19542803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e87e68a0f54b41f554a220560c01fae4bca1b4bb4b83336d6c6110f750186`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab575b18effe508097b5d8936201a72cd903f95c5c055af70a652fee9591f15f`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 5.1 MB (5097211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:43823b3c76d194b48bf19fd79dde879a47f65352dc638bc93f743de8b5863b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b0fd9dbba87f1d0495d3f376c23a11766edc9e180c9c6afddfacb7df1cbe76`

```dockerfile
```

-	Layers:
	-	`sha256:ebbbdb938672f1b98a9abf9c0267764349f2261c7295ea777971571c28ac293f`  
		Last Modified: Tue, 18 Nov 2025 18:00:17 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae083b6d0624ff996d976b7dfead8f215b20de9aedc3bef84697341f367a4d3`  
		Last Modified: Tue, 18 Nov 2025 18:00:18 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:0a17bc9dc7f1ede0aae4d4035aa269c39fdd3ad059158a3c6a569fa2bf7da8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6a1bc4c5ae216cf035ec48b010768259be2a066ee4ef066bcb9c32d445e4d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 10:01:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:01:44 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 10:08:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 10:08:36 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 10:08:36 GMT
USER user
# Tue, 18 Nov 2025 10:08:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afef2a7493fa326b06e464e36f2a79568e4c5c265515366e193165f0b4d284e`  
		Last Modified: Tue, 18 Nov 2025 10:10:42 GMT  
		Size: 18.5 MB (18549074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026bbe28877d1917f647dacffd37172e95435e1c7e9fbe30a62986bb72cd62b`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 3.3 KB (3337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3d248f54be38451080b4d25093d9df5c1c9efe1175c3cf58494a7e0fd7fe62`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 4.9 MB (4860627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:7b01cdd2258dc9fd9266a05e6cbd264f72886699285f27da4dcfa624dcb82f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb4ae2e3561846a1f14e41a61390911210a0c9ea6b4f9bace7ef57ca7a1303`

```dockerfile
```

-	Layers:
	-	`sha256:5044523627d968ee0b87912ad5e86b6f374ff85ef9a7878ae77c52dcf5581421`  
		Last Modified: Tue, 18 Nov 2025 18:00:24 GMT  
		Size: 5.6 MB (5579680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43863609ed306f6a1f2ac385d2c41ef9efb115640066a4bb3b02043bb96f7158`  
		Last Modified: Tue, 18 Nov 2025 18:00:25 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:da93e9283b14d1092e451a797eb231f916c62509d64042a7ed65617b6ab9c487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b5c6cf33fd166afa65862c57464a7a99d44516a592d7093c9c71058d5008c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:17:58 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:18:33 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:18:33 GMT
USER user
# Tue, 18 Nov 2025 02:18:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce4907214a18511e7c1676f0b93794fa538b6672045daa187e1c681bbd9019`  
		Last Modified: Tue, 18 Nov 2025 02:18:55 GMT  
		Size: 19.8 MB (19759415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dca431fe704652eca13f122842a6232de3a88619e75b4585c55d73ab6784b33`  
		Last Modified: Tue, 18 Nov 2025 02:18:52 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12fa892c886e7110c8b36d26e5b06c87bdfad4dab6e9bf9b746c2887bce206f`  
		Last Modified: Tue, 18 Nov 2025 02:18:53 GMT  
		Size: 4.9 MB (4905870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:9921bed642cdddc5b883e960fbb4efa54a43817af46e8c05c8c59611062a6056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babbc467c5248e09f8d3d0710512a06a92fbd5173a81414b551f82cab3d5d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:a1fee033f27a53ca8a99d5789a2cf1a16782bef7f265384856e2f9c62104fc55`  
		Last Modified: Tue, 18 Nov 2025 06:02:18 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd54ab02d147f06764006021d0881cd166981d03206bbcbfdca3215249d036e1`  
		Last Modified: Tue, 18 Nov 2025 06:02:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:1e663ae10149c0b4d9df663b9da7bb650a58deea6cb49343c8191884eb0ec8ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:alpine` - linux; amd64

```console
$ docker pull irssi@sha256:faf9e4f6be7260cc0682ec1445c6826e0bdcdc63f4a064eb8a981701bb709594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8798df3f4b34c7e6f52a3727072b2c410704453c6794f69663ce299680c47d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e11827177f1c189b726b09341a9159227f1bfd85f6bfa5e738af089ccd47cc`  
		Last Modified: Wed, 08 Oct 2025 22:39:07 GMT  
		Size: 10.4 MB (10396003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6644b44e4c465f7087dbb97380180e75f01380c552303d8a2486f385aad34f35`  
		Last Modified: Wed, 08 Oct 2025 22:39:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b031546d04685e49a4d43b8482a34aaa0e6a3a6d75e947a09671aaf238e1ffc`  
		Last Modified: Wed, 08 Oct 2025 22:39:05 GMT  
		Size: 6.0 MB (5973981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:60dc002a8263e274525a471186038e9a631be6a5c61c1fd9e0ec2accade632f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be809ef2f20f547ecb812fc7251645454e581cc3d872627c003659069a74285e`

```dockerfile
```

-	Layers:
	-	`sha256:7def044fb5b5a27bb8a83fe2e1f6903b88c7090d91d03cc25c2be92d2b115084`  
		Last Modified: Thu, 09 Oct 2025 01:59:25 GMT  
		Size: 1.3 MB (1270668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d745c2ae7ce01c7631e58d7cf581615e9c45ca2b8d31cccaa988c9e5257205`  
		Last Modified: Thu, 09 Oct 2025 01:59:26 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:8dfb08ad7779ab00246287f396771e855c5271e8e67f8fcb68229714505701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4ac8e569bab3223b4cbc8f2ffb5137d951b2efa8fbca448cdef1d3e4925de`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b352b3151cd505887f05e68a9791f679acceebf79736c8050c72db1b5191a`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 9.6 MB (9619615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8386f23106fb9eeab59f6f1e82d6fda32cd5130f7e9240952ab361424133835`  
		Last Modified: Wed, 08 Oct 2025 21:42:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5176e22c73a447407c118250d8b7084c947461ad88e0f8ffba848633ef457d1`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 5.8 MB (5802239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3529f2221a487a696afdfab5dd8793069c4e5153fdd0bbc77b1a10ed59976e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402305c7b183a88a4427e0caf1314f408323bb659aab78e52073f5d4946a814`

```dockerfile
```

-	Layers:
	-	`sha256:40cb74de7dde3071930d2507974b11b96e2a2fcf0dd4cc4063ea7658469d44d0`  
		Last Modified: Wed, 08 Oct 2025 22:59:36 GMT  
		Size: 17.5 KB (17462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1c77198ac74e17d59093ac465b9d5cb18f5cf9b495d394dc7fe1757c6cd43c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18234853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e381f20e12f748a613e6b9d046d4f23726de50b2d6209ee706e26cdc81cd9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355e9f8d23dd7df754d0fc9b69cb593d77843421e4fdc90e0999ac63d910671`  
		Last Modified: Wed, 08 Oct 2025 21:42:22 GMT  
		Size: 9.4 MB (9449582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d327d03f3716120871e15d8a53213e2201fb4c543cff4cfda89d44a362924f5b`  
		Last Modified: Wed, 08 Oct 2025 21:42:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7bac72cbbe13e0d2ca93a7e2045c3cee7af4a9a99e4f4a137d438a669963e`  
		Last Modified: Wed, 08 Oct 2025 21:42:21 GMT  
		Size: 5.6 MB (5562729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:a538097b3d9e95fd66c681e163119ee4fda34648e1138be1471be07765e086b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1291403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd05d16ceb8c11139b6c2e140bdd3f2ff4d48d4eeae0c78b36653e7f2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:66532285c363d95627518c5ee59b11b1d8179d0e9a5459c633c0d02618fed06d`  
		Last Modified: Wed, 08 Oct 2025 22:59:39 GMT  
		Size: 1.3 MB (1273726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f81d5bd314d48e57ad6439aa665accb301d8fa90cf9cfbc734e80cc3932d07`  
		Last Modified: Wed, 08 Oct 2025 22:59:40 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6312b888a6893a7c5bcbfa3b983ab38749f99778b44a99530ef47a5fa8afe92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6748a647916da83e7b32a7fc1af7248d48c18b28e2c35d2403a1aeaba48783`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d53dd86b6f70255a46f81ded3715200f2293ef56b5b5e4a9bd208fe73a5a4`  
		Last Modified: Wed, 08 Oct 2025 21:28:34 GMT  
		Size: 10.4 MB (10358145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35b8acbeb2e8727c286447b6769cf3d016bb4864c5ad35e2e295e2f173749a`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb455678cd1949819acffee4a71aa2ae7f91c1aae58a696c6666455cd9924e53`  
		Last Modified: Wed, 08 Oct 2025 21:28:35 GMT  
		Size: 5.8 MB (5847748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:816e238d7fee6ac073eb8bd4ed99e37a650f1d462c391ae4ae546450436b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f33b353f49dad9739f03717967b6ed81661089b4a5f7503a731715f3f4e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:d1eb3ee699a52f4b20f4604d2e59b51c391ac02eb535317009268ef8a4fc45df`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 1.3 MB (1270772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309170da33d1e1e4b4a1a75c21c0120ff197fc0e4fb56a433d3097dd47cdb44b`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:e66bdc96a17047cd31d803681e0c481fef6963c4d0120511222702e892610149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19616013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9546217ea8e23f6143afa741cd4e2050c708ad5ad67102826bac0bd4e68e070`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ef0d9eddfed06ea09466e4f959f424bd4487ea48914b239e32d9a01ae664b`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 9.9 MB (9940223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1546130b809d653b7ffb8056fabb7cde5c59816ee611d191515f665953378af9`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05246638c115aace0ae244236cec9016bac4501e4699e0b5761e13d518f3aa7`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 6.1 MB (6055871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b12b29108acc7caee0ab23ab7c1191d2861b6bf4761b820569a0bb5519120cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3cccb44b653f9d355429131978d3190d1b78b70f94e13b2cc06e9f7997a5e`

```dockerfile
```

-	Layers:
	-	`sha256:3ae7b6184d4abc32aca3718238c88832fa852fc8a1b082f050f7d291dfde1737`  
		Last Modified: Wed, 08 Oct 2025 22:59:48 GMT  
		Size: 1.3 MB (1270623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7720d5b50178fd0c79f8f0d50307c9837e7c9413280ecc69217fdc55705d6b3f`  
		Last Modified: Wed, 08 Oct 2025 22:59:49 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:11ec21937e624e10112a9366a2e39f63804c250cd288519f31d38458aa0c9d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20560595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dfe8eb30ae660e9f6b618bd8acba1eb372978247dff8685fcdb0393231e246`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c17d61a4d1554d280ba28d7252c2f305090eeac61b357dd6b76bd73c43c63`  
		Last Modified: Thu, 09 Oct 2025 00:45:13 GMT  
		Size: 10.6 MB (10595397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26efea3de5b42df966c34855cef32948787b76acb851a4084e3e3ad212766f3`  
		Last Modified: Thu, 09 Oct 2025 00:45:11 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa99ddfbbb8375b453f006a945c8fa07c1ce170fda8448f7b653f0ac29d72c7b`  
		Last Modified: Thu, 09 Oct 2025 00:45:07 GMT  
		Size: 6.2 MB (6231972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:9c4cef9155fe22476444ceb17f379012b0c8b3e5e05a7c96919fa63eff2fdfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179a2005edd691213f7786f101a4bd63364292c1882766e726e961190a7a7a47`

```dockerfile
```

-	Layers:
	-	`sha256:33a5c683cc42bda4a70c31f9d11afeffee44599ee508e945b64f8f0f007364b0`  
		Last Modified: Thu, 09 Oct 2025 01:59:38 GMT  
		Size: 1.3 MB (1268775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ee5b46b5c6c2bdcc6f69f3de81a1779cddf19f1c547cb5807d97cd7e0429e`  
		Last Modified: Thu, 09 Oct 2025 01:59:39 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:af936cabadda0c93ca3a229f630f7a5f4888f182b0cbb68edba78dbfaf1dd897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19342220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6546997bb677e945cd6914f29dcdd5d93b42fce0ffcc5b7109c0829285bcea25`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90056e842713293c53c6dce4290bfbd298df758358806bd5d3bec46230a89716`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 9.8 MB (9840947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c83cc5e93d426e4646d9cce9fdd7a659215fc178d82320a85f6c6e13ce0939`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486e128aa6ab32a4665c7cdcb3ed936f18c1e8bf06a7a4d7414222f0a89ac9`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 6.0 MB (5985049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:7bdbcb1c990676d35120b16117a0adacceb673203918e2e310ce5e5bb9f8ef01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1819ad33d43cee11f7584b364a2e91ced1b9b8229dea8fc4e7bf7cad969bfe7`

```dockerfile
```

-	Layers:
	-	`sha256:0191fc70832b0a543dfdac6c4787f835b7dd8fd57d9e0b7c1a864173c00c5b5a`  
		Last Modified: Thu, 09 Oct 2025 07:59:31 GMT  
		Size: 1.3 MB (1268771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101fedb5dfade0a1d32aed1260a2c4e061defe2886d8bccdd1cabcc4f65ab848`  
		Last Modified: Thu, 09 Oct 2025 07:59:32 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:f3623b26ebb6e5ca70e89646c7b5dc3cc4923efff13fcf40e13603205b1d2c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20728269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc9af67d43ea3efb18b38b4dd936194a56cde8d7cedf49529c2085f844b996`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a35a93027b47a44ea544d9fee84d01ab7be35185d9c512211141ce9d358b9c`  
		Last Modified: Thu, 09 Oct 2025 00:42:42 GMT  
		Size: 11.0 MB (10953642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054cb0439f6b75b07dcf89d2ae109ef474c8c1ca0e6748b16768e98125bfadd4`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439f567e83e96d3eb1406d4ffb34da86c733b3fc27798542727ad6be641a537`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 6.1 MB (6124398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:033679be33af045692166464cde309c06c55d1e3c2f0f70ff8f5a32a40c138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3b68e4209308a841644a418b0f59ac60f7f2626e13c308ee01fa66528b5f4b`

```dockerfile
```

-	Layers:
	-	`sha256:874c4b424a680cfa6457999c0ce435d96b02cffc5203fa3f92b393d5811628a1`  
		Last Modified: Thu, 09 Oct 2025 01:59:58 GMT  
		Size: 1.3 MB (1268717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586c45ea22dc49613e4d853a8c98ede4e76cc44653d06cf317710f979f305a99`  
		Last Modified: Thu, 09 Oct 2025 01:59:59 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.22`

```console
$ docker pull irssi@sha256:1e663ae10149c0b4d9df663b9da7bb650a58deea6cb49343c8191884eb0ec8ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:alpine3.22` - linux; amd64

```console
$ docker pull irssi@sha256:faf9e4f6be7260cc0682ec1445c6826e0bdcdc63f4a064eb8a981701bb709594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8798df3f4b34c7e6f52a3727072b2c410704453c6794f69663ce299680c47d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e11827177f1c189b726b09341a9159227f1bfd85f6bfa5e738af089ccd47cc`  
		Last Modified: Wed, 08 Oct 2025 22:39:07 GMT  
		Size: 10.4 MB (10396003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6644b44e4c465f7087dbb97380180e75f01380c552303d8a2486f385aad34f35`  
		Last Modified: Wed, 08 Oct 2025 22:39:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b031546d04685e49a4d43b8482a34aaa0e6a3a6d75e947a09671aaf238e1ffc`  
		Last Modified: Wed, 08 Oct 2025 22:39:05 GMT  
		Size: 6.0 MB (5973981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:60dc002a8263e274525a471186038e9a631be6a5c61c1fd9e0ec2accade632f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be809ef2f20f547ecb812fc7251645454e581cc3d872627c003659069a74285e`

```dockerfile
```

-	Layers:
	-	`sha256:7def044fb5b5a27bb8a83fe2e1f6903b88c7090d91d03cc25c2be92d2b115084`  
		Last Modified: Thu, 09 Oct 2025 01:59:25 GMT  
		Size: 1.3 MB (1270668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d745c2ae7ce01c7631e58d7cf581615e9c45ca2b8d31cccaa988c9e5257205`  
		Last Modified: Thu, 09 Oct 2025 01:59:26 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; arm variant v6

```console
$ docker pull irssi@sha256:8dfb08ad7779ab00246287f396771e855c5271e8e67f8fcb68229714505701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4ac8e569bab3223b4cbc8f2ffb5137d951b2efa8fbca448cdef1d3e4925de`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b352b3151cd505887f05e68a9791f679acceebf79736c8050c72db1b5191a`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 9.6 MB (9619615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8386f23106fb9eeab59f6f1e82d6fda32cd5130f7e9240952ab361424133835`  
		Last Modified: Wed, 08 Oct 2025 21:42:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5176e22c73a447407c118250d8b7084c947461ad88e0f8ffba848633ef457d1`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 5.8 MB (5802239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:3529f2221a487a696afdfab5dd8793069c4e5153fdd0bbc77b1a10ed59976e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402305c7b183a88a4427e0caf1314f408323bb659aab78e52073f5d4946a814`

```dockerfile
```

-	Layers:
	-	`sha256:40cb74de7dde3071930d2507974b11b96e2a2fcf0dd4cc4063ea7658469d44d0`  
		Last Modified: Wed, 08 Oct 2025 22:59:36 GMT  
		Size: 17.5 KB (17462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1c77198ac74e17d59093ac465b9d5cb18f5cf9b495d394dc7fe1757c6cd43c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18234853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e381f20e12f748a613e6b9d046d4f23726de50b2d6209ee706e26cdc81cd9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355e9f8d23dd7df754d0fc9b69cb593d77843421e4fdc90e0999ac63d910671`  
		Last Modified: Wed, 08 Oct 2025 21:42:22 GMT  
		Size: 9.4 MB (9449582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d327d03f3716120871e15d8a53213e2201fb4c543cff4cfda89d44a362924f5b`  
		Last Modified: Wed, 08 Oct 2025 21:42:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7bac72cbbe13e0d2ca93a7e2045c3cee7af4a9a99e4f4a137d438a669963e`  
		Last Modified: Wed, 08 Oct 2025 21:42:21 GMT  
		Size: 5.6 MB (5562729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:a538097b3d9e95fd66c681e163119ee4fda34648e1138be1471be07765e086b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1291403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd05d16ceb8c11139b6c2e140bdd3f2ff4d48d4eeae0c78b36653e7f2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:66532285c363d95627518c5ee59b11b1d8179d0e9a5459c633c0d02618fed06d`  
		Last Modified: Wed, 08 Oct 2025 22:59:39 GMT  
		Size: 1.3 MB (1273726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f81d5bd314d48e57ad6439aa665accb301d8fa90cf9cfbc734e80cc3932d07`  
		Last Modified: Wed, 08 Oct 2025 22:59:40 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6312b888a6893a7c5bcbfa3b983ab38749f99778b44a99530ef47a5fa8afe92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6748a647916da83e7b32a7fc1af7248d48c18b28e2c35d2403a1aeaba48783`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d53dd86b6f70255a46f81ded3715200f2293ef56b5b5e4a9bd208fe73a5a4`  
		Last Modified: Wed, 08 Oct 2025 21:28:34 GMT  
		Size: 10.4 MB (10358145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35b8acbeb2e8727c286447b6769cf3d016bb4864c5ad35e2e295e2f173749a`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb455678cd1949819acffee4a71aa2ae7f91c1aae58a696c6666455cd9924e53`  
		Last Modified: Wed, 08 Oct 2025 21:28:35 GMT  
		Size: 5.8 MB (5847748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:816e238d7fee6ac073eb8bd4ed99e37a650f1d462c391ae4ae546450436b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f33b353f49dad9739f03717967b6ed81661089b4a5f7503a731715f3f4e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:d1eb3ee699a52f4b20f4604d2e59b51c391ac02eb535317009268ef8a4fc45df`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 1.3 MB (1270772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309170da33d1e1e4b4a1a75c21c0120ff197fc0e4fb56a433d3097dd47cdb44b`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; 386

```console
$ docker pull irssi@sha256:e66bdc96a17047cd31d803681e0c481fef6963c4d0120511222702e892610149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19616013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9546217ea8e23f6143afa741cd4e2050c708ad5ad67102826bac0bd4e68e070`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ef0d9eddfed06ea09466e4f959f424bd4487ea48914b239e32d9a01ae664b`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 9.9 MB (9940223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1546130b809d653b7ffb8056fabb7cde5c59816ee611d191515f665953378af9`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05246638c115aace0ae244236cec9016bac4501e4699e0b5761e13d518f3aa7`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 6.1 MB (6055871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:b12b29108acc7caee0ab23ab7c1191d2861b6bf4761b820569a0bb5519120cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3cccb44b653f9d355429131978d3190d1b78b70f94e13b2cc06e9f7997a5e`

```dockerfile
```

-	Layers:
	-	`sha256:3ae7b6184d4abc32aca3718238c88832fa852fc8a1b082f050f7d291dfde1737`  
		Last Modified: Wed, 08 Oct 2025 22:59:48 GMT  
		Size: 1.3 MB (1270623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7720d5b50178fd0c79f8f0d50307c9837e7c9413280ecc69217fdc55705d6b3f`  
		Last Modified: Wed, 08 Oct 2025 22:59:49 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; ppc64le

```console
$ docker pull irssi@sha256:11ec21937e624e10112a9366a2e39f63804c250cd288519f31d38458aa0c9d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20560595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dfe8eb30ae660e9f6b618bd8acba1eb372978247dff8685fcdb0393231e246`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c17d61a4d1554d280ba28d7252c2f305090eeac61b357dd6b76bd73c43c63`  
		Last Modified: Thu, 09 Oct 2025 00:45:13 GMT  
		Size: 10.6 MB (10595397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26efea3de5b42df966c34855cef32948787b76acb851a4084e3e3ad212766f3`  
		Last Modified: Thu, 09 Oct 2025 00:45:11 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa99ddfbbb8375b453f006a945c8fa07c1ce170fda8448f7b653f0ac29d72c7b`  
		Last Modified: Thu, 09 Oct 2025 00:45:07 GMT  
		Size: 6.2 MB (6231972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:9c4cef9155fe22476444ceb17f379012b0c8b3e5e05a7c96919fa63eff2fdfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179a2005edd691213f7786f101a4bd63364292c1882766e726e961190a7a7a47`

```dockerfile
```

-	Layers:
	-	`sha256:33a5c683cc42bda4a70c31f9d11afeffee44599ee508e945b64f8f0f007364b0`  
		Last Modified: Thu, 09 Oct 2025 01:59:38 GMT  
		Size: 1.3 MB (1268775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ee5b46b5c6c2bdcc6f69f3de81a1779cddf19f1c547cb5807d97cd7e0429e`  
		Last Modified: Thu, 09 Oct 2025 01:59:39 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; riscv64

```console
$ docker pull irssi@sha256:af936cabadda0c93ca3a229f630f7a5f4888f182b0cbb68edba78dbfaf1dd897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19342220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6546997bb677e945cd6914f29dcdd5d93b42fce0ffcc5b7109c0829285bcea25`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90056e842713293c53c6dce4290bfbd298df758358806bd5d3bec46230a89716`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 9.8 MB (9840947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c83cc5e93d426e4646d9cce9fdd7a659215fc178d82320a85f6c6e13ce0939`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486e128aa6ab32a4665c7cdcb3ed936f18c1e8bf06a7a4d7414222f0a89ac9`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 6.0 MB (5985049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:7bdbcb1c990676d35120b16117a0adacceb673203918e2e310ce5e5bb9f8ef01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1819ad33d43cee11f7584b364a2e91ced1b9b8229dea8fc4e7bf7cad969bfe7`

```dockerfile
```

-	Layers:
	-	`sha256:0191fc70832b0a543dfdac6c4787f835b7dd8fd57d9e0b7c1a864173c00c5b5a`  
		Last Modified: Thu, 09 Oct 2025 07:59:31 GMT  
		Size: 1.3 MB (1268771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101fedb5dfade0a1d32aed1260a2c4e061defe2886d8bccdd1cabcc4f65ab848`  
		Last Modified: Thu, 09 Oct 2025 07:59:32 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; s390x

```console
$ docker pull irssi@sha256:f3623b26ebb6e5ca70e89646c7b5dc3cc4923efff13fcf40e13603205b1d2c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20728269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc9af67d43ea3efb18b38b4dd936194a56cde8d7cedf49529c2085f844b996`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a35a93027b47a44ea544d9fee84d01ab7be35185d9c512211141ce9d358b9c`  
		Last Modified: Thu, 09 Oct 2025 00:42:42 GMT  
		Size: 11.0 MB (10953642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054cb0439f6b75b07dcf89d2ae109ef474c8c1ca0e6748b16768e98125bfadd4`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439f567e83e96d3eb1406d4ffb34da86c733b3fc27798542727ad6be641a537`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 6.1 MB (6124398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:033679be33af045692166464cde309c06c55d1e3c2f0f70ff8f5a32a40c138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3b68e4209308a841644a418b0f59ac60f7f2626e13c308ee01fa66528b5f4b`

```dockerfile
```

-	Layers:
	-	`sha256:874c4b424a680cfa6457999c0ce435d96b02cffc5203fa3f92b393d5811628a1`  
		Last Modified: Thu, 09 Oct 2025 01:59:58 GMT  
		Size: 1.3 MB (1268717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586c45ea22dc49613e4d853a8c98ede4e76cc44653d06cf317710f979f305a99`  
		Last Modified: Thu, 09 Oct 2025 01:59:59 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:f16b9ab6967270a5b2d0745b7f6b9233f6226b9866de8e46ab3f67f20167dde3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:latest` - linux; amd64

```console
$ docker pull irssi@sha256:1c3ad0c692729985069dc605f6970c498536ff77cdc28731957a9981bb5cc69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8b5071dd14f9cc7babdbbb92be355488770afbb4baa1dd4193f835544e54d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:18:09 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 04:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 04:18:46 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 04:18:46 GMT
USER user
# Tue, 18 Nov 2025 04:18:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3defe69b9d42ee331ee4997997e0b6950a228ac42a28acb744b2a217802984`  
		Last Modified: Tue, 18 Nov 2025 04:19:08 GMT  
		Size: 19.2 MB (19222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d261d2d2be0daf5812e199043e646cd3b38c72c6a85a46d1aa2664afbbfdab`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb0ce4ebcc67d4eb7b0fd5a6f142adedb46b4a4b5c9f752bb3663092160fd4`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 4.9 MB (4866605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:22bdb7c49ddfaba85497f04c9d268938716f3b3352fe24378d933a7732e8d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d4070dfa4342b3ae917c1f765452b8b31cbfe6c04864d806db24d761ba3c65`

```dockerfile
```

-	Layers:
	-	`sha256:5234daf2a71968c25322c71bfea4cdc75082624fc15fcfa85f68596c0e1e8722`  
		Last Modified: Tue, 18 Nov 2025 06:01:31 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6a5104b772e5ddb76df8ed09e14d2aaf8f4757fd03c65a00ce68904337b081`  
		Last Modified: Tue, 18 Nov 2025 06:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3bfeabfea3f173a6eef66224244f7c8ab79162e4b3e3454b5d7b951b699e6d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce561de65d9ced729b270243f33a9fe650e7088512ea128954c48a408518f61`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:22:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:23:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:23:21 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:23:21 GMT
USER user
# Tue, 18 Nov 2025 02:23:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e77346f90948edf43f33edec1b3c918cc8196b58e71fc74d47eb901d26a7c88`  
		Last Modified: Tue, 18 Nov 2025 02:23:39 GMT  
		Size: 18.3 MB (18286955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20fff4d4c2bb97e0fc743edd41339f9e7f2db5706f958f8419de0227c19fa9`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deede23e33150dccc8ce32f23f864d2a100697bb5c3f5f0d51414ec4913c97f`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 4.7 MB (4709653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:92486d0301f23f7f5fef04e23a1038f9c9c424a3a47ade435591fdd52853f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1456fb2be5b0b7cdc491b833efa2a0ceb4796c5c761a82e6ef643577401e6`

```dockerfile
```

-	Layers:
	-	`sha256:6273392ed72e310ca2593fd6731c533c6f636ed1289f29f728e45fc25e8d45b3`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c338421356fba9d226382ee2864822813fdd13c90654bd98562c53392aa9884f`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6206945589cb5f70880eb627ea43ce5e83dc6b09e69ad976fc69ec0a8a671e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e2dfadf9b6f72f29f6e28ff5885e16008ea991da97c386c12c6effd41ef773`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:24:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:24:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:24:41 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:24:41 GMT
USER user
# Tue, 18 Nov 2025 02:24:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07012b32f4cdf9145076ab6689e96bf750c40d6358ddc6b3d983ed86522093b2`  
		Last Modified: Tue, 18 Nov 2025 02:25:00 GMT  
		Size: 17.9 MB (17909541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317eec7c88d4aa0563b4acdfa018d18e2244d1cd4faaa808233aad6ed8c4eef`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e397c097f4a4f9d07fc0ad13a259eb1c5dc9952ad435619e84f81acd7aa5a`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 4.6 MB (4558582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:2807406dbaf53bd4128387747c9380192177098c869b02c4fbc0e079734b4a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912225e9dca4300bbd0be1c71db46f637c20bb0ae39dd56905152d9fd37712e7`

```dockerfile
```

-	Layers:
	-	`sha256:826b1dd7affc3defc30e532bafe21b81af9274fe59f9cb13bc8880b266566410`  
		Last Modified: Tue, 18 Nov 2025 06:01:49 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caba9a457c37510c70d5629f0b91ebfec1b4e1fddabcf69e4581cc62b8efbdf9`  
		Last Modified: Tue, 18 Nov 2025 06:01:51 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0ca154f240d8e55d9139562ed162f6d09ed917369e5d3ac0ef11f4277868a144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494da41086e91ed2e2a5b5a81ed84f81af0313ded1a6a19ca4935a9ed697e260`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:19:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:20:13 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:20:13 GMT
USER user
# Tue, 18 Nov 2025 02:20:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619a9a2c5679b92c7e4905e08f05810e02f68d89d06b10524e21d2583f4ab16`  
		Last Modified: Tue, 18 Nov 2025 02:20:32 GMT  
		Size: 19.0 MB (19049113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494e61b822c7885405295c0e02e3d6f750e57594294fe2d8b997a0632065745d`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84635b25a37fcbf6ec3700e051e040f70178ad0e6880c9c76aeef1ebcfdf275`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 4.8 MB (4781743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:6b955f8723ba03a2a30061c1a89c6af489d1442317213524c5594663f9d28695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b845fa96792ab508c1cabce079cc6822b4d3ed51f4ff9cc1486fb4becdb2b9`

```dockerfile
```

-	Layers:
	-	`sha256:1e1288c631711328c43fbd795987044f9c19d6d7ca488586f7d48b2d1bbf9fc9`  
		Last Modified: Tue, 18 Nov 2025 06:01:56 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3627aff8962b25f0eb1a595d760c047d53573e5a83de81ffd5ee43ffde3e283f`  
		Last Modified: Tue, 18 Nov 2025 06:01:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:9ca8e0716038e4dbc489c402c36d6bdc49bb1c6dc80a6050371e0ebb63798b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afefadafe5f8e789fb22f477834b8855758beefa989deb19c7f4e79699e5e89`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:17:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:17:16 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:17:16 GMT
USER user
# Tue, 18 Nov 2025 02:17:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2fb43e1b281a402bf774cd8bde6070d229add5d03c870cbfe7c8e16f2cbb7`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 18.7 MB (18740862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6997edee7df4e50b70fa845f324ec76992912dec560143cbead27a7aec43803b`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a3e4cae20c6dc7e982f2a19aa8de8e2b641b6bcc81e72f1bef2930dca363d`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 4.9 MB (4868298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:59d4050c0c1cd29128be910eccf5ea2a035052b836f46e045244c9f64fa4298c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1003b498f9e79e27d0402d3e70dfc68a8d4f2e5fb76327ddf0d269848f164933`

```dockerfile
```

-	Layers:
	-	`sha256:dae334eb70cbeb2210f0f00af9826de6e0af19a4045d45c351ccd063c967c44c`  
		Last Modified: Tue, 18 Nov 2025 06:02:04 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f17fc2c6b6001ffa3a573775d2cbcfc57f6836267cf4f7578260842ada1b7`  
		Last Modified: Tue, 18 Nov 2025 06:02:05 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:459fe708abbb929ace6e5502ac492cb132f84c0e1b80e5a3dd662a7d98b6470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72533238806364f21d117ef1051d9f72e86e6063d9c6683bc210cea47127bda`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 15:03:14 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 15:03:14 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 15:04:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 15:04:50 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 15:04:50 GMT
USER user
# Tue, 18 Nov 2025 15:04:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f858dd24ce7b2766334f11cb720c162ec10dcc1115c24b7c5a2cb933f4732e`  
		Last Modified: Tue, 18 Nov 2025 15:05:24 GMT  
		Size: 19.5 MB (19542803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e87e68a0f54b41f554a220560c01fae4bca1b4bb4b83336d6c6110f750186`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab575b18effe508097b5d8936201a72cd903f95c5c055af70a652fee9591f15f`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 5.1 MB (5097211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:43823b3c76d194b48bf19fd79dde879a47f65352dc638bc93f743de8b5863b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b0fd9dbba87f1d0495d3f376c23a11766edc9e180c9c6afddfacb7df1cbe76`

```dockerfile
```

-	Layers:
	-	`sha256:ebbbdb938672f1b98a9abf9c0267764349f2261c7295ea777971571c28ac293f`  
		Last Modified: Tue, 18 Nov 2025 18:00:17 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae083b6d0624ff996d976b7dfead8f215b20de9aedc3bef84697341f367a4d3`  
		Last Modified: Tue, 18 Nov 2025 18:00:18 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; riscv64

```console
$ docker pull irssi@sha256:0a17bc9dc7f1ede0aae4d4035aa269c39fdd3ad059158a3c6a569fa2bf7da8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6a1bc4c5ae216cf035ec48b010768259be2a066ee4ef066bcb9c32d445e4d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 10:01:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:01:44 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 10:08:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 10:08:36 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 10:08:36 GMT
USER user
# Tue, 18 Nov 2025 10:08:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afef2a7493fa326b06e464e36f2a79568e4c5c265515366e193165f0b4d284e`  
		Last Modified: Tue, 18 Nov 2025 10:10:42 GMT  
		Size: 18.5 MB (18549074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026bbe28877d1917f647dacffd37172e95435e1c7e9fbe30a62986bb72cd62b`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 3.3 KB (3337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3d248f54be38451080b4d25093d9df5c1c9efe1175c3cf58494a7e0fd7fe62`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 4.9 MB (4860627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:7b01cdd2258dc9fd9266a05e6cbd264f72886699285f27da4dcfa624dcb82f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb4ae2e3561846a1f14e41a61390911210a0c9ea6b4f9bace7ef57ca7a1303`

```dockerfile
```

-	Layers:
	-	`sha256:5044523627d968ee0b87912ad5e86b6f374ff85ef9a7878ae77c52dcf5581421`  
		Last Modified: Tue, 18 Nov 2025 18:00:24 GMT  
		Size: 5.6 MB (5579680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43863609ed306f6a1f2ac385d2c41ef9efb115640066a4bb3b02043bb96f7158`  
		Last Modified: Tue, 18 Nov 2025 18:00:25 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:da93e9283b14d1092e451a797eb231f916c62509d64042a7ed65617b6ab9c487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b5c6cf33fd166afa65862c57464a7a99d44516a592d7093c9c71058d5008c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:17:58 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:18:33 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:18:33 GMT
USER user
# Tue, 18 Nov 2025 02:18:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce4907214a18511e7c1676f0b93794fa538b6672045daa187e1c681bbd9019`  
		Last Modified: Tue, 18 Nov 2025 02:18:55 GMT  
		Size: 19.8 MB (19759415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dca431fe704652eca13f122842a6232de3a88619e75b4585c55d73ab6784b33`  
		Last Modified: Tue, 18 Nov 2025 02:18:52 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12fa892c886e7110c8b36d26e5b06c87bdfad4dab6e9bf9b746c2887bce206f`  
		Last Modified: Tue, 18 Nov 2025 02:18:53 GMT  
		Size: 4.9 MB (4905870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:9921bed642cdddc5b883e960fbb4efa54a43817af46e8c05c8c59611062a6056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babbc467c5248e09f8d3d0710512a06a92fbd5173a81414b551f82cab3d5d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:a1fee033f27a53ca8a99d5789a2cf1a16782bef7f265384856e2f9c62104fc55`  
		Last Modified: Tue, 18 Nov 2025 06:02:18 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd54ab02d147f06764006021d0881cd166981d03206bbcbfdca3215249d036e1`  
		Last Modified: Tue, 18 Nov 2025 06:02:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:trixie`

```console
$ docker pull irssi@sha256:f16b9ab6967270a5b2d0745b7f6b9233f6226b9866de8e46ab3f67f20167dde3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:trixie` - linux; amd64

```console
$ docker pull irssi@sha256:1c3ad0c692729985069dc605f6970c498536ff77cdc28731957a9981bb5cc69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8b5071dd14f9cc7babdbbb92be355488770afbb4baa1dd4193f835544e54d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:18:09 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 04:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 04:18:46 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 04:18:46 GMT
USER user
# Tue, 18 Nov 2025 04:18:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3defe69b9d42ee331ee4997997e0b6950a228ac42a28acb744b2a217802984`  
		Last Modified: Tue, 18 Nov 2025 04:19:08 GMT  
		Size: 19.2 MB (19222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d261d2d2be0daf5812e199043e646cd3b38c72c6a85a46d1aa2664afbbfdab`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb0ce4ebcc67d4eb7b0fd5a6f142adedb46b4a4b5c9f752bb3663092160fd4`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 4.9 MB (4866605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:22bdb7c49ddfaba85497f04c9d268938716f3b3352fe24378d933a7732e8d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d4070dfa4342b3ae917c1f765452b8b31cbfe6c04864d806db24d761ba3c65`

```dockerfile
```

-	Layers:
	-	`sha256:5234daf2a71968c25322c71bfea4cdc75082624fc15fcfa85f68596c0e1e8722`  
		Last Modified: Tue, 18 Nov 2025 06:01:31 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6a5104b772e5ddb76df8ed09e14d2aaf8f4757fd03c65a00ce68904337b081`  
		Last Modified: Tue, 18 Nov 2025 06:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3bfeabfea3f173a6eef66224244f7c8ab79162e4b3e3454b5d7b951b699e6d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce561de65d9ced729b270243f33a9fe650e7088512ea128954c48a408518f61`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:22:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:23:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:23:21 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:23:21 GMT
USER user
# Tue, 18 Nov 2025 02:23:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e77346f90948edf43f33edec1b3c918cc8196b58e71fc74d47eb901d26a7c88`  
		Last Modified: Tue, 18 Nov 2025 02:23:39 GMT  
		Size: 18.3 MB (18286955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20fff4d4c2bb97e0fc743edd41339f9e7f2db5706f958f8419de0227c19fa9`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deede23e33150dccc8ce32f23f864d2a100697bb5c3f5f0d51414ec4913c97f`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 4.7 MB (4709653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:92486d0301f23f7f5fef04e23a1038f9c9c424a3a47ade435591fdd52853f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1456fb2be5b0b7cdc491b833efa2a0ceb4796c5c761a82e6ef643577401e6`

```dockerfile
```

-	Layers:
	-	`sha256:6273392ed72e310ca2593fd6731c533c6f636ed1289f29f728e45fc25e8d45b3`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c338421356fba9d226382ee2864822813fdd13c90654bd98562c53392aa9884f`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6206945589cb5f70880eb627ea43ce5e83dc6b09e69ad976fc69ec0a8a671e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e2dfadf9b6f72f29f6e28ff5885e16008ea991da97c386c12c6effd41ef773`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:24:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:24:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:24:41 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:24:41 GMT
USER user
# Tue, 18 Nov 2025 02:24:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07012b32f4cdf9145076ab6689e96bf750c40d6358ddc6b3d983ed86522093b2`  
		Last Modified: Tue, 18 Nov 2025 02:25:00 GMT  
		Size: 17.9 MB (17909541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317eec7c88d4aa0563b4acdfa018d18e2244d1cd4faaa808233aad6ed8c4eef`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e397c097f4a4f9d07fc0ad13a259eb1c5dc9952ad435619e84f81acd7aa5a`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 4.6 MB (4558582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2807406dbaf53bd4128387747c9380192177098c869b02c4fbc0e079734b4a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912225e9dca4300bbd0be1c71db46f637c20bb0ae39dd56905152d9fd37712e7`

```dockerfile
```

-	Layers:
	-	`sha256:826b1dd7affc3defc30e532bafe21b81af9274fe59f9cb13bc8880b266566410`  
		Last Modified: Tue, 18 Nov 2025 06:01:49 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caba9a457c37510c70d5629f0b91ebfec1b4e1fddabcf69e4581cc62b8efbdf9`  
		Last Modified: Tue, 18 Nov 2025 06:01:51 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0ca154f240d8e55d9139562ed162f6d09ed917369e5d3ac0ef11f4277868a144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494da41086e91ed2e2a5b5a81ed84f81af0313ded1a6a19ca4935a9ed697e260`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:19:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:20:13 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:20:13 GMT
USER user
# Tue, 18 Nov 2025 02:20:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619a9a2c5679b92c7e4905e08f05810e02f68d89d06b10524e21d2583f4ab16`  
		Last Modified: Tue, 18 Nov 2025 02:20:32 GMT  
		Size: 19.0 MB (19049113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494e61b822c7885405295c0e02e3d6f750e57594294fe2d8b997a0632065745d`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84635b25a37fcbf6ec3700e051e040f70178ad0e6880c9c76aeef1ebcfdf275`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 4.8 MB (4781743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6b955f8723ba03a2a30061c1a89c6af489d1442317213524c5594663f9d28695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b845fa96792ab508c1cabce079cc6822b4d3ed51f4ff9cc1486fb4becdb2b9`

```dockerfile
```

-	Layers:
	-	`sha256:1e1288c631711328c43fbd795987044f9c19d6d7ca488586f7d48b2d1bbf9fc9`  
		Last Modified: Tue, 18 Nov 2025 06:01:56 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3627aff8962b25f0eb1a595d760c047d53573e5a83de81ffd5ee43ffde3e283f`  
		Last Modified: Tue, 18 Nov 2025 06:01:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; 386

```console
$ docker pull irssi@sha256:9ca8e0716038e4dbc489c402c36d6bdc49bb1c6dc80a6050371e0ebb63798b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afefadafe5f8e789fb22f477834b8855758beefa989deb19c7f4e79699e5e89`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:17:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:17:16 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:17:16 GMT
USER user
# Tue, 18 Nov 2025 02:17:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2fb43e1b281a402bf774cd8bde6070d229add5d03c870cbfe7c8e16f2cbb7`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 18.7 MB (18740862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6997edee7df4e50b70fa845f324ec76992912dec560143cbead27a7aec43803b`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a3e4cae20c6dc7e982f2a19aa8de8e2b641b6bcc81e72f1bef2930dca363d`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 4.9 MB (4868298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:59d4050c0c1cd29128be910eccf5ea2a035052b836f46e045244c9f64fa4298c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1003b498f9e79e27d0402d3e70dfc68a8d4f2e5fb76327ddf0d269848f164933`

```dockerfile
```

-	Layers:
	-	`sha256:dae334eb70cbeb2210f0f00af9826de6e0af19a4045d45c351ccd063c967c44c`  
		Last Modified: Tue, 18 Nov 2025 06:02:04 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f17fc2c6b6001ffa3a573775d2cbcfc57f6836267cf4f7578260842ada1b7`  
		Last Modified: Tue, 18 Nov 2025 06:02:05 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:459fe708abbb929ace6e5502ac492cb132f84c0e1b80e5a3dd662a7d98b6470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72533238806364f21d117ef1051d9f72e86e6063d9c6683bc210cea47127bda`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 15:03:14 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 15:03:14 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 15:04:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 15:04:50 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 15:04:50 GMT
USER user
# Tue, 18 Nov 2025 15:04:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f858dd24ce7b2766334f11cb720c162ec10dcc1115c24b7c5a2cb933f4732e`  
		Last Modified: Tue, 18 Nov 2025 15:05:24 GMT  
		Size: 19.5 MB (19542803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e87e68a0f54b41f554a220560c01fae4bca1b4bb4b83336d6c6110f750186`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab575b18effe508097b5d8936201a72cd903f95c5c055af70a652fee9591f15f`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 5.1 MB (5097211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:43823b3c76d194b48bf19fd79dde879a47f65352dc638bc93f743de8b5863b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b0fd9dbba87f1d0495d3f376c23a11766edc9e180c9c6afddfacb7df1cbe76`

```dockerfile
```

-	Layers:
	-	`sha256:ebbbdb938672f1b98a9abf9c0267764349f2261c7295ea777971571c28ac293f`  
		Last Modified: Tue, 18 Nov 2025 18:00:17 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae083b6d0624ff996d976b7dfead8f215b20de9aedc3bef84697341f367a4d3`  
		Last Modified: Tue, 18 Nov 2025 18:00:18 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:0a17bc9dc7f1ede0aae4d4035aa269c39fdd3ad059158a3c6a569fa2bf7da8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6a1bc4c5ae216cf035ec48b010768259be2a066ee4ef066bcb9c32d445e4d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 10:01:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:01:44 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 10:08:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 10:08:36 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 10:08:36 GMT
USER user
# Tue, 18 Nov 2025 10:08:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afef2a7493fa326b06e464e36f2a79568e4c5c265515366e193165f0b4d284e`  
		Last Modified: Tue, 18 Nov 2025 10:10:42 GMT  
		Size: 18.5 MB (18549074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026bbe28877d1917f647dacffd37172e95435e1c7e9fbe30a62986bb72cd62b`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 3.3 KB (3337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3d248f54be38451080b4d25093d9df5c1c9efe1175c3cf58494a7e0fd7fe62`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 4.9 MB (4860627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:7b01cdd2258dc9fd9266a05e6cbd264f72886699285f27da4dcfa624dcb82f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb4ae2e3561846a1f14e41a61390911210a0c9ea6b4f9bace7ef57ca7a1303`

```dockerfile
```

-	Layers:
	-	`sha256:5044523627d968ee0b87912ad5e86b6f374ff85ef9a7878ae77c52dcf5581421`  
		Last Modified: Tue, 18 Nov 2025 18:00:24 GMT  
		Size: 5.6 MB (5579680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43863609ed306f6a1f2ac385d2c41ef9efb115640066a4bb3b02043bb96f7158`  
		Last Modified: Tue, 18 Nov 2025 18:00:25 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; s390x

```console
$ docker pull irssi@sha256:da93e9283b14d1092e451a797eb231f916c62509d64042a7ed65617b6ab9c487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b5c6cf33fd166afa65862c57464a7a99d44516a592d7093c9c71058d5008c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:17:58 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:18:33 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:18:33 GMT
USER user
# Tue, 18 Nov 2025 02:18:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce4907214a18511e7c1676f0b93794fa538b6672045daa187e1c681bbd9019`  
		Last Modified: Tue, 18 Nov 2025 02:18:55 GMT  
		Size: 19.8 MB (19759415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dca431fe704652eca13f122842a6232de3a88619e75b4585c55d73ab6784b33`  
		Last Modified: Tue, 18 Nov 2025 02:18:52 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12fa892c886e7110c8b36d26e5b06c87bdfad4dab6e9bf9b746c2887bce206f`  
		Last Modified: Tue, 18 Nov 2025 02:18:53 GMT  
		Size: 4.9 MB (4905870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:9921bed642cdddc5b883e960fbb4efa54a43817af46e8c05c8c59611062a6056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babbc467c5248e09f8d3d0710512a06a92fbd5173a81414b551f82cab3d5d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:a1fee033f27a53ca8a99d5789a2cf1a16782bef7f265384856e2f9c62104fc55`  
		Last Modified: Tue, 18 Nov 2025 06:02:18 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd54ab02d147f06764006021d0881cd166981d03206bbcbfdca3215249d036e1`  
		Last Modified: Tue, 18 Nov 2025 06:02:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json
