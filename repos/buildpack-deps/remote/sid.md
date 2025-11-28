## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:84c7f50eff5f18e5e394d01d2fa8c2e2eeb58de52bb817c4fe1f35b05463e1c1
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

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f1036d1d3d1072a6d24a881e0b0b0f4739728e2c1cf9cab6df2895a526b16653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.7 MB (345746019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68796e3aa3a5b31f11a003bdb7b594240cdaa071d40283677262e94680c64f68`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 05:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 10:25:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:63fb544511bd02db3b85f4aa7407dbf6c6f5cd7cb1c0c1e65d055477ac245bcf`  
		Last Modified: Tue, 18 Nov 2025 02:31:43 GMT  
		Size: 48.5 MB (48500427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f587827fecd245749e6cb3adce116c1cb03e4aa424acd20250747a6b892e702f`  
		Last Modified: Tue, 18 Nov 2025 05:10:46 GMT  
		Size: 27.2 MB (27218199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabf9349c60b2bb444b4ff62048607f959a17f08b5026c6f0602163dac69f315`  
		Last Modified: Tue, 18 Nov 2025 06:38:55 GMT  
		Size: 70.8 MB (70835264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f84970ae79bfb9a8d8f74a5dd6c503ebd2ccb0dd9f39b61d786f0293589e50`  
		Last Modified: Tue, 18 Nov 2025 14:31:00 GMT  
		Size: 199.2 MB (199192129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:56fb0575105a1c7d5ca811521c7dedae963bf5254bf2276aab2d9e7389413e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16264476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21e13a4d988acc1ee35558ea0c70ddeea42b0966c09260fd0d0ea63f74949b1`

```dockerfile
```

-	Layers:
	-	`sha256:c780442a786f4e3135a0cbec2bf27b29174a9d3a379063f8a29991a228b4d6fc`  
		Last Modified: Tue, 18 Nov 2025 11:21:46 GMT  
		Size: 16.3 MB (16254343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e14fd3ad298acd43675aa6870ac43c423a5b6ac817c00e24dc9b4f984266f542`  
		Last Modified: Tue, 18 Nov 2025 11:21:47 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0a1b1f72af6f6338079f7148e1414e729883132f423295d996e124fd0d7676ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293756718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2879640722112188115c407ba72ffe504e9f1cb55ab495f4c1368a6f718c1861`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:59:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:28:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:22:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:249f143dbba2558bd4f87316a884ba0d2b99358af5b3c63e9ac2b9640e6f9846`  
		Last Modified: Tue, 18 Nov 2025 01:12:47 GMT  
		Size: 45.0 MB (45003691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdd7e51b270e55f3a7a9a2d43268061869ee4c4d0b6076dffdec9ff8ef06009`  
		Last Modified: Tue, 18 Nov 2025 03:59:26 GMT  
		Size: 24.9 MB (24946289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b78319f4c6f1757d125d21ba9e88a135787bf828fe59c5234a165914a13aa00`  
		Last Modified: Tue, 18 Nov 2025 05:29:13 GMT  
		Size: 65.5 MB (65528313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df725a769d8719e32d3cc09c4683ab2b9cb9a8b0d734fcdd3bc1d185e839ed`  
		Last Modified: Tue, 18 Nov 2025 14:30:54 GMT  
		Size: 158.3 MB (158278425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:192ef01aed1a92e6dc46f0fdb31977540ae3afdfe0a8ba33dab9bb6f2fb0b1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16021486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6101b8682a5d52af287680d3d83434f568491e741014c15b9c1b7e2a94b9e6`

```dockerfile
```

-	Layers:
	-	`sha256:fe50c8ffd0a9ca0a7166497f210f77086270da4dbf4ebd8838387b5c4cdd0a2a`  
		Last Modified: Tue, 18 Nov 2025 08:22:52 GMT  
		Size: 16.0 MB (16011291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:042310df324321e36cd1823df37fff7cb35fbfbfd7c07a0b4d55414c8dd31113`  
		Last Modified: Tue, 18 Nov 2025 08:22:53 GMT  
		Size: 10.2 KB (10195 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:09b935d1db77f92cfe9ebfe2b68f1cc88b8abf5ecd2a77056eaf00c6370f1eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334679300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2d24efbd9fde0f77105660116833e9843f9e3068d3a4827868080ceca52527`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:26:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:35:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2b90f6fb16dc868101354a233036d6d70e13cd3477e4df5ab59f2ccc8607c1d4`  
		Last Modified: Tue, 18 Nov 2025 01:13:53 GMT  
		Size: 48.6 MB (48591389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f615e7cb4b13e78f79053e3ff3386cb79b093cd2d91fe819f692264eb1475`  
		Last Modified: Tue, 18 Nov 2025 03:26:37 GMT  
		Size: 26.4 MB (26445334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8961176208fb3c6520aee3a23dd4452025d1885baea507b988ee8fdfe1d8b591`  
		Last Modified: Tue, 18 Nov 2025 05:39:35 GMT  
		Size: 70.5 MB (70473388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdf2e288fc97b8ac4d59a1e19623443f9d468782962eb3f4ed050296d55b7f7`  
		Last Modified: Tue, 18 Nov 2025 09:13:47 GMT  
		Size: 189.2 MB (189169189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d1256c463e474f81d497ffb124828e27c6f7155e2f867c5654ca97d14180ea27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16339104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c945c66cfbe74a5bce3db4dc2ae08c86ed658c548bcc74f8966ffe51a7334ff`

```dockerfile
```

-	Layers:
	-	`sha256:61430c1ddf44684f3fd275b439437107189e4cb49bf8fc75307293ee228a12fe`  
		Last Modified: Tue, 18 Nov 2025 08:23:06 GMT  
		Size: 16.3 MB (16328892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d93e86de7d873bcde12b7b009830dee3e34c46bffd91f11df084712c041a4ce`  
		Last Modified: Tue, 18 Nov 2025 08:23:07 GMT  
		Size: 10.2 KB (10212 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4be685340503a9a03a404f05ed39e97c8faad113923190eb0806e306753fd00f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.7 MB (353746873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73306812d9e33e61f02f5e86539bdb9eebee3bddb3cc5a2b88c048b145454220`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 02:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:10:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:55:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b1df74e42eaae76d71bf2c2aa402328d711dcdb63b4080ae4e7050388c00bad0`  
		Last Modified: Tue, 18 Nov 2025 01:12:57 GMT  
		Size: 49.8 MB (49833161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f52a4943d5de6ba698c20cbf767503261cc0eb7a108778d7a744e58da50d69`  
		Last Modified: Tue, 18 Nov 2025 02:57:26 GMT  
		Size: 28.4 MB (28445026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c64ad57b1efbe9eee5d9f5467a2b33ba6f6ba2ddf2dc652251bee45a3cc32f`  
		Last Modified: Tue, 18 Nov 2025 04:10:48 GMT  
		Size: 73.0 MB (72966735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0480e8cd920336bd68820ef5b18788d283fe9a92889b63f50618ca85845e5903`  
		Last Modified: Tue, 18 Nov 2025 14:30:54 GMT  
		Size: 202.5 MB (202501951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:966d8d4c4cd7285c6b728fc7b78b9121375da87e47c5472f5b259618a1d7bcab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16234234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c703f61c81cc021e755d18285462244225212909c4b2b4869c6dbb5eeb5f1ab`

```dockerfile
```

-	Layers:
	-	`sha256:921d4dd0abe2fbbf9b8315864302fa6f64a08e2de4fec5ecc264d3a2db717670`  
		Last Modified: Tue, 18 Nov 2025 08:23:20 GMT  
		Size: 16.2 MB (16224123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2d6e292b5065f902a4c4eb5e4bab7dd4da2f90bb1a690264adb7df3ed477407`  
		Last Modified: Tue, 18 Nov 2025 08:23:21 GMT  
		Size: 10.1 KB (10111 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a21abb667e2c4ba45580023c8f1bd3592d3397951cdb7fecb4d30501ffe80bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.6 MB (350639598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b291747da511ceec5d0d7a9cea8e5ea4ba65d16e4023c9b8b0fe98b78a887d85`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 04:06:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:52:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 08:17:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:233726152393942e1ef6b4533705d6bb3e4142964e6e486a7902cf456eab5151`  
		Last Modified: Tue, 18 Nov 2025 01:56:30 GMT  
		Size: 53.3 MB (53335631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8247117b12d78345474708e2bcd8a4be4ebcad8965145f6ab351c359ba9869b`  
		Last Modified: Tue, 18 Nov 2025 04:07:17 GMT  
		Size: 28.8 MB (28838475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df21c22b8199e396dd68073d81a213289efbf6a3e913789e13269dae310802c`  
		Last Modified: Tue, 18 Nov 2025 06:53:03 GMT  
		Size: 76.6 MB (76569175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630d1e40b9d0e13098920c6b26b3c2b64fe405597d473ef6e78888037547dd0d`  
		Last Modified: Tue, 18 Nov 2025 14:30:49 GMT  
		Size: 191.9 MB (191896317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7e128cfae338f8608d768fdc0f51f80be4979c038aca75cc0a96e60a6c771640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16238654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d1901f3ace143a9ec8cb7a464e37b2c85f2879ccb605eabe4980ed572f0f5e`

```dockerfile
```

-	Layers:
	-	`sha256:03a5babb24490f519e5724f20800e37c2ac5432d7cc5caac255161c8960aac88`  
		Last Modified: Tue, 18 Nov 2025 11:22:40 GMT  
		Size: 16.2 MB (16228489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3b98b48612f210716dd5526f4258cf9ea2223f065bc75dee3c89c7f0d3cf379`  
		Last Modified: Tue, 18 Nov 2025 11:22:41 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:560382490893079040e0ff079cfbd4f17fb94c7d743cbb76e636f2755db32f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.1 MB (452138991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26071e0c7b6ba26393f5e5fa6eae79e0699d8e431cd5fdc51d66f78916b24d6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1763337600'
# Wed, 19 Nov 2025 19:33:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 22:22:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 22 Nov 2025 21:31:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ed67ff00f4a63ed57f98b299833d8c2bd5b7627bfdca1af20fe366dfb5d9d552`  
		Last Modified: Tue, 18 Nov 2025 01:34:50 GMT  
		Size: 46.8 MB (46807232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12faa2c8d5976c2936626416dbd958b979633ec7e97e5fb377956f757414803`  
		Last Modified: Wed, 19 Nov 2025 19:35:09 GMT  
		Size: 26.4 MB (26394813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c856553cdba1b452f2934482676983f9c2dee9a9410ebeeee2db907f70948a`  
		Last Modified: Thu, 20 Nov 2025 22:25:57 GMT  
		Size: 69.6 MB (69597545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bf6d06ff1c105ed6a3cf1531c6c52c5a38a0e4bce47bfec4b65cce8f7da031`  
		Last Modified: Sat, 22 Nov 2025 21:55:08 GMT  
		Size: 309.3 MB (309339401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eeab707c587e210436d5cb35faae401130eb0565134bc00462108a2f98436dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16311848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79bcc184d1b5e0bffab3e5364c548db87ff63867971b3ddcbf2584dd1c2f088`

```dockerfile
```

-	Layers:
	-	`sha256:9524882e97e0c9f78e82eded7c97a04d66c93abb3be29254aae9d06ee47133cc`  
		Last Modified: Sat, 22 Nov 2025 23:21:13 GMT  
		Size: 16.3 MB (16301683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e341bcdb3aaa46b4d3f480a30a2055291cd10a05824e42f4a7084bfabe8d212`  
		Last Modified: Sat, 22 Nov 2025 23:21:14 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b5069e2df4afe2669fbe2fbe6550d61b125a369656d84b1ee637e5c48b05bd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314043589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbcbaf20206284fea4891a4fb83e0fe970ff9fa99f1c639af9adbf5e8a210b7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 16:21:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 17:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 18:13:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3fac6ecee4cd3dcadd720b65cbc3dc0f3dad0b4ed9c8b5d4ab2833f1e8d9ed22`  
		Last Modified: Tue, 18 Nov 2025 11:50:57 GMT  
		Size: 48.4 MB (48370424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165c3b5545bcabb40092d94aecec534cb4b55ae8e70b0d58ae879cce24508532`  
		Last Modified: Tue, 18 Nov 2025 16:21:54 GMT  
		Size: 28.3 MB (28338991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43eaccb5c28ea9f4e8082e22dee4766d2480b9df74579ce01f2f4291398a97a`  
		Last Modified: Tue, 18 Nov 2025 17:13:26 GMT  
		Size: 71.7 MB (71705173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f29225e45d027053fdb28d7ebf9d9afa1f9b40117426f1fa5cad3639e0949c`  
		Last Modified: Tue, 18 Nov 2025 21:15:56 GMT  
		Size: 165.6 MB (165629001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c547e25d559c3bcb2e0278c19fa811e10877066631cd03f2dcf65cbe80e739b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16031140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0c2fa522befbd4c6ea48321ff43de748f56d25295e08093cc713f5a8331745`

```dockerfile
```

-	Layers:
	-	`sha256:721df2f45c9e83395e69fc2653ef95e75a2d9878e59211082f91b51d7535623b`  
		Last Modified: Tue, 18 Nov 2025 20:21:34 GMT  
		Size: 16.0 MB (16021007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa2544ce90ba4443e482511969172933fac8ad7a9ee98313e100bf67b9eb13f`  
		Last Modified: Tue, 18 Nov 2025 20:21:35 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json
