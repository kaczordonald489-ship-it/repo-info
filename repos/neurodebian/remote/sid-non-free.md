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
