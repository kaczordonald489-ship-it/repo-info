## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:534ba650eac31c2c66fb38d6c248556d25642e0fcf09800704649199b7e93919
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

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2940a831484767b51387a19c49667d02d0ea401e61cc436a961d350cc281fdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76129809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444e29d1bac68fb8ce837b814aa56c8fdfd68c50346aca34b649b397ceceaaae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:17:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e9c2d709d1a081127422a39a26861612ac4b73362a9abfb7ce643122e4082a`  
		Last Modified: Thu, 13 Nov 2025 23:09:24 GMT  
		Size: 7.1 MB (7106219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf061a3e4b28f5b0f11f543ece8916fca76516dfb846035bd9dc5de298fdb10`  
		Last Modified: Fri, 14 Nov 2025 00:17:59 GMT  
		Size: 39.5 MB (39486792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b5e0f934ea02499072903db401fce0921a859c8e2cc5968c822725a8bd2291b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5819978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0469dfc17b503e13dbdfef4cdda585b0acc7319d49440afe472c8ccb73c45ffc`

```dockerfile
```

-	Layers:
	-	`sha256:9e40d622215e4823316083688bf80f76f60c43fa95352be926327f55e5c28cf6`  
		Last Modified: Fri, 14 Nov 2025 02:20:28 GMT  
		Size: 5.8 MB (5812698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acdba8817c33f2a578ed6763bc1d35d9e796be36f5137081653cc20cf198d71`  
		Last Modified: Fri, 14 Nov 2025 02:20:29 GMT  
		Size: 7.3 KB (7280 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:42d117f84e61ce88a829aa90d6adfad648ac8697b581e8b8e888b57d06142f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75905223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c3a17cd688358bbc8348c1e16fa150af846d24209e7bc0b436e2d1953ae79a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:24:03 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:24:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:24:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:24:03 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:24:06 GMT
ADD file:94045c8d87683c20b28046857f569ac4ad9ec1c53b4f70e51c2badd873183cea in / 
# Mon, 13 Oct 2025 17:24:06 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:08:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4179ba9965faf453aec60ab64b5f5722816899d199d00def462ceb5d7057ad8b`  
		Last Modified: Wed, 15 Oct 2025 15:02:27 GMT  
		Size: 26.6 MB (26643386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9739de5d0afd9dca9ee20aee0e521243eef34d61181c7d41fe75a6734b107392`  
		Last Modified: Thu, 13 Nov 2025 23:09:03 GMT  
		Size: 7.0 MB (7009806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cefb3b89f82c2f9f1f8a2d1663021cb28b865bdf024df5a0fa38a4689cc301`  
		Last Modified: Fri, 14 Nov 2025 00:17:03 GMT  
		Size: 42.3 MB (42252031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:514385968f356ca40a154552a343a245b9e21f8fada9bd6a739b25fa568a3a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5821323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d714f817558d54cbb82e189ca179ffaf14345bc3f627719d52f38f92f2013a18`

```dockerfile
```

-	Layers:
	-	`sha256:cdaa846dc48efdc10afc5bec127f3cd43ac9f8abc390f5f9ef4cb701b0b2f75b`  
		Last Modified: Fri, 14 Nov 2025 02:20:34 GMT  
		Size: 5.8 MB (5813978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55fb73792d8bc6983016b71c2e12a543a9e0773779398533af939c1301998c45`  
		Last Modified: Fri, 14 Nov 2025 02:20:35 GMT  
		Size: 7.3 KB (7345 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:836f6709ca78e31161abea5788962c5bc7957dfd29c70a92e7e758e0e39cb381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73818929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d8a21c236d03ed418497748be890a85ecec429ea5962f20a39a070ec424a6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e799c76d7a2425b1efa4aab18a6ff0211a5844ff8737a1e027e934d92c1ac935`  
		Last Modified: Thu, 13 Nov 2025 23:09:14 GMT  
		Size: 7.1 MB (7052496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49217ce448c26b20627a680018d900a35c40f3e69f48b5b26ec74e21d1de561`  
		Last Modified: Fri, 14 Nov 2025 00:16:43 GMT  
		Size: 39.4 MB (39382556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:30ff2565293afee3f3695dbd797648e2953fca61648255135fbce4ce5948342b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5826453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07795723e499cb52a0186aa8acb20f064aa0e78270b10108300397affe2fa55`

```dockerfile
```

-	Layers:
	-	`sha256:d62f3e1cefed0d5296a87c84b185c7304ae9fcbbb60a35acb5147370646b5000`  
		Last Modified: Fri, 14 Nov 2025 02:20:41 GMT  
		Size: 5.8 MB (5819092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4db69ab1bbd96491055ba23f7a3b8e8fc6f7f1f8b9795575a225510acb9124f7`  
		Last Modified: Fri, 14 Nov 2025 02:20:42 GMT  
		Size: 7.4 KB (7361 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3ad5a24d0f27882471e6a967ef8555cb5992ed54a84db3b41d4b5dac1d93305f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86391750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bb4125bcf34eae6c93b89def31d4e24e81c312c9ee43cea3030b1c07fae1a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:08:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:59:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b4eeb4fa727e52ece1ec36da1e56c3bc96b88b022439cbbda81d3cb75e1cb5`  
		Last Modified: Thu, 13 Nov 2025 23:09:20 GMT  
		Size: 8.2 MB (8184640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0eab2c1d2cc02d16d2ae935456c3d265b4f5040901d1907314411a0075bb11`  
		Last Modified: Fri, 14 Nov 2025 02:00:18 GMT  
		Size: 43.8 MB (43760388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b52d981effe11d2b52bdf8ee40e4ac532ec5da2fea0834a55a1010152e3b0fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac971098f70046ff258851e0200eecaa8fae2d138712fe279f99d68b7c52dca4`

```dockerfile
```

-	Layers:
	-	`sha256:8fd11bcc5110a07a95da8698d9fb466457688f3c93f6cd58a5925d9784b947fa`  
		Last Modified: Fri, 14 Nov 2025 02:20:48 GMT  
		Size: 5.8 MB (5820542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdbf70f9b747c016f87ca9886439ae63a077d6a07930137caa732854df873f79`  
		Last Modified: Fri, 14 Nov 2025 02:20:49 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ee8eae3965a13b752286e959ffae4f1d5773720f612aa0f519ce8abc03d43007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76465917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02572ad838ea40438732c7514241f13771e25f929e9675fcb4d8c29e8445689`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:49:58 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:49:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:49:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:49:59 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:50:36 GMT
ADD file:16753c6442cb9871940bcae347672f49a6a001793657c89f4fff53584922f035 in / 
# Mon, 13 Oct 2025 17:50:39 GMT
CMD ["/bin/bash"]
# Sat, 15 Nov 2025 13:00:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Nov 2025 18:38:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5284c23c7e2d64db45a1d6cd39e83038698f86052acddf8ba9fa989a1c5ca270`  
		Last Modified: Sat, 15 Nov 2025 10:01:45 GMT  
		Size: 27.0 MB (27042158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7443a254ed640b3e9cc4214e379249f0da2318389406feff1663a907d6beb399`  
		Last Modified: Sat, 15 Nov 2025 13:01:35 GMT  
		Size: 7.1 MB (7118011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb21c499deddbc9d2b2ad93e65920f2ffe6a7bce1d8a8f3bcc857acda40161a7`  
		Last Modified: Sat, 15 Nov 2025 18:41:25 GMT  
		Size: 42.3 MB (42305748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ef36e1c500a96dcd8b664303244caec511857a561ddd944d570077075042c42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e97ed5204c4186e630032b5787394ade8a71444e9e14f423eab6859d85217cd`

```dockerfile
```

-	Layers:
	-	`sha256:856ce4ba95e42c7f30e4945119da7600a17e6a25b4021bc3e9e4ced2fb5b7f58`  
		Last Modified: Sat, 15 Nov 2025 20:19:35 GMT  
		Size: 5.8 MB (5803084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270c080c51b7282342e80cf6f7b44a5a3bb8451b68df93a3dd2987f1aa6f1b28`  
		Last Modified: Sat, 15 Nov 2025 20:19:36 GMT  
		Size: 7.3 KB (7311 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a60a8736d4f984516dad5ea4af7cc0238601675ddde5effd9f78826e6ccc1ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74441002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4afc20e372ff30978822b37ed637149413b12369807f3deaa6071c2006ca5ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:08:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:16:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2764735b13b9a123bf68ddb184df4ab1cf34712d89ac583a3087b795e7427c5`  
		Last Modified: Thu, 13 Nov 2025 23:09:20 GMT  
		Size: 7.0 MB (7018104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb5bd96c8ad65a70840d84c16f2558e8884de802eb817ca5e6b558bc3b1dc2`  
		Last Modified: Fri, 14 Nov 2025 00:16:41 GMT  
		Size: 39.4 MB (39419613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:210e19f85c8cf829dab67fd84ad404210bd703c1c17766b016c98ec8df9b17a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5820896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb879d93b2fc7ea9717ed7f9a8b92c8eb2cc87eda0bc0b3ae2268ec3aa45213`

```dockerfile
```

-	Layers:
	-	`sha256:a612c2fab52232e2df3f218d9e4a3c066fef6121166ae11a796ba086cbbe222a`  
		Last Modified: Fri, 14 Nov 2025 02:21:01 GMT  
		Size: 5.8 MB (5813617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b802a111d2816955f4f3fc50c03aec34c23755b01b82ffc717e062cbaf80dd3e`  
		Last Modified: Fri, 14 Nov 2025 02:21:02 GMT  
		Size: 7.3 KB (7279 bytes)  
		MIME: application/vnd.in-toto+json
