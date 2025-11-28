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
$ docker pull neurodebian@sha256:cec27486ade4093b3aa428c2aaaca469fd8beb4ba6fb8763fe5365b82f0f3751
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
$ docker pull neurodebian@sha256:b992a1aba72afdfc4db3866656606b54502e0e0ed75a01c44a8bbe682ee0121e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59845829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f563a4f42c84971da0b2c7135fe04512f7525eab72cd63caf558ce9ce90d0e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:23:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:24:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:24:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:24:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332597ec821475bbabd342c180adc5558f6faa9683bd335ec7649caf6790c4f5`  
		Last Modified: Tue, 18 Nov 2025 05:24:17 GMT  
		Size: 11.3 MB (11269512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26214aeb11956a0b8f9ea005f79999e0946adc1929d07a7bd8507c65c1c7bf74`  
		Last Modified: Tue, 18 Nov 2025 05:24:15 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1e22a67666689cbfddc15036ea3d22fe64804db66109123f07325860301219`  
		Last Modified: Tue, 18 Nov 2025 05:24:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b704bd7e985830a1a0d113313768d0a910e543b5a7ca60276d1b194e80685de7`  
		Last Modified: Tue, 18 Nov 2025 05:24:15 GMT  
		Size: 93.4 KB (93380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6e53aac955ba1df60f5ce578bc327d7639298e2ca456a89c9ccb40c76e050a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9f0aa6ae2a3b9f6bc99dc5c0feec8475f074f7fe4c0d766974d79d9f279671`

```dockerfile
```

-	Layers:
	-	`sha256:23f36d2082ffa9462fe810209c8a7fac4c00fd13172d0a39bf0be5427074414b`  
		Last Modified: Tue, 18 Nov 2025 08:08:12 GMT  
		Size: 4.1 MB (4075236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d153fae45e633f80f2eb958081dd125343cd7528215d10d908fcef89a0ea677`  
		Last Modified: Tue, 18 Nov 2025 08:08:13 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:50a5a625b28c32c49bccd1b8d57923ee03ea30f76a7ac8f3389642470916bba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ac2181dd0537950d96d6b71f88ff00dd793b6457e2a1bc5e0d058cbb43684a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:51:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:51:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:51:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:51:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62390544d51e9e4e416e49b6d9beb1a6cc3c83979b1221df2a79f2ff23ea921f`  
		Last Modified: Tue, 18 Nov 2025 03:51:39 GMT  
		Size: 11.3 MB (11253505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bd7b45b845c00ce3b9f9b8550fd08ded78e3770e7b6b8c6594f1360627b697`  
		Last Modified: Tue, 18 Nov 2025 03:51:38 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1521afcc0a45d7d89d38fe3092052dab1c78fee7db3ab723626e2c7b2f37c3b`  
		Last Modified: Tue, 18 Nov 2025 03:51:38 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109959872cbd45e0cb947130faa31d3da05f5978e79bda669d4be8d31ae5d9cb`  
		Last Modified: Tue, 18 Nov 2025 03:51:38 GMT  
		Size: 93.5 KB (93539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f756360076a198bf499569584dd893dc71581cd8142f514a7fcae2b7f797f972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7320ee090c63c4ddbef1519e14e84705f7ca28c41758f1ebadd780630514b6`

```dockerfile
```

-	Layers:
	-	`sha256:7e1c5cdbbbea15f5fa8f04f34f1eafe471962d5b9f7d16a8a0240dd5c158c78f`  
		Last Modified: Tue, 18 Nov 2025 05:08:37 GMT  
		Size: 4.1 MB (4075478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f04f4ad24905c1c37df3cd350cc8d3cb49a3f52670111846504f97240995eb`  
		Last Modified: Tue, 18 Nov 2025 05:08:38 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:b6f14671d17cd5a54c06ebd8f12c443709475eb0e62f46cee85102c8ef88151a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5d236fa58b4bd4fb3ff0348bb61f1a831a62de744715a38961d7cb07394c8f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:59:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:59:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 02:59:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:00:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8975fd88545a557d6130aaf0939ec9d94115f11b7beac2c3cfbb4c4f95f493bd`  
		Last Modified: Tue, 18 Nov 2025 03:00:43 GMT  
		Size: 11.7 MB (11690134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc851a44c9f3c9f983ce75368901731b6ec4407c164ee071d7d980f036b22f0f`  
		Last Modified: Tue, 18 Nov 2025 03:00:43 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe683a35f9a9a79e411adfa0e8758b3ab5a011e16cd010feddf70124539be2da`  
		Last Modified: Tue, 18 Nov 2025 03:00:41 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecad0060cfe14dce44d058568b622d3bc352786338181af4107306f90ce9cb3`  
		Last Modified: Tue, 18 Nov 2025 03:00:41 GMT  
		Size: 93.4 KB (93410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0024515340fc9614a49927171b075de2297c3be5d3e668b6661e791e665f14f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da43d3bd5dacb12ef9c1b8aa391f77db5288843666a12bc67d8ec4e5ece03cda`

```dockerfile
```

-	Layers:
	-	`sha256:b1660ba43570c243d0bf22b1f3a4a49672b9d495e11d58e918bfabfe422fbd40`  
		Last Modified: Tue, 18 Nov 2025 05:08:42 GMT  
		Size: 4.1 MB (4073204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b36d81ea50f285f482a84cc2899f2d25fbdffa2b443e57944bd263e6886e283a`  
		Last Modified: Tue, 18 Nov 2025 05:08:43 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:d346efc1653ce69298b0583c215759f69e4c520b1687b306ae31ee696ee1ca62
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
$ docker pull neurodebian@sha256:c8ead1f42c634e681b9cdac2bf63ba48bc04ef8800d888bbab9ac6bc443233b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9ceed3d827ee121c147b39aee58e02ca8f8f14e9be70c9899aa69c0e4db108`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:24:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:24:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:24:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:24:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:24:20 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52f85a9e90a8b30122ba1fd3c2518caa5dfa52bad3467bf81a8895b3ef33d4a`  
		Last Modified: Tue, 18 Nov 2025 05:24:35 GMT  
		Size: 11.3 MB (11269784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c5250e45b37b7a4ff8c28cceb975c813e947b0cecc421a569c75cf55bb3c60`  
		Last Modified: Tue, 18 Nov 2025 05:24:34 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193261405425b3c59f2c41fb87d2b4d31680bf8592a977be1caf0a5113b36ae1`  
		Last Modified: Tue, 18 Nov 2025 05:24:34 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13be725ce53a3aa8771c7b171f351ebd4ed147048d82dc5056b9c1f81e85ac4`  
		Last Modified: Tue, 18 Nov 2025 05:24:35 GMT  
		Size: 93.4 KB (93374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee0f9162a0042d874a36b09ff302bd44f0f89155feccf6d3f925f58ec54e728`  
		Last Modified: Tue, 18 Nov 2025 05:24:35 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed9d4c3f6b45fcc01320121fddd661becdf4e23be51c8630c3bccdcb27c45d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ada510161ccd0cbdb6e2b1d71f378cbfe93e95b0896c977ac560e969d2f1c0`

```dockerfile
```

-	Layers:
	-	`sha256:abdc6af02c68406dc3e31ead91fc836045df6d11811540bdc969c352335f9a0c`  
		Last Modified: Tue, 18 Nov 2025 08:08:17 GMT  
		Size: 4.1 MB (4075272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a9eb26d88e694e6a18b0aa1414822b139d8020bb0108bdeb82201e5a65f8b6`  
		Last Modified: Tue, 18 Nov 2025 08:08:18 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:799a9fdaeac12508072ad286af1e4e7af48fdb6b90fa105569d75c585522decb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9196b72b4cef17624139168cb8a29ac1a83af665a592f750bb3c2721486de148`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:52:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:52:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:52:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:52:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:52:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8807214d6bb58ce93643f23da0d4f513c5ad5c1d7afbca79b7efed5365942ca8`  
		Last Modified: Tue, 18 Nov 2025 03:52:35 GMT  
		Size: 11.3 MB (11253434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6c6e4641d306f35a7865dc55f0617616dc6b1fdffcb7dc3efedf0737835a76`  
		Last Modified: Tue, 18 Nov 2025 03:52:34 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba37d77eb8f27c5b50207c5ded85c692607c6c8731c3646f7aa887fb707d9b4`  
		Last Modified: Tue, 18 Nov 2025 03:52:34 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f35d356531128f85210ebbce70caffc3b026330c2f6cf599438d5cc6fd6ca6`  
		Last Modified: Tue, 18 Nov 2025 03:52:34 GMT  
		Size: 93.5 KB (93515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a21ba5c85c56614c9af83a1aedff34ebaa1eb2f907abf5f9e128f2413b19b7`  
		Last Modified: Tue, 18 Nov 2025 03:52:34 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed1488b88f01f98361118e77ce3f25f9d4948315e0be7528e934b3f88bfb8bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4703273c9e0ef5f78614bb8691d50f70c13a6b84a97abe62174461caddfb7da`

```dockerfile
```

-	Layers:
	-	`sha256:ff89c214db7039e198f750d1504e92a410cfd11dc52faaab1c904d28bfb17e10`  
		Last Modified: Tue, 18 Nov 2025 05:08:52 GMT  
		Size: 4.1 MB (4075514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cb4ebb333c44656c1f30b692d638ce65ab8a9add9573811002d77ae7ef10360`  
		Last Modified: Tue, 18 Nov 2025 05:08:53 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:2b8d3d240bdf2e13a28c55a3342b49ba13fc0ceb8366f34fa9cc11f991fb02a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61253059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f231018d42fd321a780aaa8de73caa2d59d077695636f36a0cee80ee8f81bd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:01:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:01:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:01:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:01:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:01:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a93d0237e128ad08fcddfd034244077cd71dc323e8c25586ee8ee24728ec4d6`  
		Last Modified: Tue, 18 Nov 2025 03:01:29 GMT  
		Size: 11.7 MB (11690161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff35b78322711c76b309f998cde01420d157ca97747d0dca1c2f1303f2e4c85b`  
		Last Modified: Tue, 18 Nov 2025 03:01:27 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fce1d0ab5d7eed1f6fb618d4f905b41413bb9793db1989d6d8a7329d274744`  
		Last Modified: Tue, 18 Nov 2025 03:01:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbe045baa9269b254e517da9ffee8d4ba6c88e789fb777f5c77bc4120b4f6a1`  
		Last Modified: Tue, 18 Nov 2025 03:01:26 GMT  
		Size: 93.4 KB (93412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd1f28a6350b9b83efd2d573a2963eda9ec1c308dba86dd4c23ade9b1ee1518`  
		Last Modified: Tue, 18 Nov 2025 03:01:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:52ca226625f2cc7d0ec9f3f7a67f8c1a133b4d6d44935fa551176ef9f7c9e27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d398885232ce92f7fdad4175c8954f4a3fafcbfb91f3380e2bcc238b0788425d`

```dockerfile
```

-	Layers:
	-	`sha256:9eae406c595dd9fb241902d88fff47118b84928d56f49314f5e086ef1b4626a5`  
		Last Modified: Tue, 18 Nov 2025 05:08:57 GMT  
		Size: 4.1 MB (4073240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abb0e974253a831d2dc5b7732b8c9a0ea76c6d4ce502ff780e687782910c8a5b`  
		Last Modified: Tue, 18 Nov 2025 05:08:58 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:4a17725e892257ad4267fc45a29f31e2c2893d7b34fc4da4feada937b7169692
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
$ docker pull neurodebian@sha256:52b23456ab2f9d29fd759ecaf2e5a2541030add2851a9b053a51c2d867599c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7d7b6f18d2ebf89a1081e0b667b4c8a57cd1c4916e28e5a24d831549248bdc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:22:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:23:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027086a669e3187a5bf55f93556ceea5dd486b73a28bc08d86aeb65a70793707`  
		Last Modified: Tue, 18 Nov 2025 05:23:16 GMT  
		Size: 11.1 MB (11105091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d191edd77c0ae59bd17b0f6640a0bf2d8749774ef5877ce401308fc7547fed3`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18651e8f324fcd83223a52a2730112eef035e1ceb11219aa7de401d66434f20c`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977616fa4c9e859613cd50ad00c392b3a050ff5e4a7cef8078fad26854d79113`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 101.4 KB (101405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f3d82782aafc3fabcb0f4cd571387f5f0469eef5209184cb44f4f03e814e201a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f061182ed89de96f15a42206b239284ea10a77684e0117e45c8c83a75cee0bd5`

```dockerfile
```

-	Layers:
	-	`sha256:72e2841e7d8a353d852c2136dfde3cbb9389c533a5e49bdf8cd92300794ceed3`  
		Last Modified: Tue, 18 Nov 2025 08:08:23 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db020feaeee2fafa232e497baf959f91c0631ea5ef2f7c8f5db85e3332bac212`  
		Last Modified: Tue, 18 Nov 2025 08:08:24 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7a0e1a673379a86a94d3c2e3bdb42728b33fc4c251ff6891b1acd4a0ee392337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91a451e442d2e4459f8608f6798004fbcdecc5b1e051cc8175efd38e757b228`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:49:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:49:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:49:35 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:49:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722ffbbe605a785238ffca2eb8744eca1f0f76e1718902782cfa899d81515702`  
		Last Modified: Tue, 18 Nov 2025 03:49:53 GMT  
		Size: 11.1 MB (11106099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fb98ab4c345ad520c24eb6e96667d26e24c539579fc55b995d86777c6bb33e`  
		Last Modified: Tue, 18 Nov 2025 03:49:52 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea69364ab834cf76a2f1ed7a4892a53173db03de6c6957be53af710be6d154e`  
		Last Modified: Tue, 18 Nov 2025 03:49:52 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc8a13c0c8e09eea2ec7010f3f7c34d2f741e4026897300d421405d259332f9`  
		Last Modified: Tue, 18 Nov 2025 03:49:52 GMT  
		Size: 101.1 KB (101107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3130883b211251a00c8f3138872d2127f486ff9b84eb8de852200a2db4de557c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5b0b8e3b177bd5d484e96e7564af795d83a58c23b9e5d5059342292132fca4`

```dockerfile
```

-	Layers:
	-	`sha256:4dd6ac5ab9c023c50b5e8c1658a66a76ee36f0f03532fa710143b1b133af7592`  
		Last Modified: Tue, 18 Nov 2025 05:08:59 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ca9c35ba0c1fb4e0e1288a61902514b9b4d9045956de4d3b40fe5fa9dc8ad9`  
		Last Modified: Tue, 18 Nov 2025 05:09:00 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:5aa69718f1efaca3418c6d918472ccc3610a069dad9a5de8dec3ea485a595596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee264702ebd5954f33c687a868e40ef83a54e39bb0fa536e18202657530adc9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 02:59:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:59:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 02:59:02 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 02:59:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ff276d829f31f5253bbd1b7f53ddf75bfd6004f7fcc06ea8ad1b23a242b12d3b`  
		Last Modified: Tue, 18 Nov 2025 01:13:28 GMT  
		Size: 54.7 MB (54699599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad6c4930bd9f54fe6d2bb6d571f25016096ca17f5042810bd28ad8cd30e0587`  
		Last Modified: Tue, 18 Nov 2025 02:59:20 GMT  
		Size: 11.5 MB (11500406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e6ed60e67a01f2bd9eb7737b35f9071edcafffa6a7408cae777d51d9aa773d`  
		Last Modified: Tue, 18 Nov 2025 02:59:19 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba69b163bcb414900c226707b4e354f29cb924661cd161524e15552c784f5b6c`  
		Last Modified: Tue, 18 Nov 2025 02:59:19 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3ee899bbd601f3a72f64d5c1253c7739d0a559b58cd7d06c6c3fb6f3699916`  
		Last Modified: Tue, 18 Nov 2025 02:59:19 GMT  
		Size: 101.3 KB (101277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:31e9b963b769aa8402cb4f8e020e7d2d926e8589b11ccc0473e774492f589e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0865b8f651164a8cce85f937a8680f329663d66744888c46adf7d5ffa95c6c9`

```dockerfile
```

-	Layers:
	-	`sha256:ee00c44865291a391a9bcaf7b8de266296f6f9be6aa7c0b628ea626c63eaa1f3`  
		Last Modified: Tue, 18 Nov 2025 05:09:04 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:108db865401eccf5faad0834934c22e016bb182f2028e5f435587351e58dc2fa`  
		Last Modified: Tue, 18 Nov 2025 05:09:05 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:294271293f3a3b1b58ef6390a7af7967eac1f49364eb3be82ec4fce535c823e5
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
$ docker pull neurodebian@sha256:b5362f16c8bef59c161be65b8021f12f06d0bcf3ddb0a4b6a919891540bea705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507393086679db487cfe16d03c9f41a88eb355e0a27d1f0fa0b858110d6cd872`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:23:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:23:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:23:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:23:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:23:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556ae439bdcb8b47bec75f40f721c7ce74bc68d13285ae81e49f3d08edc3a67e`  
		Last Modified: Tue, 18 Nov 2025 05:23:40 GMT  
		Size: 11.1 MB (11105079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2112f97d5afa272740c88cdbbbac424ecf5d2fbdaa3203906800955ead6013e`  
		Last Modified: Tue, 18 Nov 2025 05:23:38 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742817595129cc418a0cc3abeae9c4c0acf9104674ef2cea757ced23c0a9c4a5`  
		Last Modified: Tue, 18 Nov 2025 05:23:38 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85410c47b996246a8855aadc2edaed772d3395afe5f1396e1843e715b6d238c`  
		Last Modified: Tue, 18 Nov 2025 05:23:38 GMT  
		Size: 101.4 KB (101378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3422aa1f4f380d754a9c44531abd048ad4dc1c3f3fd1f70900e176c8f9758a2`  
		Last Modified: Tue, 18 Nov 2025 05:23:38 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e6c7721c3a90d1bb3162f7255d43d777cc2cb06f9dd1c7a9a0b0a49f835678f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21ae0f35686fc72f57d385dd548eb3e7ff39a0d27c04cc1c81dc7e2ff2545f6`

```dockerfile
```

-	Layers:
	-	`sha256:3378751582ec403ee5b1043d29bb0868f75dbf736b7c2bc80ce43d58aea0893a`  
		Last Modified: Tue, 18 Nov 2025 08:08:29 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7bfaf79598970461a37decff4cf866e509c8fca018712f99e2c03f4443a6b8a`  
		Last Modified: Tue, 18 Nov 2025 08:08:30 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:43921c44590d322ea3a2200551d5e4cd52721ac1eab9a993940d6502a91cde14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f12c8a424ceaf8c8108c2caff5e386aaf192c375945faf61f353be561852656`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:50:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:50:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:50:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:50:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:50:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062c2b3ce83caad4b37ac1e7102fc1fccb79e2c6fa03b1c809c88fdf9800df8d`  
		Last Modified: Tue, 18 Nov 2025 03:50:50 GMT  
		Size: 11.1 MB (11106024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374c795581cfa6a07227e0c8adadafb18aad92ab4687691c420ef8bce3905149`  
		Last Modified: Tue, 18 Nov 2025 03:50:49 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac04a8b962c8a03ae75c44fe4910852f14b54684a668dc2c85c4af38d23ee22`  
		Last Modified: Tue, 18 Nov 2025 03:50:49 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc1e68c8213d3d297e1e6dae792d728019447243ab71ffcd7b55daaa8014d33`  
		Last Modified: Tue, 18 Nov 2025 03:50:49 GMT  
		Size: 101.1 KB (101113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55940f735946c2165111b6142e534996c25a04f9f49ad7c4f9258520c46db14`  
		Last Modified: Tue, 18 Nov 2025 03:50:49 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ec92181c786d637edc61066712b4fd1a4bfa44f14b829347814a0995f92a377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b320f6bbd5e202338100a948bd681dab926c6680c6668b9e9c8b356ca6b36a4c`

```dockerfile
```

-	Layers:
	-	`sha256:2329ddc9b423c293e808126b639e5506f6722f297c6660fe4fb982ae665fe2eb`  
		Last Modified: Tue, 18 Nov 2025 05:09:06 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53f59167813de90e0d35b3758f73c7d1cb28273148c1c33923373754be604b2e`  
		Last Modified: Tue, 18 Nov 2025 05:09:07 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:d006be0275eaeacc066e7c1abaa4162b0441e35d06c5379d4bfaba35d726f029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da139b3f0b4fdd084098e6b854d27ddf4938477b28b064d3976600ed6b02ee4f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 02:59:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:59:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 02:59:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 02:59:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:59:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ff276d829f31f5253bbd1b7f53ddf75bfd6004f7fcc06ea8ad1b23a242b12d3b`  
		Last Modified: Tue, 18 Nov 2025 01:13:28 GMT  
		Size: 54.7 MB (54699599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34469d4c6ca4dbf4ca7c8b004510f5a4d8e65a6c741c78d358e654c585925090`  
		Last Modified: Tue, 18 Nov 2025 02:59:33 GMT  
		Size: 11.5 MB (11500397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b78335af44e7378b37d0d3942b21f81ea7df0b78b02cd8976ac4b1e05ca9770`  
		Last Modified: Tue, 18 Nov 2025 02:59:33 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9cf98358c9e5929b880c3bde56350327837146f26e234f971a33cbce4b264b`  
		Last Modified: Tue, 18 Nov 2025 02:59:33 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55446bca2ac686c36703461bc98ec398278137e80fb2be821f9b461f530ba7`  
		Last Modified: Tue, 18 Nov 2025 02:59:33 GMT  
		Size: 101.3 KB (101295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fb474d5a9aa8943ecfe880e17031d1d3cf2994ef46944b562887b34a9688c7`  
		Last Modified: Tue, 18 Nov 2025 02:59:33 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0773445db0bee45b7afb385282eeb1ef903ba46b512d9dbe03af455d1086959a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751d385b351522bf7506ec4d98ee5deff26beedd0293f50f99efda08ef287fab`

```dockerfile
```

-	Layers:
	-	`sha256:42a7737f79e78022f2cc02f43fd5fe92aa0d20f085e4132c32862c94618bfb43`  
		Last Modified: Tue, 18 Nov 2025 05:09:12 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e6a8129866aeae07bc265478b80a0f570896460cc1696db254e67a6601b4238`  
		Last Modified: Tue, 18 Nov 2025 05:09:12 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:edb0c941528b9c8bfbb6a1fa482f0f5f1ae301e2572f450c19f373cbe5ca834f
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
$ docker pull neurodebian@sha256:366043713c7e6c0f03a9162bdb0a9e212e53a24123d07737478413ab4748d081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60181684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92dd0de9504e0bbe4409feadaddfb844ce08396abb0240bbc740a26215a3273b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 05:25:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:25:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:25:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:25:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76694dc296168bbffa890c84fb372e9c250bf33e0ad63a6146b169a57d983e2f`  
		Last Modified: Tue, 18 Nov 2025 02:29:31 GMT  
		Size: 48.5 MB (48500434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a49a253a05dd471c0e155f0f4f91ccc25fc59aa6c7bd527b323117b5250122`  
		Last Modified: Tue, 18 Nov 2025 05:25:52 GMT  
		Size: 11.6 MB (11588572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f16a4357781996ad9405179bea144b87856496993b9d2465452eedb14b76c8d`  
		Last Modified: Tue, 18 Nov 2025 05:25:53 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fe7c5d321e038a5990a22a2794a9547dec8a5799070ae3bede181248aee6b3`  
		Last Modified: Tue, 18 Nov 2025 05:25:52 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd9cd7a5c6fc267eff9196ac84bf0b83ad2ae80012b3d0bed5097cd7ce35a60`  
		Last Modified: Tue, 18 Nov 2025 05:25:52 GMT  
		Size: 89.8 KB (89776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f6ab5e45c7d79f972e35364b00e1e85380de600340204f791446433806794927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63c79d811b1da0bdc1d1993a6713d5f35d3b1fe5ddb60cd02a9272b93c89567`

```dockerfile
```

-	Layers:
	-	`sha256:d4326f39e0f4993ebbeb784b9a60db70483b40b2a3fe5331c79ad0b853782ac9`  
		Last Modified: Tue, 18 Nov 2025 08:08:33 GMT  
		Size: 3.6 MB (3577401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:727dabe4e2300565ad3af0d1d71e64f1dc685726f00be034d66a37cccd3bf876`  
		Last Modified: Tue, 18 Nov 2025 08:08:34 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0240320d50e0a735877ce9c1b680fc83383e5270c5252f3c5a6bf75773613d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59939892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f450dccc1910f9ea53442d037d9c07d6ea9730ad8afe22c7e145b5abbaedbbae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:54:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:54:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:54:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:54:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:25dea15c4ffeb70e1112f1ee06dd948a8ab9dfc3b79ef239cb96080cc27ff1be`  
		Last Modified: Tue, 18 Nov 2025 01:13:47 GMT  
		Size: 48.6 MB (48591184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e8cb6f2050f012301a38350d5b24e1d46c45d720d48514c166af2fa18ea87b`  
		Last Modified: Tue, 18 Nov 2025 03:55:06 GMT  
		Size: 11.3 MB (11255308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12dbc4a5a7d2672202d31ee9d7b29cb5d29a06f08566f247a363e2a63cb672a`  
		Last Modified: Tue, 18 Nov 2025 03:55:05 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccded1fb17ef0c142f8ae7bf64a99b345608c6adb5b81d14998da21c5d8e1a35`  
		Last Modified: Tue, 18 Nov 2025 03:55:05 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b042a4e6d45996fb48df60228a59d091830538e87ac00c0c3658e24d51ff587`  
		Last Modified: Tue, 18 Nov 2025 03:55:05 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d3b1559336fbc2de9e0c6065656e01b75ce0df387ba7457fca8fe58753121d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8978b1b94f45f5e132e11ff42fb8cdcf5277ac0ced6a06a87f419ef33bf4098`

```dockerfile
```

-	Layers:
	-	`sha256:b86a5b4eac17beb5568c3a961e76e6ffd482a8fc5ec835e684237bf06a5cb8c3`  
		Last Modified: Tue, 18 Nov 2025 05:09:15 GMT  
		Size: 3.6 MB (3578277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe1379a897c2fa408e0db91fe9afff334ac85006ef732f63644534ff4740f523`  
		Last Modified: Tue, 18 Nov 2025 05:09:15 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:9366598d8a26fb7d7dd14cd014de708e079a3f843b4c78957d0e2679eae472a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61659763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db37c76901f7f42765728dbcbe87d2e8d8ca7d08fa2840b5a41eed82241f696`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:03:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:03:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:03:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:03:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:898cf630ac245ec9ad865c96204520b86bb7b8760d5bd2f14bd02745e43d82f4`  
		Last Modified: Tue, 18 Nov 2025 01:13:40 GMT  
		Size: 49.8 MB (49832238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c99ed386714c4bb450506732ee810d85aab0f3dda4715c62ff3e15a4836519`  
		Last Modified: Tue, 18 Nov 2025 03:03:26 GMT  
		Size: 11.7 MB (11734481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fa4cd2f7a74e88e9df00cae2773c07d4f1b3ca5896efea246d4fc9c3d3b3fe`  
		Last Modified: Tue, 18 Nov 2025 03:03:25 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5326d561abb9377288ec05ed7812d09e6ad68ee1ffc3de192c6f36932e161aec`  
		Last Modified: Tue, 18 Nov 2025 03:03:25 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d381cf813812673b11780614a577a1610403eacd68b7a3a520cf58035f4591`  
		Last Modified: Tue, 18 Nov 2025 03:03:25 GMT  
		Size: 90.1 KB (90139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2496c2ba33112048fbc1b81a7e227709bb6d6dfebe4a95a1255c75d60b255087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0158a608fc9a1d83a4d807ed24061af7eae148722c2b6ee838a398f41eebdc4a`

```dockerfile
```

-	Layers:
	-	`sha256:509c1cfcd262c48dcd9ba2791f9f220ab486ca9b0d97c7c174a9264ae3597447`  
		Last Modified: Tue, 18 Nov 2025 05:09:20 GMT  
		Size: 3.6 MB (3575364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaf47288a7336f776c2fd7ef0a4483fd2b5da91c83ceb5d5ae52968a4d81d32e`  
		Last Modified: Tue, 18 Nov 2025 05:09:20 GMT  
		Size: 13.9 KB (13903 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:99748e3801a87ca4754f030cbe146f3d2d61e73399fe09d89e6d2fb75c3ff494
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
$ docker pull neurodebian@sha256:feaed26b03c949d0932e37e6e74f547fa6f99ad36f56d1aaf9574b4303d94193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60182204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567098fb1b1386891c3045fa629bf7193516c5be3c1e7ea4583b46e9f125f01e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 05:25:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:25:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:25:38 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:25:41 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:25:41 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:76694dc296168bbffa890c84fb372e9c250bf33e0ad63a6146b169a57d983e2f`  
		Last Modified: Tue, 18 Nov 2025 02:29:31 GMT  
		Size: 48.5 MB (48500434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6f932371b762d4ebd76295ed523041ce96b651c8d6f99058e56fde0193577c`  
		Last Modified: Tue, 18 Nov 2025 05:26:05 GMT  
		Size: 11.6 MB (11588603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb95424eca70e0b48eb1362dc9faf54d6cf60c34acb74bebc377ccd001eb0a5b`  
		Last Modified: Tue, 18 Nov 2025 05:25:55 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751758c3326f3120503e1065f2ee9d96dab1645821c5d9040b49ea54b7e4b182`  
		Last Modified: Tue, 18 Nov 2025 05:25:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e407f8ac8dd6b87d5030356d06d625859834a1b2fadc44b8b309603476fa0b3a`  
		Last Modified: Tue, 18 Nov 2025 05:25:55 GMT  
		Size: 89.8 KB (89813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bf0c4c970ca715981804e3d2797bc8cc57df79fc87b3e0d8f079f416f688ad`  
		Last Modified: Tue, 18 Nov 2025 05:25:55 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dd9844cc45fbe3e9de05e6c77c740d47a5f577608e3b189b07fb86b1cb4ee288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85735ebb9f37ee391cb4778514b2f1e223e828f04d47c74fdf38f6a08dde99c8`

```dockerfile
```

-	Layers:
	-	`sha256:938f600c2b882bab1eac886bc2abee6d9baca24359cb1c9bc53463214580ac7d`  
		Last Modified: Tue, 18 Nov 2025 08:08:40 GMT  
		Size: 3.6 MB (3577437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0cccbb40e13d48227175631b605120ebd5591330729672805e5b424dfb34585`  
		Last Modified: Tue, 18 Nov 2025 08:08:41 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:64186adde6428fae5c84a5002a30127063d0e3db638a8e2a0ecf21ba6744d014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59940274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2540b57cd8e8582e9238a43716c2655c40d1d64033d51b15977395dfd3a37fe5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:55:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:55:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:55:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:55:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:55:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:25dea15c4ffeb70e1112f1ee06dd948a8ab9dfc3b79ef239cb96080cc27ff1be`  
		Last Modified: Tue, 18 Nov 2025 01:13:47 GMT  
		Size: 48.6 MB (48591184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7442761efa65f5c2b8ea533bdf899a42a7675c104757f17e02556f4fb8e9b1`  
		Last Modified: Tue, 18 Nov 2025 03:55:30 GMT  
		Size: 11.3 MB (11255244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48646b8eda1068da8aaed34b5cab1846deb098a42975c11138a3a5949dbf2b40`  
		Last Modified: Tue, 18 Nov 2025 03:55:28 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74eee381d7f6529a319746474450b633a97370dce62728e2ef7ad068a023a2f2`  
		Last Modified: Tue, 18 Nov 2025 03:55:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7d4af7149a94e629b6505577fcbe8866b4bab79ca6f413e0a47f39515ac258`  
		Last Modified: Tue, 18 Nov 2025 03:55:28 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6cdc60206bb5f64f8f48ac0b1ada92e0746562966eb4588e033f00586bfff1`  
		Last Modified: Tue, 18 Nov 2025 03:55:28 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:30e70f2997d786cd98e0bd721ece2fe2b7fa22520c9e84c2a97875debc9767eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6882a6e3ee02ae9ae4109396d8e989351a7877d8e2876e150ad3670ced3c95`

```dockerfile
```

-	Layers:
	-	`sha256:4d89ca1be6665cdfc905578b87af2c5bcc78c8cbab78dc211a784b9f6e401e1b`  
		Last Modified: Tue, 18 Nov 2025 05:09:24 GMT  
		Size: 3.6 MB (3578313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c76a11b7847af5b890757dc45a0626a35c12771f24ac9352bf5efbde44662bf`  
		Last Modified: Tue, 18 Nov 2025 05:09:25 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:5af48f027b4bf48cdee6090d22551922b9a844d5d5a07910d479a440e699496a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61660272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9346116137dfaa71689745f00f12a0b4289514a6e182a2e5ca85439dd3403175`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:03:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:03:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:03:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:03:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:03:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:898cf630ac245ec9ad865c96204520b86bb7b8760d5bd2f14bd02745e43d82f4`  
		Last Modified: Tue, 18 Nov 2025 01:13:40 GMT  
		Size: 49.8 MB (49832238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0b6295fb3a0de9675da59780f9f04f82fb6dcdc2676ee484a93d1d29644c69`  
		Last Modified: Tue, 18 Nov 2025 03:03:50 GMT  
		Size: 11.7 MB (11734522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d910717d3eb8247dc5797a539a4501e15f2baabc57447b9e40100725d7bf149`  
		Last Modified: Tue, 18 Nov 2025 03:03:48 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac3671e7d327a12e834092b1f44ca16784cd66ea96c40cf45f0398e1b99af04`  
		Last Modified: Tue, 18 Nov 2025 03:03:48 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f22aff5a131d31db729bd6138d046dacb2be96f9ded5b0c4d416274d261cdf`  
		Last Modified: Tue, 18 Nov 2025 03:03:48 GMT  
		Size: 90.2 KB (90163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a543a8735d0a34b0f63dc1dcaa2ed6d8f2db203b8b5c1ee2d951c571b57353`  
		Last Modified: Tue, 18 Nov 2025 03:03:48 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a0f6863f842eabeed89212f42d99ec2925a2ff7a135b4e11706b9828510aa27d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2041d6b5f4b3615ac3cd6a4e876b23a9a9d37bb780b40e3482302391c9b87358`

```dockerfile
```

-	Layers:
	-	`sha256:6f42b733b57f390b5db85df406b02ab8db246d4befc1ad0cc48b1305eb6d15dd`  
		Last Modified: Tue, 18 Nov 2025 05:09:29 GMT  
		Size: 3.6 MB (3575400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4d1f5346f232ba860339a91bb3c9310d60c2691ca72115e3462cda0ecdd79d1`  
		Last Modified: Tue, 18 Nov 2025 05:09:30 GMT  
		Size: 15.9 KB (15928 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:0e98bbc3daae66df44ae11a5588f2309b4d0b0a3d5759a236557a26319c2c5b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:e6772d070a574f00e1ad07efb0f799b7e9d9020fccf9887c7f6378c50bdbe816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d6aeb77e4a5a773edcad5fc10b5e08d8f387161a9b7b5d93e1cb1aac4e3735`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3881e591a9050bd6250b7975f2a62d69ce9d4bc181a569e43d583973bfffafd6`  
		Last Modified: Thu, 13 Nov 2025 23:31:35 GMT  
		Size: 3.6 MB (3625726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7763c1732252c316b49e1a5ebe3d01e0ad636198993b3e20e7267f9fe62d4283`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59987cb0b364dad0627b12e7ef72104aea08b23fff39930f94dac5b79cf2585`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91714d8e9de2a6eab65bf534a21daeac5f710d6f823714736754481479f25eb`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 111.3 KB (111253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:74faf561f221e4ff0722a9a6a5469d286311b0d29d710a50c1c2f2d408089335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5093bdb0233d5e701687d2c9157af64b57724e81b512be660289bb7a4c8f7216`

```dockerfile
```

-	Layers:
	-	`sha256:288a50939bde1611937533ae039c8544b98d95d75331e8bde2456927a7ddea17`  
		Last Modified: Fri, 14 Nov 2025 02:07:40 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:941444796f9904d69ff28378466addce903b01de5df5c0c291ea8d117c6aff74`  
		Last Modified: Fri, 14 Nov 2025 02:07:41 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:09ed49f28825e5330d749e8aa583e2f0c2c88ace7f935f79fd1b4ee7cfd6502a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31094789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170be1c0c9e62fba389535f45096cb097ffcd73e82e10f8e5f2bbeb7101e7716`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:30:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:30:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:30:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:30:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4fc061e7db4abc03b992399d4d51a6e96a401904e29c8c7cfff6c2b0ef4cbc`  
		Last Modified: Thu, 13 Nov 2025 23:31:03 GMT  
		Size: 3.6 MB (3598146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e356cef2bd87e42a124fc4d5e82057772ca5cf202c6c194f6884f04283430a`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7f921b9372d265e8d3805815b0e98436f5f4b92fc0dae86070b7f4f269f992`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562a8628e6dc417f84896302f26a4b6c43f921ca7ce9b73b785936f7e5d51be2`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 110.6 KB (110588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4d3a9691d374823b1b504cf09f6f82049355ef10aa41d07d3be46ed00124eda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb368a6d54f82c2cad7c303b49a01491c62b68e3a47065952793b1df828ae`

```dockerfile
```

-	Layers:
	-	`sha256:c8a0004225abd4f8c618461be1e72c1192172f7ccfd4fa7f0839dbdc35d24f43`  
		Last Modified: Fri, 14 Nov 2025 02:07:45 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:200a3136b60277a7c0dac564342f17944ff690ca89305553d8bd0bcd74108f3a`  
		Last Modified: Fri, 14 Nov 2025 02:07:46 GMT  
		Size: 14.1 KB (14056 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:120b8715dd3a26a2af4049512591dcbb112d36e4accff9d7fded93e27ce47062
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ef9dcfb5426525d36ca828760110823e06e065cca0c4ac0682d0a506e9cf12e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33276245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abbe750921d6da2c2bf91fa655875aa86d26da7d2c93cd08dc4d8b4f91445af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3881e591a9050bd6250b7975f2a62d69ce9d4bc181a569e43d583973bfffafd6`  
		Last Modified: Thu, 13 Nov 2025 23:31:35 GMT  
		Size: 3.6 MB (3625726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7763c1732252c316b49e1a5ebe3d01e0ad636198993b3e20e7267f9fe62d4283`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59987cb0b364dad0627b12e7ef72104aea08b23fff39930f94dac5b79cf2585`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91714d8e9de2a6eab65bf534a21daeac5f710d6f823714736754481479f25eb`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 111.3 KB (111253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87663c843a43743cb4efbfd154e030c6591b4085d0c1d047a156158b9c47142a`  
		Last Modified: Thu, 13 Nov 2025 23:31:58 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8b9b5e291adc948bf145496030828a9a408c3399355380347b0ff72c16e2a880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970a1d784b637f4a06999658bbd7cfd5f71517ef14610d1888be4fc2d5614399`

```dockerfile
```

-	Layers:
	-	`sha256:19ad39194fba9b75b47c96c260e5431b390f0c1f40747e8857c995d53dd228f0`  
		Last Modified: Fri, 14 Nov 2025 02:07:48 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd46be2a48617b0b0891f5fe27958f8e2350a649da215ce9a4995e5a9a62d43d`  
		Last Modified: Fri, 14 Nov 2025 02:07:48 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8c05f54ab64c544f5b1833f0d31ef94804c914c6debd693acfce0dc0320660cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31095110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2b987bf931381f750375f7be732736b38d67dd928c373fb3ac7f7703364fd3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608dccde847e272476e52044e62fdf40902fdf981eba3f9e853d9bb36c3ebdf5`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 3.6 MB (3598157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff367c25857e7c190e4c69803b560c6e428a2f6fdcdef7291ed9c54595fd3a7`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d785e7ece3388bd939c0607e15ed02803f8e48b590bbf43d7b628f2275ed86`  
		Last Modified: Thu, 13 Nov 2025 23:31:37 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411f09f71214f6303934a66000e111fee3918961b6f6726ed9b784feeceb7fcf`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 110.6 KB (110611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa2aa73e9807dfaff0d65e73fea59b7275dac6754311bac380e78c75cf4c922`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f02cab47a327aef8e9eea19cc7a8da708ad76b7fd1cee2ccdc47f302f2cade08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5d2870c8ff27e82579456117c17077c9ecc56cf9812adeb91b20dcd8fdb489`

```dockerfile
```

-	Layers:
	-	`sha256:196e2a812f54eccdc16bfcfe68a337ef2397641ccf3672d5f6846a2c19b4a34d`  
		Last Modified: Fri, 14 Nov 2025 02:07:52 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be4dac85cb072f2caede51d4767494f8e063e10991e49a2febf5e030defd53e2`  
		Last Modified: Fri, 14 Nov 2025 02:07:53 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:018039aa28469cb574577be011ffba1b39df9ca46864a220f31a05a376249830
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
$ docker pull neurodebian@sha256:a6b82875250b39bce69a473895862362fc6c0fc619b8aa62cecbc36ddafea16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59672386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44fc91da823f52c537b6e13a4c462a693e58d4a8ea793dd62e90e451905af64`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:24:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:24:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:24:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:24:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbc7b1c2d62df985e7aff96ee3ece36abe8cf517d7f993fe66c2a5d85e28a00`  
		Last Modified: Tue, 18 Nov 2025 05:25:09 GMT  
		Size: 10.3 MB (10289731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5364e6fa5c4502194ff9ec23ca3d5e09b80eeccc4f4f58584beafec862b4f8b`  
		Last Modified: Tue, 18 Nov 2025 05:25:06 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e3e7f0c19fc5bfe238e52366df56925c734e376f238cc681974db438f32253`  
		Last Modified: Tue, 18 Nov 2025 05:25:06 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1ca7993e2d88612125c1707875d1da317111bb55e9cd88b5bbe786067453a7`  
		Last Modified: Tue, 18 Nov 2025 05:25:06 GMT  
		Size: 90.2 KB (90204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:df927e54faea7df4d76f3a405b8d22dfe4a687c81abd444f5389a9d65bb4aeb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2d4278a656ee84173516bbd88d5c411730eaca56631895ecae5b804adaa9a`

```dockerfile
```

-	Layers:
	-	`sha256:3c0e4dc230c96b33215e0db6946acca5920ddc0b14b5270e6497a701a792a37b`  
		Last Modified: Tue, 18 Nov 2025 08:08:51 GMT  
		Size: 3.6 MB (3613029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c182edb049488b2af0cf55dff839e72d56dbd8f86a9812723dc44ca3903f66`  
		Last Modified: Tue, 18 Nov 2025 08:08:52 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:03f45755a0cbd0fa591dc83b3f174f408ec09689438dd1f600685d2cde3859bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec1e38ad20d40f39f7b16d2bbf5d3dcaddb31d59c129758a0bf91ac4a087408`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:53:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:53:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:53:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:53:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39eff5378ff39f272aafcd4e6eb21f0002984d7ba123df62005a1c72b904f39f`  
		Last Modified: Tue, 18 Nov 2025 03:53:24 GMT  
		Size: 10.1 MB (10073386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7768b0faa974ae0a24a5fc2d6d8ab83d8bfbaac5c1c6b88142e79c4e9331d292`  
		Last Modified: Tue, 18 Nov 2025 03:53:23 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4803b1be5a4e9ea2b53fa1893acd4bfcfcc977b674beb4d6c9df3d231a97eb4e`  
		Last Modified: Tue, 18 Nov 2025 03:53:23 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239af7ab87748df14555e1392f8dbd23b17160c367fd5fab152ab0d11134d812`  
		Last Modified: Tue, 18 Nov 2025 03:53:23 GMT  
		Size: 90.9 KB (90895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4233619c2439c669dcbd798b18d3779f25a61d90424651cd1a47825c92259fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c67bfaa7bdaea4ffbeca1e70fcfdbd3beb9885e4ede0de846eb219c971de3e`

```dockerfile
```

-	Layers:
	-	`sha256:105073c6ec3e7f5c078d5e10ecdbbf90eaf703f3743f3044afb9c8e051305965`  
		Last Modified: Tue, 18 Nov 2025 05:09:31 GMT  
		Size: 3.6 MB (3614556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfef6ecb903761ecd001f5326ba3ebf4549b1e7fd94a1e645e8f1707779545e4`  
		Last Modified: Tue, 18 Nov 2025 05:09:32 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:17dfc4286fd752b3d3d0bf9fb20d8810070cd8191073f82eaa5374a0e65cbccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4b5d6645061105ccbb028eb3fefe29edfa9a55b0172aa02ee45104cffd1993`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:01:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:01:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:01:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:01:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bf2a49c122745d1757b9ecb1c9b1d8252491e66b62d1c279080155aaa530a615`  
		Last Modified: Tue, 18 Nov 2025 01:13:10 GMT  
		Size: 50.8 MB (50801744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e17a20228b22b602cbbfa5680fffb9f4f423b2b773d66726620a3e615f494c`  
		Last Modified: Tue, 18 Nov 2025 03:02:14 GMT  
		Size: 10.5 MB (10462815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d43cb3b26404265a2415ae726de37e382f8bca2b3573d437ed0af59780d869`  
		Last Modified: Tue, 18 Nov 2025 03:02:13 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a98988b1a0d709c24b8a75b233813c646170d9954599a23bc28f542a481ccce`  
		Last Modified: Tue, 18 Nov 2025 03:02:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7df26ae6119f7ad73c3e54631b21eeca4094687be7a3ef5df86c7c0077dac9`  
		Last Modified: Tue, 18 Nov 2025 03:02:13 GMT  
		Size: 90.6 KB (90602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5cb23b9eed1f0fee69d391b347817aacd1bb16034b6dc063849bb4362d18bec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a0c9860b662de961e7066a34a6cf69a21b4362ea5bc02fe635ad924a557071`

```dockerfile
```

-	Layers:
	-	`sha256:4d4d4e2a77ef0acaa1a67ff1b69ebcc224babe7fb3cdc53b737a11cb53e2332e`  
		Last Modified: Tue, 18 Nov 2025 05:09:36 GMT  
		Size: 3.6 MB (3610978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0491f3d73f6c0769dcbd447cf474664a488215c438ced43977ad268347ba666d`  
		Last Modified: Tue, 18 Nov 2025 05:09:36 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:f6780519431067a744bf9cd5c67a3af9d80bbd6705a0e17b784ae3d117768809
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
$ docker pull neurodebian@sha256:7e4dba6577c604f109e75c30cf20e4f6fd699286502fcfb453b4bfb22cb48527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60182085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73970ee9b45105fb655a0dde7518d96ca729ff9ba43a0ca4b7338c67060af4ff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 05:26:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:26:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:26:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:26:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:63fb544511bd02db3b85f4aa7407dbf6c6f5cd7cb1c0c1e65d055477ac245bcf`  
		Last Modified: Tue, 18 Nov 2025 02:31:43 GMT  
		Size: 48.5 MB (48500427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd6e3358f9a9d38391f078b89e94e4fab3194e262c2c4912482c748b3dc375f`  
		Last Modified: Tue, 18 Nov 2025 05:26:33 GMT  
		Size: 11.6 MB (11588927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ae8f61696c3e71e17c0f2c9c8a0fa545b960d97eea442de3dad605fd6be80a`  
		Last Modified: Tue, 18 Nov 2025 05:26:32 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1577d641287ece0d6f861e7b6ea8895e1625249c9fe9a5e35508a1564ad2186`  
		Last Modified: Tue, 18 Nov 2025 05:26:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44c99b2d280c8613effd222ebbadc96bb2d7e02b2fa1acfee6227b830b2dbb6`  
		Last Modified: Tue, 18 Nov 2025 05:26:32 GMT  
		Size: 89.8 KB (89829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ec8497f0bd4ec4c67fabbcc277e209ddd51f1bb88ec8c6f83ec88a45d5939ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9ef28067c818eb96ef79ef4d952d161d5df5ef05746762cded700e6b46ce62`

```dockerfile
```

-	Layers:
	-	`sha256:bf147eec738b6618cb9898c72065974527c1f91c9ab72bc2312754d3860265ca`  
		Last Modified: Tue, 18 Nov 2025 08:08:56 GMT  
		Size: 3.6 MB (3577395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd1a1293a55e0d1e1951acdc9c5ad6a34ada3007054ae1b7e0ce609fbc96ab95`  
		Last Modified: Tue, 18 Nov 2025 08:08:57 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:541357f0ecf1813a8cbd720ff8f96f2cd982d89fd4bc89827c69d551b0163a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59940394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45372882da5d68ae7df8f8d65d5521dcd46ddef2d90a0366725a381de0b94cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:56:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:56:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:56:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:56:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2b90f6fb16dc868101354a233036d6d70e13cd3477e4df5ab59f2ccc8607c1d4`  
		Last Modified: Tue, 18 Nov 2025 01:13:53 GMT  
		Size: 48.6 MB (48591389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2c0b4f8506d03d13edc8f4045814717acfb0bd4cc0328aae44b4d8f1bb7d1f`  
		Last Modified: Tue, 18 Nov 2025 03:56:30 GMT  
		Size: 11.3 MB (11255621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02b54aa8ab0ab54e708c0c245ecdc268d95f50763ee5e6a6ed6a4adb1d2b80c`  
		Last Modified: Tue, 18 Nov 2025 03:56:31 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137f7f093c10ede28087087e92707167136eed0692d4cb8a57ff45159fe7ab43`  
		Last Modified: Tue, 18 Nov 2025 03:56:29 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2204582058e6da481caf8d806747650c50de23d03051094ad0639f303ac14315`  
		Last Modified: Tue, 18 Nov 2025 03:56:29 GMT  
		Size: 90.5 KB (90480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fde860d58516366ee33015d1436096dd5e23e8f17964da184f085573fd9cc39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3ab53141102408437089c3592249acd27598f72cfda4ae449b0b6ce85fc3a7`

```dockerfile
```

-	Layers:
	-	`sha256:3124dcc841b669bd8bed1254d0af82173424f14bc28093da966b9fa449b12735`  
		Last Modified: Tue, 18 Nov 2025 05:09:40 GMT  
		Size: 3.6 MB (3578271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2859914cd0af245c67d2aa284e5b6e40a46c065c99688f18da5d11a1320ce86`  
		Last Modified: Tue, 18 Nov 2025 05:09:41 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:cf250cb431aad9ebe2b195e7d6e846fb7684629d0bb110655d9b36c9902c9895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61660804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52b9c65d4da4a7a8580d37a51890774004410d2d1e5c564e1dd6c82e528a45c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:04:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:04:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:04:28 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:04:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b1df74e42eaae76d71bf2c2aa402328d711dcdb63b4080ae4e7050388c00bad0`  
		Last Modified: Tue, 18 Nov 2025 01:12:57 GMT  
		Size: 49.8 MB (49833161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b695f28e24e29bb497155794be92fb6864604ef5dcf9c7b8df607b037003c3`  
		Last Modified: Tue, 18 Nov 2025 03:04:46 GMT  
		Size: 11.7 MB (11734531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c7ee6a50715b7cbfe05ff35e8bc76866ea39eed7bc2312aac9189a98e60b4`  
		Last Modified: Tue, 18 Nov 2025 03:04:45 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698291bc223fcddc6f726de48b27d024db48b81354767ae1e7c278be80cc8c7c`  
		Last Modified: Tue, 18 Nov 2025 03:04:45 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c145c0389a87f3aa4c268694c98e50f6b0661557e0f4bd035134a4b8ea4858`  
		Last Modified: Tue, 18 Nov 2025 03:04:45 GMT  
		Size: 90.2 KB (90211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:100db007c6b4b3ad449b053788054967155478cb079a7ae6b46e829e8e338726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace921b5ef700155ccd0cf3b3785a2c55a76118407491be2df5d0a9a3e77668a`

```dockerfile
```

-	Layers:
	-	`sha256:9f412a45176e3fe1ab3f8f36c151902556e9c91c43d32015b8e453ceb4f2072b`  
		Last Modified: Tue, 18 Nov 2025 05:09:45 GMT  
		Size: 3.6 MB (3575358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d47ad7342a0b76ced1fe2e5779fbfed36c343b6e87c8b2b260a0cc83d9f53ebd`  
		Last Modified: Tue, 18 Nov 2025 05:09:46 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:c5581a4d453de72755f23515c2070ae0f211f8375ea147fa941339c5f6978f7c
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
$ docker pull neurodebian@sha256:e762587ae4044d398a4950827433a33757d3e118c3df11cd0a90fb82ce53dc8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60182437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5925223478748274668b5ec192c8efdd7ff04cd7ce3a4a0ddce021a46f4fc50b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 05:26:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:26:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:26:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:26:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:26:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:63fb544511bd02db3b85f4aa7407dbf6c6f5cd7cb1c0c1e65d055477ac245bcf`  
		Last Modified: Tue, 18 Nov 2025 02:31:43 GMT  
		Size: 48.5 MB (48500427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868501aae139938a2df6b8c1e34a48b3f8aa21b1d0da7c2e70e050d39175ec5c`  
		Last Modified: Tue, 18 Nov 2025 05:27:00 GMT  
		Size: 11.6 MB (11588863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470d047aa02066b96ec1483e1ed7bea661ac4a8f05ad598c6bbc17eb277035bf`  
		Last Modified: Tue, 18 Nov 2025 05:26:59 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2bff1bd5008202d0cf3b78801f1d6cb6e71c6418c3d3b331e8581eef9cb7ff`  
		Last Modified: Tue, 18 Nov 2025 05:26:59 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64ceb5cc47fd60e60b7751683b3117dce7b49fc7ece1eb62194765e538bf40d`  
		Last Modified: Tue, 18 Nov 2025 05:26:59 GMT  
		Size: 89.8 KB (89827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78caf42b1e460472b71623a4528efb1808b4001eba2e6860bcc6c8d3c75c41d9`  
		Last Modified: Tue, 18 Nov 2025 05:26:59 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c78fc698df0d640da2e09714972bdcca64fcf270b12f2f7ec4455c1f7b03f978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e9aa74511cab257d2f5476a4dd6e98674487cd3c2671fb021dab55e03e1157`

```dockerfile
```

-	Layers:
	-	`sha256:dedd26f7e64d36e3a4121a0b02d24e8e73025be59f89a540652e8c44b4239f9e`  
		Last Modified: Tue, 18 Nov 2025 08:09:02 GMT  
		Size: 3.6 MB (3577431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4951412701f1be19c6efd634bd5d4c33331017fbfea4356190ede4f13343a4f5`  
		Last Modified: Tue, 18 Nov 2025 08:09:03 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9c548a571e85b70b292b96813cd00941bf3e96b959057db5b2572c2dfee4aeca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59940885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5c33d75154b40af5a4e2ed79dfdfd6a916e3cda19c539fe5f34c6f4cf23f76`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:57:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:57:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:57:14 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:57:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:57:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2b90f6fb16dc868101354a233036d6d70e13cd3477e4df5ab59f2ccc8607c1d4`  
		Last Modified: Tue, 18 Nov 2025 01:13:53 GMT  
		Size: 48.6 MB (48591389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1473a9ef112b3354ecb8ad37437881c07c1330a179af790e6197afe69d118085`  
		Last Modified: Tue, 18 Nov 2025 03:57:32 GMT  
		Size: 11.3 MB (11255640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee7b3173ae7900350aa0c13fb1183ca91219d5891202b3cff35eeaf1c80b7d5`  
		Last Modified: Tue, 18 Nov 2025 03:57:31 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9797247299d9f83b806b73618e195baa0f95d2ddc9b81bb9c6cb69852d70360a`  
		Last Modified: Tue, 18 Nov 2025 03:57:31 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305d3575bebd85f0bb2b4936522cbfe2058213f281cf396211a6dcaba921569a`  
		Last Modified: Tue, 18 Nov 2025 03:57:31 GMT  
		Size: 90.5 KB (90533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07a8228ced17f46f7ea430082bebae91f27757072506586bc99ec87f75f6d0a`  
		Last Modified: Tue, 18 Nov 2025 03:57:31 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ef97f524e0b4f5a6f8fbe1cf7cc8862b248979d93944230a0e6ef10ce6a2bc5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a332782142e357fb40eae518f5fc9a7ccd220d630e0da1481cedc4f1684377e`

```dockerfile
```

-	Layers:
	-	`sha256:6cd1b21fff2d2212e067d9150271763da862a313f3c4b2fcb4e5fa0c42f1f4ca`  
		Last Modified: Tue, 18 Nov 2025 05:09:49 GMT  
		Size: 3.6 MB (3578307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581ffbae3cc89923c70c60e4c5b10f6337934afca176aedaec8dbb8f3f4fc942`  
		Last Modified: Tue, 18 Nov 2025 05:09:50 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:2355b2b15ca42c2281d7dbc7f25dba05c3f444218ac341d44b0cc3b91e6c4f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61661269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8e397017c23070f405400256017fd62c2efb1acaaf65aa58abd92fbccc4b86`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:05:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:05:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:05:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:05:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:05:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b1df74e42eaae76d71bf2c2aa402328d711dcdb63b4080ae4e7050388c00bad0`  
		Last Modified: Tue, 18 Nov 2025 01:12:57 GMT  
		Size: 49.8 MB (49833161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320747deac046e78cc6cd5bf1f43512ceac0dcd4bc46633b37bac1da49cc2347`  
		Last Modified: Tue, 18 Nov 2025 03:05:50 GMT  
		Size: 11.7 MB (11734574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb1dc298560a964b377102c4017b5c4f003eac17020d279bbc350786f83b343`  
		Last Modified: Tue, 18 Nov 2025 03:05:49 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cacfbd2b30909444f5547038302340f534c5a64f670a16b357f7b9bfbf040c`  
		Last Modified: Tue, 18 Nov 2025 03:05:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc92a3f91e7b2a6ae7fe7bfc48ae16482ba42011cd41e8ef88915792904294f`  
		Last Modified: Tue, 18 Nov 2025 03:05:49 GMT  
		Size: 90.2 KB (90212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63c4ce8d0e216b5aab98536e70d2080de788be29e1760ab60b24b41b43d0a18`  
		Last Modified: Tue, 18 Nov 2025 03:05:49 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:31bf8c50269d41bc97ac9cd64fd1c8d86ec815b301ed715139861791cd73eb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2729a5a69bdcfbb87abddc99d2d863357ac7cbe6d4132f113c0dc4325fc8557`

```dockerfile
```

-	Layers:
	-	`sha256:2aa0e8b7828a6c1deff36c806b411f7001a9cd34e0af414a449a1094d7119b5c`  
		Last Modified: Tue, 18 Nov 2025 05:09:53 GMT  
		Size: 3.6 MB (3575394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecb4ecd39798b3b865e36c5ec98d70a94d6385b022ee279c0de675396f9f5a84`  
		Last Modified: Tue, 18 Nov 2025 05:09:54 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:4a17725e892257ad4267fc45a29f31e2c2893d7b34fc4da4feada937b7169692
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
$ docker pull neurodebian@sha256:52b23456ab2f9d29fd759ecaf2e5a2541030add2851a9b053a51c2d867599c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7d7b6f18d2ebf89a1081e0b667b4c8a57cd1c4916e28e5a24d831549248bdc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:22:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:23:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027086a669e3187a5bf55f93556ceea5dd486b73a28bc08d86aeb65a70793707`  
		Last Modified: Tue, 18 Nov 2025 05:23:16 GMT  
		Size: 11.1 MB (11105091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d191edd77c0ae59bd17b0f6640a0bf2d8749774ef5877ce401308fc7547fed3`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18651e8f324fcd83223a52a2730112eef035e1ceb11219aa7de401d66434f20c`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977616fa4c9e859613cd50ad00c392b3a050ff5e4a7cef8078fad26854d79113`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 101.4 KB (101405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f3d82782aafc3fabcb0f4cd571387f5f0469eef5209184cb44f4f03e814e201a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f061182ed89de96f15a42206b239284ea10a77684e0117e45c8c83a75cee0bd5`

```dockerfile
```

-	Layers:
	-	`sha256:72e2841e7d8a353d852c2136dfde3cbb9389c533a5e49bdf8cd92300794ceed3`  
		Last Modified: Tue, 18 Nov 2025 08:08:23 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db020feaeee2fafa232e497baf959f91c0631ea5ef2f7c8f5db85e3332bac212`  
		Last Modified: Tue, 18 Nov 2025 08:08:24 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7a0e1a673379a86a94d3c2e3bdb42728b33fc4c251ff6891b1acd4a0ee392337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91a451e442d2e4459f8608f6798004fbcdecc5b1e051cc8175efd38e757b228`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:49:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:49:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:49:35 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:49:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722ffbbe605a785238ffca2eb8744eca1f0f76e1718902782cfa899d81515702`  
		Last Modified: Tue, 18 Nov 2025 03:49:53 GMT  
		Size: 11.1 MB (11106099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fb98ab4c345ad520c24eb6e96667d26e24c539579fc55b995d86777c6bb33e`  
		Last Modified: Tue, 18 Nov 2025 03:49:52 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea69364ab834cf76a2f1ed7a4892a53173db03de6c6957be53af710be6d154e`  
		Last Modified: Tue, 18 Nov 2025 03:49:52 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc8a13c0c8e09eea2ec7010f3f7c34d2f741e4026897300d421405d259332f9`  
		Last Modified: Tue, 18 Nov 2025 03:49:52 GMT  
		Size: 101.1 KB (101107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3130883b211251a00c8f3138872d2127f486ff9b84eb8de852200a2db4de557c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5b0b8e3b177bd5d484e96e7564af795d83a58c23b9e5d5059342292132fca4`

```dockerfile
```

-	Layers:
	-	`sha256:4dd6ac5ab9c023c50b5e8c1658a66a76ee36f0f03532fa710143b1b133af7592`  
		Last Modified: Tue, 18 Nov 2025 05:08:59 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ca9c35ba0c1fb4e0e1288a61902514b9b4d9045956de4d3b40fe5fa9dc8ad9`  
		Last Modified: Tue, 18 Nov 2025 05:09:00 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:5aa69718f1efaca3418c6d918472ccc3610a069dad9a5de8dec3ea485a595596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee264702ebd5954f33c687a868e40ef83a54e39bb0fa536e18202657530adc9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 02:59:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:59:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 02:59:02 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 02:59:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ff276d829f31f5253bbd1b7f53ddf75bfd6004f7fcc06ea8ad1b23a242b12d3b`  
		Last Modified: Tue, 18 Nov 2025 01:13:28 GMT  
		Size: 54.7 MB (54699599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad6c4930bd9f54fe6d2bb6d571f25016096ca17f5042810bd28ad8cd30e0587`  
		Last Modified: Tue, 18 Nov 2025 02:59:20 GMT  
		Size: 11.5 MB (11500406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e6ed60e67a01f2bd9eb7737b35f9071edcafffa6a7408cae777d51d9aa773d`  
		Last Modified: Tue, 18 Nov 2025 02:59:19 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba69b163bcb414900c226707b4e354f29cb924661cd161524e15552c784f5b6c`  
		Last Modified: Tue, 18 Nov 2025 02:59:19 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3ee899bbd601f3a72f64d5c1253c7739d0a559b58cd7d06c6c3fb6f3699916`  
		Last Modified: Tue, 18 Nov 2025 02:59:19 GMT  
		Size: 101.3 KB (101277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:31e9b963b769aa8402cb4f8e020e7d2d926e8589b11ccc0473e774492f589e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0865b8f651164a8cce85f937a8680f329663d66744888c46adf7d5ffa95c6c9`

```dockerfile
```

-	Layers:
	-	`sha256:ee00c44865291a391a9bcaf7b8de266296f6f9be6aa7c0b628ea626c63eaa1f3`  
		Last Modified: Tue, 18 Nov 2025 05:09:04 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:108db865401eccf5faad0834934c22e016bb182f2028e5f435587351e58dc2fa`  
		Last Modified: Tue, 18 Nov 2025 05:09:05 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:294271293f3a3b1b58ef6390a7af7967eac1f49364eb3be82ec4fce535c823e5
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
$ docker pull neurodebian@sha256:b5362f16c8bef59c161be65b8021f12f06d0bcf3ddb0a4b6a919891540bea705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507393086679db487cfe16d03c9f41a88eb355e0a27d1f0fa0b858110d6cd872`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:23:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:23:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:23:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:23:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:23:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556ae439bdcb8b47bec75f40f721c7ce74bc68d13285ae81e49f3d08edc3a67e`  
		Last Modified: Tue, 18 Nov 2025 05:23:40 GMT  
		Size: 11.1 MB (11105079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2112f97d5afa272740c88cdbbbac424ecf5d2fbdaa3203906800955ead6013e`  
		Last Modified: Tue, 18 Nov 2025 05:23:38 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742817595129cc418a0cc3abeae9c4c0acf9104674ef2cea757ced23c0a9c4a5`  
		Last Modified: Tue, 18 Nov 2025 05:23:38 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85410c47b996246a8855aadc2edaed772d3395afe5f1396e1843e715b6d238c`  
		Last Modified: Tue, 18 Nov 2025 05:23:38 GMT  
		Size: 101.4 KB (101378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3422aa1f4f380d754a9c44531abd048ad4dc1c3f3fd1f70900e176c8f9758a2`  
		Last Modified: Tue, 18 Nov 2025 05:23:38 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e6c7721c3a90d1bb3162f7255d43d777cc2cb06f9dd1c7a9a0b0a49f835678f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21ae0f35686fc72f57d385dd548eb3e7ff39a0d27c04cc1c81dc7e2ff2545f6`

```dockerfile
```

-	Layers:
	-	`sha256:3378751582ec403ee5b1043d29bb0868f75dbf736b7c2bc80ce43d58aea0893a`  
		Last Modified: Tue, 18 Nov 2025 08:08:29 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7bfaf79598970461a37decff4cf866e509c8fca018712f99e2c03f4443a6b8a`  
		Last Modified: Tue, 18 Nov 2025 08:08:30 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:43921c44590d322ea3a2200551d5e4cd52721ac1eab9a993940d6502a91cde14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f12c8a424ceaf8c8108c2caff5e386aaf192c375945faf61f353be561852656`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:50:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:50:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:50:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:50:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:50:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062c2b3ce83caad4b37ac1e7102fc1fccb79e2c6fa03b1c809c88fdf9800df8d`  
		Last Modified: Tue, 18 Nov 2025 03:50:50 GMT  
		Size: 11.1 MB (11106024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374c795581cfa6a07227e0c8adadafb18aad92ab4687691c420ef8bce3905149`  
		Last Modified: Tue, 18 Nov 2025 03:50:49 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac04a8b962c8a03ae75c44fe4910852f14b54684a668dc2c85c4af38d23ee22`  
		Last Modified: Tue, 18 Nov 2025 03:50:49 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc1e68c8213d3d297e1e6dae792d728019447243ab71ffcd7b55daaa8014d33`  
		Last Modified: Tue, 18 Nov 2025 03:50:49 GMT  
		Size: 101.1 KB (101113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55940f735946c2165111b6142e534996c25a04f9f49ad7c4f9258520c46db14`  
		Last Modified: Tue, 18 Nov 2025 03:50:49 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ec92181c786d637edc61066712b4fd1a4bfa44f14b829347814a0995f92a377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b320f6bbd5e202338100a948bd681dab926c6680c6668b9e9c8b356ca6b36a4c`

```dockerfile
```

-	Layers:
	-	`sha256:2329ddc9b423c293e808126b639e5506f6722f297c6660fe4fb982ae665fe2eb`  
		Last Modified: Tue, 18 Nov 2025 05:09:06 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53f59167813de90e0d35b3758f73c7d1cb28273148c1c33923373754be604b2e`  
		Last Modified: Tue, 18 Nov 2025 05:09:07 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:d006be0275eaeacc066e7c1abaa4162b0441e35d06c5379d4bfaba35d726f029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da139b3f0b4fdd084098e6b854d27ddf4938477b28b064d3976600ed6b02ee4f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 02:59:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:59:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 02:59:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 02:59:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:59:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ff276d829f31f5253bbd1b7f53ddf75bfd6004f7fcc06ea8ad1b23a242b12d3b`  
		Last Modified: Tue, 18 Nov 2025 01:13:28 GMT  
		Size: 54.7 MB (54699599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34469d4c6ca4dbf4ca7c8b004510f5a4d8e65a6c741c78d358e654c585925090`  
		Last Modified: Tue, 18 Nov 2025 02:59:33 GMT  
		Size: 11.5 MB (11500397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b78335af44e7378b37d0d3942b21f81ea7df0b78b02cd8976ac4b1e05ca9770`  
		Last Modified: Tue, 18 Nov 2025 02:59:33 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9cf98358c9e5929b880c3bde56350327837146f26e234f971a33cbce4b264b`  
		Last Modified: Tue, 18 Nov 2025 02:59:33 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55446bca2ac686c36703461bc98ec398278137e80fb2be821f9b461f530ba7`  
		Last Modified: Tue, 18 Nov 2025 02:59:33 GMT  
		Size: 101.3 KB (101295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fb474d5a9aa8943ecfe880e17031d1d3cf2994ef46944b562887b34a9688c7`  
		Last Modified: Tue, 18 Nov 2025 02:59:33 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0773445db0bee45b7afb385282eeb1ef903ba46b512d9dbe03af455d1086959a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751d385b351522bf7506ec4d98ee5deff26beedd0293f50f99efda08ef287fab`

```dockerfile
```

-	Layers:
	-	`sha256:42a7737f79e78022f2cc02f43fd5fe92aa0d20f085e4132c32862c94618bfb43`  
		Last Modified: Tue, 18 Nov 2025 05:09:12 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e6a8129866aeae07bc265478b80a0f570896460cc1696db254e67a6601b4238`  
		Last Modified: Tue, 18 Nov 2025 05:09:12 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:cec27486ade4093b3aa428c2aaaca469fd8beb4ba6fb8763fe5365b82f0f3751
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
$ docker pull neurodebian@sha256:b992a1aba72afdfc4db3866656606b54502e0e0ed75a01c44a8bbe682ee0121e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59845829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f563a4f42c84971da0b2c7135fe04512f7525eab72cd63caf558ce9ce90d0e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:23:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:24:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:24:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:24:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332597ec821475bbabd342c180adc5558f6faa9683bd335ec7649caf6790c4f5`  
		Last Modified: Tue, 18 Nov 2025 05:24:17 GMT  
		Size: 11.3 MB (11269512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26214aeb11956a0b8f9ea005f79999e0946adc1929d07a7bd8507c65c1c7bf74`  
		Last Modified: Tue, 18 Nov 2025 05:24:15 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1e22a67666689cbfddc15036ea3d22fe64804db66109123f07325860301219`  
		Last Modified: Tue, 18 Nov 2025 05:24:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b704bd7e985830a1a0d113313768d0a910e543b5a7ca60276d1b194e80685de7`  
		Last Modified: Tue, 18 Nov 2025 05:24:15 GMT  
		Size: 93.4 KB (93380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6e53aac955ba1df60f5ce578bc327d7639298e2ca456a89c9ccb40c76e050a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9f0aa6ae2a3b9f6bc99dc5c0feec8475f074f7fe4c0d766974d79d9f279671`

```dockerfile
```

-	Layers:
	-	`sha256:23f36d2082ffa9462fe810209c8a7fac4c00fd13172d0a39bf0be5427074414b`  
		Last Modified: Tue, 18 Nov 2025 08:08:12 GMT  
		Size: 4.1 MB (4075236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d153fae45e633f80f2eb958081dd125343cd7528215d10d908fcef89a0ea677`  
		Last Modified: Tue, 18 Nov 2025 08:08:13 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:50a5a625b28c32c49bccd1b8d57923ee03ea30f76a7ac8f3389642470916bba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ac2181dd0537950d96d6b71f88ff00dd793b6457e2a1bc5e0d058cbb43684a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:51:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:51:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:51:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:51:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62390544d51e9e4e416e49b6d9beb1a6cc3c83979b1221df2a79f2ff23ea921f`  
		Last Modified: Tue, 18 Nov 2025 03:51:39 GMT  
		Size: 11.3 MB (11253505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bd7b45b845c00ce3b9f9b8550fd08ded78e3770e7b6b8c6594f1360627b697`  
		Last Modified: Tue, 18 Nov 2025 03:51:38 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1521afcc0a45d7d89d38fe3092052dab1c78fee7db3ab723626e2c7b2f37c3b`  
		Last Modified: Tue, 18 Nov 2025 03:51:38 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109959872cbd45e0cb947130faa31d3da05f5978e79bda669d4be8d31ae5d9cb`  
		Last Modified: Tue, 18 Nov 2025 03:51:38 GMT  
		Size: 93.5 KB (93539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f756360076a198bf499569584dd893dc71581cd8142f514a7fcae2b7f797f972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7320ee090c63c4ddbef1519e14e84705f7ca28c41758f1ebadd780630514b6`

```dockerfile
```

-	Layers:
	-	`sha256:7e1c5cdbbbea15f5fa8f04f34f1eafe471962d5b9f7d16a8a0240dd5c158c78f`  
		Last Modified: Tue, 18 Nov 2025 05:08:37 GMT  
		Size: 4.1 MB (4075478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f04f4ad24905c1c37df3cd350cc8d3cb49a3f52670111846504f97240995eb`  
		Last Modified: Tue, 18 Nov 2025 05:08:38 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:b6f14671d17cd5a54c06ebd8f12c443709475eb0e62f46cee85102c8ef88151a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5d236fa58b4bd4fb3ff0348bb61f1a831a62de744715a38961d7cb07394c8f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:59:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:59:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 02:59:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:00:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8975fd88545a557d6130aaf0939ec9d94115f11b7beac2c3cfbb4c4f95f493bd`  
		Last Modified: Tue, 18 Nov 2025 03:00:43 GMT  
		Size: 11.7 MB (11690134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc851a44c9f3c9f983ce75368901731b6ec4407c164ee071d7d980f036b22f0f`  
		Last Modified: Tue, 18 Nov 2025 03:00:43 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe683a35f9a9a79e411adfa0e8758b3ab5a011e16cd010feddf70124539be2da`  
		Last Modified: Tue, 18 Nov 2025 03:00:41 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecad0060cfe14dce44d058568b622d3bc352786338181af4107306f90ce9cb3`  
		Last Modified: Tue, 18 Nov 2025 03:00:41 GMT  
		Size: 93.4 KB (93410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0024515340fc9614a49927171b075de2297c3be5d3e668b6661e791e665f14f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da43d3bd5dacb12ef9c1b8aa391f77db5288843666a12bc67d8ec4e5ece03cda`

```dockerfile
```

-	Layers:
	-	`sha256:b1660ba43570c243d0bf22b1f3a4a49672b9d495e11d58e918bfabfe422fbd40`  
		Last Modified: Tue, 18 Nov 2025 05:08:42 GMT  
		Size: 4.1 MB (4073204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b36d81ea50f285f482a84cc2899f2d25fbdffa2b443e57944bd263e6886e283a`  
		Last Modified: Tue, 18 Nov 2025 05:08:43 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:d346efc1653ce69298b0583c215759f69e4c520b1687b306ae31ee696ee1ca62
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
$ docker pull neurodebian@sha256:c8ead1f42c634e681b9cdac2bf63ba48bc04ef8800d888bbab9ac6bc443233b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9ceed3d827ee121c147b39aee58e02ca8f8f14e9be70c9899aa69c0e4db108`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:24:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:24:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:24:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:24:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:24:20 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52f85a9e90a8b30122ba1fd3c2518caa5dfa52bad3467bf81a8895b3ef33d4a`  
		Last Modified: Tue, 18 Nov 2025 05:24:35 GMT  
		Size: 11.3 MB (11269784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c5250e45b37b7a4ff8c28cceb975c813e947b0cecc421a569c75cf55bb3c60`  
		Last Modified: Tue, 18 Nov 2025 05:24:34 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193261405425b3c59f2c41fb87d2b4d31680bf8592a977be1caf0a5113b36ae1`  
		Last Modified: Tue, 18 Nov 2025 05:24:34 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13be725ce53a3aa8771c7b171f351ebd4ed147048d82dc5056b9c1f81e85ac4`  
		Last Modified: Tue, 18 Nov 2025 05:24:35 GMT  
		Size: 93.4 KB (93374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee0f9162a0042d874a36b09ff302bd44f0f89155feccf6d3f925f58ec54e728`  
		Last Modified: Tue, 18 Nov 2025 05:24:35 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed9d4c3f6b45fcc01320121fddd661becdf4e23be51c8630c3bccdcb27c45d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ada510161ccd0cbdb6e2b1d71f378cbfe93e95b0896c977ac560e969d2f1c0`

```dockerfile
```

-	Layers:
	-	`sha256:abdc6af02c68406dc3e31ead91fc836045df6d11811540bdc969c352335f9a0c`  
		Last Modified: Tue, 18 Nov 2025 08:08:17 GMT  
		Size: 4.1 MB (4075272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a9eb26d88e694e6a18b0aa1414822b139d8020bb0108bdeb82201e5a65f8b6`  
		Last Modified: Tue, 18 Nov 2025 08:08:18 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:799a9fdaeac12508072ad286af1e4e7af48fdb6b90fa105569d75c585522decb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9196b72b4cef17624139168cb8a29ac1a83af665a592f750bb3c2721486de148`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:52:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:52:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:52:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:52:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:52:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8807214d6bb58ce93643f23da0d4f513c5ad5c1d7afbca79b7efed5365942ca8`  
		Last Modified: Tue, 18 Nov 2025 03:52:35 GMT  
		Size: 11.3 MB (11253434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6c6e4641d306f35a7865dc55f0617616dc6b1fdffcb7dc3efedf0737835a76`  
		Last Modified: Tue, 18 Nov 2025 03:52:34 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba37d77eb8f27c5b50207c5ded85c692607c6c8731c3646f7aa887fb707d9b4`  
		Last Modified: Tue, 18 Nov 2025 03:52:34 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f35d356531128f85210ebbce70caffc3b026330c2f6cf599438d5cc6fd6ca6`  
		Last Modified: Tue, 18 Nov 2025 03:52:34 GMT  
		Size: 93.5 KB (93515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a21ba5c85c56614c9af83a1aedff34ebaa1eb2f907abf5f9e128f2413b19b7`  
		Last Modified: Tue, 18 Nov 2025 03:52:34 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed1488b88f01f98361118e77ce3f25f9d4948315e0be7528e934b3f88bfb8bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4703273c9e0ef5f78614bb8691d50f70c13a6b84a97abe62174461caddfb7da`

```dockerfile
```

-	Layers:
	-	`sha256:ff89c214db7039e198f750d1504e92a410cfd11dc52faaab1c904d28bfb17e10`  
		Last Modified: Tue, 18 Nov 2025 05:08:52 GMT  
		Size: 4.1 MB (4075514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cb4ebb333c44656c1f30b692d638ce65ab8a9add9573811002d77ae7ef10360`  
		Last Modified: Tue, 18 Nov 2025 05:08:53 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:2b8d3d240bdf2e13a28c55a3342b49ba13fc0ceb8366f34fa9cc11f991fb02a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61253059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f231018d42fd321a780aaa8de73caa2d59d077695636f36a0cee80ee8f81bd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:01:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:01:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:01:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:01:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:01:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a93d0237e128ad08fcddfd034244077cd71dc323e8c25586ee8ee24728ec4d6`  
		Last Modified: Tue, 18 Nov 2025 03:01:29 GMT  
		Size: 11.7 MB (11690161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff35b78322711c76b309f998cde01420d157ca97747d0dca1c2f1303f2e4c85b`  
		Last Modified: Tue, 18 Nov 2025 03:01:27 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fce1d0ab5d7eed1f6fb618d4f905b41413bb9793db1989d6d8a7329d274744`  
		Last Modified: Tue, 18 Nov 2025 03:01:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbe045baa9269b254e517da9ffee8d4ba6c88e789fb777f5c77bc4120b4f6a1`  
		Last Modified: Tue, 18 Nov 2025 03:01:26 GMT  
		Size: 93.4 KB (93412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd1f28a6350b9b83efd2d573a2963eda9ec1c308dba86dd4c23ade9b1ee1518`  
		Last Modified: Tue, 18 Nov 2025 03:01:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:52ca226625f2cc7d0ec9f3f7a67f8c1a133b4d6d44935fa551176ef9f7c9e27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d398885232ce92f7fdad4175c8954f4a3fafcbfb91f3380e2bcc238b0788425d`

```dockerfile
```

-	Layers:
	-	`sha256:9eae406c595dd9fb241902d88fff47118b84928d56f49314f5e086ef1b4626a5`  
		Last Modified: Tue, 18 Nov 2025 05:08:57 GMT  
		Size: 4.1 MB (4073240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abb0e974253a831d2dc5b7732b8c9a0ea76c6d4ce502ff780e687782910c8a5b`  
		Last Modified: Tue, 18 Nov 2025 05:08:58 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:018039aa28469cb574577be011ffba1b39df9ca46864a220f31a05a376249830
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
$ docker pull neurodebian@sha256:a6b82875250b39bce69a473895862362fc6c0fc619b8aa62cecbc36ddafea16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59672386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44fc91da823f52c537b6e13a4c462a693e58d4a8ea793dd62e90e451905af64`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:24:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:24:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:24:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:24:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbc7b1c2d62df985e7aff96ee3ece36abe8cf517d7f993fe66c2a5d85e28a00`  
		Last Modified: Tue, 18 Nov 2025 05:25:09 GMT  
		Size: 10.3 MB (10289731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5364e6fa5c4502194ff9ec23ca3d5e09b80eeccc4f4f58584beafec862b4f8b`  
		Last Modified: Tue, 18 Nov 2025 05:25:06 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e3e7f0c19fc5bfe238e52366df56925c734e376f238cc681974db438f32253`  
		Last Modified: Tue, 18 Nov 2025 05:25:06 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1ca7993e2d88612125c1707875d1da317111bb55e9cd88b5bbe786067453a7`  
		Last Modified: Tue, 18 Nov 2025 05:25:06 GMT  
		Size: 90.2 KB (90204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:df927e54faea7df4d76f3a405b8d22dfe4a687c81abd444f5389a9d65bb4aeb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2d4278a656ee84173516bbd88d5c411730eaca56631895ecae5b804adaa9a`

```dockerfile
```

-	Layers:
	-	`sha256:3c0e4dc230c96b33215e0db6946acca5920ddc0b14b5270e6497a701a792a37b`  
		Last Modified: Tue, 18 Nov 2025 08:08:51 GMT  
		Size: 3.6 MB (3613029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c182edb049488b2af0cf55dff839e72d56dbd8f86a9812723dc44ca3903f66`  
		Last Modified: Tue, 18 Nov 2025 08:08:52 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:03f45755a0cbd0fa591dc83b3f174f408ec09689438dd1f600685d2cde3859bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec1e38ad20d40f39f7b16d2bbf5d3dcaddb31d59c129758a0bf91ac4a087408`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:53:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:53:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:53:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:53:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39eff5378ff39f272aafcd4e6eb21f0002984d7ba123df62005a1c72b904f39f`  
		Last Modified: Tue, 18 Nov 2025 03:53:24 GMT  
		Size: 10.1 MB (10073386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7768b0faa974ae0a24a5fc2d6d8ab83d8bfbaac5c1c6b88142e79c4e9331d292`  
		Last Modified: Tue, 18 Nov 2025 03:53:23 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4803b1be5a4e9ea2b53fa1893acd4bfcfcc977b674beb4d6c9df3d231a97eb4e`  
		Last Modified: Tue, 18 Nov 2025 03:53:23 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239af7ab87748df14555e1392f8dbd23b17160c367fd5fab152ab0d11134d812`  
		Last Modified: Tue, 18 Nov 2025 03:53:23 GMT  
		Size: 90.9 KB (90895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4233619c2439c669dcbd798b18d3779f25a61d90424651cd1a47825c92259fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c67bfaa7bdaea4ffbeca1e70fcfdbd3beb9885e4ede0de846eb219c971de3e`

```dockerfile
```

-	Layers:
	-	`sha256:105073c6ec3e7f5c078d5e10ecdbbf90eaf703f3743f3044afb9c8e051305965`  
		Last Modified: Tue, 18 Nov 2025 05:09:31 GMT  
		Size: 3.6 MB (3614556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfef6ecb903761ecd001f5326ba3ebf4549b1e7fd94a1e645e8f1707779545e4`  
		Last Modified: Tue, 18 Nov 2025 05:09:32 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:17dfc4286fd752b3d3d0bf9fb20d8810070cd8191073f82eaa5374a0e65cbccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4b5d6645061105ccbb028eb3fefe29edfa9a55b0172aa02ee45104cffd1993`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:01:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:01:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:01:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:01:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bf2a49c122745d1757b9ecb1c9b1d8252491e66b62d1c279080155aaa530a615`  
		Last Modified: Tue, 18 Nov 2025 01:13:10 GMT  
		Size: 50.8 MB (50801744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e17a20228b22b602cbbfa5680fffb9f4f423b2b773d66726620a3e615f494c`  
		Last Modified: Tue, 18 Nov 2025 03:02:14 GMT  
		Size: 10.5 MB (10462815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d43cb3b26404265a2415ae726de37e382f8bca2b3573d437ed0af59780d869`  
		Last Modified: Tue, 18 Nov 2025 03:02:13 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a98988b1a0d709c24b8a75b233813c646170d9954599a23bc28f542a481ccce`  
		Last Modified: Tue, 18 Nov 2025 03:02:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7df26ae6119f7ad73c3e54631b21eeca4094687be7a3ef5df86c7c0077dac9`  
		Last Modified: Tue, 18 Nov 2025 03:02:13 GMT  
		Size: 90.6 KB (90602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5cb23b9eed1f0fee69d391b347817aacd1bb16034b6dc063849bb4362d18bec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a0c9860b662de961e7066a34a6cf69a21b4362ea5bc02fe635ad924a557071`

```dockerfile
```

-	Layers:
	-	`sha256:4d4d4e2a77ef0acaa1a67ff1b69ebcc224babe7fb3cdc53b737a11cb53e2332e`  
		Last Modified: Tue, 18 Nov 2025 05:09:36 GMT  
		Size: 3.6 MB (3610978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0491f3d73f6c0769dcbd447cf474664a488215c438ced43977ad268347ba666d`  
		Last Modified: Tue, 18 Nov 2025 05:09:36 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:99e725ba2098d9f5e4ac5df767e2791f2262c541d9d3ce6882a7df90623ca8f4
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
$ docker pull neurodebian@sha256:e3189cb38355d9a10e6ee69e26edb6de39b465cd8205913d981661a29d17dc79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59673174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa59c2c3a955fb01be15b8113061546e9756a4d36c3c7470857ae9c252cc428e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:25:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:25:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:25:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:25:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:25:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16dc4dbae62748d5ea26ad4fa94cc1e428529554cea8d528dae4b9e632092a3`  
		Last Modified: Tue, 18 Nov 2025 05:25:28 GMT  
		Size: 10.3 MB (10290035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f327eeba29be5557be80af3b3e54fb4b66e7f3114688f91d0d1a86e4c984e22`  
		Last Modified: Tue, 18 Nov 2025 05:25:27 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41eef2006d4e3c6079b7b7337b729efde57322b6d767c4c14d885db8d04b5b`  
		Last Modified: Tue, 18 Nov 2025 05:25:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d9879da8be8e094ac028797b0fae41f652046596a4c4ee377662c727affdcd`  
		Last Modified: Tue, 18 Nov 2025 05:25:28 GMT  
		Size: 90.2 KB (90243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266c69e3259acfd42f890841b091de6cfd0c84ac1ae6a4b555eecaf76fd850e9`  
		Last Modified: Tue, 18 Nov 2025 05:25:28 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0ddfdbc93c093ddbc557c782dec3add89cf90224b2a180e7e5a71db3a4f8882d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0e797be24246896583645947ee35f3f7738ecb63481336f5cb31d86c2f4ce8`

```dockerfile
```

-	Layers:
	-	`sha256:6108611c93b32a422b3f74aab105a2735fdd09db8ae15bbd2c08ae8a70670e13`  
		Last Modified: Tue, 18 Nov 2025 08:09:20 GMT  
		Size: 3.6 MB (3613069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36168299857e7e157d6e02f98dd16e7bb6377db14cc095d6a0b8df02014250c2`  
		Last Modified: Tue, 18 Nov 2025 08:09:21 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:cbe051ff9e65e938ef970ed213bed1845e12d099468e69ee359adf3f29216d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d723f4d19be58aaf30cbc45c642741452d891db5e4ce1244af5c7ab9483bd6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:53:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:53:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:53:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:54:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:54:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a505c9bb250d77e4640e96c444c4fac586fc1433c373bbef83a7256e04d6ade`  
		Last Modified: Tue, 18 Nov 2025 03:54:19 GMT  
		Size: 10.1 MB (10073459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904db87cf72b19c511cfe31ac93b95a3ed1ba1f7c9bb7582ee6eb938d2e164d4`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842dfa2696e5c96bc037b37dd0932b97434244d91043450150d9e96bdd37472b`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaca400b700bdb23c02eff76b5d0d5caf6a698ebaf8497f19a82b8f417b1b01e`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 90.9 KB (90944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d36449c0d721c1d3cd641f286b2d678c32dcaa57534317626ed05a07c2d19fe`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6e09f67ac5afd71c56c4130e2c079060e9181289a300b5159f7fdcc66744b050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72700cb5e900ded97e722e6c8b510c0b93dc64d74713213f9746adc344fea7d`

```dockerfile
```

-	Layers:
	-	`sha256:9c9cb02fac134943ac6de2142d5414212aaa7d7329798636b6a8f64c46838920`  
		Last Modified: Tue, 18 Nov 2025 05:10:07 GMT  
		Size: 3.6 MB (3614596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52009749de1793d97606f0008b38292d4695967e6cac6f459d6a77f967bde8c8`  
		Last Modified: Tue, 18 Nov 2025 05:10:08 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:df5a33264cb70ceafdfdded5c3985656daf4489cbef1599dc6d616fb55d10d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91d5238a64d084798a94a0f5bbcbab41284c53a2939727b9ef7d026393e446b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:02:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:02:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:02:35 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:02:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:02:39 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:bf2a49c122745d1757b9ecb1c9b1d8252491e66b62d1c279080155aaa530a615`  
		Last Modified: Tue, 18 Nov 2025 01:13:10 GMT  
		Size: 50.8 MB (50801744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5c0824538c3115239695f48f023fa765aa984377851b00dc5bda2cfb78f0f4`  
		Last Modified: Tue, 18 Nov 2025 03:02:54 GMT  
		Size: 10.5 MB (10462815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efd84fd0f053203220666c2fc0ad3385d5508791dc63fa0de95dda5f7b47034`  
		Last Modified: Tue, 18 Nov 2025 03:02:53 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43491474c911114c1ea18ff4901547554394f1757ff2be3facef60a2af71163`  
		Last Modified: Tue, 18 Nov 2025 03:02:53 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5294129b5628e65891a7dd0fe5bd29ff3190e979eb91d98d77278a9614c0085`  
		Last Modified: Tue, 18 Nov 2025 03:02:53 GMT  
		Size: 90.6 KB (90617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f592a181d12cc8795e06ae7cd55f2152c4e55653b5a2f8e1d71a65305a29d9`  
		Last Modified: Tue, 18 Nov 2025 03:02:53 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:488f520ba92c5294e525ab10cdb9145c7b5c9dff6eedbad68ac5de96b13dbf35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b13ba51f807628099a34bcb151c6aa443a39e3bccfb5506b3456315ba489fb8`

```dockerfile
```

-	Layers:
	-	`sha256:a0f61787fb9b6f94344751cfb224a1243f2bf661be7453be08765c8f77bdc249`  
		Last Modified: Tue, 18 Nov 2025 05:10:11 GMT  
		Size: 3.6 MB (3611018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07484fba44c1bfedea9943a0c3add1849143bf110d7703773edeec6a8ba5769c`  
		Last Modified: Tue, 18 Nov 2025 05:10:12 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140`

```console
$ docker pull neurodebian@sha256:edb0c941528b9c8bfbb6a1fa482f0f5f1ae301e2572f450c19f373cbe5ca834f
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
$ docker pull neurodebian@sha256:366043713c7e6c0f03a9162bdb0a9e212e53a24123d07737478413ab4748d081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60181684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92dd0de9504e0bbe4409feadaddfb844ce08396abb0240bbc740a26215a3273b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 05:25:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:25:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:25:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:25:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76694dc296168bbffa890c84fb372e9c250bf33e0ad63a6146b169a57d983e2f`  
		Last Modified: Tue, 18 Nov 2025 02:29:31 GMT  
		Size: 48.5 MB (48500434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a49a253a05dd471c0e155f0f4f91ccc25fc59aa6c7bd527b323117b5250122`  
		Last Modified: Tue, 18 Nov 2025 05:25:52 GMT  
		Size: 11.6 MB (11588572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f16a4357781996ad9405179bea144b87856496993b9d2465452eedb14b76c8d`  
		Last Modified: Tue, 18 Nov 2025 05:25:53 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fe7c5d321e038a5990a22a2794a9547dec8a5799070ae3bede181248aee6b3`  
		Last Modified: Tue, 18 Nov 2025 05:25:52 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd9cd7a5c6fc267eff9196ac84bf0b83ad2ae80012b3d0bed5097cd7ce35a60`  
		Last Modified: Tue, 18 Nov 2025 05:25:52 GMT  
		Size: 89.8 KB (89776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f6ab5e45c7d79f972e35364b00e1e85380de600340204f791446433806794927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63c79d811b1da0bdc1d1993a6713d5f35d3b1fe5ddb60cd02a9272b93c89567`

```dockerfile
```

-	Layers:
	-	`sha256:d4326f39e0f4993ebbeb784b9a60db70483b40b2a3fe5331c79ad0b853782ac9`  
		Last Modified: Tue, 18 Nov 2025 08:08:33 GMT  
		Size: 3.6 MB (3577401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:727dabe4e2300565ad3af0d1d71e64f1dc685726f00be034d66a37cccd3bf876`  
		Last Modified: Tue, 18 Nov 2025 08:08:34 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0240320d50e0a735877ce9c1b680fc83383e5270c5252f3c5a6bf75773613d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59939892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f450dccc1910f9ea53442d037d9c07d6ea9730ad8afe22c7e145b5abbaedbbae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:54:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:54:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:54:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:54:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:25dea15c4ffeb70e1112f1ee06dd948a8ab9dfc3b79ef239cb96080cc27ff1be`  
		Last Modified: Tue, 18 Nov 2025 01:13:47 GMT  
		Size: 48.6 MB (48591184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e8cb6f2050f012301a38350d5b24e1d46c45d720d48514c166af2fa18ea87b`  
		Last Modified: Tue, 18 Nov 2025 03:55:06 GMT  
		Size: 11.3 MB (11255308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12dbc4a5a7d2672202d31ee9d7b29cb5d29a06f08566f247a363e2a63cb672a`  
		Last Modified: Tue, 18 Nov 2025 03:55:05 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccded1fb17ef0c142f8ae7bf64a99b345608c6adb5b81d14998da21c5d8e1a35`  
		Last Modified: Tue, 18 Nov 2025 03:55:05 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b042a4e6d45996fb48df60228a59d091830538e87ac00c0c3658e24d51ff587`  
		Last Modified: Tue, 18 Nov 2025 03:55:05 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d3b1559336fbc2de9e0c6065656e01b75ce0df387ba7457fca8fe58753121d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8978b1b94f45f5e132e11ff42fb8cdcf5277ac0ced6a06a87f419ef33bf4098`

```dockerfile
```

-	Layers:
	-	`sha256:b86a5b4eac17beb5568c3a961e76e6ffd482a8fc5ec835e684237bf06a5cb8c3`  
		Last Modified: Tue, 18 Nov 2025 05:09:15 GMT  
		Size: 3.6 MB (3578277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe1379a897c2fa408e0db91fe9afff334ac85006ef732f63644534ff4740f523`  
		Last Modified: Tue, 18 Nov 2025 05:09:15 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; 386

```console
$ docker pull neurodebian@sha256:9366598d8a26fb7d7dd14cd014de708e079a3f843b4c78957d0e2679eae472a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61659763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db37c76901f7f42765728dbcbe87d2e8d8ca7d08fa2840b5a41eed82241f696`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:03:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:03:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:03:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:03:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:898cf630ac245ec9ad865c96204520b86bb7b8760d5bd2f14bd02745e43d82f4`  
		Last Modified: Tue, 18 Nov 2025 01:13:40 GMT  
		Size: 49.8 MB (49832238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c99ed386714c4bb450506732ee810d85aab0f3dda4715c62ff3e15a4836519`  
		Last Modified: Tue, 18 Nov 2025 03:03:26 GMT  
		Size: 11.7 MB (11734481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fa4cd2f7a74e88e9df00cae2773c07d4f1b3ca5896efea246d4fc9c3d3b3fe`  
		Last Modified: Tue, 18 Nov 2025 03:03:25 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5326d561abb9377288ec05ed7812d09e6ad68ee1ffc3de192c6f36932e161aec`  
		Last Modified: Tue, 18 Nov 2025 03:03:25 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d381cf813812673b11780614a577a1610403eacd68b7a3a520cf58035f4591`  
		Last Modified: Tue, 18 Nov 2025 03:03:25 GMT  
		Size: 90.1 KB (90139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2496c2ba33112048fbc1b81a7e227709bb6d6dfebe4a95a1255c75d60b255087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0158a608fc9a1d83a4d807ed24061af7eae148722c2b6ee838a398f41eebdc4a`

```dockerfile
```

-	Layers:
	-	`sha256:509c1cfcd262c48dcd9ba2791f9f220ab486ca9b0d97c7c174a9264ae3597447`  
		Last Modified: Tue, 18 Nov 2025 05:09:20 GMT  
		Size: 3.6 MB (3575364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaf47288a7336f776c2fd7ef0a4483fd2b5da91c83ceb5d5ae52968a4d81d32e`  
		Last Modified: Tue, 18 Nov 2025 05:09:20 GMT  
		Size: 13.9 KB (13903 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:99748e3801a87ca4754f030cbe146f3d2d61e73399fe09d89e6d2fb75c3ff494
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
$ docker pull neurodebian@sha256:feaed26b03c949d0932e37e6e74f547fa6f99ad36f56d1aaf9574b4303d94193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60182204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567098fb1b1386891c3045fa629bf7193516c5be3c1e7ea4583b46e9f125f01e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 05:25:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:25:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:25:38 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:25:41 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:25:41 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:76694dc296168bbffa890c84fb372e9c250bf33e0ad63a6146b169a57d983e2f`  
		Last Modified: Tue, 18 Nov 2025 02:29:31 GMT  
		Size: 48.5 MB (48500434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6f932371b762d4ebd76295ed523041ce96b651c8d6f99058e56fde0193577c`  
		Last Modified: Tue, 18 Nov 2025 05:26:05 GMT  
		Size: 11.6 MB (11588603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb95424eca70e0b48eb1362dc9faf54d6cf60c34acb74bebc377ccd001eb0a5b`  
		Last Modified: Tue, 18 Nov 2025 05:25:55 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751758c3326f3120503e1065f2ee9d96dab1645821c5d9040b49ea54b7e4b182`  
		Last Modified: Tue, 18 Nov 2025 05:25:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e407f8ac8dd6b87d5030356d06d625859834a1b2fadc44b8b309603476fa0b3a`  
		Last Modified: Tue, 18 Nov 2025 05:25:55 GMT  
		Size: 89.8 KB (89813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bf0c4c970ca715981804e3d2797bc8cc57df79fc87b3e0d8f079f416f688ad`  
		Last Modified: Tue, 18 Nov 2025 05:25:55 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dd9844cc45fbe3e9de05e6c77c740d47a5f577608e3b189b07fb86b1cb4ee288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85735ebb9f37ee391cb4778514b2f1e223e828f04d47c74fdf38f6a08dde99c8`

```dockerfile
```

-	Layers:
	-	`sha256:938f600c2b882bab1eac886bc2abee6d9baca24359cb1c9bc53463214580ac7d`  
		Last Modified: Tue, 18 Nov 2025 08:08:40 GMT  
		Size: 3.6 MB (3577437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0cccbb40e13d48227175631b605120ebd5591330729672805e5b424dfb34585`  
		Last Modified: Tue, 18 Nov 2025 08:08:41 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:64186adde6428fae5c84a5002a30127063d0e3db638a8e2a0ecf21ba6744d014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59940274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2540b57cd8e8582e9238a43716c2655c40d1d64033d51b15977395dfd3a37fe5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:55:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:55:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:55:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:55:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:55:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:25dea15c4ffeb70e1112f1ee06dd948a8ab9dfc3b79ef239cb96080cc27ff1be`  
		Last Modified: Tue, 18 Nov 2025 01:13:47 GMT  
		Size: 48.6 MB (48591184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7442761efa65f5c2b8ea533bdf899a42a7675c104757f17e02556f4fb8e9b1`  
		Last Modified: Tue, 18 Nov 2025 03:55:30 GMT  
		Size: 11.3 MB (11255244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48646b8eda1068da8aaed34b5cab1846deb098a42975c11138a3a5949dbf2b40`  
		Last Modified: Tue, 18 Nov 2025 03:55:28 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74eee381d7f6529a319746474450b633a97370dce62728e2ef7ad068a023a2f2`  
		Last Modified: Tue, 18 Nov 2025 03:55:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7d4af7149a94e629b6505577fcbe8866b4bab79ca6f413e0a47f39515ac258`  
		Last Modified: Tue, 18 Nov 2025 03:55:28 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6cdc60206bb5f64f8f48ac0b1ada92e0746562966eb4588e033f00586bfff1`  
		Last Modified: Tue, 18 Nov 2025 03:55:28 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:30e70f2997d786cd98e0bd721ece2fe2b7fa22520c9e84c2a97875debc9767eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6882a6e3ee02ae9ae4109396d8e989351a7877d8e2876e150ad3670ced3c95`

```dockerfile
```

-	Layers:
	-	`sha256:4d89ca1be6665cdfc905578b87af2c5bcc78c8cbab78dc211a784b9f6e401e1b`  
		Last Modified: Tue, 18 Nov 2025 05:09:24 GMT  
		Size: 3.6 MB (3578313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c76a11b7847af5b890757dc45a0626a35c12771f24ac9352bf5efbde44662bf`  
		Last Modified: Tue, 18 Nov 2025 05:09:25 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:5af48f027b4bf48cdee6090d22551922b9a844d5d5a07910d479a440e699496a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61660272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9346116137dfaa71689745f00f12a0b4289514a6e182a2e5ca85439dd3403175`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:03:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:03:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:03:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:03:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:03:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:898cf630ac245ec9ad865c96204520b86bb7b8760d5bd2f14bd02745e43d82f4`  
		Last Modified: Tue, 18 Nov 2025 01:13:40 GMT  
		Size: 49.8 MB (49832238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0b6295fb3a0de9675da59780f9f04f82fb6dcdc2676ee484a93d1d29644c69`  
		Last Modified: Tue, 18 Nov 2025 03:03:50 GMT  
		Size: 11.7 MB (11734522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d910717d3eb8247dc5797a539a4501e15f2baabc57447b9e40100725d7bf149`  
		Last Modified: Tue, 18 Nov 2025 03:03:48 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac3671e7d327a12e834092b1f44ca16784cd66ea96c40cf45f0398e1b99af04`  
		Last Modified: Tue, 18 Nov 2025 03:03:48 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f22aff5a131d31db729bd6138d046dacb2be96f9ded5b0c4d416274d261cdf`  
		Last Modified: Tue, 18 Nov 2025 03:03:48 GMT  
		Size: 90.2 KB (90163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a543a8735d0a34b0f63dc1dcaa2ed6d8f2db203b8b5c1ee2d951c571b57353`  
		Last Modified: Tue, 18 Nov 2025 03:03:48 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a0f6863f842eabeed89212f42d99ec2925a2ff7a135b4e11706b9828510aa27d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2041d6b5f4b3615ac3cd6a4e876b23a9a9d37bb780b40e3482302391c9b87358`

```dockerfile
```

-	Layers:
	-	`sha256:6f42b733b57f390b5db85df406b02ab8db246d4befc1ad0cc48b1305eb6d15dd`  
		Last Modified: Tue, 18 Nov 2025 05:09:29 GMT  
		Size: 3.6 MB (3575400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4d1f5346f232ba860339a91bb3c9310d60c2691ca72115e3462cda0ecdd79d1`  
		Last Modified: Tue, 18 Nov 2025 05:09:30 GMT  
		Size: 15.9 KB (15928 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:0e98bbc3daae66df44ae11a5588f2309b4d0b0a3d5759a236557a26319c2c5b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:e6772d070a574f00e1ad07efb0f799b7e9d9020fccf9887c7f6378c50bdbe816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d6aeb77e4a5a773edcad5fc10b5e08d8f387161a9b7b5d93e1cb1aac4e3735`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3881e591a9050bd6250b7975f2a62d69ce9d4bc181a569e43d583973bfffafd6`  
		Last Modified: Thu, 13 Nov 2025 23:31:35 GMT  
		Size: 3.6 MB (3625726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7763c1732252c316b49e1a5ebe3d01e0ad636198993b3e20e7267f9fe62d4283`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59987cb0b364dad0627b12e7ef72104aea08b23fff39930f94dac5b79cf2585`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91714d8e9de2a6eab65bf534a21daeac5f710d6f823714736754481479f25eb`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 111.3 KB (111253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:74faf561f221e4ff0722a9a6a5469d286311b0d29d710a50c1c2f2d408089335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5093bdb0233d5e701687d2c9157af64b57724e81b512be660289bb7a4c8f7216`

```dockerfile
```

-	Layers:
	-	`sha256:288a50939bde1611937533ae039c8544b98d95d75331e8bde2456927a7ddea17`  
		Last Modified: Fri, 14 Nov 2025 02:07:40 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:941444796f9904d69ff28378466addce903b01de5df5c0c291ea8d117c6aff74`  
		Last Modified: Fri, 14 Nov 2025 02:07:41 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:09ed49f28825e5330d749e8aa583e2f0c2c88ace7f935f79fd1b4ee7cfd6502a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31094789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170be1c0c9e62fba389535f45096cb097ffcd73e82e10f8e5f2bbeb7101e7716`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:30:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:30:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:30:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:30:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4fc061e7db4abc03b992399d4d51a6e96a401904e29c8c7cfff6c2b0ef4cbc`  
		Last Modified: Thu, 13 Nov 2025 23:31:03 GMT  
		Size: 3.6 MB (3598146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e356cef2bd87e42a124fc4d5e82057772ca5cf202c6c194f6884f04283430a`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7f921b9372d265e8d3805815b0e98436f5f4b92fc0dae86070b7f4f269f992`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562a8628e6dc417f84896302f26a4b6c43f921ca7ce9b73b785936f7e5d51be2`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 110.6 KB (110588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4d3a9691d374823b1b504cf09f6f82049355ef10aa41d07d3be46ed00124eda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb368a6d54f82c2cad7c303b49a01491c62b68e3a47065952793b1df828ae`

```dockerfile
```

-	Layers:
	-	`sha256:c8a0004225abd4f8c618461be1e72c1192172f7ccfd4fa7f0839dbdc35d24f43`  
		Last Modified: Fri, 14 Nov 2025 02:07:45 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:200a3136b60277a7c0dac564342f17944ff690ca89305553d8bd0bcd74108f3a`  
		Last Modified: Fri, 14 Nov 2025 02:07:46 GMT  
		Size: 14.1 KB (14056 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:120b8715dd3a26a2af4049512591dcbb112d36e4accff9d7fded93e27ce47062
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ef9dcfb5426525d36ca828760110823e06e065cca0c4ac0682d0a506e9cf12e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33276245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abbe750921d6da2c2bf91fa655875aa86d26da7d2c93cd08dc4d8b4f91445af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3881e591a9050bd6250b7975f2a62d69ce9d4bc181a569e43d583973bfffafd6`  
		Last Modified: Thu, 13 Nov 2025 23:31:35 GMT  
		Size: 3.6 MB (3625726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7763c1732252c316b49e1a5ebe3d01e0ad636198993b3e20e7267f9fe62d4283`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59987cb0b364dad0627b12e7ef72104aea08b23fff39930f94dac5b79cf2585`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91714d8e9de2a6eab65bf534a21daeac5f710d6f823714736754481479f25eb`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 111.3 KB (111253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87663c843a43743cb4efbfd154e030c6591b4085d0c1d047a156158b9c47142a`  
		Last Modified: Thu, 13 Nov 2025 23:31:58 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8b9b5e291adc948bf145496030828a9a408c3399355380347b0ff72c16e2a880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970a1d784b637f4a06999658bbd7cfd5f71517ef14610d1888be4fc2d5614399`

```dockerfile
```

-	Layers:
	-	`sha256:19ad39194fba9b75b47c96c260e5431b390f0c1f40747e8857c995d53dd228f0`  
		Last Modified: Fri, 14 Nov 2025 02:07:48 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd46be2a48617b0b0891f5fe27958f8e2350a649da215ce9a4995e5a9a62d43d`  
		Last Modified: Fri, 14 Nov 2025 02:07:48 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8c05f54ab64c544f5b1833f0d31ef94804c914c6debd693acfce0dc0320660cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31095110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2b987bf931381f750375f7be732736b38d67dd928c373fb3ac7f7703364fd3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608dccde847e272476e52044e62fdf40902fdf981eba3f9e853d9bb36c3ebdf5`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 3.6 MB (3598157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff367c25857e7c190e4c69803b560c6e428a2f6fdcdef7291ed9c54595fd3a7`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d785e7ece3388bd939c0607e15ed02803f8e48b590bbf43d7b628f2275ed86`  
		Last Modified: Thu, 13 Nov 2025 23:31:37 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411f09f71214f6303934a66000e111fee3918961b6f6726ed9b784feeceb7fcf`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 110.6 KB (110611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa2aa73e9807dfaff0d65e73fea59b7275dac6754311bac380e78c75cf4c922`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f02cab47a327aef8e9eea19cc7a8da708ad76b7fd1cee2ccdc47f302f2cade08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5d2870c8ff27e82579456117c17077c9ecc56cf9812adeb91b20dcd8fdb489`

```dockerfile
```

-	Layers:
	-	`sha256:196e2a812f54eccdc16bfcfe68a337ef2397641ccf3672d5f6846a2c19b4a34d`  
		Last Modified: Fri, 14 Nov 2025 02:07:52 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be4dac85cb072f2caede51d4767494f8e063e10991e49a2febf5e030defd53e2`  
		Last Modified: Fri, 14 Nov 2025 02:07:53 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:86ac08e0cbf2640750a131de8ddf9bb285ed3c0359b84a4489b870b5bd4b9d73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:2f888be4d7159ed9a03884f72b0a18d428983c3c093c51acf701c4f3a8f58db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33394268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e41a68f6806fe09a43691a06544a172872ab66d56d34fd116ac854f53aa973a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:32:05 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a0ad9b4aaae6e7e946573addf6867a419111a60fc9323198684be47d29ab8e`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 3.6 MB (3562811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2192c9cd8ae78f10eb620c49dd6c3f1c97dbc3a99b8e0e54442bf4c4085d50be`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3fd385eef297b7ab043fbd27de442eb44e742de653f6f0beec541e5624920c`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9ba4094a4680b7c79b70bf18ec8e50552bb4bcde925a278b84fdf831ae1ce`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 103.9 KB (103855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:30e09776cbad0fdeb6250eeb59b6c85db722439c89e9ea463b8846b520362ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98fcd14e1e482b89c9f2956dd0d711c27c1041d1eecbc57b8cee5f200fb7e014`

```dockerfile
```

-	Layers:
	-	`sha256:7cb594c99ab7f7379858b0869eccc55ee5d16dd0c7a117ec2ea6286621e09d2e`  
		Last Modified: Fri, 14 Nov 2025 02:08:05 GMT  
		Size: 2.1 MB (2120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:874d5cd16621b1ee0eb69f6c404dabe165681b10474bdb7a0c987170e3243da9`  
		Last Modified: Fri, 14 Nov 2025 02:08:06 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:96b42b877a4656e7863be6795ffe062410d426123d20fcbe050944554329e1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32530527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79a782002d75afde88daf47c99b398edb58da7b5d5cca3827577832434b8abc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a253dba035401f762d0613aa4d977ce12d945bc1918bfb08a17ba7331fe815`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 3.6 MB (3561049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bd3e1c5570e7cd4878353726e4bd0fe6a358ae3cd2dad02e393d59d98803f9`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 2.6 KB (2640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b495cbf000ce9a258736ce76444ca683648a9ba468ca5d3d6cfde0d8bc89402`  
		Last Modified: Thu, 13 Nov 2025 23:31:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a7199ab9252b8ed239c8c34dd3a013dd0b7c2c06d87c00c361824931df4c86`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 104.6 KB (104607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5f3d14db57b4fa3eeb6cbb447024bf03395dfe359f372b7f4917ee462f439907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe6e66c6e7d0f92c843a2215edea604807c6be3f7f5ff9f9929c74d8d3d52f9`

```dockerfile
```

-	Layers:
	-	`sha256:ad647f1003e7e0dec3bdc34b289daefb923cc8e0c1305ba7b14f3a2108d14a3a`  
		Last Modified: Fri, 14 Nov 2025 02:08:10 GMT  
		Size: 2.1 MB (2121910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c6007dbe7aee0b4fb818dc38799ebc8efd1b7438bf95762182955214aecc0d`  
		Last Modified: Fri, 14 Nov 2025 02:08:11 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:184659c45ef82521389ee748e1ee4bbe1449f0946581307e3e93d86e0e058f4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c299aad60e1e7f11d4286835ce579930df7f598ed9b1015fcaa7c79713c42957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33394810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ed87def879102b787b9246c739018511b4b589c34932b0ef713c6c61de668d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:32:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:16 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c0e1d7b3f111e4566e1d12f6c0632e153c201260a9826542321f8ea23bcafa`  
		Last Modified: Thu, 13 Nov 2025 23:32:28 GMT  
		Size: 3.6 MB (3562936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b40e8d70ead7cc4f0cd07dae1ee6920efb006cb20528bcc7de39094ddf9874`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5ee6c709ae7dad0afff7391eaaa68296673cf0205a608f9bce6d4f7500e650`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd86eb2b24e5478ee0f7d4c55df8e6c357a999c4083997d6162434e36abba3f`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 103.8 KB (103841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b41bb95e32d18baa23088cddd23dfe1c3c097445ffe768613d34800b4c0c5`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:93bbbca7ef64d9156a3013b0c4e3fa3312e91da86a098db01ea9d83029661afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2465328c5c5e8df05ad265eb773fbf3e584134d29936e5a21430c0d9164a3e3`

```dockerfile
```

-	Layers:
	-	`sha256:aabcb977352301fab1d6dabefc144dcce2ebf0a3030cecf40cf83bc2aa92770b`  
		Last Modified: Fri, 14 Nov 2025 02:08:20 GMT  
		Size: 2.1 MB (2120901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82c114f49a06e6a45987c7131d46b1fe1220101c4997f7726a576f2a5543d25b`  
		Last Modified: Fri, 14 Nov 2025 02:08:21 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c6af2ae93699e738b6c0895055144b4bb347920aca7f91e4451aa75dde146236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32531089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989acad9c141ce3dcea15e9a18df4c3ea56ceedb189ef7a6b8b8dfac6823e87c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876648f4bcbbd9a79fe03bc85730393c6e24075dde48714e37bee27c5e932691`  
		Last Modified: Thu, 13 Nov 2025 23:32:17 GMT  
		Size: 3.6 MB (3561120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c874b0b5bacc6d952a7735777f05b95f3c5bcbe6b7f7d50b6dabee2398abad59`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660eaa03fbbddfa884bad13382570eba092d15224cbac502584ceb4f39f1bc8c`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05849e9ea827053df3f7378003dad6aefab958b313dcfc532a8b8cd4826355d`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 104.7 KB (104669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa5566c0de4309a0ef6703f3bee20e95197bb23f5d2a711b7cd280db22508a1`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:da8153a7c5dabd74fc895825a81e69cddc07810acc5675ecc956059d31108d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71031b6901d4ed1fbb3d94ff534deb64c3c8c0902724a95d29584e35420ca5f2`

```dockerfile
```

-	Layers:
	-	`sha256:6e2ac3e4bbdc32139f4d1a5d2b49adbffdd230b9c2f1f6cbc7952707749b342d`  
		Last Modified: Fri, 14 Nov 2025 02:08:25 GMT  
		Size: 2.1 MB (2121946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:024cf6e9493f7a6f8cac5b000f292b1bc84bfbbc6fb5d69d25b04d6d3c090a55`  
		Last Modified: Fri, 14 Nov 2025 02:08:26 GMT  
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
		Last Modified: Fri, 03 Oct 2025 12:41:25 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807958f6dce95c2cf132ab919d751d642e0834efea8afabde5dd80a06382164`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
		Size: 6.9 MB (6862222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9d85781ba57065c27119c5b829ede85b21f4be4c79ed21b52b5dd18e69324e`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b6000f4f29de58b9c57f46bf4c2915a41aecfde0ffe93b519dc150c2e05839`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b298e1353c735a6385e6a62cecbfe1d1b59a32feea6c006fe2970e9a377fb0`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
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
		Last Modified: Fri, 10 Oct 2025 01:07:52 GMT  
		Size: 2.1 MB (2129387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb29516268d88fbe0487f9e71585d01a2863eda154c3b84c932731ccf47ffd8`  
		Last Modified: Fri, 10 Oct 2025 01:07:54 GMT  
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
		Last Modified: Fri, 03 Oct 2025 12:41:25 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b8d7c0516946e6186f0c1918a80da44ccc80465d586f0db577e9c5e3fa309`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 6.4 MB (6392372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccd7c148caa4ff621b2e8f1407d0680d8b216fd3b91aade2da4e3bcf67242ab`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63a7c688f7b81b2251c0096fc2033ac1c2243330fd41da718cf8002ec93dae1`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a8bb23e4d96a15bc63dda952317ea8ba3a8efd39c025f4e5d59b26d5afc57c`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
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
		Last Modified: Fri, 10 Oct 2025 01:07:59 GMT  
		Size: 2.1 MB (2129631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3369301dca599eb9decd9b13cef9db3cbe5da13f1a35be39a2983729b9cd67db`  
		Last Modified: Fri, 10 Oct 2025 01:08:00 GMT  
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
		Last Modified: Fri, 03 Oct 2025 12:41:25 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e95813fe4718cf415f65b5a2a6aff41cf1ca472b75f81f0e71c88a2c1e75e9`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
		Size: 6.9 MB (6862197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c069ba67e04af50034555225735086ac2d283d240d8ce7e46a9d3308c6398c25`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7163aa66b2f0788a2fd8bfb24efa8a573ed390b32865ae0266981836fb3f2a`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4744d7aa582d29cc5ee3a878017b70e760a48aaf077eeaf1aa5c0b98f225a81b`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 103.6 KB (103637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709942cf2f7b8bc52d31c967ec725251f89630a82eb3debdaafff34b2502aec6`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
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
		Last Modified: Fri, 10 Oct 2025 01:08:09 GMT  
		Size: 2.1 MB (2129423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63f0d6a23d261b81b7b10446e66dbf147c195e56727be3c4c4095beb8744927b`  
		Last Modified: Fri, 10 Oct 2025 01:08:10 GMT  
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
		Last Modified: Fri, 03 Oct 2025 12:41:25 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d08ff3fe3897ede8ef5bf7e75a8c754e9da90066ad638138411914e6569fcb`  
		Last Modified: Thu, 09 Oct 2025 21:22:12 GMT  
		Size: 6.4 MB (6392412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87458cf3c50f45fec6029a8e2d31f7dc2c30d63c5e92c7e4f4d7ddbf1fd1fb4`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fabfa39ef821d160c97bf91453f07634d072ad956ea83de4da94873f2b71a97`  
		Last Modified: Thu, 09 Oct 2025 21:22:12 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9d80fbf3cdda43cd93b73ef0b7215c959689c5073a718bc28b1a88b435aeda`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 104.2 KB (104235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3181f804aca7e1622946b1391b32ee30ccebfbdb03426caab02bcd300d54cd8b`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
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
		Last Modified: Fri, 10 Oct 2025 01:08:14 GMT  
		Size: 2.1 MB (2129667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0912356738dd5be0731ed4354e13efdb3bb03dfc003407132e1ed93bde4ad42a`  
		Last Modified: Fri, 10 Oct 2025 01:08:15 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:86ac08e0cbf2640750a131de8ddf9bb285ed3c0359b84a4489b870b5bd4b9d73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:2f888be4d7159ed9a03884f72b0a18d428983c3c093c51acf701c4f3a8f58db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33394268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e41a68f6806fe09a43691a06544a172872ab66d56d34fd116ac854f53aa973a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:32:05 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a0ad9b4aaae6e7e946573addf6867a419111a60fc9323198684be47d29ab8e`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 3.6 MB (3562811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2192c9cd8ae78f10eb620c49dd6c3f1c97dbc3a99b8e0e54442bf4c4085d50be`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3fd385eef297b7ab043fbd27de442eb44e742de653f6f0beec541e5624920c`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9ba4094a4680b7c79b70bf18ec8e50552bb4bcde925a278b84fdf831ae1ce`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 103.9 KB (103855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:30e09776cbad0fdeb6250eeb59b6c85db722439c89e9ea463b8846b520362ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98fcd14e1e482b89c9f2956dd0d711c27c1041d1eecbc57b8cee5f200fb7e014`

```dockerfile
```

-	Layers:
	-	`sha256:7cb594c99ab7f7379858b0869eccc55ee5d16dd0c7a117ec2ea6286621e09d2e`  
		Last Modified: Fri, 14 Nov 2025 02:08:05 GMT  
		Size: 2.1 MB (2120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:874d5cd16621b1ee0eb69f6c404dabe165681b10474bdb7a0c987170e3243da9`  
		Last Modified: Fri, 14 Nov 2025 02:08:06 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:96b42b877a4656e7863be6795ffe062410d426123d20fcbe050944554329e1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32530527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79a782002d75afde88daf47c99b398edb58da7b5d5cca3827577832434b8abc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a253dba035401f762d0613aa4d977ce12d945bc1918bfb08a17ba7331fe815`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 3.6 MB (3561049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bd3e1c5570e7cd4878353726e4bd0fe6a358ae3cd2dad02e393d59d98803f9`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 2.6 KB (2640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b495cbf000ce9a258736ce76444ca683648a9ba468ca5d3d6cfde0d8bc89402`  
		Last Modified: Thu, 13 Nov 2025 23:31:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a7199ab9252b8ed239c8c34dd3a013dd0b7c2c06d87c00c361824931df4c86`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 104.6 KB (104607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5f3d14db57b4fa3eeb6cbb447024bf03395dfe359f372b7f4917ee462f439907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe6e66c6e7d0f92c843a2215edea604807c6be3f7f5ff9f9929c74d8d3d52f9`

```dockerfile
```

-	Layers:
	-	`sha256:ad647f1003e7e0dec3bdc34b289daefb923cc8e0c1305ba7b14f3a2108d14a3a`  
		Last Modified: Fri, 14 Nov 2025 02:08:10 GMT  
		Size: 2.1 MB (2121910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c6007dbe7aee0b4fb818dc38799ebc8efd1b7438bf95762182955214aecc0d`  
		Last Modified: Fri, 14 Nov 2025 02:08:11 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:184659c45ef82521389ee748e1ee4bbe1449f0946581307e3e93d86e0e058f4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c299aad60e1e7f11d4286835ce579930df7f598ed9b1015fcaa7c79713c42957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33394810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ed87def879102b787b9246c739018511b4b589c34932b0ef713c6c61de668d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:32:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:16 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c0e1d7b3f111e4566e1d12f6c0632e153c201260a9826542321f8ea23bcafa`  
		Last Modified: Thu, 13 Nov 2025 23:32:28 GMT  
		Size: 3.6 MB (3562936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b40e8d70ead7cc4f0cd07dae1ee6920efb006cb20528bcc7de39094ddf9874`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5ee6c709ae7dad0afff7391eaaa68296673cf0205a608f9bce6d4f7500e650`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd86eb2b24e5478ee0f7d4c55df8e6c357a999c4083997d6162434e36abba3f`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 103.8 KB (103841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b41bb95e32d18baa23088cddd23dfe1c3c097445ffe768613d34800b4c0c5`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:93bbbca7ef64d9156a3013b0c4e3fa3312e91da86a098db01ea9d83029661afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2465328c5c5e8df05ad265eb773fbf3e584134d29936e5a21430c0d9164a3e3`

```dockerfile
```

-	Layers:
	-	`sha256:aabcb977352301fab1d6dabefc144dcce2ebf0a3030cecf40cf83bc2aa92770b`  
		Last Modified: Fri, 14 Nov 2025 02:08:20 GMT  
		Size: 2.1 MB (2120901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82c114f49a06e6a45987c7131d46b1fe1220101c4997f7726a576f2a5543d25b`  
		Last Modified: Fri, 14 Nov 2025 02:08:21 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c6af2ae93699e738b6c0895055144b4bb347920aca7f91e4451aa75dde146236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32531089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989acad9c141ce3dcea15e9a18df4c3ea56ceedb189ef7a6b8b8dfac6823e87c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876648f4bcbbd9a79fe03bc85730393c6e24075dde48714e37bee27c5e932691`  
		Last Modified: Thu, 13 Nov 2025 23:32:17 GMT  
		Size: 3.6 MB (3561120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c874b0b5bacc6d952a7735777f05b95f3c5bcbe6b7f7d50b6dabee2398abad59`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660eaa03fbbddfa884bad13382570eba092d15224cbac502584ceb4f39f1bc8c`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05849e9ea827053df3f7378003dad6aefab958b313dcfc532a8b8cd4826355d`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 104.7 KB (104669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa5566c0de4309a0ef6703f3bee20e95197bb23f5d2a711b7cd280db22508a1`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:da8153a7c5dabd74fc895825a81e69cddc07810acc5675ecc956059d31108d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71031b6901d4ed1fbb3d94ff534deb64c3c8c0902724a95d29584e35420ca5f2`

```dockerfile
```

-	Layers:
	-	`sha256:6e2ac3e4bbdc32139f4d1a5d2b49adbffdd230b9c2f1f6cbc7952707749b342d`  
		Last Modified: Fri, 14 Nov 2025 02:08:25 GMT  
		Size: 2.1 MB (2121946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:024cf6e9493f7a6f8cac5b000f292b1bc84bfbbc6fb5d69d25b04d6d3c090a55`  
		Last Modified: Fri, 14 Nov 2025 02:08:26 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:99e725ba2098d9f5e4ac5df767e2791f2262c541d9d3ce6882a7df90623ca8f4
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
$ docker pull neurodebian@sha256:e3189cb38355d9a10e6ee69e26edb6de39b465cd8205913d981661a29d17dc79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59673174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa59c2c3a955fb01be15b8113061546e9756a4d36c3c7470857ae9c252cc428e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:25:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:25:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:25:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:25:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:25:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16dc4dbae62748d5ea26ad4fa94cc1e428529554cea8d528dae4b9e632092a3`  
		Last Modified: Tue, 18 Nov 2025 05:25:28 GMT  
		Size: 10.3 MB (10290035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f327eeba29be5557be80af3b3e54fb4b66e7f3114688f91d0d1a86e4c984e22`  
		Last Modified: Tue, 18 Nov 2025 05:25:27 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41eef2006d4e3c6079b7b7337b729efde57322b6d767c4c14d885db8d04b5b`  
		Last Modified: Tue, 18 Nov 2025 05:25:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d9879da8be8e094ac028797b0fae41f652046596a4c4ee377662c727affdcd`  
		Last Modified: Tue, 18 Nov 2025 05:25:28 GMT  
		Size: 90.2 KB (90243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266c69e3259acfd42f890841b091de6cfd0c84ac1ae6a4b555eecaf76fd850e9`  
		Last Modified: Tue, 18 Nov 2025 05:25:28 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0ddfdbc93c093ddbc557c782dec3add89cf90224b2a180e7e5a71db3a4f8882d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0e797be24246896583645947ee35f3f7738ecb63481336f5cb31d86c2f4ce8`

```dockerfile
```

-	Layers:
	-	`sha256:6108611c93b32a422b3f74aab105a2735fdd09db8ae15bbd2c08ae8a70670e13`  
		Last Modified: Tue, 18 Nov 2025 08:09:20 GMT  
		Size: 3.6 MB (3613069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36168299857e7e157d6e02f98dd16e7bb6377db14cc095d6a0b8df02014250c2`  
		Last Modified: Tue, 18 Nov 2025 08:09:21 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:cbe051ff9e65e938ef970ed213bed1845e12d099468e69ee359adf3f29216d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d723f4d19be58aaf30cbc45c642741452d891db5e4ce1244af5c7ab9483bd6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:53:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:53:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:53:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:54:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:54:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a505c9bb250d77e4640e96c444c4fac586fc1433c373bbef83a7256e04d6ade`  
		Last Modified: Tue, 18 Nov 2025 03:54:19 GMT  
		Size: 10.1 MB (10073459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904db87cf72b19c511cfe31ac93b95a3ed1ba1f7c9bb7582ee6eb938d2e164d4`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842dfa2696e5c96bc037b37dd0932b97434244d91043450150d9e96bdd37472b`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaca400b700bdb23c02eff76b5d0d5caf6a698ebaf8497f19a82b8f417b1b01e`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 90.9 KB (90944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d36449c0d721c1d3cd641f286b2d678c32dcaa57534317626ed05a07c2d19fe`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6e09f67ac5afd71c56c4130e2c079060e9181289a300b5159f7fdcc66744b050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72700cb5e900ded97e722e6c8b510c0b93dc64d74713213f9746adc344fea7d`

```dockerfile
```

-	Layers:
	-	`sha256:9c9cb02fac134943ac6de2142d5414212aaa7d7329798636b6a8f64c46838920`  
		Last Modified: Tue, 18 Nov 2025 05:10:07 GMT  
		Size: 3.6 MB (3614596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52009749de1793d97606f0008b38292d4695967e6cac6f459d6a77f967bde8c8`  
		Last Modified: Tue, 18 Nov 2025 05:10:08 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:df5a33264cb70ceafdfdded5c3985656daf4489cbef1599dc6d616fb55d10d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91d5238a64d084798a94a0f5bbcbab41284c53a2939727b9ef7d026393e446b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:02:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:02:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:02:35 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:02:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:02:39 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:bf2a49c122745d1757b9ecb1c9b1d8252491e66b62d1c279080155aaa530a615`  
		Last Modified: Tue, 18 Nov 2025 01:13:10 GMT  
		Size: 50.8 MB (50801744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5c0824538c3115239695f48f023fa765aa984377851b00dc5bda2cfb78f0f4`  
		Last Modified: Tue, 18 Nov 2025 03:02:54 GMT  
		Size: 10.5 MB (10462815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efd84fd0f053203220666c2fc0ad3385d5508791dc63fa0de95dda5f7b47034`  
		Last Modified: Tue, 18 Nov 2025 03:02:53 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43491474c911114c1ea18ff4901547554394f1757ff2be3facef60a2af71163`  
		Last Modified: Tue, 18 Nov 2025 03:02:53 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5294129b5628e65891a7dd0fe5bd29ff3190e979eb91d98d77278a9614c0085`  
		Last Modified: Tue, 18 Nov 2025 03:02:53 GMT  
		Size: 90.6 KB (90617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f592a181d12cc8795e06ae7cd55f2152c4e55653b5a2f8e1d71a65305a29d9`  
		Last Modified: Tue, 18 Nov 2025 03:02:53 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:488f520ba92c5294e525ab10cdb9145c7b5c9dff6eedbad68ac5de96b13dbf35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b13ba51f807628099a34bcb151c6aa443a39e3bccfb5506b3456315ba489fb8`

```dockerfile
```

-	Layers:
	-	`sha256:a0f61787fb9b6f94344751cfb224a1243f2bf661be7453be08765c8f77bdc249`  
		Last Modified: Tue, 18 Nov 2025 05:10:11 GMT  
		Size: 3.6 MB (3611018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07484fba44c1bfedea9943a0c3add1849143bf110d7703773edeec6a8ba5769c`  
		Last Modified: Tue, 18 Nov 2025 05:10:12 GMT  
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
		Last Modified: Fri, 03 Oct 2025 12:41:25 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807958f6dce95c2cf132ab919d751d642e0834efea8afabde5dd80a06382164`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
		Size: 6.9 MB (6862222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9d85781ba57065c27119c5b829ede85b21f4be4c79ed21b52b5dd18e69324e`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b6000f4f29de58b9c57f46bf4c2915a41aecfde0ffe93b519dc150c2e05839`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b298e1353c735a6385e6a62cecbfe1d1b59a32feea6c006fe2970e9a377fb0`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
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
		Last Modified: Fri, 10 Oct 2025 01:07:52 GMT  
		Size: 2.1 MB (2129387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb29516268d88fbe0487f9e71585d01a2863eda154c3b84c932731ccf47ffd8`  
		Last Modified: Fri, 10 Oct 2025 01:07:54 GMT  
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
		Last Modified: Fri, 03 Oct 2025 12:41:25 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b8d7c0516946e6186f0c1918a80da44ccc80465d586f0db577e9c5e3fa309`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 6.4 MB (6392372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccd7c148caa4ff621b2e8f1407d0680d8b216fd3b91aade2da4e3bcf67242ab`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63a7c688f7b81b2251c0096fc2033ac1c2243330fd41da718cf8002ec93dae1`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a8bb23e4d96a15bc63dda952317ea8ba3a8efd39c025f4e5d59b26d5afc57c`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
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
		Last Modified: Fri, 10 Oct 2025 01:07:59 GMT  
		Size: 2.1 MB (2129631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3369301dca599eb9decd9b13cef9db3cbe5da13f1a35be39a2983729b9cd67db`  
		Last Modified: Fri, 10 Oct 2025 01:08:00 GMT  
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
		Last Modified: Fri, 03 Oct 2025 12:41:25 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e95813fe4718cf415f65b5a2a6aff41cf1ca472b75f81f0e71c88a2c1e75e9`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
		Size: 6.9 MB (6862197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c069ba67e04af50034555225735086ac2d283d240d8ce7e46a9d3308c6398c25`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7163aa66b2f0788a2fd8bfb24efa8a573ed390b32865ae0266981836fb3f2a`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4744d7aa582d29cc5ee3a878017b70e760a48aaf077eeaf1aa5c0b98f225a81b`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 103.6 KB (103637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709942cf2f7b8bc52d31c967ec725251f89630a82eb3debdaafff34b2502aec6`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
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
		Last Modified: Fri, 10 Oct 2025 01:08:09 GMT  
		Size: 2.1 MB (2129423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63f0d6a23d261b81b7b10446e66dbf147c195e56727be3c4c4095beb8744927b`  
		Last Modified: Fri, 10 Oct 2025 01:08:10 GMT  
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
		Last Modified: Fri, 03 Oct 2025 12:41:25 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d08ff3fe3897ede8ef5bf7e75a8c754e9da90066ad638138411914e6569fcb`  
		Last Modified: Thu, 09 Oct 2025 21:22:12 GMT  
		Size: 6.4 MB (6392412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87458cf3c50f45fec6029a8e2d31f7dc2c30d63c5e92c7e4f4d7ddbf1fd1fb4`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fabfa39ef821d160c97bf91453f07634d072ad956ea83de4da94873f2b71a97`  
		Last Modified: Thu, 09 Oct 2025 21:22:12 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9d80fbf3cdda43cd93b73ef0b7215c959689c5073a718bc28b1a88b435aeda`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 104.2 KB (104235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3181f804aca7e1622946b1391b32ee30ccebfbdb03426caab02bcd300d54cd8b`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
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
		Last Modified: Fri, 10 Oct 2025 01:08:14 GMT  
		Size: 2.1 MB (2129667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0912356738dd5be0731ed4354e13efdb3bb03dfc003407132e1ed93bde4ad42a`  
		Last Modified: Fri, 10 Oct 2025 01:08:15 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:f6780519431067a744bf9cd5c67a3af9d80bbd6705a0e17b784ae3d117768809
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
$ docker pull neurodebian@sha256:7e4dba6577c604f109e75c30cf20e4f6fd699286502fcfb453b4bfb22cb48527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60182085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73970ee9b45105fb655a0dde7518d96ca729ff9ba43a0ca4b7338c67060af4ff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 05:26:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:26:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:26:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:26:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:63fb544511bd02db3b85f4aa7407dbf6c6f5cd7cb1c0c1e65d055477ac245bcf`  
		Last Modified: Tue, 18 Nov 2025 02:31:43 GMT  
		Size: 48.5 MB (48500427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd6e3358f9a9d38391f078b89e94e4fab3194e262c2c4912482c748b3dc375f`  
		Last Modified: Tue, 18 Nov 2025 05:26:33 GMT  
		Size: 11.6 MB (11588927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ae8f61696c3e71e17c0f2c9c8a0fa545b960d97eea442de3dad605fd6be80a`  
		Last Modified: Tue, 18 Nov 2025 05:26:32 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1577d641287ece0d6f861e7b6ea8895e1625249c9fe9a5e35508a1564ad2186`  
		Last Modified: Tue, 18 Nov 2025 05:26:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44c99b2d280c8613effd222ebbadc96bb2d7e02b2fa1acfee6227b830b2dbb6`  
		Last Modified: Tue, 18 Nov 2025 05:26:32 GMT  
		Size: 89.8 KB (89829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ec8497f0bd4ec4c67fabbcc277e209ddd51f1bb88ec8c6f83ec88a45d5939ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9ef28067c818eb96ef79ef4d952d161d5df5ef05746762cded700e6b46ce62`

```dockerfile
```

-	Layers:
	-	`sha256:bf147eec738b6618cb9898c72065974527c1f91c9ab72bc2312754d3860265ca`  
		Last Modified: Tue, 18 Nov 2025 08:08:56 GMT  
		Size: 3.6 MB (3577395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd1a1293a55e0d1e1951acdc9c5ad6a34ada3007054ae1b7e0ce609fbc96ab95`  
		Last Modified: Tue, 18 Nov 2025 08:08:57 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:541357f0ecf1813a8cbd720ff8f96f2cd982d89fd4bc89827c69d551b0163a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59940394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45372882da5d68ae7df8f8d65d5521dcd46ddef2d90a0366725a381de0b94cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:56:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:56:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:56:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:56:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2b90f6fb16dc868101354a233036d6d70e13cd3477e4df5ab59f2ccc8607c1d4`  
		Last Modified: Tue, 18 Nov 2025 01:13:53 GMT  
		Size: 48.6 MB (48591389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2c0b4f8506d03d13edc8f4045814717acfb0bd4cc0328aae44b4d8f1bb7d1f`  
		Last Modified: Tue, 18 Nov 2025 03:56:30 GMT  
		Size: 11.3 MB (11255621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02b54aa8ab0ab54e708c0c245ecdc268d95f50763ee5e6a6ed6a4adb1d2b80c`  
		Last Modified: Tue, 18 Nov 2025 03:56:31 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137f7f093c10ede28087087e92707167136eed0692d4cb8a57ff45159fe7ab43`  
		Last Modified: Tue, 18 Nov 2025 03:56:29 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2204582058e6da481caf8d806747650c50de23d03051094ad0639f303ac14315`  
		Last Modified: Tue, 18 Nov 2025 03:56:29 GMT  
		Size: 90.5 KB (90480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fde860d58516366ee33015d1436096dd5e23e8f17964da184f085573fd9cc39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3ab53141102408437089c3592249acd27598f72cfda4ae449b0b6ce85fc3a7`

```dockerfile
```

-	Layers:
	-	`sha256:3124dcc841b669bd8bed1254d0af82173424f14bc28093da966b9fa449b12735`  
		Last Modified: Tue, 18 Nov 2025 05:09:40 GMT  
		Size: 3.6 MB (3578271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2859914cd0af245c67d2aa284e5b6e40a46c065c99688f18da5d11a1320ce86`  
		Last Modified: Tue, 18 Nov 2025 05:09:41 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:cf250cb431aad9ebe2b195e7d6e846fb7684629d0bb110655d9b36c9902c9895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61660804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52b9c65d4da4a7a8580d37a51890774004410d2d1e5c564e1dd6c82e528a45c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:04:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:04:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:04:28 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:04:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b1df74e42eaae76d71bf2c2aa402328d711dcdb63b4080ae4e7050388c00bad0`  
		Last Modified: Tue, 18 Nov 2025 01:12:57 GMT  
		Size: 49.8 MB (49833161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b695f28e24e29bb497155794be92fb6864604ef5dcf9c7b8df607b037003c3`  
		Last Modified: Tue, 18 Nov 2025 03:04:46 GMT  
		Size: 11.7 MB (11734531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c7ee6a50715b7cbfe05ff35e8bc76866ea39eed7bc2312aac9189a98e60b4`  
		Last Modified: Tue, 18 Nov 2025 03:04:45 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698291bc223fcddc6f726de48b27d024db48b81354767ae1e7c278be80cc8c7c`  
		Last Modified: Tue, 18 Nov 2025 03:04:45 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c145c0389a87f3aa4c268694c98e50f6b0661557e0f4bd035134a4b8ea4858`  
		Last Modified: Tue, 18 Nov 2025 03:04:45 GMT  
		Size: 90.2 KB (90211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:100db007c6b4b3ad449b053788054967155478cb079a7ae6b46e829e8e338726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace921b5ef700155ccd0cf3b3785a2c55a76118407491be2df5d0a9a3e77668a`

```dockerfile
```

-	Layers:
	-	`sha256:9f412a45176e3fe1ab3f8f36c151902556e9c91c43d32015b8e453ceb4f2072b`  
		Last Modified: Tue, 18 Nov 2025 05:09:45 GMT  
		Size: 3.6 MB (3575358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d47ad7342a0b76ced1fe2e5779fbfed36c343b6e87c8b2b260a0cc83d9f53ebd`  
		Last Modified: Tue, 18 Nov 2025 05:09:46 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:c5581a4d453de72755f23515c2070ae0f211f8375ea147fa941339c5f6978f7c
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
$ docker pull neurodebian@sha256:e762587ae4044d398a4950827433a33757d3e118c3df11cd0a90fb82ce53dc8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60182437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5925223478748274668b5ec192c8efdd7ff04cd7ce3a4a0ddce021a46f4fc50b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 05:26:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:26:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:26:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:26:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:26:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:63fb544511bd02db3b85f4aa7407dbf6c6f5cd7cb1c0c1e65d055477ac245bcf`  
		Last Modified: Tue, 18 Nov 2025 02:31:43 GMT  
		Size: 48.5 MB (48500427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868501aae139938a2df6b8c1e34a48b3f8aa21b1d0da7c2e70e050d39175ec5c`  
		Last Modified: Tue, 18 Nov 2025 05:27:00 GMT  
		Size: 11.6 MB (11588863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470d047aa02066b96ec1483e1ed7bea661ac4a8f05ad598c6bbc17eb277035bf`  
		Last Modified: Tue, 18 Nov 2025 05:26:59 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2bff1bd5008202d0cf3b78801f1d6cb6e71c6418c3d3b331e8581eef9cb7ff`  
		Last Modified: Tue, 18 Nov 2025 05:26:59 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64ceb5cc47fd60e60b7751683b3117dce7b49fc7ece1eb62194765e538bf40d`  
		Last Modified: Tue, 18 Nov 2025 05:26:59 GMT  
		Size: 89.8 KB (89827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78caf42b1e460472b71623a4528efb1808b4001eba2e6860bcc6c8d3c75c41d9`  
		Last Modified: Tue, 18 Nov 2025 05:26:59 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c78fc698df0d640da2e09714972bdcca64fcf270b12f2f7ec4455c1f7b03f978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e9aa74511cab257d2f5476a4dd6e98674487cd3c2671fb021dab55e03e1157`

```dockerfile
```

-	Layers:
	-	`sha256:dedd26f7e64d36e3a4121a0b02d24e8e73025be59f89a540652e8c44b4239f9e`  
		Last Modified: Tue, 18 Nov 2025 08:09:02 GMT  
		Size: 3.6 MB (3577431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4951412701f1be19c6efd634bd5d4c33331017fbfea4356190ede4f13343a4f5`  
		Last Modified: Tue, 18 Nov 2025 08:09:03 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9c548a571e85b70b292b96813cd00941bf3e96b959057db5b2572c2dfee4aeca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59940885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5c33d75154b40af5a4e2ed79dfdfd6a916e3cda19c539fe5f34c6f4cf23f76`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:57:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:57:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:57:14 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:57:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:57:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2b90f6fb16dc868101354a233036d6d70e13cd3477e4df5ab59f2ccc8607c1d4`  
		Last Modified: Tue, 18 Nov 2025 01:13:53 GMT  
		Size: 48.6 MB (48591389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1473a9ef112b3354ecb8ad37437881c07c1330a179af790e6197afe69d118085`  
		Last Modified: Tue, 18 Nov 2025 03:57:32 GMT  
		Size: 11.3 MB (11255640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee7b3173ae7900350aa0c13fb1183ca91219d5891202b3cff35eeaf1c80b7d5`  
		Last Modified: Tue, 18 Nov 2025 03:57:31 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9797247299d9f83b806b73618e195baa0f95d2ddc9b81bb9c6cb69852d70360a`  
		Last Modified: Tue, 18 Nov 2025 03:57:31 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305d3575bebd85f0bb2b4936522cbfe2058213f281cf396211a6dcaba921569a`  
		Last Modified: Tue, 18 Nov 2025 03:57:31 GMT  
		Size: 90.5 KB (90533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07a8228ced17f46f7ea430082bebae91f27757072506586bc99ec87f75f6d0a`  
		Last Modified: Tue, 18 Nov 2025 03:57:31 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ef97f524e0b4f5a6f8fbe1cf7cc8862b248979d93944230a0e6ef10ce6a2bc5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a332782142e357fb40eae518f5fc9a7ccd220d630e0da1481cedc4f1684377e`

```dockerfile
```

-	Layers:
	-	`sha256:6cd1b21fff2d2212e067d9150271763da862a313f3c4b2fcb4e5fa0c42f1f4ca`  
		Last Modified: Tue, 18 Nov 2025 05:09:49 GMT  
		Size: 3.6 MB (3578307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581ffbae3cc89923c70c60e4c5b10f6337934afca176aedaec8dbb8f3f4fc942`  
		Last Modified: Tue, 18 Nov 2025 05:09:50 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:2355b2b15ca42c2281d7dbc7f25dba05c3f444218ac341d44b0cc3b91e6c4f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61661269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8e397017c23070f405400256017fd62c2efb1acaaf65aa58abd92fbccc4b86`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:05:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:05:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:05:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:05:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:05:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b1df74e42eaae76d71bf2c2aa402328d711dcdb63b4080ae4e7050388c00bad0`  
		Last Modified: Tue, 18 Nov 2025 01:12:57 GMT  
		Size: 49.8 MB (49833161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320747deac046e78cc6cd5bf1f43512ceac0dcd4bc46633b37bac1da49cc2347`  
		Last Modified: Tue, 18 Nov 2025 03:05:50 GMT  
		Size: 11.7 MB (11734574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb1dc298560a964b377102c4017b5c4f003eac17020d279bbc350786f83b343`  
		Last Modified: Tue, 18 Nov 2025 03:05:49 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cacfbd2b30909444f5547038302340f534c5a64f670a16b357f7b9bfbf040c`  
		Last Modified: Tue, 18 Nov 2025 03:05:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc92a3f91e7b2a6ae7fe7bfc48ae16482ba42011cd41e8ef88915792904294f`  
		Last Modified: Tue, 18 Nov 2025 03:05:49 GMT  
		Size: 90.2 KB (90212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63c4ce8d0e216b5aab98536e70d2080de788be29e1760ab60b24b41b43d0a18`  
		Last Modified: Tue, 18 Nov 2025 03:05:49 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:31bf8c50269d41bc97ac9cd64fd1c8d86ec815b301ed715139861791cd73eb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2729a5a69bdcfbb87abddc99d2d863357ac7cbe6d4132f113c0dc4325fc8557`

```dockerfile
```

-	Layers:
	-	`sha256:2aa0e8b7828a6c1deff36c806b411f7001a9cd34e0af414a449a1094d7119b5c`  
		Last Modified: Tue, 18 Nov 2025 05:09:53 GMT  
		Size: 3.6 MB (3575394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecb4ecd39798b3b865e36c5ec98d70a94d6385b022ee279c0de675396f9f5a84`  
		Last Modified: Tue, 18 Nov 2025 05:09:54 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:018039aa28469cb574577be011ffba1b39df9ca46864a220f31a05a376249830
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
$ docker pull neurodebian@sha256:a6b82875250b39bce69a473895862362fc6c0fc619b8aa62cecbc36ddafea16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59672386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44fc91da823f52c537b6e13a4c462a693e58d4a8ea793dd62e90e451905af64`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:24:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:24:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:24:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:24:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbc7b1c2d62df985e7aff96ee3ece36abe8cf517d7f993fe66c2a5d85e28a00`  
		Last Modified: Tue, 18 Nov 2025 05:25:09 GMT  
		Size: 10.3 MB (10289731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5364e6fa5c4502194ff9ec23ca3d5e09b80eeccc4f4f58584beafec862b4f8b`  
		Last Modified: Tue, 18 Nov 2025 05:25:06 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e3e7f0c19fc5bfe238e52366df56925c734e376f238cc681974db438f32253`  
		Last Modified: Tue, 18 Nov 2025 05:25:06 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1ca7993e2d88612125c1707875d1da317111bb55e9cd88b5bbe786067453a7`  
		Last Modified: Tue, 18 Nov 2025 05:25:06 GMT  
		Size: 90.2 KB (90204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:df927e54faea7df4d76f3a405b8d22dfe4a687c81abd444f5389a9d65bb4aeb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2d4278a656ee84173516bbd88d5c411730eaca56631895ecae5b804adaa9a`

```dockerfile
```

-	Layers:
	-	`sha256:3c0e4dc230c96b33215e0db6946acca5920ddc0b14b5270e6497a701a792a37b`  
		Last Modified: Tue, 18 Nov 2025 08:08:51 GMT  
		Size: 3.6 MB (3613029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c182edb049488b2af0cf55dff839e72d56dbd8f86a9812723dc44ca3903f66`  
		Last Modified: Tue, 18 Nov 2025 08:08:52 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:03f45755a0cbd0fa591dc83b3f174f408ec09689438dd1f600685d2cde3859bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec1e38ad20d40f39f7b16d2bbf5d3dcaddb31d59c129758a0bf91ac4a087408`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:53:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:53:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:53:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:53:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39eff5378ff39f272aafcd4e6eb21f0002984d7ba123df62005a1c72b904f39f`  
		Last Modified: Tue, 18 Nov 2025 03:53:24 GMT  
		Size: 10.1 MB (10073386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7768b0faa974ae0a24a5fc2d6d8ab83d8bfbaac5c1c6b88142e79c4e9331d292`  
		Last Modified: Tue, 18 Nov 2025 03:53:23 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4803b1be5a4e9ea2b53fa1893acd4bfcfcc977b674beb4d6c9df3d231a97eb4e`  
		Last Modified: Tue, 18 Nov 2025 03:53:23 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239af7ab87748df14555e1392f8dbd23b17160c367fd5fab152ab0d11134d812`  
		Last Modified: Tue, 18 Nov 2025 03:53:23 GMT  
		Size: 90.9 KB (90895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4233619c2439c669dcbd798b18d3779f25a61d90424651cd1a47825c92259fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c67bfaa7bdaea4ffbeca1e70fcfdbd3beb9885e4ede0de846eb219c971de3e`

```dockerfile
```

-	Layers:
	-	`sha256:105073c6ec3e7f5c078d5e10ecdbbf90eaf703f3743f3044afb9c8e051305965`  
		Last Modified: Tue, 18 Nov 2025 05:09:31 GMT  
		Size: 3.6 MB (3614556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfef6ecb903761ecd001f5326ba3ebf4549b1e7fd94a1e645e8f1707779545e4`  
		Last Modified: Tue, 18 Nov 2025 05:09:32 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:17dfc4286fd752b3d3d0bf9fb20d8810070cd8191073f82eaa5374a0e65cbccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4b5d6645061105ccbb028eb3fefe29edfa9a55b0172aa02ee45104cffd1993`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:01:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:01:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:01:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:01:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bf2a49c122745d1757b9ecb1c9b1d8252491e66b62d1c279080155aaa530a615`  
		Last Modified: Tue, 18 Nov 2025 01:13:10 GMT  
		Size: 50.8 MB (50801744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e17a20228b22b602cbbfa5680fffb9f4f423b2b773d66726620a3e615f494c`  
		Last Modified: Tue, 18 Nov 2025 03:02:14 GMT  
		Size: 10.5 MB (10462815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d43cb3b26404265a2415ae726de37e382f8bca2b3573d437ed0af59780d869`  
		Last Modified: Tue, 18 Nov 2025 03:02:13 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a98988b1a0d709c24b8a75b233813c646170d9954599a23bc28f542a481ccce`  
		Last Modified: Tue, 18 Nov 2025 03:02:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7df26ae6119f7ad73c3e54631b21eeca4094687be7a3ef5df86c7c0077dac9`  
		Last Modified: Tue, 18 Nov 2025 03:02:13 GMT  
		Size: 90.6 KB (90602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5cb23b9eed1f0fee69d391b347817aacd1bb16034b6dc063849bb4362d18bec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a0c9860b662de961e7066a34a6cf69a21b4362ea5bc02fe635ad924a557071`

```dockerfile
```

-	Layers:
	-	`sha256:4d4d4e2a77ef0acaa1a67ff1b69ebcc224babe7fb3cdc53b737a11cb53e2332e`  
		Last Modified: Tue, 18 Nov 2025 05:09:36 GMT  
		Size: 3.6 MB (3610978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0491f3d73f6c0769dcbd447cf474664a488215c438ced43977ad268347ba666d`  
		Last Modified: Tue, 18 Nov 2025 05:09:36 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:99e725ba2098d9f5e4ac5df767e2791f2262c541d9d3ce6882a7df90623ca8f4
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
$ docker pull neurodebian@sha256:e3189cb38355d9a10e6ee69e26edb6de39b465cd8205913d981661a29d17dc79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59673174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa59c2c3a955fb01be15b8113061546e9756a4d36c3c7470857ae9c252cc428e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:25:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:25:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:25:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:25:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:25:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16dc4dbae62748d5ea26ad4fa94cc1e428529554cea8d528dae4b9e632092a3`  
		Last Modified: Tue, 18 Nov 2025 05:25:28 GMT  
		Size: 10.3 MB (10290035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f327eeba29be5557be80af3b3e54fb4b66e7f3114688f91d0d1a86e4c984e22`  
		Last Modified: Tue, 18 Nov 2025 05:25:27 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41eef2006d4e3c6079b7b7337b729efde57322b6d767c4c14d885db8d04b5b`  
		Last Modified: Tue, 18 Nov 2025 05:25:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d9879da8be8e094ac028797b0fae41f652046596a4c4ee377662c727affdcd`  
		Last Modified: Tue, 18 Nov 2025 05:25:28 GMT  
		Size: 90.2 KB (90243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266c69e3259acfd42f890841b091de6cfd0c84ac1ae6a4b555eecaf76fd850e9`  
		Last Modified: Tue, 18 Nov 2025 05:25:28 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0ddfdbc93c093ddbc557c782dec3add89cf90224b2a180e7e5a71db3a4f8882d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0e797be24246896583645947ee35f3f7738ecb63481336f5cb31d86c2f4ce8`

```dockerfile
```

-	Layers:
	-	`sha256:6108611c93b32a422b3f74aab105a2735fdd09db8ae15bbd2c08ae8a70670e13`  
		Last Modified: Tue, 18 Nov 2025 08:09:20 GMT  
		Size: 3.6 MB (3613069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36168299857e7e157d6e02f98dd16e7bb6377db14cc095d6a0b8df02014250c2`  
		Last Modified: Tue, 18 Nov 2025 08:09:21 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:cbe051ff9e65e938ef970ed213bed1845e12d099468e69ee359adf3f29216d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d723f4d19be58aaf30cbc45c642741452d891db5e4ce1244af5c7ab9483bd6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:53:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:53:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:53:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:54:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:54:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a505c9bb250d77e4640e96c444c4fac586fc1433c373bbef83a7256e04d6ade`  
		Last Modified: Tue, 18 Nov 2025 03:54:19 GMT  
		Size: 10.1 MB (10073459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904db87cf72b19c511cfe31ac93b95a3ed1ba1f7c9bb7582ee6eb938d2e164d4`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842dfa2696e5c96bc037b37dd0932b97434244d91043450150d9e96bdd37472b`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaca400b700bdb23c02eff76b5d0d5caf6a698ebaf8497f19a82b8f417b1b01e`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 90.9 KB (90944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d36449c0d721c1d3cd641f286b2d678c32dcaa57534317626ed05a07c2d19fe`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6e09f67ac5afd71c56c4130e2c079060e9181289a300b5159f7fdcc66744b050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72700cb5e900ded97e722e6c8b510c0b93dc64d74713213f9746adc344fea7d`

```dockerfile
```

-	Layers:
	-	`sha256:9c9cb02fac134943ac6de2142d5414212aaa7d7329798636b6a8f64c46838920`  
		Last Modified: Tue, 18 Nov 2025 05:10:07 GMT  
		Size: 3.6 MB (3614596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52009749de1793d97606f0008b38292d4695967e6cac6f459d6a77f967bde8c8`  
		Last Modified: Tue, 18 Nov 2025 05:10:08 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:df5a33264cb70ceafdfdded5c3985656daf4489cbef1599dc6d616fb55d10d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91d5238a64d084798a94a0f5bbcbab41284c53a2939727b9ef7d026393e446b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:02:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:02:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:02:35 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:02:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:02:39 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:bf2a49c122745d1757b9ecb1c9b1d8252491e66b62d1c279080155aaa530a615`  
		Last Modified: Tue, 18 Nov 2025 01:13:10 GMT  
		Size: 50.8 MB (50801744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5c0824538c3115239695f48f023fa765aa984377851b00dc5bda2cfb78f0f4`  
		Last Modified: Tue, 18 Nov 2025 03:02:54 GMT  
		Size: 10.5 MB (10462815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efd84fd0f053203220666c2fc0ad3385d5508791dc63fa0de95dda5f7b47034`  
		Last Modified: Tue, 18 Nov 2025 03:02:53 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43491474c911114c1ea18ff4901547554394f1757ff2be3facef60a2af71163`  
		Last Modified: Tue, 18 Nov 2025 03:02:53 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5294129b5628e65891a7dd0fe5bd29ff3190e979eb91d98d77278a9614c0085`  
		Last Modified: Tue, 18 Nov 2025 03:02:53 GMT  
		Size: 90.6 KB (90617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f592a181d12cc8795e06ae7cd55f2152c4e55653b5a2f8e1d71a65305a29d9`  
		Last Modified: Tue, 18 Nov 2025 03:02:53 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:488f520ba92c5294e525ab10cdb9145c7b5c9dff6eedbad68ac5de96b13dbf35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b13ba51f807628099a34bcb151c6aa443a39e3bccfb5506b3456315ba489fb8`

```dockerfile
```

-	Layers:
	-	`sha256:a0f61787fb9b6f94344751cfb224a1243f2bf661be7453be08765c8f77bdc249`  
		Last Modified: Tue, 18 Nov 2025 05:10:11 GMT  
		Size: 3.6 MB (3611018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07484fba44c1bfedea9943a0c3add1849143bf110d7703773edeec6a8ba5769c`  
		Last Modified: Tue, 18 Nov 2025 05:10:12 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
