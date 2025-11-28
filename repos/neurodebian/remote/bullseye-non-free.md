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
