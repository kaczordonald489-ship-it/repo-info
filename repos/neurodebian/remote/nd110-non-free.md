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
