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
