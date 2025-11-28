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
