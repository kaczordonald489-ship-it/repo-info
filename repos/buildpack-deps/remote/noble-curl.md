## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:66a7e91430822053b212291adcb37633707bf47ac2237ee3af70e68555978289
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

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9f5998e7392165c49348a1d0abde647adfd0a878c8e7a35a4917dcd0be175689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43351493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26645e611b5117f4bbdc24e8ad48d1ec1414be79468a955c74eabe0e82e145a`
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
# Thu, 15 Jan 2026 22:10:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d24600144cacfa54a1db917d1d7d6ed28315e6561b4c63104291a19482b851e`  
		Last Modified: Thu, 15 Jan 2026 22:10:49 GMT  
		Size: 13.6 MB (13625482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b1d6d894f34f86d44f48bcbedd393ca2b596892324ae934feca458d91308559b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60898e1bfbdf411d731d92de1d593496b74847b72730d681792b70636feedfdf`

```dockerfile
```

-	Layers:
	-	`sha256:57ee5fe272bdbe19846c01fce52c7bf82bafcef8a62762213c6433c80733c1b5`  
		Last Modified: Thu, 15 Jan 2026 22:10:49 GMT  
		Size: 2.6 MB (2607813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a4f1f09d054fb363394336848f17f4fcc38059c00957f23cc6ae1842f171a4c`  
		Last Modified: Thu, 15 Jan 2026 22:10:48 GMT  
		Size: 6.9 KB (6916 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f02dbc80070130308cce4d07b8564cf34333c4dbda2fe53b0ae2626f09a8e830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39638623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdc9c714915344990938afb33277596efed9f28a108bb286cc3c449e1a65a7d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:59 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:02 GMT
ADD file:9e6534a5b837dcbcc4b9596878a4feeb07210fb34c7385aeee0217ff03c2460e in / 
# Tue, 13 Jan 2026 05:40:03 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:06:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a56277e49d30e9a430d5cefad3038f88470a8681e48b806fff292791ed54f1fc`  
		Last Modified: Tue, 13 Jan 2026 06:35:51 GMT  
		Size: 26.9 MB (26853837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d01dcaabd8c1049b7b623de5cebb3e36f9ea25b3413b45c8d04138182a76cbf`  
		Last Modified: Thu, 15 Jan 2026 22:07:03 GMT  
		Size: 12.8 MB (12784786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a142296a5a8f713c5992fe8c9cf47758aa3d1cb6f3115d36c4991854e8d41c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa3882d007301bb2d43965de8a56850c41947d4bd86cac7160ed8cfa8aa930a`

```dockerfile
```

-	Layers:
	-	`sha256:544580ad4cb5824485d86378f01fc96683fc9e907ae3cd080a80c4699f3a8b1c`  
		Last Modified: Thu, 15 Jan 2026 22:07:03 GMT  
		Size: 2.6 MB (2610117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a0a27db9649899ab7c44e0d6ae7c5ba0fdb88c27702a44aed5ee7ee16d2def4`  
		Last Modified: Thu, 15 Jan 2026 22:07:02 GMT  
		Size: 7.0 KB (6980 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ea200a48a717927b83ef2850026ee8ff6b4782e933ec02fb7878bf721069703c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42324028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa7f6729150396a5a97805dfb9aa4832821b7a72fe39ac70c22e4eea8b7f649`
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
# Thu, 15 Jan 2026 22:10:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba4d2c3c95189803c083cd23835a29467c160f5e38bf036d9d758cd45ea187f`  
		Last Modified: Thu, 15 Jan 2026 22:10:40 GMT  
		Size: 13.5 MB (13460204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fc002bb81b8b87cadf5e9fad16260f4e5b6bc109f047b3082ba85accb2fd74e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577d3bd1ec51985e4c0abab3f838411745cffe9c8f5b274d2cd0f8b407486e41`

```dockerfile
```

-	Layers:
	-	`sha256:1ccb3fc31b557f97f55f235d0b24c4373a16030bd5c02598936d7a5b696a876f`  
		Last Modified: Thu, 15 Jan 2026 22:10:40 GMT  
		Size: 2.6 MB (2608871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd8d631b0f1cb4b362a3bfd5e9f71341b8c9cf484a61fb9ef5324daeabfe2af`  
		Last Modified: Thu, 15 Jan 2026 22:10:40 GMT  
		Size: 7.0 KB (6996 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:01b0fb9ee61bbca244beb66d72aff74da3277eb314f07f3189f7789fc524a22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50260090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f1e39b8c9872ae80082764b4db4e2f63f40c76d3610afd41ecab6b9abbb7d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be50b69a5b2999820c4fd9871118355d2b55c7889ea84216402be50a2125226`  
		Last Modified: Thu, 15 Jan 2026 22:07:38 GMT  
		Size: 16.0 MB (15953931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fcbda51c70b013c1ef3fd977da149ac883f3e5aee6253f390fc7fd653ce00a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2619378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80359d0721257ff45388dd393cf77ff878d82eaa50fb134d517efd7f5a5c4042`

```dockerfile
```

-	Layers:
	-	`sha256:9e58d3831d30bd21c3eda164428e267d2cdcbb3d0616be664e2c7c02461e5d63`  
		Last Modified: Thu, 15 Jan 2026 22:07:37 GMT  
		Size: 2.6 MB (2612432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c2281eeb115949496bae7cd8ae8ba29ada10ca1bc6c0ff4eda33df874aa5181`  
		Last Modified: Thu, 15 Jan 2026 22:07:37 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:622189e65b8226a7cce14effe21235f1b90cd71b9af3f39687d65c8ff4f8c0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45284029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856935f362a00060d2065d74fae1978d947325d630b03f08a1dfbbe4acf85608`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 06:14:56 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:14:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:14:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:14:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:15:46 GMT
ADD file:8d0655de001e92042901c645c76202ac355acb6fa186561e7344a0829ffd983d in / 
# Tue, 13 Jan 2026 06:15:51 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 18:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f151392858868452ec0f1f8d2947624e8dcdecf23bce587cfbd7c38a3264f9df`  
		Last Modified: Tue, 13 Jan 2026 06:36:06 GMT  
		Size: 31.0 MB (30953090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aa37a63720515321479a1b97dc2892cdbe1fe7821a8e0975eaba80f062c279`  
		Last Modified: Mon, 19 Jan 2026 18:06:28 GMT  
		Size: 14.3 MB (14330939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f30af61ed387fce0b74a1be324e3e577b09d0d39a371c3639ec02745aff10220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2608660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2dd0e5ab58d40e2bb2210eb8d0fab219899349271cbebdad1a7ec074fb6961`

```dockerfile
```

-	Layers:
	-	`sha256:83680a693c0f5b24adc901bfac6e5992fe299fd2eaf4ad4daf8dcd946fe7c021`  
		Last Modified: Mon, 19 Jan 2026 18:06:26 GMT  
		Size: 2.6 MB (2601712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66b3739ec0155b44321c757478c6648e07bb800ab380f9c171af0583c5738cc0`  
		Last Modified: Mon, 19 Jan 2026 18:06:26 GMT  
		Size: 6.9 KB (6948 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:adf17c1ac5f52688518d55f8e42fdcd3532bd2926a86a6fe6e4d9712d958482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44847190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5fa15f5539b61a6962416739f2f60de61bcc6470cfbb306a5b05ca4b72ca3c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 06:29:20 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:29:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:29:22 GMT
ADD file:55a7874afa0094b7b4c6edc68b58164a34177fa761bc6e673ddb0c846b91f26f in / 
# Tue, 13 Jan 2026 06:29:22 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:06:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:88318e41cf944fd93c8b2fdfaeb1378b17ed0e2440ef9811f9820449bf19a6ad`  
		Last Modified: Tue, 13 Jan 2026 06:36:13 GMT  
		Size: 29.9 MB (29909204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08e8ae4a562592bab8bf88b1b4e4fe3d6b21c46eca4884a5623f97e569f1946`  
		Last Modified: Thu, 15 Jan 2026 22:06:34 GMT  
		Size: 14.9 MB (14937986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1efecd3baa366cd274d9f8aa28bc7788813afca2b1787c1986e6328aa0c79610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb1e96625a8f1e81d29524b4f5625c005343d39c8d6cdf5bdb31cd3acdde308`

```dockerfile
```

-	Layers:
	-	`sha256:8131c2c9310d055a71c6de514df099a59b25bc0cac763f85d13a1574d68f4ef4`  
		Last Modified: Thu, 15 Jan 2026 22:06:34 GMT  
		Size: 2.6 MB (2610638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:126624e8aa710028d53bf7d1e4218ad630fdc4013e03a9487479e304dd94fcdd`  
		Last Modified: Thu, 15 Jan 2026 22:06:34 GMT  
		Size: 6.9 KB (6916 bytes)  
		MIME: application/vnd.in-toto+json
