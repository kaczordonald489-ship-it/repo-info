<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spiped`

-	[`spiped:1`](#spiped1)
-	[`spiped:1-alpine`](#spiped1-alpine)
-	[`spiped:1.6`](#spiped16)
-	[`spiped:1.6-alpine`](#spiped16-alpine)
-	[`spiped:1.6.4`](#spiped164)
-	[`spiped:1.6.4-alpine`](#spiped164-alpine)
-	[`spiped:alpine`](#spipedalpine)
-	[`spiped:latest`](#spipedlatest)

## `spiped:1`

```console
$ docker pull spiped@sha256:34315b961d97a51a2f75462b746fe8d36675f1cbc14efc584e59d4e3c7474a14
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

### `spiped:1` - linux; amd64

```console
$ docker pull spiped@sha256:b3660acfa7a6a9cf97d1a5f93df3664e3e03bc08d910dab9b4b54848908a258b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36829177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3372948bef2f8d7c6739c6204657e83fb87886fcc88b375918094272e282f408`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:44:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 03:44:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:45:14 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 03:45:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:45:14 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 03:45:14 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 03:45:14 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:45:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:45:14 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a39244bed5ea8df7cb602a090dbbd3939b97f478baa139e3aee1e5a704e2b35`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da47b3153bf0722ec1767737c189949df5c1c3e97723a4c6ffc89122a2a7c01`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72580f5c19083374ba391bfc528f9b44e3a51afb6a5b0d02fa8c59031a9308c0`  
		Last Modified: Tue, 03 Feb 2026 03:45:22 GMT  
		Size: 7.0 MB (7048206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0796f5973461c160794337bb40af6d6be9d8c7d3428a09c11fa955977a71a917`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fd4947db4ca06e91365c991a661ce6626632bb16d6be6b537a14848c4d7d76`  
		Last Modified: Tue, 03 Feb 2026 03:45:22 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:4d99388c193bdf8e8b699d01999d00ec0d2fc5cec3fb4633ffa18667876463cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bf6c967fe6ef5c305d8f8959a6d36b766dc5469be7d5ae3df8a3a4f9a211bb`

```dockerfile
```

-	Layers:
	-	`sha256:2c79eebf592958937bd16a955ab368dedeb6e06b01a34f44731c86d401dbb187`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 3.6 MB (3626224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6fa59c781fe40cd4cc26e11b53f6e32ce1b7d83fb2002738ff56e280f8d5538`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:109585037b63d0abc51efbf37b4ad70e0228247d1e55e0a08438e7e85170e5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33739445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1b9d15e0681349dc0e221452ca8fddaa88baa07b1d0eb939d71466ba91613b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:24:52 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 03:24:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:25:24 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 03:25:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:25:24 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 03:25:24 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 03:25:24 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:25:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b458a4c9218319872f47d5435f0cdfb3b09636dc7f888b37ef49cdb46c70c8`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbeba32ee56074d975540593173b1eb1cb2a55122d770171b03fb49a6514ef95`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 835.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae365a816bc4b9d002b6c4b8ea75585dfc0ead71e4e8a6101c6bb2607a1d5295`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 5.8 MB (5789512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d02d4e2cf01320108039dc28276d4db4f84f09a42b67451f3b8804fa23ab72`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cac25af4583ededf146f86babef7ebfc2aca84fa0f007d835968066eb646ae5`  
		Last Modified: Tue, 03 Feb 2026 03:25:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:29ab4d3ebb43cdf0bee03a52b5937b6ef650c1333d2867f16fb087504b8fd235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c144228fed63e13f70d75d8302e895c7f203f7c040da3ffd35c4197e34406ea9`

```dockerfile
```

-	Layers:
	-	`sha256:cd7f0f86f71184db69f10a9ec9de636883be6a73ece119da2f41fd9458bb3b2e`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 3.6 MB (3619218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636a639c9a36fc7e25753a33e119e0d643e972123002f04d0854abd6410661c9`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:2db234f117df0f3bb6d6bdaf1c3c32fcc47310588ac51b92cafcfdaa2a495945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31800771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db8a26d24435640659c3cc86c7c12f64fa75e291a657a0083272899caab2112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:28:12 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 03:28:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 03:28:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:28:39 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 03:28:39 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 03:28:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:28:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:28:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0c6df2b95e059eb6b4a0862339f6ebceb74af147d2a41d012d8d060b5de415`  
		Last Modified: Tue, 03 Feb 2026 03:28:46 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0664940b3aae87aa58fc424fca71375278ce662985f954c7983028d752bafacc`  
		Last Modified: Tue, 03 Feb 2026 03:28:46 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e5a94203a10ff32000a8c0ebd03be7cb400d2fe21c3abdd898fa2154950d17`  
		Last Modified: Tue, 03 Feb 2026 03:28:47 GMT  
		Size: 5.6 MB (5584651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97237f1098ba03c1cd5077978ab4ce814a06a400a6638d16e23bebeaebf38ec`  
		Last Modified: Tue, 03 Feb 2026 03:28:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c10fbeab436bcf9758306ef8bd0b97e1af3dcb3da6591d0a7857810b57fe1b`  
		Last Modified: Tue, 03 Feb 2026 03:28:47 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:dbfe43d783cc81a3f9a6e036a235a7bd73805ff41a6801c4d2b2e470c3d58d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb29e7b1482a847481858e027aee1372bc60b2311b95628754b2f1b10ecaa33`

```dockerfile
```

-	Layers:
	-	`sha256:2ee5233df73b0c0ac70f36a5fcf4432cc9a1cbeb39b093abeeea90e80e5892b7`  
		Last Modified: Tue, 03 Feb 2026 03:28:47 GMT  
		Size: 3.6 MB (3618339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae58f5efea5807b4dbaddf41a8e713795b0d010c8edae28cd8065c2fcd2f0b73`  
		Last Modified: Tue, 03 Feb 2026 03:28:46 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0bdd0976e20f1acc9da2f7e2f38593dd3a50dcc087d5c187b4171f48ad3cc2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36375265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c49dcde0f9bab665574bee4cd9730d12851c7a1fe4d23b316dd9b10cee0b4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:43:36 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 02:43:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:01 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 02:44:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:44:01 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 02:44:01 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 02:44:01 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:44:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:44:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79064b13669c24767c630a07d76f9e042c468d7f40ca82f42d303bf2be4b2b10`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc46fd10114f43117c0ab2973feb788c02135531ddae05d59ae6d76879484557`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8922319902b1ebfe33f49b30b6ff2459d48ebe911999cbdb9925f498368110c2`  
		Last Modified: Tue, 03 Feb 2026 02:44:09 GMT  
		Size: 6.2 MB (6232826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f955d89d90ca6f1fdabd3019bfc4b670b2ee30029964553e30a5038cb814382`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae512a1d3f02e4268ff11ea8a34b88fd9b6ecd39a919636f6796577b91a221f`  
		Last Modified: Tue, 03 Feb 2026 02:44:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:62381220fa8be885003b494140a6a223d59366d095e22d07adc386816f5320ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8f7ad13ce93ec496896006709bbfada6506515b9aa7625421f99a8617cc37d`

```dockerfile
```

-	Layers:
	-	`sha256:5cc9d869283c2d37bc51695715d16b8714cc723f3e5f2dc0c071dfd6c129c085`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 3.6 MB (3621260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9e154fec71f9918fa0df235055eddf49f9d3dec0c19a8375e274e17fa0e0f94`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:728d78d73281646241fcb222dd9d31839cc9aac1002495caf447df5a12ef920d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37738880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9564f7127f6b19ae5edc1b7f098e2b5b56ba26da5624f12f8584011789e48511`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:08 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 02:49:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:35 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 02:49:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:49:35 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 02:49:35 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 02:49:35 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:49:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02829238b73397f5db890306da7b1f20106c90b28ca1b84ba15b5c229988d41`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4c072969b7cd6ee6467a4a3a8f1dcb749e0dd44d587ed12aed46112cc3f7f5`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87a1e605addae0e4b7407519d3894921fb10c0ec0c56901cb897f7648f7e02f`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 6.4 MB (6442653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ab5f20c688ea298a203de76462564834f67c9ae32e08abe388568afc9601b4`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1228c6ab6d3ba9275ec1bdf95149ba0707aac1bc10e56a008e54869ed8c067e6`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:3f7115b5b9ffad8cf20373c0cedc384e1d578a3f8a7a76efdd1c411fa21c6e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4979b6c39719537a1a3389ce653676cba980691dabacf86bd9bf60de44411192`

```dockerfile
```

-	Layers:
	-	`sha256:fc748c2e8ded79871f86fca112978f029acdf4be424dc35223ea12e68eaccf66`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 3.6 MB (3620353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01f61cc4549486f16775e1a20ae99dc3952a5a48da9ac5400003ca5116c8bae`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 14.9 KB (14945 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:00be49bc99e5b1b637212c605b1848e0b4df978cc1034499cfaea49b6cacb195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40442941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a74d36a815a80a1ee0731f7f9d410231c3f06cd8ffce9e56ec21426052cdbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:21:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 05:21:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:22:15 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 05:22:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 05:22:15 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 05:22:15 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 05:22:16 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 05:22:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 05:22:16 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54dfec51c06ef5546fc59a333f4b2a700322fc6c08919bf3a34ec2a5634f7b3`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb6ba71a55079b27d2707951a5de51bb2735b3c843e7de0603e966f576a4b42`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa10d34f820fe96de44722a9d2956fd2fffb6c97bfdedbe70eefe38c76f4e372`  
		Last Modified: Tue, 03 Feb 2026 05:22:31 GMT  
		Size: 6.8 MB (6840384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a84985e24e00269a3c8628e7ff0586606414c566bc3a545ceb82366fca76b2`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36df81ecd8796a18c1949857ba62294cf17fe04d7c01f5794facab1eed173ad0`  
		Last Modified: Tue, 03 Feb 2026 05:22:31 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:e34582c751fb4395383437efc5f2ec1e67212bcb14fbc6d710ccd948b6b76e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14889a1d30656cb6f7af02127fae886ef833336f77c621279f791307c5b87a66`

```dockerfile
```

-	Layers:
	-	`sha256:34553b7d1a70804c1f632c8f54460c9d539a26a9f51085d8abdbb770a45417b8`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 3.6 MB (3621961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef2dc18746c6c4784daccf3fb9a520974f92134b86634839540e539c353f9b8`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; riscv64

```console
$ docker pull spiped@sha256:c3726522ae3244f8e5fc4fff7b8f5caaa648c5af80dd1242df5b9b0203a50b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37632620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6901900fa0f28a8994f2a5c6167065703cea25c38b46e682c7aa85ebf4c50f8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 05:28:46 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 16 Jan 2026 05:29:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 05:32:13 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 16 Jan 2026 05:32:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 16 Jan 2026 05:32:13 GMT
VOLUME [/spiped]
# Fri, 16 Jan 2026 05:32:13 GMT
WORKDIR /spiped
# Fri, 16 Jan 2026 05:32:13 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 05:32:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 05:32:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0565826c8fe4b1dacce6d9e839c402d5f7f058df52502fb3afc9c1fe362273ab`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54f9b8a5d71461439339ce26a0c07c07fbc5a8f883874f06636ae124d4b6406`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e14934a15b1e232262f936875f5c3c3faf525c75fb01a98c1e77355c8d3879`  
		Last Modified: Fri, 16 Jan 2026 05:33:27 GMT  
		Size: 9.4 MB (9358574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcad698be725811e7e426b85f2dd52a1d1e7963a1d1977d99b6853d7b29d1d99`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492e62971c5bbebb5c3ac87efe8c5f00292840225c2295daf96e49886856bd0d`  
		Last Modified: Fri, 16 Jan 2026 05:33:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:20c580ff798af1e2f3b4ea4d32d2a4df3f8a4d6cf589acca184232c7eb9ff72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e539bf6b82092c6a4f98991afff364af3c7d9c9f618a72fdbf396b9090cbdd62`

```dockerfile
```

-	Layers:
	-	`sha256:468f7c87bf94fe22429b696b878ab697ecd32432c631e71062b7bd058b3faab0`  
		Last Modified: Fri, 16 Jan 2026 05:33:26 GMT  
		Size: 3.6 MB (3613367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7df9a72d10446f51bf6f2ad7ea6f3b30523ac77067a2eef729971e3a94c4d9a`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:138fe4dcc8fb5c0df1a9fe39769aa482f8103179104fb7822432be26d9dc06f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35962521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2d8e7d46dd49c524188f2706e57f1bf10de8a88227685ba47956a2187b9e35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:43:35 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 03:43:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 03:43:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:43:54 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 03:43:54 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 03:43:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:43:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:43:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cb804f8c11f523ce62a7bc09d236baf84abd6e284119dc6e7c812b046ba3ce`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8af71d5729ead8e60802ee40cd20b30288f02d50d14e682fc9af8c7a6aae22`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4467051214cb85c78e6cb79968f755a9833b4b38239855bb9eaca4f83bb5bd`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 6.1 MB (6121999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099202750066c7aa99797cb9282aa06e8187d7a87d111d1af849e70e955f5045`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd30b70482ee075552a0a8c1163f912098b4cfc94f09bb564d7846c8ae6ac9b`  
		Last Modified: Tue, 03 Feb 2026 03:44:06 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:00b19a2ff8b9daff2d46f3641d4e0f1be5d24395d4dfe12e381a836c8ac5e89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f5f17e17e5f54014ea830b208ced2160254e9afd41c57533a22f20ba746d9c`

```dockerfile
```

-	Layers:
	-	`sha256:edf825008cc03344fb619906e7e7ec2b9fc14fd95212f82320a2b93e91e1ade1`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 3.6 MB (3618587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3e88bd64df43446d50200b8b468c4d96319ccedeaec436cca1e26bfa1c2a59`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:2e861202f057586ae2e6dc3a5290d61949120d861e272b5700c1e30e1ae9774c
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

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:45aa25e16b20aaf22415c03717dfbffb2460250d93ccfbf50d304296f0323560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c42c3ad8f87ea2a2987c07857dc357c5caa6eb7fe68f8ab758c81d2c67f6316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:36:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:36:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:36:57 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:36:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:36:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255f2b198269941f9011d88cebad6e20b25c8054b5ac4ebd1b07f9750a69d255`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed562f6049bf766f9af2aeb064224279b938162b44667a74bc7ca9c31ac1d70a`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d0ab7b6d45d1dbeebe557e32936e50678b9985769e6bd0ff3e1ff5e433e69`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 107.6 KB (107647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868415b885be47751e88ed3c97ca195abec55deffeb9f4ad2846ad3d25cdec28`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d8f030e4a64f48108d2120539708364c71dc39133649b15a0ad263ec9bfe40`  
		Last Modified: Wed, 28 Jan 2026 02:37:04 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:14bccfab21e7b3f36806b9521edfd711ef99c418ce1a38f2c913859e95caa2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0f387ff25d96b6eec2a5942d1be095ce8d2cd8945dadefd293a3706d31ea69`

```dockerfile
```

-	Layers:
	-	`sha256:3abca7ed4aae68f57768d18d39b5d6b1c58a733af4507188677241020e39e0d9`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6768ac276576d5f59511c63ded4afa12e2d77d28be7bffc6d1537d58bb57bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 14.3 KB (14259 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3840e207c5f175385b57ca037766c41623e4a780197b93760ca83297bd8e51ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07ce0978d45ec15bdc0a08bdc59ff908f2bd78005af85d4bbad7345be081ee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:44 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a5ad93e4f03c704fabcd2728cb1ab8244c96ef0876f3fcc9779085a8d3be96`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092107d3ff0fcf3229ae39acf729a354fda97b10c713e7073d550bb7c69025bc`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb00245db6ff8769dfa116d0e6194c8908449cd54b3995e5f0044b278d0fb45`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 89.2 KB (89154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3375ee92dad5bd59b0dde03ad45bdf7a8f7df3aaa1e2847b17cdd6734893cfb8`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc41431154f4cccb130328f9bda92ac3cd374c3bc4ef8b29827399ebd22bc749`  
		Last Modified: Wed, 28 Jan 2026 02:56:49 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:193c4ff5e06269d1446ab3235284aa43d244fdbc13dffdc98c715540fcc455e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060b8b064e4aba529d56ef354367ffae940f6b152b36f64ea427dfcd51e51f1e`

```dockerfile
```

-	Layers:
	-	`sha256:9257c6b08dae939c45fb6b5cd969064dde84328d15653df8b0ab98dae6b31d32`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 14.1 KB (14146 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:71592cfee4b071cad3b52c3cfdefddd8ff72e3d5e644d8859d2d8cec8397a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c48ddb927471eeb09c0d2e183b02bb1074d36b5caa9dbd3477ee935a8eed01f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:25 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:34 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ba379620ebeacb95d57ee5ff3ce395b9868fe9f8d00a5b85dd41df19b3a23`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471e6c87dbde5f46d8cd1e26b6a653a7d77209c851df54df0c065355b1c36749`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 8.0 KB (7952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917e2b19aaa32cc304579e079305131ee112e7015524177e84f33379315c24f6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 81.7 KB (81685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d229583db181996be822e85b4fe259ecd55350b04637a090977de317d8cb53`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283dd24da1a4b40bed9d28f9196f24341abf5ee8a13f180db2b3e6daa7e85b8d`  
		Last Modified: Wed, 28 Jan 2026 02:56:40 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b0d30665b0b25a584022937647a82e260a99dc3822f06eae03c777c08c589459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de7b9137b4705f6bfaa43d68be9ab47cda877656a88568a8b98eaecf834d723`

```dockerfile
```

-	Layers:
	-	`sha256:bf20f6c9425bc14bf83c368ad820cbac85037f9cfe9e8f428105dcae79aa5f0a`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c326467351e8aaa1070327395a8ce06feaf36e791288cc8d0efc059293853a6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:effcfa5e900325dc5a9f2ce725d32bb928170b9fae13c2414035f7c74db4832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129da21c1ac14cfe9747c51280fa104e3e2a4a7fb499fce9d2f79394c096e45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:37:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:37:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:37:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:37:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215f43d3f31692bff6dbb7a8464a9777ff146fd6817d85616dd79d628db9a4e`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a149826e8201bd60e39e8acb8c71ee749c537b2c783a541e04af7a7b3fc6b5d`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3816514d66f19e4e15afc0dae177ea8f1397bbaeba0189b4a33a3f265afbb21`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 100.6 KB (100615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f073eca19d0c28ea18c16d7aa1388a52393935ac0e76036549b53fca85d50741`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ae442366147b99273aabaaf180c7a0347dd957817ff21ec6495a8f374fd7b5`  
		Last Modified: Wed, 28 Jan 2026 02:38:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:20c426c97f5ccc77dcb4c2895905f7a3e9aedaf5bf12fbf4b3ff87748f7ebc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f74a0ff8267a4110c62ab6dcdcf2bf4949f9f54a7ff5e5b96a7e78b99f9770c`

```dockerfile
```

-	Layers:
	-	`sha256:ce7e8f74c44956e8b3a9213e0686a5007c77ddc5cd5210760e512537c99dcb4f`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5744a1e9a5178b40c2e43ceccdad37fa256e17fb5a7e73342aa361c38b071ea6`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:d29799b7499dd97718236dec910ca0fb21a58b93b04c13b9d32bd3972850d109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c829adab8d4ab1c5c9eef2ab8cd6fc3b09ac7a5b2c98b60eb750eaadcf3ca449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:31:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:31:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:31:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:31:32 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:31:32 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:31:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088b329d71531fcaf8b6b6b5fb05bd132488a9b146463fda72d73f3b193da77`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6327ced333146d36cce9bad13d15f14d00cfba342ef14347eb76323f377623`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f74692486d32e3c25efb4bcdbdd450b58db493d05a003140a026ba85c130a6`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 120.1 KB (120096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b377c56ed7e39aeec7320819a810cd8637819dc2c7f00e5f02f6008223d5ed8`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e023ec54765d4d3764e0855b6d7cfe0e2f9966db68bd933fe3f4fe6c41a2474f`  
		Last Modified: Wed, 28 Jan 2026 02:31:38 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:49494f0bf8ea2a9ac91bc338facd2f7cede025b28b7848656878d7ce0deadf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16387e224ee0b4762e3111436b2fdc3a8bfebe61d796cc65af094da1ebf76cd0`

```dockerfile
```

-	Layers:
	-	`sha256:bdc547d749394448a39cd679c285ba250424589df32f26c116cdc3bca37fedf9`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f968b5a19cf7dfb341a81ce64526ba67dbdecae7dbd82f7332ab1f24bf7e26a`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 14.2 KB (14223 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:ec49e51d1b31aef6ee4c32cbd2374c5115032febd535905c0146f19ca7d1b88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3856312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52e05f6841b2c0f9dcb913e52c349b3ec2747c75f53e9b3d6a41cd3c6103a9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:19 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:59:21 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:59:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:59:33 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:59:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:59:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52389dd33bb155b2c78fa5202c8c9909e97b12049d41f7cb5369100d2a7be819`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd5646a7c2ce724b02160a31080c85b3571ffddbc309ccb39fb23e5075d4aa`  
		Last Modified: Wed, 28 Jan 2026 03:59:47 GMT  
		Size: 8.0 KB (7956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d83f042b4cb936ae2f704768b0462b7f539ba799143799dc6a8ce0babc73884`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 112.7 KB (112673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f4a6884030927f7cdd451b10bba40c6cf61fd40534ca3a9cf653bb742ea8f`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fbfb80739dd4ce26eb065be080a75c602340f3242a297925caf40baf400db0`  
		Last Modified: Wed, 28 Jan 2026 03:59:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1d08517919e2dfe608c1e408886b7ef4659cd9f15bf49a67583fe931eb307650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68d34137d518c2381ecd841ecef0a23786265f08c1952e0ed2134cc2ba9073`

```dockerfile
```

-	Layers:
	-	`sha256:b57bb2bf93c55cd637df776032387ee2beae0039a87bacf4e588dd43aaa36711`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a73d72709b0315e9f657137bb6dbf7c0679131d8e10876ea8a1bb94e4201b4`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0e7e07e5944d0951da4949f8298cdccfa6ec9395c2d0ddf983aa7f40bf7807f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565f6907e5ae385b224d048c255c22407d6a59d79533da4912c486d4ee1360`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:56:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 29 Jan 2026 18:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 29 Jan 2026 18:58:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
VOLUME [/spiped]
# Thu, 29 Jan 2026 18:58:39 GMT
WORKDIR /spiped
# Thu, 29 Jan 2026 18:58:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 18:58:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:58:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85b2fc2b9bdc2a30eea3483d034231cba4cf794b774e9c668e43189f965204b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a35d458c7098a7c5f24f347a75cf6930f742a2e14ae40067defc23e63d57b5`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbbaf165e7e5cf59739b8e5317789f9a907da0dc26f3803ae533e05f7a2068e`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 98.9 KB (98867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0973003e6d2e757a9f14bfb9ab4d4b6be0abf8bbdfa7a9b699232646e0df6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509faeca8d8af4689f4b76d19f92f0deeb48d08e62ab656d5ad988fe97b48e9`  
		Last Modified: Thu, 29 Jan 2026 18:59:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45c5a2bccce0c2d968718cdc5b92e2d54486ce35d6f21169c8e2975138906721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3828726b576d70b513dac001f2810887cf67c235a77086291ebdeb6df7a249f`

```dockerfile
```

-	Layers:
	-	`sha256:53e8f0117ebdf17125860003417afad58a90f091d2b04b6763e9b4ce1899228b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0edfbeca58a13ce30fdd21ef302873aa05c28498d058231b777fe51653a06eb6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 14.3 KB (14304 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:0aeb96b9c7c968a0ad51a4c785e0c76534a115d395c587eacd587a3aad55b360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b72691935166b1882b3040950315ed19d9cf1a3678909a868fa5c27a1a58e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:05:48 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:05:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:05:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:05:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0789ee1817b07966cd80a07b05a82d8e0c9bf85f6053f4955ac4731e47448ad`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e526c5a7e2d6f02b24c7ed3860ec8221dcd7d0c6e4112d267da6729a13890448`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10bca7622d69f6335c554b1c8cec2a82753df66ed9cf072d635820439e1af3c`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.9 KB (96933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d81cea7ec993f5c76e72bd06b1579e878f6a4d1a4a2f11114f710747ef40d4`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086ab53d5ebb5741d97d120d1a1ad7797bf2fda46a7ff1f9a033efa0117cd233`  
		Last Modified: Wed, 28 Jan 2026 03:06:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32f5675d459d866b7c69b2159549861b770e81fa270485088e909f23c515b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76bce779a8727519c7fb65566c2ce929337d21a3d6addd2f301cd51f95516c4`

```dockerfile
```

-	Layers:
	-	`sha256:85780af5cccece93dbeac028f8517ebc14f3298ca69ddd75bcf80809c0ea3432`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797300601f0f43bd14d2b3e327c7100b2a1b8356e4290096f308e710af773718`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:34315b961d97a51a2f75462b746fe8d36675f1cbc14efc584e59d4e3c7474a14
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

### `spiped:1.6` - linux; amd64

```console
$ docker pull spiped@sha256:b3660acfa7a6a9cf97d1a5f93df3664e3e03bc08d910dab9b4b54848908a258b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36829177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3372948bef2f8d7c6739c6204657e83fb87886fcc88b375918094272e282f408`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:44:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 03:44:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:45:14 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 03:45:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:45:14 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 03:45:14 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 03:45:14 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:45:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:45:14 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a39244bed5ea8df7cb602a090dbbd3939b97f478baa139e3aee1e5a704e2b35`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da47b3153bf0722ec1767737c189949df5c1c3e97723a4c6ffc89122a2a7c01`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72580f5c19083374ba391bfc528f9b44e3a51afb6a5b0d02fa8c59031a9308c0`  
		Last Modified: Tue, 03 Feb 2026 03:45:22 GMT  
		Size: 7.0 MB (7048206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0796f5973461c160794337bb40af6d6be9d8c7d3428a09c11fa955977a71a917`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fd4947db4ca06e91365c991a661ce6626632bb16d6be6b537a14848c4d7d76`  
		Last Modified: Tue, 03 Feb 2026 03:45:22 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:4d99388c193bdf8e8b699d01999d00ec0d2fc5cec3fb4633ffa18667876463cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bf6c967fe6ef5c305d8f8959a6d36b766dc5469be7d5ae3df8a3a4f9a211bb`

```dockerfile
```

-	Layers:
	-	`sha256:2c79eebf592958937bd16a955ab368dedeb6e06b01a34f44731c86d401dbb187`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 3.6 MB (3626224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6fa59c781fe40cd4cc26e11b53f6e32ce1b7d83fb2002738ff56e280f8d5538`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:109585037b63d0abc51efbf37b4ad70e0228247d1e55e0a08438e7e85170e5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33739445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1b9d15e0681349dc0e221452ca8fddaa88baa07b1d0eb939d71466ba91613b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:24:52 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 03:24:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:25:24 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 03:25:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:25:24 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 03:25:24 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 03:25:24 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:25:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b458a4c9218319872f47d5435f0cdfb3b09636dc7f888b37ef49cdb46c70c8`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbeba32ee56074d975540593173b1eb1cb2a55122d770171b03fb49a6514ef95`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 835.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae365a816bc4b9d002b6c4b8ea75585dfc0ead71e4e8a6101c6bb2607a1d5295`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 5.8 MB (5789512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d02d4e2cf01320108039dc28276d4db4f84f09a42b67451f3b8804fa23ab72`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cac25af4583ededf146f86babef7ebfc2aca84fa0f007d835968066eb646ae5`  
		Last Modified: Tue, 03 Feb 2026 03:25:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:29ab4d3ebb43cdf0bee03a52b5937b6ef650c1333d2867f16fb087504b8fd235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c144228fed63e13f70d75d8302e895c7f203f7c040da3ffd35c4197e34406ea9`

```dockerfile
```

-	Layers:
	-	`sha256:cd7f0f86f71184db69f10a9ec9de636883be6a73ece119da2f41fd9458bb3b2e`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 3.6 MB (3619218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636a639c9a36fc7e25753a33e119e0d643e972123002f04d0854abd6410661c9`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:2db234f117df0f3bb6d6bdaf1c3c32fcc47310588ac51b92cafcfdaa2a495945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31800771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db8a26d24435640659c3cc86c7c12f64fa75e291a657a0083272899caab2112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:28:12 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 03:28:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 03:28:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:28:39 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 03:28:39 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 03:28:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:28:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:28:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0c6df2b95e059eb6b4a0862339f6ebceb74af147d2a41d012d8d060b5de415`  
		Last Modified: Tue, 03 Feb 2026 03:28:46 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0664940b3aae87aa58fc424fca71375278ce662985f954c7983028d752bafacc`  
		Last Modified: Tue, 03 Feb 2026 03:28:46 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e5a94203a10ff32000a8c0ebd03be7cb400d2fe21c3abdd898fa2154950d17`  
		Last Modified: Tue, 03 Feb 2026 03:28:47 GMT  
		Size: 5.6 MB (5584651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97237f1098ba03c1cd5077978ab4ce814a06a400a6638d16e23bebeaebf38ec`  
		Last Modified: Tue, 03 Feb 2026 03:28:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c10fbeab436bcf9758306ef8bd0b97e1af3dcb3da6591d0a7857810b57fe1b`  
		Last Modified: Tue, 03 Feb 2026 03:28:47 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:dbfe43d783cc81a3f9a6e036a235a7bd73805ff41a6801c4d2b2e470c3d58d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb29e7b1482a847481858e027aee1372bc60b2311b95628754b2f1b10ecaa33`

```dockerfile
```

-	Layers:
	-	`sha256:2ee5233df73b0c0ac70f36a5fcf4432cc9a1cbeb39b093abeeea90e80e5892b7`  
		Last Modified: Tue, 03 Feb 2026 03:28:47 GMT  
		Size: 3.6 MB (3618339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae58f5efea5807b4dbaddf41a8e713795b0d010c8edae28cd8065c2fcd2f0b73`  
		Last Modified: Tue, 03 Feb 2026 03:28:46 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0bdd0976e20f1acc9da2f7e2f38593dd3a50dcc087d5c187b4171f48ad3cc2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36375265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c49dcde0f9bab665574bee4cd9730d12851c7a1fe4d23b316dd9b10cee0b4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:43:36 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 02:43:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:01 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 02:44:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:44:01 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 02:44:01 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 02:44:01 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:44:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:44:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79064b13669c24767c630a07d76f9e042c468d7f40ca82f42d303bf2be4b2b10`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc46fd10114f43117c0ab2973feb788c02135531ddae05d59ae6d76879484557`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8922319902b1ebfe33f49b30b6ff2459d48ebe911999cbdb9925f498368110c2`  
		Last Modified: Tue, 03 Feb 2026 02:44:09 GMT  
		Size: 6.2 MB (6232826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f955d89d90ca6f1fdabd3019bfc4b670b2ee30029964553e30a5038cb814382`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae512a1d3f02e4268ff11ea8a34b88fd9b6ecd39a919636f6796577b91a221f`  
		Last Modified: Tue, 03 Feb 2026 02:44:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:62381220fa8be885003b494140a6a223d59366d095e22d07adc386816f5320ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8f7ad13ce93ec496896006709bbfada6506515b9aa7625421f99a8617cc37d`

```dockerfile
```

-	Layers:
	-	`sha256:5cc9d869283c2d37bc51695715d16b8714cc723f3e5f2dc0c071dfd6c129c085`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 3.6 MB (3621260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9e154fec71f9918fa0df235055eddf49f9d3dec0c19a8375e274e17fa0e0f94`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:728d78d73281646241fcb222dd9d31839cc9aac1002495caf447df5a12ef920d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37738880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9564f7127f6b19ae5edc1b7f098e2b5b56ba26da5624f12f8584011789e48511`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:08 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 02:49:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:35 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 02:49:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:49:35 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 02:49:35 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 02:49:35 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:49:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02829238b73397f5db890306da7b1f20106c90b28ca1b84ba15b5c229988d41`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4c072969b7cd6ee6467a4a3a8f1dcb749e0dd44d587ed12aed46112cc3f7f5`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87a1e605addae0e4b7407519d3894921fb10c0ec0c56901cb897f7648f7e02f`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 6.4 MB (6442653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ab5f20c688ea298a203de76462564834f67c9ae32e08abe388568afc9601b4`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1228c6ab6d3ba9275ec1bdf95149ba0707aac1bc10e56a008e54869ed8c067e6`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:3f7115b5b9ffad8cf20373c0cedc384e1d578a3f8a7a76efdd1c411fa21c6e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4979b6c39719537a1a3389ce653676cba980691dabacf86bd9bf60de44411192`

```dockerfile
```

-	Layers:
	-	`sha256:fc748c2e8ded79871f86fca112978f029acdf4be424dc35223ea12e68eaccf66`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 3.6 MB (3620353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01f61cc4549486f16775e1a20ae99dc3952a5a48da9ac5400003ca5116c8bae`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 14.9 KB (14945 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:00be49bc99e5b1b637212c605b1848e0b4df978cc1034499cfaea49b6cacb195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40442941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a74d36a815a80a1ee0731f7f9d410231c3f06cd8ffce9e56ec21426052cdbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:21:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 05:21:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:22:15 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 05:22:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 05:22:15 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 05:22:15 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 05:22:16 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 05:22:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 05:22:16 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54dfec51c06ef5546fc59a333f4b2a700322fc6c08919bf3a34ec2a5634f7b3`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb6ba71a55079b27d2707951a5de51bb2735b3c843e7de0603e966f576a4b42`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa10d34f820fe96de44722a9d2956fd2fffb6c97bfdedbe70eefe38c76f4e372`  
		Last Modified: Tue, 03 Feb 2026 05:22:31 GMT  
		Size: 6.8 MB (6840384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a84985e24e00269a3c8628e7ff0586606414c566bc3a545ceb82366fca76b2`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36df81ecd8796a18c1949857ba62294cf17fe04d7c01f5794facab1eed173ad0`  
		Last Modified: Tue, 03 Feb 2026 05:22:31 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:e34582c751fb4395383437efc5f2ec1e67212bcb14fbc6d710ccd948b6b76e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14889a1d30656cb6f7af02127fae886ef833336f77c621279f791307c5b87a66`

```dockerfile
```

-	Layers:
	-	`sha256:34553b7d1a70804c1f632c8f54460c9d539a26a9f51085d8abdbb770a45417b8`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 3.6 MB (3621961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef2dc18746c6c4784daccf3fb9a520974f92134b86634839540e539c353f9b8`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; riscv64

```console
$ docker pull spiped@sha256:c3726522ae3244f8e5fc4fff7b8f5caaa648c5af80dd1242df5b9b0203a50b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37632620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6901900fa0f28a8994f2a5c6167065703cea25c38b46e682c7aa85ebf4c50f8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 05:28:46 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 16 Jan 2026 05:29:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 05:32:13 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 16 Jan 2026 05:32:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 16 Jan 2026 05:32:13 GMT
VOLUME [/spiped]
# Fri, 16 Jan 2026 05:32:13 GMT
WORKDIR /spiped
# Fri, 16 Jan 2026 05:32:13 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 05:32:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 05:32:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0565826c8fe4b1dacce6d9e839c402d5f7f058df52502fb3afc9c1fe362273ab`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54f9b8a5d71461439339ce26a0c07c07fbc5a8f883874f06636ae124d4b6406`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e14934a15b1e232262f936875f5c3c3faf525c75fb01a98c1e77355c8d3879`  
		Last Modified: Fri, 16 Jan 2026 05:33:27 GMT  
		Size: 9.4 MB (9358574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcad698be725811e7e426b85f2dd52a1d1e7963a1d1977d99b6853d7b29d1d99`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492e62971c5bbebb5c3ac87efe8c5f00292840225c2295daf96e49886856bd0d`  
		Last Modified: Fri, 16 Jan 2026 05:33:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:20c580ff798af1e2f3b4ea4d32d2a4df3f8a4d6cf589acca184232c7eb9ff72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e539bf6b82092c6a4f98991afff364af3c7d9c9f618a72fdbf396b9090cbdd62`

```dockerfile
```

-	Layers:
	-	`sha256:468f7c87bf94fe22429b696b878ab697ecd32432c631e71062b7bd058b3faab0`  
		Last Modified: Fri, 16 Jan 2026 05:33:26 GMT  
		Size: 3.6 MB (3613367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7df9a72d10446f51bf6f2ad7ea6f3b30523ac77067a2eef729971e3a94c4d9a`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:138fe4dcc8fb5c0df1a9fe39769aa482f8103179104fb7822432be26d9dc06f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35962521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2d8e7d46dd49c524188f2706e57f1bf10de8a88227685ba47956a2187b9e35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:43:35 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 03:43:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 03:43:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:43:54 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 03:43:54 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 03:43:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:43:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:43:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cb804f8c11f523ce62a7bc09d236baf84abd6e284119dc6e7c812b046ba3ce`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8af71d5729ead8e60802ee40cd20b30288f02d50d14e682fc9af8c7a6aae22`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4467051214cb85c78e6cb79968f755a9833b4b38239855bb9eaca4f83bb5bd`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 6.1 MB (6121999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099202750066c7aa99797cb9282aa06e8187d7a87d111d1af849e70e955f5045`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd30b70482ee075552a0a8c1163f912098b4cfc94f09bb564d7846c8ae6ac9b`  
		Last Modified: Tue, 03 Feb 2026 03:44:06 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:00b19a2ff8b9daff2d46f3641d4e0f1be5d24395d4dfe12e381a836c8ac5e89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f5f17e17e5f54014ea830b208ced2160254e9afd41c57533a22f20ba746d9c`

```dockerfile
```

-	Layers:
	-	`sha256:edf825008cc03344fb619906e7e7ec2b9fc14fd95212f82320a2b93e91e1ade1`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 3.6 MB (3618587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3e88bd64df43446d50200b8b468c4d96319ccedeaec436cca1e26bfa1c2a59`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:2e861202f057586ae2e6dc3a5290d61949120d861e272b5700c1e30e1ae9774c
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

### `spiped:1.6-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:45aa25e16b20aaf22415c03717dfbffb2460250d93ccfbf50d304296f0323560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c42c3ad8f87ea2a2987c07857dc357c5caa6eb7fe68f8ab758c81d2c67f6316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:36:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:36:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:36:57 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:36:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:36:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255f2b198269941f9011d88cebad6e20b25c8054b5ac4ebd1b07f9750a69d255`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed562f6049bf766f9af2aeb064224279b938162b44667a74bc7ca9c31ac1d70a`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d0ab7b6d45d1dbeebe557e32936e50678b9985769e6bd0ff3e1ff5e433e69`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 107.6 KB (107647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868415b885be47751e88ed3c97ca195abec55deffeb9f4ad2846ad3d25cdec28`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d8f030e4a64f48108d2120539708364c71dc39133649b15a0ad263ec9bfe40`  
		Last Modified: Wed, 28 Jan 2026 02:37:04 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:14bccfab21e7b3f36806b9521edfd711ef99c418ce1a38f2c913859e95caa2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0f387ff25d96b6eec2a5942d1be095ce8d2cd8945dadefd293a3706d31ea69`

```dockerfile
```

-	Layers:
	-	`sha256:3abca7ed4aae68f57768d18d39b5d6b1c58a733af4507188677241020e39e0d9`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6768ac276576d5f59511c63ded4afa12e2d77d28be7bffc6d1537d58bb57bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 14.3 KB (14259 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3840e207c5f175385b57ca037766c41623e4a780197b93760ca83297bd8e51ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07ce0978d45ec15bdc0a08bdc59ff908f2bd78005af85d4bbad7345be081ee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:44 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a5ad93e4f03c704fabcd2728cb1ab8244c96ef0876f3fcc9779085a8d3be96`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092107d3ff0fcf3229ae39acf729a354fda97b10c713e7073d550bb7c69025bc`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb00245db6ff8769dfa116d0e6194c8908449cd54b3995e5f0044b278d0fb45`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 89.2 KB (89154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3375ee92dad5bd59b0dde03ad45bdf7a8f7df3aaa1e2847b17cdd6734893cfb8`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc41431154f4cccb130328f9bda92ac3cd374c3bc4ef8b29827399ebd22bc749`  
		Last Modified: Wed, 28 Jan 2026 02:56:49 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:193c4ff5e06269d1446ab3235284aa43d244fdbc13dffdc98c715540fcc455e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060b8b064e4aba529d56ef354367ffae940f6b152b36f64ea427dfcd51e51f1e`

```dockerfile
```

-	Layers:
	-	`sha256:9257c6b08dae939c45fb6b5cd969064dde84328d15653df8b0ab98dae6b31d32`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 14.1 KB (14146 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:71592cfee4b071cad3b52c3cfdefddd8ff72e3d5e644d8859d2d8cec8397a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c48ddb927471eeb09c0d2e183b02bb1074d36b5caa9dbd3477ee935a8eed01f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:25 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:34 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ba379620ebeacb95d57ee5ff3ce395b9868fe9f8d00a5b85dd41df19b3a23`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471e6c87dbde5f46d8cd1e26b6a653a7d77209c851df54df0c065355b1c36749`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 8.0 KB (7952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917e2b19aaa32cc304579e079305131ee112e7015524177e84f33379315c24f6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 81.7 KB (81685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d229583db181996be822e85b4fe259ecd55350b04637a090977de317d8cb53`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283dd24da1a4b40bed9d28f9196f24341abf5ee8a13f180db2b3e6daa7e85b8d`  
		Last Modified: Wed, 28 Jan 2026 02:56:40 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b0d30665b0b25a584022937647a82e260a99dc3822f06eae03c777c08c589459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de7b9137b4705f6bfaa43d68be9ab47cda877656a88568a8b98eaecf834d723`

```dockerfile
```

-	Layers:
	-	`sha256:bf20f6c9425bc14bf83c368ad820cbac85037f9cfe9e8f428105dcae79aa5f0a`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c326467351e8aaa1070327395a8ce06feaf36e791288cc8d0efc059293853a6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:effcfa5e900325dc5a9f2ce725d32bb928170b9fae13c2414035f7c74db4832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129da21c1ac14cfe9747c51280fa104e3e2a4a7fb499fce9d2f79394c096e45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:37:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:37:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:37:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:37:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215f43d3f31692bff6dbb7a8464a9777ff146fd6817d85616dd79d628db9a4e`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a149826e8201bd60e39e8acb8c71ee749c537b2c783a541e04af7a7b3fc6b5d`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3816514d66f19e4e15afc0dae177ea8f1397bbaeba0189b4a33a3f265afbb21`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 100.6 KB (100615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f073eca19d0c28ea18c16d7aa1388a52393935ac0e76036549b53fca85d50741`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ae442366147b99273aabaaf180c7a0347dd957817ff21ec6495a8f374fd7b5`  
		Last Modified: Wed, 28 Jan 2026 02:38:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:20c426c97f5ccc77dcb4c2895905f7a3e9aedaf5bf12fbf4b3ff87748f7ebc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f74a0ff8267a4110c62ab6dcdcf2bf4949f9f54a7ff5e5b96a7e78b99f9770c`

```dockerfile
```

-	Layers:
	-	`sha256:ce7e8f74c44956e8b3a9213e0686a5007c77ddc5cd5210760e512537c99dcb4f`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5744a1e9a5178b40c2e43ceccdad37fa256e17fb5a7e73342aa361c38b071ea6`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:d29799b7499dd97718236dec910ca0fb21a58b93b04c13b9d32bd3972850d109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c829adab8d4ab1c5c9eef2ab8cd6fc3b09ac7a5b2c98b60eb750eaadcf3ca449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:31:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:31:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:31:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:31:32 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:31:32 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:31:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088b329d71531fcaf8b6b6b5fb05bd132488a9b146463fda72d73f3b193da77`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6327ced333146d36cce9bad13d15f14d00cfba342ef14347eb76323f377623`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f74692486d32e3c25efb4bcdbdd450b58db493d05a003140a026ba85c130a6`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 120.1 KB (120096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b377c56ed7e39aeec7320819a810cd8637819dc2c7f00e5f02f6008223d5ed8`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e023ec54765d4d3764e0855b6d7cfe0e2f9966db68bd933fe3f4fe6c41a2474f`  
		Last Modified: Wed, 28 Jan 2026 02:31:38 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:49494f0bf8ea2a9ac91bc338facd2f7cede025b28b7848656878d7ce0deadf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16387e224ee0b4762e3111436b2fdc3a8bfebe61d796cc65af094da1ebf76cd0`

```dockerfile
```

-	Layers:
	-	`sha256:bdc547d749394448a39cd679c285ba250424589df32f26c116cdc3bca37fedf9`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f968b5a19cf7dfb341a81ce64526ba67dbdecae7dbd82f7332ab1f24bf7e26a`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 14.2 KB (14223 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:ec49e51d1b31aef6ee4c32cbd2374c5115032febd535905c0146f19ca7d1b88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3856312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52e05f6841b2c0f9dcb913e52c349b3ec2747c75f53e9b3d6a41cd3c6103a9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:19 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:59:21 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:59:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:59:33 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:59:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:59:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52389dd33bb155b2c78fa5202c8c9909e97b12049d41f7cb5369100d2a7be819`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd5646a7c2ce724b02160a31080c85b3571ffddbc309ccb39fb23e5075d4aa`  
		Last Modified: Wed, 28 Jan 2026 03:59:47 GMT  
		Size: 8.0 KB (7956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d83f042b4cb936ae2f704768b0462b7f539ba799143799dc6a8ce0babc73884`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 112.7 KB (112673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f4a6884030927f7cdd451b10bba40c6cf61fd40534ca3a9cf653bb742ea8f`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fbfb80739dd4ce26eb065be080a75c602340f3242a297925caf40baf400db0`  
		Last Modified: Wed, 28 Jan 2026 03:59:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1d08517919e2dfe608c1e408886b7ef4659cd9f15bf49a67583fe931eb307650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68d34137d518c2381ecd841ecef0a23786265f08c1952e0ed2134cc2ba9073`

```dockerfile
```

-	Layers:
	-	`sha256:b57bb2bf93c55cd637df776032387ee2beae0039a87bacf4e588dd43aaa36711`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a73d72709b0315e9f657137bb6dbf7c0679131d8e10876ea8a1bb94e4201b4`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0e7e07e5944d0951da4949f8298cdccfa6ec9395c2d0ddf983aa7f40bf7807f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565f6907e5ae385b224d048c255c22407d6a59d79533da4912c486d4ee1360`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:56:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 29 Jan 2026 18:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 29 Jan 2026 18:58:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
VOLUME [/spiped]
# Thu, 29 Jan 2026 18:58:39 GMT
WORKDIR /spiped
# Thu, 29 Jan 2026 18:58:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 18:58:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:58:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85b2fc2b9bdc2a30eea3483d034231cba4cf794b774e9c668e43189f965204b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a35d458c7098a7c5f24f347a75cf6930f742a2e14ae40067defc23e63d57b5`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbbaf165e7e5cf59739b8e5317789f9a907da0dc26f3803ae533e05f7a2068e`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 98.9 KB (98867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0973003e6d2e757a9f14bfb9ab4d4b6be0abf8bbdfa7a9b699232646e0df6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509faeca8d8af4689f4b76d19f92f0deeb48d08e62ab656d5ad988fe97b48e9`  
		Last Modified: Thu, 29 Jan 2026 18:59:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45c5a2bccce0c2d968718cdc5b92e2d54486ce35d6f21169c8e2975138906721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3828726b576d70b513dac001f2810887cf67c235a77086291ebdeb6df7a249f`

```dockerfile
```

-	Layers:
	-	`sha256:53e8f0117ebdf17125860003417afad58a90f091d2b04b6763e9b4ce1899228b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0edfbeca58a13ce30fdd21ef302873aa05c28498d058231b777fe51653a06eb6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 14.3 KB (14304 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:0aeb96b9c7c968a0ad51a4c785e0c76534a115d395c587eacd587a3aad55b360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b72691935166b1882b3040950315ed19d9cf1a3678909a868fa5c27a1a58e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:05:48 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:05:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:05:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:05:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0789ee1817b07966cd80a07b05a82d8e0c9bf85f6053f4955ac4731e47448ad`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e526c5a7e2d6f02b24c7ed3860ec8221dcd7d0c6e4112d267da6729a13890448`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10bca7622d69f6335c554b1c8cec2a82753df66ed9cf072d635820439e1af3c`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.9 KB (96933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d81cea7ec993f5c76e72bd06b1579e878f6a4d1a4a2f11114f710747ef40d4`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086ab53d5ebb5741d97d120d1a1ad7797bf2fda46a7ff1f9a033efa0117cd233`  
		Last Modified: Wed, 28 Jan 2026 03:06:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32f5675d459d866b7c69b2159549861b770e81fa270485088e909f23c515b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76bce779a8727519c7fb65566c2ce929337d21a3d6addd2f301cd51f95516c4`

```dockerfile
```

-	Layers:
	-	`sha256:85780af5cccece93dbeac028f8517ebc14f3298ca69ddd75bcf80809c0ea3432`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797300601f0f43bd14d2b3e327c7100b2a1b8356e4290096f308e710af773718`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4`

```console
$ docker pull spiped@sha256:34315b961d97a51a2f75462b746fe8d36675f1cbc14efc584e59d4e3c7474a14
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

### `spiped:1.6.4` - linux; amd64

```console
$ docker pull spiped@sha256:b3660acfa7a6a9cf97d1a5f93df3664e3e03bc08d910dab9b4b54848908a258b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36829177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3372948bef2f8d7c6739c6204657e83fb87886fcc88b375918094272e282f408`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:44:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 03:44:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:45:14 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 03:45:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:45:14 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 03:45:14 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 03:45:14 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:45:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:45:14 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a39244bed5ea8df7cb602a090dbbd3939b97f478baa139e3aee1e5a704e2b35`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da47b3153bf0722ec1767737c189949df5c1c3e97723a4c6ffc89122a2a7c01`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72580f5c19083374ba391bfc528f9b44e3a51afb6a5b0d02fa8c59031a9308c0`  
		Last Modified: Tue, 03 Feb 2026 03:45:22 GMT  
		Size: 7.0 MB (7048206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0796f5973461c160794337bb40af6d6be9d8c7d3428a09c11fa955977a71a917`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fd4947db4ca06e91365c991a661ce6626632bb16d6be6b537a14848c4d7d76`  
		Last Modified: Tue, 03 Feb 2026 03:45:22 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:4d99388c193bdf8e8b699d01999d00ec0d2fc5cec3fb4633ffa18667876463cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bf6c967fe6ef5c305d8f8959a6d36b766dc5469be7d5ae3df8a3a4f9a211bb`

```dockerfile
```

-	Layers:
	-	`sha256:2c79eebf592958937bd16a955ab368dedeb6e06b01a34f44731c86d401dbb187`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 3.6 MB (3626224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6fa59c781fe40cd4cc26e11b53f6e32ce1b7d83fb2002738ff56e280f8d5538`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v5

```console
$ docker pull spiped@sha256:109585037b63d0abc51efbf37b4ad70e0228247d1e55e0a08438e7e85170e5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33739445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1b9d15e0681349dc0e221452ca8fddaa88baa07b1d0eb939d71466ba91613b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:24:52 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 03:24:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:25:24 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 03:25:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:25:24 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 03:25:24 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 03:25:24 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:25:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b458a4c9218319872f47d5435f0cdfb3b09636dc7f888b37ef49cdb46c70c8`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbeba32ee56074d975540593173b1eb1cb2a55122d770171b03fb49a6514ef95`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 835.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae365a816bc4b9d002b6c4b8ea75585dfc0ead71e4e8a6101c6bb2607a1d5295`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 5.8 MB (5789512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d02d4e2cf01320108039dc28276d4db4f84f09a42b67451f3b8804fa23ab72`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cac25af4583ededf146f86babef7ebfc2aca84fa0f007d835968066eb646ae5`  
		Last Modified: Tue, 03 Feb 2026 03:25:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:29ab4d3ebb43cdf0bee03a52b5937b6ef650c1333d2867f16fb087504b8fd235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c144228fed63e13f70d75d8302e895c7f203f7c040da3ffd35c4197e34406ea9`

```dockerfile
```

-	Layers:
	-	`sha256:cd7f0f86f71184db69f10a9ec9de636883be6a73ece119da2f41fd9458bb3b2e`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 3.6 MB (3619218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636a639c9a36fc7e25753a33e119e0d643e972123002f04d0854abd6410661c9`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v7

```console
$ docker pull spiped@sha256:2db234f117df0f3bb6d6bdaf1c3c32fcc47310588ac51b92cafcfdaa2a495945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31800771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db8a26d24435640659c3cc86c7c12f64fa75e291a657a0083272899caab2112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:28:12 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 03:28:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 03:28:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:28:39 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 03:28:39 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 03:28:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:28:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:28:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0c6df2b95e059eb6b4a0862339f6ebceb74af147d2a41d012d8d060b5de415`  
		Last Modified: Tue, 03 Feb 2026 03:28:46 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0664940b3aae87aa58fc424fca71375278ce662985f954c7983028d752bafacc`  
		Last Modified: Tue, 03 Feb 2026 03:28:46 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e5a94203a10ff32000a8c0ebd03be7cb400d2fe21c3abdd898fa2154950d17`  
		Last Modified: Tue, 03 Feb 2026 03:28:47 GMT  
		Size: 5.6 MB (5584651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97237f1098ba03c1cd5077978ab4ce814a06a400a6638d16e23bebeaebf38ec`  
		Last Modified: Tue, 03 Feb 2026 03:28:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c10fbeab436bcf9758306ef8bd0b97e1af3dcb3da6591d0a7857810b57fe1b`  
		Last Modified: Tue, 03 Feb 2026 03:28:47 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:dbfe43d783cc81a3f9a6e036a235a7bd73805ff41a6801c4d2b2e470c3d58d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb29e7b1482a847481858e027aee1372bc60b2311b95628754b2f1b10ecaa33`

```dockerfile
```

-	Layers:
	-	`sha256:2ee5233df73b0c0ac70f36a5fcf4432cc9a1cbeb39b093abeeea90e80e5892b7`  
		Last Modified: Tue, 03 Feb 2026 03:28:47 GMT  
		Size: 3.6 MB (3618339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae58f5efea5807b4dbaddf41a8e713795b0d010c8edae28cd8065c2fcd2f0b73`  
		Last Modified: Tue, 03 Feb 2026 03:28:46 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0bdd0976e20f1acc9da2f7e2f38593dd3a50dcc087d5c187b4171f48ad3cc2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36375265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c49dcde0f9bab665574bee4cd9730d12851c7a1fe4d23b316dd9b10cee0b4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:43:36 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 02:43:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:01 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 02:44:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:44:01 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 02:44:01 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 02:44:01 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:44:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:44:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79064b13669c24767c630a07d76f9e042c468d7f40ca82f42d303bf2be4b2b10`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc46fd10114f43117c0ab2973feb788c02135531ddae05d59ae6d76879484557`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8922319902b1ebfe33f49b30b6ff2459d48ebe911999cbdb9925f498368110c2`  
		Last Modified: Tue, 03 Feb 2026 02:44:09 GMT  
		Size: 6.2 MB (6232826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f955d89d90ca6f1fdabd3019bfc4b670b2ee30029964553e30a5038cb814382`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae512a1d3f02e4268ff11ea8a34b88fd9b6ecd39a919636f6796577b91a221f`  
		Last Modified: Tue, 03 Feb 2026 02:44:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:62381220fa8be885003b494140a6a223d59366d095e22d07adc386816f5320ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8f7ad13ce93ec496896006709bbfada6506515b9aa7625421f99a8617cc37d`

```dockerfile
```

-	Layers:
	-	`sha256:5cc9d869283c2d37bc51695715d16b8714cc723f3e5f2dc0c071dfd6c129c085`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 3.6 MB (3621260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9e154fec71f9918fa0df235055eddf49f9d3dec0c19a8375e274e17fa0e0f94`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; 386

```console
$ docker pull spiped@sha256:728d78d73281646241fcb222dd9d31839cc9aac1002495caf447df5a12ef920d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37738880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9564f7127f6b19ae5edc1b7f098e2b5b56ba26da5624f12f8584011789e48511`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:08 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 02:49:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:35 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 02:49:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:49:35 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 02:49:35 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 02:49:35 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:49:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02829238b73397f5db890306da7b1f20106c90b28ca1b84ba15b5c229988d41`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4c072969b7cd6ee6467a4a3a8f1dcb749e0dd44d587ed12aed46112cc3f7f5`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87a1e605addae0e4b7407519d3894921fb10c0ec0c56901cb897f7648f7e02f`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 6.4 MB (6442653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ab5f20c688ea298a203de76462564834f67c9ae32e08abe388568afc9601b4`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1228c6ab6d3ba9275ec1bdf95149ba0707aac1bc10e56a008e54869ed8c067e6`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:3f7115b5b9ffad8cf20373c0cedc384e1d578a3f8a7a76efdd1c411fa21c6e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4979b6c39719537a1a3389ce653676cba980691dabacf86bd9bf60de44411192`

```dockerfile
```

-	Layers:
	-	`sha256:fc748c2e8ded79871f86fca112978f029acdf4be424dc35223ea12e68eaccf66`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 3.6 MB (3620353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01f61cc4549486f16775e1a20ae99dc3952a5a48da9ac5400003ca5116c8bae`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 14.9 KB (14945 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; ppc64le

```console
$ docker pull spiped@sha256:00be49bc99e5b1b637212c605b1848e0b4df978cc1034499cfaea49b6cacb195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40442941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a74d36a815a80a1ee0731f7f9d410231c3f06cd8ffce9e56ec21426052cdbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:21:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 05:21:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:22:15 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 05:22:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 05:22:15 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 05:22:15 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 05:22:16 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 05:22:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 05:22:16 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54dfec51c06ef5546fc59a333f4b2a700322fc6c08919bf3a34ec2a5634f7b3`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb6ba71a55079b27d2707951a5de51bb2735b3c843e7de0603e966f576a4b42`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa10d34f820fe96de44722a9d2956fd2fffb6c97bfdedbe70eefe38c76f4e372`  
		Last Modified: Tue, 03 Feb 2026 05:22:31 GMT  
		Size: 6.8 MB (6840384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a84985e24e00269a3c8628e7ff0586606414c566bc3a545ceb82366fca76b2`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36df81ecd8796a18c1949857ba62294cf17fe04d7c01f5794facab1eed173ad0`  
		Last Modified: Tue, 03 Feb 2026 05:22:31 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:e34582c751fb4395383437efc5f2ec1e67212bcb14fbc6d710ccd948b6b76e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14889a1d30656cb6f7af02127fae886ef833336f77c621279f791307c5b87a66`

```dockerfile
```

-	Layers:
	-	`sha256:34553b7d1a70804c1f632c8f54460c9d539a26a9f51085d8abdbb770a45417b8`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 3.6 MB (3621961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef2dc18746c6c4784daccf3fb9a520974f92134b86634839540e539c353f9b8`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; riscv64

```console
$ docker pull spiped@sha256:c3726522ae3244f8e5fc4fff7b8f5caaa648c5af80dd1242df5b9b0203a50b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37632620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6901900fa0f28a8994f2a5c6167065703cea25c38b46e682c7aa85ebf4c50f8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 05:28:46 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 16 Jan 2026 05:29:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 05:32:13 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 16 Jan 2026 05:32:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 16 Jan 2026 05:32:13 GMT
VOLUME [/spiped]
# Fri, 16 Jan 2026 05:32:13 GMT
WORKDIR /spiped
# Fri, 16 Jan 2026 05:32:13 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 05:32:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 05:32:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0565826c8fe4b1dacce6d9e839c402d5f7f058df52502fb3afc9c1fe362273ab`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54f9b8a5d71461439339ce26a0c07c07fbc5a8f883874f06636ae124d4b6406`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e14934a15b1e232262f936875f5c3c3faf525c75fb01a98c1e77355c8d3879`  
		Last Modified: Fri, 16 Jan 2026 05:33:27 GMT  
		Size: 9.4 MB (9358574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcad698be725811e7e426b85f2dd52a1d1e7963a1d1977d99b6853d7b29d1d99`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492e62971c5bbebb5c3ac87efe8c5f00292840225c2295daf96e49886856bd0d`  
		Last Modified: Fri, 16 Jan 2026 05:33:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:20c580ff798af1e2f3b4ea4d32d2a4df3f8a4d6cf589acca184232c7eb9ff72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e539bf6b82092c6a4f98991afff364af3c7d9c9f618a72fdbf396b9090cbdd62`

```dockerfile
```

-	Layers:
	-	`sha256:468f7c87bf94fe22429b696b878ab697ecd32432c631e71062b7bd058b3faab0`  
		Last Modified: Fri, 16 Jan 2026 05:33:26 GMT  
		Size: 3.6 MB (3613367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7df9a72d10446f51bf6f2ad7ea6f3b30523ac77067a2eef729971e3a94c4d9a`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; s390x

```console
$ docker pull spiped@sha256:138fe4dcc8fb5c0df1a9fe39769aa482f8103179104fb7822432be26d9dc06f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35962521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2d8e7d46dd49c524188f2706e57f1bf10de8a88227685ba47956a2187b9e35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:43:35 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 03:43:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 03:43:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:43:54 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 03:43:54 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 03:43:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:43:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:43:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cb804f8c11f523ce62a7bc09d236baf84abd6e284119dc6e7c812b046ba3ce`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8af71d5729ead8e60802ee40cd20b30288f02d50d14e682fc9af8c7a6aae22`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4467051214cb85c78e6cb79968f755a9833b4b38239855bb9eaca4f83bb5bd`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 6.1 MB (6121999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099202750066c7aa99797cb9282aa06e8187d7a87d111d1af849e70e955f5045`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd30b70482ee075552a0a8c1163f912098b4cfc94f09bb564d7846c8ae6ac9b`  
		Last Modified: Tue, 03 Feb 2026 03:44:06 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:00b19a2ff8b9daff2d46f3641d4e0f1be5d24395d4dfe12e381a836c8ac5e89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f5f17e17e5f54014ea830b208ced2160254e9afd41c57533a22f20ba746d9c`

```dockerfile
```

-	Layers:
	-	`sha256:edf825008cc03344fb619906e7e7ec2b9fc14fd95212f82320a2b93e91e1ade1`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 3.6 MB (3618587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3e88bd64df43446d50200b8b468c4d96319ccedeaec436cca1e26bfa1c2a59`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4-alpine`

```console
$ docker pull spiped@sha256:2e861202f057586ae2e6dc3a5290d61949120d861e272b5700c1e30e1ae9774c
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

### `spiped:1.6.4-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:45aa25e16b20aaf22415c03717dfbffb2460250d93ccfbf50d304296f0323560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c42c3ad8f87ea2a2987c07857dc357c5caa6eb7fe68f8ab758c81d2c67f6316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:36:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:36:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:36:57 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:36:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:36:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255f2b198269941f9011d88cebad6e20b25c8054b5ac4ebd1b07f9750a69d255`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed562f6049bf766f9af2aeb064224279b938162b44667a74bc7ca9c31ac1d70a`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d0ab7b6d45d1dbeebe557e32936e50678b9985769e6bd0ff3e1ff5e433e69`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 107.6 KB (107647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868415b885be47751e88ed3c97ca195abec55deffeb9f4ad2846ad3d25cdec28`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d8f030e4a64f48108d2120539708364c71dc39133649b15a0ad263ec9bfe40`  
		Last Modified: Wed, 28 Jan 2026 02:37:04 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:14bccfab21e7b3f36806b9521edfd711ef99c418ce1a38f2c913859e95caa2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0f387ff25d96b6eec2a5942d1be095ce8d2cd8945dadefd293a3706d31ea69`

```dockerfile
```

-	Layers:
	-	`sha256:3abca7ed4aae68f57768d18d39b5d6b1c58a733af4507188677241020e39e0d9`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6768ac276576d5f59511c63ded4afa12e2d77d28be7bffc6d1537d58bb57bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 14.3 KB (14259 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3840e207c5f175385b57ca037766c41623e4a780197b93760ca83297bd8e51ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07ce0978d45ec15bdc0a08bdc59ff908f2bd78005af85d4bbad7345be081ee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:44 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a5ad93e4f03c704fabcd2728cb1ab8244c96ef0876f3fcc9779085a8d3be96`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092107d3ff0fcf3229ae39acf729a354fda97b10c713e7073d550bb7c69025bc`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb00245db6ff8769dfa116d0e6194c8908449cd54b3995e5f0044b278d0fb45`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 89.2 KB (89154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3375ee92dad5bd59b0dde03ad45bdf7a8f7df3aaa1e2847b17cdd6734893cfb8`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc41431154f4cccb130328f9bda92ac3cd374c3bc4ef8b29827399ebd22bc749`  
		Last Modified: Wed, 28 Jan 2026 02:56:49 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:193c4ff5e06269d1446ab3235284aa43d244fdbc13dffdc98c715540fcc455e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060b8b064e4aba529d56ef354367ffae940f6b152b36f64ea427dfcd51e51f1e`

```dockerfile
```

-	Layers:
	-	`sha256:9257c6b08dae939c45fb6b5cd969064dde84328d15653df8b0ab98dae6b31d32`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 14.1 KB (14146 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:71592cfee4b071cad3b52c3cfdefddd8ff72e3d5e644d8859d2d8cec8397a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c48ddb927471eeb09c0d2e183b02bb1074d36b5caa9dbd3477ee935a8eed01f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:25 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:34 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ba379620ebeacb95d57ee5ff3ce395b9868fe9f8d00a5b85dd41df19b3a23`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471e6c87dbde5f46d8cd1e26b6a653a7d77209c851df54df0c065355b1c36749`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 8.0 KB (7952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917e2b19aaa32cc304579e079305131ee112e7015524177e84f33379315c24f6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 81.7 KB (81685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d229583db181996be822e85b4fe259ecd55350b04637a090977de317d8cb53`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283dd24da1a4b40bed9d28f9196f24341abf5ee8a13f180db2b3e6daa7e85b8d`  
		Last Modified: Wed, 28 Jan 2026 02:56:40 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b0d30665b0b25a584022937647a82e260a99dc3822f06eae03c777c08c589459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de7b9137b4705f6bfaa43d68be9ab47cda877656a88568a8b98eaecf834d723`

```dockerfile
```

-	Layers:
	-	`sha256:bf20f6c9425bc14bf83c368ad820cbac85037f9cfe9e8f428105dcae79aa5f0a`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c326467351e8aaa1070327395a8ce06feaf36e791288cc8d0efc059293853a6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:effcfa5e900325dc5a9f2ce725d32bb928170b9fae13c2414035f7c74db4832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129da21c1ac14cfe9747c51280fa104e3e2a4a7fb499fce9d2f79394c096e45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:37:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:37:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:37:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:37:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215f43d3f31692bff6dbb7a8464a9777ff146fd6817d85616dd79d628db9a4e`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a149826e8201bd60e39e8acb8c71ee749c537b2c783a541e04af7a7b3fc6b5d`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3816514d66f19e4e15afc0dae177ea8f1397bbaeba0189b4a33a3f265afbb21`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 100.6 KB (100615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f073eca19d0c28ea18c16d7aa1388a52393935ac0e76036549b53fca85d50741`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ae442366147b99273aabaaf180c7a0347dd957817ff21ec6495a8f374fd7b5`  
		Last Modified: Wed, 28 Jan 2026 02:38:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:20c426c97f5ccc77dcb4c2895905f7a3e9aedaf5bf12fbf4b3ff87748f7ebc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f74a0ff8267a4110c62ab6dcdcf2bf4949f9f54a7ff5e5b96a7e78b99f9770c`

```dockerfile
```

-	Layers:
	-	`sha256:ce7e8f74c44956e8b3a9213e0686a5007c77ddc5cd5210760e512537c99dcb4f`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5744a1e9a5178b40c2e43ceccdad37fa256e17fb5a7e73342aa361c38b071ea6`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; 386

```console
$ docker pull spiped@sha256:d29799b7499dd97718236dec910ca0fb21a58b93b04c13b9d32bd3972850d109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c829adab8d4ab1c5c9eef2ab8cd6fc3b09ac7a5b2c98b60eb750eaadcf3ca449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:31:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:31:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:31:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:31:32 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:31:32 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:31:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088b329d71531fcaf8b6b6b5fb05bd132488a9b146463fda72d73f3b193da77`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6327ced333146d36cce9bad13d15f14d00cfba342ef14347eb76323f377623`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f74692486d32e3c25efb4bcdbdd450b58db493d05a003140a026ba85c130a6`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 120.1 KB (120096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b377c56ed7e39aeec7320819a810cd8637819dc2c7f00e5f02f6008223d5ed8`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e023ec54765d4d3764e0855b6d7cfe0e2f9966db68bd933fe3f4fe6c41a2474f`  
		Last Modified: Wed, 28 Jan 2026 02:31:38 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:49494f0bf8ea2a9ac91bc338facd2f7cede025b28b7848656878d7ce0deadf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16387e224ee0b4762e3111436b2fdc3a8bfebe61d796cc65af094da1ebf76cd0`

```dockerfile
```

-	Layers:
	-	`sha256:bdc547d749394448a39cd679c285ba250424589df32f26c116cdc3bca37fedf9`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f968b5a19cf7dfb341a81ce64526ba67dbdecae7dbd82f7332ab1f24bf7e26a`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 14.2 KB (14223 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:ec49e51d1b31aef6ee4c32cbd2374c5115032febd535905c0146f19ca7d1b88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3856312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52e05f6841b2c0f9dcb913e52c349b3ec2747c75f53e9b3d6a41cd3c6103a9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:19 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:59:21 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:59:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:59:33 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:59:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:59:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52389dd33bb155b2c78fa5202c8c9909e97b12049d41f7cb5369100d2a7be819`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd5646a7c2ce724b02160a31080c85b3571ffddbc309ccb39fb23e5075d4aa`  
		Last Modified: Wed, 28 Jan 2026 03:59:47 GMT  
		Size: 8.0 KB (7956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d83f042b4cb936ae2f704768b0462b7f539ba799143799dc6a8ce0babc73884`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 112.7 KB (112673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f4a6884030927f7cdd451b10bba40c6cf61fd40534ca3a9cf653bb742ea8f`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fbfb80739dd4ce26eb065be080a75c602340f3242a297925caf40baf400db0`  
		Last Modified: Wed, 28 Jan 2026 03:59:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1d08517919e2dfe608c1e408886b7ef4659cd9f15bf49a67583fe931eb307650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68d34137d518c2381ecd841ecef0a23786265f08c1952e0ed2134cc2ba9073`

```dockerfile
```

-	Layers:
	-	`sha256:b57bb2bf93c55cd637df776032387ee2beae0039a87bacf4e588dd43aaa36711`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a73d72709b0315e9f657137bb6dbf7c0679131d8e10876ea8a1bb94e4201b4`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0e7e07e5944d0951da4949f8298cdccfa6ec9395c2d0ddf983aa7f40bf7807f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565f6907e5ae385b224d048c255c22407d6a59d79533da4912c486d4ee1360`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:56:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 29 Jan 2026 18:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 29 Jan 2026 18:58:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
VOLUME [/spiped]
# Thu, 29 Jan 2026 18:58:39 GMT
WORKDIR /spiped
# Thu, 29 Jan 2026 18:58:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 18:58:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:58:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85b2fc2b9bdc2a30eea3483d034231cba4cf794b774e9c668e43189f965204b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a35d458c7098a7c5f24f347a75cf6930f742a2e14ae40067defc23e63d57b5`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbbaf165e7e5cf59739b8e5317789f9a907da0dc26f3803ae533e05f7a2068e`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 98.9 KB (98867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0973003e6d2e757a9f14bfb9ab4d4b6be0abf8bbdfa7a9b699232646e0df6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509faeca8d8af4689f4b76d19f92f0deeb48d08e62ab656d5ad988fe97b48e9`  
		Last Modified: Thu, 29 Jan 2026 18:59:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45c5a2bccce0c2d968718cdc5b92e2d54486ce35d6f21169c8e2975138906721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3828726b576d70b513dac001f2810887cf67c235a77086291ebdeb6df7a249f`

```dockerfile
```

-	Layers:
	-	`sha256:53e8f0117ebdf17125860003417afad58a90f091d2b04b6763e9b4ce1899228b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0edfbeca58a13ce30fdd21ef302873aa05c28498d058231b777fe51653a06eb6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 14.3 KB (14304 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:0aeb96b9c7c968a0ad51a4c785e0c76534a115d395c587eacd587a3aad55b360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b72691935166b1882b3040950315ed19d9cf1a3678909a868fa5c27a1a58e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:05:48 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:05:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:05:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:05:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0789ee1817b07966cd80a07b05a82d8e0c9bf85f6053f4955ac4731e47448ad`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e526c5a7e2d6f02b24c7ed3860ec8221dcd7d0c6e4112d267da6729a13890448`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10bca7622d69f6335c554b1c8cec2a82753df66ed9cf072d635820439e1af3c`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.9 KB (96933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d81cea7ec993f5c76e72bd06b1579e878f6a4d1a4a2f11114f710747ef40d4`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086ab53d5ebb5741d97d120d1a1ad7797bf2fda46a7ff1f9a033efa0117cd233`  
		Last Modified: Wed, 28 Jan 2026 03:06:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32f5675d459d866b7c69b2159549861b770e81fa270485088e909f23c515b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76bce779a8727519c7fb65566c2ce929337d21a3d6addd2f301cd51f95516c4`

```dockerfile
```

-	Layers:
	-	`sha256:85780af5cccece93dbeac028f8517ebc14f3298ca69ddd75bcf80809c0ea3432`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797300601f0f43bd14d2b3e327c7100b2a1b8356e4290096f308e710af773718`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:2e861202f057586ae2e6dc3a5290d61949120d861e272b5700c1e30e1ae9774c
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

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:45aa25e16b20aaf22415c03717dfbffb2460250d93ccfbf50d304296f0323560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c42c3ad8f87ea2a2987c07857dc357c5caa6eb7fe68f8ab758c81d2c67f6316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:36:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:36:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:36:57 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:36:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:36:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255f2b198269941f9011d88cebad6e20b25c8054b5ac4ebd1b07f9750a69d255`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed562f6049bf766f9af2aeb064224279b938162b44667a74bc7ca9c31ac1d70a`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d0ab7b6d45d1dbeebe557e32936e50678b9985769e6bd0ff3e1ff5e433e69`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 107.6 KB (107647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868415b885be47751e88ed3c97ca195abec55deffeb9f4ad2846ad3d25cdec28`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d8f030e4a64f48108d2120539708364c71dc39133649b15a0ad263ec9bfe40`  
		Last Modified: Wed, 28 Jan 2026 02:37:04 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:14bccfab21e7b3f36806b9521edfd711ef99c418ce1a38f2c913859e95caa2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0f387ff25d96b6eec2a5942d1be095ce8d2cd8945dadefd293a3706d31ea69`

```dockerfile
```

-	Layers:
	-	`sha256:3abca7ed4aae68f57768d18d39b5d6b1c58a733af4507188677241020e39e0d9`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6768ac276576d5f59511c63ded4afa12e2d77d28be7bffc6d1537d58bb57bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 14.3 KB (14259 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3840e207c5f175385b57ca037766c41623e4a780197b93760ca83297bd8e51ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07ce0978d45ec15bdc0a08bdc59ff908f2bd78005af85d4bbad7345be081ee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:44 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a5ad93e4f03c704fabcd2728cb1ab8244c96ef0876f3fcc9779085a8d3be96`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092107d3ff0fcf3229ae39acf729a354fda97b10c713e7073d550bb7c69025bc`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb00245db6ff8769dfa116d0e6194c8908449cd54b3995e5f0044b278d0fb45`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 89.2 KB (89154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3375ee92dad5bd59b0dde03ad45bdf7a8f7df3aaa1e2847b17cdd6734893cfb8`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc41431154f4cccb130328f9bda92ac3cd374c3bc4ef8b29827399ebd22bc749`  
		Last Modified: Wed, 28 Jan 2026 02:56:49 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:193c4ff5e06269d1446ab3235284aa43d244fdbc13dffdc98c715540fcc455e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060b8b064e4aba529d56ef354367ffae940f6b152b36f64ea427dfcd51e51f1e`

```dockerfile
```

-	Layers:
	-	`sha256:9257c6b08dae939c45fb6b5cd969064dde84328d15653df8b0ab98dae6b31d32`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 14.1 KB (14146 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:71592cfee4b071cad3b52c3cfdefddd8ff72e3d5e644d8859d2d8cec8397a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c48ddb927471eeb09c0d2e183b02bb1074d36b5caa9dbd3477ee935a8eed01f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:25 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:34 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ba379620ebeacb95d57ee5ff3ce395b9868fe9f8d00a5b85dd41df19b3a23`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471e6c87dbde5f46d8cd1e26b6a653a7d77209c851df54df0c065355b1c36749`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 8.0 KB (7952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917e2b19aaa32cc304579e079305131ee112e7015524177e84f33379315c24f6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 81.7 KB (81685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d229583db181996be822e85b4fe259ecd55350b04637a090977de317d8cb53`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283dd24da1a4b40bed9d28f9196f24341abf5ee8a13f180db2b3e6daa7e85b8d`  
		Last Modified: Wed, 28 Jan 2026 02:56:40 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b0d30665b0b25a584022937647a82e260a99dc3822f06eae03c777c08c589459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de7b9137b4705f6bfaa43d68be9ab47cda877656a88568a8b98eaecf834d723`

```dockerfile
```

-	Layers:
	-	`sha256:bf20f6c9425bc14bf83c368ad820cbac85037f9cfe9e8f428105dcae79aa5f0a`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c326467351e8aaa1070327395a8ce06feaf36e791288cc8d0efc059293853a6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:effcfa5e900325dc5a9f2ce725d32bb928170b9fae13c2414035f7c74db4832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129da21c1ac14cfe9747c51280fa104e3e2a4a7fb499fce9d2f79394c096e45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:37:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:37:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:37:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:37:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215f43d3f31692bff6dbb7a8464a9777ff146fd6817d85616dd79d628db9a4e`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a149826e8201bd60e39e8acb8c71ee749c537b2c783a541e04af7a7b3fc6b5d`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3816514d66f19e4e15afc0dae177ea8f1397bbaeba0189b4a33a3f265afbb21`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 100.6 KB (100615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f073eca19d0c28ea18c16d7aa1388a52393935ac0e76036549b53fca85d50741`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ae442366147b99273aabaaf180c7a0347dd957817ff21ec6495a8f374fd7b5`  
		Last Modified: Wed, 28 Jan 2026 02:38:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:20c426c97f5ccc77dcb4c2895905f7a3e9aedaf5bf12fbf4b3ff87748f7ebc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f74a0ff8267a4110c62ab6dcdcf2bf4949f9f54a7ff5e5b96a7e78b99f9770c`

```dockerfile
```

-	Layers:
	-	`sha256:ce7e8f74c44956e8b3a9213e0686a5007c77ddc5cd5210760e512537c99dcb4f`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5744a1e9a5178b40c2e43ceccdad37fa256e17fb5a7e73342aa361c38b071ea6`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:d29799b7499dd97718236dec910ca0fb21a58b93b04c13b9d32bd3972850d109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c829adab8d4ab1c5c9eef2ab8cd6fc3b09ac7a5b2c98b60eb750eaadcf3ca449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:31:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:31:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:31:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:31:32 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:31:32 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:31:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088b329d71531fcaf8b6b6b5fb05bd132488a9b146463fda72d73f3b193da77`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6327ced333146d36cce9bad13d15f14d00cfba342ef14347eb76323f377623`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f74692486d32e3c25efb4bcdbdd450b58db493d05a003140a026ba85c130a6`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 120.1 KB (120096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b377c56ed7e39aeec7320819a810cd8637819dc2c7f00e5f02f6008223d5ed8`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e023ec54765d4d3764e0855b6d7cfe0e2f9966db68bd933fe3f4fe6c41a2474f`  
		Last Modified: Wed, 28 Jan 2026 02:31:38 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:49494f0bf8ea2a9ac91bc338facd2f7cede025b28b7848656878d7ce0deadf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16387e224ee0b4762e3111436b2fdc3a8bfebe61d796cc65af094da1ebf76cd0`

```dockerfile
```

-	Layers:
	-	`sha256:bdc547d749394448a39cd679c285ba250424589df32f26c116cdc3bca37fedf9`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f968b5a19cf7dfb341a81ce64526ba67dbdecae7dbd82f7332ab1f24bf7e26a`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 14.2 KB (14223 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:ec49e51d1b31aef6ee4c32cbd2374c5115032febd535905c0146f19ca7d1b88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3856312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52e05f6841b2c0f9dcb913e52c349b3ec2747c75f53e9b3d6a41cd3c6103a9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:19 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:59:21 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:59:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:59:33 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:59:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:59:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52389dd33bb155b2c78fa5202c8c9909e97b12049d41f7cb5369100d2a7be819`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd5646a7c2ce724b02160a31080c85b3571ffddbc309ccb39fb23e5075d4aa`  
		Last Modified: Wed, 28 Jan 2026 03:59:47 GMT  
		Size: 8.0 KB (7956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d83f042b4cb936ae2f704768b0462b7f539ba799143799dc6a8ce0babc73884`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 112.7 KB (112673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f4a6884030927f7cdd451b10bba40c6cf61fd40534ca3a9cf653bb742ea8f`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fbfb80739dd4ce26eb065be080a75c602340f3242a297925caf40baf400db0`  
		Last Modified: Wed, 28 Jan 2026 03:59:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1d08517919e2dfe608c1e408886b7ef4659cd9f15bf49a67583fe931eb307650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68d34137d518c2381ecd841ecef0a23786265f08c1952e0ed2134cc2ba9073`

```dockerfile
```

-	Layers:
	-	`sha256:b57bb2bf93c55cd637df776032387ee2beae0039a87bacf4e588dd43aaa36711`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a73d72709b0315e9f657137bb6dbf7c0679131d8e10876ea8a1bb94e4201b4`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0e7e07e5944d0951da4949f8298cdccfa6ec9395c2d0ddf983aa7f40bf7807f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565f6907e5ae385b224d048c255c22407d6a59d79533da4912c486d4ee1360`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:56:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 29 Jan 2026 18:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 29 Jan 2026 18:58:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
VOLUME [/spiped]
# Thu, 29 Jan 2026 18:58:39 GMT
WORKDIR /spiped
# Thu, 29 Jan 2026 18:58:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 18:58:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:58:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85b2fc2b9bdc2a30eea3483d034231cba4cf794b774e9c668e43189f965204b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a35d458c7098a7c5f24f347a75cf6930f742a2e14ae40067defc23e63d57b5`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbbaf165e7e5cf59739b8e5317789f9a907da0dc26f3803ae533e05f7a2068e`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 98.9 KB (98867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0973003e6d2e757a9f14bfb9ab4d4b6be0abf8bbdfa7a9b699232646e0df6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509faeca8d8af4689f4b76d19f92f0deeb48d08e62ab656d5ad988fe97b48e9`  
		Last Modified: Thu, 29 Jan 2026 18:59:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45c5a2bccce0c2d968718cdc5b92e2d54486ce35d6f21169c8e2975138906721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3828726b576d70b513dac001f2810887cf67c235a77086291ebdeb6df7a249f`

```dockerfile
```

-	Layers:
	-	`sha256:53e8f0117ebdf17125860003417afad58a90f091d2b04b6763e9b4ce1899228b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0edfbeca58a13ce30fdd21ef302873aa05c28498d058231b777fe51653a06eb6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 14.3 KB (14304 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:0aeb96b9c7c968a0ad51a4c785e0c76534a115d395c587eacd587a3aad55b360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b72691935166b1882b3040950315ed19d9cf1a3678909a868fa5c27a1a58e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:05:48 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:05:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:05:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:05:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0789ee1817b07966cd80a07b05a82d8e0c9bf85f6053f4955ac4731e47448ad`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e526c5a7e2d6f02b24c7ed3860ec8221dcd7d0c6e4112d267da6729a13890448`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10bca7622d69f6335c554b1c8cec2a82753df66ed9cf072d635820439e1af3c`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.9 KB (96933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d81cea7ec993f5c76e72bd06b1579e878f6a4d1a4a2f11114f710747ef40d4`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086ab53d5ebb5741d97d120d1a1ad7797bf2fda46a7ff1f9a033efa0117cd233`  
		Last Modified: Wed, 28 Jan 2026 03:06:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32f5675d459d866b7c69b2159549861b770e81fa270485088e909f23c515b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76bce779a8727519c7fb65566c2ce929337d21a3d6addd2f301cd51f95516c4`

```dockerfile
```

-	Layers:
	-	`sha256:85780af5cccece93dbeac028f8517ebc14f3298ca69ddd75bcf80809c0ea3432`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797300601f0f43bd14d2b3e327c7100b2a1b8356e4290096f308e710af773718`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:34315b961d97a51a2f75462b746fe8d36675f1cbc14efc584e59d4e3c7474a14
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

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:b3660acfa7a6a9cf97d1a5f93df3664e3e03bc08d910dab9b4b54848908a258b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36829177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3372948bef2f8d7c6739c6204657e83fb87886fcc88b375918094272e282f408`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:44:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 03:44:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:45:14 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 03:45:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:45:14 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 03:45:14 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 03:45:14 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:45:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:45:14 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a39244bed5ea8df7cb602a090dbbd3939b97f478baa139e3aee1e5a704e2b35`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da47b3153bf0722ec1767737c189949df5c1c3e97723a4c6ffc89122a2a7c01`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72580f5c19083374ba391bfc528f9b44e3a51afb6a5b0d02fa8c59031a9308c0`  
		Last Modified: Tue, 03 Feb 2026 03:45:22 GMT  
		Size: 7.0 MB (7048206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0796f5973461c160794337bb40af6d6be9d8c7d3428a09c11fa955977a71a917`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fd4947db4ca06e91365c991a661ce6626632bb16d6be6b537a14848c4d7d76`  
		Last Modified: Tue, 03 Feb 2026 03:45:22 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:4d99388c193bdf8e8b699d01999d00ec0d2fc5cec3fb4633ffa18667876463cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bf6c967fe6ef5c305d8f8959a6d36b766dc5469be7d5ae3df8a3a4f9a211bb`

```dockerfile
```

-	Layers:
	-	`sha256:2c79eebf592958937bd16a955ab368dedeb6e06b01a34f44731c86d401dbb187`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 3.6 MB (3626224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6fa59c781fe40cd4cc26e11b53f6e32ce1b7d83fb2002738ff56e280f8d5538`  
		Last Modified: Tue, 03 Feb 2026 03:45:21 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:109585037b63d0abc51efbf37b4ad70e0228247d1e55e0a08438e7e85170e5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33739445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1b9d15e0681349dc0e221452ca8fddaa88baa07b1d0eb939d71466ba91613b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:24:52 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 03:24:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:25:24 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 03:25:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:25:24 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 03:25:24 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 03:25:24 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:25:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b458a4c9218319872f47d5435f0cdfb3b09636dc7f888b37ef49cdb46c70c8`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbeba32ee56074d975540593173b1eb1cb2a55122d770171b03fb49a6514ef95`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 835.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae365a816bc4b9d002b6c4b8ea75585dfc0ead71e4e8a6101c6bb2607a1d5295`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 5.8 MB (5789512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d02d4e2cf01320108039dc28276d4db4f84f09a42b67451f3b8804fa23ab72`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cac25af4583ededf146f86babef7ebfc2aca84fa0f007d835968066eb646ae5`  
		Last Modified: Tue, 03 Feb 2026 03:25:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:29ab4d3ebb43cdf0bee03a52b5937b6ef650c1333d2867f16fb087504b8fd235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c144228fed63e13f70d75d8302e895c7f203f7c040da3ffd35c4197e34406ea9`

```dockerfile
```

-	Layers:
	-	`sha256:cd7f0f86f71184db69f10a9ec9de636883be6a73ece119da2f41fd9458bb3b2e`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 3.6 MB (3619218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636a639c9a36fc7e25753a33e119e0d643e972123002f04d0854abd6410661c9`  
		Last Modified: Tue, 03 Feb 2026 03:25:31 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:2db234f117df0f3bb6d6bdaf1c3c32fcc47310588ac51b92cafcfdaa2a495945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31800771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db8a26d24435640659c3cc86c7c12f64fa75e291a657a0083272899caab2112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:28:12 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 03:28:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 03:28:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:28:39 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 03:28:39 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 03:28:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:28:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:28:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0c6df2b95e059eb6b4a0862339f6ebceb74af147d2a41d012d8d060b5de415`  
		Last Modified: Tue, 03 Feb 2026 03:28:46 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0664940b3aae87aa58fc424fca71375278ce662985f954c7983028d752bafacc`  
		Last Modified: Tue, 03 Feb 2026 03:28:46 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e5a94203a10ff32000a8c0ebd03be7cb400d2fe21c3abdd898fa2154950d17`  
		Last Modified: Tue, 03 Feb 2026 03:28:47 GMT  
		Size: 5.6 MB (5584651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97237f1098ba03c1cd5077978ab4ce814a06a400a6638d16e23bebeaebf38ec`  
		Last Modified: Tue, 03 Feb 2026 03:28:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c10fbeab436bcf9758306ef8bd0b97e1af3dcb3da6591d0a7857810b57fe1b`  
		Last Modified: Tue, 03 Feb 2026 03:28:47 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:dbfe43d783cc81a3f9a6e036a235a7bd73805ff41a6801c4d2b2e470c3d58d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb29e7b1482a847481858e027aee1372bc60b2311b95628754b2f1b10ecaa33`

```dockerfile
```

-	Layers:
	-	`sha256:2ee5233df73b0c0ac70f36a5fcf4432cc9a1cbeb39b093abeeea90e80e5892b7`  
		Last Modified: Tue, 03 Feb 2026 03:28:47 GMT  
		Size: 3.6 MB (3618339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae58f5efea5807b4dbaddf41a8e713795b0d010c8edae28cd8065c2fcd2f0b73`  
		Last Modified: Tue, 03 Feb 2026 03:28:46 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0bdd0976e20f1acc9da2f7e2f38593dd3a50dcc087d5c187b4171f48ad3cc2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36375265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c49dcde0f9bab665574bee4cd9730d12851c7a1fe4d23b316dd9b10cee0b4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:43:36 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 02:43:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:01 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 02:44:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:44:01 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 02:44:01 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 02:44:01 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:44:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:44:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79064b13669c24767c630a07d76f9e042c468d7f40ca82f42d303bf2be4b2b10`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc46fd10114f43117c0ab2973feb788c02135531ddae05d59ae6d76879484557`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8922319902b1ebfe33f49b30b6ff2459d48ebe911999cbdb9925f498368110c2`  
		Last Modified: Tue, 03 Feb 2026 02:44:09 GMT  
		Size: 6.2 MB (6232826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f955d89d90ca6f1fdabd3019bfc4b670b2ee30029964553e30a5038cb814382`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae512a1d3f02e4268ff11ea8a34b88fd9b6ecd39a919636f6796577b91a221f`  
		Last Modified: Tue, 03 Feb 2026 02:44:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:62381220fa8be885003b494140a6a223d59366d095e22d07adc386816f5320ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8f7ad13ce93ec496896006709bbfada6506515b9aa7625421f99a8617cc37d`

```dockerfile
```

-	Layers:
	-	`sha256:5cc9d869283c2d37bc51695715d16b8714cc723f3e5f2dc0c071dfd6c129c085`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 3.6 MB (3621260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9e154fec71f9918fa0df235055eddf49f9d3dec0c19a8375e274e17fa0e0f94`  
		Last Modified: Tue, 03 Feb 2026 02:44:08 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:728d78d73281646241fcb222dd9d31839cc9aac1002495caf447df5a12ef920d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37738880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9564f7127f6b19ae5edc1b7f098e2b5b56ba26da5624f12f8584011789e48511`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:08 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 02:49:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:35 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 02:49:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:49:35 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 02:49:35 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 02:49:35 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:49:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02829238b73397f5db890306da7b1f20106c90b28ca1b84ba15b5c229988d41`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4c072969b7cd6ee6467a4a3a8f1dcb749e0dd44d587ed12aed46112cc3f7f5`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87a1e605addae0e4b7407519d3894921fb10c0ec0c56901cb897f7648f7e02f`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 6.4 MB (6442653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ab5f20c688ea298a203de76462564834f67c9ae32e08abe388568afc9601b4`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1228c6ab6d3ba9275ec1bdf95149ba0707aac1bc10e56a008e54869ed8c067e6`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:3f7115b5b9ffad8cf20373c0cedc384e1d578a3f8a7a76efdd1c411fa21c6e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4979b6c39719537a1a3389ce653676cba980691dabacf86bd9bf60de44411192`

```dockerfile
```

-	Layers:
	-	`sha256:fc748c2e8ded79871f86fca112978f029acdf4be424dc35223ea12e68eaccf66`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 3.6 MB (3620353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01f61cc4549486f16775e1a20ae99dc3952a5a48da9ac5400003ca5116c8bae`  
		Last Modified: Tue, 03 Feb 2026 02:49:42 GMT  
		Size: 14.9 KB (14945 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:00be49bc99e5b1b637212c605b1848e0b4df978cc1034499cfaea49b6cacb195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40442941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a74d36a815a80a1ee0731f7f9d410231c3f06cd8ffce9e56ec21426052cdbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:21:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 05:21:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:22:15 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 05:22:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 05:22:15 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 05:22:15 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 05:22:16 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 05:22:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 05:22:16 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54dfec51c06ef5546fc59a333f4b2a700322fc6c08919bf3a34ec2a5634f7b3`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb6ba71a55079b27d2707951a5de51bb2735b3c843e7de0603e966f576a4b42`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa10d34f820fe96de44722a9d2956fd2fffb6c97bfdedbe70eefe38c76f4e372`  
		Last Modified: Tue, 03 Feb 2026 05:22:31 GMT  
		Size: 6.8 MB (6840384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a84985e24e00269a3c8628e7ff0586606414c566bc3a545ceb82366fca76b2`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36df81ecd8796a18c1949857ba62294cf17fe04d7c01f5794facab1eed173ad0`  
		Last Modified: Tue, 03 Feb 2026 05:22:31 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:e34582c751fb4395383437efc5f2ec1e67212bcb14fbc6d710ccd948b6b76e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14889a1d30656cb6f7af02127fae886ef833336f77c621279f791307c5b87a66`

```dockerfile
```

-	Layers:
	-	`sha256:34553b7d1a70804c1f632c8f54460c9d539a26a9f51085d8abdbb770a45417b8`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 3.6 MB (3621961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef2dc18746c6c4784daccf3fb9a520974f92134b86634839540e539c353f9b8`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; riscv64

```console
$ docker pull spiped@sha256:c3726522ae3244f8e5fc4fff7b8f5caaa648c5af80dd1242df5b9b0203a50b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37632620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6901900fa0f28a8994f2a5c6167065703cea25c38b46e682c7aa85ebf4c50f8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 05:28:46 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 16 Jan 2026 05:29:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 05:32:13 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 16 Jan 2026 05:32:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 16 Jan 2026 05:32:13 GMT
VOLUME [/spiped]
# Fri, 16 Jan 2026 05:32:13 GMT
WORKDIR /spiped
# Fri, 16 Jan 2026 05:32:13 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 05:32:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 05:32:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0565826c8fe4b1dacce6d9e839c402d5f7f058df52502fb3afc9c1fe362273ab`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54f9b8a5d71461439339ce26a0c07c07fbc5a8f883874f06636ae124d4b6406`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e14934a15b1e232262f936875f5c3c3faf525c75fb01a98c1e77355c8d3879`  
		Last Modified: Fri, 16 Jan 2026 05:33:27 GMT  
		Size: 9.4 MB (9358574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcad698be725811e7e426b85f2dd52a1d1e7963a1d1977d99b6853d7b29d1d99`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492e62971c5bbebb5c3ac87efe8c5f00292840225c2295daf96e49886856bd0d`  
		Last Modified: Fri, 16 Jan 2026 05:33:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:20c580ff798af1e2f3b4ea4d32d2a4df3f8a4d6cf589acca184232c7eb9ff72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e539bf6b82092c6a4f98991afff364af3c7d9c9f618a72fdbf396b9090cbdd62`

```dockerfile
```

-	Layers:
	-	`sha256:468f7c87bf94fe22429b696b878ab697ecd32432c631e71062b7bd058b3faab0`  
		Last Modified: Fri, 16 Jan 2026 05:33:26 GMT  
		Size: 3.6 MB (3613367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7df9a72d10446f51bf6f2ad7ea6f3b30523ac77067a2eef729971e3a94c4d9a`  
		Last Modified: Fri, 16 Jan 2026 05:33:25 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:138fe4dcc8fb5c0df1a9fe39769aa482f8103179104fb7822432be26d9dc06f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35962521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2d8e7d46dd49c524188f2706e57f1bf10de8a88227685ba47956a2187b9e35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:43:35 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 03:43:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 03:43:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:43:54 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 03:43:54 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 03:43:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:43:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:43:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cb804f8c11f523ce62a7bc09d236baf84abd6e284119dc6e7c812b046ba3ce`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8af71d5729ead8e60802ee40cd20b30288f02d50d14e682fc9af8c7a6aae22`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4467051214cb85c78e6cb79968f755a9833b4b38239855bb9eaca4f83bb5bd`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 6.1 MB (6121999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099202750066c7aa99797cb9282aa06e8187d7a87d111d1af849e70e955f5045`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd30b70482ee075552a0a8c1163f912098b4cfc94f09bb564d7846c8ae6ac9b`  
		Last Modified: Tue, 03 Feb 2026 03:44:06 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:00b19a2ff8b9daff2d46f3641d4e0f1be5d24395d4dfe12e381a836c8ac5e89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f5f17e17e5f54014ea830b208ced2160254e9afd41c57533a22f20ba746d9c`

```dockerfile
```

-	Layers:
	-	`sha256:edf825008cc03344fb619906e7e7ec2b9fc14fd95212f82320a2b93e91e1ade1`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 3.6 MB (3618587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3e88bd64df43446d50200b8b468c4d96319ccedeaec436cca1e26bfa1c2a59`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json
