## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:005fb96d6eb14346e4c129e2ec503835f0ee597e4fd9e67f3b559f30a086cccf
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

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:40d21e6efe43ede73d13b192c06d91c9e901a71e2d260270b486a3f232ad39e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136915900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde165be2a8010f40b579896f04700fbbb7ed26f6cf5ed2e32cff02e4fafd2f1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbceb003542957cee7df7b79249eaf0a71d21c5203d086969b565fb6dec85d86`  
		Last Modified: Tue, 03 Feb 2026 03:28:33 GMT  
		Size: 64.4 MB (64395971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f19a8045e142b4921a1bc7d081cbfa32fca517e6690f2e628871cd76b86d0e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7973357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856deee9009f84fa45605948efcaa6a499458813d0d6deed5f9bfcc9b47212c8`

```dockerfile
```

-	Layers:
	-	`sha256:0e1951049224fe015f22b7eaf61f16501a18b2b88cf101c1e49898a23d470852`  
		Last Modified: Tue, 03 Feb 2026 03:28:31 GMT  
		Size: 8.0 MB (7966048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:559d12c60308b827929064b993a644b9b762e8acbc8f2a998f7b066b54e47f61`  
		Last Modified: Tue, 03 Feb 2026 03:28:31 GMT  
		Size: 7.3 KB (7309 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1e77683fd6494b50e1ad1899b060d649c71422f68d6f0a7564486c3bdce6c642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130739375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c57ccb190748ef26d32c983a8909f70764eb425e13eb35e2304ccf83904d87`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:17:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:48989bca0bd1f08c49cfd2a8eae58c5ffcacc0f005e701953d88f28a5e398ee1`  
		Last Modified: Tue, 03 Feb 2026 01:13:21 GMT  
		Size: 46.0 MB (46016664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8c031851c0852eda9cc103afa92ccd1ccefa07dd936a71f291d45de349d70b`  
		Last Modified: Tue, 03 Feb 2026 03:26:08 GMT  
		Size: 22.7 MB (22713907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2787358314b0b690e6368b20e1faf8551e6eaee19cdf0cf05d8e0a7e3fd0707`  
		Last Modified: Tue, 03 Feb 2026 05:17:27 GMT  
		Size: 62.0 MB (62008804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:071c718d4cc4f92cd5ffe292cf7b3d6ba99bba526e88aca7ed68d925f03a92c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f52043c605ee639e66f92e29ebccb6b62ce8a52c6463a8247b8883b5e80401`

```dockerfile
```

-	Layers:
	-	`sha256:8bbf21d96e702aaa79cbbd07e750bd80c2ac8a36458129d580527992b35ddf39`  
		Last Modified: Tue, 03 Feb 2026 05:17:26 GMT  
		Size: 8.0 MB (7967906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a61e724931bf00c300195508df2bc5471d323dcdf3c199092220de9f6caca3c`  
		Last Modified: Tue, 03 Feb 2026 05:17:25 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e6fae156bcb3c0274277d65b3d4df820ee140f4a029ac5869e040f1c6dac3f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125792740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e57ecbbfb94918fc1febb684b447b2afe6bedee2595aea7a8f7690090d17c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:424cab4c9a6a41cd57ee6de8e95726c4d76fe3e913bd9c7731865fd244771971`  
		Last Modified: Tue, 03 Feb 2026 01:13:26 GMT  
		Size: 44.2 MB (44198733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7fc27aeb6b79b5764735a819c5fdf5feb13c904bdffa0dee2b4c1c5f3935e7`  
		Last Modified: Tue, 03 Feb 2026 03:30:05 GMT  
		Size: 21.9 MB (21942045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb0551578bad740c3a20b6a29166ce3ad8980e037c23d30c90a060f62da5338`  
		Last Modified: Tue, 03 Feb 2026 05:00:10 GMT  
		Size: 59.7 MB (59651962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bc85f3c50fed0bdb934cfb613c0b9993dc7d11efbc5fa0e6603e774332fda614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261ada7f281d60463b0990b2a4fe7ee887ffc87506964b509fc1d096907f0e34`

```dockerfile
```

-	Layers:
	-	`sha256:5cb9f823d3f3f20006368806335bdbe2bd946dc062250e283d810bd5e991f4b6`  
		Last Modified: Tue, 03 Feb 2026 05:00:08 GMT  
		Size: 8.0 MB (7967325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87f673e4acf83b18de624e2abe21d1e389afecc7267aea42cb849732e5687ee3`  
		Last Modified: Tue, 03 Feb 2026 05:00:09 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:308d161115e27acfca3827f8ae3450e93a57ccab6d5158651367259dbc98bb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136450485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a95fac2bc55f60ef2dc7ef3e8db392f140e700a8f114496cd16b2b783aa088`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e9aa4982c2a67e202ea283fc3760e94d8d8b16966c616e01ad0238abbaac82`  
		Last Modified: Tue, 03 Feb 2026 03:46:50 GMT  
		Size: 64.5 MB (64479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3b63cef43ba943ca10a49d10d1849630837ea438982883acc8fc5cb20e2db86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7979831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe34898cb3d22d472733b039e7fad7f2e0b7df89a00472a85120ef8d077c235`

```dockerfile
```

-	Layers:
	-	`sha256:62bb5e181692bea40115dc91b0ecc9cd9e12062cb19372707dc29c5842245e94`  
		Last Modified: Tue, 03 Feb 2026 03:46:48 GMT  
		Size: 8.0 MB (7972441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7713e321bfd5436f51f38ef094105d4414cf1a76a52338dea12dceb60521309f`  
		Last Modified: Tue, 03 Feb 2026 03:46:48 GMT  
		Size: 7.4 KB (7390 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c5c8e2e38f8495503b82e0fab19643bbf77d6e7b1e5d61571a9966d9a1c3529f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140575118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db5033d7bf8dadc92cb46116d22b34a8c0199b268906824ec7ef15bfc893789`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a7f977a794a5fd56ece19f51541cec3b8ba447f10234ab001213bf850f92f64d`  
		Last Modified: Tue, 03 Feb 2026 01:13:34 GMT  
		Size: 49.5 MB (49468454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50ea552b26a58c13b4166d933269500891fb4897db09bc72d932372276b158f`  
		Last Modified: Tue, 03 Feb 2026 02:49:31 GMT  
		Size: 24.9 MB (24872100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc15e0cd687cd62190081200fbe30ab5102ae840cc68b0386259c387aef2b9a`  
		Last Modified: Tue, 03 Feb 2026 03:25:00 GMT  
		Size: 66.2 MB (66234564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:06d8f9832dbd0deb9a67361d2ccf45d2cf358189f6b68f82c2e778a5fb0f9e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2cd9621b9d3c83f82ad005794d2bc713fb5984209ca0221af864effd8b66b5`

```dockerfile
```

-	Layers:
	-	`sha256:0200b157873d87118bf9521b70f04f30d998ca61ac8be2adb075ecbfe0e729e0`  
		Last Modified: Tue, 03 Feb 2026 03:24:58 GMT  
		Size: 8.0 MB (7962206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12b121682e20b23cd1046a34f036d14ab34a9a1b7afa91d5148d47ec4d36644`  
		Last Modified: Tue, 03 Feb 2026 03:24:58 GMT  
		Size: 7.3 KB (7288 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e5b416c113c981b86177347536b9279e2ec8cfb409fee86a8336d1be1d9b3afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135688007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f660c505d809e5512532cee6372c7b1dfcc45d1c62ae2f2c493b80adea26ac2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 16:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 21:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b4c94e33bcdbce9a62a95be51a6e5f8ed2efc653e4be8f8f6722aa13d9d65461`  
		Last Modified: Tue, 13 Jan 2026 00:40:12 GMT  
		Size: 48.8 MB (48763393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3ebdc0d40ea56bd8ca0e23bf6a7db8ca22ab77cacf0ba126e24eb42d35c708`  
		Last Modified: Tue, 13 Jan 2026 16:17:52 GMT  
		Size: 23.6 MB (23614652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ee435e05dd9c53ddee45b81a8f55939374cd926a0e00239c752bb0832a5f8b`  
		Last Modified: Tue, 13 Jan 2026 21:22:59 GMT  
		Size: 63.3 MB (63309962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:98b0f6910c5538dcc512332f6b391404c69402dc05121b876b5ea14307a3b413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d29c3aa527471dc7b331e6e4442a0bf5ee88d81e2322c6d3d3ac147fb1b895c`

```dockerfile
```

-	Layers:
	-	`sha256:dba41830b710b75a68631b78e96a1b7d3b206614c05f6c6f04fd73989dfbac5c`  
		Last Modified: Tue, 13 Jan 2026 21:22:52 GMT  
		Size: 7.1 KB (7143 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:47efa1225a64ed792c781deb5b96be02dffe3427783bc560abc08496a18a13e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147844095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2f09a2e9d2cfc9271c954edfda29bd1ce8e39d88ca7a0864676f1080cd1b1e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 06:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2769c4ec4b4d67e8059086401477839f8b9d5a5026dd27df50a3c7ce33b9db`  
		Last Modified: Tue, 13 Jan 2026 03:35:30 GMT  
		Size: 25.7 MB (25670703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5fcb80ea7d84a82ea96c11045a4f40d0943808d5c5334ea90de2f7ed44f4c4`  
		Last Modified: Tue, 13 Jan 2026 06:38:28 GMT  
		Size: 69.8 MB (69846016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:779ef3a40304fe29db75036ac6e245eb949d8462a56420532f88ed53916eb79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf931bcc8631166959ea7d5145f2bd45f39dd0f626e083214a45a5039197dc25`

```dockerfile
```

-	Layers:
	-	`sha256:5d9d5d52aee7e0f79b249386755b884ba1a40e1a3069d5bcf708234b8a3ce17e`  
		Last Modified: Tue, 13 Jan 2026 06:38:26 GMT  
		Size: 8.0 MB (7973921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf767eae7a9f074c137bcc247c679dbb5c7a1e8be7bac01a73d7ecf653150c55`  
		Last Modified: Tue, 13 Jan 2026 06:38:25 GMT  
		Size: 7.3 KB (7342 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3f5d7f7711b70f8436ecdca206c32c8830c63eee2ff3d51b00c3ce73823b24d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134673296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2194c9c37c4f210263a6b9ddd00dcea2c974d027ad219e3e4e6a9c1245d3c03d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:28:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3072e3eb8c224dc593a4e18a3785b06d51467102b1cd9dd426d3d31d0e6831b8`  
		Last Modified: Tue, 03 Feb 2026 03:44:33 GMT  
		Size: 24.0 MB (24033633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61724404ca7e7ee67a943113b2e679af71546a07f66af094570e811bbc9fa743`  
		Last Modified: Tue, 03 Feb 2026 05:29:11 GMT  
		Size: 63.5 MB (63501320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dff4055e76a9684e3c207d34e4d974f19698bc50ea5cb5a641815dbe3a68458d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49de26c5c65e684080e7a79a6ea77e687bd1276379e30730da88345b7a55ffc1`

```dockerfile
```

-	Layers:
	-	`sha256:b456ee3158088962f210826487e6fd56e6def69ef609a0f91473508b8bb2e40a`  
		Last Modified: Tue, 03 Feb 2026 05:29:10 GMT  
		Size: 8.0 MB (7962361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5abf999e9d9b9caeb9f6a2aead2e5a1d4fb0589e510667ee588e327d1a61ec58`  
		Last Modified: Tue, 03 Feb 2026 05:29:09 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json
