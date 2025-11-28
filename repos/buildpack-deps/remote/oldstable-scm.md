## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:d53764b18bfc089bf80ad00cb0312a7bcbd13a208d39f03070fc4bc88518fd20
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:03ee5cf8786d9feca4f6ac3d93dcd2bae6f969a1450f49330f0479417a31e12f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136906371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1080579d76debeaf7eed1e29b782f257c96bceb7e0725319297782d8e6716d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078b2eece9b24f617524f986db4dd04f977e3e7d6fe15a9088a584147bc6ba05`  
		Last Modified: Tue, 18 Nov 2025 06:38:36 GMT  
		Size: 64.4 MB (64396262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5953190726ce9ccbf3ad0b6768c474b3f48b45690b256bc2ec46f7b503bfe077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7972715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee8c1ff20eba1d80da654bae4bc7cc96d51d1e3d939b89217763b210e0fc0d8`

```dockerfile
```

-	Layers:
	-	`sha256:2de61e9b5516a0992977ac8d688a39bceda916584eee83e40c393ded3f1721d5`  
		Last Modified: Tue, 18 Nov 2025 08:20:34 GMT  
		Size: 8.0 MB (7965405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f6eb5c57f1962f2268ae871983a474e0d1704caeedbac740f146c37c46011c6`  
		Last Modified: Tue, 18 Nov 2025 08:20:35 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d5b85a1a39e7c94524218b4c6f805b50ade3daf65f05d4f83da637d54632b51b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130731950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d9766b9ca23bbd939fa20f2c5fe19a14d4a81913407ed93a7afb8990a4997b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:26:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:08:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e9ddcd7a1b6dfd5162ea10e9d236186eb8c814b710fa53b95a5a543a21573b38`  
		Last Modified: Tue, 18 Nov 2025 01:13:58 GMT  
		Size: 46.0 MB (46015831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad589659a3ab8a5efe8198e1ee9fa790fcf26937e030eba01738a074b5c099d7`  
		Last Modified: Tue, 18 Nov 2025 03:26:40 GMT  
		Size: 22.7 MB (22705754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cea8ca5112d5f4a4132c63005a6f1e78659fc63451a1196b67118980c547043`  
		Last Modified: Tue, 18 Nov 2025 05:08:52 GMT  
		Size: 62.0 MB (62010365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:85fad5cf496170577bbda2b871e40e1ee9d15f5b20a3f75b91931de8a7d8dd5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ec58dc49339a583ecb7923949f9ac2b17ab1f052d92fc795b7254da61d252d`

```dockerfile
```

-	Layers:
	-	`sha256:40b91d7642d56672840009be70c044b0ebe90e120a8e6ab8c1c6fbf9df9ec8f8`  
		Last Modified: Tue, 18 Nov 2025 05:22:24 GMT  
		Size: 8.0 MB (7967263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:582d2ce7ea7934d513ab4f3020837d1733ba009f2e43332c9dce803e26e5f09e`  
		Last Modified: Tue, 18 Nov 2025 05:22:25 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8e67b36641226285a3294711498f4635e425e4e23dfe0a15e1f1605698ff5920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125782948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09001823ecc6d3e956ab9f75853479d6a61dfa98969ef317631085cffba31b89`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b6eb0fb27a6d99b6b7a2a32ab126d30b16ebd113a3a3e174d37a032cde9bd1`  
		Last Modified: Tue, 18 Nov 2025 05:28:17 GMT  
		Size: 59.7 MB (59652137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bf19de49d85a81959243780c544b4ebad1f7330b8c14140b6e4135999a33cbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1b88ed1da31c864c30044ae22ba2d269e1a4d3113615c8d23fc025cc70a06f`

```dockerfile
```

-	Layers:
	-	`sha256:56143f92cb8e7c89c9a244a029df48080382b280b3d29af246eb365cb7b1a6dd`  
		Last Modified: Tue, 18 Nov 2025 08:20:46 GMT  
		Size: 8.0 MB (7966682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91c1c6eeca789b10fc72a62245bdb8e1e8b7b0f2b2257b3461344a15170fc7b6`  
		Last Modified: Tue, 18 Nov 2025 08:20:47 GMT  
		Size: 7.4 KB (7373 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:60c5491b5f504c9802b959bc053b92f8b00cc3773cf3e3b96071d1de1f8f5506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136328872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9594da32f43b559cc4182d237e1001b0bc07ed8bd1221ef41d3f160120c475a2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25d805ffe4d6247a3ab7494e663f6ae84d04e36c5270a200f1d1d34db32a26c`  
		Last Modified: Tue, 18 Nov 2025 05:38:35 GMT  
		Size: 64.4 MB (64371414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d38f3456897674e16e5dd4f76c775aabfdda78df3e6dbbf0a3afb02d3dcba8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7979188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35536d30e919872b14b8905b2f572b1f9f24f5a6b2beaa1c7da6e6d96d44d550`

```dockerfile
```

-	Layers:
	-	`sha256:a3e82f73958eba177c44b9a5dc758a964664d11febb5a65e2583e3972eb8e138`  
		Last Modified: Tue, 18 Nov 2025 07:25:36 GMT  
		Size: 8.0 MB (7971798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fd8854845629e842f3d16b729e56a0134079ec99340bb62e868e4ac8a839443`  
		Last Modified: Tue, 18 Nov 2025 07:25:37 GMT  
		Size: 7.4 KB (7390 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0bec8a0c5399cd78fe0d075f6571a69597878b96f7889eb6889230efa760d049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140565151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ccae0925678dc96081720fc4b69c16e306a791cf10688ebdf081facc5802a5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:56:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:08:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1ac37f50532a7306717e1be2f4760a581740981b55bfee41fb74edf971bbbb`  
		Last Modified: Tue, 18 Nov 2025 02:56:28 GMT  
		Size: 24.9 MB (24864418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931488dec4785216610c9f2c064b20b308e9839859b58a6fb0171606dd6f0514`  
		Last Modified: Tue, 18 Nov 2025 04:08:56 GMT  
		Size: 66.2 MB (66233867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c1d4df1d1c5b946999d283d480b42db7e75d52a77b0379e81c608157b16b7775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7968852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d64e7e114f237b97defa471ee24bde7d58525b23dafd9f4a613206d36339dd`

```dockerfile
```

-	Layers:
	-	`sha256:91be35fa4ed705a29d14199a07cc22776142acd19b9947a3634baecf0e459f9a`  
		Last Modified: Tue, 18 Nov 2025 05:22:42 GMT  
		Size: 8.0 MB (7961564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590ebb80918d9191c80feef9e0438f412fea25ba29e02e818a5b9abb3aeee3c8`  
		Last Modified: Tue, 18 Nov 2025 05:22:43 GMT  
		Size: 7.3 KB (7288 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:dc7da414708bb9f400864b40e99b2644e8d1b14464c3a577bdd6626f41c26959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135684290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a85a60561104e7f47d68629ca53643c8fdc21ebe32b516d2bd66ad92438dc3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 19:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:11:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6d4a3f53f449c0e9b84d889c71d1f21df5764d821465bd1337060660aa78c65e`  
		Last Modified: Tue, 18 Nov 2025 01:11:17 GMT  
		Size: 48.8 MB (48760956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754bf41c56cb3beefc6b6211c26bdc048d41c337f12bc0bbfcfa89dfb5de99b7`  
		Last Modified: Tue, 18 Nov 2025 19:40:58 GMT  
		Size: 23.6 MB (23614038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7a4cb619dbd7fcb3e0be3246f973ccbe692039c1fd01a193751c60045de0d3`  
		Last Modified: Tue, 18 Nov 2025 22:12:34 GMT  
		Size: 63.3 MB (63309296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7483e2f5aa6a5d102a7bf7aa7d3cad52a939107fcfa7499945663d0a58a2aa88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2d024e66befa5d9c67b7bcd36fb9c6a01f43287418b60ab667a5d16477f50f`

```dockerfile
```

-	Layers:
	-	`sha256:9f605995184cb2dc7aadc2355d7d34606ce9ba91f1695b36eea388afbc962b06`  
		Last Modified: Tue, 18 Nov 2025 23:20:48 GMT  
		Size: 7.1 KB (7143 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9eb34891b2fefa65a21976a7ae272d55c9cb9beb86d137197932ec7e70425ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147844603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9571b9c226e1a3f9baaa3f20d08869cd496716939186b29f2603be8b9a1f6f27`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:51:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17787af1df16ce560e48a9be892094ace19b1aecc7f06ca1e97a2e20987822a5`  
		Last Modified: Tue, 18 Nov 2025 04:05:05 GMT  
		Size: 25.7 MB (25672018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4d717b62eb888bb16cb77af768613d5d676b28f09ab1cb591a5130af4b846f`  
		Last Modified: Tue, 18 Nov 2025 06:52:50 GMT  
		Size: 69.8 MB (69845622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8e1d858b51759f09f85f81cfa230fe67b6ec38c85edd61f1dde556bd617f07aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf7c62827fc0b739b5164766d8b400ef8781841d9fa9a4d19607a0ceeb6b9c1`

```dockerfile
```

-	Layers:
	-	`sha256:efdb95afb41086eefde8eff81597ebe725e980c0f8f7cc9774031030a4f67f5a`  
		Last Modified: Tue, 18 Nov 2025 08:21:05 GMT  
		Size: 8.0 MB (7973276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b655d725526c38b58c956b0ba41b0eb8593955d128fb8680cc5a8f6a3de0434`  
		Last Modified: Tue, 18 Nov 2025 08:21:05 GMT  
		Size: 7.3 KB (7342 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:36b27b0345efca0a3faf224112971842bc888aa8e1c16623b45682be1d9fa85c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134666268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7983ba75782de998c39275f1b8b2fdc525ce295b2bc6a2509703e275a4ecefdf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:56:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f80247bcc58a5a903807561f3aad626158855a07b7817a9ed9975e9775ae2`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 24.0 MB (24027180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b099f215b279a7199da193e9e90d7e8e46ea9dfcda3ebe6c6379eb56d436eeae`  
		Last Modified: Tue, 18 Nov 2025 05:57:22 GMT  
		Size: 63.5 MB (63501447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:731b503260a52a68ff8fc60ff84e43af2315f4a7ea3113f0e049f57c96d24817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0caf03b920bc434f4e2dd0e9b73c1953ec26764148de538f7f31db573afc6dd4`

```dockerfile
```

-	Layers:
	-	`sha256:0eaf7176873b2fe9a2b8c2de2fd09e4c3e8e4612544c445e853be3d0330c629e`  
		Last Modified: Tue, 18 Nov 2025 08:21:12 GMT  
		Size: 8.0 MB (7961718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd23260b46a45272fda15fd6d4fc45103a7eba9fc6fc810ffdb972e736f96268`  
		Last Modified: Tue, 18 Nov 2025 08:21:13 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json
