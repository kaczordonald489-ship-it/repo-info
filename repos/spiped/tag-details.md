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
$ docker pull spiped@sha256:14ac6360e8a5cc0681580eac1d35bd5a3e4ddc9ed298399e1fcd782738f1baff
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
$ docker pull spiped@sha256:71455e5f7b6d93aae95424129833776689d2cc74f24675f33f11ef10e6f23ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36827283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ede578b23de9ed50043b1c78c384603da62a3b7df444af4e2148f0ff7266201`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:05:43 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 05:05:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:06:09 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 05:06:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 05:06:09 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 05:06:09 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 05:06:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:06:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e801c735c8ed3e544c7e5ec21fdadcb62e4f17e393072bc529855d7c3ae6e6e3`  
		Last Modified: Tue, 18 Nov 2025 05:06:21 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62b3c0fd7b0226ff6077d6b86bbb98a9632fc381cdf3917cf3e1c2f3fb915b9`  
		Last Modified: Tue, 18 Nov 2025 05:06:21 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf671102a10bab89ec80e76bc081b60c8db003c182c52b6e8749c8a00c3bc30`  
		Last Modified: Tue, 18 Nov 2025 05:06:22 GMT  
		Size: 7.0 MB (7048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ffc5a597d5117a8c3287526d416f057a71493f8bedac7a8e932ca15fa08879`  
		Last Modified: Tue, 18 Nov 2025 05:06:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c216a1dbbce2a0979e20d22a121252fde68d545aa23d1a63e9fa1d0c1db1aa53`  
		Last Modified: Tue, 18 Nov 2025 05:06:22 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:09e9e14162507839346b641426b8f6e1d553bb6078045280c57c1e104a75609c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701a082ef72b657e38c5604e48c263523b8f7b7fa5d78baf9e8ff64d708c3cc3`

```dockerfile
```

-	Layers:
	-	`sha256:fca3db4d709b67d3eeea80bb0284b7c014f40447b56781ee5d2f76f709fd4731`  
		Last Modified: Tue, 18 Nov 2025 08:05:17 GMT  
		Size: 3.6 MB (3626126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a54777a6f2567357088e3edbe62f36d27179125f9de343fda2c159e13e6507a9`  
		Last Modified: Tue, 18 Nov 2025 08:05:18 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:426a7b4ca8678d05e601961162fe4882cec8306e061a2a0ef28e5a4c185e6f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33735923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10f6e5284bc9be0c9fac9071ed5b283aba4e14d014ee6d22cc9577c0245ea88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:25:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 03:25:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:25:47 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 03:25:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:25:47 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 03:25:47 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 03:25:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:25:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19fa3fdca9ccb78808adc904f1814dd017d243bc5c179b0184c715efee222be`  
		Last Modified: Tue, 18 Nov 2025 03:26:00 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcab93afc62cae522725518ebc636cb915e984509d2388ef161ec154a31871d`  
		Last Modified: Tue, 18 Nov 2025 03:26:00 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b355f0770e6bdb66cfcde4ec30ce6a64c64aceb80958f3f48ebaee839ebdf4a`  
		Last Modified: Tue, 18 Nov 2025 03:26:01 GMT  
		Size: 5.8 MB (5789403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c31ee5d96793c7ab7dfb0f7c297aa1fdf92f4dfafc7100f5ac826de7f77bcf`  
		Last Modified: Tue, 18 Nov 2025 03:26:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c62d3d9536df883ab32c9923d67ce50b87b7e9d54f24c3d9927df9a4d7ddd8`  
		Last Modified: Tue, 18 Nov 2025 03:26:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:63bcd50ec3d14a45a2622b1289292f044900493251741ad97a3826b02db799f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a41f8c68e813123499d266c105fe6688bd6bcf8f237ad01c607367081e8516d`

```dockerfile
```

-	Layers:
	-	`sha256:95c1b6d653d55c72f719d0d09ae969adc36a878dbb3f973015cb26e24ec47903`  
		Last Modified: Tue, 18 Nov 2025 05:05:42 GMT  
		Size: 3.6 MB (3619120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d337c054c04289865a82162a0b6c7329d66ce9691d8bc79d7317489e0c00da0`  
		Last Modified: Tue, 18 Nov 2025 05:05:43 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e9235510be401662fdf9dc150727d52c180223c03f705dd62a4748d9c641ec77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31797132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcf78acee4c0ddc840c2c11a73f8024cb2182d36c20c420e53f35655e2baa6b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:50:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 03:50:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:50:29 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 03:50:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:50:29 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 03:50:29 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 03:50:29 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:50:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:50:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c2cce7df782c8ffa98b09b5026801fd75852fbcc542adda17f2cf674e45181`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422558407904c55bd813e2874a4f66dbfa77cf5efd6db4ed74e52303b441fd29`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fde1d67328042aa04d86b94a193406c1202f0b3541d1c95e7ecc18665ec645`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 5.6 MB (5584802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d6aec61101ef5fb65ec8aa6c4a388c95a5c739b4cae742d9f325477eee3143`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf79b5edc379842c06ef54040d0ded6b238383a6bb48036d8c47a64ab6448096`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:b7b3eab355c7919d43eddafd5cd7c953037bca700170b3c7db17cac1d4581d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be853f3e5bf6bd636b07d5fb91dbb5fb3ba07feaff4963e2ffc605c15e6eb836`

```dockerfile
```

-	Layers:
	-	`sha256:6102950244e9d1ff5d896169fd9854a475d74013ac69c10c65ef6fa2a7790929`  
		Last Modified: Tue, 18 Nov 2025 05:05:47 GMT  
		Size: 3.6 MB (3618241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89d6945e35f196e6b467782a87d7058b1b71566296fc00d94d16329ebc11706`  
		Last Modified: Tue, 18 Nov 2025 05:05:48 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:591fd9434499864d8c1158d89fce00904f6e06d5f392d8262b8c0d7efe39a889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36373157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d242e4657c201f08d46371f334bef5a4a2cfd1eb25ee0a73c00a8e00ac11c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:16:33 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 03:16:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:16:58 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 03:16:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:16:58 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 03:16:58 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 03:16:58 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:16:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:16:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba947a8faede3668130b9a9844eb382708be72367360c131942ce30e890f69c0`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096566cbdfead671dd335e66add44869360797178bf789ed21020aca50249756`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770ec9847c8da429b5188dce7cfaf6ac4b91c4582b3daf192ec92ce2d0299d39`  
		Last Modified: Tue, 18 Nov 2025 03:17:17 GMT  
		Size: 6.2 MB (6232178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d361a094ee90fb336f01e4261818ea22ad6cbc3e39fcce6cb5515b43368904`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524f95e648c0618b5d3b38bdc5cebea65cd4a987dad6fe870e1c305b7207e056`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:de69fcb855bd36d7eaa9a4ecfd53eff2bc04325b0e445720719ed66200cd6c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b52e32c61f8b7849ff947d47141644644953fe7b4d630ee19f40f1748cd66e7`

```dockerfile
```

-	Layers:
	-	`sha256:e3050659ccb70e389b03aa9e8d57539e7786ce53a093f045530af7adae8420da`  
		Last Modified: Tue, 18 Nov 2025 05:05:52 GMT  
		Size: 3.6 MB (3621162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a15fce2cffa58340c6b086eca26c3afabf400aded7333fa7f1c729656d8a9d4d`  
		Last Modified: Tue, 18 Nov 2025 05:05:53 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:23467bd729a8745214c4b47148d1e1dc68c54a8dc6f5f30d56700dd1da4c2aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37737826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b78410d027a00d586d005faef3d9ff264953f988d103bd949a43bfd4926e41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:55:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 02:55:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:55:32 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 02:55:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 02:55:32 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 02:55:32 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 02:55:32 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:55:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:55:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e080cdd1c9f6aad444c1d45fad2abef1c289e41be4b0b209145cba950a2d1759`  
		Last Modified: Tue, 18 Nov 2025 02:55:47 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fdec3d410a5b0ba820cf2f8ac384a67d232c8b7310aebeff1969941baf76d7`  
		Last Modified: Tue, 18 Nov 2025 02:55:46 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f6c7b2758bf989a21f93bfd024042bb2f176e19736daf32ab03cd3ba82dfe5`  
		Last Modified: Tue, 18 Nov 2025 02:55:46 GMT  
		Size: 6.4 MB (6442390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad5965c68a8d870fd340c771fcd0a822fa69e20665680f3039ba7b5756b5e92`  
		Last Modified: Tue, 18 Nov 2025 02:55:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aecb0f69473c2cc21216ed84c0d6d97b09b06e4110d3ea920870a95a00dc818`  
		Last Modified: Tue, 18 Nov 2025 02:55:46 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:89c3d55f090feb68455bd160a8c266cac5a849c39289fd7149847c0181d249ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1703098239e0a9df934e917a5c529ca1c413e2d3fb88b91f5941dec211bdcf8`

```dockerfile
```

-	Layers:
	-	`sha256:ee5bfd23df5e05f29413baba8619cc9e1a1770cea921068409bf0312e61351f9`  
		Last Modified: Tue, 18 Nov 2025 05:05:56 GMT  
		Size: 3.6 MB (3620255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7197602a5065e42953129b118d4095d83e4e031c50f2a67b79f800e9f23560f9`  
		Last Modified: Tue, 18 Nov 2025 05:05:57 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:f9d387a803cfdd1985be0085b60de474124c1fc4131c42d948af42ce3d1759a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40439568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a498e2f8e9c00da85debf16c2073bab51c2c9c0b653433b60f9fc513844e047a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 16:44:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 16:44:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 16:46:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 16:46:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 16:46:07 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 16:46:08 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 16:46:08 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 16:46:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 16:46:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ffe02bc5e011d9cb893ac7ecba601951db86c3c857770e41c5d43a375f8dc`  
		Last Modified: Tue, 18 Nov 2025 16:46:29 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30cf6ef4f4a65c31760e988a5e30d9051d0527712a0e99804a8a5b0bf18cde0`  
		Last Modified: Tue, 18 Nov 2025 16:46:29 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d358c24c19ff6d1e35bbd7a807ef937d4fad4ad9eec488f7e55242059f3e56`  
		Last Modified: Tue, 18 Nov 2025 16:46:30 GMT  
		Size: 6.8 MB (6840337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdd1994aaf0ebbf11da5c4ea4079110c42903e9c55fc736d0715dd2520f4a1d`  
		Last Modified: Tue, 18 Nov 2025 16:46:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef167886b835c0bad9761aaad863c77b11f1e68a30eaa1da5bd0f60046c501b8`  
		Last Modified: Tue, 18 Nov 2025 16:46:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:ce5eced8b97263e3d4500f5786fbf71960c445cd50ad00ef6c40caec7b4e269d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50da01383f3afc5380b2a08f818385dd40286fad66e9f0b21cb3163eba38de6`

```dockerfile
```

-	Layers:
	-	`sha256:4118ca48356c09b8c0b5e6e18d5c8e335596d648c22a32941a0c602926107479`  
		Last Modified: Tue, 18 Nov 2025 20:05:03 GMT  
		Size: 3.6 MB (3621863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf6d27b90bd496865de3bbc67e759074e3fbbbb4c1d8067f8b47ac14fd450fb`  
		Last Modified: Tue, 18 Nov 2025 20:05:04 GMT  
		Size: 15.0 KB (15028 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; riscv64

```console
$ docker pull spiped@sha256:959ca9b18f8621408db5465afde15c6950d3c775a4b30b7afcbbecebe2c13da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37633874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6569fae25137810bd7151d5788496634850dbf582ed479ba779d2f76c148264a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:22:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 19 Nov 2025 19:23:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 19:26:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 19 Nov 2025 19:26:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 19 Nov 2025 19:26:22 GMT
VOLUME [/spiped]
# Wed, 19 Nov 2025 19:26:22 GMT
WORKDIR /spiped
# Wed, 19 Nov 2025 19:26:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 19 Nov 2025 19:26:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Nov 2025 19:26:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d95c0473e2a3ebd4bb8143470f2c4574e809b688d0a73464613a79cebd8c5f`  
		Last Modified: Wed, 19 Nov 2025 19:27:53 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa754d41483b1cdfee7949eeb674d5dbf834f7436ffec40fb1450db638145de5`  
		Last Modified: Wed, 19 Nov 2025 19:27:53 GMT  
		Size: 820.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3692d569c1db6381f3be1989acf3ecde5ca830214a2d215cde5dd31675d2749c`  
		Last Modified: Wed, 19 Nov 2025 19:27:54 GMT  
		Size: 9.4 MB (9358381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32fd578990cfe31e14f8792a3e597ae02f3d352751be338bebcb7cd6e0b1c74`  
		Last Modified: Wed, 19 Nov 2025 19:27:53 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98f8f5e6a20cabd1e5b017f926e971a243a4f3a1a77bf31df8c75b0ddb7ea10`  
		Last Modified: Wed, 19 Nov 2025 19:27:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:50fec440ac1cd513e81f4ca03fdcecf5f2054e293af66362f154bf705b89876f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5177bbce1bb2f0302d87f2b11fbe5d8db563bcb4796bd8fe8db26cf53ea0f3ae`

```dockerfile
```

-	Layers:
	-	`sha256:8e66ff47ad83b988d6f182d9f81c66275ad954f7ec9deb15d983342bfc9edd22`  
		Last Modified: Wed, 19 Nov 2025 23:04:44 GMT  
		Size: 3.6 MB (3613269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9faa99ec8424007503d60c406ef512e9259c10b056d1a123b6ee4b2ad8c6f807`  
		Last Modified: Wed, 19 Nov 2025 23:04:45 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:0cc161584fd80bfa10ff2782bfcfa1c4be74a02047ba26409d0389e8f2e14240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35957952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6305c3b1ea8d0e6c559e141387c419530d60f59572ad26ce258790dc913ffd1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:01:37 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 04:01:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 04:01:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 04:01:54 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 04:01:54 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 04:01:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:01:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:01:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a9f8204c54a671034d8c9e635eef8807f29cb90649065a9ba5e66bed4acfbf`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda0974bd23cf2a73bb4f152623809d2fc8e734905a457114c9c03ca36a01144`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d727647b8da22b57df503f6765a7797eee413482299726be8d98cbdf2270b3`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 6.1 MB (6121210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50b0de3d190c1cc7a6dc935b91e017801f2b3e5df36dcbe0d9e09ed2f763d8b`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8006a7de8a5327bf044f7f4e3e2e62d600c335b9245de92a76e57cefc083159e`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:ead10e78092e259d73cef02c88d71b85a73429c3b8303d3dbab7b84f5b018218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1542f64d650d2fcd16668e14181f913919f85779f78af5d2dcb2dd5a04a5229`

```dockerfile
```

-	Layers:
	-	`sha256:a3101f855d36ca311ded5b1214062b9109c30cfe662a7936b96eda160aaa8843`  
		Last Modified: Tue, 18 Nov 2025 05:06:07 GMT  
		Size: 3.6 MB (3618489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ed9bffb5ad34ddcb7b0cf4d59648545bb7eec8d096db3e28ef312d2c3f72b76`  
		Last Modified: Tue, 18 Nov 2025 05:06:08 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:7b9625a81e8db9045c4eaf8f9bf40b8ef8c78a666bb7201d8d7c80538a418f7a
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
$ docker pull spiped@sha256:7d011e9e579768cd749e2df95806a3b739ebbdd516385dac92f2e9cda3570e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9d66303cac034d8960b8128b5967170028d350ecf6e131c4bf30b000a3f836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c041bc04e274276fc6a842ca20a0cf973af7c178bcfb6575c0d8203718fc91`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f81b6f5c689713065e6b968619711a3bd698fd708594cc90dae3977d54ca24e`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a035501670b01c25e6d7ce231bae87ef493bb668e877be52618f03679b673c4f`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 107.6 KB (107645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f81362a47a6b65eaf0da33a0c61df7c9a874d76861e5ae8fa0bc16547593db`  
		Last Modified: Wed, 08 Oct 2025 22:58:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ae81c7faaf7b0d0454b9d217085e8da2f5e5a72ead2527e67506b0d4834801`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ed8b2f715fbc09ab5fcc75433e022573fd8e46bded0d7dd791180a01b3d4a8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b323748eb9cefd40fcfe67d6c7dd561a4f5c4498457b7739b98161ea53a531c`

```dockerfile
```

-	Layers:
	-	`sha256:64366b1f73c30d49b216afd6a2acb0a27ad6d69bbaf554934ef1fb5a1b8ae379`  
		Last Modified: Thu, 09 Oct 2025 01:04:34 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d77f4db066b7ca49f19231acfa8a9f30749e3884bc787f4fcb01d3cb8a54b848`  
		Last Modified: Thu, 09 Oct 2025 01:04:35 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:07f6c1ec4d9a40087ba1fabf98ca259b39af58fe0aa3d1b5aff7a5c9c85aab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66830d62439293e746c3d4171b26eb7b060853f622562e26647e13254243d153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153e87cee3c8273a66e75e0a084e6876c74329042a77778cc75c7865eafb5817`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e054efed96e629a0c9a72dadd2a8d348aa66730afa5f59ce6e02a530b64b8d73`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dbbcac13a86093cd5821deda5686d525abf33f1ffacea149ae0a0b642a332f`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 89.2 KB (89158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6448f1d44fa11364cf66800119dd7e5e05fc9b9d8384cce8cc858006c0684aae`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fa931b05c23aa0b5927c5fc4bea0d9aa65908b7ac3e936a5a5888060a49337`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e083a00e19dd556e9a671f1709ffc708a0ab8d2a7373856218a44de2df24d462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47da3cb18e03a2142fd48220b0903336c0d8a799d804ac3b38780211559ba36`

```dockerfile
```

-	Layers:
	-	`sha256:069680ffcf03350d43ef8d45bcb21dafd37c1132acdfce2d83391a239a85d47e`  
		Last Modified: Thu, 09 Oct 2025 01:04:38 GMT  
		Size: 14.2 KB (14190 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:742d7ee47c94e03887525e682c2614d90b9b1f43f674ce4407bcf06b787caa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3312569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db7cd0fffd0a4f2c540dfe37e4c940cf5c7595aeffea1bf7acc4b1793c73d9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a85ed9579bf45ac1db2ef56f4067b84fe0c4d8e51e006ec1d925eb0c32bf22`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85621545c13dee2ff1d8660f7847266105703d040c19d1816e374881a3bdf6e`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8afad049c072c9b6d3ed2946f7d0c0782835979f90696b68ac6e4c0efff5bf4`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 81.7 KB (81688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35464221f20a70de628e3018e70c13c2e8ed9970a791049f1ba3bae429355536`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d6fea506e0050596918141446ad53da32b5b3a4fc9c7a5d497caf9a7ec6390`  
		Last Modified: Wed, 08 Oct 2025 22:10:18 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1db53d701cc5320b98ed95f8e8288e9c84ddb8ad31b517b42fe2faa626874b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f53816c0890232fc85b4017c83eabcfb11884aeab001b608b66e2a8c9e183e3`

```dockerfile
```

-	Layers:
	-	`sha256:f33fdb1fd07f91c527d8c950dcb81f1eea51882f51d66c0f4da88547240c6499`  
		Last Modified: Thu, 09 Oct 2025 01:04:42 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a9fe69db1d74bfbe4aa6a07c0fb4e0e59f4eff9e1636b7e0c486b6435b788b`  
		Last Modified: Thu, 09 Oct 2025 01:04:42 GMT  
		Size: 14.4 KB (14405 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1c2f38931ee0ff681a7c140bbc874fa1ff5837de4baf9a50a3498fbcb12a9668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b0a53163c15fa0112f2865ee8a52cbed044f04fc7001f7bd1f5e407cd57237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94547f3886a10ef8162a5d7fe9f4308e302dcfd48f5be2db3b1e5d4b5156d815`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ee5fd6e341869b5bcb70e517a1466b54c5191790816dd7956a41164690328b`  
		Last Modified: Wed, 08 Oct 2025 22:29:32 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba2ed7625e00fce702c1adbf90233532e0e4e98935a777f6bdffa076b1c3be2`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 100.6 KB (100621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1612c8ef14c84a7450d3ced7f152a93e533ffbb92d525fae7dde4c2988e230d7`  
		Last Modified: Wed, 08 Oct 2025 22:29:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433ac69ec6618a756cde4ab30a4488c3f0f7b89df240ede5a7b0a29d66250444`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f599a056737cf26e2f1e5bfb25bf8cf6f92cea0ea27b040de42b2e4bf139168f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1c665f9e5776de9d503dbefb3dccddb1d230d81716f5b086b02065d6f512d0`

```dockerfile
```

-	Layers:
	-	`sha256:8c6690f0ed02188be28287964aecbd171476e7e9484ec40d030c20c7b0e182c3`  
		Last Modified: Thu, 09 Oct 2025 01:04:46 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde4ac6f12c825868630b75c268c91338db29a424c87e551c1153694da325c83`  
		Last Modified: Thu, 09 Oct 2025 01:04:46 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac72ab4f716c2dabdad650618a34deccd477e31f604bf27a1f630a7a8433d994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf996beac99b6a5d8eae08ab4703a9cc11bccf3cb429e61a25bebf2947e4b519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664f8e36f37724daee2260066812a0de8999a28949591daef235c15d49ca301a`  
		Last Modified: Wed, 08 Oct 2025 22:22:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee281d18609c0bc414db88c7d17dd26aca0857610126d3e6d974952f5a414ab`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e8cb95edb963d4e91f7f5ea1c0881091c485846b9df554d3c11102b6a6a753`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 120.1 KB (120110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473aab810bb857acc1c39fc855966c0a2de5edd8a71287cf2183cea8dc6fdc4b`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1968cadac684d87fbcd83e1d646d178ae33c9242a480ddbd04f8fdf77b5e2ed`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2e9fe75d8ecfc557edbdaa8476f159fdb286886f6212788ecb61cda153b3ee2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e13e74ee61a3719d708f5b8486f092d523816b5c47e960b60b25a5d76b1aaee`

```dockerfile
```

-	Layers:
	-	`sha256:565649aba2f7ebad36d4ce1a64e495876030406355bb0f7a99f41f82b8300791`  
		Last Modified: Thu, 09 Oct 2025 01:04:50 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf1923abaf687d0c1af4d1718e1e365a3359dbf3e5ff8c339291f60bb0fc220`  
		Last Modified: Thu, 09 Oct 2025 01:04:51 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:506cee7907557b7efa054dc1a4c3261e8956700c9f553e9eb8d9a3470a368431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3854263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca7a1787271596d011a96a2b5632780587dd9653d8b0410f93093e13ecb8fcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf524fa67a04db3aef99fc4ab2113633c6c1965d0f890616009377904a6284`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9d95b7526b98e836dea8e7e9792130d0d6d71b1d6259e6f954ddffc64f5cc`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011805850ee2924d217a7651762c507b895c90911b4151207fe8e82e4388fcce`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 112.7 KB (112682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcef441d2768884d48fcb3b73e59f27e5fe6fc1cb5484df89fd3db0df4ce9437`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03005fd392da3ad1cd46c719335ac18f079118e761584617fe8c73405301647d`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:55eac1eb38ff8ce12fb98d86fb70542b4620b4c59ff746effba30530ad8676de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a3d2f7338bf8715707424b7b716c4498d4c3b844d2dc7387da9a1c64357879`

```dockerfile
```

-	Layers:
	-	`sha256:e3e6cde5a2631b7b9b782bb7fdfcf5de409ca1736416d9573c8888daf799d9e0`  
		Last Modified: Thu, 09 Oct 2025 07:04:30 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9220e8aff0f38f3e237e21c128db8adfad10ae35fb9db4dc56ead1ff1235e9d`  
		Last Modified: Thu, 09 Oct 2025 07:04:31 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0f378090b0e02992217f4f2a73d59cfb8c76cf62d83fec92991b3a8b1f0bfcc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a7d261c52ce9f797be48d32c37a2c3f66b54a18d3599dd071fefa04e588df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c352072eefdbb94e63d3787f16fac871ba719ed362861b9e97b581edd60548`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaa05a9bc37f5bb35d75064bac3af035a1d3a82ac079befd8019359672cc322`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51a4b112c1b7e8d19565628602648b41c69109d0f16548d16e781b095481e4d`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 98.9 KB (98862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971a3bdcb8df001e3163788a7484aea74c6bf79af7ec5c42ae330638a863112`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e689628a891ec93dec38687edd123814871319bfb552253a1ab8608d94fa74`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ef79fccc5586c74ed7a097a019247ca0f6644364c4e1b931202ce2f00cf4e38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c35fd6859715e249d4b311ca37e3e8e7886a7ce1788f0688877545e1f0fb2b`

```dockerfile
```

-	Layers:
	-	`sha256:624da72bc5bd15d76a69efe794516160d8151dc3f9b207f42a5b8b5165948a76`  
		Last Modified: Fri, 10 Oct 2025 22:04:34 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83fb34ab49138178f6f97cf97ae672fc5e173707dec2895a8d5b36f2e7689a5`  
		Last Modified: Fri, 10 Oct 2025 22:04:35 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:be3e9a57eb9caa9fb853c68e3efdc680d9d441f399d676b7a437f56a46d71b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3755528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eee68dd7eaa10392bbfe4c42a39adf582bc976bf97937637b807540ed7960af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eca97998e3d4f083ea39c1b7e9bd8d771aaa888745b8a60d6baff87ab6f8f37`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae19bb237945d6597aced8fc4cd16e5d4f06869978f4f6eb5d90a8bc9be7f39`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 8.0 KB (7957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce433dda6c532473e5da602686ec5186ad28c43789f172a14efc1cd9e38093d`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 96.9 KB (96944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867b81ca187d86754818499befad84648bb33d900aa6c797f74f14d7f06589dd`  
		Last Modified: Thu, 09 Oct 2025 02:26:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de821656be3d9d0eadaa8bfe8c17052ce64308ac54b60bb962a59498810f549e`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:daeef3e785369b94f4c3fec6e7b468c0aa8bcc71748eb82a5dcb98744d0c094a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff814477e4912c3dbc0dc6c3b2d236588fe065252c86c9a2ed142e200619a8a`

```dockerfile
```

-	Layers:
	-	`sha256:3ccf297cff7eee80cdb3e7128fdeabdb48c58df324a049928273000e72eba72d`  
		Last Modified: Thu, 09 Oct 2025 04:04:35 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfca2be336420edbf2af734bab83d3864c289d0e61390ac2cfc5f6d7f183847`  
		Last Modified: Thu, 09 Oct 2025 04:04:36 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:14ac6360e8a5cc0681580eac1d35bd5a3e4ddc9ed298399e1fcd782738f1baff
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
$ docker pull spiped@sha256:71455e5f7b6d93aae95424129833776689d2cc74f24675f33f11ef10e6f23ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36827283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ede578b23de9ed50043b1c78c384603da62a3b7df444af4e2148f0ff7266201`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:05:43 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 05:05:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:06:09 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 05:06:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 05:06:09 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 05:06:09 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 05:06:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:06:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e801c735c8ed3e544c7e5ec21fdadcb62e4f17e393072bc529855d7c3ae6e6e3`  
		Last Modified: Tue, 18 Nov 2025 05:06:21 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62b3c0fd7b0226ff6077d6b86bbb98a9632fc381cdf3917cf3e1c2f3fb915b9`  
		Last Modified: Tue, 18 Nov 2025 05:06:21 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf671102a10bab89ec80e76bc081b60c8db003c182c52b6e8749c8a00c3bc30`  
		Last Modified: Tue, 18 Nov 2025 05:06:22 GMT  
		Size: 7.0 MB (7048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ffc5a597d5117a8c3287526d416f057a71493f8bedac7a8e932ca15fa08879`  
		Last Modified: Tue, 18 Nov 2025 05:06:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c216a1dbbce2a0979e20d22a121252fde68d545aa23d1a63e9fa1d0c1db1aa53`  
		Last Modified: Tue, 18 Nov 2025 05:06:22 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:09e9e14162507839346b641426b8f6e1d553bb6078045280c57c1e104a75609c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701a082ef72b657e38c5604e48c263523b8f7b7fa5d78baf9e8ff64d708c3cc3`

```dockerfile
```

-	Layers:
	-	`sha256:fca3db4d709b67d3eeea80bb0284b7c014f40447b56781ee5d2f76f709fd4731`  
		Last Modified: Tue, 18 Nov 2025 08:05:17 GMT  
		Size: 3.6 MB (3626126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a54777a6f2567357088e3edbe62f36d27179125f9de343fda2c159e13e6507a9`  
		Last Modified: Tue, 18 Nov 2025 08:05:18 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:426a7b4ca8678d05e601961162fe4882cec8306e061a2a0ef28e5a4c185e6f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33735923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10f6e5284bc9be0c9fac9071ed5b283aba4e14d014ee6d22cc9577c0245ea88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:25:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 03:25:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:25:47 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 03:25:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:25:47 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 03:25:47 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 03:25:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:25:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19fa3fdca9ccb78808adc904f1814dd017d243bc5c179b0184c715efee222be`  
		Last Modified: Tue, 18 Nov 2025 03:26:00 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcab93afc62cae522725518ebc636cb915e984509d2388ef161ec154a31871d`  
		Last Modified: Tue, 18 Nov 2025 03:26:00 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b355f0770e6bdb66cfcde4ec30ce6a64c64aceb80958f3f48ebaee839ebdf4a`  
		Last Modified: Tue, 18 Nov 2025 03:26:01 GMT  
		Size: 5.8 MB (5789403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c31ee5d96793c7ab7dfb0f7c297aa1fdf92f4dfafc7100f5ac826de7f77bcf`  
		Last Modified: Tue, 18 Nov 2025 03:26:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c62d3d9536df883ab32c9923d67ce50b87b7e9d54f24c3d9927df9a4d7ddd8`  
		Last Modified: Tue, 18 Nov 2025 03:26:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:63bcd50ec3d14a45a2622b1289292f044900493251741ad97a3826b02db799f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a41f8c68e813123499d266c105fe6688bd6bcf8f237ad01c607367081e8516d`

```dockerfile
```

-	Layers:
	-	`sha256:95c1b6d653d55c72f719d0d09ae969adc36a878dbb3f973015cb26e24ec47903`  
		Last Modified: Tue, 18 Nov 2025 05:05:42 GMT  
		Size: 3.6 MB (3619120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d337c054c04289865a82162a0b6c7329d66ce9691d8bc79d7317489e0c00da0`  
		Last Modified: Tue, 18 Nov 2025 05:05:43 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e9235510be401662fdf9dc150727d52c180223c03f705dd62a4748d9c641ec77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31797132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcf78acee4c0ddc840c2c11a73f8024cb2182d36c20c420e53f35655e2baa6b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:50:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 03:50:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:50:29 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 03:50:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:50:29 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 03:50:29 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 03:50:29 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:50:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:50:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c2cce7df782c8ffa98b09b5026801fd75852fbcc542adda17f2cf674e45181`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422558407904c55bd813e2874a4f66dbfa77cf5efd6db4ed74e52303b441fd29`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fde1d67328042aa04d86b94a193406c1202f0b3541d1c95e7ecc18665ec645`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 5.6 MB (5584802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d6aec61101ef5fb65ec8aa6c4a388c95a5c739b4cae742d9f325477eee3143`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf79b5edc379842c06ef54040d0ded6b238383a6bb48036d8c47a64ab6448096`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:b7b3eab355c7919d43eddafd5cd7c953037bca700170b3c7db17cac1d4581d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be853f3e5bf6bd636b07d5fb91dbb5fb3ba07feaff4963e2ffc605c15e6eb836`

```dockerfile
```

-	Layers:
	-	`sha256:6102950244e9d1ff5d896169fd9854a475d74013ac69c10c65ef6fa2a7790929`  
		Last Modified: Tue, 18 Nov 2025 05:05:47 GMT  
		Size: 3.6 MB (3618241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89d6945e35f196e6b467782a87d7058b1b71566296fc00d94d16329ebc11706`  
		Last Modified: Tue, 18 Nov 2025 05:05:48 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:591fd9434499864d8c1158d89fce00904f6e06d5f392d8262b8c0d7efe39a889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36373157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d242e4657c201f08d46371f334bef5a4a2cfd1eb25ee0a73c00a8e00ac11c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:16:33 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 03:16:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:16:58 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 03:16:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:16:58 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 03:16:58 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 03:16:58 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:16:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:16:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba947a8faede3668130b9a9844eb382708be72367360c131942ce30e890f69c0`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096566cbdfead671dd335e66add44869360797178bf789ed21020aca50249756`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770ec9847c8da429b5188dce7cfaf6ac4b91c4582b3daf192ec92ce2d0299d39`  
		Last Modified: Tue, 18 Nov 2025 03:17:17 GMT  
		Size: 6.2 MB (6232178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d361a094ee90fb336f01e4261818ea22ad6cbc3e39fcce6cb5515b43368904`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524f95e648c0618b5d3b38bdc5cebea65cd4a987dad6fe870e1c305b7207e056`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:de69fcb855bd36d7eaa9a4ecfd53eff2bc04325b0e445720719ed66200cd6c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b52e32c61f8b7849ff947d47141644644953fe7b4d630ee19f40f1748cd66e7`

```dockerfile
```

-	Layers:
	-	`sha256:e3050659ccb70e389b03aa9e8d57539e7786ce53a093f045530af7adae8420da`  
		Last Modified: Tue, 18 Nov 2025 05:05:52 GMT  
		Size: 3.6 MB (3621162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a15fce2cffa58340c6b086eca26c3afabf400aded7333fa7f1c729656d8a9d4d`  
		Last Modified: Tue, 18 Nov 2025 05:05:53 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:23467bd729a8745214c4b47148d1e1dc68c54a8dc6f5f30d56700dd1da4c2aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37737826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b78410d027a00d586d005faef3d9ff264953f988d103bd949a43bfd4926e41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:55:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 02:55:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:55:32 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 02:55:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 02:55:32 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 02:55:32 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 02:55:32 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:55:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:55:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e080cdd1c9f6aad444c1d45fad2abef1c289e41be4b0b209145cba950a2d1759`  
		Last Modified: Tue, 18 Nov 2025 02:55:47 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fdec3d410a5b0ba820cf2f8ac384a67d232c8b7310aebeff1969941baf76d7`  
		Last Modified: Tue, 18 Nov 2025 02:55:46 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f6c7b2758bf989a21f93bfd024042bb2f176e19736daf32ab03cd3ba82dfe5`  
		Last Modified: Tue, 18 Nov 2025 02:55:46 GMT  
		Size: 6.4 MB (6442390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad5965c68a8d870fd340c771fcd0a822fa69e20665680f3039ba7b5756b5e92`  
		Last Modified: Tue, 18 Nov 2025 02:55:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aecb0f69473c2cc21216ed84c0d6d97b09b06e4110d3ea920870a95a00dc818`  
		Last Modified: Tue, 18 Nov 2025 02:55:46 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:89c3d55f090feb68455bd160a8c266cac5a849c39289fd7149847c0181d249ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1703098239e0a9df934e917a5c529ca1c413e2d3fb88b91f5941dec211bdcf8`

```dockerfile
```

-	Layers:
	-	`sha256:ee5bfd23df5e05f29413baba8619cc9e1a1770cea921068409bf0312e61351f9`  
		Last Modified: Tue, 18 Nov 2025 05:05:56 GMT  
		Size: 3.6 MB (3620255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7197602a5065e42953129b118d4095d83e4e031c50f2a67b79f800e9f23560f9`  
		Last Modified: Tue, 18 Nov 2025 05:05:57 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:f9d387a803cfdd1985be0085b60de474124c1fc4131c42d948af42ce3d1759a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40439568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a498e2f8e9c00da85debf16c2073bab51c2c9c0b653433b60f9fc513844e047a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 16:44:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 16:44:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 16:46:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 16:46:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 16:46:07 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 16:46:08 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 16:46:08 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 16:46:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 16:46:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ffe02bc5e011d9cb893ac7ecba601951db86c3c857770e41c5d43a375f8dc`  
		Last Modified: Tue, 18 Nov 2025 16:46:29 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30cf6ef4f4a65c31760e988a5e30d9051d0527712a0e99804a8a5b0bf18cde0`  
		Last Modified: Tue, 18 Nov 2025 16:46:29 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d358c24c19ff6d1e35bbd7a807ef937d4fad4ad9eec488f7e55242059f3e56`  
		Last Modified: Tue, 18 Nov 2025 16:46:30 GMT  
		Size: 6.8 MB (6840337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdd1994aaf0ebbf11da5c4ea4079110c42903e9c55fc736d0715dd2520f4a1d`  
		Last Modified: Tue, 18 Nov 2025 16:46:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef167886b835c0bad9761aaad863c77b11f1e68a30eaa1da5bd0f60046c501b8`  
		Last Modified: Tue, 18 Nov 2025 16:46:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:ce5eced8b97263e3d4500f5786fbf71960c445cd50ad00ef6c40caec7b4e269d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50da01383f3afc5380b2a08f818385dd40286fad66e9f0b21cb3163eba38de6`

```dockerfile
```

-	Layers:
	-	`sha256:4118ca48356c09b8c0b5e6e18d5c8e335596d648c22a32941a0c602926107479`  
		Last Modified: Tue, 18 Nov 2025 20:05:03 GMT  
		Size: 3.6 MB (3621863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf6d27b90bd496865de3bbc67e759074e3fbbbb4c1d8067f8b47ac14fd450fb`  
		Last Modified: Tue, 18 Nov 2025 20:05:04 GMT  
		Size: 15.0 KB (15028 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; riscv64

```console
$ docker pull spiped@sha256:959ca9b18f8621408db5465afde15c6950d3c775a4b30b7afcbbecebe2c13da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37633874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6569fae25137810bd7151d5788496634850dbf582ed479ba779d2f76c148264a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:22:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 19 Nov 2025 19:23:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 19:26:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 19 Nov 2025 19:26:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 19 Nov 2025 19:26:22 GMT
VOLUME [/spiped]
# Wed, 19 Nov 2025 19:26:22 GMT
WORKDIR /spiped
# Wed, 19 Nov 2025 19:26:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 19 Nov 2025 19:26:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Nov 2025 19:26:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d95c0473e2a3ebd4bb8143470f2c4574e809b688d0a73464613a79cebd8c5f`  
		Last Modified: Wed, 19 Nov 2025 19:27:53 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa754d41483b1cdfee7949eeb674d5dbf834f7436ffec40fb1450db638145de5`  
		Last Modified: Wed, 19 Nov 2025 19:27:53 GMT  
		Size: 820.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3692d569c1db6381f3be1989acf3ecde5ca830214a2d215cde5dd31675d2749c`  
		Last Modified: Wed, 19 Nov 2025 19:27:54 GMT  
		Size: 9.4 MB (9358381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32fd578990cfe31e14f8792a3e597ae02f3d352751be338bebcb7cd6e0b1c74`  
		Last Modified: Wed, 19 Nov 2025 19:27:53 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98f8f5e6a20cabd1e5b017f926e971a243a4f3a1a77bf31df8c75b0ddb7ea10`  
		Last Modified: Wed, 19 Nov 2025 19:27:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:50fec440ac1cd513e81f4ca03fdcecf5f2054e293af66362f154bf705b89876f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5177bbce1bb2f0302d87f2b11fbe5d8db563bcb4796bd8fe8db26cf53ea0f3ae`

```dockerfile
```

-	Layers:
	-	`sha256:8e66ff47ad83b988d6f182d9f81c66275ad954f7ec9deb15d983342bfc9edd22`  
		Last Modified: Wed, 19 Nov 2025 23:04:44 GMT  
		Size: 3.6 MB (3613269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9faa99ec8424007503d60c406ef512e9259c10b056d1a123b6ee4b2ad8c6f807`  
		Last Modified: Wed, 19 Nov 2025 23:04:45 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:0cc161584fd80bfa10ff2782bfcfa1c4be74a02047ba26409d0389e8f2e14240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35957952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6305c3b1ea8d0e6c559e141387c419530d60f59572ad26ce258790dc913ffd1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:01:37 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 04:01:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 04:01:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 04:01:54 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 04:01:54 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 04:01:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:01:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:01:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a9f8204c54a671034d8c9e635eef8807f29cb90649065a9ba5e66bed4acfbf`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda0974bd23cf2a73bb4f152623809d2fc8e734905a457114c9c03ca36a01144`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d727647b8da22b57df503f6765a7797eee413482299726be8d98cbdf2270b3`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 6.1 MB (6121210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50b0de3d190c1cc7a6dc935b91e017801f2b3e5df36dcbe0d9e09ed2f763d8b`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8006a7de8a5327bf044f7f4e3e2e62d600c335b9245de92a76e57cefc083159e`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:ead10e78092e259d73cef02c88d71b85a73429c3b8303d3dbab7b84f5b018218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1542f64d650d2fcd16668e14181f913919f85779f78af5d2dcb2dd5a04a5229`

```dockerfile
```

-	Layers:
	-	`sha256:a3101f855d36ca311ded5b1214062b9109c30cfe662a7936b96eda160aaa8843`  
		Last Modified: Tue, 18 Nov 2025 05:06:07 GMT  
		Size: 3.6 MB (3618489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ed9bffb5ad34ddcb7b0cf4d59648545bb7eec8d096db3e28ef312d2c3f72b76`  
		Last Modified: Tue, 18 Nov 2025 05:06:08 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:7b9625a81e8db9045c4eaf8f9bf40b8ef8c78a666bb7201d8d7c80538a418f7a
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
$ docker pull spiped@sha256:7d011e9e579768cd749e2df95806a3b739ebbdd516385dac92f2e9cda3570e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9d66303cac034d8960b8128b5967170028d350ecf6e131c4bf30b000a3f836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c041bc04e274276fc6a842ca20a0cf973af7c178bcfb6575c0d8203718fc91`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f81b6f5c689713065e6b968619711a3bd698fd708594cc90dae3977d54ca24e`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a035501670b01c25e6d7ce231bae87ef493bb668e877be52618f03679b673c4f`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 107.6 KB (107645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f81362a47a6b65eaf0da33a0c61df7c9a874d76861e5ae8fa0bc16547593db`  
		Last Modified: Wed, 08 Oct 2025 22:58:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ae81c7faaf7b0d0454b9d217085e8da2f5e5a72ead2527e67506b0d4834801`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ed8b2f715fbc09ab5fcc75433e022573fd8e46bded0d7dd791180a01b3d4a8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b323748eb9cefd40fcfe67d6c7dd561a4f5c4498457b7739b98161ea53a531c`

```dockerfile
```

-	Layers:
	-	`sha256:64366b1f73c30d49b216afd6a2acb0a27ad6d69bbaf554934ef1fb5a1b8ae379`  
		Last Modified: Thu, 09 Oct 2025 01:04:34 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d77f4db066b7ca49f19231acfa8a9f30749e3884bc787f4fcb01d3cb8a54b848`  
		Last Modified: Thu, 09 Oct 2025 01:04:35 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:07f6c1ec4d9a40087ba1fabf98ca259b39af58fe0aa3d1b5aff7a5c9c85aab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66830d62439293e746c3d4171b26eb7b060853f622562e26647e13254243d153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153e87cee3c8273a66e75e0a084e6876c74329042a77778cc75c7865eafb5817`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e054efed96e629a0c9a72dadd2a8d348aa66730afa5f59ce6e02a530b64b8d73`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dbbcac13a86093cd5821deda5686d525abf33f1ffacea149ae0a0b642a332f`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 89.2 KB (89158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6448f1d44fa11364cf66800119dd7e5e05fc9b9d8384cce8cc858006c0684aae`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fa931b05c23aa0b5927c5fc4bea0d9aa65908b7ac3e936a5a5888060a49337`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e083a00e19dd556e9a671f1709ffc708a0ab8d2a7373856218a44de2df24d462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47da3cb18e03a2142fd48220b0903336c0d8a799d804ac3b38780211559ba36`

```dockerfile
```

-	Layers:
	-	`sha256:069680ffcf03350d43ef8d45bcb21dafd37c1132acdfce2d83391a239a85d47e`  
		Last Modified: Thu, 09 Oct 2025 01:04:38 GMT  
		Size: 14.2 KB (14190 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:742d7ee47c94e03887525e682c2614d90b9b1f43f674ce4407bcf06b787caa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3312569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db7cd0fffd0a4f2c540dfe37e4c940cf5c7595aeffea1bf7acc4b1793c73d9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a85ed9579bf45ac1db2ef56f4067b84fe0c4d8e51e006ec1d925eb0c32bf22`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85621545c13dee2ff1d8660f7847266105703d040c19d1816e374881a3bdf6e`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8afad049c072c9b6d3ed2946f7d0c0782835979f90696b68ac6e4c0efff5bf4`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 81.7 KB (81688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35464221f20a70de628e3018e70c13c2e8ed9970a791049f1ba3bae429355536`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d6fea506e0050596918141446ad53da32b5b3a4fc9c7a5d497caf9a7ec6390`  
		Last Modified: Wed, 08 Oct 2025 22:10:18 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1db53d701cc5320b98ed95f8e8288e9c84ddb8ad31b517b42fe2faa626874b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f53816c0890232fc85b4017c83eabcfb11884aeab001b608b66e2a8c9e183e3`

```dockerfile
```

-	Layers:
	-	`sha256:f33fdb1fd07f91c527d8c950dcb81f1eea51882f51d66c0f4da88547240c6499`  
		Last Modified: Thu, 09 Oct 2025 01:04:42 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a9fe69db1d74bfbe4aa6a07c0fb4e0e59f4eff9e1636b7e0c486b6435b788b`  
		Last Modified: Thu, 09 Oct 2025 01:04:42 GMT  
		Size: 14.4 KB (14405 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1c2f38931ee0ff681a7c140bbc874fa1ff5837de4baf9a50a3498fbcb12a9668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b0a53163c15fa0112f2865ee8a52cbed044f04fc7001f7bd1f5e407cd57237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94547f3886a10ef8162a5d7fe9f4308e302dcfd48f5be2db3b1e5d4b5156d815`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ee5fd6e341869b5bcb70e517a1466b54c5191790816dd7956a41164690328b`  
		Last Modified: Wed, 08 Oct 2025 22:29:32 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba2ed7625e00fce702c1adbf90233532e0e4e98935a777f6bdffa076b1c3be2`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 100.6 KB (100621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1612c8ef14c84a7450d3ced7f152a93e533ffbb92d525fae7dde4c2988e230d7`  
		Last Modified: Wed, 08 Oct 2025 22:29:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433ac69ec6618a756cde4ab30a4488c3f0f7b89df240ede5a7b0a29d66250444`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f599a056737cf26e2f1e5bfb25bf8cf6f92cea0ea27b040de42b2e4bf139168f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1c665f9e5776de9d503dbefb3dccddb1d230d81716f5b086b02065d6f512d0`

```dockerfile
```

-	Layers:
	-	`sha256:8c6690f0ed02188be28287964aecbd171476e7e9484ec40d030c20c7b0e182c3`  
		Last Modified: Thu, 09 Oct 2025 01:04:46 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde4ac6f12c825868630b75c268c91338db29a424c87e551c1153694da325c83`  
		Last Modified: Thu, 09 Oct 2025 01:04:46 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac72ab4f716c2dabdad650618a34deccd477e31f604bf27a1f630a7a8433d994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf996beac99b6a5d8eae08ab4703a9cc11bccf3cb429e61a25bebf2947e4b519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664f8e36f37724daee2260066812a0de8999a28949591daef235c15d49ca301a`  
		Last Modified: Wed, 08 Oct 2025 22:22:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee281d18609c0bc414db88c7d17dd26aca0857610126d3e6d974952f5a414ab`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e8cb95edb963d4e91f7f5ea1c0881091c485846b9df554d3c11102b6a6a753`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 120.1 KB (120110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473aab810bb857acc1c39fc855966c0a2de5edd8a71287cf2183cea8dc6fdc4b`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1968cadac684d87fbcd83e1d646d178ae33c9242a480ddbd04f8fdf77b5e2ed`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2e9fe75d8ecfc557edbdaa8476f159fdb286886f6212788ecb61cda153b3ee2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e13e74ee61a3719d708f5b8486f092d523816b5c47e960b60b25a5d76b1aaee`

```dockerfile
```

-	Layers:
	-	`sha256:565649aba2f7ebad36d4ce1a64e495876030406355bb0f7a99f41f82b8300791`  
		Last Modified: Thu, 09 Oct 2025 01:04:50 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf1923abaf687d0c1af4d1718e1e365a3359dbf3e5ff8c339291f60bb0fc220`  
		Last Modified: Thu, 09 Oct 2025 01:04:51 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:506cee7907557b7efa054dc1a4c3261e8956700c9f553e9eb8d9a3470a368431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3854263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca7a1787271596d011a96a2b5632780587dd9653d8b0410f93093e13ecb8fcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf524fa67a04db3aef99fc4ab2113633c6c1965d0f890616009377904a6284`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9d95b7526b98e836dea8e7e9792130d0d6d71b1d6259e6f954ddffc64f5cc`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011805850ee2924d217a7651762c507b895c90911b4151207fe8e82e4388fcce`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 112.7 KB (112682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcef441d2768884d48fcb3b73e59f27e5fe6fc1cb5484df89fd3db0df4ce9437`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03005fd392da3ad1cd46c719335ac18f079118e761584617fe8c73405301647d`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:55eac1eb38ff8ce12fb98d86fb70542b4620b4c59ff746effba30530ad8676de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a3d2f7338bf8715707424b7b716c4498d4c3b844d2dc7387da9a1c64357879`

```dockerfile
```

-	Layers:
	-	`sha256:e3e6cde5a2631b7b9b782bb7fdfcf5de409ca1736416d9573c8888daf799d9e0`  
		Last Modified: Thu, 09 Oct 2025 07:04:30 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9220e8aff0f38f3e237e21c128db8adfad10ae35fb9db4dc56ead1ff1235e9d`  
		Last Modified: Thu, 09 Oct 2025 07:04:31 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0f378090b0e02992217f4f2a73d59cfb8c76cf62d83fec92991b3a8b1f0bfcc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a7d261c52ce9f797be48d32c37a2c3f66b54a18d3599dd071fefa04e588df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c352072eefdbb94e63d3787f16fac871ba719ed362861b9e97b581edd60548`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaa05a9bc37f5bb35d75064bac3af035a1d3a82ac079befd8019359672cc322`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51a4b112c1b7e8d19565628602648b41c69109d0f16548d16e781b095481e4d`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 98.9 KB (98862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971a3bdcb8df001e3163788a7484aea74c6bf79af7ec5c42ae330638a863112`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e689628a891ec93dec38687edd123814871319bfb552253a1ab8608d94fa74`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ef79fccc5586c74ed7a097a019247ca0f6644364c4e1b931202ce2f00cf4e38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c35fd6859715e249d4b311ca37e3e8e7886a7ce1788f0688877545e1f0fb2b`

```dockerfile
```

-	Layers:
	-	`sha256:624da72bc5bd15d76a69efe794516160d8151dc3f9b207f42a5b8b5165948a76`  
		Last Modified: Fri, 10 Oct 2025 22:04:34 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83fb34ab49138178f6f97cf97ae672fc5e173707dec2895a8d5b36f2e7689a5`  
		Last Modified: Fri, 10 Oct 2025 22:04:35 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:be3e9a57eb9caa9fb853c68e3efdc680d9d441f399d676b7a437f56a46d71b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3755528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eee68dd7eaa10392bbfe4c42a39adf582bc976bf97937637b807540ed7960af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eca97998e3d4f083ea39c1b7e9bd8d771aaa888745b8a60d6baff87ab6f8f37`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae19bb237945d6597aced8fc4cd16e5d4f06869978f4f6eb5d90a8bc9be7f39`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 8.0 KB (7957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce433dda6c532473e5da602686ec5186ad28c43789f172a14efc1cd9e38093d`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 96.9 KB (96944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867b81ca187d86754818499befad84648bb33d900aa6c797f74f14d7f06589dd`  
		Last Modified: Thu, 09 Oct 2025 02:26:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de821656be3d9d0eadaa8bfe8c17052ce64308ac54b60bb962a59498810f549e`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:daeef3e785369b94f4c3fec6e7b468c0aa8bcc71748eb82a5dcb98744d0c094a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff814477e4912c3dbc0dc6c3b2d236588fe065252c86c9a2ed142e200619a8a`

```dockerfile
```

-	Layers:
	-	`sha256:3ccf297cff7eee80cdb3e7128fdeabdb48c58df324a049928273000e72eba72d`  
		Last Modified: Thu, 09 Oct 2025 04:04:35 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfca2be336420edbf2af734bab83d3864c289d0e61390ac2cfc5f6d7f183847`  
		Last Modified: Thu, 09 Oct 2025 04:04:36 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4`

```console
$ docker pull spiped@sha256:14ac6360e8a5cc0681580eac1d35bd5a3e4ddc9ed298399e1fcd782738f1baff
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
$ docker pull spiped@sha256:71455e5f7b6d93aae95424129833776689d2cc74f24675f33f11ef10e6f23ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36827283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ede578b23de9ed50043b1c78c384603da62a3b7df444af4e2148f0ff7266201`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:05:43 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 05:05:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:06:09 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 05:06:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 05:06:09 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 05:06:09 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 05:06:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:06:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e801c735c8ed3e544c7e5ec21fdadcb62e4f17e393072bc529855d7c3ae6e6e3`  
		Last Modified: Tue, 18 Nov 2025 05:06:21 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62b3c0fd7b0226ff6077d6b86bbb98a9632fc381cdf3917cf3e1c2f3fb915b9`  
		Last Modified: Tue, 18 Nov 2025 05:06:21 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf671102a10bab89ec80e76bc081b60c8db003c182c52b6e8749c8a00c3bc30`  
		Last Modified: Tue, 18 Nov 2025 05:06:22 GMT  
		Size: 7.0 MB (7048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ffc5a597d5117a8c3287526d416f057a71493f8bedac7a8e932ca15fa08879`  
		Last Modified: Tue, 18 Nov 2025 05:06:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c216a1dbbce2a0979e20d22a121252fde68d545aa23d1a63e9fa1d0c1db1aa53`  
		Last Modified: Tue, 18 Nov 2025 05:06:22 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:09e9e14162507839346b641426b8f6e1d553bb6078045280c57c1e104a75609c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701a082ef72b657e38c5604e48c263523b8f7b7fa5d78baf9e8ff64d708c3cc3`

```dockerfile
```

-	Layers:
	-	`sha256:fca3db4d709b67d3eeea80bb0284b7c014f40447b56781ee5d2f76f709fd4731`  
		Last Modified: Tue, 18 Nov 2025 08:05:17 GMT  
		Size: 3.6 MB (3626126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a54777a6f2567357088e3edbe62f36d27179125f9de343fda2c159e13e6507a9`  
		Last Modified: Tue, 18 Nov 2025 08:05:18 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v5

```console
$ docker pull spiped@sha256:426a7b4ca8678d05e601961162fe4882cec8306e061a2a0ef28e5a4c185e6f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33735923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10f6e5284bc9be0c9fac9071ed5b283aba4e14d014ee6d22cc9577c0245ea88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:25:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 03:25:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:25:47 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 03:25:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:25:47 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 03:25:47 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 03:25:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:25:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19fa3fdca9ccb78808adc904f1814dd017d243bc5c179b0184c715efee222be`  
		Last Modified: Tue, 18 Nov 2025 03:26:00 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcab93afc62cae522725518ebc636cb915e984509d2388ef161ec154a31871d`  
		Last Modified: Tue, 18 Nov 2025 03:26:00 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b355f0770e6bdb66cfcde4ec30ce6a64c64aceb80958f3f48ebaee839ebdf4a`  
		Last Modified: Tue, 18 Nov 2025 03:26:01 GMT  
		Size: 5.8 MB (5789403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c31ee5d96793c7ab7dfb0f7c297aa1fdf92f4dfafc7100f5ac826de7f77bcf`  
		Last Modified: Tue, 18 Nov 2025 03:26:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c62d3d9536df883ab32c9923d67ce50b87b7e9d54f24c3d9927df9a4d7ddd8`  
		Last Modified: Tue, 18 Nov 2025 03:26:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:63bcd50ec3d14a45a2622b1289292f044900493251741ad97a3826b02db799f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a41f8c68e813123499d266c105fe6688bd6bcf8f237ad01c607367081e8516d`

```dockerfile
```

-	Layers:
	-	`sha256:95c1b6d653d55c72f719d0d09ae969adc36a878dbb3f973015cb26e24ec47903`  
		Last Modified: Tue, 18 Nov 2025 05:05:42 GMT  
		Size: 3.6 MB (3619120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d337c054c04289865a82162a0b6c7329d66ce9691d8bc79d7317489e0c00da0`  
		Last Modified: Tue, 18 Nov 2025 05:05:43 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e9235510be401662fdf9dc150727d52c180223c03f705dd62a4748d9c641ec77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31797132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcf78acee4c0ddc840c2c11a73f8024cb2182d36c20c420e53f35655e2baa6b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:50:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 03:50:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:50:29 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 03:50:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:50:29 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 03:50:29 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 03:50:29 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:50:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:50:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c2cce7df782c8ffa98b09b5026801fd75852fbcc542adda17f2cf674e45181`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422558407904c55bd813e2874a4f66dbfa77cf5efd6db4ed74e52303b441fd29`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fde1d67328042aa04d86b94a193406c1202f0b3541d1c95e7ecc18665ec645`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 5.6 MB (5584802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d6aec61101ef5fb65ec8aa6c4a388c95a5c739b4cae742d9f325477eee3143`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf79b5edc379842c06ef54040d0ded6b238383a6bb48036d8c47a64ab6448096`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:b7b3eab355c7919d43eddafd5cd7c953037bca700170b3c7db17cac1d4581d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be853f3e5bf6bd636b07d5fb91dbb5fb3ba07feaff4963e2ffc605c15e6eb836`

```dockerfile
```

-	Layers:
	-	`sha256:6102950244e9d1ff5d896169fd9854a475d74013ac69c10c65ef6fa2a7790929`  
		Last Modified: Tue, 18 Nov 2025 05:05:47 GMT  
		Size: 3.6 MB (3618241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89d6945e35f196e6b467782a87d7058b1b71566296fc00d94d16329ebc11706`  
		Last Modified: Tue, 18 Nov 2025 05:05:48 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:591fd9434499864d8c1158d89fce00904f6e06d5f392d8262b8c0d7efe39a889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36373157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d242e4657c201f08d46371f334bef5a4a2cfd1eb25ee0a73c00a8e00ac11c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:16:33 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 03:16:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:16:58 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 03:16:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:16:58 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 03:16:58 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 03:16:58 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:16:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:16:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba947a8faede3668130b9a9844eb382708be72367360c131942ce30e890f69c0`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096566cbdfead671dd335e66add44869360797178bf789ed21020aca50249756`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770ec9847c8da429b5188dce7cfaf6ac4b91c4582b3daf192ec92ce2d0299d39`  
		Last Modified: Tue, 18 Nov 2025 03:17:17 GMT  
		Size: 6.2 MB (6232178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d361a094ee90fb336f01e4261818ea22ad6cbc3e39fcce6cb5515b43368904`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524f95e648c0618b5d3b38bdc5cebea65cd4a987dad6fe870e1c305b7207e056`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:de69fcb855bd36d7eaa9a4ecfd53eff2bc04325b0e445720719ed66200cd6c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b52e32c61f8b7849ff947d47141644644953fe7b4d630ee19f40f1748cd66e7`

```dockerfile
```

-	Layers:
	-	`sha256:e3050659ccb70e389b03aa9e8d57539e7786ce53a093f045530af7adae8420da`  
		Last Modified: Tue, 18 Nov 2025 05:05:52 GMT  
		Size: 3.6 MB (3621162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a15fce2cffa58340c6b086eca26c3afabf400aded7333fa7f1c729656d8a9d4d`  
		Last Modified: Tue, 18 Nov 2025 05:05:53 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; 386

```console
$ docker pull spiped@sha256:23467bd729a8745214c4b47148d1e1dc68c54a8dc6f5f30d56700dd1da4c2aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37737826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b78410d027a00d586d005faef3d9ff264953f988d103bd949a43bfd4926e41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:55:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 02:55:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:55:32 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 02:55:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 02:55:32 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 02:55:32 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 02:55:32 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:55:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:55:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e080cdd1c9f6aad444c1d45fad2abef1c289e41be4b0b209145cba950a2d1759`  
		Last Modified: Tue, 18 Nov 2025 02:55:47 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fdec3d410a5b0ba820cf2f8ac384a67d232c8b7310aebeff1969941baf76d7`  
		Last Modified: Tue, 18 Nov 2025 02:55:46 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f6c7b2758bf989a21f93bfd024042bb2f176e19736daf32ab03cd3ba82dfe5`  
		Last Modified: Tue, 18 Nov 2025 02:55:46 GMT  
		Size: 6.4 MB (6442390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad5965c68a8d870fd340c771fcd0a822fa69e20665680f3039ba7b5756b5e92`  
		Last Modified: Tue, 18 Nov 2025 02:55:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aecb0f69473c2cc21216ed84c0d6d97b09b06e4110d3ea920870a95a00dc818`  
		Last Modified: Tue, 18 Nov 2025 02:55:46 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:89c3d55f090feb68455bd160a8c266cac5a849c39289fd7149847c0181d249ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1703098239e0a9df934e917a5c529ca1c413e2d3fb88b91f5941dec211bdcf8`

```dockerfile
```

-	Layers:
	-	`sha256:ee5bfd23df5e05f29413baba8619cc9e1a1770cea921068409bf0312e61351f9`  
		Last Modified: Tue, 18 Nov 2025 05:05:56 GMT  
		Size: 3.6 MB (3620255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7197602a5065e42953129b118d4095d83e4e031c50f2a67b79f800e9f23560f9`  
		Last Modified: Tue, 18 Nov 2025 05:05:57 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; ppc64le

```console
$ docker pull spiped@sha256:f9d387a803cfdd1985be0085b60de474124c1fc4131c42d948af42ce3d1759a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40439568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a498e2f8e9c00da85debf16c2073bab51c2c9c0b653433b60f9fc513844e047a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 16:44:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 16:44:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 16:46:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 16:46:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 16:46:07 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 16:46:08 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 16:46:08 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 16:46:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 16:46:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ffe02bc5e011d9cb893ac7ecba601951db86c3c857770e41c5d43a375f8dc`  
		Last Modified: Tue, 18 Nov 2025 16:46:29 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30cf6ef4f4a65c31760e988a5e30d9051d0527712a0e99804a8a5b0bf18cde0`  
		Last Modified: Tue, 18 Nov 2025 16:46:29 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d358c24c19ff6d1e35bbd7a807ef937d4fad4ad9eec488f7e55242059f3e56`  
		Last Modified: Tue, 18 Nov 2025 16:46:30 GMT  
		Size: 6.8 MB (6840337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdd1994aaf0ebbf11da5c4ea4079110c42903e9c55fc736d0715dd2520f4a1d`  
		Last Modified: Tue, 18 Nov 2025 16:46:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef167886b835c0bad9761aaad863c77b11f1e68a30eaa1da5bd0f60046c501b8`  
		Last Modified: Tue, 18 Nov 2025 16:46:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:ce5eced8b97263e3d4500f5786fbf71960c445cd50ad00ef6c40caec7b4e269d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50da01383f3afc5380b2a08f818385dd40286fad66e9f0b21cb3163eba38de6`

```dockerfile
```

-	Layers:
	-	`sha256:4118ca48356c09b8c0b5e6e18d5c8e335596d648c22a32941a0c602926107479`  
		Last Modified: Tue, 18 Nov 2025 20:05:03 GMT  
		Size: 3.6 MB (3621863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf6d27b90bd496865de3bbc67e759074e3fbbbb4c1d8067f8b47ac14fd450fb`  
		Last Modified: Tue, 18 Nov 2025 20:05:04 GMT  
		Size: 15.0 KB (15028 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; riscv64

```console
$ docker pull spiped@sha256:959ca9b18f8621408db5465afde15c6950d3c775a4b30b7afcbbecebe2c13da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37633874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6569fae25137810bd7151d5788496634850dbf582ed479ba779d2f76c148264a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:22:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 19 Nov 2025 19:23:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 19:26:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 19 Nov 2025 19:26:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 19 Nov 2025 19:26:22 GMT
VOLUME [/spiped]
# Wed, 19 Nov 2025 19:26:22 GMT
WORKDIR /spiped
# Wed, 19 Nov 2025 19:26:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 19 Nov 2025 19:26:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Nov 2025 19:26:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d95c0473e2a3ebd4bb8143470f2c4574e809b688d0a73464613a79cebd8c5f`  
		Last Modified: Wed, 19 Nov 2025 19:27:53 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa754d41483b1cdfee7949eeb674d5dbf834f7436ffec40fb1450db638145de5`  
		Last Modified: Wed, 19 Nov 2025 19:27:53 GMT  
		Size: 820.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3692d569c1db6381f3be1989acf3ecde5ca830214a2d215cde5dd31675d2749c`  
		Last Modified: Wed, 19 Nov 2025 19:27:54 GMT  
		Size: 9.4 MB (9358381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32fd578990cfe31e14f8792a3e597ae02f3d352751be338bebcb7cd6e0b1c74`  
		Last Modified: Wed, 19 Nov 2025 19:27:53 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98f8f5e6a20cabd1e5b017f926e971a243a4f3a1a77bf31df8c75b0ddb7ea10`  
		Last Modified: Wed, 19 Nov 2025 19:27:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:50fec440ac1cd513e81f4ca03fdcecf5f2054e293af66362f154bf705b89876f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5177bbce1bb2f0302d87f2b11fbe5d8db563bcb4796bd8fe8db26cf53ea0f3ae`

```dockerfile
```

-	Layers:
	-	`sha256:8e66ff47ad83b988d6f182d9f81c66275ad954f7ec9deb15d983342bfc9edd22`  
		Last Modified: Wed, 19 Nov 2025 23:04:44 GMT  
		Size: 3.6 MB (3613269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9faa99ec8424007503d60c406ef512e9259c10b056d1a123b6ee4b2ad8c6f807`  
		Last Modified: Wed, 19 Nov 2025 23:04:45 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; s390x

```console
$ docker pull spiped@sha256:0cc161584fd80bfa10ff2782bfcfa1c4be74a02047ba26409d0389e8f2e14240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35957952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6305c3b1ea8d0e6c559e141387c419530d60f59572ad26ce258790dc913ffd1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:01:37 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 04:01:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 04:01:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 04:01:54 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 04:01:54 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 04:01:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:01:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:01:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a9f8204c54a671034d8c9e635eef8807f29cb90649065a9ba5e66bed4acfbf`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda0974bd23cf2a73bb4f152623809d2fc8e734905a457114c9c03ca36a01144`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d727647b8da22b57df503f6765a7797eee413482299726be8d98cbdf2270b3`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 6.1 MB (6121210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50b0de3d190c1cc7a6dc935b91e017801f2b3e5df36dcbe0d9e09ed2f763d8b`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8006a7de8a5327bf044f7f4e3e2e62d600c335b9245de92a76e57cefc083159e`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:ead10e78092e259d73cef02c88d71b85a73429c3b8303d3dbab7b84f5b018218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1542f64d650d2fcd16668e14181f913919f85779f78af5d2dcb2dd5a04a5229`

```dockerfile
```

-	Layers:
	-	`sha256:a3101f855d36ca311ded5b1214062b9109c30cfe662a7936b96eda160aaa8843`  
		Last Modified: Tue, 18 Nov 2025 05:06:07 GMT  
		Size: 3.6 MB (3618489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ed9bffb5ad34ddcb7b0cf4d59648545bb7eec8d096db3e28ef312d2c3f72b76`  
		Last Modified: Tue, 18 Nov 2025 05:06:08 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4-alpine`

```console
$ docker pull spiped@sha256:7b9625a81e8db9045c4eaf8f9bf40b8ef8c78a666bb7201d8d7c80538a418f7a
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
$ docker pull spiped@sha256:7d011e9e579768cd749e2df95806a3b739ebbdd516385dac92f2e9cda3570e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9d66303cac034d8960b8128b5967170028d350ecf6e131c4bf30b000a3f836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c041bc04e274276fc6a842ca20a0cf973af7c178bcfb6575c0d8203718fc91`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f81b6f5c689713065e6b968619711a3bd698fd708594cc90dae3977d54ca24e`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a035501670b01c25e6d7ce231bae87ef493bb668e877be52618f03679b673c4f`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 107.6 KB (107645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f81362a47a6b65eaf0da33a0c61df7c9a874d76861e5ae8fa0bc16547593db`  
		Last Modified: Wed, 08 Oct 2025 22:58:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ae81c7faaf7b0d0454b9d217085e8da2f5e5a72ead2527e67506b0d4834801`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ed8b2f715fbc09ab5fcc75433e022573fd8e46bded0d7dd791180a01b3d4a8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b323748eb9cefd40fcfe67d6c7dd561a4f5c4498457b7739b98161ea53a531c`

```dockerfile
```

-	Layers:
	-	`sha256:64366b1f73c30d49b216afd6a2acb0a27ad6d69bbaf554934ef1fb5a1b8ae379`  
		Last Modified: Thu, 09 Oct 2025 01:04:34 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d77f4db066b7ca49f19231acfa8a9f30749e3884bc787f4fcb01d3cb8a54b848`  
		Last Modified: Thu, 09 Oct 2025 01:04:35 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:07f6c1ec4d9a40087ba1fabf98ca259b39af58fe0aa3d1b5aff7a5c9c85aab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66830d62439293e746c3d4171b26eb7b060853f622562e26647e13254243d153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153e87cee3c8273a66e75e0a084e6876c74329042a77778cc75c7865eafb5817`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e054efed96e629a0c9a72dadd2a8d348aa66730afa5f59ce6e02a530b64b8d73`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dbbcac13a86093cd5821deda5686d525abf33f1ffacea149ae0a0b642a332f`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 89.2 KB (89158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6448f1d44fa11364cf66800119dd7e5e05fc9b9d8384cce8cc858006c0684aae`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fa931b05c23aa0b5927c5fc4bea0d9aa65908b7ac3e936a5a5888060a49337`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e083a00e19dd556e9a671f1709ffc708a0ab8d2a7373856218a44de2df24d462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47da3cb18e03a2142fd48220b0903336c0d8a799d804ac3b38780211559ba36`

```dockerfile
```

-	Layers:
	-	`sha256:069680ffcf03350d43ef8d45bcb21dafd37c1132acdfce2d83391a239a85d47e`  
		Last Modified: Thu, 09 Oct 2025 01:04:38 GMT  
		Size: 14.2 KB (14190 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:742d7ee47c94e03887525e682c2614d90b9b1f43f674ce4407bcf06b787caa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3312569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db7cd0fffd0a4f2c540dfe37e4c940cf5c7595aeffea1bf7acc4b1793c73d9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a85ed9579bf45ac1db2ef56f4067b84fe0c4d8e51e006ec1d925eb0c32bf22`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85621545c13dee2ff1d8660f7847266105703d040c19d1816e374881a3bdf6e`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8afad049c072c9b6d3ed2946f7d0c0782835979f90696b68ac6e4c0efff5bf4`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 81.7 KB (81688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35464221f20a70de628e3018e70c13c2e8ed9970a791049f1ba3bae429355536`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d6fea506e0050596918141446ad53da32b5b3a4fc9c7a5d497caf9a7ec6390`  
		Last Modified: Wed, 08 Oct 2025 22:10:18 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1db53d701cc5320b98ed95f8e8288e9c84ddb8ad31b517b42fe2faa626874b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f53816c0890232fc85b4017c83eabcfb11884aeab001b608b66e2a8c9e183e3`

```dockerfile
```

-	Layers:
	-	`sha256:f33fdb1fd07f91c527d8c950dcb81f1eea51882f51d66c0f4da88547240c6499`  
		Last Modified: Thu, 09 Oct 2025 01:04:42 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a9fe69db1d74bfbe4aa6a07c0fb4e0e59f4eff9e1636b7e0c486b6435b788b`  
		Last Modified: Thu, 09 Oct 2025 01:04:42 GMT  
		Size: 14.4 KB (14405 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1c2f38931ee0ff681a7c140bbc874fa1ff5837de4baf9a50a3498fbcb12a9668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b0a53163c15fa0112f2865ee8a52cbed044f04fc7001f7bd1f5e407cd57237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94547f3886a10ef8162a5d7fe9f4308e302dcfd48f5be2db3b1e5d4b5156d815`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ee5fd6e341869b5bcb70e517a1466b54c5191790816dd7956a41164690328b`  
		Last Modified: Wed, 08 Oct 2025 22:29:32 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba2ed7625e00fce702c1adbf90233532e0e4e98935a777f6bdffa076b1c3be2`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 100.6 KB (100621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1612c8ef14c84a7450d3ced7f152a93e533ffbb92d525fae7dde4c2988e230d7`  
		Last Modified: Wed, 08 Oct 2025 22:29:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433ac69ec6618a756cde4ab30a4488c3f0f7b89df240ede5a7b0a29d66250444`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f599a056737cf26e2f1e5bfb25bf8cf6f92cea0ea27b040de42b2e4bf139168f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1c665f9e5776de9d503dbefb3dccddb1d230d81716f5b086b02065d6f512d0`

```dockerfile
```

-	Layers:
	-	`sha256:8c6690f0ed02188be28287964aecbd171476e7e9484ec40d030c20c7b0e182c3`  
		Last Modified: Thu, 09 Oct 2025 01:04:46 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde4ac6f12c825868630b75c268c91338db29a424c87e551c1153694da325c83`  
		Last Modified: Thu, 09 Oct 2025 01:04:46 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac72ab4f716c2dabdad650618a34deccd477e31f604bf27a1f630a7a8433d994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf996beac99b6a5d8eae08ab4703a9cc11bccf3cb429e61a25bebf2947e4b519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664f8e36f37724daee2260066812a0de8999a28949591daef235c15d49ca301a`  
		Last Modified: Wed, 08 Oct 2025 22:22:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee281d18609c0bc414db88c7d17dd26aca0857610126d3e6d974952f5a414ab`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e8cb95edb963d4e91f7f5ea1c0881091c485846b9df554d3c11102b6a6a753`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 120.1 KB (120110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473aab810bb857acc1c39fc855966c0a2de5edd8a71287cf2183cea8dc6fdc4b`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1968cadac684d87fbcd83e1d646d178ae33c9242a480ddbd04f8fdf77b5e2ed`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2e9fe75d8ecfc557edbdaa8476f159fdb286886f6212788ecb61cda153b3ee2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e13e74ee61a3719d708f5b8486f092d523816b5c47e960b60b25a5d76b1aaee`

```dockerfile
```

-	Layers:
	-	`sha256:565649aba2f7ebad36d4ce1a64e495876030406355bb0f7a99f41f82b8300791`  
		Last Modified: Thu, 09 Oct 2025 01:04:50 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf1923abaf687d0c1af4d1718e1e365a3359dbf3e5ff8c339291f60bb0fc220`  
		Last Modified: Thu, 09 Oct 2025 01:04:51 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:506cee7907557b7efa054dc1a4c3261e8956700c9f553e9eb8d9a3470a368431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3854263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca7a1787271596d011a96a2b5632780587dd9653d8b0410f93093e13ecb8fcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf524fa67a04db3aef99fc4ab2113633c6c1965d0f890616009377904a6284`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9d95b7526b98e836dea8e7e9792130d0d6d71b1d6259e6f954ddffc64f5cc`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011805850ee2924d217a7651762c507b895c90911b4151207fe8e82e4388fcce`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 112.7 KB (112682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcef441d2768884d48fcb3b73e59f27e5fe6fc1cb5484df89fd3db0df4ce9437`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03005fd392da3ad1cd46c719335ac18f079118e761584617fe8c73405301647d`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:55eac1eb38ff8ce12fb98d86fb70542b4620b4c59ff746effba30530ad8676de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a3d2f7338bf8715707424b7b716c4498d4c3b844d2dc7387da9a1c64357879`

```dockerfile
```

-	Layers:
	-	`sha256:e3e6cde5a2631b7b9b782bb7fdfcf5de409ca1736416d9573c8888daf799d9e0`  
		Last Modified: Thu, 09 Oct 2025 07:04:30 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9220e8aff0f38f3e237e21c128db8adfad10ae35fb9db4dc56ead1ff1235e9d`  
		Last Modified: Thu, 09 Oct 2025 07:04:31 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0f378090b0e02992217f4f2a73d59cfb8c76cf62d83fec92991b3a8b1f0bfcc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a7d261c52ce9f797be48d32c37a2c3f66b54a18d3599dd071fefa04e588df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c352072eefdbb94e63d3787f16fac871ba719ed362861b9e97b581edd60548`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaa05a9bc37f5bb35d75064bac3af035a1d3a82ac079befd8019359672cc322`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51a4b112c1b7e8d19565628602648b41c69109d0f16548d16e781b095481e4d`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 98.9 KB (98862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971a3bdcb8df001e3163788a7484aea74c6bf79af7ec5c42ae330638a863112`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e689628a891ec93dec38687edd123814871319bfb552253a1ab8608d94fa74`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ef79fccc5586c74ed7a097a019247ca0f6644364c4e1b931202ce2f00cf4e38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c35fd6859715e249d4b311ca37e3e8e7886a7ce1788f0688877545e1f0fb2b`

```dockerfile
```

-	Layers:
	-	`sha256:624da72bc5bd15d76a69efe794516160d8151dc3f9b207f42a5b8b5165948a76`  
		Last Modified: Fri, 10 Oct 2025 22:04:34 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83fb34ab49138178f6f97cf97ae672fc5e173707dec2895a8d5b36f2e7689a5`  
		Last Modified: Fri, 10 Oct 2025 22:04:35 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:be3e9a57eb9caa9fb853c68e3efdc680d9d441f399d676b7a437f56a46d71b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3755528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eee68dd7eaa10392bbfe4c42a39adf582bc976bf97937637b807540ed7960af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eca97998e3d4f083ea39c1b7e9bd8d771aaa888745b8a60d6baff87ab6f8f37`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae19bb237945d6597aced8fc4cd16e5d4f06869978f4f6eb5d90a8bc9be7f39`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 8.0 KB (7957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce433dda6c532473e5da602686ec5186ad28c43789f172a14efc1cd9e38093d`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 96.9 KB (96944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867b81ca187d86754818499befad84648bb33d900aa6c797f74f14d7f06589dd`  
		Last Modified: Thu, 09 Oct 2025 02:26:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de821656be3d9d0eadaa8bfe8c17052ce64308ac54b60bb962a59498810f549e`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:daeef3e785369b94f4c3fec6e7b468c0aa8bcc71748eb82a5dcb98744d0c094a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff814477e4912c3dbc0dc6c3b2d236588fe065252c86c9a2ed142e200619a8a`

```dockerfile
```

-	Layers:
	-	`sha256:3ccf297cff7eee80cdb3e7128fdeabdb48c58df324a049928273000e72eba72d`  
		Last Modified: Thu, 09 Oct 2025 04:04:35 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfca2be336420edbf2af734bab83d3864c289d0e61390ac2cfc5f6d7f183847`  
		Last Modified: Thu, 09 Oct 2025 04:04:36 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:7b9625a81e8db9045c4eaf8f9bf40b8ef8c78a666bb7201d8d7c80538a418f7a
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
$ docker pull spiped@sha256:7d011e9e579768cd749e2df95806a3b739ebbdd516385dac92f2e9cda3570e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9d66303cac034d8960b8128b5967170028d350ecf6e131c4bf30b000a3f836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c041bc04e274276fc6a842ca20a0cf973af7c178bcfb6575c0d8203718fc91`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f81b6f5c689713065e6b968619711a3bd698fd708594cc90dae3977d54ca24e`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a035501670b01c25e6d7ce231bae87ef493bb668e877be52618f03679b673c4f`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 107.6 KB (107645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f81362a47a6b65eaf0da33a0c61df7c9a874d76861e5ae8fa0bc16547593db`  
		Last Modified: Wed, 08 Oct 2025 22:58:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ae81c7faaf7b0d0454b9d217085e8da2f5e5a72ead2527e67506b0d4834801`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ed8b2f715fbc09ab5fcc75433e022573fd8e46bded0d7dd791180a01b3d4a8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b323748eb9cefd40fcfe67d6c7dd561a4f5c4498457b7739b98161ea53a531c`

```dockerfile
```

-	Layers:
	-	`sha256:64366b1f73c30d49b216afd6a2acb0a27ad6d69bbaf554934ef1fb5a1b8ae379`  
		Last Modified: Thu, 09 Oct 2025 01:04:34 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d77f4db066b7ca49f19231acfa8a9f30749e3884bc787f4fcb01d3cb8a54b848`  
		Last Modified: Thu, 09 Oct 2025 01:04:35 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:07f6c1ec4d9a40087ba1fabf98ca259b39af58fe0aa3d1b5aff7a5c9c85aab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66830d62439293e746c3d4171b26eb7b060853f622562e26647e13254243d153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153e87cee3c8273a66e75e0a084e6876c74329042a77778cc75c7865eafb5817`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e054efed96e629a0c9a72dadd2a8d348aa66730afa5f59ce6e02a530b64b8d73`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dbbcac13a86093cd5821deda5686d525abf33f1ffacea149ae0a0b642a332f`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 89.2 KB (89158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6448f1d44fa11364cf66800119dd7e5e05fc9b9d8384cce8cc858006c0684aae`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fa931b05c23aa0b5927c5fc4bea0d9aa65908b7ac3e936a5a5888060a49337`  
		Last Modified: Wed, 08 Oct 2025 22:09:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e083a00e19dd556e9a671f1709ffc708a0ab8d2a7373856218a44de2df24d462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47da3cb18e03a2142fd48220b0903336c0d8a799d804ac3b38780211559ba36`

```dockerfile
```

-	Layers:
	-	`sha256:069680ffcf03350d43ef8d45bcb21dafd37c1132acdfce2d83391a239a85d47e`  
		Last Modified: Thu, 09 Oct 2025 01:04:38 GMT  
		Size: 14.2 KB (14190 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:742d7ee47c94e03887525e682c2614d90b9b1f43f674ce4407bcf06b787caa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3312569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db7cd0fffd0a4f2c540dfe37e4c940cf5c7595aeffea1bf7acc4b1793c73d9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a85ed9579bf45ac1db2ef56f4067b84fe0c4d8e51e006ec1d925eb0c32bf22`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85621545c13dee2ff1d8660f7847266105703d040c19d1816e374881a3bdf6e`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8afad049c072c9b6d3ed2946f7d0c0782835979f90696b68ac6e4c0efff5bf4`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 81.7 KB (81688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35464221f20a70de628e3018e70c13c2e8ed9970a791049f1ba3bae429355536`  
		Last Modified: Wed, 08 Oct 2025 22:10:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d6fea506e0050596918141446ad53da32b5b3a4fc9c7a5d497caf9a7ec6390`  
		Last Modified: Wed, 08 Oct 2025 22:10:18 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1db53d701cc5320b98ed95f8e8288e9c84ddb8ad31b517b42fe2faa626874b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f53816c0890232fc85b4017c83eabcfb11884aeab001b608b66e2a8c9e183e3`

```dockerfile
```

-	Layers:
	-	`sha256:f33fdb1fd07f91c527d8c950dcb81f1eea51882f51d66c0f4da88547240c6499`  
		Last Modified: Thu, 09 Oct 2025 01:04:42 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a9fe69db1d74bfbe4aa6a07c0fb4e0e59f4eff9e1636b7e0c486b6435b788b`  
		Last Modified: Thu, 09 Oct 2025 01:04:42 GMT  
		Size: 14.4 KB (14405 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1c2f38931ee0ff681a7c140bbc874fa1ff5837de4baf9a50a3498fbcb12a9668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b0a53163c15fa0112f2865ee8a52cbed044f04fc7001f7bd1f5e407cd57237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94547f3886a10ef8162a5d7fe9f4308e302dcfd48f5be2db3b1e5d4b5156d815`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ee5fd6e341869b5bcb70e517a1466b54c5191790816dd7956a41164690328b`  
		Last Modified: Wed, 08 Oct 2025 22:29:32 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba2ed7625e00fce702c1adbf90233532e0e4e98935a777f6bdffa076b1c3be2`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 100.6 KB (100621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1612c8ef14c84a7450d3ced7f152a93e533ffbb92d525fae7dde4c2988e230d7`  
		Last Modified: Wed, 08 Oct 2025 22:29:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433ac69ec6618a756cde4ab30a4488c3f0f7b89df240ede5a7b0a29d66250444`  
		Last Modified: Wed, 08 Oct 2025 22:29:31 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f599a056737cf26e2f1e5bfb25bf8cf6f92cea0ea27b040de42b2e4bf139168f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1c665f9e5776de9d503dbefb3dccddb1d230d81716f5b086b02065d6f512d0`

```dockerfile
```

-	Layers:
	-	`sha256:8c6690f0ed02188be28287964aecbd171476e7e9484ec40d030c20c7b0e182c3`  
		Last Modified: Thu, 09 Oct 2025 01:04:46 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde4ac6f12c825868630b75c268c91338db29a424c87e551c1153694da325c83`  
		Last Modified: Thu, 09 Oct 2025 01:04:46 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac72ab4f716c2dabdad650618a34deccd477e31f604bf27a1f630a7a8433d994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf996beac99b6a5d8eae08ab4703a9cc11bccf3cb429e61a25bebf2947e4b519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664f8e36f37724daee2260066812a0de8999a28949591daef235c15d49ca301a`  
		Last Modified: Wed, 08 Oct 2025 22:22:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee281d18609c0bc414db88c7d17dd26aca0857610126d3e6d974952f5a414ab`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e8cb95edb963d4e91f7f5ea1c0881091c485846b9df554d3c11102b6a6a753`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 120.1 KB (120110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473aab810bb857acc1c39fc855966c0a2de5edd8a71287cf2183cea8dc6fdc4b`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1968cadac684d87fbcd83e1d646d178ae33c9242a480ddbd04f8fdf77b5e2ed`  
		Last Modified: Wed, 08 Oct 2025 22:22:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2e9fe75d8ecfc557edbdaa8476f159fdb286886f6212788ecb61cda153b3ee2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e13e74ee61a3719d708f5b8486f092d523816b5c47e960b60b25a5d76b1aaee`

```dockerfile
```

-	Layers:
	-	`sha256:565649aba2f7ebad36d4ce1a64e495876030406355bb0f7a99f41f82b8300791`  
		Last Modified: Thu, 09 Oct 2025 01:04:50 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf1923abaf687d0c1af4d1718e1e365a3359dbf3e5ff8c339291f60bb0fc220`  
		Last Modified: Thu, 09 Oct 2025 01:04:51 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:506cee7907557b7efa054dc1a4c3261e8956700c9f553e9eb8d9a3470a368431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3854263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca7a1787271596d011a96a2b5632780587dd9653d8b0410f93093e13ecb8fcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf524fa67a04db3aef99fc4ab2113633c6c1965d0f890616009377904a6284`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9d95b7526b98e836dea8e7e9792130d0d6d71b1d6259e6f954ddffc64f5cc`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011805850ee2924d217a7651762c507b895c90911b4151207fe8e82e4388fcce`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 112.7 KB (112682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcef441d2768884d48fcb3b73e59f27e5fe6fc1cb5484df89fd3db0df4ce9437`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03005fd392da3ad1cd46c719335ac18f079118e761584617fe8c73405301647d`  
		Last Modified: Thu, 09 Oct 2025 03:32:10 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:55eac1eb38ff8ce12fb98d86fb70542b4620b4c59ff746effba30530ad8676de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a3d2f7338bf8715707424b7b716c4498d4c3b844d2dc7387da9a1c64357879`

```dockerfile
```

-	Layers:
	-	`sha256:e3e6cde5a2631b7b9b782bb7fdfcf5de409ca1736416d9573c8888daf799d9e0`  
		Last Modified: Thu, 09 Oct 2025 07:04:30 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9220e8aff0f38f3e237e21c128db8adfad10ae35fb9db4dc56ead1ff1235e9d`  
		Last Modified: Thu, 09 Oct 2025 07:04:31 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0f378090b0e02992217f4f2a73d59cfb8c76cf62d83fec92991b3a8b1f0bfcc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a7d261c52ce9f797be48d32c37a2c3f66b54a18d3599dd071fefa04e588df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c352072eefdbb94e63d3787f16fac871ba719ed362861b9e97b581edd60548`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaa05a9bc37f5bb35d75064bac3af035a1d3a82ac079befd8019359672cc322`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51a4b112c1b7e8d19565628602648b41c69109d0f16548d16e781b095481e4d`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 98.9 KB (98862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971a3bdcb8df001e3163788a7484aea74c6bf79af7ec5c42ae330638a863112`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e689628a891ec93dec38687edd123814871319bfb552253a1ab8608d94fa74`  
		Last Modified: Fri, 10 Oct 2025 20:50:10 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ef79fccc5586c74ed7a097a019247ca0f6644364c4e1b931202ce2f00cf4e38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c35fd6859715e249d4b311ca37e3e8e7886a7ce1788f0688877545e1f0fb2b`

```dockerfile
```

-	Layers:
	-	`sha256:624da72bc5bd15d76a69efe794516160d8151dc3f9b207f42a5b8b5165948a76`  
		Last Modified: Fri, 10 Oct 2025 22:04:34 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83fb34ab49138178f6f97cf97ae672fc5e173707dec2895a8d5b36f2e7689a5`  
		Last Modified: Fri, 10 Oct 2025 22:04:35 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:be3e9a57eb9caa9fb853c68e3efdc680d9d441f399d676b7a437f56a46d71b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3755528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eee68dd7eaa10392bbfe4c42a39adf582bc976bf97937637b807540ed7960af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eca97998e3d4f083ea39c1b7e9bd8d771aaa888745b8a60d6baff87ab6f8f37`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae19bb237945d6597aced8fc4cd16e5d4f06869978f4f6eb5d90a8bc9be7f39`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 8.0 KB (7957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce433dda6c532473e5da602686ec5186ad28c43789f172a14efc1cd9e38093d`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 96.9 KB (96944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867b81ca187d86754818499befad84648bb33d900aa6c797f74f14d7f06589dd`  
		Last Modified: Thu, 09 Oct 2025 02:26:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de821656be3d9d0eadaa8bfe8c17052ce64308ac54b60bb962a59498810f549e`  
		Last Modified: Thu, 09 Oct 2025 02:26:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:daeef3e785369b94f4c3fec6e7b468c0aa8bcc71748eb82a5dcb98744d0c094a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff814477e4912c3dbc0dc6c3b2d236588fe065252c86c9a2ed142e200619a8a`

```dockerfile
```

-	Layers:
	-	`sha256:3ccf297cff7eee80cdb3e7128fdeabdb48c58df324a049928273000e72eba72d`  
		Last Modified: Thu, 09 Oct 2025 04:04:35 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfca2be336420edbf2af734bab83d3864c289d0e61390ac2cfc5f6d7f183847`  
		Last Modified: Thu, 09 Oct 2025 04:04:36 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:14ac6360e8a5cc0681580eac1d35bd5a3e4ddc9ed298399e1fcd782738f1baff
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
$ docker pull spiped@sha256:71455e5f7b6d93aae95424129833776689d2cc74f24675f33f11ef10e6f23ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36827283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ede578b23de9ed50043b1c78c384603da62a3b7df444af4e2148f0ff7266201`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:05:43 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 05:05:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:06:09 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 05:06:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 05:06:09 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 05:06:09 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 05:06:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:06:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e801c735c8ed3e544c7e5ec21fdadcb62e4f17e393072bc529855d7c3ae6e6e3`  
		Last Modified: Tue, 18 Nov 2025 05:06:21 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62b3c0fd7b0226ff6077d6b86bbb98a9632fc381cdf3917cf3e1c2f3fb915b9`  
		Last Modified: Tue, 18 Nov 2025 05:06:21 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf671102a10bab89ec80e76bc081b60c8db003c182c52b6e8749c8a00c3bc30`  
		Last Modified: Tue, 18 Nov 2025 05:06:22 GMT  
		Size: 7.0 MB (7048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ffc5a597d5117a8c3287526d416f057a71493f8bedac7a8e932ca15fa08879`  
		Last Modified: Tue, 18 Nov 2025 05:06:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c216a1dbbce2a0979e20d22a121252fde68d545aa23d1a63e9fa1d0c1db1aa53`  
		Last Modified: Tue, 18 Nov 2025 05:06:22 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:09e9e14162507839346b641426b8f6e1d553bb6078045280c57c1e104a75609c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701a082ef72b657e38c5604e48c263523b8f7b7fa5d78baf9e8ff64d708c3cc3`

```dockerfile
```

-	Layers:
	-	`sha256:fca3db4d709b67d3eeea80bb0284b7c014f40447b56781ee5d2f76f709fd4731`  
		Last Modified: Tue, 18 Nov 2025 08:05:17 GMT  
		Size: 3.6 MB (3626126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a54777a6f2567357088e3edbe62f36d27179125f9de343fda2c159e13e6507a9`  
		Last Modified: Tue, 18 Nov 2025 08:05:18 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:426a7b4ca8678d05e601961162fe4882cec8306e061a2a0ef28e5a4c185e6f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33735923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10f6e5284bc9be0c9fac9071ed5b283aba4e14d014ee6d22cc9577c0245ea88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:25:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 03:25:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:25:47 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 03:25:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:25:47 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 03:25:47 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 03:25:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:25:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19fa3fdca9ccb78808adc904f1814dd017d243bc5c179b0184c715efee222be`  
		Last Modified: Tue, 18 Nov 2025 03:26:00 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcab93afc62cae522725518ebc636cb915e984509d2388ef161ec154a31871d`  
		Last Modified: Tue, 18 Nov 2025 03:26:00 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b355f0770e6bdb66cfcde4ec30ce6a64c64aceb80958f3f48ebaee839ebdf4a`  
		Last Modified: Tue, 18 Nov 2025 03:26:01 GMT  
		Size: 5.8 MB (5789403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c31ee5d96793c7ab7dfb0f7c297aa1fdf92f4dfafc7100f5ac826de7f77bcf`  
		Last Modified: Tue, 18 Nov 2025 03:26:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c62d3d9536df883ab32c9923d67ce50b87b7e9d54f24c3d9927df9a4d7ddd8`  
		Last Modified: Tue, 18 Nov 2025 03:26:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:63bcd50ec3d14a45a2622b1289292f044900493251741ad97a3826b02db799f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a41f8c68e813123499d266c105fe6688bd6bcf8f237ad01c607367081e8516d`

```dockerfile
```

-	Layers:
	-	`sha256:95c1b6d653d55c72f719d0d09ae969adc36a878dbb3f973015cb26e24ec47903`  
		Last Modified: Tue, 18 Nov 2025 05:05:42 GMT  
		Size: 3.6 MB (3619120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d337c054c04289865a82162a0b6c7329d66ce9691d8bc79d7317489e0c00da0`  
		Last Modified: Tue, 18 Nov 2025 05:05:43 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e9235510be401662fdf9dc150727d52c180223c03f705dd62a4748d9c641ec77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31797132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcf78acee4c0ddc840c2c11a73f8024cb2182d36c20c420e53f35655e2baa6b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:50:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 03:50:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:50:29 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 03:50:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:50:29 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 03:50:29 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 03:50:29 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:50:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:50:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c2cce7df782c8ffa98b09b5026801fd75852fbcc542adda17f2cf674e45181`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422558407904c55bd813e2874a4f66dbfa77cf5efd6db4ed74e52303b441fd29`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fde1d67328042aa04d86b94a193406c1202f0b3541d1c95e7ecc18665ec645`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 5.6 MB (5584802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d6aec61101ef5fb65ec8aa6c4a388c95a5c739b4cae742d9f325477eee3143`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf79b5edc379842c06ef54040d0ded6b238383a6bb48036d8c47a64ab6448096`  
		Last Modified: Tue, 18 Nov 2025 03:50:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:b7b3eab355c7919d43eddafd5cd7c953037bca700170b3c7db17cac1d4581d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be853f3e5bf6bd636b07d5fb91dbb5fb3ba07feaff4963e2ffc605c15e6eb836`

```dockerfile
```

-	Layers:
	-	`sha256:6102950244e9d1ff5d896169fd9854a475d74013ac69c10c65ef6fa2a7790929`  
		Last Modified: Tue, 18 Nov 2025 05:05:47 GMT  
		Size: 3.6 MB (3618241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89d6945e35f196e6b467782a87d7058b1b71566296fc00d94d16329ebc11706`  
		Last Modified: Tue, 18 Nov 2025 05:05:48 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:591fd9434499864d8c1158d89fce00904f6e06d5f392d8262b8c0d7efe39a889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36373157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d242e4657c201f08d46371f334bef5a4a2cfd1eb25ee0a73c00a8e00ac11c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:16:33 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 03:16:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:16:58 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 03:16:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:16:58 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 03:16:58 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 03:16:58 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:16:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:16:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba947a8faede3668130b9a9844eb382708be72367360c131942ce30e890f69c0`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096566cbdfead671dd335e66add44869360797178bf789ed21020aca50249756`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770ec9847c8da429b5188dce7cfaf6ac4b91c4582b3daf192ec92ce2d0299d39`  
		Last Modified: Tue, 18 Nov 2025 03:17:17 GMT  
		Size: 6.2 MB (6232178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d361a094ee90fb336f01e4261818ea22ad6cbc3e39fcce6cb5515b43368904`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524f95e648c0618b5d3b38bdc5cebea65cd4a987dad6fe870e1c305b7207e056`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:de69fcb855bd36d7eaa9a4ecfd53eff2bc04325b0e445720719ed66200cd6c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b52e32c61f8b7849ff947d47141644644953fe7b4d630ee19f40f1748cd66e7`

```dockerfile
```

-	Layers:
	-	`sha256:e3050659ccb70e389b03aa9e8d57539e7786ce53a093f045530af7adae8420da`  
		Last Modified: Tue, 18 Nov 2025 05:05:52 GMT  
		Size: 3.6 MB (3621162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a15fce2cffa58340c6b086eca26c3afabf400aded7333fa7f1c729656d8a9d4d`  
		Last Modified: Tue, 18 Nov 2025 05:05:53 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:23467bd729a8745214c4b47148d1e1dc68c54a8dc6f5f30d56700dd1da4c2aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37737826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b78410d027a00d586d005faef3d9ff264953f988d103bd949a43bfd4926e41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:55:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 02:55:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:55:32 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 02:55:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 02:55:32 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 02:55:32 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 02:55:32 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:55:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:55:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e080cdd1c9f6aad444c1d45fad2abef1c289e41be4b0b209145cba950a2d1759`  
		Last Modified: Tue, 18 Nov 2025 02:55:47 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fdec3d410a5b0ba820cf2f8ac384a67d232c8b7310aebeff1969941baf76d7`  
		Last Modified: Tue, 18 Nov 2025 02:55:46 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f6c7b2758bf989a21f93bfd024042bb2f176e19736daf32ab03cd3ba82dfe5`  
		Last Modified: Tue, 18 Nov 2025 02:55:46 GMT  
		Size: 6.4 MB (6442390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad5965c68a8d870fd340c771fcd0a822fa69e20665680f3039ba7b5756b5e92`  
		Last Modified: Tue, 18 Nov 2025 02:55:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aecb0f69473c2cc21216ed84c0d6d97b09b06e4110d3ea920870a95a00dc818`  
		Last Modified: Tue, 18 Nov 2025 02:55:46 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:89c3d55f090feb68455bd160a8c266cac5a849c39289fd7149847c0181d249ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1703098239e0a9df934e917a5c529ca1c413e2d3fb88b91f5941dec211bdcf8`

```dockerfile
```

-	Layers:
	-	`sha256:ee5bfd23df5e05f29413baba8619cc9e1a1770cea921068409bf0312e61351f9`  
		Last Modified: Tue, 18 Nov 2025 05:05:56 GMT  
		Size: 3.6 MB (3620255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7197602a5065e42953129b118d4095d83e4e031c50f2a67b79f800e9f23560f9`  
		Last Modified: Tue, 18 Nov 2025 05:05:57 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:f9d387a803cfdd1985be0085b60de474124c1fc4131c42d948af42ce3d1759a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40439568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a498e2f8e9c00da85debf16c2073bab51c2c9c0b653433b60f9fc513844e047a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 16:44:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 16:44:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 16:46:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 16:46:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 16:46:07 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 16:46:08 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 16:46:08 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 16:46:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 16:46:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ffe02bc5e011d9cb893ac7ecba601951db86c3c857770e41c5d43a375f8dc`  
		Last Modified: Tue, 18 Nov 2025 16:46:29 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30cf6ef4f4a65c31760e988a5e30d9051d0527712a0e99804a8a5b0bf18cde0`  
		Last Modified: Tue, 18 Nov 2025 16:46:29 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d358c24c19ff6d1e35bbd7a807ef937d4fad4ad9eec488f7e55242059f3e56`  
		Last Modified: Tue, 18 Nov 2025 16:46:30 GMT  
		Size: 6.8 MB (6840337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdd1994aaf0ebbf11da5c4ea4079110c42903e9c55fc736d0715dd2520f4a1d`  
		Last Modified: Tue, 18 Nov 2025 16:46:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef167886b835c0bad9761aaad863c77b11f1e68a30eaa1da5bd0f60046c501b8`  
		Last Modified: Tue, 18 Nov 2025 16:46:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:ce5eced8b97263e3d4500f5786fbf71960c445cd50ad00ef6c40caec7b4e269d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50da01383f3afc5380b2a08f818385dd40286fad66e9f0b21cb3163eba38de6`

```dockerfile
```

-	Layers:
	-	`sha256:4118ca48356c09b8c0b5e6e18d5c8e335596d648c22a32941a0c602926107479`  
		Last Modified: Tue, 18 Nov 2025 20:05:03 GMT  
		Size: 3.6 MB (3621863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf6d27b90bd496865de3bbc67e759074e3fbbbb4c1d8067f8b47ac14fd450fb`  
		Last Modified: Tue, 18 Nov 2025 20:05:04 GMT  
		Size: 15.0 KB (15028 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; riscv64

```console
$ docker pull spiped@sha256:959ca9b18f8621408db5465afde15c6950d3c775a4b30b7afcbbecebe2c13da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37633874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6569fae25137810bd7151d5788496634850dbf582ed479ba779d2f76c148264a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:22:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 19 Nov 2025 19:23:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 19:26:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 19 Nov 2025 19:26:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 19 Nov 2025 19:26:22 GMT
VOLUME [/spiped]
# Wed, 19 Nov 2025 19:26:22 GMT
WORKDIR /spiped
# Wed, 19 Nov 2025 19:26:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 19 Nov 2025 19:26:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Nov 2025 19:26:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d95c0473e2a3ebd4bb8143470f2c4574e809b688d0a73464613a79cebd8c5f`  
		Last Modified: Wed, 19 Nov 2025 19:27:53 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa754d41483b1cdfee7949eeb674d5dbf834f7436ffec40fb1450db638145de5`  
		Last Modified: Wed, 19 Nov 2025 19:27:53 GMT  
		Size: 820.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3692d569c1db6381f3be1989acf3ecde5ca830214a2d215cde5dd31675d2749c`  
		Last Modified: Wed, 19 Nov 2025 19:27:54 GMT  
		Size: 9.4 MB (9358381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32fd578990cfe31e14f8792a3e597ae02f3d352751be338bebcb7cd6e0b1c74`  
		Last Modified: Wed, 19 Nov 2025 19:27:53 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98f8f5e6a20cabd1e5b017f926e971a243a4f3a1a77bf31df8c75b0ddb7ea10`  
		Last Modified: Wed, 19 Nov 2025 19:27:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:50fec440ac1cd513e81f4ca03fdcecf5f2054e293af66362f154bf705b89876f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5177bbce1bb2f0302d87f2b11fbe5d8db563bcb4796bd8fe8db26cf53ea0f3ae`

```dockerfile
```

-	Layers:
	-	`sha256:8e66ff47ad83b988d6f182d9f81c66275ad954f7ec9deb15d983342bfc9edd22`  
		Last Modified: Wed, 19 Nov 2025 23:04:44 GMT  
		Size: 3.6 MB (3613269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9faa99ec8424007503d60c406ef512e9259c10b056d1a123b6ee4b2ad8c6f807`  
		Last Modified: Wed, 19 Nov 2025 23:04:45 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:0cc161584fd80bfa10ff2782bfcfa1c4be74a02047ba26409d0389e8f2e14240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35957952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6305c3b1ea8d0e6c559e141387c419530d60f59572ad26ce258790dc913ffd1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:01:37 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 18 Nov 2025 04:01:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 18 Nov 2025 04:01:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 04:01:54 GMT
VOLUME [/spiped]
# Tue, 18 Nov 2025 04:01:54 GMT
WORKDIR /spiped
# Tue, 18 Nov 2025 04:01:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:01:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:01:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a9f8204c54a671034d8c9e635eef8807f29cb90649065a9ba5e66bed4acfbf`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda0974bd23cf2a73bb4f152623809d2fc8e734905a457114c9c03ca36a01144`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d727647b8da22b57df503f6765a7797eee413482299726be8d98cbdf2270b3`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 6.1 MB (6121210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50b0de3d190c1cc7a6dc935b91e017801f2b3e5df36dcbe0d9e09ed2f763d8b`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8006a7de8a5327bf044f7f4e3e2e62d600c335b9245de92a76e57cefc083159e`  
		Last Modified: Tue, 18 Nov 2025 04:02:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:ead10e78092e259d73cef02c88d71b85a73429c3b8303d3dbab7b84f5b018218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1542f64d650d2fcd16668e14181f913919f85779f78af5d2dcb2dd5a04a5229`

```dockerfile
```

-	Layers:
	-	`sha256:a3101f855d36ca311ded5b1214062b9109c30cfe662a7936b96eda160aaa8843`  
		Last Modified: Tue, 18 Nov 2025 05:06:07 GMT  
		Size: 3.6 MB (3618489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ed9bffb5ad34ddcb7b0cf4d59648545bb7eec8d096db3e28ef312d2c3f72b76`  
		Last Modified: Tue, 18 Nov 2025 05:06:08 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json
