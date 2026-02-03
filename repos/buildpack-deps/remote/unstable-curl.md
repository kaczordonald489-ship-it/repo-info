## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:36d19b65372629e4415031ca37ac83189f419041f23a4ccbb95865819641d988
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:058997fc85e08e5d1ecdd9b15f230c63f29c2699c7097612e63d72faef4ff8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75880819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb59c1e7b53870c496f4bbbacd038ba73caf4aa9242460ac46ee7cd2ff5cb6f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e5dc831051d738f5c1db4254dde56feb7c9e75e136e23995d896f1b6e1ba752f`  
		Last Modified: Tue, 03 Feb 2026 01:15:47 GMT  
		Size: 48.7 MB (48654703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7215d01a65c1956de10f370e9c70556dc553159f6db5154f95cf3f4792912cc`  
		Last Modified: Tue, 03 Feb 2026 02:43:08 GMT  
		Size: 27.2 MB (27226116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:445d9597d3492dbc7608a69f67a419bac209655f02e7993725e8e6d8ff93ca4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4136946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc204aa30611f82461ac3dfec5ae4a8bcdb29670ab19f3d75aeee71eef5cd440`

```dockerfile
```

-	Layers:
	-	`sha256:57b732576ea84c995e92599beb0731e76199e53e4192b8a7ebe464e527f372a0`  
		Last Modified: Tue, 03 Feb 2026 02:43:07 GMT  
		Size: 4.1 MB (4130185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21b1564573094c103a4428d42a6c165175e92fb6c6a18377857a8ad4e2892f9a`  
		Last Modified: Tue, 03 Feb 2026 02:43:07 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5b09645dd3640edb1013e700e1854fa95191a77d65b8b351e359d5d48001c179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70531894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07247d7b2bcb54e5a7c59c9acc1ca4167ce36c2bfde26eeb4e9c6feb36ede641`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 03:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:659484058ac0aeb678184c63f6d8d114ad6c5b9d6dec2a7ef5b116eede567c38`  
		Last Modified: Tue, 03 Feb 2026 01:14:09 GMT  
		Size: 45.6 MB (45617401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe3a9f29c87d719cd363c9ea832a530a5b4b4746470456e3c9b94d23ec5870e`  
		Last Modified: Tue, 03 Feb 2026 03:32:06 GMT  
		Size: 24.9 MB (24914493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c86f831d9d4d4dd1b0b464620e342c72918d529f133b90007d6bba84efad0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4138506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26fbac1b5f0821688d1f11ce0a3591f1bc35126ffd8ab3bb697dfb6898bf0937`

```dockerfile
```

-	Layers:
	-	`sha256:e071db481ad7502a7979d9a098d39d5c4e39cf89094e818d0204c9c8c4dece9d`  
		Last Modified: Tue, 03 Feb 2026 03:32:06 GMT  
		Size: 4.1 MB (4131681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a92116314c29bb49f00f0a6cbc2ecdf1b2bd67b019095dbbcb86660e528cc6c`  
		Last Modified: Tue, 03 Feb 2026 03:32:06 GMT  
		Size: 6.8 KB (6825 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3d33b1ae01d8d80536574c6498fee0a9e21ccb766185306265218275e992c2e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75202327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c88b819f0943d3ecb83d7958fbdb4a86ce079e583f6559c6a326bbbde2c7a00`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:45:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:02c386337e70e225c826a0b6295dc937d7a841e7301f60fa7a03adccf75af2ad`  
		Last Modified: Tue, 03 Feb 2026 01:15:52 GMT  
		Size: 48.7 MB (48679232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d5d2801ff6474ef689dcd67964dfaeac9d07e6acea8bddf570dd1be8c55d9`  
		Last Modified: Tue, 03 Feb 2026 02:45:59 GMT  
		Size: 26.5 MB (26523095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:66803a3aee5459faba6f2c43566554cb2ec816c8907c524acca32d15b7c7184c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4147218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af3b4b49d8dca87f626886872068ee60424661d23321852ce6adb07a4aab921`

```dockerfile
```

-	Layers:
	-	`sha256:99b5675973436d033593512704c61ffbeef11ffa5f46a8a1289afb856246c289`  
		Last Modified: Tue, 03 Feb 2026 02:45:58 GMT  
		Size: 4.1 MB (4140378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fb90abf315629b4dd269d58b29446c6e65b4bd97f08dbd96c2adcced8e8951a`  
		Last Modified: Tue, 03 Feb 2026 02:45:58 GMT  
		Size: 6.8 KB (6840 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0a86f1bc1c30272536a79ffc612f47d96b189e6d9ee0034fa290d58f62495ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78475253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88adb1dcfd2606449005a1461a9333645bbd91fcaeedf70279c6be34a7e9b2fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:49:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e68504863f049552110bc4132aac67ebf9360a9ca0dd44ced1eb7009b5560a2`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 50.0 MB (49988982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0705ca0064646c1e4566b7b80128c6bea2154bc55479916bab1429dd99abce8`  
		Last Modified: Tue, 03 Feb 2026 02:49:58 GMT  
		Size: 28.5 MB (28486271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6104876abc4be0150bff1e9138781f1ea11d028a4514570c3572e09956717d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4134018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935c7836c888449ae197d4094778ea64a984751b49f554586a9c76f09bccc323`

```dockerfile
```

-	Layers:
	-	`sha256:7f443441bc30a9a90fedb309f950d55ba602f07bc14b9f496f5e6d2ad6395bc7`  
		Last Modified: Tue, 03 Feb 2026 02:49:57 GMT  
		Size: 4.1 MB (4127279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c782bc9cc91ebe3547caea3c2fdd23adda9176cc66b9643ed0d84b285097d860`  
		Last Modified: Tue, 03 Feb 2026 02:49:57 GMT  
		Size: 6.7 KB (6739 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bd57fa184b8e2813d64447ab1873e4866741af06ee0f061da470fd1da4486624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83093784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d12cd0122b439b3f5a27a0420b0d29379dc298ba98773306307b0e5257a2af`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 05:23:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:73480cc26c615330eccab26ce34bdcf83d5889a7e09a86213699bf4e4f64bc74`  
		Last Modified: Tue, 03 Feb 2026 01:14:38 GMT  
		Size: 53.6 MB (53584520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46f8ef4210c5f651d581237fe6e5782b63d5da72519ff94633f59a07cfaed33`  
		Last Modified: Tue, 03 Feb 2026 05:23:30 GMT  
		Size: 29.5 MB (29509264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:95a2eac3a7c533302d2ab905c5d38d5158e2833ff534fce789d7fd7e0addd169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02d4c95afca2d2edbb556246384c1dc2ebf803a47e88325b4ec011878dc3598`

```dockerfile
```

-	Layers:
	-	`sha256:618d06ad388c3e1c4a3987d78f964b1689e91227e9cf451bbc237c665cb7f16a`  
		Last Modified: Tue, 03 Feb 2026 05:23:29 GMT  
		Size: 4.1 MB (4134072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d2dbf1edcf029c352c5433e10efeaa6d849c3400cd26ba9bc0047bc505f8c0`  
		Last Modified: Tue, 03 Feb 2026 05:23:29 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:13175392da6a3a9c8dd4577e73ea51664db1f26abcd7dcaf13ef3b64ca3d8f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73596037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a42e59fa05e2ab3bf7545722004bbbfe43fa8f3e8c6327667e3b7428b2ca6b6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1768176000'
# Fri, 16 Jan 2026 06:44:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3f1a05ef5786076b47fcd681b3f4ff2ab26c932b463a6ab7c885cf7684b1355a`  
		Last Modified: Tue, 13 Jan 2026 00:55:56 GMT  
		Size: 46.9 MB (46856753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2839eb91239c64d14daceac3c851cd6aded1a2915fa193b50025c045cf501598`  
		Last Modified: Fri, 16 Jan 2026 06:45:41 GMT  
		Size: 26.7 MB (26739284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:281f3df94de125a7d6ea37b2d0352da590c45c86dfa819cc1b7d9cab78a67f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fa41d37633ad8cc11fdf06b05c5f1c250378af7119b5b8bb4c09b0bf709b12`

```dockerfile
```

-	Layers:
	-	`sha256:99a207a91a3ce372d3008711036e005a7d6e1a2bfc5f66ddba5ce8e099cb5f0a`  
		Last Modified: Fri, 16 Jan 2026 06:45:38 GMT  
		Size: 4.1 MB (4105773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e20a036e05bf60ff268c23de6755cb85cc8d54c685cb36e18ffc1fcc24871850`  
		Last Modified: Fri, 16 Jan 2026 06:45:37 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c532d734f7e844c56d0c6e6f5d53acb790432e66fadee6fbe8d7a978af03566b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75420929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378396a9415899ad961de5438c029b55a6a4b8bf1df6a33f841fc0bb67fba1d2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 03:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3bfb68c2648b1088debcce6bc605d7ea6709b6f129c9ce647bf0a7c385d8350b`  
		Last Modified: Tue, 03 Feb 2026 01:13:18 GMT  
		Size: 48.4 MB (48421195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd1e07a5a5c7ee531c5adb5cc340d101adfb8e3eab835cd2272f521de25591b`  
		Last Modified: Tue, 03 Feb 2026 03:45:17 GMT  
		Size: 27.0 MB (26999734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:46286f97eba09e863a0ccec9f17a649047ac7f17e491ef752ed7057684c42f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4138354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5cb175477d1fc2aba2b8934c1505a564b15c1566ea121aff9c199fa46e53c6`

```dockerfile
```

-	Layers:
	-	`sha256:7ba9aa61d7cfa2f1f0ae0c0332283150ddb2a7586b55423df8b5edcb27b0bd03`  
		Last Modified: Tue, 03 Feb 2026 03:45:17 GMT  
		Size: 4.1 MB (4131594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d2144c3bc71583a20e050158472bd6d8259abb35cd26e573d75b406334b1ca1`  
		Last Modified: Tue, 03 Feb 2026 03:45:17 GMT  
		Size: 6.8 KB (6760 bytes)  
		MIME: application/vnd.in-toto+json
