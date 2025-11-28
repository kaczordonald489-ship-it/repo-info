## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:0f2dc351b81e90242e8e30bd6aa070f74ddc4e142450ece3497809dceb64d4a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a4e97fbb201fc1b7394641ffcac790a1d43ecce17c19e47b81d3f55f0673c217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74903405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad760374f57b217a6af4978768eb2f938bc7d9b395dc286f15d459a2eb3a49dc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae668646f447b181fe300ae6756351b6167aa2578be449b167ba79ed4926798`  
		Last Modified: Tue, 18 Nov 2025 05:11:30 GMT  
		Size: 25.6 MB (25613858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f9b522bbeeb25203f59d27fa3ce59335236bbf5660c243b39e5b6204e0c431aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b764d221cfccfc95c1b69f636749bb6e8e15848842f4768db6449b4d42a5a23`

```dockerfile
```

-	Layers:
	-	`sha256:cf92f074ec805350f68e3d89901c20d8884307842bb2fbe95384e3c125335a64`  
		Last Modified: Tue, 18 Nov 2025 08:20:55 GMT  
		Size: 4.1 MB (4118874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ca9ab3de9bf9daba5d0215194d6bd071e85e74bf728c37e27b535d60d4f5646`  
		Last Modified: Tue, 18 Nov 2025 08:20:56 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0b538700f5abd3d25095cd34c08db213922eb9124b05bf4eca54b8edbd7650b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71794575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad95ba957016a7996e39c7d8a58dc5ac1dccebe81426b03a43367fc65151270`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d5c9e476f1b8d1f67ce6ab99ac45c57bfe3b7cbada7b61c1dbd969f0656bfff9`  
		Last Modified: Tue, 18 Nov 2025 01:14:11 GMT  
		Size: 47.4 MB (47448757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a9b3c9a263aa4b01f8e95a9864f401b11f5c835e6ef84b9a950304c2fcaf86`  
		Last Modified: Tue, 18 Nov 2025 03:26:45 GMT  
		Size: 24.3 MB (24345818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:446dd81211ca4623b1185e7947947790a01680a09c71fb301b014c9fb26d98d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cfb9e517a0eb4160acf2531b882583277e6f51c4a969426f3674a63363d369`

```dockerfile
```

-	Layers:
	-	`sha256:2a1bb9fc627714a9bbd1f0857b933fed7db42dee539d9a3f2774f955a22f8150`  
		Last Modified: Tue, 18 Nov 2025 05:22:51 GMT  
		Size: 4.1 MB (4121864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1d040fba046e9bb451ccb52c7959a52c76ae6ee6f0d1fecebfa485cf57a8879`  
		Last Modified: Tue, 18 Nov 2025 05:22:52 GMT  
		Size: 7.2 KB (7157 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fcd059fd19e1082ae347ab773f2cf2323268404c55c431e32ed80bc3529d5ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69338279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c23c2b89bded0f73f43eee75e060c9b610575319ece4e0ec2738c990b4a5f23`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7fcec123a6a2e24d64f8dd8d3ff01f16ba0839656e71d971698d0e8151a28a21`  
		Last Modified: Tue, 18 Nov 2025 01:14:26 GMT  
		Size: 45.7 MB (45718279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebfeb92d3792e2087594f2ee9ee695fe97cc51ccaf846f755d71e0b58f7f78c`  
		Last Modified: Tue, 18 Nov 2025 04:00:39 GMT  
		Size: 23.6 MB (23620000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ccfd4a80df7c77f1582add95f5fc6142dbc2245de025ecdaed8684c1f4209d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359199011c0db54d9046a20b726756a58bf4ce281c86a2990177a54cde9e1398`

```dockerfile
```

-	Layers:
	-	`sha256:6ee95b539b3bac9ab24c20bb3b5aa9e3fa4f07f4bcd9e8c895cd469b30d5b71f`  
		Last Modified: Tue, 18 Nov 2025 05:22:56 GMT  
		Size: 4.1 MB (4120375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:115d8dcda89a1768ba951150ffccff3fcd27e642bc680e273fdb30e650ab48f5`  
		Last Modified: Tue, 18 Nov 2025 05:22:57 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ef4e852e8a75412c2b74f2d8bf0741e060d4df4f7ad01ec38cf5b6356075c964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74671243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab3098a915dcd740d1b1d7bda23729db75aea22e0a692024ca5dfb51012102a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14656e63ca309d8cfd09d01a9dbb3d1ea2d59a5efe7d40b9716f822e821385ab`  
		Last Modified: Tue, 18 Nov 2025 03:27:58 GMT  
		Size: 25.0 MB (25021011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6f75b5a7397cbc72d73feb2ee3c39e0a157bc70ce1a6ab7de567bee09378a2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee3b73ac06660553a92757cf3c8213f8fab09cee1e479c1d84c92c0da374161`

```dockerfile
```

-	Layers:
	-	`sha256:b5a8de475dbeda4258c6104cb7d3c831f1bc0a3a4b2aa71dacaf118a54602e09`  
		Last Modified: Tue, 18 Nov 2025 05:23:02 GMT  
		Size: 4.1 MB (4120416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f72e432312f2a83ee144fc11f010f38f4a0edecb933a40446c8f8c71f6f14e4c`  
		Last Modified: Tue, 18 Nov 2025 05:23:03 GMT  
		Size: 7.2 KB (7178 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:74347c4222ac71c19238202dfe539cae7f5ef6ae25e02abb972c9eded16aecf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77578159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06868e416cbb0dfbda36f6444fe0abf33211c1db7d996f7cc5547dff0b5cf7d5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bf2a49c122745d1757b9ecb1c9b1d8252491e66b62d1c279080155aaa530a615`  
		Last Modified: Tue, 18 Nov 2025 01:13:10 GMT  
		Size: 50.8 MB (50801744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cfb736286179e6858e8b04a47a815f4071567b3b6f8b36ca52b15e872e6cea`  
		Last Modified: Tue, 18 Nov 2025 02:57:24 GMT  
		Size: 26.8 MB (26776415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5696d4713749381d87bc454f9b676e6e72b58d57b4adf083812d4abd63517625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c523d8e09f463d7b8bfda755da1cc8bcb0bc98f0dd01540eae1cdf772c811fa`

```dockerfile
```

-	Layers:
	-	`sha256:3c50752d13ffc77b94f62977d5de99888846203ad804fc73db48426b8a49dfee`  
		Last Modified: Tue, 18 Nov 2025 05:23:07 GMT  
		Size: 4.1 MB (4115982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9ae0c63454f89bb2eeecfadc345504cb1a07aa6cd5cf35ed7ee3d21183c35a`  
		Last Modified: Tue, 18 Nov 2025 05:23:08 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5fb7f5fd225c9d8f07a146607bc2ac7da2c1c368b9e0b8914719ac73fe3a0909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80105404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8395076bf92316e001f36a11cb5cf4bb2c0f7f68c57f1a98fb8df9c4c5363df8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a859b52534a1e3522c593c1835bd1bee34ff20a865f32f140257d45048a18099`  
		Last Modified: Tue, 18 Nov 2025 04:09:23 GMT  
		Size: 27.0 MB (26996919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9f637a5b712730427b11b1628c4aab17d2420d806e94316e3c2469a704c23d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b475d682615671e9596865f92393d55417d822f4f2b8d143b0d6fd82a1599a`

```dockerfile
```

-	Layers:
	-	`sha256:2eef732e933badb6e0b06d17048259aaffb52dfa443d6f663d6ac913fff6aff8`  
		Last Modified: Tue, 18 Nov 2025 05:23:12 GMT  
		Size: 4.1 MB (4122720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31dc1b5ff9f2b86a95f4dfb322966a1fcc95fdfa86b77fe47aaf7bdace71e9c4`  
		Last Modified: Tue, 18 Nov 2025 05:23:13 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cd7a4e5aeb16008379b366317cf1baba2212ad8b69b15d194334feb8b2d497c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72724931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f821c61a96b7386c3040b129bc60a5d7e86bcbbe4492624cb671c0f068096206`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccc0dcc6b4231d5f1f223a1330c6630cb9406136f8e738cb2b0e628d1b35022`  
		Last Modified: Wed, 19 Nov 2025 19:38:34 GMT  
		Size: 25.0 MB (24953736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f4079fc7a57f4d7da24e96e5b337327b8a1975a77e47924a4d84949cddcfe540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4118508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a9464f285046c1fdabda8e395e1e886e4d9e5b7b0436a09adc865255b2dbad`

```dockerfile
```

-	Layers:
	-	`sha256:1dcbbbdbfca769deead1708261cd9434d4f59db239b2e6a3672eb933379e0616`  
		Last Modified: Wed, 19 Nov 2025 20:20:09 GMT  
		Size: 4.1 MB (4111384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b922f94583c64f3ae64155092d59c62307ca77db0d9bac7c75c6d37f4a74f9ed`  
		Last Modified: Wed, 19 Nov 2025 20:20:10 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:66a2ebfea794afa35b7a56261705bbbb8e8dffcc589480d131f42f80e5f82aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76132553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdde0e6842c8fbd41b5e8566d15c109e7c95f67b6104a48bc3810dd4725eea63`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f811fd500c593f696ff4afefd96c823d7f8788d50f510057207bfc40b4a405ca`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 26.8 MB (26786539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5891845b30954d4ea7bf6c1f7b640a3efcb0b5fe73f0963242554c8eec75442d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd649d6b29e748b2a267dec1f850bf95d940fb6535701818aa9f483a7b5ccad1`

```dockerfile
```

-	Layers:
	-	`sha256:8c31915791a71dbe20c90f82110385ca77290653e5102f3b36ebf25df13962ca`  
		Last Modified: Tue, 18 Nov 2025 05:23:21 GMT  
		Size: 4.1 MB (4120284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3afadfbf106a42ae481149a996c26ced8102764f5449fc8fb7398e0301638ef`  
		Last Modified: Tue, 18 Nov 2025 05:23:21 GMT  
		Size: 7.1 KB (7085 bytes)  
		MIME: application/vnd.in-toto+json
