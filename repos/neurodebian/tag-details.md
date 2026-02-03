<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bookworm`](#neurodebianbookworm)
-	[`neurodebian:bookworm-non-free`](#neurodebianbookworm-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:forky`](#neurodebianforky)
-	[`neurodebian:forky-non-free`](#neurodebianforky-non-free)
-	[`neurodebian:jammy`](#neurodebianjammy)
-	[`neurodebian:jammy-non-free`](#neurodebianjammy-non-free)
-	[`neurodebian:latest`](#neurodebianlatest)
-	[`neurodebian:nd`](#neurodebiannd)
-	[`neurodebian:nd-non-free`](#neurodebiannd-non-free)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd120`](#neurodebiannd120)
-	[`neurodebian:nd120-non-free`](#neurodebiannd120-non-free)
-	[`neurodebian:nd130`](#neurodebiannd130)
-	[`neurodebian:nd130-non-free`](#neurodebiannd130-non-free)
-	[`neurodebian:nd140`](#neurodebiannd140)
-	[`neurodebian:nd140-non-free`](#neurodebiannd140-non-free)
-	[`neurodebian:nd22.04`](#neurodebiannd2204)
-	[`neurodebian:nd22.04-non-free`](#neurodebiannd2204-non-free)
-	[`neurodebian:nd24.04`](#neurodebiannd2404)
-	[`neurodebian:nd24.04-non-free`](#neurodebiannd2404-non-free)
-	[`neurodebian:nd25.04`](#neurodebiannd2504)
-	[`neurodebian:nd25.04-non-free`](#neurodebiannd2504-non-free)
-	[`neurodebian:noble`](#neurodebiannoble)
-	[`neurodebian:noble-non-free`](#neurodebiannoble-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)
-	[`neurodebian:plucky`](#neurodebianplucky)
-	[`neurodebian:plucky-non-free`](#neurodebianplucky-non-free)
-	[`neurodebian:sid`](#neurodebiansid)
-	[`neurodebian:sid-non-free`](#neurodebiansid-non-free)
-	[`neurodebian:trixie`](#neurodebiantrixie)
-	[`neurodebian:trixie-non-free`](#neurodebiantrixie-non-free)

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:f1b4f2ecb2536ed462000f6c9038959182e67d622eef44c5ea0ff7bfaf7e509d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:c1242f1ae926b10fac848bae44a495dccd66a1f230b6b7fed29b1f6a0d61b415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90ffe9ae6a0219a6a9bb417e0807677106ca2fdd75bfa7c85c32f6b7b19a61d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:48:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:42 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2076e118117aaae08d4043f950fcfaf533cbf38d422320c2d3e4e79fd1cb42e0`  
		Last Modified: Tue, 03 Feb 2026 02:48:56 GMT  
		Size: 11.3 MB (11273502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adaf593435563a325b4e351870a254d93ace4a6f6e07a0076246d00cb5465a4`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9b8967af24b7aecf27b7cce202956704c3b50f82c4085ecce2a9a7160bd959`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b33b63666fc4fd13332f7b20b6bdbe9ca7b0a7ffa3038bb9e9fff447c9777c9`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 93.4 KB (93407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a0d1ebd5434d67fae166a6c83a948abf5b042772ba034630f0f2f66f59f73ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19eff2aa6afd5c085e13f1a2dd7f58dc001e6100f286fe390bd5ba170a02014`

```dockerfile
```

-	Layers:
	-	`sha256:c8bca7e18d0064b9ef958dc8aca15d79c44717eef437552691266c3fc08cb082`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cca950dd7c438bcf4a08ac81d7d99a6ee39835a490ee62f3eb322f3b651ec73`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a825b8dfeaffd1bc173ea5d15af02b32c121fd426067bd93de21c9b0b8473829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59714558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf967e7a2b8332edc2032368cd4cc76c09f252bda502d5584cc30e62e93e6a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:51:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3266c9acb92d5ab093d574343ae67394c8340ee57dc673ee80e32d4b1febb73a`  
		Last Modified: Tue, 03 Feb 2026 02:51:20 GMT  
		Size: 11.3 MB (11252882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90ad8a19b89b650fc2ae655f9f1ba6c4c33a4e78bc900ba4787b3ce4f3624c1`  
		Last Modified: Tue, 03 Feb 2026 02:51:20 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5340c77e8e063fecb5791e93211158603333e1e95fc58c0e803d4697821562bc`  
		Last Modified: Tue, 03 Feb 2026 02:51:20 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb9296d3cf1afb97b856e1075f492c18b57ebb73ff639fff0a950dc633cd3cf`  
		Last Modified: Tue, 03 Feb 2026 02:51:20 GMT  
		Size: 93.5 KB (93542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c058d45c29b4cf6c2565081f5987d5732793cc8f0d5446d9130f693c0b53247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88347108f9cb3045f3960417a1bd87b0861f0802d052f3ef8831338ce86b01b9`

```dockerfile
```

-	Layers:
	-	`sha256:c141eb8ef0ef7d5dff7d7bef9f987bd457984435ab33077b3a20f40904fd3eb0`  
		Last Modified: Tue, 03 Feb 2026 02:51:20 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41cc2cd7208471c68a447348e06615156161dbbca540a71502a9b494919699c7`  
		Last Modified: Tue, 03 Feb 2026 02:51:20 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:a4c2d54476a243c1e3446744e1ba1c2214cabef3820e37dc8c8904eb4552582a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61257022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820b2ad9ffd6327a389770a6137a17652f679fe852b86fe63e2627c9ad9555bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:50:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:11 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a7f977a794a5fd56ece19f51541cec3b8ba447f10234ab001213bf850f92f64d`  
		Last Modified: Tue, 03 Feb 2026 01:13:34 GMT  
		Size: 49.5 MB (49468454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26b7baeabeade531ef7f9c1e90bb83ec231559000bcb172a3d42c9c52a13581`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 11.7 MB (11692965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545298cfcb2c0ef599758efa0bb2433ddba17671129a91b2f81d0f8c01de360e`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e3e586f3ba7f832374d99d5f3c2ebebe5198e3591951ded0a25f8016be0c57`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ffda1436e97be251fe611d4411ad207185b88106b305a875a268f22d2e54d3`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 93.4 KB (93425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:975c1b6232f112b4d91d722d790f9635ed313933a851013d7ba1e0be636dc6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2eb365ca11e1109453dd15f2b465da21f8daa56c23b3a6952c3d6b42ee61a5`

```dockerfile
```

-	Layers:
	-	`sha256:7fcf231778ddaf83b1d3e91394058200a344269891e8a9b9be1404a47eb9c669`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 4.1 MB (4073846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e067cfdbb37f564eb7ac8e086244b1a9fe445646b82fa379028478e6ff88f9eb`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:b854e40c7710fcc1176cc13e0c671a175266e060f49c78fdcdd8392eb6145496
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e89cb8491347c3793299b4609dc9f486e374e7e6b3871024cdaa52a242e8f889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea60233cd27143f98be7c617d34a2b7abccc6ff2aabcc29751782a270e795b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:48:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:49 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c45697feb00d0b63cd7fac2b980d8cb335c36bdc7ec19133c10ac21ea5e36fd`  
		Last Modified: Tue, 03 Feb 2026 02:48:58 GMT  
		Size: 11.3 MB (11273436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bba6c203b9ebf4afc38346aebc78ede9b2b21c6744a3a63f7fd29c95bbec92`  
		Last Modified: Tue, 03 Feb 2026 02:48:57 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71877ab4d7a4f26899206a9f324de43293a354660fed1fd6bbc7313294974b4`  
		Last Modified: Tue, 03 Feb 2026 02:48:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4479e797285f1f997594e3d4cf6214b8c6d464e7fafd77f8344aa65ae6180541`  
		Last Modified: Tue, 03 Feb 2026 02:48:57 GMT  
		Size: 93.4 KB (93380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769627860e6b9788b55ff0f269633177f23ea77468d5f7e497b9b2a68e432c98`  
		Last Modified: Tue, 03 Feb 2026 02:48:58 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1aca7321e3f7be0a4a173952cd6e7d2f376d911b90eda28aed731f8858aa437a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5604db43735de04e2a0de391c3b42da87fa2823aa41080a13383d7db4ed34d7`

```dockerfile
```

-	Layers:
	-	`sha256:e014afc086f73ae28b94d4c5f55d120bf2c935b26fe4bfc6e4841a31381aeba3`  
		Last Modified: Tue, 03 Feb 2026 02:48:57 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c58749e130661407c54b4f05e54b5e92070583915549b6dca5ee525921770f`  
		Last Modified: Tue, 03 Feb 2026 02:48:57 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e599ff7d96b232003874e2d68d248e8639ab13b311cc9c72d10ed0c88d60d16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59715134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fc55d172f895c9096019f144d0bdf0d4b3370e77a142a82b35256615baff23`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:51:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b68f8edacfdf5365bc59762f6e137b3cb4a57dcef4e8f3d8676326d25cfa7e`  
		Last Modified: Tue, 03 Feb 2026 02:51:56 GMT  
		Size: 11.3 MB (11252963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440f4b13f161e074886ad5cb9584c84f836571ad61d9d2b6694228d25e2f5849`  
		Last Modified: Tue, 03 Feb 2026 02:51:55 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1065c34065e9ea4961334cc417397a9203ead63b9b4add9a6c8125098a9e88cf`  
		Last Modified: Tue, 03 Feb 2026 02:51:55 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d2be16ad111846291203cf7e0ed1c0f46a1da47bcb6ed7ed03a702b0754d33`  
		Last Modified: Tue, 03 Feb 2026 02:51:55 GMT  
		Size: 93.6 KB (93589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b974cb7e1d873a1873954b5d412eea6edd026a6228509fd17c719d1712ee7c`  
		Last Modified: Tue, 03 Feb 2026 02:51:56 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e2dcc4eaad8355f1791200cfbb013339bd40f1bda315125585515d6896a729dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a491c7a3eba1c7c25d91299811e639e01eaaea5b257f1baa80d29cdfacbc393`

```dockerfile
```

-	Layers:
	-	`sha256:b7a85c747dd7d17a5b5f7274e409a93b2074eeb2832567d114126adca088aa50`  
		Last Modified: Tue, 03 Feb 2026 02:51:56 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c563d6ce14f0efda1477101a2fac4ae3fb9f7ba0005edf2c6dbb99e7c350d92`  
		Last Modified: Tue, 03 Feb 2026 02:51:55 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:15c4fd7f4ae69dda15f010fe14f030228c0ec31df32eee923704fad6a66840f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61257438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611853ff5e7b7314aea5f6ecb0764d406f9482ab9a27ba2f0573f193147239ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:50:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:15 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a7f977a794a5fd56ece19f51541cec3b8ba447f10234ab001213bf850f92f64d`  
		Last Modified: Tue, 03 Feb 2026 01:13:34 GMT  
		Size: 49.5 MB (49468454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de10e295966a7e5139d07603a07981adef413a49af2017977a73771b0cb96116`  
		Last Modified: Tue, 03 Feb 2026 02:50:23 GMT  
		Size: 11.7 MB (11692927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899d3418df53b95a5eea13aa82e46a5f3b5129543401d1b47e0fa907fe96c7e2`  
		Last Modified: Tue, 03 Feb 2026 02:50:23 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061c713a7d20c03075ab7e707af26fbdee5d96e664024b10389d9b5bfe835c14`  
		Last Modified: Tue, 03 Feb 2026 02:50:23 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63abd2041f6dec416c3b3c0d53b05dc4b3d3563f2ab10a125135e7823fda57dc`  
		Last Modified: Tue, 03 Feb 2026 02:50:23 GMT  
		Size: 93.4 KB (93427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5248525f02ee083731f715c3859b5c4e5db3b48374f0469bf8c31c5bea0e7221`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:60fdbaee666240a3d2a3f5922e3b34a11fa6676451f909ba37d55858eeb6beec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d09d36dd5eee401ff246b91d94ebc3509c6067b37f8f0078fc2543d58a573f`

```dockerfile
```

-	Layers:
	-	`sha256:5082655454d356bead422988875229dc0c780bc132a607d4ad0b39323d1271a7`  
		Last Modified: Tue, 03 Feb 2026 02:50:23 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd67c4b2a9465922f45d2d9498654a70dbf46d43a1b1379d4fb11911aea99389`  
		Last Modified: Tue, 03 Feb 2026 02:50:23 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:885ab45ebd96b8c8a149ab0916f3bea94054a593cdce6a6f2d8c4ba09aa27396
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:4ecd9d1443e75181863e1b0a0427e8661fe92478615af709b630787153110c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03739d2be3885eea98c095c9c74a10e89108d70ea5b2d847b8bd4eff7a14a21`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:48:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5012d8636e02354fc754917a5033735462dd0859681a109ccc1d487ff5a0cbf`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 11.1 MB (11103507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958c347c1e407c069a4d2260fef1c8c469021a6e69859e324c4cc80a7ec71c79`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35c37d32450eca29c1869c861c8b6211f487e8459cb481d58bb785e689ccb2c`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59abc559ead350f7d45163c15a158239544ac872d73e287e28c62ec5d8d18573`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 101.5 KB (101459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:280100744d6de918a33f4507f434ad023c0711e4c6788351c5d3f00bb1fd15ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d5313ade697365c5833199af043d3c89e529d7424c8c2b152a0eebacb9eba8`

```dockerfile
```

-	Layers:
	-	`sha256:f1be9831e14fae35c899ab4f09a3310194c3a382bf28babcc9d58c730aced7a8`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ef553d164e1c42152cdab3a581c5a74ff6db0a28b1ed04399d3942e993e238`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:86cfc34b840820a8fe84956bd371e6199e13e4a058829457a6e7744cfb8360b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63471602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdfa29e52ee39c97a34b1b1c90fffba3941ae1c1e71e4e54a3e48a5236e115e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:51:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:02 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58879c86c59c7df27e0a73b9871db9be284e7b8f556d768ce7fb3fb480f9e206`  
		Last Modified: Tue, 03 Feb 2026 02:51:16 GMT  
		Size: 11.1 MB (11109967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314e0f97e0b03075b4d990a2ed9fa571367773fa25893b53abe071aa0e8346f2`  
		Last Modified: Tue, 03 Feb 2026 02:51:16 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8939451b05ca684069c3474313ac5ddda1d805d5d47d1b6ace08e474d7abe43`  
		Last Modified: Tue, 03 Feb 2026 02:51:16 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8a02c619f5296c2e4f4af6c7934197573f843edfbe6c9b93209815263bad23`  
		Last Modified: Tue, 03 Feb 2026 02:51:16 GMT  
		Size: 101.2 KB (101156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a1a848719d7d0597021427147569793781f7c99ac283ce53c9c16f2e77d67198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f878a4517c2277fbb3ec9fa17526aaca27b8d1c6d2c7cf68308cb2923b7d000`

```dockerfile
```

-	Layers:
	-	`sha256:3df4a4551a3a59bfc804f8866169620df0c3f66ce55aa2651d987ade9193fedd`  
		Last Modified: Tue, 03 Feb 2026 02:51:16 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b266db82fea3e86e4d5da2f69f0bba092bc90388911a1a0a784b3049371303c7`  
		Last Modified: Tue, 03 Feb 2026 02:51:16 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:1354f1ba7aa85b916ee958170cc7f050521000edc06c0220ab0cf6973176f09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66305210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4da1f09e5d913306d7d286ac599b7b695e8ea981b3a1e5b82766088cdf3209a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:50:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f6d70808fcfec5fc2c45e150a669aa79950bfd30968e7ba0de2c962cff56fc33`  
		Last Modified: Tue, 03 Feb 2026 01:13:58 GMT  
		Size: 54.7 MB (54699582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9765b7cdc157a2219f748b055e54b374ab46c88982ba130b80275b5ecbb6fcd0`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 11.5 MB (11502195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6922f2485c8fd18c9ee31feb2a1e54e28e70fbad4799bb50222116212c3ddd76`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1a7b780248edd8b5c2395aed2fd482edddda39a73f74ed0809c302882cd079`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3b0d8566f41d7aec87b6b984dc4efeb7f44430c851566e02f98bf290d961bc`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 101.3 KB (101277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8af366ff88aa6538a80fc1c5bcaf92a68758fa13237a31ef1c7869480bdab3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c649e84a44d41ec14a3f312f22561643cb8e92c41a625c7460cb1e8b576c6cd`

```dockerfile
```

-	Layers:
	-	`sha256:f6f7876a1fa47fff70e97fa7f5bc6879aaf558a242b44885694bf41fd8a52b49`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93bb6ee6d764fe93e3d6a5da1a083ac6a14962c64a50b3b1e7c6aaa9f29c9629`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:77194295cf5f5eaaad2c4923d519cba7c14716b51a98a35f4e82a7cff61e4243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c6fe056761bf624c48323aa68b1a0f5d713c4d0b61832e061ca1ea7ecda933c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21627ce4e7ec3d7e88f1abe7fa4bc41c147db83695ed04258bda3a7b6dc4445b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:48:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:32 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:35 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1d633e2bc91aea90973516b45752d540db2ea3cedbfabefc881c030ae1e19f`  
		Last Modified: Tue, 03 Feb 2026 02:48:45 GMT  
		Size: 11.1 MB (11103524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c5bcd939835f01a3b851bb6cd334c3fdaceae44dc5ad0b2ff9983495d88ad0`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0cc5228ca7eca77a2a40283d1d9ae0330aa87b2d01ff8cf386e2e04e296e29`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b465d2202f2a38722e786a7c0e5bd9671a551c9ebbcc46d3929a4bce2970a3`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 101.4 KB (101429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9cdf47e555c97d954a83f3afa5500cf5b0c917f7db57b2737a13e136b200a8`  
		Last Modified: Tue, 03 Feb 2026 02:48:45 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fff433a0c16911f96bb25b6fb337a61b0a4c392e54d963c253c382e94f961fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6144505b81e88e04ceec7346c279a36e30e6c8747e2c29b4a53bcccf0a4224`

```dockerfile
```

-	Layers:
	-	`sha256:83904257f196bddf92b45b7631562668036000f57c2d47b653b38066e4e63f45`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf75af788ef139571dc1aa51a678c8b24d5627b132e55c158d9d084f744edd4e`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2e3447d7574d73923eee873cfe9c4fd867860560a331d24a796d44afbf56f4dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63471688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7af8b4f564086a1bd49480d1a6447df23ef006de28ac8dc3a7957f9c3645fbb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:51:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca39f502305b0c1bb375baecb8b56080c0991ad9fcc2e55ead25e0e3ba8b605`  
		Last Modified: Tue, 03 Feb 2026 02:51:21 GMT  
		Size: 11.1 MB (11109715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22aa437d699f198f3f9813d737b57370795c888aed4b7e381da936681d2844f9`  
		Last Modified: Tue, 03 Feb 2026 02:51:21 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8af9c45551b8fe56d8931700d67d1898765bf48ff4fc0a841fcef4022fd91e`  
		Last Modified: Tue, 03 Feb 2026 02:51:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d9ba681f82005822c01d2a02aa6bbbc2f0c4e74e910ed45365de4a5d91aa7`  
		Last Modified: Tue, 03 Feb 2026 02:51:21 GMT  
		Size: 101.1 KB (101108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a674ac10c9220b624e0ff4c35168ff1dbaba397cbce00f24887b33295cc9734`  
		Last Modified: Tue, 03 Feb 2026 02:51:22 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:46c11994357bb45b93289a8ab73043cfef60e892ecc08e61df264f12f61755ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af38135cb49d019d049c5c688c37bdf8cce80c7f48f4bb60962094f2d6e3669`

```dockerfile
```

-	Layers:
	-	`sha256:28f9c55cbf2f619573983902d942b6239ff8a851047c1b98418bb2c718901fdb`  
		Last Modified: Tue, 03 Feb 2026 02:51:21 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99deaae6542b3b7ebda4bc486334410dafdd2c554f530e8f6b3961b0b8ef2166`  
		Last Modified: Tue, 03 Feb 2026 02:51:21 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:08b312b3fe28f63548e1c157cfbf5bfd51baa274c71c6fb170097708022c7057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66305759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa07c637ab99777fbe8867c39480e039f706dee25ae6f758cbef8a47483d487`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:50:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f6d70808fcfec5fc2c45e150a669aa79950bfd30968e7ba0de2c962cff56fc33`  
		Last Modified: Tue, 03 Feb 2026 01:13:58 GMT  
		Size: 54.7 MB (54699582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664978e2ab7548b095db8bbf8dbd5af37114ce8462bb64e43a6c661837548a96`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 11.5 MB (11502354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a712b3803ebc860aac4c28daea93cb3141b2973ebeb843c9a85897d924831ef`  
		Last Modified: Tue, 03 Feb 2026 02:50:21 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2dea87f7cb441a246f0ff27aba64c9e2587db205a062d183d9ea534f7800cf5`  
		Last Modified: Tue, 03 Feb 2026 02:50:21 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187883a3231287ee0e5fc6ae4b66e97e5c3496ec4439202d8f5533c6915c9c39`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 101.3 KB (101281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a50d37cc3aca1dd7b883e568ddf0ea92b1274b3d68e294b5f0c780939275010`  
		Last Modified: Tue, 03 Feb 2026 02:50:23 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:799acc823b45de4ec480828b3518a7b8dcaf3571218225b105f1dce2331bd076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad48092ed58e67c71d2c73d1b255420a060ffa4b699e3502f7827418dbec4b7e`

```dockerfile
```

-	Layers:
	-	`sha256:ebdad496ad0a1912aada804329d687f8a8a79114d956aa14c80b300ceb666a60`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7913432ee7aa90d184c5cd7aeedc2fe42e140b06b4f14393bc2272604efefdac`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:e60e70dd2ecc36918ee4ef7a12501e9a8c5aa4238ec448c3ab89f0565356a8db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky` - linux; amd64

```console
$ docker pull neurodebian@sha256:62557098c459de418b2e59e2e0374ded8453839c8dc8a8a635e934e25b272fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60289672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e09429446df5077bffdd30968e77332ee3dbad06f3b3bea0d5d4e95d262872`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:49:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e7ee730174f13176a4a2ca706f251743bedcb5459da1b8f275d5b6bcc67c0aef`  
		Last Modified: Tue, 03 Feb 2026 01:14:19 GMT  
		Size: 48.7 MB (48655735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2730c822ebcac3a15d3d766e879e3429b4f9adf6fe76271ccfc76c249537f502`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 11.5 MB (11540381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1930f996b21f85d26d813979c448b5cc33d9133a8314e6eec99d3e973f6035c`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2a47c885c79a443813591c82a08a80cadd63adef2c8d39f9547d22badfcacb`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc7445e516a5d581aed9ea2f12b0eaeed7fb0988a1b7763124e12ff75af87a`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 90.6 KB (90648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6aed34d51bd5ea07823221ec742d4e2d9232789220b79efe8f13368675e3040f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3787c78d5c00b60dd7bf2b7563d0ab9a1f311b1efe8e20720192ef75f7123075`

```dockerfile
```

-	Layers:
	-	`sha256:5b86a2fd5679538630a28183b3b3ba91097d7d8705bb17616d47cf9348996af0`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 3.6 MB (3608543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d480378322cf7188821388658920d0bdc152a426690dd4aca8e70b9eb5cd12aa`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c3c2279dfef5b1dc5801320cca47e07527c809bfd5b8501e47a54886d752e589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60016699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5303416cf8c75cf18340519a6abdb2c2603976b0e99f7947a44a4386905605d9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:51:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2309f92dd0c61c985b2d0f865b8d146291a99f7a179b5a243da4f72d2cb33817`  
		Last Modified: Tue, 03 Feb 2026 01:14:24 GMT  
		Size: 48.7 MB (48678525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe9791138d0a57aaca050f57b565887e667f14821c8231f93c2d0c305c7e471`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 11.2 MB (11243891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c0a9f59ed57dde67760c8b95b1ac9a6e2b6a87a29f3ffe1bb31f968cf15933`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e2416924c6e88fd98b2ecc7ba1069de6c6c9b1579c057f3ace4d1ce181bb26`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb4e195e6cd71c46f9c6a5642063ca9d7395067cbc82cec1f6c0c133adfd0a4`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 91.4 KB (91373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e16860a4e030141224640806bb45d2e39341e64caea29bc7a7b88081583ec337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84bfffc9dcc54d9ba58efca740fba1097bfef5a19b1896c56713736816def4dd`

```dockerfile
```

-	Layers:
	-	`sha256:172889f9237c9e8233f219895f1fe9b57a489f5bd8800559fb0fa2feda3cf7ab`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 3.6 MB (3618081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76cc10f725eb0b8fd8134c1c72a383f9d97018377dc013bed07e8ea5d26e62ec`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 14.1 KB (14056 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:372715dd9d593229a9937c8e98543f99da9162df29c92ca6eac1f1fc5ab78228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61860090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670a3c8d8684fcd47ddc6995df4f4337300ec88be2777020a509d2a71a2a36fc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:50:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:38 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bd6304d6e56f66e13385dc7464436c6e3933118a9e5b697acc2b57e9b6d5e5cc`  
		Last Modified: Tue, 03 Feb 2026 01:14:23 GMT  
		Size: 50.0 MB (49981936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b0e91a2c7873b83c48aa15d9575016025f65009bb2a2697185fc7c1cb3258a`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 11.8 MB (11784286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b778f855abd2e9eba1fb32ff318ee9e04561d33943ad5ee010c23514f44c7f9b`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b124115f9efbbfa225774d314331b6efc9cb5a56f0297c3b8a3a232389266b`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b21d5c5dbc2b33cca4880d981b958ba838908e34a46b81d62441314a5465015`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 91.0 KB (90964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:adb60bd7608494b5e43c5616cf74a0c141d1c97857da108077e02b9a48877c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3620386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62470d32ade636f2b7255e3643887b7193c4ef781667ece2d405e4c84592332b`

```dockerfile
```

-	Layers:
	-	`sha256:5d9a2f5cdcd0a0287877961e006e91a56b955f9e17dcbfc60d768d2544743d64`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 3.6 MB (3606482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f6368f043ceb8e4c5ed5e1a65f2c65f04f6fe87b106c5b112dc5c93161a9a7`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:0f18bc1f784f10280a845619e4cb21c545b4bedff88df1e685f5404a23735f3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a163bb449af86570efbb2c848f4a56b0a9f75e2c9bab460fac75b282e0ee9659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60290217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ebf1e005f416f00f58c9265e914c41d744ca6aa1cfbeee885ba91c67104b69`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:49:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e7ee730174f13176a4a2ca706f251743bedcb5459da1b8f275d5b6bcc67c0aef`  
		Last Modified: Tue, 03 Feb 2026 01:14:19 GMT  
		Size: 48.7 MB (48655735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbb37aa9daedccd57c940309ed43a39d7248abc940a23204d466caa4499871f`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 11.5 MB (11540452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1930f996b21f85d26d813979c448b5cc33d9133a8314e6eec99d3e973f6035c`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2a47c885c79a443813591c82a08a80cadd63adef2c8d39f9547d22badfcacb`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035ddd951380f76413ebc0059b6934df85dc73f566840fbe23db460cfcd656e9`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 90.7 KB (90675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ef19c1eb6c1cbf32f075f42496b94816b18968b15c0f0b69876955199b6719`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:14a013c4124a4a318ef9462fba9ce8e7d4f7ade0f5398b9583274cdf91689f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3624538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f2134a5a1a99b81c7e83acec3a0283963987a07471c68c3cdf183c9f72d260`

```dockerfile
```

-	Layers:
	-	`sha256:2164015860c8679b1861e5dd23a57a9c9cf4dfe0487d529174fcf93b3b40604d`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 3.6 MB (3608579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cff4e739dd29e441abfa38f38ab0d7eff091449c92875d8627eed5ac223629`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8782f0cbd867e5cbf0a00809d2009fc7d99b9dac92bc8d074fbb25ad4928217b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60017116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92256154c8d58a75a4a78ba1066be026d1a4d93461b9883112013f1f315b31d6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:51:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2309f92dd0c61c985b2d0f865b8d146291a99f7a179b5a243da4f72d2cb33817`  
		Last Modified: Tue, 03 Feb 2026 01:14:24 GMT  
		Size: 48.7 MB (48678525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026f011967afc3b9472b0c743cd8832587b7373c1a9e793ef57c52f8e1c2061c`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 11.2 MB (11243869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c36ebd2a34f62d27f0d7cef3ead3d16165f9623f928d1bfe2b41b30f74c828`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac5250fe806def3c12f50acd0b6fe7d6851fec3d0a5e991b2638d7543c0dca3`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d313056e5d16e90d2205cc6d85f4999bb2e91762bf29d6f405fe2a6bec2fe67f`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 91.4 KB (91372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5cbbb997fec7584e04e4b04ed9e8fdbdf6ca498e81490eaa86e4db34a6c603`  
		Last Modified: Tue, 03 Feb 2026 02:51:54 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:94e7098c49dd9439a3e0b5fd3a09d5ec77087becdfd9c3a9a528a18285e3ebf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd4e5d034a0bd7358ad9328e4e08533bdf5014b7277fa2e24279b515eb53b93`

```dockerfile
```

-	Layers:
	-	`sha256:556e59f143cdbd0a487dbeb922c3d70dae2429bed531b17f3c08f7d816f3ad23`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 3.6 MB (3618117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9bdedb5ebac73f1c7c14c80ceacc95ed4c954edb869cd21a8abb346bdf0a2d0`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:76db44b9c094c727694409a86d9d46053c182d88334960270e0c32f0cc439d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61860509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfdd9ac4c6dff21718140687ea8b4349667ed4e76bda91b250de02cd621303e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:50:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:38 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:bd6304d6e56f66e13385dc7464436c6e3933118a9e5b697acc2b57e9b6d5e5cc`  
		Last Modified: Tue, 03 Feb 2026 01:14:23 GMT  
		Size: 50.0 MB (49981936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c435bc3bbcc2b13bab5e538cf235a937f4a4af7f766c52a475efea971328f83f`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 11.8 MB (11784268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de453593ab8b3ceefaf8d95e35ed8836a37f66dbace8e41451254c44d8f0c8d`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b124115f9efbbfa225774d314331b6efc9cb5a56f0297c3b8a3a232389266b`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1864f2cc4b84a441ce01b9bc21922485dea409990a9b34103b645bd80a06f53`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 90.9 KB (90948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcecd183b72d5159137f34d97a72e00182f405589c991bd975f0f5f998d8f0a0`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:35d6816101ce8f76f0bb8cdfcd919c4655940a119331a86e7031cc025cd18677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e1cc49c57572daa393062465301f86970c1cec84f1d7fbd9df4d0baa233c5c`

```dockerfile
```

-	Layers:
	-	`sha256:c78197de2901716faabbc631b5648a6ca556f3490d2677f1df58ce0ad3ffa0eb`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 3.6 MB (3606518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:842ed29984a6b5bb38a099c5776fce07d0557ca96adf412a06ad3ad9508c1747`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:19ec59ed4b51fae27dd278d0bf11380b21edf2718a14a056b71c205ea984a184
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:e497487cf2720a736bacbaedac3ae2436433d09e6ad0bd8a65c86d41f4d063a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33274380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43de36e1bb01c325b9bcc5b3aa2750460e5d3413af9817fb57aff5043948e09`
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
# Thu, 15 Jan 2026 22:34:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:34:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:34:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c31a1de4315e0b58b79ce211ded98e483a09dfdc7f9a6499a9a7ce21a39391`  
		Last Modified: Thu, 15 Jan 2026 22:34:24 GMT  
		Size: 3.6 MB (3624300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ba782c854a068481cc1d19b2b885bc3941b0f687797867734b959977f68bcb`  
		Last Modified: Thu, 15 Jan 2026 22:34:23 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b50cebc4c825ee52a417c7198f1be150abccfd99fab7124120dc49208d23b3`  
		Last Modified: Thu, 15 Jan 2026 22:34:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4ddc7f4be458215b98db1adbbcdd655a576940b797584f026f194d25aea142`  
		Last Modified: Thu, 15 Jan 2026 22:34:24 GMT  
		Size: 111.2 KB (111235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:25d21931ef63fecca937fa9c226d4b9c972c6a07ab7b12d6cd472e98c2f391b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bf0f83a34f3cf53098c7ebd08efc3892d2749a28113b59f8b7fae1fc13e58c`

```dockerfile
```

-	Layers:
	-	`sha256:11dd9334d128520572ee5d6644d929c8e386a02ca3d2ec2ff0bcf28cf4bda108`  
		Last Modified: Thu, 15 Jan 2026 22:34:24 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07dbb8c42e97f3cbb99e13a0cce5eaeb2908125d20a39eb7a012208555bb6be0`  
		Last Modified: Thu, 15 Jan 2026 22:34:23 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:de8c6e985f8ebfc9f9818ad855d16fa99573bd46e0e9f4dd84d73e19618c9a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31098806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fd5b3ddc77a114383c7ee36112f4540c8891c057f8e7a8cc490ac45e5716fc`
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
# Thu, 15 Jan 2026 22:36:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:36:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:36:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:36:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13a4ea43c440ed4c5c6940006aeb234cf69c04ad0392d10b84fd9766e4a34f8`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 3.6 MB (3602633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae0723c728afe1d94014082337ee6c2c149eac4aa6f8373a264ae6ef9d99e8f`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7101abc79e23d3f25054e865a814a95478cc4e41c4b4ccbee0cc361e535cc37d`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506c3cd39c7b72b92ef079ad69cd3630b8af83c92b6ffe3230be891653be676b`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 110.5 KB (110499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:886473be4217eaa0f6c8744ebd3176ca4d06f19d1a76302fb19c67bd0726beaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468d90fb319d993524a4713f622cc2c3e500cd78f13f40e5551c0563785618fd`

```dockerfile
```

-	Layers:
	-	`sha256:58f1ed8735b4542a9a1bea99b6f344ded0a424a110de890d71fa473bc53b359d`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d01ecd9429deb21559e16c32c9f4e387c8f8033115397f07ceae09f9725024d`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:f8a04f8a8dc04df731f84789fcb71e800edabbf6bb1aebd975bbca1fa8f1c3a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2cd764c7884ab25b110fddde83cf33834467579766c56cb1ab549e9a3ea90470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33274712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc3af720234bde69d207e0f9fdc641e991f2697f3fee5ae0aec4cf34d6223c0`
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
# Thu, 15 Jan 2026 22:34:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:34:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:34:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:28 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b59d1ef943d834ee1a50db8acc83df82aaf8bb732bc303a4d9ac314ca79ada8`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 3.6 MB (3624349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903068be00a686117d5126046cccd885353091e8878694caf04fcdb458f28010`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a7436405aa87ebd15250cc5d262e3a512295411df4ec41ab2b7a149be703da`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09c2a0a07d862cba86e9245a3f5fc8b54ab7bc332077758a597ebd129314c71`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 111.2 KB (111237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb3eba37faf714db0851cc8861baaa63273442a84287700b6607cbf7e50d4d2`  
		Last Modified: Thu, 15 Jan 2026 22:34:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:93e9d3bcff981b6bdaebb3818c9abfdf384cfce638b89d07c9d9da38979e63c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d61845c72e5e377c08f2a586fe8d061339c3f115497261045d09f1c31a2058e`

```dockerfile
```

-	Layers:
	-	`sha256:5fb780292168a3a5dbe5f8ce395b7bf5beb0798a6ebe2dc57020d67f10741c2e`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfd6a705adf1df71c78ac76d86175ef0b0fa0cde1b1b6ec1f5a5a5337153629e`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 16.2 KB (16159 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:741ddf278e88035b94dc004a4c6a12f141ac542d2e852ecc9b064c70994cbadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31099022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9af2062e8549cae074e26beb662b0eb5efc3f3383962c6318a236bb569173e8`
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
# Thu, 15 Jan 2026 22:37:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:37:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:37:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39623f164b7c134bd7c870258397b9ae29b76f658821cd89c872006781773a07`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 3.6 MB (3602582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc84ee017cfa97d082301a68c097692ea26fbf238220f31788ab3777fb0915`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62e658825b155b9da439360822a1b71de7886aa64a9f6b2ed952f31379c285f`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf949af04af6e2380e6e33215d31850a1aaf11a41caf3df6b222373f2d115b`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 110.5 KB (110485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ade6120433a2a5a27b1949103586f6bea98efdfbdcde54a84ec40fc4703e39`  
		Last Modified: Thu, 15 Jan 2026 22:37:15 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2f764bf523306b0471b6acd75e196f3491fa44291dc40435483f27e5d5637037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b21632db7bd9623230cd92a59777549d877ad4ed24e036f4a1ca309c4a29973`

```dockerfile
```

-	Layers:
	-	`sha256:09017ddbca29fb71dcab82dce0807d3653f2cca9f0d865f7a27c96666e61c0b9`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd1544fac022fe23da5e4aa065119ee55176834cec20f0c37704625726caef3`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:9e594df6bac4c9c0c4daa53c980bb4b3a83e3fa0d293167d551e63d718150e45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:da3b9227f84c0e82c2a1cd4cb5e96ec28789730085a1ac4652b6bb91620d43a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59678819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be8b026c74f7c723c4dd8ef3d34903dbf19b1ec0bcfb0356313abfeee3f0d4a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:48:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae41ec031155c98b455bb78067eba48a17546176cae679a09109c6f40044b853`  
		Last Modified: Tue, 03 Feb 2026 02:49:08 GMT  
		Size: 10.3 MB (10292604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c456de52ce89d78c3e11be3ed11cac3ff2a3bbf1b5b7acbcc34864caa6ed1b`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901c3f547274c1b9aba5a4c1dca0de6439e3641e2927b7ff0e29ba10f2598771`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e44b0ddaace5231fb0277c41a8f1dd1b9a803222537517cf5fc0faf0163b35`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 90.4 KB (90356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0af8d1c9f950620612b890e7e6a4d8c5e0b2b9f2e5fdfb0bced7707c0f81c1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a741a8c1833792cc9553aecb085450cdb9f1664685ce094c1941eda5289f656`

```dockerfile
```

-	Layers:
	-	`sha256:e40985eb60787ad8aa5df064ec78906a87d592650d3cb7bd4e4d35fef41aeff0`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 3.6 MB (3614068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c276c637f8dbb8e68f06bb64f124d7e82ae5dde2c17bdf3085ab2d27b05e7a9`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e3fad9231ad143b2ff8fd64aa94fc567d24640473609aa9e53813ba25514dd56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59819618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61bb57dc02b437ffa494706757c4e8012b3ca9dc37c95e0eb0a621d87abe9dcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:51:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22da6bb4121ff52ec24b7b3ca19672a3a6dd5bd671413dade3605ce5d9db5212`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 10.1 MB (10073679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff00c0307437e770f79d7730e90f4fe49614963cc352021322f601722e96861`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8be89556aee6cfbc97cba23e7039718bbfb9e26c495ebeecc6b35befaaca0f`  
		Last Modified: Tue, 03 Feb 2026 02:51:45 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e2e18971c937c3084a9bc87a08e8529f6a4134d0df2863e3a7122cc88202f`  
		Last Modified: Tue, 03 Feb 2026 02:51:45 GMT  
		Size: 91.0 KB (91017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:77bdc7555a73675a432f3ed42bdd322df51878adcfd7f5430a8078b80b1dff39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ee510c4dd9d6ee4305db104fdbbaaaa61cda87948394e49326c32b36e0dda2`

```dockerfile
```

-	Layers:
	-	`sha256:3e9450b0d7b05d40b743a7a02ed1088df21be4b25b167218b0ed71e322282c79`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 3.6 MB (3615595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aaf88d71cb5e6047430224faeccaa93971261590bea6c175d6ab5d6990d57c`  
		Last Modified: Tue, 03 Feb 2026 02:51:45 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:0c07f5e657cc09b86e2e9d42cfe321237c14a5e56f50e8ddfbd4e883d1df05f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61365542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd0e10b4f3310ce286b4442d36b326afc8ee52d43f2fe723ebb88a02ac4ff15`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:50:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:13 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b536877d3c0a030ad79a6593cd07fd6d9d694a4ee908632c85159f47caa880c2`  
		Last Modified: Tue, 03 Feb 2026 01:15:09 GMT  
		Size: 50.8 MB (50805135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8584529105db32472d0fb905ba0ffd3f044b43449f19a931af68cbff933e6f0`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 10.5 MB (10466733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5467fcd76c4951d6cee5b8fea463953e06cbf6b3499279c34eb9e44fe4a41b`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468da32b58b2c95585f26b570d4c00790c123586d464617db5182bb2a4f019bc`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639673e23612c864203b2e3ffc9651b21dbf4b2aa62f36a7a66ecdf0a75bb6a2`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 90.8 KB (90764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3a8babc935e1f8f1e38243dbb223658ef808b3e8c0a544f215cff45d7986f31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8d14de849f297db4adf9be12411a7e0ca06be0469961ec5dea52a603352dcc`

```dockerfile
```

-	Layers:
	-	`sha256:1cff4584330b4a198de56e38439573dd2692d53421016a7605697ac702459b73`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 3.6 MB (3612016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c846b8599cc185520df1fabe5df76ae8f9e4cd8995574b29094363d2157ba84`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:5736c97073ee74f8f16e62030c34d68ea731f86e107e74b0c781593277e9dbb7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:742f81326d6458fc4835788d8fe3317f77b687290629fc738389f12c4814df3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60288474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d9d256c1ca3e4c144c863cc2281316c3cc3eb45088369a88aea3a40a0914ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e5dc831051d738f5c1db4254dde56feb7c9e75e136e23995d896f1b6e1ba752f`  
		Last Modified: Tue, 03 Feb 2026 01:15:47 GMT  
		Size: 48.7 MB (48654703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911d1558a1b3010131d47ee741db0963c889273e31e2a95035fd6cfb9f17c1`  
		Last Modified: Tue, 03 Feb 2026 02:49:21 GMT  
		Size: 11.5 MB (11540410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582397b9dc850b850ffd74061feea99dfb6b237c0192d6191177bd0a6cd86b64`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6309d0a7b6729391c7f1314a74b6b06b07c4646ed52a3d9e7ce4cb11daa5bc`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0740384dd13f89422fe1f4638c08fb758dc33e4f5c9810aa0b1d0a69d7fae0bb`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 90.5 KB (90457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4e1ba3408ddc3dfef56dc25b1915ff61fc917b613ede0a431592467c4b4864a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba3eb40824aca52a92259785bc8cb173186a6bb1ccb406742f34f2f6ebfec74`

```dockerfile
```

-	Layers:
	-	`sha256:7d69e622a5bfed66bf691b20cdf1aa82f53f6f580b821ab40aec94be47d4d4b1`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 3.6 MB (3607661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7e7edca04a0e1aa36eebfdd3e3f3946a1ce7603207a77681ec83592f931e12`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9f8d97f995caee3f00eabda2e5b2e80dda71f89f30a2aa9880a5822d60e61fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60017241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed43c76e582a60593bacd55fe4dcd315ba8213831d318c188385c0990e8cbcc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:51:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:02c386337e70e225c826a0b6295dc937d7a841e7301f60fa7a03adccf75af2ad`  
		Last Modified: Tue, 03 Feb 2026 01:15:52 GMT  
		Size: 48.7 MB (48679232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd35008056e1180ece221c285a1c86c1769a7176cb5d2e594f69e6d206f64ae`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 11.2 MB (11243894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92aab31c07432757e3c05a48406dacbb80522a11812614df8c6a1d9a79a3154`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7f8a8c48aa5f798b4c9dd2715c2e97c069e5446870e61c7604c9e8621078cf`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689f86ee7d710aaf5e5f25e6ab2160a673cbeba10275adc492d11b0573243f78`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 91.2 KB (91207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a6e4e155a78bd1cf49dbc0345cedd63cd782f42ca24d03ebbc9eec6770f30589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a8d05e0e918a47d8eba4c94f215675f9e099ec13d995e05081385ee0a01f8d`

```dockerfile
```

-	Layers:
	-	`sha256:995820befc47d1c55c6cc54493b19e2c17b2821c3c7a7aecd5c807d813f05460`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 3.6 MB (3617199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f93978bff663ff63536a1550e800673779f73f1aa275a88ecc1f1ad05e58bf8c`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:6a90c95db1a2638b60aa36691d3a536024d2108a161f2c5fe47c17d301bb22c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61867005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6f605f6913d479e305f041c7a9b47ccb2ebb97207c2fbb42fd8a3f7c4c3f17`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:50:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5e68504863f049552110bc4132aac67ebf9360a9ca0dd44ced1eb7009b5560a2`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 50.0 MB (49988982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e9787e5aeae5594380d4cbb775abd6fa3ec27c76a2ec4cca5e9405d5336bbb`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 11.8 MB (11784382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b778f855abd2e9eba1fb32ff318ee9e04561d33943ad5ee010c23514f44c7f9b`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b76d608765aa6285fce58e5f3f7c2d318b20960b933cd4f0f96f93b8350f7e`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4740d9cbf74ca39636ca18c075358ca3fc32195250247fc9c8a961bfbd5437c7`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 90.7 KB (90737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1d1e658726c43eec3951bcb02149b6f9ed20f79e8668fbe71937320ed8f4814a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3619476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66420441c356368d62eef101d1964d2aa0a638f7076eb7e63133073408c60356`

```dockerfile
```

-	Layers:
	-	`sha256:960074c60cda9620fb77ba8ba0212d8d0ae309978f421b6147062e8f62cfe20e`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 3.6 MB (3605601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9187b2aaf43c788908a856edf1454a2ea59994c22e7278cf0676b60711104265`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 13.9 KB (13875 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:ba3a5b3b2b48154994a4f7695bc318ef6d6a9549ef04ddaa919ea05049e886f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a34bd5c63c5d4d902f50950efd6ce5dca64b1addf6060d5cb0d1249f0cbee543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60288827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308f8f8e8e8be830f406d62dc791fd094ace9d9714082e5a38b94de80c022113`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:49:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e5dc831051d738f5c1db4254dde56feb7c9e75e136e23995d896f1b6e1ba752f`  
		Last Modified: Tue, 03 Feb 2026 01:15:47 GMT  
		Size: 48.7 MB (48654703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7002f3da964c57bd455c7ea9aea032a614f96ad162a44a4e3be7f438517c9a`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 11.5 MB (11540369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582397b9dc850b850ffd74061feea99dfb6b237c0192d6191177bd0a6cd86b64`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfae06b9f53d369e6035db2bb25acc88db5141f15668b9c187df731a53d6330`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0675e38a13a9ae911bed6a859416965f3afb652c0c0bde63d3aa4b7c256fd8`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 90.4 KB (90432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a622e4dd49c0b33475fbc290bee154d0d2fa0f6b39499fc01581d935969bf0`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e40dd2e539b3db456883132b1b1edd605a481e44ded2b819881cb3566719049d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a040ca843f8191579ffafa4b24724273fd39a8d8db116dbf48cb294a674d25ac`

```dockerfile
```

-	Layers:
	-	`sha256:80d0cd2e330fc9bf7aa1ae15a2864ea8ed86232bb2bdabd6bdfc79ab09150396`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 3.6 MB (3607697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44da38342d0de406e284f67ea9541752f7cdaec248b21cc9996fbba57ab3770`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d73b7d2e2e9a0ad75e6d8f2f202ac45c5c90804f7fd491f04759f8c9ab560ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60017503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55231f6fa6a70347e96f433340baac503f1e0bc79c0414cf4e2cd569707fe81`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:51:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:02c386337e70e225c826a0b6295dc937d7a841e7301f60fa7a03adccf75af2ad`  
		Last Modified: Tue, 03 Feb 2026 01:15:52 GMT  
		Size: 48.7 MB (48679232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72169edcd3114aed53fcfb33bb985a27c25f0be4ce0b90c7ee3b2602e511eb55`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 11.2 MB (11243763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aa6d785888f0c8b41e2b5e14ac04e5cd32dc32e062cef01e52dd756c1b6029`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388b2d36400e3f10c42b37febaa865685b8cea7dfdad772bb4cb4648074b6df6`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c459f79798bb027f6a4cf0b4a000a6cce488b3b3163fe0705ab4981141f549`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 91.2 KB (91186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4117407e6309b71a85ba30e66e465b94f6a37a79cf55f9f2c9dce60d28096c`  
		Last Modified: Tue, 03 Feb 2026 02:52:01 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1130f85f99e63a69789b6108372d5894b1d29ab420ebaf59267e41ca7a6562ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde2abd89ee4f4696f8234059b1d01413d7e73a51ec67b0f521b58b71cd0cab6`

```dockerfile
```

-	Layers:
	-	`sha256:fe2137c73c306d7eb945a76ae5920f36787323e1cb8075c3895577f467340eb2`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 3.6 MB (3617235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:375c5dbafd2c21265776eed0de1841a836200f05b1e2f050c3ded17494a3b686`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 16.1 KB (16070 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:09d2a82a7755f31bdc924260b1004d9e18f89b53e70681bf9f52e5d7c38265b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61867112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e26265fed5bec7a6be142173b02f16f7dc8000655ce83cfeb5f076665d6436`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:50:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5e68504863f049552110bc4132aac67ebf9360a9ca0dd44ced1eb7009b5560a2`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 50.0 MB (49988982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4b67206060b17bfa3f7c139d34dc7edde12328d9c0813401b6e218eeb526c2`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 11.8 MB (11784066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12563f627f2b777c32fad8fe06dc8a81cc93f797fecbcabcdd16f1a26568ac2c`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65b76f0d68fd4c718faf7b6a1dc01fe7c5addcba58f6273fab12fa8a150f330`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af106d4cc2812bb0918ebbd81516dad845621128fb2918143205c8255f2683f5`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 90.7 KB (90739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894703054bb720e327a2e8882bc8458ade09a154ae2005401bc22f71b7dbb7c`  
		Last Modified: Tue, 03 Feb 2026 02:50:52 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f3e41fe08d7abe4d29d2ffc0de45275ed7b5ca3b8280228247ca7c0828af736e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08921bcb04326e7d1d3cd578e21a03f61ee55fbb62ab7c207503b48aa6a75322`

```dockerfile
```

-	Layers:
	-	`sha256:7a558ce5ffa36aad5b5023dcfa30033ae66b7efd72b87f4fe8ab2ee6c15257b4`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 3.6 MB (3605637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdc2c6ad005dcf4f986126d621753f79ca7d6682cde71dab23e896c5930c544f`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 15.9 KB (15900 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:885ab45ebd96b8c8a149ab0916f3bea94054a593cdce6a6f2d8c4ba09aa27396
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:4ecd9d1443e75181863e1b0a0427e8661fe92478615af709b630787153110c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03739d2be3885eea98c095c9c74a10e89108d70ea5b2d847b8bd4eff7a14a21`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:48:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5012d8636e02354fc754917a5033735462dd0859681a109ccc1d487ff5a0cbf`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 11.1 MB (11103507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958c347c1e407c069a4d2260fef1c8c469021a6e69859e324c4cc80a7ec71c79`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35c37d32450eca29c1869c861c8b6211f487e8459cb481d58bb785e689ccb2c`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59abc559ead350f7d45163c15a158239544ac872d73e287e28c62ec5d8d18573`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 101.5 KB (101459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:280100744d6de918a33f4507f434ad023c0711e4c6788351c5d3f00bb1fd15ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d5313ade697365c5833199af043d3c89e529d7424c8c2b152a0eebacb9eba8`

```dockerfile
```

-	Layers:
	-	`sha256:f1be9831e14fae35c899ab4f09a3310194c3a382bf28babcc9d58c730aced7a8`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ef553d164e1c42152cdab3a581c5a74ff6db0a28b1ed04399d3942e993e238`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:86cfc34b840820a8fe84956bd371e6199e13e4a058829457a6e7744cfb8360b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63471602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdfa29e52ee39c97a34b1b1c90fffba3941ae1c1e71e4e54a3e48a5236e115e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:51:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:02 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58879c86c59c7df27e0a73b9871db9be284e7b8f556d768ce7fb3fb480f9e206`  
		Last Modified: Tue, 03 Feb 2026 02:51:16 GMT  
		Size: 11.1 MB (11109967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314e0f97e0b03075b4d990a2ed9fa571367773fa25893b53abe071aa0e8346f2`  
		Last Modified: Tue, 03 Feb 2026 02:51:16 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8939451b05ca684069c3474313ac5ddda1d805d5d47d1b6ace08e474d7abe43`  
		Last Modified: Tue, 03 Feb 2026 02:51:16 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8a02c619f5296c2e4f4af6c7934197573f843edfbe6c9b93209815263bad23`  
		Last Modified: Tue, 03 Feb 2026 02:51:16 GMT  
		Size: 101.2 KB (101156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a1a848719d7d0597021427147569793781f7c99ac283ce53c9c16f2e77d67198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f878a4517c2277fbb3ec9fa17526aaca27b8d1c6d2c7cf68308cb2923b7d000`

```dockerfile
```

-	Layers:
	-	`sha256:3df4a4551a3a59bfc804f8866169620df0c3f66ce55aa2651d987ade9193fedd`  
		Last Modified: Tue, 03 Feb 2026 02:51:16 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b266db82fea3e86e4d5da2f69f0bba092bc90388911a1a0a784b3049371303c7`  
		Last Modified: Tue, 03 Feb 2026 02:51:16 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:1354f1ba7aa85b916ee958170cc7f050521000edc06c0220ab0cf6973176f09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66305210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4da1f09e5d913306d7d286ac599b7b695e8ea981b3a1e5b82766088cdf3209a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:50:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f6d70808fcfec5fc2c45e150a669aa79950bfd30968e7ba0de2c962cff56fc33`  
		Last Modified: Tue, 03 Feb 2026 01:13:58 GMT  
		Size: 54.7 MB (54699582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9765b7cdc157a2219f748b055e54b374ab46c88982ba130b80275b5ecbb6fcd0`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 11.5 MB (11502195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6922f2485c8fd18c9ee31feb2a1e54e28e70fbad4799bb50222116212c3ddd76`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1a7b780248edd8b5c2395aed2fd482edddda39a73f74ed0809c302882cd079`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3b0d8566f41d7aec87b6b984dc4efeb7f44430c851566e02f98bf290d961bc`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 101.3 KB (101277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8af366ff88aa6538a80fc1c5bcaf92a68758fa13237a31ef1c7869480bdab3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c649e84a44d41ec14a3f312f22561643cb8e92c41a625c7460cb1e8b576c6cd`

```dockerfile
```

-	Layers:
	-	`sha256:f6f7876a1fa47fff70e97fa7f5bc6879aaf558a242b44885694bf41fd8a52b49`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93bb6ee6d764fe93e3d6a5da1a083ac6a14962c64a50b3b1e7c6aaa9f29c9629`  
		Last Modified: Tue, 03 Feb 2026 02:50:14 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:77194295cf5f5eaaad2c4923d519cba7c14716b51a98a35f4e82a7cff61e4243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c6fe056761bf624c48323aa68b1a0f5d713c4d0b61832e061ca1ea7ecda933c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21627ce4e7ec3d7e88f1abe7fa4bc41c147db83695ed04258bda3a7b6dc4445b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:48:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:32 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:35 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1d633e2bc91aea90973516b45752d540db2ea3cedbfabefc881c030ae1e19f`  
		Last Modified: Tue, 03 Feb 2026 02:48:45 GMT  
		Size: 11.1 MB (11103524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c5bcd939835f01a3b851bb6cd334c3fdaceae44dc5ad0b2ff9983495d88ad0`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0cc5228ca7eca77a2a40283d1d9ae0330aa87b2d01ff8cf386e2e04e296e29`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b465d2202f2a38722e786a7c0e5bd9671a551c9ebbcc46d3929a4bce2970a3`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 101.4 KB (101429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9cdf47e555c97d954a83f3afa5500cf5b0c917f7db57b2737a13e136b200a8`  
		Last Modified: Tue, 03 Feb 2026 02:48:45 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fff433a0c16911f96bb25b6fb337a61b0a4c392e54d963c253c382e94f961fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6144505b81e88e04ceec7346c279a36e30e6c8747e2c29b4a53bcccf0a4224`

```dockerfile
```

-	Layers:
	-	`sha256:83904257f196bddf92b45b7631562668036000f57c2d47b653b38066e4e63f45`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf75af788ef139571dc1aa51a678c8b24d5627b132e55c158d9d084f744edd4e`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2e3447d7574d73923eee873cfe9c4fd867860560a331d24a796d44afbf56f4dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63471688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7af8b4f564086a1bd49480d1a6447df23ef006de28ac8dc3a7957f9c3645fbb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:51:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca39f502305b0c1bb375baecb8b56080c0991ad9fcc2e55ead25e0e3ba8b605`  
		Last Modified: Tue, 03 Feb 2026 02:51:21 GMT  
		Size: 11.1 MB (11109715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22aa437d699f198f3f9813d737b57370795c888aed4b7e381da936681d2844f9`  
		Last Modified: Tue, 03 Feb 2026 02:51:21 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8af9c45551b8fe56d8931700d67d1898765bf48ff4fc0a841fcef4022fd91e`  
		Last Modified: Tue, 03 Feb 2026 02:51:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d9ba681f82005822c01d2a02aa6bbbc2f0c4e74e910ed45365de4a5d91aa7`  
		Last Modified: Tue, 03 Feb 2026 02:51:21 GMT  
		Size: 101.1 KB (101108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a674ac10c9220b624e0ff4c35168ff1dbaba397cbce00f24887b33295cc9734`  
		Last Modified: Tue, 03 Feb 2026 02:51:22 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:46c11994357bb45b93289a8ab73043cfef60e892ecc08e61df264f12f61755ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af38135cb49d019d049c5c688c37bdf8cce80c7f48f4bb60962094f2d6e3669`

```dockerfile
```

-	Layers:
	-	`sha256:28f9c55cbf2f619573983902d942b6239ff8a851047c1b98418bb2c718901fdb`  
		Last Modified: Tue, 03 Feb 2026 02:51:21 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99deaae6542b3b7ebda4bc486334410dafdd2c554f530e8f6b3961b0b8ef2166`  
		Last Modified: Tue, 03 Feb 2026 02:51:21 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:08b312b3fe28f63548e1c157cfbf5bfd51baa274c71c6fb170097708022c7057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66305759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa07c637ab99777fbe8867c39480e039f706dee25ae6f758cbef8a47483d487`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:50:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f6d70808fcfec5fc2c45e150a669aa79950bfd30968e7ba0de2c962cff56fc33`  
		Last Modified: Tue, 03 Feb 2026 01:13:58 GMT  
		Size: 54.7 MB (54699582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664978e2ab7548b095db8bbf8dbd5af37114ce8462bb64e43a6c661837548a96`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 11.5 MB (11502354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a712b3803ebc860aac4c28daea93cb3141b2973ebeb843c9a85897d924831ef`  
		Last Modified: Tue, 03 Feb 2026 02:50:21 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2dea87f7cb441a246f0ff27aba64c9e2587db205a062d183d9ea534f7800cf5`  
		Last Modified: Tue, 03 Feb 2026 02:50:21 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187883a3231287ee0e5fc6ae4b66e97e5c3496ec4439202d8f5533c6915c9c39`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 101.3 KB (101281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a50d37cc3aca1dd7b883e568ddf0ea92b1274b3d68e294b5f0c780939275010`  
		Last Modified: Tue, 03 Feb 2026 02:50:23 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:799acc823b45de4ec480828b3518a7b8dcaf3571218225b105f1dce2331bd076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad48092ed58e67c71d2c73d1b255420a060ffa4b699e3502f7827418dbec4b7e`

```dockerfile
```

-	Layers:
	-	`sha256:ebdad496ad0a1912aada804329d687f8a8a79114d956aa14c80b300ceb666a60`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7913432ee7aa90d184c5cd7aeedc2fe42e140b06b4f14393bc2272604efefdac`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:f1b4f2ecb2536ed462000f6c9038959182e67d622eef44c5ea0ff7bfaf7e509d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120` - linux; amd64

```console
$ docker pull neurodebian@sha256:c1242f1ae926b10fac848bae44a495dccd66a1f230b6b7fed29b1f6a0d61b415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90ffe9ae6a0219a6a9bb417e0807677106ca2fdd75bfa7c85c32f6b7b19a61d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:48:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:42 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2076e118117aaae08d4043f950fcfaf533cbf38d422320c2d3e4e79fd1cb42e0`  
		Last Modified: Tue, 03 Feb 2026 02:48:56 GMT  
		Size: 11.3 MB (11273502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adaf593435563a325b4e351870a254d93ace4a6f6e07a0076246d00cb5465a4`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9b8967af24b7aecf27b7cce202956704c3b50f82c4085ecce2a9a7160bd959`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b33b63666fc4fd13332f7b20b6bdbe9ca7b0a7ffa3038bb9e9fff447c9777c9`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 93.4 KB (93407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a0d1ebd5434d67fae166a6c83a948abf5b042772ba034630f0f2f66f59f73ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19eff2aa6afd5c085e13f1a2dd7f58dc001e6100f286fe390bd5ba170a02014`

```dockerfile
```

-	Layers:
	-	`sha256:c8bca7e18d0064b9ef958dc8aca15d79c44717eef437552691266c3fc08cb082`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cca950dd7c438bcf4a08ac81d7d99a6ee39835a490ee62f3eb322f3b651ec73`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a825b8dfeaffd1bc173ea5d15af02b32c121fd426067bd93de21c9b0b8473829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59714558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf967e7a2b8332edc2032368cd4cc76c09f252bda502d5584cc30e62e93e6a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:51:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3266c9acb92d5ab093d574343ae67394c8340ee57dc673ee80e32d4b1febb73a`  
		Last Modified: Tue, 03 Feb 2026 02:51:20 GMT  
		Size: 11.3 MB (11252882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90ad8a19b89b650fc2ae655f9f1ba6c4c33a4e78bc900ba4787b3ce4f3624c1`  
		Last Modified: Tue, 03 Feb 2026 02:51:20 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5340c77e8e063fecb5791e93211158603333e1e95fc58c0e803d4697821562bc`  
		Last Modified: Tue, 03 Feb 2026 02:51:20 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb9296d3cf1afb97b856e1075f492c18b57ebb73ff639fff0a950dc633cd3cf`  
		Last Modified: Tue, 03 Feb 2026 02:51:20 GMT  
		Size: 93.5 KB (93542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c058d45c29b4cf6c2565081f5987d5732793cc8f0d5446d9130f693c0b53247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88347108f9cb3045f3960417a1bd87b0861f0802d052f3ef8831338ce86b01b9`

```dockerfile
```

-	Layers:
	-	`sha256:c141eb8ef0ef7d5dff7d7bef9f987bd457984435ab33077b3a20f40904fd3eb0`  
		Last Modified: Tue, 03 Feb 2026 02:51:20 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41cc2cd7208471c68a447348e06615156161dbbca540a71502a9b494919699c7`  
		Last Modified: Tue, 03 Feb 2026 02:51:20 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:a4c2d54476a243c1e3446744e1ba1c2214cabef3820e37dc8c8904eb4552582a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61257022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820b2ad9ffd6327a389770a6137a17652f679fe852b86fe63e2627c9ad9555bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:50:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:11 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a7f977a794a5fd56ece19f51541cec3b8ba447f10234ab001213bf850f92f64d`  
		Last Modified: Tue, 03 Feb 2026 01:13:34 GMT  
		Size: 49.5 MB (49468454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26b7baeabeade531ef7f9c1e90bb83ec231559000bcb172a3d42c9c52a13581`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 11.7 MB (11692965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545298cfcb2c0ef599758efa0bb2433ddba17671129a91b2f81d0f8c01de360e`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e3e586f3ba7f832374d99d5f3c2ebebe5198e3591951ded0a25f8016be0c57`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ffda1436e97be251fe611d4411ad207185b88106b305a875a268f22d2e54d3`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 93.4 KB (93425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:975c1b6232f112b4d91d722d790f9635ed313933a851013d7ba1e0be636dc6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2eb365ca11e1109453dd15f2b465da21f8daa56c23b3a6952c3d6b42ee61a5`

```dockerfile
```

-	Layers:
	-	`sha256:7fcf231778ddaf83b1d3e91394058200a344269891e8a9b9be1404a47eb9c669`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 4.1 MB (4073846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e067cfdbb37f564eb7ac8e086244b1a9fe445646b82fa379028478e6ff88f9eb`  
		Last Modified: Tue, 03 Feb 2026 02:50:22 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:b854e40c7710fcc1176cc13e0c671a175266e060f49c78fdcdd8392eb6145496
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e89cb8491347c3793299b4609dc9f486e374e7e6b3871024cdaa52a242e8f889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea60233cd27143f98be7c617d34a2b7abccc6ff2aabcc29751782a270e795b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:48:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:49 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c45697feb00d0b63cd7fac2b980d8cb335c36bdc7ec19133c10ac21ea5e36fd`  
		Last Modified: Tue, 03 Feb 2026 02:48:58 GMT  
		Size: 11.3 MB (11273436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bba6c203b9ebf4afc38346aebc78ede9b2b21c6744a3a63f7fd29c95bbec92`  
		Last Modified: Tue, 03 Feb 2026 02:48:57 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71877ab4d7a4f26899206a9f324de43293a354660fed1fd6bbc7313294974b4`  
		Last Modified: Tue, 03 Feb 2026 02:48:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4479e797285f1f997594e3d4cf6214b8c6d464e7fafd77f8344aa65ae6180541`  
		Last Modified: Tue, 03 Feb 2026 02:48:57 GMT  
		Size: 93.4 KB (93380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769627860e6b9788b55ff0f269633177f23ea77468d5f7e497b9b2a68e432c98`  
		Last Modified: Tue, 03 Feb 2026 02:48:58 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1aca7321e3f7be0a4a173952cd6e7d2f376d911b90eda28aed731f8858aa437a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5604db43735de04e2a0de391c3b42da87fa2823aa41080a13383d7db4ed34d7`

```dockerfile
```

-	Layers:
	-	`sha256:e014afc086f73ae28b94d4c5f55d120bf2c935b26fe4bfc6e4841a31381aeba3`  
		Last Modified: Tue, 03 Feb 2026 02:48:57 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c58749e130661407c54b4f05e54b5e92070583915549b6dca5ee525921770f`  
		Last Modified: Tue, 03 Feb 2026 02:48:57 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e599ff7d96b232003874e2d68d248e8639ab13b311cc9c72d10ed0c88d60d16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59715134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fc55d172f895c9096019f144d0bdf0d4b3370e77a142a82b35256615baff23`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:51:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b68f8edacfdf5365bc59762f6e137b3cb4a57dcef4e8f3d8676326d25cfa7e`  
		Last Modified: Tue, 03 Feb 2026 02:51:56 GMT  
		Size: 11.3 MB (11252963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440f4b13f161e074886ad5cb9584c84f836571ad61d9d2b6694228d25e2f5849`  
		Last Modified: Tue, 03 Feb 2026 02:51:55 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1065c34065e9ea4961334cc417397a9203ead63b9b4add9a6c8125098a9e88cf`  
		Last Modified: Tue, 03 Feb 2026 02:51:55 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d2be16ad111846291203cf7e0ed1c0f46a1da47bcb6ed7ed03a702b0754d33`  
		Last Modified: Tue, 03 Feb 2026 02:51:55 GMT  
		Size: 93.6 KB (93589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b974cb7e1d873a1873954b5d412eea6edd026a6228509fd17c719d1712ee7c`  
		Last Modified: Tue, 03 Feb 2026 02:51:56 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e2dcc4eaad8355f1791200cfbb013339bd40f1bda315125585515d6896a729dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a491c7a3eba1c7c25d91299811e639e01eaaea5b257f1baa80d29cdfacbc393`

```dockerfile
```

-	Layers:
	-	`sha256:b7a85c747dd7d17a5b5f7274e409a93b2074eeb2832567d114126adca088aa50`  
		Last Modified: Tue, 03 Feb 2026 02:51:56 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c563d6ce14f0efda1477101a2fac4ae3fb9f7ba0005edf2c6dbb99e7c350d92`  
		Last Modified: Tue, 03 Feb 2026 02:51:55 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:15c4fd7f4ae69dda15f010fe14f030228c0ec31df32eee923704fad6a66840f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61257438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611853ff5e7b7314aea5f6ecb0764d406f9482ab9a27ba2f0573f193147239ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:50:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:15 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a7f977a794a5fd56ece19f51541cec3b8ba447f10234ab001213bf850f92f64d`  
		Last Modified: Tue, 03 Feb 2026 01:13:34 GMT  
		Size: 49.5 MB (49468454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de10e295966a7e5139d07603a07981adef413a49af2017977a73771b0cb96116`  
		Last Modified: Tue, 03 Feb 2026 02:50:23 GMT  
		Size: 11.7 MB (11692927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899d3418df53b95a5eea13aa82e46a5f3b5129543401d1b47e0fa907fe96c7e2`  
		Last Modified: Tue, 03 Feb 2026 02:50:23 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061c713a7d20c03075ab7e707af26fbdee5d96e664024b10389d9b5bfe835c14`  
		Last Modified: Tue, 03 Feb 2026 02:50:23 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63abd2041f6dec416c3b3c0d53b05dc4b3d3563f2ab10a125135e7823fda57dc`  
		Last Modified: Tue, 03 Feb 2026 02:50:23 GMT  
		Size: 93.4 KB (93427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5248525f02ee083731f715c3859b5c4e5db3b48374f0469bf8c31c5bea0e7221`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:60fdbaee666240a3d2a3f5922e3b34a11fa6676451f909ba37d55858eeb6beec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d09d36dd5eee401ff246b91d94ebc3509c6067b37f8f0078fc2543d58a573f`

```dockerfile
```

-	Layers:
	-	`sha256:5082655454d356bead422988875229dc0c780bc132a607d4ad0b39323d1271a7`  
		Last Modified: Tue, 03 Feb 2026 02:50:23 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd67c4b2a9465922f45d2d9498654a70dbf46d43a1b1379d4fb11911aea99389`  
		Last Modified: Tue, 03 Feb 2026 02:50:23 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:9e594df6bac4c9c0c4daa53c980bb4b3a83e3fa0d293167d551e63d718150e45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130` - linux; amd64

```console
$ docker pull neurodebian@sha256:da3b9227f84c0e82c2a1cd4cb5e96ec28789730085a1ac4652b6bb91620d43a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59678819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be8b026c74f7c723c4dd8ef3d34903dbf19b1ec0bcfb0356313abfeee3f0d4a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:48:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae41ec031155c98b455bb78067eba48a17546176cae679a09109c6f40044b853`  
		Last Modified: Tue, 03 Feb 2026 02:49:08 GMT  
		Size: 10.3 MB (10292604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c456de52ce89d78c3e11be3ed11cac3ff2a3bbf1b5b7acbcc34864caa6ed1b`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901c3f547274c1b9aba5a4c1dca0de6439e3641e2927b7ff0e29ba10f2598771`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e44b0ddaace5231fb0277c41a8f1dd1b9a803222537517cf5fc0faf0163b35`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 90.4 KB (90356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0af8d1c9f950620612b890e7e6a4d8c5e0b2b9f2e5fdfb0bced7707c0f81c1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a741a8c1833792cc9553aecb085450cdb9f1664685ce094c1941eda5289f656`

```dockerfile
```

-	Layers:
	-	`sha256:e40985eb60787ad8aa5df064ec78906a87d592650d3cb7bd4e4d35fef41aeff0`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 3.6 MB (3614068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c276c637f8dbb8e68f06bb64f124d7e82ae5dde2c17bdf3085ab2d27b05e7a9`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e3fad9231ad143b2ff8fd64aa94fc567d24640473609aa9e53813ba25514dd56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59819618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61bb57dc02b437ffa494706757c4e8012b3ca9dc37c95e0eb0a621d87abe9dcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:51:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22da6bb4121ff52ec24b7b3ca19672a3a6dd5bd671413dade3605ce5d9db5212`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 10.1 MB (10073679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff00c0307437e770f79d7730e90f4fe49614963cc352021322f601722e96861`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8be89556aee6cfbc97cba23e7039718bbfb9e26c495ebeecc6b35befaaca0f`  
		Last Modified: Tue, 03 Feb 2026 02:51:45 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e2e18971c937c3084a9bc87a08e8529f6a4134d0df2863e3a7122cc88202f`  
		Last Modified: Tue, 03 Feb 2026 02:51:45 GMT  
		Size: 91.0 KB (91017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:77bdc7555a73675a432f3ed42bdd322df51878adcfd7f5430a8078b80b1dff39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ee510c4dd9d6ee4305db104fdbbaaaa61cda87948394e49326c32b36e0dda2`

```dockerfile
```

-	Layers:
	-	`sha256:3e9450b0d7b05d40b743a7a02ed1088df21be4b25b167218b0ed71e322282c79`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 3.6 MB (3615595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aaf88d71cb5e6047430224faeccaa93971261590bea6c175d6ab5d6990d57c`  
		Last Modified: Tue, 03 Feb 2026 02:51:45 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:0c07f5e657cc09b86e2e9d42cfe321237c14a5e56f50e8ddfbd4e883d1df05f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61365542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd0e10b4f3310ce286b4442d36b326afc8ee52d43f2fe723ebb88a02ac4ff15`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:50:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:13 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b536877d3c0a030ad79a6593cd07fd6d9d694a4ee908632c85159f47caa880c2`  
		Last Modified: Tue, 03 Feb 2026 01:15:09 GMT  
		Size: 50.8 MB (50805135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8584529105db32472d0fb905ba0ffd3f044b43449f19a931af68cbff933e6f0`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 10.5 MB (10466733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5467fcd76c4951d6cee5b8fea463953e06cbf6b3499279c34eb9e44fe4a41b`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468da32b58b2c95585f26b570d4c00790c123586d464617db5182bb2a4f019bc`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639673e23612c864203b2e3ffc9651b21dbf4b2aa62f36a7a66ecdf0a75bb6a2`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 90.8 KB (90764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3a8babc935e1f8f1e38243dbb223658ef808b3e8c0a544f215cff45d7986f31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8d14de849f297db4adf9be12411a7e0ca06be0469961ec5dea52a603352dcc`

```dockerfile
```

-	Layers:
	-	`sha256:1cff4584330b4a198de56e38439573dd2692d53421016a7605697ac702459b73`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 3.6 MB (3612016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c846b8599cc185520df1fabe5df76ae8f9e4cd8995574b29094363d2157ba84`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:006ddee33bc319d072a14cc4d994bc2ecabbee1b0945976e1df7658fb4255fed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bfe6f18aa6a74c90c1bef54a8ecbfd1554d462da56f4431077902cee7e35743f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59679073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1734174826d480fd0ca4221a27524fe98e871a54a19c068307ec6b8d151189d5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f763d27f0cca3eca63d032df25da1781edc10ad21bb6ec6472a87765b5d494`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 10.3 MB (10292413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2193d3bb29390a43b5fe3cf6ef36f5d049269591f33a3f65f1c3ebf33ea628`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f82edf0cab6319880f6003cb047a9679b2b534d136feeba495550f279df6cb9`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae03b3a868a98138feda4a04a1f015e865a3599f8231275cde4e2d3ab18157`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 90.4 KB (90354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4f2df40ce739fcaf54c09cdf8f844f97b7b89ddd3a009cf66056798e7a816d`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73fbf95673c18f9bfa0a30481eb45b538fec3995c608702a1c1d90e08da42446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9f83b2f6643450c6e9f512971c820c8345c704dcd2e8cc7a8756a02e736f86`

```dockerfile
```

-	Layers:
	-	`sha256:6c76910ec532300ba0ac33261e0fa300df86a2a7236c44063bcf717e3999b372`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 3.6 MB (3614108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48dd7f90c47288d683499a84f5abe7001a411496c218e1bd8e77b25b0888176`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4c13946a073d0e0d9f2340b836b54e9a9dba1f010f04df5dd200dbc7b1b5af23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59820236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c689286b6669d33d79af74959237011ecd70075c64056e24a6d02c270876d1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:51:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba456ea91fba33b0b2266f0965cf72ec30eb7f1d6c06aa2a1c64acb11287462c`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 10.1 MB (10073826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c8707cbc6b46ef363481729ebc07a939af077bb4b56fc62ac5a4ff2270d3b2`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba3130f7897eb800b59a9393f231600424ff257e4f3e7b2648b3541566c64df`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbc4bfaf80cebb772173dc6b7ebf4d6c65aa74b8a1100448ee711a7b11f0f2e`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 91.0 KB (91037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60db51e8517172f9d697f6dd3dfd52ed53bc5d6102dfde87d9d7b154e3f0f1ac`  
		Last Modified: Tue, 03 Feb 2026 02:51:47 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a0bb841aee3fa661b5cf22150ac560131f548d1e2f6de469929472a1cae8d039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad53c32ccedf0d4c008cbe8f0cc3fa2f71fa4b95414674e681a85c5e5b8f37c4`

```dockerfile
```

-	Layers:
	-	`sha256:130d559f8c021baf79e6466c9df7613170e752a7e5cd42a30367c9f470ca7e5d`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 3.6 MB (3615635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349032d3fccfe1a4b3f53e519f7c3f349aaa60303d81e595a5a2f73a422d2b63`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1b7cc3e8e887276f4b47a7a7f3fdb6a9d8ccad482d37c05d554655857987d25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61365948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a8a124a6dc9a583795fdffe09999ff8fe4b6724e1f73ee53a9cc663d7baf26`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:50:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b536877d3c0a030ad79a6593cd07fd6d9d694a4ee908632c85159f47caa880c2`  
		Last Modified: Tue, 03 Feb 2026 01:15:09 GMT  
		Size: 50.8 MB (50805135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151531fafaa44052b8ef62edab30c39e82df6362c327e633a87856cab112f38b`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 10.5 MB (10466690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c46322ddba400bbf437e7982be185466ac3a30b6c3e18306fb107df084ef6f`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2601d6950df113d96bbe256462649bc0356027670c0fdeeea1a36db50b8070d6`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbc29155f72161458e612a5e0f3deefd8c0b90f6c6b725d755d6cbb64fdaeb3`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 90.8 KB (90767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a58325440b9ddaee417a935c1ba847b99eca4326d8cbc0cfb83ad3ec4e62d6c`  
		Last Modified: Tue, 03 Feb 2026 02:50:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1a1c6b5b1309c9a6d397be72aec7d51df19e72b1ed14d8e559ddaac54b8d45a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834635029b6ce5298f9a745d504c4600d908f105eebe44ef56cca8eff573a1f3`

```dockerfile
```

-	Layers:
	-	`sha256:baf157ba5397d5cc0efb14f1b4af8b0e255ff3dcd41813d3551db6e42c9b6e1e`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 3.6 MB (3612056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190165ca7a14affd0179a3d6aa5c67852f9eccbb4f971c73979a03c8629c2d97`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140`

```console
$ docker pull neurodebian@sha256:e60e70dd2ecc36918ee4ef7a12501e9a8c5aa4238ec448c3ab89f0565356a8db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd140` - linux; amd64

```console
$ docker pull neurodebian@sha256:62557098c459de418b2e59e2e0374ded8453839c8dc8a8a635e934e25b272fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60289672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e09429446df5077bffdd30968e77332ee3dbad06f3b3bea0d5d4e95d262872`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:49:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e7ee730174f13176a4a2ca706f251743bedcb5459da1b8f275d5b6bcc67c0aef`  
		Last Modified: Tue, 03 Feb 2026 01:14:19 GMT  
		Size: 48.7 MB (48655735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2730c822ebcac3a15d3d766e879e3429b4f9adf6fe76271ccfc76c249537f502`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 11.5 MB (11540381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1930f996b21f85d26d813979c448b5cc33d9133a8314e6eec99d3e973f6035c`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2a47c885c79a443813591c82a08a80cadd63adef2c8d39f9547d22badfcacb`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc7445e516a5d581aed9ea2f12b0eaeed7fb0988a1b7763124e12ff75af87a`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 90.6 KB (90648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6aed34d51bd5ea07823221ec742d4e2d9232789220b79efe8f13368675e3040f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3787c78d5c00b60dd7bf2b7563d0ab9a1f311b1efe8e20720192ef75f7123075`

```dockerfile
```

-	Layers:
	-	`sha256:5b86a2fd5679538630a28183b3b3ba91097d7d8705bb17616d47cf9348996af0`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 3.6 MB (3608543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d480378322cf7188821388658920d0bdc152a426690dd4aca8e70b9eb5cd12aa`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c3c2279dfef5b1dc5801320cca47e07527c809bfd5b8501e47a54886d752e589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60016699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5303416cf8c75cf18340519a6abdb2c2603976b0e99f7947a44a4386905605d9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:51:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2309f92dd0c61c985b2d0f865b8d146291a99f7a179b5a243da4f72d2cb33817`  
		Last Modified: Tue, 03 Feb 2026 01:14:24 GMT  
		Size: 48.7 MB (48678525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe9791138d0a57aaca050f57b565887e667f14821c8231f93c2d0c305c7e471`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 11.2 MB (11243891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c0a9f59ed57dde67760c8b95b1ac9a6e2b6a87a29f3ffe1bb31f968cf15933`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e2416924c6e88fd98b2ecc7ba1069de6c6c9b1579c057f3ace4d1ce181bb26`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb4e195e6cd71c46f9c6a5642063ca9d7395067cbc82cec1f6c0c133adfd0a4`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 91.4 KB (91373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e16860a4e030141224640806bb45d2e39341e64caea29bc7a7b88081583ec337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84bfffc9dcc54d9ba58efca740fba1097bfef5a19b1896c56713736816def4dd`

```dockerfile
```

-	Layers:
	-	`sha256:172889f9237c9e8233f219895f1fe9b57a489f5bd8800559fb0fa2feda3cf7ab`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 3.6 MB (3618081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76cc10f725eb0b8fd8134c1c72a383f9d97018377dc013bed07e8ea5d26e62ec`  
		Last Modified: Tue, 03 Feb 2026 02:51:48 GMT  
		Size: 14.1 KB (14056 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; 386

```console
$ docker pull neurodebian@sha256:372715dd9d593229a9937c8e98543f99da9162df29c92ca6eac1f1fc5ab78228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61860090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670a3c8d8684fcd47ddc6995df4f4337300ec88be2777020a509d2a71a2a36fc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:50:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:38 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bd6304d6e56f66e13385dc7464436c6e3933118a9e5b697acc2b57e9b6d5e5cc`  
		Last Modified: Tue, 03 Feb 2026 01:14:23 GMT  
		Size: 50.0 MB (49981936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b0e91a2c7873b83c48aa15d9575016025f65009bb2a2697185fc7c1cb3258a`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 11.8 MB (11784286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b778f855abd2e9eba1fb32ff318ee9e04561d33943ad5ee010c23514f44c7f9b`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b124115f9efbbfa225774d314331b6efc9cb5a56f0297c3b8a3a232389266b`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b21d5c5dbc2b33cca4880d981b958ba838908e34a46b81d62441314a5465015`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 91.0 KB (90964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:adb60bd7608494b5e43c5616cf74a0c141d1c97857da108077e02b9a48877c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3620386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62470d32ade636f2b7255e3643887b7193c4ef781667ece2d405e4c84592332b`

```dockerfile
```

-	Layers:
	-	`sha256:5d9a2f5cdcd0a0287877961e006e91a56b955f9e17dcbfc60d768d2544743d64`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 3.6 MB (3606482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f6368f043ceb8e4c5ed5e1a65f2c65f04f6fe87b106c5b112dc5c93161a9a7`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:0f18bc1f784f10280a845619e4cb21c545b4bedff88df1e685f5404a23735f3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd140-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a163bb449af86570efbb2c848f4a56b0a9f75e2c9bab460fac75b282e0ee9659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60290217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ebf1e005f416f00f58c9265e914c41d744ca6aa1cfbeee885ba91c67104b69`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:49:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e7ee730174f13176a4a2ca706f251743bedcb5459da1b8f275d5b6bcc67c0aef`  
		Last Modified: Tue, 03 Feb 2026 01:14:19 GMT  
		Size: 48.7 MB (48655735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbb37aa9daedccd57c940309ed43a39d7248abc940a23204d466caa4499871f`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 11.5 MB (11540452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1930f996b21f85d26d813979c448b5cc33d9133a8314e6eec99d3e973f6035c`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2a47c885c79a443813591c82a08a80cadd63adef2c8d39f9547d22badfcacb`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035ddd951380f76413ebc0059b6934df85dc73f566840fbe23db460cfcd656e9`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 90.7 KB (90675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ef19c1eb6c1cbf32f075f42496b94816b18968b15c0f0b69876955199b6719`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:14a013c4124a4a318ef9462fba9ce8e7d4f7ade0f5398b9583274cdf91689f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3624538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f2134a5a1a99b81c7e83acec3a0283963987a07471c68c3cdf183c9f72d260`

```dockerfile
```

-	Layers:
	-	`sha256:2164015860c8679b1861e5dd23a57a9c9cf4dfe0487d529174fcf93b3b40604d`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 3.6 MB (3608579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cff4e739dd29e441abfa38f38ab0d7eff091449c92875d8627eed5ac223629`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8782f0cbd867e5cbf0a00809d2009fc7d99b9dac92bc8d074fbb25ad4928217b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60017116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92256154c8d58a75a4a78ba1066be026d1a4d93461b9883112013f1f315b31d6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:51:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2309f92dd0c61c985b2d0f865b8d146291a99f7a179b5a243da4f72d2cb33817`  
		Last Modified: Tue, 03 Feb 2026 01:14:24 GMT  
		Size: 48.7 MB (48678525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026f011967afc3b9472b0c743cd8832587b7373c1a9e793ef57c52f8e1c2061c`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 11.2 MB (11243869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c36ebd2a34f62d27f0d7cef3ead3d16165f9623f928d1bfe2b41b30f74c828`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac5250fe806def3c12f50acd0b6fe7d6851fec3d0a5e991b2638d7543c0dca3`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d313056e5d16e90d2205cc6d85f4999bb2e91762bf29d6f405fe2a6bec2fe67f`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 91.4 KB (91372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5cbbb997fec7584e04e4b04ed9e8fdbdf6ca498e81490eaa86e4db34a6c603`  
		Last Modified: Tue, 03 Feb 2026 02:51:54 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:94e7098c49dd9439a3e0b5fd3a09d5ec77087becdfd9c3a9a528a18285e3ebf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd4e5d034a0bd7358ad9328e4e08533bdf5014b7277fa2e24279b515eb53b93`

```dockerfile
```

-	Layers:
	-	`sha256:556e59f143cdbd0a487dbeb922c3d70dae2429bed531b17f3c08f7d816f3ad23`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 3.6 MB (3618117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9bdedb5ebac73f1c7c14c80ceacc95ed4c954edb869cd21a8abb346bdf0a2d0`  
		Last Modified: Tue, 03 Feb 2026 02:51:53 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:76db44b9c094c727694409a86d9d46053c182d88334960270e0c32f0cc439d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61860509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfdd9ac4c6dff21718140687ea8b4349667ed4e76bda91b250de02cd621303e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:50:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:38 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:bd6304d6e56f66e13385dc7464436c6e3933118a9e5b697acc2b57e9b6d5e5cc`  
		Last Modified: Tue, 03 Feb 2026 01:14:23 GMT  
		Size: 50.0 MB (49981936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c435bc3bbcc2b13bab5e538cf235a937f4a4af7f766c52a475efea971328f83f`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 11.8 MB (11784268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de453593ab8b3ceefaf8d95e35ed8836a37f66dbace8e41451254c44d8f0c8d`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b124115f9efbbfa225774d314331b6efc9cb5a56f0297c3b8a3a232389266b`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1864f2cc4b84a441ce01b9bc21922485dea409990a9b34103b645bd80a06f53`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 90.9 KB (90948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcecd183b72d5159137f34d97a72e00182f405589c991bd975f0f5f998d8f0a0`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:35d6816101ce8f76f0bb8cdfcd919c4655940a119331a86e7031cc025cd18677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e1cc49c57572daa393062465301f86970c1cec84f1d7fbd9df4d0baa233c5c`

```dockerfile
```

-	Layers:
	-	`sha256:c78197de2901716faabbc631b5648a6ca556f3490d2677f1df58ce0ad3ffa0eb`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 3.6 MB (3606518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:842ed29984a6b5bb38a099c5776fce07d0557ca96adf412a06ad3ad9508c1747`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:19ec59ed4b51fae27dd278d0bf11380b21edf2718a14a056b71c205ea984a184
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:e497487cf2720a736bacbaedac3ae2436433d09e6ad0bd8a65c86d41f4d063a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33274380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43de36e1bb01c325b9bcc5b3aa2750460e5d3413af9817fb57aff5043948e09`
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
# Thu, 15 Jan 2026 22:34:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:34:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:34:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c31a1de4315e0b58b79ce211ded98e483a09dfdc7f9a6499a9a7ce21a39391`  
		Last Modified: Thu, 15 Jan 2026 22:34:24 GMT  
		Size: 3.6 MB (3624300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ba782c854a068481cc1d19b2b885bc3941b0f687797867734b959977f68bcb`  
		Last Modified: Thu, 15 Jan 2026 22:34:23 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b50cebc4c825ee52a417c7198f1be150abccfd99fab7124120dc49208d23b3`  
		Last Modified: Thu, 15 Jan 2026 22:34:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4ddc7f4be458215b98db1adbbcdd655a576940b797584f026f194d25aea142`  
		Last Modified: Thu, 15 Jan 2026 22:34:24 GMT  
		Size: 111.2 KB (111235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:25d21931ef63fecca937fa9c226d4b9c972c6a07ab7b12d6cd472e98c2f391b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bf0f83a34f3cf53098c7ebd08efc3892d2749a28113b59f8b7fae1fc13e58c`

```dockerfile
```

-	Layers:
	-	`sha256:11dd9334d128520572ee5d6644d929c8e386a02ca3d2ec2ff0bcf28cf4bda108`  
		Last Modified: Thu, 15 Jan 2026 22:34:24 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07dbb8c42e97f3cbb99e13a0cce5eaeb2908125d20a39eb7a012208555bb6be0`  
		Last Modified: Thu, 15 Jan 2026 22:34:23 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:de8c6e985f8ebfc9f9818ad855d16fa99573bd46e0e9f4dd84d73e19618c9a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31098806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fd5b3ddc77a114383c7ee36112f4540c8891c057f8e7a8cc490ac45e5716fc`
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
# Thu, 15 Jan 2026 22:36:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:36:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:36:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:36:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13a4ea43c440ed4c5c6940006aeb234cf69c04ad0392d10b84fd9766e4a34f8`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 3.6 MB (3602633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae0723c728afe1d94014082337ee6c2c149eac4aa6f8373a264ae6ef9d99e8f`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7101abc79e23d3f25054e865a814a95478cc4e41c4b4ccbee0cc361e535cc37d`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506c3cd39c7b72b92ef079ad69cd3630b8af83c92b6ffe3230be891653be676b`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 110.5 KB (110499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:886473be4217eaa0f6c8744ebd3176ca4d06f19d1a76302fb19c67bd0726beaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468d90fb319d993524a4713f622cc2c3e500cd78f13f40e5551c0563785618fd`

```dockerfile
```

-	Layers:
	-	`sha256:58f1ed8735b4542a9a1bea99b6f344ded0a424a110de890d71fa473bc53b359d`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d01ecd9429deb21559e16c32c9f4e387c8f8033115397f07ceae09f9725024d`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:f8a04f8a8dc04df731f84789fcb71e800edabbf6bb1aebd975bbca1fa8f1c3a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2cd764c7884ab25b110fddde83cf33834467579766c56cb1ab549e9a3ea90470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33274712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc3af720234bde69d207e0f9fdc641e991f2697f3fee5ae0aec4cf34d6223c0`
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
# Thu, 15 Jan 2026 22:34:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:34:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:34:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:28 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b59d1ef943d834ee1a50db8acc83df82aaf8bb732bc303a4d9ac314ca79ada8`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 3.6 MB (3624349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903068be00a686117d5126046cccd885353091e8878694caf04fcdb458f28010`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a7436405aa87ebd15250cc5d262e3a512295411df4ec41ab2b7a149be703da`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09c2a0a07d862cba86e9245a3f5fc8b54ab7bc332077758a597ebd129314c71`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 111.2 KB (111237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb3eba37faf714db0851cc8861baaa63273442a84287700b6607cbf7e50d4d2`  
		Last Modified: Thu, 15 Jan 2026 22:34:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:93e9d3bcff981b6bdaebb3818c9abfdf384cfce638b89d07c9d9da38979e63c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d61845c72e5e377c08f2a586fe8d061339c3f115497261045d09f1c31a2058e`

```dockerfile
```

-	Layers:
	-	`sha256:5fb780292168a3a5dbe5f8ce395b7bf5beb0798a6ebe2dc57020d67f10741c2e`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfd6a705adf1df71c78ac76d86175ef0b0fa0cde1b1b6ec1f5a5a5337153629e`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 16.2 KB (16159 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:741ddf278e88035b94dc004a4c6a12f141ac542d2e852ecc9b064c70994cbadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31099022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9af2062e8549cae074e26beb662b0eb5efc3f3383962c6318a236bb569173e8`
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
# Thu, 15 Jan 2026 22:37:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:37:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:37:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39623f164b7c134bd7c870258397b9ae29b76f658821cd89c872006781773a07`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 3.6 MB (3602582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc84ee017cfa97d082301a68c097692ea26fbf238220f31788ab3777fb0915`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62e658825b155b9da439360822a1b71de7886aa64a9f6b2ed952f31379c285f`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf949af04af6e2380e6e33215d31850a1aaf11a41caf3df6b222373f2d115b`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 110.5 KB (110485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ade6120433a2a5a27b1949103586f6bea98efdfbdcde54a84ec40fc4703e39`  
		Last Modified: Thu, 15 Jan 2026 22:37:15 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2f764bf523306b0471b6acd75e196f3491fa44291dc40435483f27e5d5637037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b21632db7bd9623230cd92a59777549d877ad4ed24e036f4a1ca309c4a29973`

```dockerfile
```

-	Layers:
	-	`sha256:09017ddbca29fb71dcab82dce0807d3653f2cca9f0d865f7a27c96666e61c0b9`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd1544fac022fe23da5e4aa065119ee55176834cec20f0c37704625726caef3`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:3b1ea9866549892bcfb5deacf0a8f1dadf9c2f98bc63ce01b622f7745ea46c65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:39dab19ea0056fea381a2e3081c573bfd689d2656f5cc81fd3aa41ae0aafcc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33396645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a7aa252972df966e8bf224240d541b7d88ce8370c9fa313cc2adeea313cf30`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:34:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:34:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:34:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febb96c351dc6c0d19a074b7bf0a980146f228694ed515a5e6e4776348b5d83`  
		Last Modified: Thu, 15 Jan 2026 22:34:59 GMT  
		Size: 3.6 MB (3563150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baad77fe67014a99e49ccbb36bfa471550dbfe256c0a7997b77cc92db588b238`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d558af79b48a1dc1eba2fd55a45ab5177f557780a20b8afd5fecaf034f577cb`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c341089aea08830c751d3756d07510e12c782bb60ddc69ebaab8ffa5029a30bc`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 104.6 KB (104575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5a7b83fa45a2ec02faf249af7419c07420383708eb87fda857dbfe98bdaed5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3607dff0dabf71a31ae8a8d3b3a75f55737f7a69e1d3dc070f88269b85f1486`

```dockerfile
```

-	Layers:
	-	`sha256:d9ff96588e736f2de78e48e58e17efe725819c5302f84fabc2e05fe87cbe845e`  
		Last Modified: Thu, 15 Jan 2026 22:34:59 GMT  
		Size: 2.1 MB (2120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d4dd02fcbaa60ee0e870849b37cadc44a2fc95004b2b0c366e2b4f9fd44b22`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4bbd6e0261957f20c46d34962987746d93400c15e314c81f6a64419c91b7b065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32532687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24eca9e911f1ef800afe0cd19724f336ae82260d50c9f4b9f782df0356d4b3c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:37:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:37:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11d827e327f828ef515a5ee3828fc7df7429f4b6fbac0be158005236e186fe`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 3.6 MB (3560792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26e9075292abfb37049926dd278eaa023c87947273bac27af654d465972b0ca`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a28cca6467154fa487391fafc9c46ab2569d2510dcce267c204dcd1149a12f`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee7e1041691204d39dc1e2e6b9a0d184d8a90b0de7386c680d0babf4b584849`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 105.2 KB (105161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:48009258df992087de7fb120477a38bf8c9e7890ce32c805c7f253896db012ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e121faf012875be8415caaaa95813bfc205ab8f562b254334d16b738816f0f13`

```dockerfile
```

-	Layers:
	-	`sha256:f1c64391a4650e5d5a17196f03e5b2562ea6d98a2f0c2f9a560cefef58af1128`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 2.1 MB (2121910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bda8fe80c01c55cfd927fcb6b54d5213dc934c85a38e089a1945a03b8baf762`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:1ceedf2a318dba40426fe2f72e01fafa822b183fa308fcf3c39c012ee18a5443
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:29bd654a9dd78b6a5e66e56203ea411102c7f500bedb3be6946505c041958f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33397014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7220675f233145f83f0cc39ac185b91891302544e001f10d936298294ccdccb2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:35:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:35:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:35:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:35:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:35:15 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a548ca73cf3c853fcef8cc5fc4e37b42dcc57abd2ed979e56815d39fb4d2e1d`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 3.6 MB (3563186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43697b196e8d2c4b0a8ba22dda06c60a2720d7ecbb327195ef4a733a9a9199a8`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcf22aeb3829fe498fa19c16c5fdb441e50cdd85738b65a2d38355b2322d1bb`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e67f0420cd35a361f4bcd7f5637294ec870f6249ac769578cb2b697880c549`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 104.5 KB (104478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f6e8a4dba4124fe5efdf1962988721ec07e6fc6878bcc80a9a379f9253e849`  
		Last Modified: Thu, 15 Jan 2026 22:35:22 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:72734c10c1cf995c81e4a91d122677f146d6e2563af5405a01fa095d936b2f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83569a852db661e4bb3cb966fcca962060a4d94573ed0f50ec5830ef247bd5b7`

```dockerfile
```

-	Layers:
	-	`sha256:b7b9ddbe9fe86bcbffdd90e2ac87f34033401026b3ffa5b30b988156ead4f9c5`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 2.1 MB (2120901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2f23e802c7e970c3e019b577b1c7691e1f9475949ceaf9b3b66a265ad188d36`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:337e0094efc3a087b25a981421b53f1d439b30ff45c4b8cbe2de4afcaca9a9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32533146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992ff80c45aa201e62f7f3f62e219a102100fd5f4f2888527233f9f87206a02b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:37:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:37:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:37:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:56 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2aea097a4bbb9d5bdaded81482eedf9b99f3c5f026ca55b6e403563c587b66`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 3.6 MB (3560842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76004830fcab5147953ec62120e9188a61c12121f2327a2de3b15e88d02b19d`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f33a41e6ec1c2b8fe89edb69a4ffd926bd25296f84ed1cd3c94a95975d23a25`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9f32872c3ae902f9b9f8f6512093ee79fa4f3b288d84103139a75f0a04a60e`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 105.1 KB (105142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d33c20ca018680f26d1c2204d39af5752691853971325601cd21bee5c51074`  
		Last Modified: Thu, 15 Jan 2026 22:38:03 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:96427596211b20b4819332d643f7cc48057a7e9d68628988529c08c48fee0d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673f5866c150a6e4fdeaf156ee392d4569b2e7ef22f87585d60ab6552fdde497`

```dockerfile
```

-	Layers:
	-	`sha256:8892abf0464711dd694b127d86ae7fbe36a931d3c3786f23ca2bec3f10d2ea55`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 2.1 MB (2121946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e09ac7a089e43b83ed3c810459f514467750bce8124e594af9e8ae6471226a`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd25.04`

```console
$ docker pull neurodebian@sha256:ab139e2ef8b811558941eff017d1f467deaa77fcebcdf3189633727ef717dc92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd25.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:fdc67ac4dd0d651097ba75d3f513b34e66af0bdfa85db80045d15880faf9ef04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36682742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fc9a62b14ecbd0c50b253059091a66a5c95e0809527bce9cdece2619b81e21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:5c208fb70b021afc05727d8dc78f4c389e873e38646fc0f247ced1cb261ea370 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c62190a9ab61c5fadad5c83c08965df006562241538b21f41b5efd457dc50ccf`  
		Last Modified: Thu, 02 Oct 2025 22:51:56 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807958f6dce95c2cf132ab919d751d642e0834efea8afabde5dd80a06382164`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 6.9 MB (6862222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9d85781ba57065c27119c5b829ede85b21f4be4c79ed21b52b5dd18e69324e`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b6000f4f29de58b9c57f46bf4c2915a41aecfde0ffe93b519dc150c2e05839`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b298e1353c735a6385e6a62cecbfe1d1b59a32feea6c006fe2970e9a377fb0`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 103.6 KB (103644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:87fb8fcdc3533806d68ebce00bcfcf60c95a4fd2ca27173aa2131f4e12b9a92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f7aa5c68eb77711d7c5504ea0dd43319dc6ba5a495e2a39b29e42dd4613450`

```dockerfile
```

-	Layers:
	-	`sha256:34e86114d346aa4146ae590dee647494234ddff44dc9bf93ed557394aed25887`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 2.1 MB (2129387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb29516268d88fbe0487f9e71585d01a2863eda154c3b84c932731ccf47ffd8`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 14.0 KB (13987 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd25.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d0215dbda4b85ac69b750d98f8f3eb9aba18829cafe490ef6c04e7f1b5d3575f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34803835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6196b8372a58dd339a5cd7b297736021c12b067eaa196975ee6481a581ec22`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:2e32d5ba6a5a96833b0deaf9c5a7ed2559bab3a9addcff92dfe49254b9cc654e in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:49236737bff0862bb8b036b6c3ef5438b02eff6a137b08f62499d2764ac53431`  
		Last Modified: Thu, 02 Oct 2025 22:52:03 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b8d7c0516946e6186f0c1918a80da44ccc80465d586f0db577e9c5e3fa309`  
		Last Modified: Thu, 09 Oct 2025 21:21:53 GMT  
		Size: 6.4 MB (6392372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccd7c148caa4ff621b2e8f1407d0680d8b216fd3b91aade2da4e3bcf67242ab`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63a7c688f7b81b2251c0096fc2033ac1c2243330fd41da718cf8002ec93dae1`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a8bb23e4d96a15bc63dda952317ea8ba3a8efd39c025f4e5d59b26d5afc57c`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6b6e0e2468e055fd3994fdd22716a6516ca822a0b893af378cfe9b7c8c92ee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b634830ed4e5ae3eba300cf243790465b87b6d976898e0bdc93781f17d3473b`

```dockerfile
```

-	Layers:
	-	`sha256:73f73f1097d47935c4c36115e56c20ae5811fee70906bb8d0100cacf857414df`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 2.1 MB (2129631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3369301dca599eb9decd9b13cef9db3cbe5da13f1a35be39a2983729b9cd67db`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd25.04-non-free`

```console
$ docker pull neurodebian@sha256:843d307ce6bc09a7cd1b57e44466adef4c4764ea1c793ae5816c4c23f5fd2e42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd25.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7e3b0aa3a1e9664cb5a8951141d1855604212beb174f638ffd32f46742ed4bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36683143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b635066dc43129e20e37c95f2235d3e316b7d3b9c2aba40f0ffde2b54e2e6e2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:5c208fb70b021afc05727d8dc78f4c389e873e38646fc0f247ced1cb261ea370 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:c62190a9ab61c5fadad5c83c08965df006562241538b21f41b5efd457dc50ccf`  
		Last Modified: Thu, 02 Oct 2025 22:51:56 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e95813fe4718cf415f65b5a2a6aff41cf1ca472b75f81f0e71c88a2c1e75e9`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 6.9 MB (6862197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c069ba67e04af50034555225735086ac2d283d240d8ce7e46a9d3308c6398c25`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7163aa66b2f0788a2fd8bfb24efa8a573ed390b32865ae0266981836fb3f2a`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4744d7aa582d29cc5ee3a878017b70e760a48aaf077eeaf1aa5c0b98f225a81b`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 103.6 KB (103637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709942cf2f7b8bc52d31c967ec725251f89630a82eb3debdaafff34b2502aec6`  
		Last Modified: Thu, 09 Oct 2025 21:20:58 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b03d30cc46e85e007f546cd2c4a415622d8016571f0fcd74004ece8a9d69a9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b1b3d34374f9d8719267a2de2de8be8524966deb0e192f3a0d0b9e95bbf7e6`

```dockerfile
```

-	Layers:
	-	`sha256:75abe1e107a33427871261a37ffd5362e38bd76021a38d45be8b8ecfd67cf1a7`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 2.1 MB (2129423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63f0d6a23d261b81b7b10446e66dbf147c195e56727be3c4c4095beb8744927b`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd25.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8bb52949ffdc66d1b1c45b166770d0321d7082209a408f0dde0ce50355c437d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34804334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6029e77c7f8a48311858bca5d16c501aebcd7dbababb443b3c892392f8506a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:2e32d5ba6a5a96833b0deaf9c5a7ed2559bab3a9addcff92dfe49254b9cc654e in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:49236737bff0862bb8b036b6c3ef5438b02eff6a137b08f62499d2764ac53431`  
		Last Modified: Thu, 02 Oct 2025 22:52:03 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d08ff3fe3897ede8ef5bf7e75a8c754e9da90066ad638138411914e6569fcb`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 6.4 MB (6392412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87458cf3c50f45fec6029a8e2d31f7dc2c30d63c5e92c7e4f4d7ddbf1fd1fb4`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fabfa39ef821d160c97bf91453f07634d072ad956ea83de4da94873f2b71a97`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9d80fbf3cdda43cd93b73ef0b7215c959689c5073a718bc28b1a88b435aeda`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 104.2 KB (104235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3181f804aca7e1622946b1391b32ee30ccebfbdb03426caab02bcd300d54cd8b`  
		Last Modified: Thu, 09 Oct 2025 21:22:07 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:29ea36baad60d33ffbfb5fd8152d415e121532b4008b174a68251c71851548a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5656dffee277d964d7af531bee03d767b53dc21bddc33bbedf5b7d1e0c3a1668`

```dockerfile
```

-	Layers:
	-	`sha256:a897c9f03a98ed8cc43baa74786f9234dccd6f6c51fe452db7dab397fb9c66a0`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 2.1 MB (2129667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0912356738dd5be0731ed4354e13efdb3bb03dfc003407132e1ed93bde4ad42a`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:3b1ea9866549892bcfb5deacf0a8f1dadf9c2f98bc63ce01b622f7745ea46c65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:39dab19ea0056fea381a2e3081c573bfd689d2656f5cc81fd3aa41ae0aafcc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33396645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a7aa252972df966e8bf224240d541b7d88ce8370c9fa313cc2adeea313cf30`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:34:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:34:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:34:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febb96c351dc6c0d19a074b7bf0a980146f228694ed515a5e6e4776348b5d83`  
		Last Modified: Thu, 15 Jan 2026 22:34:59 GMT  
		Size: 3.6 MB (3563150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baad77fe67014a99e49ccbb36bfa471550dbfe256c0a7997b77cc92db588b238`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d558af79b48a1dc1eba2fd55a45ab5177f557780a20b8afd5fecaf034f577cb`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c341089aea08830c751d3756d07510e12c782bb60ddc69ebaab8ffa5029a30bc`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 104.6 KB (104575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5a7b83fa45a2ec02faf249af7419c07420383708eb87fda857dbfe98bdaed5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3607dff0dabf71a31ae8a8d3b3a75f55737f7a69e1d3dc070f88269b85f1486`

```dockerfile
```

-	Layers:
	-	`sha256:d9ff96588e736f2de78e48e58e17efe725819c5302f84fabc2e05fe87cbe845e`  
		Last Modified: Thu, 15 Jan 2026 22:34:59 GMT  
		Size: 2.1 MB (2120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d4dd02fcbaa60ee0e870849b37cadc44a2fc95004b2b0c366e2b4f9fd44b22`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4bbd6e0261957f20c46d34962987746d93400c15e314c81f6a64419c91b7b065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32532687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24eca9e911f1ef800afe0cd19724f336ae82260d50c9f4b9f782df0356d4b3c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:37:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:37:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11d827e327f828ef515a5ee3828fc7df7429f4b6fbac0be158005236e186fe`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 3.6 MB (3560792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26e9075292abfb37049926dd278eaa023c87947273bac27af654d465972b0ca`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a28cca6467154fa487391fafc9c46ab2569d2510dcce267c204dcd1149a12f`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee7e1041691204d39dc1e2e6b9a0d184d8a90b0de7386c680d0babf4b584849`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 105.2 KB (105161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:48009258df992087de7fb120477a38bf8c9e7890ce32c805c7f253896db012ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e121faf012875be8415caaaa95813bfc205ab8f562b254334d16b738816f0f13`

```dockerfile
```

-	Layers:
	-	`sha256:f1c64391a4650e5d5a17196f03e5b2562ea6d98a2f0c2f9a560cefef58af1128`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 2.1 MB (2121910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bda8fe80c01c55cfd927fcb6b54d5213dc934c85a38e089a1945a03b8baf762`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:1ceedf2a318dba40426fe2f72e01fafa822b183fa308fcf3c39c012ee18a5443
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:29bd654a9dd78b6a5e66e56203ea411102c7f500bedb3be6946505c041958f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33397014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7220675f233145f83f0cc39ac185b91891302544e001f10d936298294ccdccb2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:35:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:35:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:35:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:35:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:35:15 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a548ca73cf3c853fcef8cc5fc4e37b42dcc57abd2ed979e56815d39fb4d2e1d`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 3.6 MB (3563186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43697b196e8d2c4b0a8ba22dda06c60a2720d7ecbb327195ef4a733a9a9199a8`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcf22aeb3829fe498fa19c16c5fdb441e50cdd85738b65a2d38355b2322d1bb`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e67f0420cd35a361f4bcd7f5637294ec870f6249ac769578cb2b697880c549`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 104.5 KB (104478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f6e8a4dba4124fe5efdf1962988721ec07e6fc6878bcc80a9a379f9253e849`  
		Last Modified: Thu, 15 Jan 2026 22:35:22 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:72734c10c1cf995c81e4a91d122677f146d6e2563af5405a01fa095d936b2f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83569a852db661e4bb3cb966fcca962060a4d94573ed0f50ec5830ef247bd5b7`

```dockerfile
```

-	Layers:
	-	`sha256:b7b9ddbe9fe86bcbffdd90e2ac87f34033401026b3ffa5b30b988156ead4f9c5`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 2.1 MB (2120901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2f23e802c7e970c3e019b577b1c7691e1f9475949ceaf9b3b66a265ad188d36`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:337e0094efc3a087b25a981421b53f1d439b30ff45c4b8cbe2de4afcaca9a9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32533146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992ff80c45aa201e62f7f3f62e219a102100fd5f4f2888527233f9f87206a02b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:37:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:37:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:37:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:56 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2aea097a4bbb9d5bdaded81482eedf9b99f3c5f026ca55b6e403563c587b66`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 3.6 MB (3560842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76004830fcab5147953ec62120e9188a61c12121f2327a2de3b15e88d02b19d`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f33a41e6ec1c2b8fe89edb69a4ffd926bd25296f84ed1cd3c94a95975d23a25`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9f32872c3ae902f9b9f8f6512093ee79fa4f3b288d84103139a75f0a04a60e`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 105.1 KB (105142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d33c20ca018680f26d1c2204d39af5752691853971325601cd21bee5c51074`  
		Last Modified: Thu, 15 Jan 2026 22:38:03 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:96427596211b20b4819332d643f7cc48057a7e9d68628988529c08c48fee0d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673f5866c150a6e4fdeaf156ee392d4569b2e7ef22f87585d60ab6552fdde497`

```dockerfile
```

-	Layers:
	-	`sha256:8892abf0464711dd694b127d86ae7fbe36a931d3c3786f23ca2bec3f10d2ea55`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 2.1 MB (2121946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e09ac7a089e43b83ed3c810459f514467750bce8124e594af9e8ae6471226a`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:006ddee33bc319d072a14cc4d994bc2ecabbee1b0945976e1df7658fb4255fed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bfe6f18aa6a74c90c1bef54a8ecbfd1554d462da56f4431077902cee7e35743f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59679073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1734174826d480fd0ca4221a27524fe98e871a54a19c068307ec6b8d151189d5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f763d27f0cca3eca63d032df25da1781edc10ad21bb6ec6472a87765b5d494`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 10.3 MB (10292413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2193d3bb29390a43b5fe3cf6ef36f5d049269591f33a3f65f1c3ebf33ea628`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f82edf0cab6319880f6003cb047a9679b2b534d136feeba495550f279df6cb9`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae03b3a868a98138feda4a04a1f015e865a3599f8231275cde4e2d3ab18157`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 90.4 KB (90354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4f2df40ce739fcaf54c09cdf8f844f97b7b89ddd3a009cf66056798e7a816d`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73fbf95673c18f9bfa0a30481eb45b538fec3995c608702a1c1d90e08da42446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9f83b2f6643450c6e9f512971c820c8345c704dcd2e8cc7a8756a02e736f86`

```dockerfile
```

-	Layers:
	-	`sha256:6c76910ec532300ba0ac33261e0fa300df86a2a7236c44063bcf717e3999b372`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 3.6 MB (3614108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48dd7f90c47288d683499a84f5abe7001a411496c218e1bd8e77b25b0888176`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4c13946a073d0e0d9f2340b836b54e9a9dba1f010f04df5dd200dbc7b1b5af23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59820236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c689286b6669d33d79af74959237011ecd70075c64056e24a6d02c270876d1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:51:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba456ea91fba33b0b2266f0965cf72ec30eb7f1d6c06aa2a1c64acb11287462c`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 10.1 MB (10073826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c8707cbc6b46ef363481729ebc07a939af077bb4b56fc62ac5a4ff2270d3b2`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba3130f7897eb800b59a9393f231600424ff257e4f3e7b2648b3541566c64df`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbc4bfaf80cebb772173dc6b7ebf4d6c65aa74b8a1100448ee711a7b11f0f2e`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 91.0 KB (91037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60db51e8517172f9d697f6dd3dfd52ed53bc5d6102dfde87d9d7b154e3f0f1ac`  
		Last Modified: Tue, 03 Feb 2026 02:51:47 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a0bb841aee3fa661b5cf22150ac560131f548d1e2f6de469929472a1cae8d039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad53c32ccedf0d4c008cbe8f0cc3fa2f71fa4b95414674e681a85c5e5b8f37c4`

```dockerfile
```

-	Layers:
	-	`sha256:130d559f8c021baf79e6466c9df7613170e752a7e5cd42a30367c9f470ca7e5d`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 3.6 MB (3615635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349032d3fccfe1a4b3f53e519f7c3f349aaa60303d81e595a5a2f73a422d2b63`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1b7cc3e8e887276f4b47a7a7f3fdb6a9d8ccad482d37c05d554655857987d25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61365948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a8a124a6dc9a583795fdffe09999ff8fe4b6724e1f73ee53a9cc663d7baf26`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:50:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b536877d3c0a030ad79a6593cd07fd6d9d694a4ee908632c85159f47caa880c2`  
		Last Modified: Tue, 03 Feb 2026 01:15:09 GMT  
		Size: 50.8 MB (50805135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151531fafaa44052b8ef62edab30c39e82df6362c327e633a87856cab112f38b`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 10.5 MB (10466690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c46322ddba400bbf437e7982be185466ac3a30b6c3e18306fb107df084ef6f`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2601d6950df113d96bbe256462649bc0356027670c0fdeeea1a36db50b8070d6`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbc29155f72161458e612a5e0f3deefd8c0b90f6c6b725d755d6cbb64fdaeb3`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 90.8 KB (90767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a58325440b9ddaee417a935c1ba847b99eca4326d8cbc0cfb83ad3ec4e62d6c`  
		Last Modified: Tue, 03 Feb 2026 02:50:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1a1c6b5b1309c9a6d397be72aec7d51df19e72b1ed14d8e559ddaac54b8d45a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834635029b6ce5298f9a745d504c4600d908f105eebe44ef56cca8eff573a1f3`

```dockerfile
```

-	Layers:
	-	`sha256:baf157ba5397d5cc0efb14f1b4af8b0e255ff3dcd41813d3551db6e42c9b6e1e`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 3.6 MB (3612056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190165ca7a14affd0179a3d6aa5c67852f9eccbb4f971c73979a03c8629c2d97`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:plucky`

```console
$ docker pull neurodebian@sha256:ab139e2ef8b811558941eff017d1f467deaa77fcebcdf3189633727ef717dc92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:plucky` - linux; amd64

```console
$ docker pull neurodebian@sha256:fdc67ac4dd0d651097ba75d3f513b34e66af0bdfa85db80045d15880faf9ef04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36682742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fc9a62b14ecbd0c50b253059091a66a5c95e0809527bce9cdece2619b81e21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:5c208fb70b021afc05727d8dc78f4c389e873e38646fc0f247ced1cb261ea370 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c62190a9ab61c5fadad5c83c08965df006562241538b21f41b5efd457dc50ccf`  
		Last Modified: Thu, 02 Oct 2025 22:51:56 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807958f6dce95c2cf132ab919d751d642e0834efea8afabde5dd80a06382164`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 6.9 MB (6862222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9d85781ba57065c27119c5b829ede85b21f4be4c79ed21b52b5dd18e69324e`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b6000f4f29de58b9c57f46bf4c2915a41aecfde0ffe93b519dc150c2e05839`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b298e1353c735a6385e6a62cecbfe1d1b59a32feea6c006fe2970e9a377fb0`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 103.6 KB (103644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:87fb8fcdc3533806d68ebce00bcfcf60c95a4fd2ca27173aa2131f4e12b9a92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f7aa5c68eb77711d7c5504ea0dd43319dc6ba5a495e2a39b29e42dd4613450`

```dockerfile
```

-	Layers:
	-	`sha256:34e86114d346aa4146ae590dee647494234ddff44dc9bf93ed557394aed25887`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 2.1 MB (2129387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb29516268d88fbe0487f9e71585d01a2863eda154c3b84c932731ccf47ffd8`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 14.0 KB (13987 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:plucky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d0215dbda4b85ac69b750d98f8f3eb9aba18829cafe490ef6c04e7f1b5d3575f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34803835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6196b8372a58dd339a5cd7b297736021c12b067eaa196975ee6481a581ec22`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:2e32d5ba6a5a96833b0deaf9c5a7ed2559bab3a9addcff92dfe49254b9cc654e in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:49236737bff0862bb8b036b6c3ef5438b02eff6a137b08f62499d2764ac53431`  
		Last Modified: Thu, 02 Oct 2025 22:52:03 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b8d7c0516946e6186f0c1918a80da44ccc80465d586f0db577e9c5e3fa309`  
		Last Modified: Thu, 09 Oct 2025 21:21:53 GMT  
		Size: 6.4 MB (6392372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccd7c148caa4ff621b2e8f1407d0680d8b216fd3b91aade2da4e3bcf67242ab`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63a7c688f7b81b2251c0096fc2033ac1c2243330fd41da718cf8002ec93dae1`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a8bb23e4d96a15bc63dda952317ea8ba3a8efd39c025f4e5d59b26d5afc57c`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6b6e0e2468e055fd3994fdd22716a6516ca822a0b893af378cfe9b7c8c92ee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b634830ed4e5ae3eba300cf243790465b87b6d976898e0bdc93781f17d3473b`

```dockerfile
```

-	Layers:
	-	`sha256:73f73f1097d47935c4c36115e56c20ae5811fee70906bb8d0100cacf857414df`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 2.1 MB (2129631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3369301dca599eb9decd9b13cef9db3cbe5da13f1a35be39a2983729b9cd67db`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:plucky-non-free`

```console
$ docker pull neurodebian@sha256:843d307ce6bc09a7cd1b57e44466adef4c4764ea1c793ae5816c4c23f5fd2e42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:plucky-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7e3b0aa3a1e9664cb5a8951141d1855604212beb174f638ffd32f46742ed4bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36683143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b635066dc43129e20e37c95f2235d3e316b7d3b9c2aba40f0ffde2b54e2e6e2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:5c208fb70b021afc05727d8dc78f4c389e873e38646fc0f247ced1cb261ea370 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:c62190a9ab61c5fadad5c83c08965df006562241538b21f41b5efd457dc50ccf`  
		Last Modified: Thu, 02 Oct 2025 22:51:56 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e95813fe4718cf415f65b5a2a6aff41cf1ca472b75f81f0e71c88a2c1e75e9`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 6.9 MB (6862197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c069ba67e04af50034555225735086ac2d283d240d8ce7e46a9d3308c6398c25`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7163aa66b2f0788a2fd8bfb24efa8a573ed390b32865ae0266981836fb3f2a`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4744d7aa582d29cc5ee3a878017b70e760a48aaf077eeaf1aa5c0b98f225a81b`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 103.6 KB (103637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709942cf2f7b8bc52d31c967ec725251f89630a82eb3debdaafff34b2502aec6`  
		Last Modified: Thu, 09 Oct 2025 21:20:58 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b03d30cc46e85e007f546cd2c4a415622d8016571f0fcd74004ece8a9d69a9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b1b3d34374f9d8719267a2de2de8be8524966deb0e192f3a0d0b9e95bbf7e6`

```dockerfile
```

-	Layers:
	-	`sha256:75abe1e107a33427871261a37ffd5362e38bd76021a38d45be8b8ecfd67cf1a7`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 2.1 MB (2129423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63f0d6a23d261b81b7b10446e66dbf147c195e56727be3c4c4095beb8744927b`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:plucky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8bb52949ffdc66d1b1c45b166770d0321d7082209a408f0dde0ce50355c437d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34804334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6029e77c7f8a48311858bca5d16c501aebcd7dbababb443b3c892392f8506a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:2e32d5ba6a5a96833b0deaf9c5a7ed2559bab3a9addcff92dfe49254b9cc654e in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:49236737bff0862bb8b036b6c3ef5438b02eff6a137b08f62499d2764ac53431`  
		Last Modified: Thu, 02 Oct 2025 22:52:03 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d08ff3fe3897ede8ef5bf7e75a8c754e9da90066ad638138411914e6569fcb`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 6.4 MB (6392412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87458cf3c50f45fec6029a8e2d31f7dc2c30d63c5e92c7e4f4d7ddbf1fd1fb4`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fabfa39ef821d160c97bf91453f07634d072ad956ea83de4da94873f2b71a97`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9d80fbf3cdda43cd93b73ef0b7215c959689c5073a718bc28b1a88b435aeda`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 104.2 KB (104235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3181f804aca7e1622946b1391b32ee30ccebfbdb03426caab02bcd300d54cd8b`  
		Last Modified: Thu, 09 Oct 2025 21:22:07 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:29ea36baad60d33ffbfb5fd8152d415e121532b4008b174a68251c71851548a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5656dffee277d964d7af531bee03d767b53dc21bddc33bbedf5b7d1e0c3a1668`

```dockerfile
```

-	Layers:
	-	`sha256:a897c9f03a98ed8cc43baa74786f9234dccd6f6c51fe452db7dab397fb9c66a0`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 2.1 MB (2129667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0912356738dd5be0731ed4354e13efdb3bb03dfc003407132e1ed93bde4ad42a`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:5736c97073ee74f8f16e62030c34d68ea731f86e107e74b0c781593277e9dbb7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:742f81326d6458fc4835788d8fe3317f77b687290629fc738389f12c4814df3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60288474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d9d256c1ca3e4c144c863cc2281316c3cc3eb45088369a88aea3a40a0914ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e5dc831051d738f5c1db4254dde56feb7c9e75e136e23995d896f1b6e1ba752f`  
		Last Modified: Tue, 03 Feb 2026 01:15:47 GMT  
		Size: 48.7 MB (48654703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911d1558a1b3010131d47ee741db0963c889273e31e2a95035fd6cfb9f17c1`  
		Last Modified: Tue, 03 Feb 2026 02:49:21 GMT  
		Size: 11.5 MB (11540410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582397b9dc850b850ffd74061feea99dfb6b237c0192d6191177bd0a6cd86b64`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6309d0a7b6729391c7f1314a74b6b06b07c4646ed52a3d9e7ce4cb11daa5bc`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0740384dd13f89422fe1f4638c08fb758dc33e4f5c9810aa0b1d0a69d7fae0bb`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 90.5 KB (90457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4e1ba3408ddc3dfef56dc25b1915ff61fc917b613ede0a431592467c4b4864a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba3eb40824aca52a92259785bc8cb173186a6bb1ccb406742f34f2f6ebfec74`

```dockerfile
```

-	Layers:
	-	`sha256:7d69e622a5bfed66bf691b20cdf1aa82f53f6f580b821ab40aec94be47d4d4b1`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 3.6 MB (3607661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7e7edca04a0e1aa36eebfdd3e3f3946a1ce7603207a77681ec83592f931e12`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9f8d97f995caee3f00eabda2e5b2e80dda71f89f30a2aa9880a5822d60e61fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60017241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed43c76e582a60593bacd55fe4dcd315ba8213831d318c188385c0990e8cbcc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:51:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:02c386337e70e225c826a0b6295dc937d7a841e7301f60fa7a03adccf75af2ad`  
		Last Modified: Tue, 03 Feb 2026 01:15:52 GMT  
		Size: 48.7 MB (48679232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd35008056e1180ece221c285a1c86c1769a7176cb5d2e594f69e6d206f64ae`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 11.2 MB (11243894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92aab31c07432757e3c05a48406dacbb80522a11812614df8c6a1d9a79a3154`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7f8a8c48aa5f798b4c9dd2715c2e97c069e5446870e61c7604c9e8621078cf`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689f86ee7d710aaf5e5f25e6ab2160a673cbeba10275adc492d11b0573243f78`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 91.2 KB (91207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a6e4e155a78bd1cf49dbc0345cedd63cd782f42ca24d03ebbc9eec6770f30589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a8d05e0e918a47d8eba4c94f215675f9e099ec13d995e05081385ee0a01f8d`

```dockerfile
```

-	Layers:
	-	`sha256:995820befc47d1c55c6cc54493b19e2c17b2821c3c7a7aecd5c807d813f05460`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 3.6 MB (3617199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f93978bff663ff63536a1550e800673779f73f1aa275a88ecc1f1ad05e58bf8c`  
		Last Modified: Tue, 03 Feb 2026 02:51:57 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:6a90c95db1a2638b60aa36691d3a536024d2108a161f2c5fe47c17d301bb22c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61867005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6f605f6913d479e305f041c7a9b47ccb2ebb97207c2fbb42fd8a3f7c4c3f17`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:50:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5e68504863f049552110bc4132aac67ebf9360a9ca0dd44ced1eb7009b5560a2`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 50.0 MB (49988982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e9787e5aeae5594380d4cbb775abd6fa3ec27c76a2ec4cca5e9405d5336bbb`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 11.8 MB (11784382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b778f855abd2e9eba1fb32ff318ee9e04561d33943ad5ee010c23514f44c7f9b`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b76d608765aa6285fce58e5f3f7c2d318b20960b933cd4f0f96f93b8350f7e`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4740d9cbf74ca39636ca18c075358ca3fc32195250247fc9c8a961bfbd5437c7`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 90.7 KB (90737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1d1e658726c43eec3951bcb02149b6f9ed20f79e8668fbe71937320ed8f4814a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3619476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66420441c356368d62eef101d1964d2aa0a638f7076eb7e63133073408c60356`

```dockerfile
```

-	Layers:
	-	`sha256:960074c60cda9620fb77ba8ba0212d8d0ae309978f421b6147062e8f62cfe20e`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 3.6 MB (3605601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9187b2aaf43c788908a856edf1454a2ea59994c22e7278cf0676b60711104265`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 13.9 KB (13875 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:ba3a5b3b2b48154994a4f7695bc318ef6d6a9549ef04ddaa919ea05049e886f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a34bd5c63c5d4d902f50950efd6ce5dca64b1addf6060d5cb0d1249f0cbee543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60288827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308f8f8e8e8be830f406d62dc791fd094ace9d9714082e5a38b94de80c022113`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:49:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e5dc831051d738f5c1db4254dde56feb7c9e75e136e23995d896f1b6e1ba752f`  
		Last Modified: Tue, 03 Feb 2026 01:15:47 GMT  
		Size: 48.7 MB (48654703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7002f3da964c57bd455c7ea9aea032a614f96ad162a44a4e3be7f438517c9a`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 11.5 MB (11540369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582397b9dc850b850ffd74061feea99dfb6b237c0192d6191177bd0a6cd86b64`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfae06b9f53d369e6035db2bb25acc88db5141f15668b9c187df731a53d6330`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0675e38a13a9ae911bed6a859416965f3afb652c0c0bde63d3aa4b7c256fd8`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 90.4 KB (90432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a622e4dd49c0b33475fbc290bee154d0d2fa0f6b39499fc01581d935969bf0`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e40dd2e539b3db456883132b1b1edd605a481e44ded2b819881cb3566719049d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a040ca843f8191579ffafa4b24724273fd39a8d8db116dbf48cb294a674d25ac`

```dockerfile
```

-	Layers:
	-	`sha256:80d0cd2e330fc9bf7aa1ae15a2864ea8ed86232bb2bdabd6bdfc79ab09150396`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 3.6 MB (3607697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44da38342d0de406e284f67ea9541752f7cdaec248b21cc9996fbba57ab3770`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d73b7d2e2e9a0ad75e6d8f2f202ac45c5c90804f7fd491f04759f8c9ab560ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60017503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55231f6fa6a70347e96f433340baac503f1e0bc79c0414cf4e2cd569707fe81`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:51:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:02c386337e70e225c826a0b6295dc937d7a841e7301f60fa7a03adccf75af2ad`  
		Last Modified: Tue, 03 Feb 2026 01:15:52 GMT  
		Size: 48.7 MB (48679232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72169edcd3114aed53fcfb33bb985a27c25f0be4ce0b90c7ee3b2602e511eb55`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 11.2 MB (11243763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aa6d785888f0c8b41e2b5e14ac04e5cd32dc32e062cef01e52dd756c1b6029`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388b2d36400e3f10c42b37febaa865685b8cea7dfdad772bb4cb4648074b6df6`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c459f79798bb027f6a4cf0b4a000a6cce488b3b3163fe0705ab4981141f549`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 91.2 KB (91186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4117407e6309b71a85ba30e66e465b94f6a37a79cf55f9f2c9dce60d28096c`  
		Last Modified: Tue, 03 Feb 2026 02:52:01 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1130f85f99e63a69789b6108372d5894b1d29ab420ebaf59267e41ca7a6562ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde2abd89ee4f4696f8234059b1d01413d7e73a51ec67b0f521b58b71cd0cab6`

```dockerfile
```

-	Layers:
	-	`sha256:fe2137c73c306d7eb945a76ae5920f36787323e1cb8075c3895577f467340eb2`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 3.6 MB (3617235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:375c5dbafd2c21265776eed0de1841a836200f05b1e2f050c3ded17494a3b686`  
		Last Modified: Tue, 03 Feb 2026 02:52:00 GMT  
		Size: 16.1 KB (16070 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:09d2a82a7755f31bdc924260b1004d9e18f89b53e70681bf9f52e5d7c38265b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61867112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e26265fed5bec7a6be142173b02f16f7dc8000655ce83cfeb5f076665d6436`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:50:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5e68504863f049552110bc4132aac67ebf9360a9ca0dd44ced1eb7009b5560a2`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 50.0 MB (49988982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4b67206060b17bfa3f7c139d34dc7edde12328d9c0813401b6e218eeb526c2`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 11.8 MB (11784066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12563f627f2b777c32fad8fe06dc8a81cc93f797fecbcabcdd16f1a26568ac2c`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65b76f0d68fd4c718faf7b6a1dc01fe7c5addcba58f6273fab12fa8a150f330`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af106d4cc2812bb0918ebbd81516dad845621128fb2918143205c8255f2683f5`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 90.7 KB (90739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894703054bb720e327a2e8882bc8458ade09a154ae2005401bc22f71b7dbb7c`  
		Last Modified: Tue, 03 Feb 2026 02:50:52 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f3e41fe08d7abe4d29d2ffc0de45275ed7b5ca3b8280228247ca7c0828af736e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08921bcb04326e7d1d3cd578e21a03f61ee55fbb62ab7c207503b48aa6a75322`

```dockerfile
```

-	Layers:
	-	`sha256:7a558ce5ffa36aad5b5023dcfa30033ae66b7efd72b87f4fe8ab2ee6c15257b4`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 3.6 MB (3605637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdc2c6ad005dcf4f986126d621753f79ca7d6682cde71dab23e896c5930c544f`  
		Last Modified: Tue, 03 Feb 2026 02:50:51 GMT  
		Size: 15.9 KB (15900 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:9e594df6bac4c9c0c4daa53c980bb4b3a83e3fa0d293167d551e63d718150e45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie` - linux; amd64

```console
$ docker pull neurodebian@sha256:da3b9227f84c0e82c2a1cd4cb5e96ec28789730085a1ac4652b6bb91620d43a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59678819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be8b026c74f7c723c4dd8ef3d34903dbf19b1ec0bcfb0356313abfeee3f0d4a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:48:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae41ec031155c98b455bb78067eba48a17546176cae679a09109c6f40044b853`  
		Last Modified: Tue, 03 Feb 2026 02:49:08 GMT  
		Size: 10.3 MB (10292604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c456de52ce89d78c3e11be3ed11cac3ff2a3bbf1b5b7acbcc34864caa6ed1b`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901c3f547274c1b9aba5a4c1dca0de6439e3641e2927b7ff0e29ba10f2598771`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e44b0ddaace5231fb0277c41a8f1dd1b9a803222537517cf5fc0faf0163b35`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 90.4 KB (90356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0af8d1c9f950620612b890e7e6a4d8c5e0b2b9f2e5fdfb0bced7707c0f81c1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a741a8c1833792cc9553aecb085450cdb9f1664685ce094c1941eda5289f656`

```dockerfile
```

-	Layers:
	-	`sha256:e40985eb60787ad8aa5df064ec78906a87d592650d3cb7bd4e4d35fef41aeff0`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 3.6 MB (3614068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c276c637f8dbb8e68f06bb64f124d7e82ae5dde2c17bdf3085ab2d27b05e7a9`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e3fad9231ad143b2ff8fd64aa94fc567d24640473609aa9e53813ba25514dd56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59819618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61bb57dc02b437ffa494706757c4e8012b3ca9dc37c95e0eb0a621d87abe9dcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:51:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22da6bb4121ff52ec24b7b3ca19672a3a6dd5bd671413dade3605ce5d9db5212`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 10.1 MB (10073679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff00c0307437e770f79d7730e90f4fe49614963cc352021322f601722e96861`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8be89556aee6cfbc97cba23e7039718bbfb9e26c495ebeecc6b35befaaca0f`  
		Last Modified: Tue, 03 Feb 2026 02:51:45 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e2e18971c937c3084a9bc87a08e8529f6a4134d0df2863e3a7122cc88202f`  
		Last Modified: Tue, 03 Feb 2026 02:51:45 GMT  
		Size: 91.0 KB (91017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:77bdc7555a73675a432f3ed42bdd322df51878adcfd7f5430a8078b80b1dff39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ee510c4dd9d6ee4305db104fdbbaaaa61cda87948394e49326c32b36e0dda2`

```dockerfile
```

-	Layers:
	-	`sha256:3e9450b0d7b05d40b743a7a02ed1088df21be4b25b167218b0ed71e322282c79`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 3.6 MB (3615595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aaf88d71cb5e6047430224faeccaa93971261590bea6c175d6ab5d6990d57c`  
		Last Modified: Tue, 03 Feb 2026 02:51:45 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:0c07f5e657cc09b86e2e9d42cfe321237c14a5e56f50e8ddfbd4e883d1df05f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61365542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd0e10b4f3310ce286b4442d36b326afc8ee52d43f2fe723ebb88a02ac4ff15`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:50:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:13 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b536877d3c0a030ad79a6593cd07fd6d9d694a4ee908632c85159f47caa880c2`  
		Last Modified: Tue, 03 Feb 2026 01:15:09 GMT  
		Size: 50.8 MB (50805135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8584529105db32472d0fb905ba0ffd3f044b43449f19a931af68cbff933e6f0`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 10.5 MB (10466733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5467fcd76c4951d6cee5b8fea463953e06cbf6b3499279c34eb9e44fe4a41b`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468da32b58b2c95585f26b570d4c00790c123586d464617db5182bb2a4f019bc`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639673e23612c864203b2e3ffc9651b21dbf4b2aa62f36a7a66ecdf0a75bb6a2`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 90.8 KB (90764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3a8babc935e1f8f1e38243dbb223658ef808b3e8c0a544f215cff45d7986f31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8d14de849f297db4adf9be12411a7e0ca06be0469961ec5dea52a603352dcc`

```dockerfile
```

-	Layers:
	-	`sha256:1cff4584330b4a198de56e38439573dd2692d53421016a7605697ac702459b73`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 3.6 MB (3612016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c846b8599cc185520df1fabe5df76ae8f9e4cd8995574b29094363d2157ba84`  
		Last Modified: Tue, 03 Feb 2026 02:50:24 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:006ddee33bc319d072a14cc4d994bc2ecabbee1b0945976e1df7658fb4255fed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bfe6f18aa6a74c90c1bef54a8ecbfd1554d462da56f4431077902cee7e35743f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59679073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1734174826d480fd0ca4221a27524fe98e871a54a19c068307ec6b8d151189d5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f763d27f0cca3eca63d032df25da1781edc10ad21bb6ec6472a87765b5d494`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 10.3 MB (10292413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2193d3bb29390a43b5fe3cf6ef36f5d049269591f33a3f65f1c3ebf33ea628`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f82edf0cab6319880f6003cb047a9679b2b534d136feeba495550f279df6cb9`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae03b3a868a98138feda4a04a1f015e865a3599f8231275cde4e2d3ab18157`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 90.4 KB (90354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4f2df40ce739fcaf54c09cdf8f844f97b7b89ddd3a009cf66056798e7a816d`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73fbf95673c18f9bfa0a30481eb45b538fec3995c608702a1c1d90e08da42446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9f83b2f6643450c6e9f512971c820c8345c704dcd2e8cc7a8756a02e736f86`

```dockerfile
```

-	Layers:
	-	`sha256:6c76910ec532300ba0ac33261e0fa300df86a2a7236c44063bcf717e3999b372`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 3.6 MB (3614108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48dd7f90c47288d683499a84f5abe7001a411496c218e1bd8e77b25b0888176`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4c13946a073d0e0d9f2340b836b54e9a9dba1f010f04df5dd200dbc7b1b5af23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59820236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c689286b6669d33d79af74959237011ecd70075c64056e24a6d02c270876d1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:51:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba456ea91fba33b0b2266f0965cf72ec30eb7f1d6c06aa2a1c64acb11287462c`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 10.1 MB (10073826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c8707cbc6b46ef363481729ebc07a939af077bb4b56fc62ac5a4ff2270d3b2`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba3130f7897eb800b59a9393f231600424ff257e4f3e7b2648b3541566c64df`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbc4bfaf80cebb772173dc6b7ebf4d6c65aa74b8a1100448ee711a7b11f0f2e`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 91.0 KB (91037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60db51e8517172f9d697f6dd3dfd52ed53bc5d6102dfde87d9d7b154e3f0f1ac`  
		Last Modified: Tue, 03 Feb 2026 02:51:47 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a0bb841aee3fa661b5cf22150ac560131f548d1e2f6de469929472a1cae8d039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad53c32ccedf0d4c008cbe8f0cc3fa2f71fa4b95414674e681a85c5e5b8f37c4`

```dockerfile
```

-	Layers:
	-	`sha256:130d559f8c021baf79e6466c9df7613170e752a7e5cd42a30367c9f470ca7e5d`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 3.6 MB (3615635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349032d3fccfe1a4b3f53e519f7c3f349aaa60303d81e595a5a2f73a422d2b63`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1b7cc3e8e887276f4b47a7a7f3fdb6a9d8ccad482d37c05d554655857987d25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61365948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a8a124a6dc9a583795fdffe09999ff8fe4b6724e1f73ee53a9cc663d7baf26`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:50:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b536877d3c0a030ad79a6593cd07fd6d9d694a4ee908632c85159f47caa880c2`  
		Last Modified: Tue, 03 Feb 2026 01:15:09 GMT  
		Size: 50.8 MB (50805135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151531fafaa44052b8ef62edab30c39e82df6362c327e633a87856cab112f38b`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 10.5 MB (10466690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c46322ddba400bbf437e7982be185466ac3a30b6c3e18306fb107df084ef6f`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2601d6950df113d96bbe256462649bc0356027670c0fdeeea1a36db50b8070d6`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbc29155f72161458e612a5e0f3deefd8c0b90f6c6b725d755d6cbb64fdaeb3`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 90.8 KB (90767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a58325440b9ddaee417a935c1ba847b99eca4326d8cbc0cfb83ad3ec4e62d6c`  
		Last Modified: Tue, 03 Feb 2026 02:50:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1a1c6b5b1309c9a6d397be72aec7d51df19e72b1ed14d8e559ddaac54b8d45a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834635029b6ce5298f9a745d504c4600d908f105eebe44ef56cca8eff573a1f3`

```dockerfile
```

-	Layers:
	-	`sha256:baf157ba5397d5cc0efb14f1b4af8b0e255ff3dcd41813d3551db6e42c9b6e1e`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 3.6 MB (3612056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190165ca7a14affd0179a3d6aa5c67852f9eccbb4f971c73979a03c8629c2d97`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
