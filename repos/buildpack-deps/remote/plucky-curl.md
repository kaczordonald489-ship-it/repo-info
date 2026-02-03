## `buildpack-deps:plucky-curl`

```console
$ docker pull buildpack-deps@sha256:b749c50cb711edc99e6f242ddcb1711cc0c9e0cf798225dd4f0c0e4db750733a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:plucky-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d0f9e03fe92420c3af5b3de17a164a70a1b66879784676022494751097f7da4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49874311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96633f13b60006c67962e9c2768a12d176870de7020655e791ae27467f48b39f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:5c208fb70b021afc05727d8dc78f4c389e873e38646fc0f247ced1cb261ea370 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c62190a9ab61c5fadad5c83c08965df006562241538b21f41b5efd457dc50ccf`  
		Last Modified: Thu, 02 Oct 2025 22:51:56 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a062b23ec8858a53111c768e7f787cd61bb54984335f5fbd174eb0ec8367a6c1`  
		Last Modified: Thu, 09 Oct 2025 21:08:40 GMT  
		Size: 20.2 MB (20160344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4be05df4b47cc03c8f822dd5ec7b0f090703ec6b04a05df8fb3b19a517ff3689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2620470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7a64ab937eb3881457448031d873f1fea8cd8e7e32adb75a8e6b001451a708`

```dockerfile
```

-	Layers:
	-	`sha256:2119aefbee8f08fc00532b4c38f3f8ebfc1f918bbc4bfedbaad91aa0e0ab7e16`  
		Last Modified: Thu, 09 Oct 2025 21:08:39 GMT  
		Size: 2.6 MB (2613502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8291a82081fefeb6c26f4e644a93e7a22047b3bab2ef26347df5e6f4223491c`  
		Last Modified: Thu, 09 Oct 2025 21:08:39 GMT  
		Size: 7.0 KB (6968 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b4d684f694ba957ece63cc66937521f08505ce6491518db4dba7846d4f4a5173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44716685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1562aa8e7453c3d3defdfbf53bb3df06dd3dc0fbcf958c15396d42e0449a1aa8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:23587a53a3b8c233c6c6d049a58953577ccd768017b9bd6dde46eb195682e51e in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a560adc1db1b1576c34098b508ac1924a3ade1dfef0c1b3bf40e1e69968ecb16`  
		Last Modified: Thu, 02 Oct 2025 22:52:10 GMT  
		Size: 26.8 MB (26843779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437e3a045a9c9b782981e6941004f53d1cfc09bba43c98055dae478ea41bcc73`  
		Last Modified: Thu, 09 Oct 2025 21:08:20 GMT  
		Size: 17.9 MB (17872906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:591c0f066cfa18654924a23afa939768cf9dabde89b29bcd40ef84afd8f72fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2622033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499382210384a397771669c1baeae1aea2d2e1400a9caac2cd9361b94651224c`

```dockerfile
```

-	Layers:
	-	`sha256:04ed6ac4e1db695a503fae76b2d24a594a3aebe3d8ce909cb27270a126377cc8`  
		Last Modified: Thu, 09 Oct 2025 21:08:20 GMT  
		Size: 2.6 MB (2615001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e61f79d8dd8d65b05b77620078ecd38c1f56f52957200005715ec8863abc487d`  
		Last Modified: Thu, 09 Oct 2025 21:08:19 GMT  
		Size: 7.0 KB (7032 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2c5c65353a260afff1ee51f475a94cf9b5aefabce0eb31e17165c165a9ed840e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47465975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b415cf84e12c9cb30dcd134a6cc9b4c69249b1b1f2d358abafa3e67f5aabca13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:2e32d5ba6a5a96833b0deaf9c5a7ed2559bab3a9addcff92dfe49254b9cc654e in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:49236737bff0862bb8b036b6c3ef5438b02eff6a137b08f62499d2764ac53431`  
		Last Modified: Thu, 02 Oct 2025 22:52:03 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8befe8fdedddbff193b11ae8f04e5a14b70ab1514f6fa46618c72214a7b98df`  
		Last Modified: Thu, 09 Oct 2025 21:09:00 GMT  
		Size: 19.2 MB (19161632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9214906bc449646fc7ae4c2320562c5ce246c5365e9a120d452ccf85f05421b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2620807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf90477875eaffad10b2aad0b2d5b6e1d87038a00cce7529f9c32d3de480b12`

```dockerfile
```

-	Layers:
	-	`sha256:20f3857dd690b5d74738e9b715d0f2bde11a99afc3b7ac4f9c6e4b4d84e3ed63`  
		Last Modified: Thu, 09 Oct 2025 21:09:00 GMT  
		Size: 2.6 MB (2613759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e047d0dd6edb0e7ef726a3bc6ed5e44be441262bce44f07920d066aa526c4e24`  
		Last Modified: Thu, 09 Oct 2025 21:09:00 GMT  
		Size: 7.0 KB (7048 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ca8d2c92c8a346cd130d3d1f9850f43a72631b54dc02cda603ce171f8580b78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54520744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b03ab66ee0570ac0cf257854261573bc7473babade4c7c2538380ad01594282`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:eed18173e7a58a8f50e221308ff988730c708eca6728853b97742a4e6c432e56 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bb02a506ecb8532d4a8daeeb06813a7d29448655a56217ebf03cf71cacbfe138`  
		Last Modified: Thu, 02 Oct 2025 22:52:17 GMT  
		Size: 32.9 MB (32932707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069c89e19954901deddf06c2e5b6786e4c73fcd985d5658323be5514c148691f`  
		Last Modified: Thu, 09 Oct 2025 21:10:17 GMT  
		Size: 21.6 MB (21588037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5527e78a2d087d4cf75254f32b2a6fb7503cf45fd2f8c8bf0e962335a781156c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0455c539351cfaaf09ec25edcd0779e9d82ff3858afe5cd441014b67a826a9af`

```dockerfile
```

-	Layers:
	-	`sha256:0156c6db525b1b0ab78074968cf7b79b93e7598347fd1850fe08f358723896ca`  
		Last Modified: Thu, 09 Oct 2025 21:10:17 GMT  
		Size: 2.6 MB (2617320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c40bf6e9f9b1cc6ab2c6ed6010b54e38d2f3e217579bd1bdda7f4ed5ce8b7d`  
		Last Modified: Thu, 09 Oct 2025 21:10:16 GMT  
		Size: 7.0 KB (7000 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1011c452ee5a118e6d08fd65a2315c70f1c7c1e70f886c5bce0a73e1dbadbe71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49635107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76078df0cc10c301fc85c5549729db588813436207102f28b48e3912bb26706a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:58092ebd584852dfbd74f54a32f18a0a1d76ec69dcf03f284b5591901e00d4d6 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:49011545d13c540c9969f6f8188a6275d00825a8a3bd835bca525a83b0190a96`  
		Last Modified: Thu, 02 Oct 2025 22:52:24 GMT  
		Size: 29.7 MB (29738610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1fd41446f14dd53bdf43ee08ba6f4762e82b592d6fa7d346025964dbb17f1b`  
		Last Modified: Wed, 15 Oct 2025 03:35:33 GMT  
		Size: 19.9 MB (19896497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f7807218e58f389f01984ff57b432ad7c5723b88a88d70ff33e673b0a7055f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2613614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb19d33772684494b0985d68574e721f921f80896fffa6877f221eab140df1b`

```dockerfile
```

-	Layers:
	-	`sha256:28cc0e25796defdd4f7276ff1616028f2766c115a01f596076915078d8f32a83`  
		Last Modified: Wed, 15 Oct 2025 03:35:30 GMT  
		Size: 2.6 MB (2606614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59d6ee4db8061068c49355a2e969c565bb079889ea9b1be050c7965d69e2fd1b`  
		Last Modified: Wed, 15 Oct 2025 03:35:30 GMT  
		Size: 7.0 KB (7000 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7cfa3ade512bc7e332a16532db91d6fdd4df76f297d5ff2977d1648f740ee765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50133161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87f55ab87c8fefd27c5cacb14a43e0b958c4a811427099f5583dde0da22b7d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:3b0212a0e3a24e51ccb01a786936dbe714e67c8890ceb967dcc0575b9f223f69 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3841830b71e6b25c9651fbbade2595b141b4c380906e9cb5662bf660693c0670`  
		Last Modified: Thu, 02 Oct 2025 22:52:31 GMT  
		Size: 28.6 MB (28572062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60eec4ec0aa334a990ed13cbef996fcaa931bafe5e86ae5712052d312cae64c`  
		Last Modified: Thu, 09 Oct 2025 21:09:28 GMT  
		Size: 21.6 MB (21561099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b3891d2b387a22893e437db6fde9b737cedad56e8660351f55113b033b12c28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2622498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ab6b6f66d048f070a86474eda147d4053516523f310f8301377e744c40fc29`

```dockerfile
```

-	Layers:
	-	`sha256:3c1e46c1a9f84d4879bd6469b3dfafabcd6699d97ed87012b9540524550f4efe`  
		Last Modified: Thu, 09 Oct 2025 21:09:27 GMT  
		Size: 2.6 MB (2615530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8198e730e00786d53c223ec1a5e6bab6fda33e0f952f4808368d4307b27f9e`  
		Last Modified: Thu, 09 Oct 2025 21:09:27 GMT  
		Size: 7.0 KB (6968 bytes)  
		MIME: application/vnd.in-toto+json
