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
