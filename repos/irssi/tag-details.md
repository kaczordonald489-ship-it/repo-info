<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `irssi`

-	[`irssi:1`](#irssi1)
-	[`irssi:1-alpine`](#irssi1-alpine)
-	[`irssi:1-alpine3.23`](#irssi1-alpine323)
-	[`irssi:1-trixie`](#irssi1-trixie)
-	[`irssi:1.4`](#irssi14)
-	[`irssi:1.4-alpine`](#irssi14-alpine)
-	[`irssi:1.4-alpine3.23`](#irssi14-alpine323)
-	[`irssi:1.4-trixie`](#irssi14-trixie)
-	[`irssi:1.4.5`](#irssi145)
-	[`irssi:1.4.5-alpine`](#irssi145-alpine)
-	[`irssi:1.4.5-alpine3.23`](#irssi145-alpine323)
-	[`irssi:1.4.5-trixie`](#irssi145-trixie)
-	[`irssi:alpine`](#irssialpine)
-	[`irssi:alpine3.23`](#irssialpine323)
-	[`irssi:latest`](#irssilatest)
-	[`irssi:trixie`](#irssitrixie)

## `irssi:1`

```console
$ docker pull irssi@sha256:609a2ed50953d52717592390ee3e98c01c9d73570d22d00bae780781a867411d
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
$ docker pull irssi@sha256:9fae60e7bc9fc24c9db14714ff3340dec77f5694a9c1b466a89d06b539eed73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53870996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208ed2331d877493655ffbf5715d5ee7e7b1f90234b46c4b6347d2f3fe5616b9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:21:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:21:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:21:59 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:21:59 GMT
USER user
# Tue, 03 Feb 2026 02:21:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30e33e354d1d7dda77aaf4af795ff38369ad98bc285f7ba38494d0eda9abb20`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 19.2 MB (19222126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca5a9fa5a0439cd4c3a67c55dd77ab262eaaf8fe3e4f572652f807ae50717fe`  
		Last Modified: Tue, 03 Feb 2026 02:22:08 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7eb220ebedbb0676c3eece8a52277bc0f8d265bb6dc86c6b4c0257d1248723`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 4.9 MB (4866910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:a799ddd3de8dca67e18842b9f3100c61f8e0f40248eec47e9c7d6f7cc5a671e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e411b3f5abbc6ddcbca19c4a0c1521f22b4c249b1349aa45a8611fef7d303416`

```dockerfile
```

-	Layers:
	-	`sha256:293943398617ea6ecaaefceca69694c212fd62ab6e2486655ba0c29e0ae2ba79`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0f10970bd82463907455a4e67a02508285f5300f0993369c217f187ad257c4`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:01a370482e82c1514a233b8e1154c4eeb7e1e29779ed1cfbe0ea72fea926beb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50948888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d3a4cb61f731180f34b3940bbac33a2e24aa2d6dd90ca8e9000be255fe00ee`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:36 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:17:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:17:36 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:18:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:18:24 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:18:24 GMT
USER user
# Tue, 03 Feb 2026 02:18:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bff507cc72771f546378d6ffea702ce1dfc5f7462c98cf416495c9ea7abf5d7`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 18.3 MB (18287991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b732dda1c983c4e5532a6724cc0691bb7f0d4966d926b8031665b9eb19bdf2f4`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe09db28a7bba924a281417665350a9244ac5212bd2c077490813e7355165af`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 4.7 MB (4709982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:02c91f1c49e783ce02db737a1e321704df556858a8ad779ea708f8e801327d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d96f2236d0bf313e468cac657716937a2916282fb27192e905a3ca5780053c9`

```dockerfile
```

-	Layers:
	-	`sha256:c8fb39701e198922668819c0230131b6ae48c12a1d5b030b29d0a2eb4f184198`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69d1c7aa44d9df7724589bd6968e57bcd952b965d7dd14e01f8a0dd52b3fe8c8`  
		Last Modified: Tue, 03 Feb 2026 02:18:34 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:9bd66f1060f9a00e3c4e0bef5e1eeea789fc5f4c5b409aefc8bbcf3135f7dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48685426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9e9708bc24170126dd456a2b01d0c0f067c248903162e7c96091af2380b044`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:20:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:19 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:20:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:20:19 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:20:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:20:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:20:59 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:20:59 GMT
USER user
# Tue, 03 Feb 2026 02:20:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64c57598d1759ed47b0ce33fe2ae3f2ca5dfc344280bee5c91a6e2c2cfc33b`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 17.9 MB (17909993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15370f82ce37fd15003721575f11cd865da7261620aea2b1159317aab5659913`  
		Last Modified: Tue, 03 Feb 2026 02:21:09 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420081012ce7d68e8a87df2713f5901aacfc0a3a49fe4f2ac8aa2e0825c8352`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 4.6 MB (4558319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:6849872da14db17e8b671bdfc642713a76fa2d2017b4ee56049715165db3c076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc1f967ef5736068697a132ec3311efa1a7280ec42fdaa1ed74a8029aac60bf`

```dockerfile
```

-	Layers:
	-	`sha256:b50b6b2a3c6822bb550588172036e08689e2b19d58f855b5606aded3012602bf`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0382a272fccc29001becae9a6ec2fb967f63ffe7d998d793f67a4ff9b9bfd7e`  
		Last Modified: Tue, 03 Feb 2026 02:21:09 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0e6173a8c52441af65097628532330fc826392fa4253e42657ec878c175208c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53975585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb379b987ac880b692fe2dc3dfd931da9c788161033c4e06239554bb4224eb9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:00 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:21:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:21:00 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:21:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:21:38 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:21:38 GMT
USER user
# Tue, 03 Feb 2026 02:21:38 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0532516bbb7262501000c326f37a0930c04d5f5a6565e14b1190d60f0743ce25`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 19.1 MB (19050649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6975dc48bed2afc9f4f4bd9b1665965ae2863eb4ff8cda14ac16f304476d307d`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d6ba22ebad57591e22d79dd65abfa638d56640df56deb4bf8cceb64e95620b`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 4.8 MB (4781508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:2dcaadbe83c3a2a93746c56b19d9f055a7f01810e40da8786b5e2a69a843d506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c18f2b03173ce70e0ebf01ac9749a910865184a273ace4b2b75d21222b7118`

```dockerfile
```

-	Layers:
	-	`sha256:7457b4c9d09e256e51f29dec29c3e51469b7ad175435b171f9c5d18d9599cc7b`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff3cd880792431a74dcfdc01b30e2c7bd58e08261221840c6a483be5f9b07ee`  
		Last Modified: Tue, 03 Feb 2026 02:21:47 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:d10f5d01b9d383d32f36d497a37e76510561eeeaab8a38217dc142bd2044d611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54909414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccf4252e90be99c5c6384e8ef46f99bd42f9232af75a666a85cc7b80be93dbb`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:34 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:17:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:17:34 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:18:17 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:18:17 GMT
USER user
# Tue, 03 Feb 2026 02:18:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c57cfac3b918f6dafe14bf68c93d7d16a8a4970051d18d2a06c2a0263c9145`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 18.7 MB (18743761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c5a3109babbf5c2a1d4b41cb629cbbf8d5c31b10a16a624d77a5dc4bcc39f`  
		Last Modified: Tue, 03 Feb 2026 02:18:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcbe0576fcf1e6208897d40292c8c455af77f42a3cc963ffaff8613d1ca39c1`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 4.9 MB (4868437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:426742b8e02f677fc2e475fb401cbef173d80d0e52b05e495a053dbe62b14c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47fcdb26283af7bd047252c4c37d59277a0cd6d06d787227002528e3c365a58`

```dockerfile
```

-	Layers:
	-	`sha256:a288faa1621c022dd6bd996b78e6eb5d6ee3897b462366f28ee4c3f8bfd9caca`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8db18756472041642ed74f8e1e2ae8db1340756b5fde16825cc70e1a163b56`  
		Last Modified: Tue, 03 Feb 2026 02:18:26 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:55ac6c8d4f6d789fcd2f9caaeb13ce48d776a469d82747e7c1485b5963b19dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58244327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a843d5494442193be8285e2518e0cc0dc17b289884fe2369582b93b61eab8`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:24:37 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:24:37 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:24:37 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:24:37 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:26:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:26:23 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:26:23 GMT
USER user
# Tue, 03 Feb 2026 02:26:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624f9309218047b5688e03740c3f3ec04d0a5b2e096ba1ddb57f22215b1c032e`  
		Last Modified: Tue, 03 Feb 2026 02:26:45 GMT  
		Size: 19.5 MB (19542944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b058eb5982a30c68c6eeb3fddcc4f27b629549cbc9517db75d48bcb1f65cdf`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3765444fdfedf57570813f65ad00dcb9587c7a838f36605feb402e11e81f9b`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 5.1 MB (5097836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:5052a03b5d5ed94c58e1b40d85bcc9e57efe762b73218ad11c008c90311225db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee428904aef2658d2ef8892ffdd5bd384860d0da7ee3179246ea48246a6a9b50`

```dockerfile
```

-	Layers:
	-	`sha256:2fa98124d99ee2944a940c9389ee640f1cd7264bd06b18eac34eea4ceaf8efd6`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3e4620f46fdeae2fb275ccc948845b0e4a8862b657cff3de65766f5fd7fa1e`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; riscv64

```console
$ docker pull irssi@sha256:42f25149c195922ace2d09f52039c56d767996a84e387c8b4eb7cbce5f7c67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51685610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351bf47836b31594adc21aa27395e93d1a031e65d60247048b80b4a4dd12c1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV HOME=/home/user
# Wed, 14 Jan 2026 06:26:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 06:26:49 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 14 Jan 2026 06:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 14 Jan 2026 06:33:37 GMT
WORKDIR /home/user
# Wed, 14 Jan 2026 06:33:37 GMT
USER user
# Wed, 14 Jan 2026 06:33:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f9ee6f39e761595d5c9e020ae1fb10f95fe2a2951aa757f6de57a94a5d25ab`  
		Last Modified: Wed, 14 Jan 2026 06:35:34 GMT  
		Size: 18.5 MB (18549843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef5f232538194de0e7b47d1c08ae77477427a3951186780b1f80e4a91600b4`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b07d932aff1dc5ee2440e07ea368a0ddb73f2c32cb1a8ab0bfd881b02a53f7`  
		Last Modified: Wed, 14 Jan 2026 06:35:31 GMT  
		Size: 4.9 MB (4860721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:0d0a172cbd5471aa3ec8392dc55c5bad0e4fe5bb8e39202b61a8ad6e7252ed2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f4f48da90e6ab7c83ee1b3d3d3112e940971d8bcbed03f47ee03a7d5cca5a6`

```dockerfile
```

-	Layers:
	-	`sha256:afd4f3e89883cc18160c077e4faf0da05c4455d6e0cf0af04a7f525621cba93f`  
		Last Modified: Wed, 14 Jan 2026 06:35:31 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7e2d6743dc6628d707a2e9780dc009b06754202d718210a4e2690ed143c0b`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:3507e27e096139e6c53256b46253b87c2add6684f0a537a81456df935df58f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54507448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9bb61ec181683066bef513d8c48742e3a8098735e181c1c3fff70935a09bd6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:19:25 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:20:02 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:20:02 GMT
USER user
# Tue, 03 Feb 2026 02:20:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8905651585d3b136c5d623c620a4b7471b9176370e9badfa69aa86ab3b0b2771`  
		Last Modified: Tue, 03 Feb 2026 02:20:19 GMT  
		Size: 19.8 MB (19760098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b071b126b87f268a0a29ba9f9fe74d76c9af662cee154d5c7726aae6103dc5c2`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2057418f122012d53f3e9dc13ad0f4d67e6c354b177c2e3cff726f0259e435ff`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 4.9 MB (4905841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:3fb068ad5665041ed11698505383bd5effcaa6e7a9de68a793f560dcdbd63930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7848dc8f3f1945a579bb92f67c19f8ef6b9817196a982d578c50208a9d0cb6f`

```dockerfile
```

-	Layers:
	-	`sha256:90c9b6efea1e9a1c048095f2ecb0af339f8475c5029d9074730a486e02732943`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67606c2343b9ace2f5fd62625eb54620eac701413090a31982ee610dcd1e006f`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:bc9744c4e1f3c9e4401ee35e73ff4f7c97683f5c784c5cce21910e488a4ee219
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
$ docker pull irssi@sha256:84665fb63540b0ca94547800ed0093cb97d41e1cbc0d2aa823a67e6af91fe8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20784026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6645503b9d588217c1fb06c9a2d7e278a4360e4aa22e92d8ff0af44ac2c6c10`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:47 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:47 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:47 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65c05b32f228b7007340211a175e100ca3ddb33a7e2c44b15d11799a9a84ad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 10.9 MB (10857996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c32a8914140e457d67603de3b04ccc66e688baed84d8d500f40dc885ef27a`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93abf1ed0403fdbc85fa021598a1202b3d9b55bd9d785457b554af6b86fc7d`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 6.1 MB (6063223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:7bd9c1f9350891fb6e79ac3dc4d7686c1c714bb2c12147cb089864d19ef3bc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e29e513927a47425fe64b68ba4eeb03593581de0692a732211bc7b11537936`

```dockerfile
```

-	Layers:
	-	`sha256:5d4ee629f31bfb597346562d7da53858808c502ca6820fb40a7c347520afebad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b9c1c09e72415a3ca7367aec0652ca69a856b8c6a57ef69ba919d208498b76`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:9a8babd75444eea65ebe3a06627eceb16f4d50aec2da2998fd3a611d75ed5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04e50bc1d87804658a7d29a7ebb00b20d1a22d6d21cd19f5eff93f84035eb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:23:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:23:57 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:24:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:24:17 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:24:17 GMT
USER user
# Wed, 28 Jan 2026 02:24:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5c4e6a80a684ff34083f2ded6ae6a1b0f08ded4c8c5b0967f8b209ee2cd80`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 10.1 MB (10075626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93db171eca68243a4f689b5400ef3c2ac2a1074f1eae1f9f0d049506c8756fe`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c8c890839d95ebaf447485d8492d089fc8fa23d1ca65c6349a41ac95bc961`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 5.9 MB (5893116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:424e17d1ca73b3f1d92e5d0c0b7272bbaeee943cc673a2249f0bf7ca99eeedde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7bd514eeda8663e46d4eeed484d7df02209f60112393607269af3e2c0430c`

```dockerfile
```

-	Layers:
	-	`sha256:8fbda3c9e4c0ad20ecba339d117fab2e86108fcfe33cbba7f8ddc3053d6bc89a`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:42ff91c7e5cb5046e91c18adce476ce64e5d772ab658a70c9df46e592b10ce82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18828366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ac84c98bbbaf189bedd8109f71397874c887df2e4eb32123f05470b88358b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:21 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:22:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:22:22 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:22:37 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:22:37 GMT
USER user
# Wed, 28 Jan 2026 02:22:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ae8f3941338d2191aad9429d0bd185ceeb7aeedb8fddf43adad6b57e3273e`  
		Last Modified: Wed, 28 Jan 2026 02:22:45 GMT  
		Size: 9.9 MB (9902405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770acb73451dc424aeb5afcad4a4882f5d765fcbcc8b659b8841bf77d8166afe`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda40971fe170d5e56e81f398ba01d1904a08b07386da11fe56b125109dd60b9`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 5.6 MB (5643252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:fcebcd556b705ae5c410e6b569b01096b561714c5c2fc1d7c8c746decaeef0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d96801a2a79a245717287e0380350d8e1b0c44936b6dcaf8429b0e2074bab`

```dockerfile
```

-	Layers:
	-	`sha256:e0caf0a4bbae914fea3e8ffab5d1f1752e3fc858d38e993806dd2b78f6919657`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda69d589c766de3e44adc56d464708c1c2090577cfe6fdd9a50f95229a2c4fa`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c53ef5cb4c4fb78d4ffdaad1b902adc24327fb49d4ad5c6d719dcf26f8e1ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20927195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538037fb15131e4b2540ac0e275393593929c95a1ca622c94e6c70d99874f28`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628108c2cc8068dbd74588362d3734d7b6b306883916eb33cb53af667c096440`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 10.8 MB (10792790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9361ffc4206f8e272dc8adc782da4ab39f3b1fe287c6dfb23c57814cf1e94439`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7efe759a9de929b3a25440ff73ac10595ac218ae5d0a087f34fa385d7db181f`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 5.9 MB (5936327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ac959328037122478f2c09228cf4478f1c099d3257efec2dae9823db1d16b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db6c23ab4cfc36c7b70e7f4325b9bfa25d1a31a205c632f8e25757cb01f7cef`

```dockerfile
```

-	Layers:
	-	`sha256:3b09e8c286f81074ecdbaaeccccef453ddf9951ff459e4c086e01b8968fe3b0e`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57974d8beacb812f7bb8f7b52301ddd6a66eb7f4c851dcc2ee58f100ec0208b1`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:a32c16d5607a49617e8d077ec1f9ba5b53b0001a5d70805f183e27ac8f377955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20225669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7946f5f999880045f35ea6c3b7115f7cc7ca872f2653f90c5b0a114ea701599b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:16:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:16:14 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:16:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:16:34 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:16:34 GMT
USER user
# Wed, 28 Jan 2026 02:16:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50882b3c493b99635b6de6cd7279fc00a7df160e84cd53399664993828611810`  
		Last Modified: Wed, 28 Jan 2026 02:16:41 GMT  
		Size: 10.4 MB (10393535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588c02c444f10953a0f0aac9fa979fe4a835bbefde822557708fbd3d21750de`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dcb0c68d5a17e86130988d6ddf97978ae4c3d866b099962426d869a1c1fc3`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 6.1 MB (6144150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b77b6da6595a9c4ebfe003d3192b1a97bd9a14f1fe19417ad4a8d7068acc0505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f268d469cb9fcc79cb87b83fdcbadb9fa6818bf4d9c56a441df0e015c2ec6`

```dockerfile
```

-	Layers:
	-	`sha256:1ddc13011deb856a736a8c90df7acab1227398d8a2ae9e4586daa141365096b4`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e26778e3f506818fa4ed452e58334a8e15701f1d896ec8ed2ff3288ca7ecef`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:b40803da860e141ec3ab2320cf224c304aa870a9a884cb362b69e74b6fd82b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21272396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a2c6a98e5b7978e9d4671908d2864a8d58c1b872e5ec279f9a7a67312f3e2b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:32:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:32:11 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:32:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:32:31 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:32:31 GMT
USER user
# Wed, 28 Jan 2026 02:32:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc81a5350f307da5c9651178208c0aa789db44da9179ac834ac469d70ce42cc`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 11.1 MB (11079608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505a6cbf58cbc8474040a9d448a79cab0812b78e3b1c6db13e87987f8e4d9a0`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3296179391416e1833f722cc60f06d3ee4df4255177c36a2f41a35a6ab2661b`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 6.4 MB (6362158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e2ead2561551ba2a279d799d266e484e986d5370478af7155036333e682a1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551e8fca5526f8aa868ce90e80d554f73ff2800bcf6fb3b0fb1b9013223228b5`

```dockerfile
```

-	Layers:
	-	`sha256:890481868cc7de496dcdc1f70cc0d6026227efccdd40466a57aa43304c3e345f`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9fac81ff985d048567933403c842b1d477306de718e7d5226612b3cb1eb068`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:a29b54bd9ab139f5c60185ee85db0a602092a6821866cad82df0fb45368c398c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19942208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9176875f86f8abf3bc20c65b42847d911af0be7e5863f4d6dcbd526719132c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:24:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 08:24:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 08:24:34 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 08:28:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 08:28:23 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 08:28:23 GMT
USER user
# Wed, 28 Jan 2026 08:28:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6c4248bc749950275ce15b2dff82393f4351ced2e20c7b5e2ffef3c0848ce`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 10.3 MB (10291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e176dad2b23e06165e59400a1ff2260014ec93b0fb3b8c7628a64e1adaf49f`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3131351fcf8ddb074fb73d582b50e94aa55e099ca06fc128b310489675e69c97`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 6.1 MB (6064037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:165ef1cc15b3aeae45d6479f80369f8078869b953af00ad6ddb3765a55356e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192140d2d48650b459b2a9acdce6a086c4bf08877b907f3c6bc37ce9799d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:a59cb060f285e8659782eab321b072ac7afdce9472b5395d10144bca9d127b79`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e90caa10ad17b6e48ce9a44b3d010cc7b20e200cbb6ec1067441e247ce555fc`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:e55dc3c7ee83af6ee968373464f0b874c0d9149e01ce32f4680a83b5791d2ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a042dac64e240c543befef410a12767f4051b627b63028b597010c108714083`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:19:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:19:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:20:14 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:20:14 GMT
USER user
# Wed, 28 Jan 2026 02:20:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e174cb7156ade2e31408909452271b26ae4f143ef276276f0f448b1bad2165`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 11.4 MB (11405107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2a6b19294dd14e5551b394d76102c59c84eae810434dca5ae909a1e58da672`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba483b2b5362b1905ca82789be9c963c7fde3135033f6aac9183937e5d9161`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 6.2 MB (6202965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:05475f6695b9e4e1863216bdc5de6a1a24bfec2a5baecd06f9a7bc6cd0d17408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183ed0bc53cc736e214c57eaef2cb864de7e9dbaccf5fe0a5530c72247ac1ab`

```dockerfile
```

-	Layers:
	-	`sha256:c63a0479be024622dc272c05215babf54e4fc3b5c5ab3d053c0dcf2de80483cb`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5037cc7aa93ea1e1f234114cc48a82216f93fe0b9ee46a01ee9a03609cbe19e`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.23`

```console
$ docker pull irssi@sha256:bc9744c4e1f3c9e4401ee35e73ff4f7c97683f5c784c5cce21910e488a4ee219
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

### `irssi:1-alpine3.23` - linux; amd64

```console
$ docker pull irssi@sha256:84665fb63540b0ca94547800ed0093cb97d41e1cbc0d2aa823a67e6af91fe8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20784026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6645503b9d588217c1fb06c9a2d7e278a4360e4aa22e92d8ff0af44ac2c6c10`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:47 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:47 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:47 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65c05b32f228b7007340211a175e100ca3ddb33a7e2c44b15d11799a9a84ad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 10.9 MB (10857996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c32a8914140e457d67603de3b04ccc66e688baed84d8d500f40dc885ef27a`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93abf1ed0403fdbc85fa021598a1202b3d9b55bd9d785457b554af6b86fc7d`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 6.1 MB (6063223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:7bd9c1f9350891fb6e79ac3dc4d7686c1c714bb2c12147cb089864d19ef3bc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e29e513927a47425fe64b68ba4eeb03593581de0692a732211bc7b11537936`

```dockerfile
```

-	Layers:
	-	`sha256:5d4ee629f31bfb597346562d7da53858808c502ca6820fb40a7c347520afebad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b9c1c09e72415a3ca7367aec0652ca69a856b8c6a57ef69ba919d208498b76`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:9a8babd75444eea65ebe3a06627eceb16f4d50aec2da2998fd3a611d75ed5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04e50bc1d87804658a7d29a7ebb00b20d1a22d6d21cd19f5eff93f84035eb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:23:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:23:57 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:24:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:24:17 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:24:17 GMT
USER user
# Wed, 28 Jan 2026 02:24:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5c4e6a80a684ff34083f2ded6ae6a1b0f08ded4c8c5b0967f8b209ee2cd80`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 10.1 MB (10075626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93db171eca68243a4f689b5400ef3c2ac2a1074f1eae1f9f0d049506c8756fe`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c8c890839d95ebaf447485d8492d089fc8fa23d1ca65c6349a41ac95bc961`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 5.9 MB (5893116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:424e17d1ca73b3f1d92e5d0c0b7272bbaeee943cc673a2249f0bf7ca99eeedde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7bd514eeda8663e46d4eeed484d7df02209f60112393607269af3e2c0430c`

```dockerfile
```

-	Layers:
	-	`sha256:8fbda3c9e4c0ad20ecba339d117fab2e86108fcfe33cbba7f8ddc3053d6bc89a`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:42ff91c7e5cb5046e91c18adce476ce64e5d772ab658a70c9df46e592b10ce82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18828366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ac84c98bbbaf189bedd8109f71397874c887df2e4eb32123f05470b88358b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:21 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:22:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:22:22 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:22:37 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:22:37 GMT
USER user
# Wed, 28 Jan 2026 02:22:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ae8f3941338d2191aad9429d0bd185ceeb7aeedb8fddf43adad6b57e3273e`  
		Last Modified: Wed, 28 Jan 2026 02:22:45 GMT  
		Size: 9.9 MB (9902405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770acb73451dc424aeb5afcad4a4882f5d765fcbcc8b659b8841bf77d8166afe`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda40971fe170d5e56e81f398ba01d1904a08b07386da11fe56b125109dd60b9`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 5.6 MB (5643252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:fcebcd556b705ae5c410e6b569b01096b561714c5c2fc1d7c8c746decaeef0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d96801a2a79a245717287e0380350d8e1b0c44936b6dcaf8429b0e2074bab`

```dockerfile
```

-	Layers:
	-	`sha256:e0caf0a4bbae914fea3e8ffab5d1f1752e3fc858d38e993806dd2b78f6919657`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda69d589c766de3e44adc56d464708c1c2090577cfe6fdd9a50f95229a2c4fa`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c53ef5cb4c4fb78d4ffdaad1b902adc24327fb49d4ad5c6d719dcf26f8e1ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20927195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538037fb15131e4b2540ac0e275393593929c95a1ca622c94e6c70d99874f28`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628108c2cc8068dbd74588362d3734d7b6b306883916eb33cb53af667c096440`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 10.8 MB (10792790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9361ffc4206f8e272dc8adc782da4ab39f3b1fe287c6dfb23c57814cf1e94439`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7efe759a9de929b3a25440ff73ac10595ac218ae5d0a087f34fa385d7db181f`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 5.9 MB (5936327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:ac959328037122478f2c09228cf4478f1c099d3257efec2dae9823db1d16b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db6c23ab4cfc36c7b70e7f4325b9bfa25d1a31a205c632f8e25757cb01f7cef`

```dockerfile
```

-	Layers:
	-	`sha256:3b09e8c286f81074ecdbaaeccccef453ddf9951ff459e4c086e01b8968fe3b0e`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57974d8beacb812f7bb8f7b52301ddd6a66eb7f4c851dcc2ee58f100ec0208b1`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:a32c16d5607a49617e8d077ec1f9ba5b53b0001a5d70805f183e27ac8f377955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20225669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7946f5f999880045f35ea6c3b7115f7cc7ca872f2653f90c5b0a114ea701599b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:16:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:16:14 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:16:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:16:34 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:16:34 GMT
USER user
# Wed, 28 Jan 2026 02:16:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50882b3c493b99635b6de6cd7279fc00a7df160e84cd53399664993828611810`  
		Last Modified: Wed, 28 Jan 2026 02:16:41 GMT  
		Size: 10.4 MB (10393535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588c02c444f10953a0f0aac9fa979fe4a835bbefde822557708fbd3d21750de`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dcb0c68d5a17e86130988d6ddf97978ae4c3d866b099962426d869a1c1fc3`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 6.1 MB (6144150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:b77b6da6595a9c4ebfe003d3192b1a97bd9a14f1fe19417ad4a8d7068acc0505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f268d469cb9fcc79cb87b83fdcbadb9fa6818bf4d9c56a441df0e015c2ec6`

```dockerfile
```

-	Layers:
	-	`sha256:1ddc13011deb856a736a8c90df7acab1227398d8a2ae9e4586daa141365096b4`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e26778e3f506818fa4ed452e58334a8e15701f1d896ec8ed2ff3288ca7ecef`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:b40803da860e141ec3ab2320cf224c304aa870a9a884cb362b69e74b6fd82b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21272396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a2c6a98e5b7978e9d4671908d2864a8d58c1b872e5ec279f9a7a67312f3e2b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:32:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:32:11 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:32:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:32:31 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:32:31 GMT
USER user
# Wed, 28 Jan 2026 02:32:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc81a5350f307da5c9651178208c0aa789db44da9179ac834ac469d70ce42cc`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 11.1 MB (11079608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505a6cbf58cbc8474040a9d448a79cab0812b78e3b1c6db13e87987f8e4d9a0`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3296179391416e1833f722cc60f06d3ee4df4255177c36a2f41a35a6ab2661b`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 6.4 MB (6362158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:e2ead2561551ba2a279d799d266e484e986d5370478af7155036333e682a1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551e8fca5526f8aa868ce90e80d554f73ff2800bcf6fb3b0fb1b9013223228b5`

```dockerfile
```

-	Layers:
	-	`sha256:890481868cc7de496dcdc1f70cc0d6026227efccdd40466a57aa43304c3e345f`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9fac81ff985d048567933403c842b1d477306de718e7d5226612b3cb1eb068`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:a29b54bd9ab139f5c60185ee85db0a602092a6821866cad82df0fb45368c398c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19942208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9176875f86f8abf3bc20c65b42847d911af0be7e5863f4d6dcbd526719132c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:24:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 08:24:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 08:24:34 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 08:28:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 08:28:23 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 08:28:23 GMT
USER user
# Wed, 28 Jan 2026 08:28:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6c4248bc749950275ce15b2dff82393f4351ced2e20c7b5e2ffef3c0848ce`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 10.3 MB (10291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e176dad2b23e06165e59400a1ff2260014ec93b0fb3b8c7628a64e1adaf49f`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3131351fcf8ddb074fb73d582b50e94aa55e099ca06fc128b310489675e69c97`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 6.1 MB (6064037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:165ef1cc15b3aeae45d6479f80369f8078869b953af00ad6ddb3765a55356e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192140d2d48650b459b2a9acdce6a086c4bf08877b907f3c6bc37ce9799d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:a59cb060f285e8659782eab321b072ac7afdce9472b5395d10144bca9d127b79`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e90caa10ad17b6e48ce9a44b3d010cc7b20e200cbb6ec1067441e247ce555fc`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:e55dc3c7ee83af6ee968373464f0b874c0d9149e01ce32f4680a83b5791d2ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a042dac64e240c543befef410a12767f4051b627b63028b597010c108714083`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:19:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:19:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:20:14 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:20:14 GMT
USER user
# Wed, 28 Jan 2026 02:20:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e174cb7156ade2e31408909452271b26ae4f143ef276276f0f448b1bad2165`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 11.4 MB (11405107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2a6b19294dd14e5551b394d76102c59c84eae810434dca5ae909a1e58da672`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba483b2b5362b1905ca82789be9c963c7fde3135033f6aac9183937e5d9161`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 6.2 MB (6202965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:05475f6695b9e4e1863216bdc5de6a1a24bfec2a5baecd06f9a7bc6cd0d17408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183ed0bc53cc736e214c57eaef2cb864de7e9dbaccf5fe0a5530c72247ac1ab`

```dockerfile
```

-	Layers:
	-	`sha256:c63a0479be024622dc272c05215babf54e4fc3b5c5ab3d053c0dcf2de80483cb`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5037cc7aa93ea1e1f234114cc48a82216f93fe0b9ee46a01ee9a03609cbe19e`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-trixie`

```console
$ docker pull irssi@sha256:609a2ed50953d52717592390ee3e98c01c9d73570d22d00bae780781a867411d
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
$ docker pull irssi@sha256:9fae60e7bc9fc24c9db14714ff3340dec77f5694a9c1b466a89d06b539eed73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53870996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208ed2331d877493655ffbf5715d5ee7e7b1f90234b46c4b6347d2f3fe5616b9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:21:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:21:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:21:59 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:21:59 GMT
USER user
# Tue, 03 Feb 2026 02:21:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30e33e354d1d7dda77aaf4af795ff38369ad98bc285f7ba38494d0eda9abb20`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 19.2 MB (19222126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca5a9fa5a0439cd4c3a67c55dd77ab262eaaf8fe3e4f572652f807ae50717fe`  
		Last Modified: Tue, 03 Feb 2026 02:22:08 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7eb220ebedbb0676c3eece8a52277bc0f8d265bb6dc86c6b4c0257d1248723`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 4.9 MB (4866910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:a799ddd3de8dca67e18842b9f3100c61f8e0f40248eec47e9c7d6f7cc5a671e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e411b3f5abbc6ddcbca19c4a0c1521f22b4c249b1349aa45a8611fef7d303416`

```dockerfile
```

-	Layers:
	-	`sha256:293943398617ea6ecaaefceca69694c212fd62ab6e2486655ba0c29e0ae2ba79`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0f10970bd82463907455a4e67a02508285f5300f0993369c217f187ad257c4`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:01a370482e82c1514a233b8e1154c4eeb7e1e29779ed1cfbe0ea72fea926beb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50948888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d3a4cb61f731180f34b3940bbac33a2e24aa2d6dd90ca8e9000be255fe00ee`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:36 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:17:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:17:36 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:18:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:18:24 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:18:24 GMT
USER user
# Tue, 03 Feb 2026 02:18:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bff507cc72771f546378d6ffea702ce1dfc5f7462c98cf416495c9ea7abf5d7`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 18.3 MB (18287991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b732dda1c983c4e5532a6724cc0691bb7f0d4966d926b8031665b9eb19bdf2f4`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe09db28a7bba924a281417665350a9244ac5212bd2c077490813e7355165af`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 4.7 MB (4709982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:02c91f1c49e783ce02db737a1e321704df556858a8ad779ea708f8e801327d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d96f2236d0bf313e468cac657716937a2916282fb27192e905a3ca5780053c9`

```dockerfile
```

-	Layers:
	-	`sha256:c8fb39701e198922668819c0230131b6ae48c12a1d5b030b29d0a2eb4f184198`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69d1c7aa44d9df7724589bd6968e57bcd952b965d7dd14e01f8a0dd52b3fe8c8`  
		Last Modified: Tue, 03 Feb 2026 02:18:34 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:9bd66f1060f9a00e3c4e0bef5e1eeea789fc5f4c5b409aefc8bbcf3135f7dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48685426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9e9708bc24170126dd456a2b01d0c0f067c248903162e7c96091af2380b044`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:20:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:19 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:20:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:20:19 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:20:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:20:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:20:59 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:20:59 GMT
USER user
# Tue, 03 Feb 2026 02:20:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64c57598d1759ed47b0ce33fe2ae3f2ca5dfc344280bee5c91a6e2c2cfc33b`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 17.9 MB (17909993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15370f82ce37fd15003721575f11cd865da7261620aea2b1159317aab5659913`  
		Last Modified: Tue, 03 Feb 2026 02:21:09 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420081012ce7d68e8a87df2713f5901aacfc0a3a49fe4f2ac8aa2e0825c8352`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 4.6 MB (4558319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6849872da14db17e8b671bdfc642713a76fa2d2017b4ee56049715165db3c076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc1f967ef5736068697a132ec3311efa1a7280ec42fdaa1ed74a8029aac60bf`

```dockerfile
```

-	Layers:
	-	`sha256:b50b6b2a3c6822bb550588172036e08689e2b19d58f855b5606aded3012602bf`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0382a272fccc29001becae9a6ec2fb967f63ffe7d998d793f67a4ff9b9bfd7e`  
		Last Modified: Tue, 03 Feb 2026 02:21:09 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0e6173a8c52441af65097628532330fc826392fa4253e42657ec878c175208c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53975585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb379b987ac880b692fe2dc3dfd931da9c788161033c4e06239554bb4224eb9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:00 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:21:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:21:00 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:21:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:21:38 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:21:38 GMT
USER user
# Tue, 03 Feb 2026 02:21:38 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0532516bbb7262501000c326f37a0930c04d5f5a6565e14b1190d60f0743ce25`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 19.1 MB (19050649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6975dc48bed2afc9f4f4bd9b1665965ae2863eb4ff8cda14ac16f304476d307d`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d6ba22ebad57591e22d79dd65abfa638d56640df56deb4bf8cceb64e95620b`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 4.8 MB (4781508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2dcaadbe83c3a2a93746c56b19d9f055a7f01810e40da8786b5e2a69a843d506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c18f2b03173ce70e0ebf01ac9749a910865184a273ace4b2b75d21222b7118`

```dockerfile
```

-	Layers:
	-	`sha256:7457b4c9d09e256e51f29dec29c3e51469b7ad175435b171f9c5d18d9599cc7b`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff3cd880792431a74dcfdc01b30e2c7bd58e08261221840c6a483be5f9b07ee`  
		Last Modified: Tue, 03 Feb 2026 02:21:47 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; 386

```console
$ docker pull irssi@sha256:d10f5d01b9d383d32f36d497a37e76510561eeeaab8a38217dc142bd2044d611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54909414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccf4252e90be99c5c6384e8ef46f99bd42f9232af75a666a85cc7b80be93dbb`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:34 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:17:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:17:34 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:18:17 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:18:17 GMT
USER user
# Tue, 03 Feb 2026 02:18:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c57cfac3b918f6dafe14bf68c93d7d16a8a4970051d18d2a06c2a0263c9145`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 18.7 MB (18743761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c5a3109babbf5c2a1d4b41cb629cbbf8d5c31b10a16a624d77a5dc4bcc39f`  
		Last Modified: Tue, 03 Feb 2026 02:18:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcbe0576fcf1e6208897d40292c8c455af77f42a3cc963ffaff8613d1ca39c1`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 4.9 MB (4868437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:426742b8e02f677fc2e475fb401cbef173d80d0e52b05e495a053dbe62b14c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47fcdb26283af7bd047252c4c37d59277a0cd6d06d787227002528e3c365a58`

```dockerfile
```

-	Layers:
	-	`sha256:a288faa1621c022dd6bd996b78e6eb5d6ee3897b462366f28ee4c3f8bfd9caca`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8db18756472041642ed74f8e1e2ae8db1340756b5fde16825cc70e1a163b56`  
		Last Modified: Tue, 03 Feb 2026 02:18:26 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:55ac6c8d4f6d789fcd2f9caaeb13ce48d776a469d82747e7c1485b5963b19dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58244327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a843d5494442193be8285e2518e0cc0dc17b289884fe2369582b93b61eab8`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:24:37 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:24:37 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:24:37 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:24:37 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:26:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:26:23 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:26:23 GMT
USER user
# Tue, 03 Feb 2026 02:26:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624f9309218047b5688e03740c3f3ec04d0a5b2e096ba1ddb57f22215b1c032e`  
		Last Modified: Tue, 03 Feb 2026 02:26:45 GMT  
		Size: 19.5 MB (19542944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b058eb5982a30c68c6eeb3fddcc4f27b629549cbc9517db75d48bcb1f65cdf`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3765444fdfedf57570813f65ad00dcb9587c7a838f36605feb402e11e81f9b`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 5.1 MB (5097836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:5052a03b5d5ed94c58e1b40d85bcc9e57efe762b73218ad11c008c90311225db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee428904aef2658d2ef8892ffdd5bd384860d0da7ee3179246ea48246a6a9b50`

```dockerfile
```

-	Layers:
	-	`sha256:2fa98124d99ee2944a940c9389ee640f1cd7264bd06b18eac34eea4ceaf8efd6`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3e4620f46fdeae2fb275ccc948845b0e4a8862b657cff3de65766f5fd7fa1e`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:42f25149c195922ace2d09f52039c56d767996a84e387c8b4eb7cbce5f7c67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51685610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351bf47836b31594adc21aa27395e93d1a031e65d60247048b80b4a4dd12c1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV HOME=/home/user
# Wed, 14 Jan 2026 06:26:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 06:26:49 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 14 Jan 2026 06:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 14 Jan 2026 06:33:37 GMT
WORKDIR /home/user
# Wed, 14 Jan 2026 06:33:37 GMT
USER user
# Wed, 14 Jan 2026 06:33:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f9ee6f39e761595d5c9e020ae1fb10f95fe2a2951aa757f6de57a94a5d25ab`  
		Last Modified: Wed, 14 Jan 2026 06:35:34 GMT  
		Size: 18.5 MB (18549843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef5f232538194de0e7b47d1c08ae77477427a3951186780b1f80e4a91600b4`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b07d932aff1dc5ee2440e07ea368a0ddb73f2c32cb1a8ab0bfd881b02a53f7`  
		Last Modified: Wed, 14 Jan 2026 06:35:31 GMT  
		Size: 4.9 MB (4860721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:0d0a172cbd5471aa3ec8392dc55c5bad0e4fe5bb8e39202b61a8ad6e7252ed2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f4f48da90e6ab7c83ee1b3d3d3112e940971d8bcbed03f47ee03a7d5cca5a6`

```dockerfile
```

-	Layers:
	-	`sha256:afd4f3e89883cc18160c077e4faf0da05c4455d6e0cf0af04a7f525621cba93f`  
		Last Modified: Wed, 14 Jan 2026 06:35:31 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7e2d6743dc6628d707a2e9780dc009b06754202d718210a4e2690ed143c0b`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:3507e27e096139e6c53256b46253b87c2add6684f0a537a81456df935df58f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54507448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9bb61ec181683066bef513d8c48742e3a8098735e181c1c3fff70935a09bd6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:19:25 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:20:02 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:20:02 GMT
USER user
# Tue, 03 Feb 2026 02:20:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8905651585d3b136c5d623c620a4b7471b9176370e9badfa69aa86ab3b0b2771`  
		Last Modified: Tue, 03 Feb 2026 02:20:19 GMT  
		Size: 19.8 MB (19760098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b071b126b87f268a0a29ba9f9fe74d76c9af662cee154d5c7726aae6103dc5c2`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2057418f122012d53f3e9dc13ad0f4d67e6c354b177c2e3cff726f0259e435ff`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 4.9 MB (4905841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:3fb068ad5665041ed11698505383bd5effcaa6e7a9de68a793f560dcdbd63930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7848dc8f3f1945a579bb92f67c19f8ef6b9817196a982d578c50208a9d0cb6f`

```dockerfile
```

-	Layers:
	-	`sha256:90c9b6efea1e9a1c048095f2ecb0af339f8475c5029d9074730a486e02732943`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67606c2343b9ace2f5fd62625eb54620eac701413090a31982ee610dcd1e006f`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:609a2ed50953d52717592390ee3e98c01c9d73570d22d00bae780781a867411d
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
$ docker pull irssi@sha256:9fae60e7bc9fc24c9db14714ff3340dec77f5694a9c1b466a89d06b539eed73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53870996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208ed2331d877493655ffbf5715d5ee7e7b1f90234b46c4b6347d2f3fe5616b9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:21:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:21:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:21:59 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:21:59 GMT
USER user
# Tue, 03 Feb 2026 02:21:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30e33e354d1d7dda77aaf4af795ff38369ad98bc285f7ba38494d0eda9abb20`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 19.2 MB (19222126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca5a9fa5a0439cd4c3a67c55dd77ab262eaaf8fe3e4f572652f807ae50717fe`  
		Last Modified: Tue, 03 Feb 2026 02:22:08 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7eb220ebedbb0676c3eece8a52277bc0f8d265bb6dc86c6b4c0257d1248723`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 4.9 MB (4866910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:a799ddd3de8dca67e18842b9f3100c61f8e0f40248eec47e9c7d6f7cc5a671e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e411b3f5abbc6ddcbca19c4a0c1521f22b4c249b1349aa45a8611fef7d303416`

```dockerfile
```

-	Layers:
	-	`sha256:293943398617ea6ecaaefceca69694c212fd62ab6e2486655ba0c29e0ae2ba79`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0f10970bd82463907455a4e67a02508285f5300f0993369c217f187ad257c4`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:01a370482e82c1514a233b8e1154c4eeb7e1e29779ed1cfbe0ea72fea926beb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50948888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d3a4cb61f731180f34b3940bbac33a2e24aa2d6dd90ca8e9000be255fe00ee`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:36 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:17:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:17:36 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:18:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:18:24 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:18:24 GMT
USER user
# Tue, 03 Feb 2026 02:18:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bff507cc72771f546378d6ffea702ce1dfc5f7462c98cf416495c9ea7abf5d7`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 18.3 MB (18287991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b732dda1c983c4e5532a6724cc0691bb7f0d4966d926b8031665b9eb19bdf2f4`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe09db28a7bba924a281417665350a9244ac5212bd2c077490813e7355165af`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 4.7 MB (4709982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:02c91f1c49e783ce02db737a1e321704df556858a8ad779ea708f8e801327d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d96f2236d0bf313e468cac657716937a2916282fb27192e905a3ca5780053c9`

```dockerfile
```

-	Layers:
	-	`sha256:c8fb39701e198922668819c0230131b6ae48c12a1d5b030b29d0a2eb4f184198`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69d1c7aa44d9df7724589bd6968e57bcd952b965d7dd14e01f8a0dd52b3fe8c8`  
		Last Modified: Tue, 03 Feb 2026 02:18:34 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:9bd66f1060f9a00e3c4e0bef5e1eeea789fc5f4c5b409aefc8bbcf3135f7dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48685426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9e9708bc24170126dd456a2b01d0c0f067c248903162e7c96091af2380b044`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:20:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:19 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:20:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:20:19 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:20:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:20:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:20:59 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:20:59 GMT
USER user
# Tue, 03 Feb 2026 02:20:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64c57598d1759ed47b0ce33fe2ae3f2ca5dfc344280bee5c91a6e2c2cfc33b`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 17.9 MB (17909993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15370f82ce37fd15003721575f11cd865da7261620aea2b1159317aab5659913`  
		Last Modified: Tue, 03 Feb 2026 02:21:09 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420081012ce7d68e8a87df2713f5901aacfc0a3a49fe4f2ac8aa2e0825c8352`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 4.6 MB (4558319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:6849872da14db17e8b671bdfc642713a76fa2d2017b4ee56049715165db3c076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc1f967ef5736068697a132ec3311efa1a7280ec42fdaa1ed74a8029aac60bf`

```dockerfile
```

-	Layers:
	-	`sha256:b50b6b2a3c6822bb550588172036e08689e2b19d58f855b5606aded3012602bf`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0382a272fccc29001becae9a6ec2fb967f63ffe7d998d793f67a4ff9b9bfd7e`  
		Last Modified: Tue, 03 Feb 2026 02:21:09 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0e6173a8c52441af65097628532330fc826392fa4253e42657ec878c175208c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53975585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb379b987ac880b692fe2dc3dfd931da9c788161033c4e06239554bb4224eb9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:00 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:21:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:21:00 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:21:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:21:38 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:21:38 GMT
USER user
# Tue, 03 Feb 2026 02:21:38 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0532516bbb7262501000c326f37a0930c04d5f5a6565e14b1190d60f0743ce25`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 19.1 MB (19050649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6975dc48bed2afc9f4f4bd9b1665965ae2863eb4ff8cda14ac16f304476d307d`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d6ba22ebad57591e22d79dd65abfa638d56640df56deb4bf8cceb64e95620b`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 4.8 MB (4781508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:2dcaadbe83c3a2a93746c56b19d9f055a7f01810e40da8786b5e2a69a843d506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c18f2b03173ce70e0ebf01ac9749a910865184a273ace4b2b75d21222b7118`

```dockerfile
```

-	Layers:
	-	`sha256:7457b4c9d09e256e51f29dec29c3e51469b7ad175435b171f9c5d18d9599cc7b`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff3cd880792431a74dcfdc01b30e2c7bd58e08261221840c6a483be5f9b07ee`  
		Last Modified: Tue, 03 Feb 2026 02:21:47 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:d10f5d01b9d383d32f36d497a37e76510561eeeaab8a38217dc142bd2044d611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54909414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccf4252e90be99c5c6384e8ef46f99bd42f9232af75a666a85cc7b80be93dbb`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:34 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:17:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:17:34 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:18:17 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:18:17 GMT
USER user
# Tue, 03 Feb 2026 02:18:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c57cfac3b918f6dafe14bf68c93d7d16a8a4970051d18d2a06c2a0263c9145`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 18.7 MB (18743761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c5a3109babbf5c2a1d4b41cb629cbbf8d5c31b10a16a624d77a5dc4bcc39f`  
		Last Modified: Tue, 03 Feb 2026 02:18:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcbe0576fcf1e6208897d40292c8c455af77f42a3cc963ffaff8613d1ca39c1`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 4.9 MB (4868437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:426742b8e02f677fc2e475fb401cbef173d80d0e52b05e495a053dbe62b14c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47fcdb26283af7bd047252c4c37d59277a0cd6d06d787227002528e3c365a58`

```dockerfile
```

-	Layers:
	-	`sha256:a288faa1621c022dd6bd996b78e6eb5d6ee3897b462366f28ee4c3f8bfd9caca`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8db18756472041642ed74f8e1e2ae8db1340756b5fde16825cc70e1a163b56`  
		Last Modified: Tue, 03 Feb 2026 02:18:26 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:55ac6c8d4f6d789fcd2f9caaeb13ce48d776a469d82747e7c1485b5963b19dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58244327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a843d5494442193be8285e2518e0cc0dc17b289884fe2369582b93b61eab8`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:24:37 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:24:37 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:24:37 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:24:37 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:26:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:26:23 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:26:23 GMT
USER user
# Tue, 03 Feb 2026 02:26:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624f9309218047b5688e03740c3f3ec04d0a5b2e096ba1ddb57f22215b1c032e`  
		Last Modified: Tue, 03 Feb 2026 02:26:45 GMT  
		Size: 19.5 MB (19542944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b058eb5982a30c68c6eeb3fddcc4f27b629549cbc9517db75d48bcb1f65cdf`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3765444fdfedf57570813f65ad00dcb9587c7a838f36605feb402e11e81f9b`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 5.1 MB (5097836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:5052a03b5d5ed94c58e1b40d85bcc9e57efe762b73218ad11c008c90311225db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee428904aef2658d2ef8892ffdd5bd384860d0da7ee3179246ea48246a6a9b50`

```dockerfile
```

-	Layers:
	-	`sha256:2fa98124d99ee2944a940c9389ee640f1cd7264bd06b18eac34eea4ceaf8efd6`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3e4620f46fdeae2fb275ccc948845b0e4a8862b657cff3de65766f5fd7fa1e`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; riscv64

```console
$ docker pull irssi@sha256:42f25149c195922ace2d09f52039c56d767996a84e387c8b4eb7cbce5f7c67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51685610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351bf47836b31594adc21aa27395e93d1a031e65d60247048b80b4a4dd12c1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV HOME=/home/user
# Wed, 14 Jan 2026 06:26:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 06:26:49 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 14 Jan 2026 06:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 14 Jan 2026 06:33:37 GMT
WORKDIR /home/user
# Wed, 14 Jan 2026 06:33:37 GMT
USER user
# Wed, 14 Jan 2026 06:33:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f9ee6f39e761595d5c9e020ae1fb10f95fe2a2951aa757f6de57a94a5d25ab`  
		Last Modified: Wed, 14 Jan 2026 06:35:34 GMT  
		Size: 18.5 MB (18549843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef5f232538194de0e7b47d1c08ae77477427a3951186780b1f80e4a91600b4`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b07d932aff1dc5ee2440e07ea368a0ddb73f2c32cb1a8ab0bfd881b02a53f7`  
		Last Modified: Wed, 14 Jan 2026 06:35:31 GMT  
		Size: 4.9 MB (4860721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:0d0a172cbd5471aa3ec8392dc55c5bad0e4fe5bb8e39202b61a8ad6e7252ed2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f4f48da90e6ab7c83ee1b3d3d3112e940971d8bcbed03f47ee03a7d5cca5a6`

```dockerfile
```

-	Layers:
	-	`sha256:afd4f3e89883cc18160c077e4faf0da05c4455d6e0cf0af04a7f525621cba93f`  
		Last Modified: Wed, 14 Jan 2026 06:35:31 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7e2d6743dc6628d707a2e9780dc009b06754202d718210a4e2690ed143c0b`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:3507e27e096139e6c53256b46253b87c2add6684f0a537a81456df935df58f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54507448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9bb61ec181683066bef513d8c48742e3a8098735e181c1c3fff70935a09bd6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:19:25 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:20:02 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:20:02 GMT
USER user
# Tue, 03 Feb 2026 02:20:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8905651585d3b136c5d623c620a4b7471b9176370e9badfa69aa86ab3b0b2771`  
		Last Modified: Tue, 03 Feb 2026 02:20:19 GMT  
		Size: 19.8 MB (19760098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b071b126b87f268a0a29ba9f9fe74d76c9af662cee154d5c7726aae6103dc5c2`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2057418f122012d53f3e9dc13ad0f4d67e6c354b177c2e3cff726f0259e435ff`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 4.9 MB (4905841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:3fb068ad5665041ed11698505383bd5effcaa6e7a9de68a793f560dcdbd63930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7848dc8f3f1945a579bb92f67c19f8ef6b9817196a982d578c50208a9d0cb6f`

```dockerfile
```

-	Layers:
	-	`sha256:90c9b6efea1e9a1c048095f2ecb0af339f8475c5029d9074730a486e02732943`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67606c2343b9ace2f5fd62625eb54620eac701413090a31982ee610dcd1e006f`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:bc9744c4e1f3c9e4401ee35e73ff4f7c97683f5c784c5cce21910e488a4ee219
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
$ docker pull irssi@sha256:84665fb63540b0ca94547800ed0093cb97d41e1cbc0d2aa823a67e6af91fe8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20784026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6645503b9d588217c1fb06c9a2d7e278a4360e4aa22e92d8ff0af44ac2c6c10`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:47 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:47 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:47 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65c05b32f228b7007340211a175e100ca3ddb33a7e2c44b15d11799a9a84ad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 10.9 MB (10857996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c32a8914140e457d67603de3b04ccc66e688baed84d8d500f40dc885ef27a`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93abf1ed0403fdbc85fa021598a1202b3d9b55bd9d785457b554af6b86fc7d`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 6.1 MB (6063223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:7bd9c1f9350891fb6e79ac3dc4d7686c1c714bb2c12147cb089864d19ef3bc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e29e513927a47425fe64b68ba4eeb03593581de0692a732211bc7b11537936`

```dockerfile
```

-	Layers:
	-	`sha256:5d4ee629f31bfb597346562d7da53858808c502ca6820fb40a7c347520afebad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b9c1c09e72415a3ca7367aec0652ca69a856b8c6a57ef69ba919d208498b76`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:9a8babd75444eea65ebe3a06627eceb16f4d50aec2da2998fd3a611d75ed5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04e50bc1d87804658a7d29a7ebb00b20d1a22d6d21cd19f5eff93f84035eb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:23:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:23:57 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:24:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:24:17 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:24:17 GMT
USER user
# Wed, 28 Jan 2026 02:24:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5c4e6a80a684ff34083f2ded6ae6a1b0f08ded4c8c5b0967f8b209ee2cd80`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 10.1 MB (10075626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93db171eca68243a4f689b5400ef3c2ac2a1074f1eae1f9f0d049506c8756fe`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c8c890839d95ebaf447485d8492d089fc8fa23d1ca65c6349a41ac95bc961`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 5.9 MB (5893116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:424e17d1ca73b3f1d92e5d0c0b7272bbaeee943cc673a2249f0bf7ca99eeedde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7bd514eeda8663e46d4eeed484d7df02209f60112393607269af3e2c0430c`

```dockerfile
```

-	Layers:
	-	`sha256:8fbda3c9e4c0ad20ecba339d117fab2e86108fcfe33cbba7f8ddc3053d6bc89a`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:42ff91c7e5cb5046e91c18adce476ce64e5d772ab658a70c9df46e592b10ce82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18828366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ac84c98bbbaf189bedd8109f71397874c887df2e4eb32123f05470b88358b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:21 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:22:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:22:22 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:22:37 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:22:37 GMT
USER user
# Wed, 28 Jan 2026 02:22:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ae8f3941338d2191aad9429d0bd185ceeb7aeedb8fddf43adad6b57e3273e`  
		Last Modified: Wed, 28 Jan 2026 02:22:45 GMT  
		Size: 9.9 MB (9902405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770acb73451dc424aeb5afcad4a4882f5d765fcbcc8b659b8841bf77d8166afe`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda40971fe170d5e56e81f398ba01d1904a08b07386da11fe56b125109dd60b9`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 5.6 MB (5643252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:fcebcd556b705ae5c410e6b569b01096b561714c5c2fc1d7c8c746decaeef0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d96801a2a79a245717287e0380350d8e1b0c44936b6dcaf8429b0e2074bab`

```dockerfile
```

-	Layers:
	-	`sha256:e0caf0a4bbae914fea3e8ffab5d1f1752e3fc858d38e993806dd2b78f6919657`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda69d589c766de3e44adc56d464708c1c2090577cfe6fdd9a50f95229a2c4fa`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c53ef5cb4c4fb78d4ffdaad1b902adc24327fb49d4ad5c6d719dcf26f8e1ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20927195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538037fb15131e4b2540ac0e275393593929c95a1ca622c94e6c70d99874f28`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628108c2cc8068dbd74588362d3734d7b6b306883916eb33cb53af667c096440`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 10.8 MB (10792790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9361ffc4206f8e272dc8adc782da4ab39f3b1fe287c6dfb23c57814cf1e94439`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7efe759a9de929b3a25440ff73ac10595ac218ae5d0a087f34fa385d7db181f`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 5.9 MB (5936327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ac959328037122478f2c09228cf4478f1c099d3257efec2dae9823db1d16b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db6c23ab4cfc36c7b70e7f4325b9bfa25d1a31a205c632f8e25757cb01f7cef`

```dockerfile
```

-	Layers:
	-	`sha256:3b09e8c286f81074ecdbaaeccccef453ddf9951ff459e4c086e01b8968fe3b0e`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57974d8beacb812f7bb8f7b52301ddd6a66eb7f4c851dcc2ee58f100ec0208b1`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:a32c16d5607a49617e8d077ec1f9ba5b53b0001a5d70805f183e27ac8f377955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20225669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7946f5f999880045f35ea6c3b7115f7cc7ca872f2653f90c5b0a114ea701599b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:16:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:16:14 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:16:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:16:34 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:16:34 GMT
USER user
# Wed, 28 Jan 2026 02:16:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50882b3c493b99635b6de6cd7279fc00a7df160e84cd53399664993828611810`  
		Last Modified: Wed, 28 Jan 2026 02:16:41 GMT  
		Size: 10.4 MB (10393535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588c02c444f10953a0f0aac9fa979fe4a835bbefde822557708fbd3d21750de`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dcb0c68d5a17e86130988d6ddf97978ae4c3d866b099962426d869a1c1fc3`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 6.1 MB (6144150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b77b6da6595a9c4ebfe003d3192b1a97bd9a14f1fe19417ad4a8d7068acc0505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f268d469cb9fcc79cb87b83fdcbadb9fa6818bf4d9c56a441df0e015c2ec6`

```dockerfile
```

-	Layers:
	-	`sha256:1ddc13011deb856a736a8c90df7acab1227398d8a2ae9e4586daa141365096b4`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e26778e3f506818fa4ed452e58334a8e15701f1d896ec8ed2ff3288ca7ecef`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:b40803da860e141ec3ab2320cf224c304aa870a9a884cb362b69e74b6fd82b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21272396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a2c6a98e5b7978e9d4671908d2864a8d58c1b872e5ec279f9a7a67312f3e2b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:32:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:32:11 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:32:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:32:31 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:32:31 GMT
USER user
# Wed, 28 Jan 2026 02:32:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc81a5350f307da5c9651178208c0aa789db44da9179ac834ac469d70ce42cc`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 11.1 MB (11079608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505a6cbf58cbc8474040a9d448a79cab0812b78e3b1c6db13e87987f8e4d9a0`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3296179391416e1833f722cc60f06d3ee4df4255177c36a2f41a35a6ab2661b`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 6.4 MB (6362158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e2ead2561551ba2a279d799d266e484e986d5370478af7155036333e682a1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551e8fca5526f8aa868ce90e80d554f73ff2800bcf6fb3b0fb1b9013223228b5`

```dockerfile
```

-	Layers:
	-	`sha256:890481868cc7de496dcdc1f70cc0d6026227efccdd40466a57aa43304c3e345f`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9fac81ff985d048567933403c842b1d477306de718e7d5226612b3cb1eb068`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:a29b54bd9ab139f5c60185ee85db0a602092a6821866cad82df0fb45368c398c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19942208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9176875f86f8abf3bc20c65b42847d911af0be7e5863f4d6dcbd526719132c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:24:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 08:24:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 08:24:34 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 08:28:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 08:28:23 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 08:28:23 GMT
USER user
# Wed, 28 Jan 2026 08:28:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6c4248bc749950275ce15b2dff82393f4351ced2e20c7b5e2ffef3c0848ce`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 10.3 MB (10291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e176dad2b23e06165e59400a1ff2260014ec93b0fb3b8c7628a64e1adaf49f`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3131351fcf8ddb074fb73d582b50e94aa55e099ca06fc128b310489675e69c97`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 6.1 MB (6064037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:165ef1cc15b3aeae45d6479f80369f8078869b953af00ad6ddb3765a55356e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192140d2d48650b459b2a9acdce6a086c4bf08877b907f3c6bc37ce9799d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:a59cb060f285e8659782eab321b072ac7afdce9472b5395d10144bca9d127b79`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e90caa10ad17b6e48ce9a44b3d010cc7b20e200cbb6ec1067441e247ce555fc`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:e55dc3c7ee83af6ee968373464f0b874c0d9149e01ce32f4680a83b5791d2ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a042dac64e240c543befef410a12767f4051b627b63028b597010c108714083`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:19:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:19:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:20:14 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:20:14 GMT
USER user
# Wed, 28 Jan 2026 02:20:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e174cb7156ade2e31408909452271b26ae4f143ef276276f0f448b1bad2165`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 11.4 MB (11405107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2a6b19294dd14e5551b394d76102c59c84eae810434dca5ae909a1e58da672`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba483b2b5362b1905ca82789be9c963c7fde3135033f6aac9183937e5d9161`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 6.2 MB (6202965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:05475f6695b9e4e1863216bdc5de6a1a24bfec2a5baecd06f9a7bc6cd0d17408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183ed0bc53cc736e214c57eaef2cb864de7e9dbaccf5fe0a5530c72247ac1ab`

```dockerfile
```

-	Layers:
	-	`sha256:c63a0479be024622dc272c05215babf54e4fc3b5c5ab3d053c0dcf2de80483cb`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5037cc7aa93ea1e1f234114cc48a82216f93fe0b9ee46a01ee9a03609cbe19e`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.23`

```console
$ docker pull irssi@sha256:bc9744c4e1f3c9e4401ee35e73ff4f7c97683f5c784c5cce21910e488a4ee219
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

### `irssi:1.4-alpine3.23` - linux; amd64

```console
$ docker pull irssi@sha256:84665fb63540b0ca94547800ed0093cb97d41e1cbc0d2aa823a67e6af91fe8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20784026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6645503b9d588217c1fb06c9a2d7e278a4360e4aa22e92d8ff0af44ac2c6c10`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:47 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:47 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:47 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65c05b32f228b7007340211a175e100ca3ddb33a7e2c44b15d11799a9a84ad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 10.9 MB (10857996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c32a8914140e457d67603de3b04ccc66e688baed84d8d500f40dc885ef27a`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93abf1ed0403fdbc85fa021598a1202b3d9b55bd9d785457b554af6b86fc7d`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 6.1 MB (6063223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:7bd9c1f9350891fb6e79ac3dc4d7686c1c714bb2c12147cb089864d19ef3bc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e29e513927a47425fe64b68ba4eeb03593581de0692a732211bc7b11537936`

```dockerfile
```

-	Layers:
	-	`sha256:5d4ee629f31bfb597346562d7da53858808c502ca6820fb40a7c347520afebad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b9c1c09e72415a3ca7367aec0652ca69a856b8c6a57ef69ba919d208498b76`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:9a8babd75444eea65ebe3a06627eceb16f4d50aec2da2998fd3a611d75ed5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04e50bc1d87804658a7d29a7ebb00b20d1a22d6d21cd19f5eff93f84035eb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:23:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:23:57 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:24:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:24:17 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:24:17 GMT
USER user
# Wed, 28 Jan 2026 02:24:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5c4e6a80a684ff34083f2ded6ae6a1b0f08ded4c8c5b0967f8b209ee2cd80`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 10.1 MB (10075626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93db171eca68243a4f689b5400ef3c2ac2a1074f1eae1f9f0d049506c8756fe`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c8c890839d95ebaf447485d8492d089fc8fa23d1ca65c6349a41ac95bc961`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 5.9 MB (5893116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:424e17d1ca73b3f1d92e5d0c0b7272bbaeee943cc673a2249f0bf7ca99eeedde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7bd514eeda8663e46d4eeed484d7df02209f60112393607269af3e2c0430c`

```dockerfile
```

-	Layers:
	-	`sha256:8fbda3c9e4c0ad20ecba339d117fab2e86108fcfe33cbba7f8ddc3053d6bc89a`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:42ff91c7e5cb5046e91c18adce476ce64e5d772ab658a70c9df46e592b10ce82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18828366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ac84c98bbbaf189bedd8109f71397874c887df2e4eb32123f05470b88358b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:21 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:22:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:22:22 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:22:37 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:22:37 GMT
USER user
# Wed, 28 Jan 2026 02:22:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ae8f3941338d2191aad9429d0bd185ceeb7aeedb8fddf43adad6b57e3273e`  
		Last Modified: Wed, 28 Jan 2026 02:22:45 GMT  
		Size: 9.9 MB (9902405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770acb73451dc424aeb5afcad4a4882f5d765fcbcc8b659b8841bf77d8166afe`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda40971fe170d5e56e81f398ba01d1904a08b07386da11fe56b125109dd60b9`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 5.6 MB (5643252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:fcebcd556b705ae5c410e6b569b01096b561714c5c2fc1d7c8c746decaeef0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d96801a2a79a245717287e0380350d8e1b0c44936b6dcaf8429b0e2074bab`

```dockerfile
```

-	Layers:
	-	`sha256:e0caf0a4bbae914fea3e8ffab5d1f1752e3fc858d38e993806dd2b78f6919657`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda69d589c766de3e44adc56d464708c1c2090577cfe6fdd9a50f95229a2c4fa`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c53ef5cb4c4fb78d4ffdaad1b902adc24327fb49d4ad5c6d719dcf26f8e1ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20927195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538037fb15131e4b2540ac0e275393593929c95a1ca622c94e6c70d99874f28`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628108c2cc8068dbd74588362d3734d7b6b306883916eb33cb53af667c096440`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 10.8 MB (10792790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9361ffc4206f8e272dc8adc782da4ab39f3b1fe287c6dfb23c57814cf1e94439`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7efe759a9de929b3a25440ff73ac10595ac218ae5d0a087f34fa385d7db181f`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 5.9 MB (5936327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:ac959328037122478f2c09228cf4478f1c099d3257efec2dae9823db1d16b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db6c23ab4cfc36c7b70e7f4325b9bfa25d1a31a205c632f8e25757cb01f7cef`

```dockerfile
```

-	Layers:
	-	`sha256:3b09e8c286f81074ecdbaaeccccef453ddf9951ff459e4c086e01b8968fe3b0e`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57974d8beacb812f7bb8f7b52301ddd6a66eb7f4c851dcc2ee58f100ec0208b1`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:a32c16d5607a49617e8d077ec1f9ba5b53b0001a5d70805f183e27ac8f377955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20225669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7946f5f999880045f35ea6c3b7115f7cc7ca872f2653f90c5b0a114ea701599b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:16:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:16:14 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:16:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:16:34 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:16:34 GMT
USER user
# Wed, 28 Jan 2026 02:16:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50882b3c493b99635b6de6cd7279fc00a7df160e84cd53399664993828611810`  
		Last Modified: Wed, 28 Jan 2026 02:16:41 GMT  
		Size: 10.4 MB (10393535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588c02c444f10953a0f0aac9fa979fe4a835bbefde822557708fbd3d21750de`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dcb0c68d5a17e86130988d6ddf97978ae4c3d866b099962426d869a1c1fc3`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 6.1 MB (6144150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:b77b6da6595a9c4ebfe003d3192b1a97bd9a14f1fe19417ad4a8d7068acc0505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f268d469cb9fcc79cb87b83fdcbadb9fa6818bf4d9c56a441df0e015c2ec6`

```dockerfile
```

-	Layers:
	-	`sha256:1ddc13011deb856a736a8c90df7acab1227398d8a2ae9e4586daa141365096b4`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e26778e3f506818fa4ed452e58334a8e15701f1d896ec8ed2ff3288ca7ecef`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:b40803da860e141ec3ab2320cf224c304aa870a9a884cb362b69e74b6fd82b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21272396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a2c6a98e5b7978e9d4671908d2864a8d58c1b872e5ec279f9a7a67312f3e2b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:32:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:32:11 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:32:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:32:31 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:32:31 GMT
USER user
# Wed, 28 Jan 2026 02:32:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc81a5350f307da5c9651178208c0aa789db44da9179ac834ac469d70ce42cc`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 11.1 MB (11079608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505a6cbf58cbc8474040a9d448a79cab0812b78e3b1c6db13e87987f8e4d9a0`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3296179391416e1833f722cc60f06d3ee4df4255177c36a2f41a35a6ab2661b`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 6.4 MB (6362158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:e2ead2561551ba2a279d799d266e484e986d5370478af7155036333e682a1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551e8fca5526f8aa868ce90e80d554f73ff2800bcf6fb3b0fb1b9013223228b5`

```dockerfile
```

-	Layers:
	-	`sha256:890481868cc7de496dcdc1f70cc0d6026227efccdd40466a57aa43304c3e345f`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9fac81ff985d048567933403c842b1d477306de718e7d5226612b3cb1eb068`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:a29b54bd9ab139f5c60185ee85db0a602092a6821866cad82df0fb45368c398c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19942208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9176875f86f8abf3bc20c65b42847d911af0be7e5863f4d6dcbd526719132c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:24:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 08:24:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 08:24:34 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 08:28:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 08:28:23 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 08:28:23 GMT
USER user
# Wed, 28 Jan 2026 08:28:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6c4248bc749950275ce15b2dff82393f4351ced2e20c7b5e2ffef3c0848ce`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 10.3 MB (10291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e176dad2b23e06165e59400a1ff2260014ec93b0fb3b8c7628a64e1adaf49f`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3131351fcf8ddb074fb73d582b50e94aa55e099ca06fc128b310489675e69c97`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 6.1 MB (6064037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:165ef1cc15b3aeae45d6479f80369f8078869b953af00ad6ddb3765a55356e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192140d2d48650b459b2a9acdce6a086c4bf08877b907f3c6bc37ce9799d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:a59cb060f285e8659782eab321b072ac7afdce9472b5395d10144bca9d127b79`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e90caa10ad17b6e48ce9a44b3d010cc7b20e200cbb6ec1067441e247ce555fc`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:e55dc3c7ee83af6ee968373464f0b874c0d9149e01ce32f4680a83b5791d2ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a042dac64e240c543befef410a12767f4051b627b63028b597010c108714083`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:19:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:19:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:20:14 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:20:14 GMT
USER user
# Wed, 28 Jan 2026 02:20:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e174cb7156ade2e31408909452271b26ae4f143ef276276f0f448b1bad2165`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 11.4 MB (11405107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2a6b19294dd14e5551b394d76102c59c84eae810434dca5ae909a1e58da672`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba483b2b5362b1905ca82789be9c963c7fde3135033f6aac9183937e5d9161`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 6.2 MB (6202965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:05475f6695b9e4e1863216bdc5de6a1a24bfec2a5baecd06f9a7bc6cd0d17408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183ed0bc53cc736e214c57eaef2cb864de7e9dbaccf5fe0a5530c72247ac1ab`

```dockerfile
```

-	Layers:
	-	`sha256:c63a0479be024622dc272c05215babf54e4fc3b5c5ab3d053c0dcf2de80483cb`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5037cc7aa93ea1e1f234114cc48a82216f93fe0b9ee46a01ee9a03609cbe19e`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-trixie`

```console
$ docker pull irssi@sha256:609a2ed50953d52717592390ee3e98c01c9d73570d22d00bae780781a867411d
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
$ docker pull irssi@sha256:9fae60e7bc9fc24c9db14714ff3340dec77f5694a9c1b466a89d06b539eed73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53870996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208ed2331d877493655ffbf5715d5ee7e7b1f90234b46c4b6347d2f3fe5616b9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:21:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:21:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:21:59 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:21:59 GMT
USER user
# Tue, 03 Feb 2026 02:21:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30e33e354d1d7dda77aaf4af795ff38369ad98bc285f7ba38494d0eda9abb20`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 19.2 MB (19222126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca5a9fa5a0439cd4c3a67c55dd77ab262eaaf8fe3e4f572652f807ae50717fe`  
		Last Modified: Tue, 03 Feb 2026 02:22:08 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7eb220ebedbb0676c3eece8a52277bc0f8d265bb6dc86c6b4c0257d1248723`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 4.9 MB (4866910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:a799ddd3de8dca67e18842b9f3100c61f8e0f40248eec47e9c7d6f7cc5a671e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e411b3f5abbc6ddcbca19c4a0c1521f22b4c249b1349aa45a8611fef7d303416`

```dockerfile
```

-	Layers:
	-	`sha256:293943398617ea6ecaaefceca69694c212fd62ab6e2486655ba0c29e0ae2ba79`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0f10970bd82463907455a4e67a02508285f5300f0993369c217f187ad257c4`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:01a370482e82c1514a233b8e1154c4eeb7e1e29779ed1cfbe0ea72fea926beb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50948888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d3a4cb61f731180f34b3940bbac33a2e24aa2d6dd90ca8e9000be255fe00ee`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:36 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:17:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:17:36 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:18:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:18:24 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:18:24 GMT
USER user
# Tue, 03 Feb 2026 02:18:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bff507cc72771f546378d6ffea702ce1dfc5f7462c98cf416495c9ea7abf5d7`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 18.3 MB (18287991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b732dda1c983c4e5532a6724cc0691bb7f0d4966d926b8031665b9eb19bdf2f4`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe09db28a7bba924a281417665350a9244ac5212bd2c077490813e7355165af`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 4.7 MB (4709982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:02c91f1c49e783ce02db737a1e321704df556858a8ad779ea708f8e801327d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d96f2236d0bf313e468cac657716937a2916282fb27192e905a3ca5780053c9`

```dockerfile
```

-	Layers:
	-	`sha256:c8fb39701e198922668819c0230131b6ae48c12a1d5b030b29d0a2eb4f184198`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69d1c7aa44d9df7724589bd6968e57bcd952b965d7dd14e01f8a0dd52b3fe8c8`  
		Last Modified: Tue, 03 Feb 2026 02:18:34 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:9bd66f1060f9a00e3c4e0bef5e1eeea789fc5f4c5b409aefc8bbcf3135f7dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48685426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9e9708bc24170126dd456a2b01d0c0f067c248903162e7c96091af2380b044`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:20:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:19 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:20:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:20:19 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:20:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:20:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:20:59 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:20:59 GMT
USER user
# Tue, 03 Feb 2026 02:20:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64c57598d1759ed47b0ce33fe2ae3f2ca5dfc344280bee5c91a6e2c2cfc33b`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 17.9 MB (17909993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15370f82ce37fd15003721575f11cd865da7261620aea2b1159317aab5659913`  
		Last Modified: Tue, 03 Feb 2026 02:21:09 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420081012ce7d68e8a87df2713f5901aacfc0a3a49fe4f2ac8aa2e0825c8352`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 4.6 MB (4558319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6849872da14db17e8b671bdfc642713a76fa2d2017b4ee56049715165db3c076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc1f967ef5736068697a132ec3311efa1a7280ec42fdaa1ed74a8029aac60bf`

```dockerfile
```

-	Layers:
	-	`sha256:b50b6b2a3c6822bb550588172036e08689e2b19d58f855b5606aded3012602bf`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0382a272fccc29001becae9a6ec2fb967f63ffe7d998d793f67a4ff9b9bfd7e`  
		Last Modified: Tue, 03 Feb 2026 02:21:09 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0e6173a8c52441af65097628532330fc826392fa4253e42657ec878c175208c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53975585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb379b987ac880b692fe2dc3dfd931da9c788161033c4e06239554bb4224eb9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:00 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:21:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:21:00 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:21:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:21:38 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:21:38 GMT
USER user
# Tue, 03 Feb 2026 02:21:38 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0532516bbb7262501000c326f37a0930c04d5f5a6565e14b1190d60f0743ce25`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 19.1 MB (19050649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6975dc48bed2afc9f4f4bd9b1665965ae2863eb4ff8cda14ac16f304476d307d`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d6ba22ebad57591e22d79dd65abfa638d56640df56deb4bf8cceb64e95620b`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 4.8 MB (4781508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2dcaadbe83c3a2a93746c56b19d9f055a7f01810e40da8786b5e2a69a843d506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c18f2b03173ce70e0ebf01ac9749a910865184a273ace4b2b75d21222b7118`

```dockerfile
```

-	Layers:
	-	`sha256:7457b4c9d09e256e51f29dec29c3e51469b7ad175435b171f9c5d18d9599cc7b`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff3cd880792431a74dcfdc01b30e2c7bd58e08261221840c6a483be5f9b07ee`  
		Last Modified: Tue, 03 Feb 2026 02:21:47 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; 386

```console
$ docker pull irssi@sha256:d10f5d01b9d383d32f36d497a37e76510561eeeaab8a38217dc142bd2044d611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54909414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccf4252e90be99c5c6384e8ef46f99bd42f9232af75a666a85cc7b80be93dbb`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:34 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:17:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:17:34 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:18:17 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:18:17 GMT
USER user
# Tue, 03 Feb 2026 02:18:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c57cfac3b918f6dafe14bf68c93d7d16a8a4970051d18d2a06c2a0263c9145`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 18.7 MB (18743761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c5a3109babbf5c2a1d4b41cb629cbbf8d5c31b10a16a624d77a5dc4bcc39f`  
		Last Modified: Tue, 03 Feb 2026 02:18:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcbe0576fcf1e6208897d40292c8c455af77f42a3cc963ffaff8613d1ca39c1`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 4.9 MB (4868437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:426742b8e02f677fc2e475fb401cbef173d80d0e52b05e495a053dbe62b14c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47fcdb26283af7bd047252c4c37d59277a0cd6d06d787227002528e3c365a58`

```dockerfile
```

-	Layers:
	-	`sha256:a288faa1621c022dd6bd996b78e6eb5d6ee3897b462366f28ee4c3f8bfd9caca`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8db18756472041642ed74f8e1e2ae8db1340756b5fde16825cc70e1a163b56`  
		Last Modified: Tue, 03 Feb 2026 02:18:26 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:55ac6c8d4f6d789fcd2f9caaeb13ce48d776a469d82747e7c1485b5963b19dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58244327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a843d5494442193be8285e2518e0cc0dc17b289884fe2369582b93b61eab8`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:24:37 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:24:37 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:24:37 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:24:37 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:26:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:26:23 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:26:23 GMT
USER user
# Tue, 03 Feb 2026 02:26:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624f9309218047b5688e03740c3f3ec04d0a5b2e096ba1ddb57f22215b1c032e`  
		Last Modified: Tue, 03 Feb 2026 02:26:45 GMT  
		Size: 19.5 MB (19542944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b058eb5982a30c68c6eeb3fddcc4f27b629549cbc9517db75d48bcb1f65cdf`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3765444fdfedf57570813f65ad00dcb9587c7a838f36605feb402e11e81f9b`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 5.1 MB (5097836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:5052a03b5d5ed94c58e1b40d85bcc9e57efe762b73218ad11c008c90311225db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee428904aef2658d2ef8892ffdd5bd384860d0da7ee3179246ea48246a6a9b50`

```dockerfile
```

-	Layers:
	-	`sha256:2fa98124d99ee2944a940c9389ee640f1cd7264bd06b18eac34eea4ceaf8efd6`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3e4620f46fdeae2fb275ccc948845b0e4a8862b657cff3de65766f5fd7fa1e`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:42f25149c195922ace2d09f52039c56d767996a84e387c8b4eb7cbce5f7c67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51685610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351bf47836b31594adc21aa27395e93d1a031e65d60247048b80b4a4dd12c1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV HOME=/home/user
# Wed, 14 Jan 2026 06:26:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 06:26:49 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 14 Jan 2026 06:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 14 Jan 2026 06:33:37 GMT
WORKDIR /home/user
# Wed, 14 Jan 2026 06:33:37 GMT
USER user
# Wed, 14 Jan 2026 06:33:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f9ee6f39e761595d5c9e020ae1fb10f95fe2a2951aa757f6de57a94a5d25ab`  
		Last Modified: Wed, 14 Jan 2026 06:35:34 GMT  
		Size: 18.5 MB (18549843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef5f232538194de0e7b47d1c08ae77477427a3951186780b1f80e4a91600b4`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b07d932aff1dc5ee2440e07ea368a0ddb73f2c32cb1a8ab0bfd881b02a53f7`  
		Last Modified: Wed, 14 Jan 2026 06:35:31 GMT  
		Size: 4.9 MB (4860721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:0d0a172cbd5471aa3ec8392dc55c5bad0e4fe5bb8e39202b61a8ad6e7252ed2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f4f48da90e6ab7c83ee1b3d3d3112e940971d8bcbed03f47ee03a7d5cca5a6`

```dockerfile
```

-	Layers:
	-	`sha256:afd4f3e89883cc18160c077e4faf0da05c4455d6e0cf0af04a7f525621cba93f`  
		Last Modified: Wed, 14 Jan 2026 06:35:31 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7e2d6743dc6628d707a2e9780dc009b06754202d718210a4e2690ed143c0b`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:3507e27e096139e6c53256b46253b87c2add6684f0a537a81456df935df58f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54507448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9bb61ec181683066bef513d8c48742e3a8098735e181c1c3fff70935a09bd6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:19:25 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:20:02 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:20:02 GMT
USER user
# Tue, 03 Feb 2026 02:20:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8905651585d3b136c5d623c620a4b7471b9176370e9badfa69aa86ab3b0b2771`  
		Last Modified: Tue, 03 Feb 2026 02:20:19 GMT  
		Size: 19.8 MB (19760098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b071b126b87f268a0a29ba9f9fe74d76c9af662cee154d5c7726aae6103dc5c2`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2057418f122012d53f3e9dc13ad0f4d67e6c354b177c2e3cff726f0259e435ff`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 4.9 MB (4905841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:3fb068ad5665041ed11698505383bd5effcaa6e7a9de68a793f560dcdbd63930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7848dc8f3f1945a579bb92f67c19f8ef6b9817196a982d578c50208a9d0cb6f`

```dockerfile
```

-	Layers:
	-	`sha256:90c9b6efea1e9a1c048095f2ecb0af339f8475c5029d9074730a486e02732943`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67606c2343b9ace2f5fd62625eb54620eac701413090a31982ee610dcd1e006f`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:609a2ed50953d52717592390ee3e98c01c9d73570d22d00bae780781a867411d
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
$ docker pull irssi@sha256:9fae60e7bc9fc24c9db14714ff3340dec77f5694a9c1b466a89d06b539eed73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53870996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208ed2331d877493655ffbf5715d5ee7e7b1f90234b46c4b6347d2f3fe5616b9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:21:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:21:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:21:59 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:21:59 GMT
USER user
# Tue, 03 Feb 2026 02:21:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30e33e354d1d7dda77aaf4af795ff38369ad98bc285f7ba38494d0eda9abb20`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 19.2 MB (19222126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca5a9fa5a0439cd4c3a67c55dd77ab262eaaf8fe3e4f572652f807ae50717fe`  
		Last Modified: Tue, 03 Feb 2026 02:22:08 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7eb220ebedbb0676c3eece8a52277bc0f8d265bb6dc86c6b4c0257d1248723`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 4.9 MB (4866910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:a799ddd3de8dca67e18842b9f3100c61f8e0f40248eec47e9c7d6f7cc5a671e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e411b3f5abbc6ddcbca19c4a0c1521f22b4c249b1349aa45a8611fef7d303416`

```dockerfile
```

-	Layers:
	-	`sha256:293943398617ea6ecaaefceca69694c212fd62ab6e2486655ba0c29e0ae2ba79`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0f10970bd82463907455a4e67a02508285f5300f0993369c217f187ad257c4`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:01a370482e82c1514a233b8e1154c4eeb7e1e29779ed1cfbe0ea72fea926beb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50948888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d3a4cb61f731180f34b3940bbac33a2e24aa2d6dd90ca8e9000be255fe00ee`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:36 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:17:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:17:36 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:18:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:18:24 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:18:24 GMT
USER user
# Tue, 03 Feb 2026 02:18:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bff507cc72771f546378d6ffea702ce1dfc5f7462c98cf416495c9ea7abf5d7`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 18.3 MB (18287991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b732dda1c983c4e5532a6724cc0691bb7f0d4966d926b8031665b9eb19bdf2f4`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe09db28a7bba924a281417665350a9244ac5212bd2c077490813e7355165af`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 4.7 MB (4709982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:02c91f1c49e783ce02db737a1e321704df556858a8ad779ea708f8e801327d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d96f2236d0bf313e468cac657716937a2916282fb27192e905a3ca5780053c9`

```dockerfile
```

-	Layers:
	-	`sha256:c8fb39701e198922668819c0230131b6ae48c12a1d5b030b29d0a2eb4f184198`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69d1c7aa44d9df7724589bd6968e57bcd952b965d7dd14e01f8a0dd52b3fe8c8`  
		Last Modified: Tue, 03 Feb 2026 02:18:34 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:9bd66f1060f9a00e3c4e0bef5e1eeea789fc5f4c5b409aefc8bbcf3135f7dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48685426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9e9708bc24170126dd456a2b01d0c0f067c248903162e7c96091af2380b044`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:20:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:19 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:20:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:20:19 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:20:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:20:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:20:59 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:20:59 GMT
USER user
# Tue, 03 Feb 2026 02:20:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64c57598d1759ed47b0ce33fe2ae3f2ca5dfc344280bee5c91a6e2c2cfc33b`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 17.9 MB (17909993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15370f82ce37fd15003721575f11cd865da7261620aea2b1159317aab5659913`  
		Last Modified: Tue, 03 Feb 2026 02:21:09 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420081012ce7d68e8a87df2713f5901aacfc0a3a49fe4f2ac8aa2e0825c8352`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 4.6 MB (4558319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:6849872da14db17e8b671bdfc642713a76fa2d2017b4ee56049715165db3c076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc1f967ef5736068697a132ec3311efa1a7280ec42fdaa1ed74a8029aac60bf`

```dockerfile
```

-	Layers:
	-	`sha256:b50b6b2a3c6822bb550588172036e08689e2b19d58f855b5606aded3012602bf`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0382a272fccc29001becae9a6ec2fb967f63ffe7d998d793f67a4ff9b9bfd7e`  
		Last Modified: Tue, 03 Feb 2026 02:21:09 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0e6173a8c52441af65097628532330fc826392fa4253e42657ec878c175208c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53975585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb379b987ac880b692fe2dc3dfd931da9c788161033c4e06239554bb4224eb9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:00 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:21:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:21:00 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:21:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:21:38 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:21:38 GMT
USER user
# Tue, 03 Feb 2026 02:21:38 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0532516bbb7262501000c326f37a0930c04d5f5a6565e14b1190d60f0743ce25`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 19.1 MB (19050649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6975dc48bed2afc9f4f4bd9b1665965ae2863eb4ff8cda14ac16f304476d307d`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d6ba22ebad57591e22d79dd65abfa638d56640df56deb4bf8cceb64e95620b`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 4.8 MB (4781508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:2dcaadbe83c3a2a93746c56b19d9f055a7f01810e40da8786b5e2a69a843d506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c18f2b03173ce70e0ebf01ac9749a910865184a273ace4b2b75d21222b7118`

```dockerfile
```

-	Layers:
	-	`sha256:7457b4c9d09e256e51f29dec29c3e51469b7ad175435b171f9c5d18d9599cc7b`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff3cd880792431a74dcfdc01b30e2c7bd58e08261221840c6a483be5f9b07ee`  
		Last Modified: Tue, 03 Feb 2026 02:21:47 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:d10f5d01b9d383d32f36d497a37e76510561eeeaab8a38217dc142bd2044d611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54909414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccf4252e90be99c5c6384e8ef46f99bd42f9232af75a666a85cc7b80be93dbb`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:34 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:17:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:17:34 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:18:17 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:18:17 GMT
USER user
# Tue, 03 Feb 2026 02:18:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c57cfac3b918f6dafe14bf68c93d7d16a8a4970051d18d2a06c2a0263c9145`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 18.7 MB (18743761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c5a3109babbf5c2a1d4b41cb629cbbf8d5c31b10a16a624d77a5dc4bcc39f`  
		Last Modified: Tue, 03 Feb 2026 02:18:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcbe0576fcf1e6208897d40292c8c455af77f42a3cc963ffaff8613d1ca39c1`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 4.9 MB (4868437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:426742b8e02f677fc2e475fb401cbef173d80d0e52b05e495a053dbe62b14c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47fcdb26283af7bd047252c4c37d59277a0cd6d06d787227002528e3c365a58`

```dockerfile
```

-	Layers:
	-	`sha256:a288faa1621c022dd6bd996b78e6eb5d6ee3897b462366f28ee4c3f8bfd9caca`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8db18756472041642ed74f8e1e2ae8db1340756b5fde16825cc70e1a163b56`  
		Last Modified: Tue, 03 Feb 2026 02:18:26 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:55ac6c8d4f6d789fcd2f9caaeb13ce48d776a469d82747e7c1485b5963b19dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58244327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a843d5494442193be8285e2518e0cc0dc17b289884fe2369582b93b61eab8`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:24:37 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:24:37 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:24:37 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:24:37 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:26:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:26:23 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:26:23 GMT
USER user
# Tue, 03 Feb 2026 02:26:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624f9309218047b5688e03740c3f3ec04d0a5b2e096ba1ddb57f22215b1c032e`  
		Last Modified: Tue, 03 Feb 2026 02:26:45 GMT  
		Size: 19.5 MB (19542944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b058eb5982a30c68c6eeb3fddcc4f27b629549cbc9517db75d48bcb1f65cdf`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3765444fdfedf57570813f65ad00dcb9587c7a838f36605feb402e11e81f9b`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 5.1 MB (5097836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:5052a03b5d5ed94c58e1b40d85bcc9e57efe762b73218ad11c008c90311225db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee428904aef2658d2ef8892ffdd5bd384860d0da7ee3179246ea48246a6a9b50`

```dockerfile
```

-	Layers:
	-	`sha256:2fa98124d99ee2944a940c9389ee640f1cd7264bd06b18eac34eea4ceaf8efd6`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3e4620f46fdeae2fb275ccc948845b0e4a8862b657cff3de65766f5fd7fa1e`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; riscv64

```console
$ docker pull irssi@sha256:42f25149c195922ace2d09f52039c56d767996a84e387c8b4eb7cbce5f7c67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51685610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351bf47836b31594adc21aa27395e93d1a031e65d60247048b80b4a4dd12c1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV HOME=/home/user
# Wed, 14 Jan 2026 06:26:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 06:26:49 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 14 Jan 2026 06:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 14 Jan 2026 06:33:37 GMT
WORKDIR /home/user
# Wed, 14 Jan 2026 06:33:37 GMT
USER user
# Wed, 14 Jan 2026 06:33:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f9ee6f39e761595d5c9e020ae1fb10f95fe2a2951aa757f6de57a94a5d25ab`  
		Last Modified: Wed, 14 Jan 2026 06:35:34 GMT  
		Size: 18.5 MB (18549843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef5f232538194de0e7b47d1c08ae77477427a3951186780b1f80e4a91600b4`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b07d932aff1dc5ee2440e07ea368a0ddb73f2c32cb1a8ab0bfd881b02a53f7`  
		Last Modified: Wed, 14 Jan 2026 06:35:31 GMT  
		Size: 4.9 MB (4860721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:0d0a172cbd5471aa3ec8392dc55c5bad0e4fe5bb8e39202b61a8ad6e7252ed2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f4f48da90e6ab7c83ee1b3d3d3112e940971d8bcbed03f47ee03a7d5cca5a6`

```dockerfile
```

-	Layers:
	-	`sha256:afd4f3e89883cc18160c077e4faf0da05c4455d6e0cf0af04a7f525621cba93f`  
		Last Modified: Wed, 14 Jan 2026 06:35:31 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7e2d6743dc6628d707a2e9780dc009b06754202d718210a4e2690ed143c0b`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:3507e27e096139e6c53256b46253b87c2add6684f0a537a81456df935df58f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54507448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9bb61ec181683066bef513d8c48742e3a8098735e181c1c3fff70935a09bd6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:19:25 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:20:02 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:20:02 GMT
USER user
# Tue, 03 Feb 2026 02:20:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8905651585d3b136c5d623c620a4b7471b9176370e9badfa69aa86ab3b0b2771`  
		Last Modified: Tue, 03 Feb 2026 02:20:19 GMT  
		Size: 19.8 MB (19760098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b071b126b87f268a0a29ba9f9fe74d76c9af662cee154d5c7726aae6103dc5c2`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2057418f122012d53f3e9dc13ad0f4d67e6c354b177c2e3cff726f0259e435ff`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 4.9 MB (4905841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:3fb068ad5665041ed11698505383bd5effcaa6e7a9de68a793f560dcdbd63930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7848dc8f3f1945a579bb92f67c19f8ef6b9817196a982d578c50208a9d0cb6f`

```dockerfile
```

-	Layers:
	-	`sha256:90c9b6efea1e9a1c048095f2ecb0af339f8475c5029d9074730a486e02732943`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67606c2343b9ace2f5fd62625eb54620eac701413090a31982ee610dcd1e006f`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:bc9744c4e1f3c9e4401ee35e73ff4f7c97683f5c784c5cce21910e488a4ee219
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
$ docker pull irssi@sha256:84665fb63540b0ca94547800ed0093cb97d41e1cbc0d2aa823a67e6af91fe8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20784026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6645503b9d588217c1fb06c9a2d7e278a4360e4aa22e92d8ff0af44ac2c6c10`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:47 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:47 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:47 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65c05b32f228b7007340211a175e100ca3ddb33a7e2c44b15d11799a9a84ad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 10.9 MB (10857996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c32a8914140e457d67603de3b04ccc66e688baed84d8d500f40dc885ef27a`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93abf1ed0403fdbc85fa021598a1202b3d9b55bd9d785457b554af6b86fc7d`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 6.1 MB (6063223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:7bd9c1f9350891fb6e79ac3dc4d7686c1c714bb2c12147cb089864d19ef3bc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e29e513927a47425fe64b68ba4eeb03593581de0692a732211bc7b11537936`

```dockerfile
```

-	Layers:
	-	`sha256:5d4ee629f31bfb597346562d7da53858808c502ca6820fb40a7c347520afebad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b9c1c09e72415a3ca7367aec0652ca69a856b8c6a57ef69ba919d208498b76`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:9a8babd75444eea65ebe3a06627eceb16f4d50aec2da2998fd3a611d75ed5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04e50bc1d87804658a7d29a7ebb00b20d1a22d6d21cd19f5eff93f84035eb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:23:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:23:57 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:24:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:24:17 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:24:17 GMT
USER user
# Wed, 28 Jan 2026 02:24:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5c4e6a80a684ff34083f2ded6ae6a1b0f08ded4c8c5b0967f8b209ee2cd80`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 10.1 MB (10075626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93db171eca68243a4f689b5400ef3c2ac2a1074f1eae1f9f0d049506c8756fe`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c8c890839d95ebaf447485d8492d089fc8fa23d1ca65c6349a41ac95bc961`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 5.9 MB (5893116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:424e17d1ca73b3f1d92e5d0c0b7272bbaeee943cc673a2249f0bf7ca99eeedde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7bd514eeda8663e46d4eeed484d7df02209f60112393607269af3e2c0430c`

```dockerfile
```

-	Layers:
	-	`sha256:8fbda3c9e4c0ad20ecba339d117fab2e86108fcfe33cbba7f8ddc3053d6bc89a`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:42ff91c7e5cb5046e91c18adce476ce64e5d772ab658a70c9df46e592b10ce82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18828366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ac84c98bbbaf189bedd8109f71397874c887df2e4eb32123f05470b88358b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:21 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:22:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:22:22 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:22:37 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:22:37 GMT
USER user
# Wed, 28 Jan 2026 02:22:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ae8f3941338d2191aad9429d0bd185ceeb7aeedb8fddf43adad6b57e3273e`  
		Last Modified: Wed, 28 Jan 2026 02:22:45 GMT  
		Size: 9.9 MB (9902405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770acb73451dc424aeb5afcad4a4882f5d765fcbcc8b659b8841bf77d8166afe`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda40971fe170d5e56e81f398ba01d1904a08b07386da11fe56b125109dd60b9`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 5.6 MB (5643252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:fcebcd556b705ae5c410e6b569b01096b561714c5c2fc1d7c8c746decaeef0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d96801a2a79a245717287e0380350d8e1b0c44936b6dcaf8429b0e2074bab`

```dockerfile
```

-	Layers:
	-	`sha256:e0caf0a4bbae914fea3e8ffab5d1f1752e3fc858d38e993806dd2b78f6919657`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda69d589c766de3e44adc56d464708c1c2090577cfe6fdd9a50f95229a2c4fa`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c53ef5cb4c4fb78d4ffdaad1b902adc24327fb49d4ad5c6d719dcf26f8e1ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20927195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538037fb15131e4b2540ac0e275393593929c95a1ca622c94e6c70d99874f28`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628108c2cc8068dbd74588362d3734d7b6b306883916eb33cb53af667c096440`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 10.8 MB (10792790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9361ffc4206f8e272dc8adc782da4ab39f3b1fe287c6dfb23c57814cf1e94439`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7efe759a9de929b3a25440ff73ac10595ac218ae5d0a087f34fa385d7db181f`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 5.9 MB (5936327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ac959328037122478f2c09228cf4478f1c099d3257efec2dae9823db1d16b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db6c23ab4cfc36c7b70e7f4325b9bfa25d1a31a205c632f8e25757cb01f7cef`

```dockerfile
```

-	Layers:
	-	`sha256:3b09e8c286f81074ecdbaaeccccef453ddf9951ff459e4c086e01b8968fe3b0e`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57974d8beacb812f7bb8f7b52301ddd6a66eb7f4c851dcc2ee58f100ec0208b1`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:a32c16d5607a49617e8d077ec1f9ba5b53b0001a5d70805f183e27ac8f377955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20225669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7946f5f999880045f35ea6c3b7115f7cc7ca872f2653f90c5b0a114ea701599b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:16:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:16:14 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:16:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:16:34 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:16:34 GMT
USER user
# Wed, 28 Jan 2026 02:16:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50882b3c493b99635b6de6cd7279fc00a7df160e84cd53399664993828611810`  
		Last Modified: Wed, 28 Jan 2026 02:16:41 GMT  
		Size: 10.4 MB (10393535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588c02c444f10953a0f0aac9fa979fe4a835bbefde822557708fbd3d21750de`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dcb0c68d5a17e86130988d6ddf97978ae4c3d866b099962426d869a1c1fc3`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 6.1 MB (6144150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b77b6da6595a9c4ebfe003d3192b1a97bd9a14f1fe19417ad4a8d7068acc0505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f268d469cb9fcc79cb87b83fdcbadb9fa6818bf4d9c56a441df0e015c2ec6`

```dockerfile
```

-	Layers:
	-	`sha256:1ddc13011deb856a736a8c90df7acab1227398d8a2ae9e4586daa141365096b4`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e26778e3f506818fa4ed452e58334a8e15701f1d896ec8ed2ff3288ca7ecef`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:b40803da860e141ec3ab2320cf224c304aa870a9a884cb362b69e74b6fd82b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21272396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a2c6a98e5b7978e9d4671908d2864a8d58c1b872e5ec279f9a7a67312f3e2b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:32:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:32:11 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:32:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:32:31 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:32:31 GMT
USER user
# Wed, 28 Jan 2026 02:32:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc81a5350f307da5c9651178208c0aa789db44da9179ac834ac469d70ce42cc`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 11.1 MB (11079608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505a6cbf58cbc8474040a9d448a79cab0812b78e3b1c6db13e87987f8e4d9a0`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3296179391416e1833f722cc60f06d3ee4df4255177c36a2f41a35a6ab2661b`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 6.4 MB (6362158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e2ead2561551ba2a279d799d266e484e986d5370478af7155036333e682a1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551e8fca5526f8aa868ce90e80d554f73ff2800bcf6fb3b0fb1b9013223228b5`

```dockerfile
```

-	Layers:
	-	`sha256:890481868cc7de496dcdc1f70cc0d6026227efccdd40466a57aa43304c3e345f`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9fac81ff985d048567933403c842b1d477306de718e7d5226612b3cb1eb068`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:a29b54bd9ab139f5c60185ee85db0a602092a6821866cad82df0fb45368c398c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19942208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9176875f86f8abf3bc20c65b42847d911af0be7e5863f4d6dcbd526719132c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:24:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 08:24:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 08:24:34 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 08:28:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 08:28:23 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 08:28:23 GMT
USER user
# Wed, 28 Jan 2026 08:28:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6c4248bc749950275ce15b2dff82393f4351ced2e20c7b5e2ffef3c0848ce`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 10.3 MB (10291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e176dad2b23e06165e59400a1ff2260014ec93b0fb3b8c7628a64e1adaf49f`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3131351fcf8ddb074fb73d582b50e94aa55e099ca06fc128b310489675e69c97`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 6.1 MB (6064037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:165ef1cc15b3aeae45d6479f80369f8078869b953af00ad6ddb3765a55356e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192140d2d48650b459b2a9acdce6a086c4bf08877b907f3c6bc37ce9799d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:a59cb060f285e8659782eab321b072ac7afdce9472b5395d10144bca9d127b79`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e90caa10ad17b6e48ce9a44b3d010cc7b20e200cbb6ec1067441e247ce555fc`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:e55dc3c7ee83af6ee968373464f0b874c0d9149e01ce32f4680a83b5791d2ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a042dac64e240c543befef410a12767f4051b627b63028b597010c108714083`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:19:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:19:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:20:14 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:20:14 GMT
USER user
# Wed, 28 Jan 2026 02:20:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e174cb7156ade2e31408909452271b26ae4f143ef276276f0f448b1bad2165`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 11.4 MB (11405107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2a6b19294dd14e5551b394d76102c59c84eae810434dca5ae909a1e58da672`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba483b2b5362b1905ca82789be9c963c7fde3135033f6aac9183937e5d9161`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 6.2 MB (6202965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:05475f6695b9e4e1863216bdc5de6a1a24bfec2a5baecd06f9a7bc6cd0d17408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183ed0bc53cc736e214c57eaef2cb864de7e9dbaccf5fe0a5530c72247ac1ab`

```dockerfile
```

-	Layers:
	-	`sha256:c63a0479be024622dc272c05215babf54e4fc3b5c5ab3d053c0dcf2de80483cb`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5037cc7aa93ea1e1f234114cc48a82216f93fe0b9ee46a01ee9a03609cbe19e`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.23`

```console
$ docker pull irssi@sha256:bc9744c4e1f3c9e4401ee35e73ff4f7c97683f5c784c5cce21910e488a4ee219
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

### `irssi:1.4.5-alpine3.23` - linux; amd64

```console
$ docker pull irssi@sha256:84665fb63540b0ca94547800ed0093cb97d41e1cbc0d2aa823a67e6af91fe8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20784026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6645503b9d588217c1fb06c9a2d7e278a4360e4aa22e92d8ff0af44ac2c6c10`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:47 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:47 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:47 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65c05b32f228b7007340211a175e100ca3ddb33a7e2c44b15d11799a9a84ad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 10.9 MB (10857996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c32a8914140e457d67603de3b04ccc66e688baed84d8d500f40dc885ef27a`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93abf1ed0403fdbc85fa021598a1202b3d9b55bd9d785457b554af6b86fc7d`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 6.1 MB (6063223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:7bd9c1f9350891fb6e79ac3dc4d7686c1c714bb2c12147cb089864d19ef3bc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e29e513927a47425fe64b68ba4eeb03593581de0692a732211bc7b11537936`

```dockerfile
```

-	Layers:
	-	`sha256:5d4ee629f31bfb597346562d7da53858808c502ca6820fb40a7c347520afebad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b9c1c09e72415a3ca7367aec0652ca69a856b8c6a57ef69ba919d208498b76`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:9a8babd75444eea65ebe3a06627eceb16f4d50aec2da2998fd3a611d75ed5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04e50bc1d87804658a7d29a7ebb00b20d1a22d6d21cd19f5eff93f84035eb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:23:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:23:57 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:24:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:24:17 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:24:17 GMT
USER user
# Wed, 28 Jan 2026 02:24:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5c4e6a80a684ff34083f2ded6ae6a1b0f08ded4c8c5b0967f8b209ee2cd80`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 10.1 MB (10075626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93db171eca68243a4f689b5400ef3c2ac2a1074f1eae1f9f0d049506c8756fe`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c8c890839d95ebaf447485d8492d089fc8fa23d1ca65c6349a41ac95bc961`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 5.9 MB (5893116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:424e17d1ca73b3f1d92e5d0c0b7272bbaeee943cc673a2249f0bf7ca99eeedde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7bd514eeda8663e46d4eeed484d7df02209f60112393607269af3e2c0430c`

```dockerfile
```

-	Layers:
	-	`sha256:8fbda3c9e4c0ad20ecba339d117fab2e86108fcfe33cbba7f8ddc3053d6bc89a`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:42ff91c7e5cb5046e91c18adce476ce64e5d772ab658a70c9df46e592b10ce82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18828366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ac84c98bbbaf189bedd8109f71397874c887df2e4eb32123f05470b88358b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:21 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:22:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:22:22 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:22:37 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:22:37 GMT
USER user
# Wed, 28 Jan 2026 02:22:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ae8f3941338d2191aad9429d0bd185ceeb7aeedb8fddf43adad6b57e3273e`  
		Last Modified: Wed, 28 Jan 2026 02:22:45 GMT  
		Size: 9.9 MB (9902405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770acb73451dc424aeb5afcad4a4882f5d765fcbcc8b659b8841bf77d8166afe`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda40971fe170d5e56e81f398ba01d1904a08b07386da11fe56b125109dd60b9`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 5.6 MB (5643252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:fcebcd556b705ae5c410e6b569b01096b561714c5c2fc1d7c8c746decaeef0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d96801a2a79a245717287e0380350d8e1b0c44936b6dcaf8429b0e2074bab`

```dockerfile
```

-	Layers:
	-	`sha256:e0caf0a4bbae914fea3e8ffab5d1f1752e3fc858d38e993806dd2b78f6919657`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda69d589c766de3e44adc56d464708c1c2090577cfe6fdd9a50f95229a2c4fa`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c53ef5cb4c4fb78d4ffdaad1b902adc24327fb49d4ad5c6d719dcf26f8e1ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20927195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538037fb15131e4b2540ac0e275393593929c95a1ca622c94e6c70d99874f28`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628108c2cc8068dbd74588362d3734d7b6b306883916eb33cb53af667c096440`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 10.8 MB (10792790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9361ffc4206f8e272dc8adc782da4ab39f3b1fe287c6dfb23c57814cf1e94439`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7efe759a9de929b3a25440ff73ac10595ac218ae5d0a087f34fa385d7db181f`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 5.9 MB (5936327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:ac959328037122478f2c09228cf4478f1c099d3257efec2dae9823db1d16b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db6c23ab4cfc36c7b70e7f4325b9bfa25d1a31a205c632f8e25757cb01f7cef`

```dockerfile
```

-	Layers:
	-	`sha256:3b09e8c286f81074ecdbaaeccccef453ddf9951ff459e4c086e01b8968fe3b0e`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57974d8beacb812f7bb8f7b52301ddd6a66eb7f4c851dcc2ee58f100ec0208b1`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:a32c16d5607a49617e8d077ec1f9ba5b53b0001a5d70805f183e27ac8f377955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20225669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7946f5f999880045f35ea6c3b7115f7cc7ca872f2653f90c5b0a114ea701599b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:16:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:16:14 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:16:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:16:34 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:16:34 GMT
USER user
# Wed, 28 Jan 2026 02:16:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50882b3c493b99635b6de6cd7279fc00a7df160e84cd53399664993828611810`  
		Last Modified: Wed, 28 Jan 2026 02:16:41 GMT  
		Size: 10.4 MB (10393535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588c02c444f10953a0f0aac9fa979fe4a835bbefde822557708fbd3d21750de`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dcb0c68d5a17e86130988d6ddf97978ae4c3d866b099962426d869a1c1fc3`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 6.1 MB (6144150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:b77b6da6595a9c4ebfe003d3192b1a97bd9a14f1fe19417ad4a8d7068acc0505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f268d469cb9fcc79cb87b83fdcbadb9fa6818bf4d9c56a441df0e015c2ec6`

```dockerfile
```

-	Layers:
	-	`sha256:1ddc13011deb856a736a8c90df7acab1227398d8a2ae9e4586daa141365096b4`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e26778e3f506818fa4ed452e58334a8e15701f1d896ec8ed2ff3288ca7ecef`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:b40803da860e141ec3ab2320cf224c304aa870a9a884cb362b69e74b6fd82b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21272396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a2c6a98e5b7978e9d4671908d2864a8d58c1b872e5ec279f9a7a67312f3e2b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:32:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:32:11 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:32:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:32:31 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:32:31 GMT
USER user
# Wed, 28 Jan 2026 02:32:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc81a5350f307da5c9651178208c0aa789db44da9179ac834ac469d70ce42cc`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 11.1 MB (11079608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505a6cbf58cbc8474040a9d448a79cab0812b78e3b1c6db13e87987f8e4d9a0`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3296179391416e1833f722cc60f06d3ee4df4255177c36a2f41a35a6ab2661b`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 6.4 MB (6362158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:e2ead2561551ba2a279d799d266e484e986d5370478af7155036333e682a1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551e8fca5526f8aa868ce90e80d554f73ff2800bcf6fb3b0fb1b9013223228b5`

```dockerfile
```

-	Layers:
	-	`sha256:890481868cc7de496dcdc1f70cc0d6026227efccdd40466a57aa43304c3e345f`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9fac81ff985d048567933403c842b1d477306de718e7d5226612b3cb1eb068`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:a29b54bd9ab139f5c60185ee85db0a602092a6821866cad82df0fb45368c398c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19942208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9176875f86f8abf3bc20c65b42847d911af0be7e5863f4d6dcbd526719132c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:24:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 08:24:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 08:24:34 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 08:28:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 08:28:23 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 08:28:23 GMT
USER user
# Wed, 28 Jan 2026 08:28:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6c4248bc749950275ce15b2dff82393f4351ced2e20c7b5e2ffef3c0848ce`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 10.3 MB (10291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e176dad2b23e06165e59400a1ff2260014ec93b0fb3b8c7628a64e1adaf49f`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3131351fcf8ddb074fb73d582b50e94aa55e099ca06fc128b310489675e69c97`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 6.1 MB (6064037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:165ef1cc15b3aeae45d6479f80369f8078869b953af00ad6ddb3765a55356e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192140d2d48650b459b2a9acdce6a086c4bf08877b907f3c6bc37ce9799d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:a59cb060f285e8659782eab321b072ac7afdce9472b5395d10144bca9d127b79`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e90caa10ad17b6e48ce9a44b3d010cc7b20e200cbb6ec1067441e247ce555fc`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:e55dc3c7ee83af6ee968373464f0b874c0d9149e01ce32f4680a83b5791d2ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a042dac64e240c543befef410a12767f4051b627b63028b597010c108714083`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:19:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:19:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:20:14 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:20:14 GMT
USER user
# Wed, 28 Jan 2026 02:20:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e174cb7156ade2e31408909452271b26ae4f143ef276276f0f448b1bad2165`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 11.4 MB (11405107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2a6b19294dd14e5551b394d76102c59c84eae810434dca5ae909a1e58da672`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba483b2b5362b1905ca82789be9c963c7fde3135033f6aac9183937e5d9161`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 6.2 MB (6202965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:05475f6695b9e4e1863216bdc5de6a1a24bfec2a5baecd06f9a7bc6cd0d17408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183ed0bc53cc736e214c57eaef2cb864de7e9dbaccf5fe0a5530c72247ac1ab`

```dockerfile
```

-	Layers:
	-	`sha256:c63a0479be024622dc272c05215babf54e4fc3b5c5ab3d053c0dcf2de80483cb`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5037cc7aa93ea1e1f234114cc48a82216f93fe0b9ee46a01ee9a03609cbe19e`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-trixie`

```console
$ docker pull irssi@sha256:609a2ed50953d52717592390ee3e98c01c9d73570d22d00bae780781a867411d
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
$ docker pull irssi@sha256:9fae60e7bc9fc24c9db14714ff3340dec77f5694a9c1b466a89d06b539eed73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53870996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208ed2331d877493655ffbf5715d5ee7e7b1f90234b46c4b6347d2f3fe5616b9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:21:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:21:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:21:59 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:21:59 GMT
USER user
# Tue, 03 Feb 2026 02:21:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30e33e354d1d7dda77aaf4af795ff38369ad98bc285f7ba38494d0eda9abb20`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 19.2 MB (19222126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca5a9fa5a0439cd4c3a67c55dd77ab262eaaf8fe3e4f572652f807ae50717fe`  
		Last Modified: Tue, 03 Feb 2026 02:22:08 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7eb220ebedbb0676c3eece8a52277bc0f8d265bb6dc86c6b4c0257d1248723`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 4.9 MB (4866910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:a799ddd3de8dca67e18842b9f3100c61f8e0f40248eec47e9c7d6f7cc5a671e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e411b3f5abbc6ddcbca19c4a0c1521f22b4c249b1349aa45a8611fef7d303416`

```dockerfile
```

-	Layers:
	-	`sha256:293943398617ea6ecaaefceca69694c212fd62ab6e2486655ba0c29e0ae2ba79`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0f10970bd82463907455a4e67a02508285f5300f0993369c217f187ad257c4`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:01a370482e82c1514a233b8e1154c4eeb7e1e29779ed1cfbe0ea72fea926beb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50948888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d3a4cb61f731180f34b3940bbac33a2e24aa2d6dd90ca8e9000be255fe00ee`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:36 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:17:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:17:36 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:18:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:18:24 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:18:24 GMT
USER user
# Tue, 03 Feb 2026 02:18:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bff507cc72771f546378d6ffea702ce1dfc5f7462c98cf416495c9ea7abf5d7`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 18.3 MB (18287991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b732dda1c983c4e5532a6724cc0691bb7f0d4966d926b8031665b9eb19bdf2f4`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe09db28a7bba924a281417665350a9244ac5212bd2c077490813e7355165af`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 4.7 MB (4709982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:02c91f1c49e783ce02db737a1e321704df556858a8ad779ea708f8e801327d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d96f2236d0bf313e468cac657716937a2916282fb27192e905a3ca5780053c9`

```dockerfile
```

-	Layers:
	-	`sha256:c8fb39701e198922668819c0230131b6ae48c12a1d5b030b29d0a2eb4f184198`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69d1c7aa44d9df7724589bd6968e57bcd952b965d7dd14e01f8a0dd52b3fe8c8`  
		Last Modified: Tue, 03 Feb 2026 02:18:34 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:9bd66f1060f9a00e3c4e0bef5e1eeea789fc5f4c5b409aefc8bbcf3135f7dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48685426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9e9708bc24170126dd456a2b01d0c0f067c248903162e7c96091af2380b044`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:20:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:19 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:20:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:20:19 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:20:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:20:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:20:59 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:20:59 GMT
USER user
# Tue, 03 Feb 2026 02:20:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64c57598d1759ed47b0ce33fe2ae3f2ca5dfc344280bee5c91a6e2c2cfc33b`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 17.9 MB (17909993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15370f82ce37fd15003721575f11cd865da7261620aea2b1159317aab5659913`  
		Last Modified: Tue, 03 Feb 2026 02:21:09 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420081012ce7d68e8a87df2713f5901aacfc0a3a49fe4f2ac8aa2e0825c8352`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 4.6 MB (4558319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6849872da14db17e8b671bdfc642713a76fa2d2017b4ee56049715165db3c076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc1f967ef5736068697a132ec3311efa1a7280ec42fdaa1ed74a8029aac60bf`

```dockerfile
```

-	Layers:
	-	`sha256:b50b6b2a3c6822bb550588172036e08689e2b19d58f855b5606aded3012602bf`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0382a272fccc29001becae9a6ec2fb967f63ffe7d998d793f67a4ff9b9bfd7e`  
		Last Modified: Tue, 03 Feb 2026 02:21:09 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0e6173a8c52441af65097628532330fc826392fa4253e42657ec878c175208c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53975585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb379b987ac880b692fe2dc3dfd931da9c788161033c4e06239554bb4224eb9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:00 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:21:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:21:00 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:21:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:21:38 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:21:38 GMT
USER user
# Tue, 03 Feb 2026 02:21:38 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0532516bbb7262501000c326f37a0930c04d5f5a6565e14b1190d60f0743ce25`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 19.1 MB (19050649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6975dc48bed2afc9f4f4bd9b1665965ae2863eb4ff8cda14ac16f304476d307d`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d6ba22ebad57591e22d79dd65abfa638d56640df56deb4bf8cceb64e95620b`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 4.8 MB (4781508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2dcaadbe83c3a2a93746c56b19d9f055a7f01810e40da8786b5e2a69a843d506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c18f2b03173ce70e0ebf01ac9749a910865184a273ace4b2b75d21222b7118`

```dockerfile
```

-	Layers:
	-	`sha256:7457b4c9d09e256e51f29dec29c3e51469b7ad175435b171f9c5d18d9599cc7b`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff3cd880792431a74dcfdc01b30e2c7bd58e08261221840c6a483be5f9b07ee`  
		Last Modified: Tue, 03 Feb 2026 02:21:47 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; 386

```console
$ docker pull irssi@sha256:d10f5d01b9d383d32f36d497a37e76510561eeeaab8a38217dc142bd2044d611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54909414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccf4252e90be99c5c6384e8ef46f99bd42f9232af75a666a85cc7b80be93dbb`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:34 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:17:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:17:34 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:18:17 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:18:17 GMT
USER user
# Tue, 03 Feb 2026 02:18:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c57cfac3b918f6dafe14bf68c93d7d16a8a4970051d18d2a06c2a0263c9145`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 18.7 MB (18743761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c5a3109babbf5c2a1d4b41cb629cbbf8d5c31b10a16a624d77a5dc4bcc39f`  
		Last Modified: Tue, 03 Feb 2026 02:18:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcbe0576fcf1e6208897d40292c8c455af77f42a3cc963ffaff8613d1ca39c1`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 4.9 MB (4868437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:426742b8e02f677fc2e475fb401cbef173d80d0e52b05e495a053dbe62b14c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47fcdb26283af7bd047252c4c37d59277a0cd6d06d787227002528e3c365a58`

```dockerfile
```

-	Layers:
	-	`sha256:a288faa1621c022dd6bd996b78e6eb5d6ee3897b462366f28ee4c3f8bfd9caca`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8db18756472041642ed74f8e1e2ae8db1340756b5fde16825cc70e1a163b56`  
		Last Modified: Tue, 03 Feb 2026 02:18:26 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:55ac6c8d4f6d789fcd2f9caaeb13ce48d776a469d82747e7c1485b5963b19dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58244327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a843d5494442193be8285e2518e0cc0dc17b289884fe2369582b93b61eab8`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:24:37 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:24:37 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:24:37 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:24:37 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:26:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:26:23 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:26:23 GMT
USER user
# Tue, 03 Feb 2026 02:26:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624f9309218047b5688e03740c3f3ec04d0a5b2e096ba1ddb57f22215b1c032e`  
		Last Modified: Tue, 03 Feb 2026 02:26:45 GMT  
		Size: 19.5 MB (19542944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b058eb5982a30c68c6eeb3fddcc4f27b629549cbc9517db75d48bcb1f65cdf`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3765444fdfedf57570813f65ad00dcb9587c7a838f36605feb402e11e81f9b`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 5.1 MB (5097836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:5052a03b5d5ed94c58e1b40d85bcc9e57efe762b73218ad11c008c90311225db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee428904aef2658d2ef8892ffdd5bd384860d0da7ee3179246ea48246a6a9b50`

```dockerfile
```

-	Layers:
	-	`sha256:2fa98124d99ee2944a940c9389ee640f1cd7264bd06b18eac34eea4ceaf8efd6`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3e4620f46fdeae2fb275ccc948845b0e4a8862b657cff3de65766f5fd7fa1e`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:42f25149c195922ace2d09f52039c56d767996a84e387c8b4eb7cbce5f7c67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51685610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351bf47836b31594adc21aa27395e93d1a031e65d60247048b80b4a4dd12c1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV HOME=/home/user
# Wed, 14 Jan 2026 06:26:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 06:26:49 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 14 Jan 2026 06:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 14 Jan 2026 06:33:37 GMT
WORKDIR /home/user
# Wed, 14 Jan 2026 06:33:37 GMT
USER user
# Wed, 14 Jan 2026 06:33:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f9ee6f39e761595d5c9e020ae1fb10f95fe2a2951aa757f6de57a94a5d25ab`  
		Last Modified: Wed, 14 Jan 2026 06:35:34 GMT  
		Size: 18.5 MB (18549843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef5f232538194de0e7b47d1c08ae77477427a3951186780b1f80e4a91600b4`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b07d932aff1dc5ee2440e07ea368a0ddb73f2c32cb1a8ab0bfd881b02a53f7`  
		Last Modified: Wed, 14 Jan 2026 06:35:31 GMT  
		Size: 4.9 MB (4860721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:0d0a172cbd5471aa3ec8392dc55c5bad0e4fe5bb8e39202b61a8ad6e7252ed2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f4f48da90e6ab7c83ee1b3d3d3112e940971d8bcbed03f47ee03a7d5cca5a6`

```dockerfile
```

-	Layers:
	-	`sha256:afd4f3e89883cc18160c077e4faf0da05c4455d6e0cf0af04a7f525621cba93f`  
		Last Modified: Wed, 14 Jan 2026 06:35:31 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7e2d6743dc6628d707a2e9780dc009b06754202d718210a4e2690ed143c0b`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:3507e27e096139e6c53256b46253b87c2add6684f0a537a81456df935df58f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54507448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9bb61ec181683066bef513d8c48742e3a8098735e181c1c3fff70935a09bd6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:19:25 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:20:02 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:20:02 GMT
USER user
# Tue, 03 Feb 2026 02:20:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8905651585d3b136c5d623c620a4b7471b9176370e9badfa69aa86ab3b0b2771`  
		Last Modified: Tue, 03 Feb 2026 02:20:19 GMT  
		Size: 19.8 MB (19760098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b071b126b87f268a0a29ba9f9fe74d76c9af662cee154d5c7726aae6103dc5c2`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2057418f122012d53f3e9dc13ad0f4d67e6c354b177c2e3cff726f0259e435ff`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 4.9 MB (4905841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:3fb068ad5665041ed11698505383bd5effcaa6e7a9de68a793f560dcdbd63930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7848dc8f3f1945a579bb92f67c19f8ef6b9817196a982d578c50208a9d0cb6f`

```dockerfile
```

-	Layers:
	-	`sha256:90c9b6efea1e9a1c048095f2ecb0af339f8475c5029d9074730a486e02732943`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67606c2343b9ace2f5fd62625eb54620eac701413090a31982ee610dcd1e006f`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:bc9744c4e1f3c9e4401ee35e73ff4f7c97683f5c784c5cce21910e488a4ee219
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
$ docker pull irssi@sha256:84665fb63540b0ca94547800ed0093cb97d41e1cbc0d2aa823a67e6af91fe8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20784026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6645503b9d588217c1fb06c9a2d7e278a4360e4aa22e92d8ff0af44ac2c6c10`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:47 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:47 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:47 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65c05b32f228b7007340211a175e100ca3ddb33a7e2c44b15d11799a9a84ad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 10.9 MB (10857996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c32a8914140e457d67603de3b04ccc66e688baed84d8d500f40dc885ef27a`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93abf1ed0403fdbc85fa021598a1202b3d9b55bd9d785457b554af6b86fc7d`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 6.1 MB (6063223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:7bd9c1f9350891fb6e79ac3dc4d7686c1c714bb2c12147cb089864d19ef3bc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e29e513927a47425fe64b68ba4eeb03593581de0692a732211bc7b11537936`

```dockerfile
```

-	Layers:
	-	`sha256:5d4ee629f31bfb597346562d7da53858808c502ca6820fb40a7c347520afebad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b9c1c09e72415a3ca7367aec0652ca69a856b8c6a57ef69ba919d208498b76`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:9a8babd75444eea65ebe3a06627eceb16f4d50aec2da2998fd3a611d75ed5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04e50bc1d87804658a7d29a7ebb00b20d1a22d6d21cd19f5eff93f84035eb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:23:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:23:57 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:24:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:24:17 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:24:17 GMT
USER user
# Wed, 28 Jan 2026 02:24:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5c4e6a80a684ff34083f2ded6ae6a1b0f08ded4c8c5b0967f8b209ee2cd80`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 10.1 MB (10075626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93db171eca68243a4f689b5400ef3c2ac2a1074f1eae1f9f0d049506c8756fe`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c8c890839d95ebaf447485d8492d089fc8fa23d1ca65c6349a41ac95bc961`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 5.9 MB (5893116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:424e17d1ca73b3f1d92e5d0c0b7272bbaeee943cc673a2249f0bf7ca99eeedde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7bd514eeda8663e46d4eeed484d7df02209f60112393607269af3e2c0430c`

```dockerfile
```

-	Layers:
	-	`sha256:8fbda3c9e4c0ad20ecba339d117fab2e86108fcfe33cbba7f8ddc3053d6bc89a`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:42ff91c7e5cb5046e91c18adce476ce64e5d772ab658a70c9df46e592b10ce82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18828366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ac84c98bbbaf189bedd8109f71397874c887df2e4eb32123f05470b88358b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:21 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:22:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:22:22 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:22:37 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:22:37 GMT
USER user
# Wed, 28 Jan 2026 02:22:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ae8f3941338d2191aad9429d0bd185ceeb7aeedb8fddf43adad6b57e3273e`  
		Last Modified: Wed, 28 Jan 2026 02:22:45 GMT  
		Size: 9.9 MB (9902405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770acb73451dc424aeb5afcad4a4882f5d765fcbcc8b659b8841bf77d8166afe`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda40971fe170d5e56e81f398ba01d1904a08b07386da11fe56b125109dd60b9`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 5.6 MB (5643252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:fcebcd556b705ae5c410e6b569b01096b561714c5c2fc1d7c8c746decaeef0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d96801a2a79a245717287e0380350d8e1b0c44936b6dcaf8429b0e2074bab`

```dockerfile
```

-	Layers:
	-	`sha256:e0caf0a4bbae914fea3e8ffab5d1f1752e3fc858d38e993806dd2b78f6919657`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda69d589c766de3e44adc56d464708c1c2090577cfe6fdd9a50f95229a2c4fa`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c53ef5cb4c4fb78d4ffdaad1b902adc24327fb49d4ad5c6d719dcf26f8e1ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20927195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538037fb15131e4b2540ac0e275393593929c95a1ca622c94e6c70d99874f28`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628108c2cc8068dbd74588362d3734d7b6b306883916eb33cb53af667c096440`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 10.8 MB (10792790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9361ffc4206f8e272dc8adc782da4ab39f3b1fe287c6dfb23c57814cf1e94439`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7efe759a9de929b3a25440ff73ac10595ac218ae5d0a087f34fa385d7db181f`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 5.9 MB (5936327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ac959328037122478f2c09228cf4478f1c099d3257efec2dae9823db1d16b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db6c23ab4cfc36c7b70e7f4325b9bfa25d1a31a205c632f8e25757cb01f7cef`

```dockerfile
```

-	Layers:
	-	`sha256:3b09e8c286f81074ecdbaaeccccef453ddf9951ff459e4c086e01b8968fe3b0e`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57974d8beacb812f7bb8f7b52301ddd6a66eb7f4c851dcc2ee58f100ec0208b1`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:a32c16d5607a49617e8d077ec1f9ba5b53b0001a5d70805f183e27ac8f377955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20225669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7946f5f999880045f35ea6c3b7115f7cc7ca872f2653f90c5b0a114ea701599b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:16:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:16:14 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:16:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:16:34 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:16:34 GMT
USER user
# Wed, 28 Jan 2026 02:16:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50882b3c493b99635b6de6cd7279fc00a7df160e84cd53399664993828611810`  
		Last Modified: Wed, 28 Jan 2026 02:16:41 GMT  
		Size: 10.4 MB (10393535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588c02c444f10953a0f0aac9fa979fe4a835bbefde822557708fbd3d21750de`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dcb0c68d5a17e86130988d6ddf97978ae4c3d866b099962426d869a1c1fc3`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 6.1 MB (6144150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b77b6da6595a9c4ebfe003d3192b1a97bd9a14f1fe19417ad4a8d7068acc0505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f268d469cb9fcc79cb87b83fdcbadb9fa6818bf4d9c56a441df0e015c2ec6`

```dockerfile
```

-	Layers:
	-	`sha256:1ddc13011deb856a736a8c90df7acab1227398d8a2ae9e4586daa141365096b4`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e26778e3f506818fa4ed452e58334a8e15701f1d896ec8ed2ff3288ca7ecef`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:b40803da860e141ec3ab2320cf224c304aa870a9a884cb362b69e74b6fd82b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21272396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a2c6a98e5b7978e9d4671908d2864a8d58c1b872e5ec279f9a7a67312f3e2b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:32:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:32:11 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:32:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:32:31 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:32:31 GMT
USER user
# Wed, 28 Jan 2026 02:32:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc81a5350f307da5c9651178208c0aa789db44da9179ac834ac469d70ce42cc`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 11.1 MB (11079608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505a6cbf58cbc8474040a9d448a79cab0812b78e3b1c6db13e87987f8e4d9a0`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3296179391416e1833f722cc60f06d3ee4df4255177c36a2f41a35a6ab2661b`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 6.4 MB (6362158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e2ead2561551ba2a279d799d266e484e986d5370478af7155036333e682a1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551e8fca5526f8aa868ce90e80d554f73ff2800bcf6fb3b0fb1b9013223228b5`

```dockerfile
```

-	Layers:
	-	`sha256:890481868cc7de496dcdc1f70cc0d6026227efccdd40466a57aa43304c3e345f`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9fac81ff985d048567933403c842b1d477306de718e7d5226612b3cb1eb068`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:a29b54bd9ab139f5c60185ee85db0a602092a6821866cad82df0fb45368c398c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19942208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9176875f86f8abf3bc20c65b42847d911af0be7e5863f4d6dcbd526719132c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:24:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 08:24:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 08:24:34 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 08:28:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 08:28:23 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 08:28:23 GMT
USER user
# Wed, 28 Jan 2026 08:28:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6c4248bc749950275ce15b2dff82393f4351ced2e20c7b5e2ffef3c0848ce`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 10.3 MB (10291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e176dad2b23e06165e59400a1ff2260014ec93b0fb3b8c7628a64e1adaf49f`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3131351fcf8ddb074fb73d582b50e94aa55e099ca06fc128b310489675e69c97`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 6.1 MB (6064037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:165ef1cc15b3aeae45d6479f80369f8078869b953af00ad6ddb3765a55356e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192140d2d48650b459b2a9acdce6a086c4bf08877b907f3c6bc37ce9799d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:a59cb060f285e8659782eab321b072ac7afdce9472b5395d10144bca9d127b79`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e90caa10ad17b6e48ce9a44b3d010cc7b20e200cbb6ec1067441e247ce555fc`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:e55dc3c7ee83af6ee968373464f0b874c0d9149e01ce32f4680a83b5791d2ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a042dac64e240c543befef410a12767f4051b627b63028b597010c108714083`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:19:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:19:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:20:14 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:20:14 GMT
USER user
# Wed, 28 Jan 2026 02:20:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e174cb7156ade2e31408909452271b26ae4f143ef276276f0f448b1bad2165`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 11.4 MB (11405107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2a6b19294dd14e5551b394d76102c59c84eae810434dca5ae909a1e58da672`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba483b2b5362b1905ca82789be9c963c7fde3135033f6aac9183937e5d9161`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 6.2 MB (6202965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:05475f6695b9e4e1863216bdc5de6a1a24bfec2a5baecd06f9a7bc6cd0d17408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183ed0bc53cc736e214c57eaef2cb864de7e9dbaccf5fe0a5530c72247ac1ab`

```dockerfile
```

-	Layers:
	-	`sha256:c63a0479be024622dc272c05215babf54e4fc3b5c5ab3d053c0dcf2de80483cb`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5037cc7aa93ea1e1f234114cc48a82216f93fe0b9ee46a01ee9a03609cbe19e`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.23`

```console
$ docker pull irssi@sha256:bc9744c4e1f3c9e4401ee35e73ff4f7c97683f5c784c5cce21910e488a4ee219
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

### `irssi:alpine3.23` - linux; amd64

```console
$ docker pull irssi@sha256:84665fb63540b0ca94547800ed0093cb97d41e1cbc0d2aa823a67e6af91fe8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20784026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6645503b9d588217c1fb06c9a2d7e278a4360e4aa22e92d8ff0af44ac2c6c10`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:47 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:47 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:47 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65c05b32f228b7007340211a175e100ca3ddb33a7e2c44b15d11799a9a84ad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 10.9 MB (10857996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c32a8914140e457d67603de3b04ccc66e688baed84d8d500f40dc885ef27a`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93abf1ed0403fdbc85fa021598a1202b3d9b55bd9d785457b554af6b86fc7d`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 6.1 MB (6063223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:7bd9c1f9350891fb6e79ac3dc4d7686c1c714bb2c12147cb089864d19ef3bc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e29e513927a47425fe64b68ba4eeb03593581de0692a732211bc7b11537936`

```dockerfile
```

-	Layers:
	-	`sha256:5d4ee629f31bfb597346562d7da53858808c502ca6820fb40a7c347520afebad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b9c1c09e72415a3ca7367aec0652ca69a856b8c6a57ef69ba919d208498b76`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:9a8babd75444eea65ebe3a06627eceb16f4d50aec2da2998fd3a611d75ed5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04e50bc1d87804658a7d29a7ebb00b20d1a22d6d21cd19f5eff93f84035eb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:23:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:23:57 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:24:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:24:17 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:24:17 GMT
USER user
# Wed, 28 Jan 2026 02:24:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5c4e6a80a684ff34083f2ded6ae6a1b0f08ded4c8c5b0967f8b209ee2cd80`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 10.1 MB (10075626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93db171eca68243a4f689b5400ef3c2ac2a1074f1eae1f9f0d049506c8756fe`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c8c890839d95ebaf447485d8492d089fc8fa23d1ca65c6349a41ac95bc961`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 5.9 MB (5893116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:424e17d1ca73b3f1d92e5d0c0b7272bbaeee943cc673a2249f0bf7ca99eeedde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7bd514eeda8663e46d4eeed484d7df02209f60112393607269af3e2c0430c`

```dockerfile
```

-	Layers:
	-	`sha256:8fbda3c9e4c0ad20ecba339d117fab2e86108fcfe33cbba7f8ddc3053d6bc89a`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:42ff91c7e5cb5046e91c18adce476ce64e5d772ab658a70c9df46e592b10ce82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18828366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ac84c98bbbaf189bedd8109f71397874c887df2e4eb32123f05470b88358b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:21 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:22:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:22:22 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:22:37 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:22:37 GMT
USER user
# Wed, 28 Jan 2026 02:22:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ae8f3941338d2191aad9429d0bd185ceeb7aeedb8fddf43adad6b57e3273e`  
		Last Modified: Wed, 28 Jan 2026 02:22:45 GMT  
		Size: 9.9 MB (9902405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770acb73451dc424aeb5afcad4a4882f5d765fcbcc8b659b8841bf77d8166afe`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda40971fe170d5e56e81f398ba01d1904a08b07386da11fe56b125109dd60b9`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 5.6 MB (5643252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:fcebcd556b705ae5c410e6b569b01096b561714c5c2fc1d7c8c746decaeef0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d96801a2a79a245717287e0380350d8e1b0c44936b6dcaf8429b0e2074bab`

```dockerfile
```

-	Layers:
	-	`sha256:e0caf0a4bbae914fea3e8ffab5d1f1752e3fc858d38e993806dd2b78f6919657`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda69d589c766de3e44adc56d464708c1c2090577cfe6fdd9a50f95229a2c4fa`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c53ef5cb4c4fb78d4ffdaad1b902adc24327fb49d4ad5c6d719dcf26f8e1ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20927195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538037fb15131e4b2540ac0e275393593929c95a1ca622c94e6c70d99874f28`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628108c2cc8068dbd74588362d3734d7b6b306883916eb33cb53af667c096440`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 10.8 MB (10792790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9361ffc4206f8e272dc8adc782da4ab39f3b1fe287c6dfb23c57814cf1e94439`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7efe759a9de929b3a25440ff73ac10595ac218ae5d0a087f34fa385d7db181f`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 5.9 MB (5936327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:ac959328037122478f2c09228cf4478f1c099d3257efec2dae9823db1d16b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db6c23ab4cfc36c7b70e7f4325b9bfa25d1a31a205c632f8e25757cb01f7cef`

```dockerfile
```

-	Layers:
	-	`sha256:3b09e8c286f81074ecdbaaeccccef453ddf9951ff459e4c086e01b8968fe3b0e`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57974d8beacb812f7bb8f7b52301ddd6a66eb7f4c851dcc2ee58f100ec0208b1`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:a32c16d5607a49617e8d077ec1f9ba5b53b0001a5d70805f183e27ac8f377955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20225669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7946f5f999880045f35ea6c3b7115f7cc7ca872f2653f90c5b0a114ea701599b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:16:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:16:14 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:16:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:16:34 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:16:34 GMT
USER user
# Wed, 28 Jan 2026 02:16:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50882b3c493b99635b6de6cd7279fc00a7df160e84cd53399664993828611810`  
		Last Modified: Wed, 28 Jan 2026 02:16:41 GMT  
		Size: 10.4 MB (10393535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588c02c444f10953a0f0aac9fa979fe4a835bbefde822557708fbd3d21750de`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dcb0c68d5a17e86130988d6ddf97978ae4c3d866b099962426d869a1c1fc3`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 6.1 MB (6144150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:b77b6da6595a9c4ebfe003d3192b1a97bd9a14f1fe19417ad4a8d7068acc0505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f268d469cb9fcc79cb87b83fdcbadb9fa6818bf4d9c56a441df0e015c2ec6`

```dockerfile
```

-	Layers:
	-	`sha256:1ddc13011deb856a736a8c90df7acab1227398d8a2ae9e4586daa141365096b4`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e26778e3f506818fa4ed452e58334a8e15701f1d896ec8ed2ff3288ca7ecef`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:b40803da860e141ec3ab2320cf224c304aa870a9a884cb362b69e74b6fd82b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21272396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a2c6a98e5b7978e9d4671908d2864a8d58c1b872e5ec279f9a7a67312f3e2b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:32:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:32:11 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:32:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:32:31 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:32:31 GMT
USER user
# Wed, 28 Jan 2026 02:32:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc81a5350f307da5c9651178208c0aa789db44da9179ac834ac469d70ce42cc`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 11.1 MB (11079608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505a6cbf58cbc8474040a9d448a79cab0812b78e3b1c6db13e87987f8e4d9a0`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3296179391416e1833f722cc60f06d3ee4df4255177c36a2f41a35a6ab2661b`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 6.4 MB (6362158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:e2ead2561551ba2a279d799d266e484e986d5370478af7155036333e682a1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551e8fca5526f8aa868ce90e80d554f73ff2800bcf6fb3b0fb1b9013223228b5`

```dockerfile
```

-	Layers:
	-	`sha256:890481868cc7de496dcdc1f70cc0d6026227efccdd40466a57aa43304c3e345f`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9fac81ff985d048567933403c842b1d477306de718e7d5226612b3cb1eb068`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:a29b54bd9ab139f5c60185ee85db0a602092a6821866cad82df0fb45368c398c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19942208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9176875f86f8abf3bc20c65b42847d911af0be7e5863f4d6dcbd526719132c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:24:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 08:24:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 08:24:34 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 08:28:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 08:28:23 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 08:28:23 GMT
USER user
# Wed, 28 Jan 2026 08:28:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6c4248bc749950275ce15b2dff82393f4351ced2e20c7b5e2ffef3c0848ce`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 10.3 MB (10291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e176dad2b23e06165e59400a1ff2260014ec93b0fb3b8c7628a64e1adaf49f`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3131351fcf8ddb074fb73d582b50e94aa55e099ca06fc128b310489675e69c97`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 6.1 MB (6064037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:165ef1cc15b3aeae45d6479f80369f8078869b953af00ad6ddb3765a55356e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192140d2d48650b459b2a9acdce6a086c4bf08877b907f3c6bc37ce9799d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:a59cb060f285e8659782eab321b072ac7afdce9472b5395d10144bca9d127b79`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e90caa10ad17b6e48ce9a44b3d010cc7b20e200cbb6ec1067441e247ce555fc`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:e55dc3c7ee83af6ee968373464f0b874c0d9149e01ce32f4680a83b5791d2ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a042dac64e240c543befef410a12767f4051b627b63028b597010c108714083`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:19:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:19:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:20:14 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:20:14 GMT
USER user
# Wed, 28 Jan 2026 02:20:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e174cb7156ade2e31408909452271b26ae4f143ef276276f0f448b1bad2165`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 11.4 MB (11405107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2a6b19294dd14e5551b394d76102c59c84eae810434dca5ae909a1e58da672`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba483b2b5362b1905ca82789be9c963c7fde3135033f6aac9183937e5d9161`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 6.2 MB (6202965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:05475f6695b9e4e1863216bdc5de6a1a24bfec2a5baecd06f9a7bc6cd0d17408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183ed0bc53cc736e214c57eaef2cb864de7e9dbaccf5fe0a5530c72247ac1ab`

```dockerfile
```

-	Layers:
	-	`sha256:c63a0479be024622dc272c05215babf54e4fc3b5c5ab3d053c0dcf2de80483cb`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5037cc7aa93ea1e1f234114cc48a82216f93fe0b9ee46a01ee9a03609cbe19e`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:609a2ed50953d52717592390ee3e98c01c9d73570d22d00bae780781a867411d
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
$ docker pull irssi@sha256:9fae60e7bc9fc24c9db14714ff3340dec77f5694a9c1b466a89d06b539eed73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53870996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208ed2331d877493655ffbf5715d5ee7e7b1f90234b46c4b6347d2f3fe5616b9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:21:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:21:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:21:59 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:21:59 GMT
USER user
# Tue, 03 Feb 2026 02:21:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30e33e354d1d7dda77aaf4af795ff38369ad98bc285f7ba38494d0eda9abb20`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 19.2 MB (19222126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca5a9fa5a0439cd4c3a67c55dd77ab262eaaf8fe3e4f572652f807ae50717fe`  
		Last Modified: Tue, 03 Feb 2026 02:22:08 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7eb220ebedbb0676c3eece8a52277bc0f8d265bb6dc86c6b4c0257d1248723`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 4.9 MB (4866910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:a799ddd3de8dca67e18842b9f3100c61f8e0f40248eec47e9c7d6f7cc5a671e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e411b3f5abbc6ddcbca19c4a0c1521f22b4c249b1349aa45a8611fef7d303416`

```dockerfile
```

-	Layers:
	-	`sha256:293943398617ea6ecaaefceca69694c212fd62ab6e2486655ba0c29e0ae2ba79`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0f10970bd82463907455a4e67a02508285f5300f0993369c217f187ad257c4`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:01a370482e82c1514a233b8e1154c4eeb7e1e29779ed1cfbe0ea72fea926beb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50948888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d3a4cb61f731180f34b3940bbac33a2e24aa2d6dd90ca8e9000be255fe00ee`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:36 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:17:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:17:36 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:18:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:18:24 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:18:24 GMT
USER user
# Tue, 03 Feb 2026 02:18:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bff507cc72771f546378d6ffea702ce1dfc5f7462c98cf416495c9ea7abf5d7`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 18.3 MB (18287991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b732dda1c983c4e5532a6724cc0691bb7f0d4966d926b8031665b9eb19bdf2f4`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe09db28a7bba924a281417665350a9244ac5212bd2c077490813e7355165af`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 4.7 MB (4709982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:02c91f1c49e783ce02db737a1e321704df556858a8ad779ea708f8e801327d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d96f2236d0bf313e468cac657716937a2916282fb27192e905a3ca5780053c9`

```dockerfile
```

-	Layers:
	-	`sha256:c8fb39701e198922668819c0230131b6ae48c12a1d5b030b29d0a2eb4f184198`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69d1c7aa44d9df7724589bd6968e57bcd952b965d7dd14e01f8a0dd52b3fe8c8`  
		Last Modified: Tue, 03 Feb 2026 02:18:34 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:9bd66f1060f9a00e3c4e0bef5e1eeea789fc5f4c5b409aefc8bbcf3135f7dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48685426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9e9708bc24170126dd456a2b01d0c0f067c248903162e7c96091af2380b044`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:20:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:19 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:20:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:20:19 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:20:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:20:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:20:59 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:20:59 GMT
USER user
# Tue, 03 Feb 2026 02:20:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64c57598d1759ed47b0ce33fe2ae3f2ca5dfc344280bee5c91a6e2c2cfc33b`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 17.9 MB (17909993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15370f82ce37fd15003721575f11cd865da7261620aea2b1159317aab5659913`  
		Last Modified: Tue, 03 Feb 2026 02:21:09 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420081012ce7d68e8a87df2713f5901aacfc0a3a49fe4f2ac8aa2e0825c8352`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 4.6 MB (4558319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:6849872da14db17e8b671bdfc642713a76fa2d2017b4ee56049715165db3c076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc1f967ef5736068697a132ec3311efa1a7280ec42fdaa1ed74a8029aac60bf`

```dockerfile
```

-	Layers:
	-	`sha256:b50b6b2a3c6822bb550588172036e08689e2b19d58f855b5606aded3012602bf`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0382a272fccc29001becae9a6ec2fb967f63ffe7d998d793f67a4ff9b9bfd7e`  
		Last Modified: Tue, 03 Feb 2026 02:21:09 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0e6173a8c52441af65097628532330fc826392fa4253e42657ec878c175208c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53975585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb379b987ac880b692fe2dc3dfd931da9c788161033c4e06239554bb4224eb9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:00 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:21:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:21:00 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:21:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:21:38 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:21:38 GMT
USER user
# Tue, 03 Feb 2026 02:21:38 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0532516bbb7262501000c326f37a0930c04d5f5a6565e14b1190d60f0743ce25`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 19.1 MB (19050649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6975dc48bed2afc9f4f4bd9b1665965ae2863eb4ff8cda14ac16f304476d307d`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d6ba22ebad57591e22d79dd65abfa638d56640df56deb4bf8cceb64e95620b`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 4.8 MB (4781508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:2dcaadbe83c3a2a93746c56b19d9f055a7f01810e40da8786b5e2a69a843d506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c18f2b03173ce70e0ebf01ac9749a910865184a273ace4b2b75d21222b7118`

```dockerfile
```

-	Layers:
	-	`sha256:7457b4c9d09e256e51f29dec29c3e51469b7ad175435b171f9c5d18d9599cc7b`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff3cd880792431a74dcfdc01b30e2c7bd58e08261221840c6a483be5f9b07ee`  
		Last Modified: Tue, 03 Feb 2026 02:21:47 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:d10f5d01b9d383d32f36d497a37e76510561eeeaab8a38217dc142bd2044d611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54909414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccf4252e90be99c5c6384e8ef46f99bd42f9232af75a666a85cc7b80be93dbb`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:34 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:17:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:17:34 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:18:17 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:18:17 GMT
USER user
# Tue, 03 Feb 2026 02:18:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c57cfac3b918f6dafe14bf68c93d7d16a8a4970051d18d2a06c2a0263c9145`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 18.7 MB (18743761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c5a3109babbf5c2a1d4b41cb629cbbf8d5c31b10a16a624d77a5dc4bcc39f`  
		Last Modified: Tue, 03 Feb 2026 02:18:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcbe0576fcf1e6208897d40292c8c455af77f42a3cc963ffaff8613d1ca39c1`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 4.9 MB (4868437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:426742b8e02f677fc2e475fb401cbef173d80d0e52b05e495a053dbe62b14c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47fcdb26283af7bd047252c4c37d59277a0cd6d06d787227002528e3c365a58`

```dockerfile
```

-	Layers:
	-	`sha256:a288faa1621c022dd6bd996b78e6eb5d6ee3897b462366f28ee4c3f8bfd9caca`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8db18756472041642ed74f8e1e2ae8db1340756b5fde16825cc70e1a163b56`  
		Last Modified: Tue, 03 Feb 2026 02:18:26 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:55ac6c8d4f6d789fcd2f9caaeb13ce48d776a469d82747e7c1485b5963b19dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58244327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a843d5494442193be8285e2518e0cc0dc17b289884fe2369582b93b61eab8`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:24:37 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:24:37 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:24:37 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:24:37 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:26:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:26:23 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:26:23 GMT
USER user
# Tue, 03 Feb 2026 02:26:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624f9309218047b5688e03740c3f3ec04d0a5b2e096ba1ddb57f22215b1c032e`  
		Last Modified: Tue, 03 Feb 2026 02:26:45 GMT  
		Size: 19.5 MB (19542944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b058eb5982a30c68c6eeb3fddcc4f27b629549cbc9517db75d48bcb1f65cdf`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3765444fdfedf57570813f65ad00dcb9587c7a838f36605feb402e11e81f9b`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 5.1 MB (5097836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:5052a03b5d5ed94c58e1b40d85bcc9e57efe762b73218ad11c008c90311225db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee428904aef2658d2ef8892ffdd5bd384860d0da7ee3179246ea48246a6a9b50`

```dockerfile
```

-	Layers:
	-	`sha256:2fa98124d99ee2944a940c9389ee640f1cd7264bd06b18eac34eea4ceaf8efd6`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3e4620f46fdeae2fb275ccc948845b0e4a8862b657cff3de65766f5fd7fa1e`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; riscv64

```console
$ docker pull irssi@sha256:42f25149c195922ace2d09f52039c56d767996a84e387c8b4eb7cbce5f7c67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51685610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351bf47836b31594adc21aa27395e93d1a031e65d60247048b80b4a4dd12c1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV HOME=/home/user
# Wed, 14 Jan 2026 06:26:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 06:26:49 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 14 Jan 2026 06:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 14 Jan 2026 06:33:37 GMT
WORKDIR /home/user
# Wed, 14 Jan 2026 06:33:37 GMT
USER user
# Wed, 14 Jan 2026 06:33:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f9ee6f39e761595d5c9e020ae1fb10f95fe2a2951aa757f6de57a94a5d25ab`  
		Last Modified: Wed, 14 Jan 2026 06:35:34 GMT  
		Size: 18.5 MB (18549843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef5f232538194de0e7b47d1c08ae77477427a3951186780b1f80e4a91600b4`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b07d932aff1dc5ee2440e07ea368a0ddb73f2c32cb1a8ab0bfd881b02a53f7`  
		Last Modified: Wed, 14 Jan 2026 06:35:31 GMT  
		Size: 4.9 MB (4860721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:0d0a172cbd5471aa3ec8392dc55c5bad0e4fe5bb8e39202b61a8ad6e7252ed2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f4f48da90e6ab7c83ee1b3d3d3112e940971d8bcbed03f47ee03a7d5cca5a6`

```dockerfile
```

-	Layers:
	-	`sha256:afd4f3e89883cc18160c077e4faf0da05c4455d6e0cf0af04a7f525621cba93f`  
		Last Modified: Wed, 14 Jan 2026 06:35:31 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7e2d6743dc6628d707a2e9780dc009b06754202d718210a4e2690ed143c0b`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:3507e27e096139e6c53256b46253b87c2add6684f0a537a81456df935df58f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54507448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9bb61ec181683066bef513d8c48742e3a8098735e181c1c3fff70935a09bd6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:19:25 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:20:02 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:20:02 GMT
USER user
# Tue, 03 Feb 2026 02:20:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8905651585d3b136c5d623c620a4b7471b9176370e9badfa69aa86ab3b0b2771`  
		Last Modified: Tue, 03 Feb 2026 02:20:19 GMT  
		Size: 19.8 MB (19760098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b071b126b87f268a0a29ba9f9fe74d76c9af662cee154d5c7726aae6103dc5c2`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2057418f122012d53f3e9dc13ad0f4d67e6c354b177c2e3cff726f0259e435ff`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 4.9 MB (4905841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:3fb068ad5665041ed11698505383bd5effcaa6e7a9de68a793f560dcdbd63930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7848dc8f3f1945a579bb92f67c19f8ef6b9817196a982d578c50208a9d0cb6f`

```dockerfile
```

-	Layers:
	-	`sha256:90c9b6efea1e9a1c048095f2ecb0af339f8475c5029d9074730a486e02732943`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67606c2343b9ace2f5fd62625eb54620eac701413090a31982ee610dcd1e006f`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:trixie`

```console
$ docker pull irssi@sha256:609a2ed50953d52717592390ee3e98c01c9d73570d22d00bae780781a867411d
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
$ docker pull irssi@sha256:9fae60e7bc9fc24c9db14714ff3340dec77f5694a9c1b466a89d06b539eed73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53870996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208ed2331d877493655ffbf5715d5ee7e7b1f90234b46c4b6347d2f3fe5616b9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:21:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:21:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:21:59 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:21:59 GMT
USER user
# Tue, 03 Feb 2026 02:21:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30e33e354d1d7dda77aaf4af795ff38369ad98bc285f7ba38494d0eda9abb20`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 19.2 MB (19222126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca5a9fa5a0439cd4c3a67c55dd77ab262eaaf8fe3e4f572652f807ae50717fe`  
		Last Modified: Tue, 03 Feb 2026 02:22:08 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7eb220ebedbb0676c3eece8a52277bc0f8d265bb6dc86c6b4c0257d1248723`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 4.9 MB (4866910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:a799ddd3de8dca67e18842b9f3100c61f8e0f40248eec47e9c7d6f7cc5a671e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e411b3f5abbc6ddcbca19c4a0c1521f22b4c249b1349aa45a8611fef7d303416`

```dockerfile
```

-	Layers:
	-	`sha256:293943398617ea6ecaaefceca69694c212fd62ab6e2486655ba0c29e0ae2ba79`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0f10970bd82463907455a4e67a02508285f5300f0993369c217f187ad257c4`  
		Last Modified: Tue, 03 Feb 2026 02:22:09 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:01a370482e82c1514a233b8e1154c4eeb7e1e29779ed1cfbe0ea72fea926beb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50948888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d3a4cb61f731180f34b3940bbac33a2e24aa2d6dd90ca8e9000be255fe00ee`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:36 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:17:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:17:36 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:18:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:18:24 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:18:24 GMT
USER user
# Tue, 03 Feb 2026 02:18:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bff507cc72771f546378d6ffea702ce1dfc5f7462c98cf416495c9ea7abf5d7`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 18.3 MB (18287991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b732dda1c983c4e5532a6724cc0691bb7f0d4966d926b8031665b9eb19bdf2f4`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe09db28a7bba924a281417665350a9244ac5212bd2c077490813e7355165af`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 4.7 MB (4709982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:02c91f1c49e783ce02db737a1e321704df556858a8ad779ea708f8e801327d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d96f2236d0bf313e468cac657716937a2916282fb27192e905a3ca5780053c9`

```dockerfile
```

-	Layers:
	-	`sha256:c8fb39701e198922668819c0230131b6ae48c12a1d5b030b29d0a2eb4f184198`  
		Last Modified: Tue, 03 Feb 2026 02:18:35 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69d1c7aa44d9df7724589bd6968e57bcd952b965d7dd14e01f8a0dd52b3fe8c8`  
		Last Modified: Tue, 03 Feb 2026 02:18:34 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:9bd66f1060f9a00e3c4e0bef5e1eeea789fc5f4c5b409aefc8bbcf3135f7dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48685426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9e9708bc24170126dd456a2b01d0c0f067c248903162e7c96091af2380b044`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:20:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:19 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:20:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:20:19 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:20:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:20:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:20:59 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:20:59 GMT
USER user
# Tue, 03 Feb 2026 02:20:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64c57598d1759ed47b0ce33fe2ae3f2ca5dfc344280bee5c91a6e2c2cfc33b`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 17.9 MB (17909993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15370f82ce37fd15003721575f11cd865da7261620aea2b1159317aab5659913`  
		Last Modified: Tue, 03 Feb 2026 02:21:09 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420081012ce7d68e8a87df2713f5901aacfc0a3a49fe4f2ac8aa2e0825c8352`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 4.6 MB (4558319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6849872da14db17e8b671bdfc642713a76fa2d2017b4ee56049715165db3c076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc1f967ef5736068697a132ec3311efa1a7280ec42fdaa1ed74a8029aac60bf`

```dockerfile
```

-	Layers:
	-	`sha256:b50b6b2a3c6822bb550588172036e08689e2b19d58f855b5606aded3012602bf`  
		Last Modified: Tue, 03 Feb 2026 02:21:10 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0382a272fccc29001becae9a6ec2fb967f63ffe7d998d793f67a4ff9b9bfd7e`  
		Last Modified: Tue, 03 Feb 2026 02:21:09 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0e6173a8c52441af65097628532330fc826392fa4253e42657ec878c175208c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53975585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb379b987ac880b692fe2dc3dfd931da9c788161033c4e06239554bb4224eb9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:00 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:21:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:21:00 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:21:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:21:38 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:21:38 GMT
USER user
# Tue, 03 Feb 2026 02:21:38 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0532516bbb7262501000c326f37a0930c04d5f5a6565e14b1190d60f0743ce25`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 19.1 MB (19050649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6975dc48bed2afc9f4f4bd9b1665965ae2863eb4ff8cda14ac16f304476d307d`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d6ba22ebad57591e22d79dd65abfa638d56640df56deb4bf8cceb64e95620b`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 4.8 MB (4781508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2dcaadbe83c3a2a93746c56b19d9f055a7f01810e40da8786b5e2a69a843d506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c18f2b03173ce70e0ebf01ac9749a910865184a273ace4b2b75d21222b7118`

```dockerfile
```

-	Layers:
	-	`sha256:7457b4c9d09e256e51f29dec29c3e51469b7ad175435b171f9c5d18d9599cc7b`  
		Last Modified: Tue, 03 Feb 2026 02:21:48 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff3cd880792431a74dcfdc01b30e2c7bd58e08261221840c6a483be5f9b07ee`  
		Last Modified: Tue, 03 Feb 2026 02:21:47 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; 386

```console
$ docker pull irssi@sha256:d10f5d01b9d383d32f36d497a37e76510561eeeaab8a38217dc142bd2044d611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54909414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccf4252e90be99c5c6384e8ef46f99bd42f9232af75a666a85cc7b80be93dbb`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:34 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:17:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:17:34 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:18:17 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:18:17 GMT
USER user
# Tue, 03 Feb 2026 02:18:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c57cfac3b918f6dafe14bf68c93d7d16a8a4970051d18d2a06c2a0263c9145`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 18.7 MB (18743761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c5a3109babbf5c2a1d4b41cb629cbbf8d5c31b10a16a624d77a5dc4bcc39f`  
		Last Modified: Tue, 03 Feb 2026 02:18:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcbe0576fcf1e6208897d40292c8c455af77f42a3cc963ffaff8613d1ca39c1`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 4.9 MB (4868437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:426742b8e02f677fc2e475fb401cbef173d80d0e52b05e495a053dbe62b14c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47fcdb26283af7bd047252c4c37d59277a0cd6d06d787227002528e3c365a58`

```dockerfile
```

-	Layers:
	-	`sha256:a288faa1621c022dd6bd996b78e6eb5d6ee3897b462366f28ee4c3f8bfd9caca`  
		Last Modified: Tue, 03 Feb 2026 02:18:27 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8db18756472041642ed74f8e1e2ae8db1340756b5fde16825cc70e1a163b56`  
		Last Modified: Tue, 03 Feb 2026 02:18:26 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:55ac6c8d4f6d789fcd2f9caaeb13ce48d776a469d82747e7c1485b5963b19dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58244327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a843d5494442193be8285e2518e0cc0dc17b289884fe2369582b93b61eab8`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:24:37 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:24:37 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:24:37 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:24:37 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:26:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:26:23 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:26:23 GMT
USER user
# Tue, 03 Feb 2026 02:26:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624f9309218047b5688e03740c3f3ec04d0a5b2e096ba1ddb57f22215b1c032e`  
		Last Modified: Tue, 03 Feb 2026 02:26:45 GMT  
		Size: 19.5 MB (19542944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b058eb5982a30c68c6eeb3fddcc4f27b629549cbc9517db75d48bcb1f65cdf`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3765444fdfedf57570813f65ad00dcb9587c7a838f36605feb402e11e81f9b`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 5.1 MB (5097836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:5052a03b5d5ed94c58e1b40d85bcc9e57efe762b73218ad11c008c90311225db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee428904aef2658d2ef8892ffdd5bd384860d0da7ee3179246ea48246a6a9b50`

```dockerfile
```

-	Layers:
	-	`sha256:2fa98124d99ee2944a940c9389ee640f1cd7264bd06b18eac34eea4ceaf8efd6`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3e4620f46fdeae2fb275ccc948845b0e4a8862b657cff3de65766f5fd7fa1e`  
		Last Modified: Tue, 03 Feb 2026 02:26:44 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:42f25149c195922ace2d09f52039c56d767996a84e387c8b4eb7cbce5f7c67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51685610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351bf47836b31594adc21aa27395e93d1a031e65d60247048b80b4a4dd12c1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV HOME=/home/user
# Wed, 14 Jan 2026 06:26:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 06:26:49 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 14 Jan 2026 06:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 14 Jan 2026 06:33:37 GMT
WORKDIR /home/user
# Wed, 14 Jan 2026 06:33:37 GMT
USER user
# Wed, 14 Jan 2026 06:33:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f9ee6f39e761595d5c9e020ae1fb10f95fe2a2951aa757f6de57a94a5d25ab`  
		Last Modified: Wed, 14 Jan 2026 06:35:34 GMT  
		Size: 18.5 MB (18549843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef5f232538194de0e7b47d1c08ae77477427a3951186780b1f80e4a91600b4`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b07d932aff1dc5ee2440e07ea368a0ddb73f2c32cb1a8ab0bfd881b02a53f7`  
		Last Modified: Wed, 14 Jan 2026 06:35:31 GMT  
		Size: 4.9 MB (4860721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:0d0a172cbd5471aa3ec8392dc55c5bad0e4fe5bb8e39202b61a8ad6e7252ed2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f4f48da90e6ab7c83ee1b3d3d3112e940971d8bcbed03f47ee03a7d5cca5a6`

```dockerfile
```

-	Layers:
	-	`sha256:afd4f3e89883cc18160c077e4faf0da05c4455d6e0cf0af04a7f525621cba93f`  
		Last Modified: Wed, 14 Jan 2026 06:35:31 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7e2d6743dc6628d707a2e9780dc009b06754202d718210a4e2690ed143c0b`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; s390x

```console
$ docker pull irssi@sha256:3507e27e096139e6c53256b46253b87c2add6684f0a537a81456df935df58f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54507448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9bb61ec181683066bef513d8c48742e3a8098735e181c1c3fff70935a09bd6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
ENV HOME=/home/user
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:19:25 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Feb 2026 02:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Feb 2026 02:20:02 GMT
WORKDIR /home/user
# Tue, 03 Feb 2026 02:20:02 GMT
USER user
# Tue, 03 Feb 2026 02:20:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8905651585d3b136c5d623c620a4b7471b9176370e9badfa69aa86ab3b0b2771`  
		Last Modified: Tue, 03 Feb 2026 02:20:19 GMT  
		Size: 19.8 MB (19760098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b071b126b87f268a0a29ba9f9fe74d76c9af662cee154d5c7726aae6103dc5c2`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2057418f122012d53f3e9dc13ad0f4d67e6c354b177c2e3cff726f0259e435ff`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 4.9 MB (4905841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:3fb068ad5665041ed11698505383bd5effcaa6e7a9de68a793f560dcdbd63930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7848dc8f3f1945a579bb92f67c19f8ef6b9817196a982d578c50208a9d0cb6f`

```dockerfile
```

-	Layers:
	-	`sha256:90c9b6efea1e9a1c048095f2ecb0af339f8475c5029d9074730a486e02732943`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67606c2343b9ace2f5fd62625eb54620eac701413090a31982ee610dcd1e006f`  
		Last Modified: Tue, 03 Feb 2026 02:20:18 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json
