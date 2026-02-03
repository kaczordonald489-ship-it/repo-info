## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:6068e82fb46d4856b52305a4cc0a0214432292feb7e5d17401448c02108c6b7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:cce5589b09b1167c73d487b5e6fbb3f0ece8741cb35857691a14e15730927412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124282412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c50a218baf57be073d9b36a44577f1c1b4b01c9ec7feac58995fb1499428f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:42:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee799e8390add15bd75ca0b567540a98a55aa9abc40d4c0985dca18f87c25044`  
		Last Modified: Tue, 03 Feb 2026 02:42:11 GMT  
		Size: 15.8 MB (15765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fdfb3ae60fd4b8638b772eb2ef287a4577644db16ea91d523e4c096965618c`  
		Last Modified: Tue, 03 Feb 2026 03:28:38 GMT  
		Size: 54.8 MB (54760555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b69ee5eeea114f6bb4194b3304271465f4e0d393e6214c8ce724ef04cc734d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7920273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5290318bbdd5e99c80c4dc93c837f3c03ed3204f41db1af41e93087a5a1fc569`

```dockerfile
```

-	Layers:
	-	`sha256:020c31b9de1d71d33f3d5543b51d620ea3bacfcc65a1b029d69e4b2ae98c4af7`  
		Last Modified: Tue, 03 Feb 2026 03:28:37 GMT  
		Size: 7.9 MB (7912957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b7e2058c58554cdc5187e10e41962629cbdfeb194c903b7be95afdd49527aac`  
		Last Modified: Tue, 03 Feb 2026 03:28:36 GMT  
		Size: 7.3 KB (7316 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3979699071c886082df2cc9185e88e8cb80ba661d0256529fbf8be9b41518b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114569229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33b958b59cdbc27794af9d375c9619997d7fd4ef3851045d7c74d5504b73098`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:30:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:59:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6ca5f53d580fbc72887807a74d2d1c2f8900fc3f535a8082d3df4fc3f9e84caa`  
		Last Modified: Tue, 03 Feb 2026 01:13:42 GMT  
		Size: 49.0 MB (49047418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b496e431ca97183650bec266004dde0fc1c85e5f1c690d4146afd2ea94035dc`  
		Last Modified: Tue, 03 Feb 2026 03:30:31 GMT  
		Size: 14.9 MB (14881625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466cdd399272acbb9a1e85ac72634d24be95fda0a3f55eab1a8ce1da5fc02bb0`  
		Last Modified: Tue, 03 Feb 2026 05:00:10 GMT  
		Size: 50.6 MB (50640186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ac3e4acd70bbd497015dd2a288dcf4f54314c4ddcdbe8b941dbfc2d5594c0fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7921739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9429574f7c3f161ebdafc0c036954ab8c7843e458cb72d30cd0de7bab6eab987`

```dockerfile
```

-	Layers:
	-	`sha256:2f245520310ce0d3681976695ae1957c86e2441b869e1b14d89f9621c0827f3a`  
		Last Modified: Tue, 03 Feb 2026 05:00:09 GMT  
		Size: 7.9 MB (7914359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07ac1f5b8750034c27afafea25f6ac7940ccb8e5403217649fce2f76684fe94a`  
		Last Modified: Tue, 03 Feb 2026 05:00:08 GMT  
		Size: 7.4 KB (7380 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:545286747d651d7da57ca2bb18cdbbd3b9bc7db77c323b9e2e749b002be5dc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122884976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0de1467cc3215ddf046a8069079f8ed46976241d2ce492337fbfbfc5ca696d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:45:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8786fbba60dc8d61eaf8fb6b0cf5291a807641e61a5c761e1cba765ef879da43`  
		Last Modified: Tue, 03 Feb 2026 02:45:17 GMT  
		Size: 15.8 MB (15751646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d1a0324220213f9a9398a3adcfcebda6418d2bd83212c762c2bb386f570200`  
		Last Modified: Tue, 03 Feb 2026 03:46:49 GMT  
		Size: 54.9 MB (54875010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7920de3e6268dc904f7520a935810af7357780c7096fb856d11b8fd4f6302d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7926086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6661676479b856910da5622ca6bff61cf2e97739bd68a1b9a5076ed57e9d14e`

```dockerfile
```

-	Layers:
	-	`sha256:345ae28e21e718d6da79cea0013017ce7c77db0aa41c979a5000629ff9667aff`  
		Last Modified: Tue, 03 Feb 2026 03:46:48 GMT  
		Size: 7.9 MB (7918691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88ca8a47256f720bc13c3d029c52140d1ce766488de34ed32b3b044c3f8704e7`  
		Last Modified: Tue, 03 Feb 2026 03:46:47 GMT  
		Size: 7.4 KB (7395 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2b9bbff10006e378dbc6b03efd68ec30f8b6eda2aaccf785155f0d5be4cfa9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127028944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b06ae693e3c24b37d288961aec19f7619edaca17b0dabdb47e400a9d02a89c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:49:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f6d70808fcfec5fc2c45e150a669aa79950bfd30968e7ba0de2c962cff56fc33`  
		Last Modified: Tue, 03 Feb 2026 01:13:58 GMT  
		Size: 54.7 MB (54699582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83b8227b1b97d84c4a7d4b36dd8fcd700f5f0189b543ddd06f7510ecfd20ed9`  
		Last Modified: Tue, 03 Feb 2026 02:49:37 GMT  
		Size: 16.3 MB (16270742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d99aacaea33162882dda20c6dbc4d93f0c42dec71017c78e00c9f875c6c97fe`  
		Last Modified: Tue, 03 Feb 2026 03:25:04 GMT  
		Size: 56.1 MB (56058620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fb266e11bd3303df8aee54c2d533b889d120132c8ccf8c3e528769848398912c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718dac97cded0e0870f009402fcfe64dae21c8333c030b20317609de6e6d8e62`

```dockerfile
```

-	Layers:
	-	`sha256:ff652572f02de10505655a807aea718080649713e65f22bfb4cbc99708e4589f`  
		Last Modified: Tue, 03 Feb 2026 03:25:03 GMT  
		Size: 7.9 MB (7908527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1efd1d8b568d879a47f1e4b28e54a90be3a2e0bc105fd11e639e362e8eccc4b`  
		Last Modified: Tue, 03 Feb 2026 03:25:03 GMT  
		Size: 7.3 KB (7294 bytes)  
		MIME: application/vnd.in-toto+json
