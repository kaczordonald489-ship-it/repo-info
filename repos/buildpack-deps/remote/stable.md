## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:3a9c0e0439f296fac6865bb12a3d884d68938708f84a27299785dfc9ced989fe
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

### `buildpack-deps:stable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d6abc8bc04207719f248bfe69f1059d9b343e896f7c0d357a5d5fa511133316b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.7 MB (378661966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734903e9100c57ff521ed7260eecdcd62386095ced24b49301c4b95f7203b79e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 10:25:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:ff2e6e687b6ce78177a4cac678dd533c8e72b97469f030783b6bb491f681fd4c`  
		Last Modified: Tue, 18 Nov 2025 06:39:26 GMT  
		Size: 67.8 MB (67779054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c40a3faff76845154c32b7b35d5535b201d3bd04f94a0c408f8e98f9ed98ad6`  
		Last Modified: Tue, 18 Nov 2025 11:14:49 GMT  
		Size: 236.0 MB (235979507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a2bd24ed4edf13b6cbfe9ec0289fb9a8f41e5ae2746feda2f6a79ddfd5a340ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17217753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6a479457616661769e9ab91b8f337002d6e5e395b6f87b68f80168e1e81453`

```dockerfile
```

-	Layers:
	-	`sha256:6ec863d0ff174929c6a8b4d0d764cb698ff735b492148cca694826a8605698a3`  
		Last Modified: Tue, 18 Nov 2025 11:21:16 GMT  
		Size: 17.2 MB (17207291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ad0df3c3c44366f459a34b98ec3b4f9739ac1d55f36a5c8a5a35a48ba7c0de2`  
		Last Modified: Tue, 18 Nov 2025 11:21:17 GMT  
		Size: 10.5 KB (10462 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5669b5f51d83d5e083fe6aa335c1b428951742589a4a6fc0a59a1e732b821715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342821183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95cba934963296f26d45a292a039029bc301460317d32d8eaea752af8afcb026`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:08:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:31:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:df3022b8716a9c6d6658073ff4323d54625cb7957fc65a6802c9c4662674ae4d`  
		Last Modified: Tue, 18 Nov 2025 05:08:56 GMT  
		Size: 65.3 MB (65318586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08963fe75e5bc1bc3c1d6b56076383f72f771556c0ab8447c3c248e622fd91e6`  
		Last Modified: Tue, 18 Nov 2025 06:22:02 GMT  
		Size: 205.7 MB (205708022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a0b917e19d568659e4bdc536609ecba297195ae7d321a6c8a06493da881ffce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16980023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44eb3daeb1506e9eb5b03ae64abacccccefc900de72106e62e324c1c1346b2af`

```dockerfile
```

-	Layers:
	-	`sha256:802557966e3ad48ed0e32c6bc86055c9ab41e2cb92731602ba426999013ec260`  
		Last Modified: Tue, 18 Nov 2025 07:18:20 GMT  
		Size: 17.0 MB (16969489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96ca24ddcc2380565baea8756e9c0000a61bf5c077dcdef3cb67a140715245d9`  
		Last Modified: Tue, 18 Nov 2025 07:18:21 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:916f18887c92eec1dda41c116024cca8e616fa2b3db49e72826bf1c681b7038c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325308349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ec6fb2daceb4e51dcdb36ca7c84dd4593dc46f2b1ec5734c8bd2204c01d06b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:28:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:23:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:40c45847805af09aa76d6ba7f34b42945f6767f5c3049e5027681335f35a18d5`  
		Last Modified: Tue, 18 Nov 2025 05:29:07 GMT  
		Size: 62.7 MB (62713438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7c26bb97a26732bed23444656e3bde850306d3b4a5d98a0b63b2f0257a0bb3`  
		Last Modified: Tue, 18 Nov 2025 07:37:00 GMT  
		Size: 193.3 MB (193256632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e7b74191584b942dbb5a32967dd65d18599ef3873fa6446119fef53a6d3be9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16985813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d23bba43d4b6265ec5dc091b951c5c9bd4c4a84600b070077cb56cabae3f468`

```dockerfile
```

-	Layers:
	-	`sha256:676aa07b44caf4ab5b15495e58676c3e189b158eb4f66b0e93eb05c8137cf089`  
		Last Modified: Tue, 18 Nov 2025 08:22:05 GMT  
		Size: 17.0 MB (16975279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02744826e8b5087f79bdccf1d3485f104d94f6bcaeee42b83a067ab791313d7f`  
		Last Modified: Tue, 18 Nov 2025 08:22:06 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6194bbf9157e339ea9d9c69904f1deeef9894316551d6bc639342f60b1038701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.4 MB (368368464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afaaf478bae023166385185fe1a204d6ba1fb56f9ed545fa83776f90b20aeef8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:35:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:9898fed0b4a62008cd3a65adf14beaff9f7a6dbe46176b901f31b3a21db4c6ab`  
		Last Modified: Tue, 18 Nov 2025 05:39:53 GMT  
		Size: 67.6 MB (67584762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f440f8aaa5e731bfd140931a396e53e1c2003b3316cc23a6fd1896c6e71c8428`  
		Last Modified: Tue, 18 Nov 2025 07:19:49 GMT  
		Size: 226.1 MB (226112459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d3729613d2813b6a14a43e6b9c3c0354e3b0dee22b9d085b49b0cf59863ad845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17302138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53857d389ded4f8370eca9fdaff843cf68c29594a5e478781392cd9abd9e110`

```dockerfile
```

-	Layers:
	-	`sha256:3b432eddefef4db84d983c8bebeec9e4d6eb6bee6b39b330598c0404b65581d0`  
		Last Modified: Tue, 18 Nov 2025 08:22:20 GMT  
		Size: 17.3 MB (17291585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe7cc145961e6826d8bf6e6b86ad88e13fd1f6782be3f3a67886d716e4a5f35d`  
		Last Modified: Tue, 18 Nov 2025 08:22:21 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b9307e705b7af69c901ec3d66a81df8038a7b3cb08be4ca02f44f12a0bfa6f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.4 MB (387447000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c921b2e70a0a8d13f947916b71c7624cef48a455efec5305811d322577b528e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:11:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:57:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:d3c892592b339e9b2ca91d682c607a5e915b21a67ae25c1c71d1f3ef8ea35c2f`  
		Last Modified: Tue, 18 Nov 2025 04:11:31 GMT  
		Size: 69.8 MB (69803141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a2cc22a301598554c10b84593a76f1dc7a055c549f0bdcfb133afc84a074fe`  
		Last Modified: Tue, 18 Nov 2025 06:30:32 GMT  
		Size: 240.1 MB (240065700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:344b8fc0e043a37a180469b4e00ecc4f718e34d186f8238bb82f91650501e64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17187318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d06927026ff2feb49006f682bd1048fe29e45afddeb784e037a63725eacfdd9e`

```dockerfile
```

-	Layers:
	-	`sha256:f83f2449fd82548cfdda54a898668e83875fd1d1b10df488187150ba02b1b57c`  
		Last Modified: Tue, 18 Nov 2025 07:42:26 GMT  
		Size: 17.2 MB (17176884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fb4f4364b20c160117064e6d95a9e10864d06e01b823408b4143e5072c6506c`  
		Last Modified: Tue, 18 Nov 2025 07:42:27 GMT  
		Size: 10.4 KB (10434 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:552258eb72909c8c48c9e6e19bb699dadb779f943bd6b81923e957f704c2bbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384226021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d26d1d463f2c5f9489585980dc91488638ee661db85ee2f652e0bf857ed55f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 08:22:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:0ba2b1a22ff6e7093fdd1dd2648adedf5202ef1304de7d17f711c19601d3a80e`  
		Last Modified: Tue, 18 Nov 2025 06:54:27 GMT  
		Size: 73.0 MB (73021903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8c7b0e7e39934178ce53a9a8f734eb91b249eb1d93ae50bc043579a195efbe`  
		Last Modified: Tue, 18 Nov 2025 12:40:13 GMT  
		Size: 231.1 MB (231098714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f9df62eae17e1a427aac017fd5a6c53fa1bc27b5d679df52c8dd05c83fb566ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17203340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcb321389dc3a82778b84323ea454be49892fe625b4efa57ada308d5803fe88`

```dockerfile
```

-	Layers:
	-	`sha256:476a7d186779de523849c544e62e34160ccad870af1cebaa5ebb0b2123b2505d`  
		Last Modified: Tue, 18 Nov 2025 11:22:26 GMT  
		Size: 17.2 MB (17192840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:077eaa3a247756d9e6422202f7bb591617ff3434f797c08a554c9487dca02e18`  
		Last Modified: Tue, 18 Nov 2025 11:22:27 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:078d93b781560c181154f1be785fee7a07b3e658fca2919a06258e87e446477f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.3 MB (462274178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6bb56eebcd27f68eb36a4c34d242d1c48c36cea5f22b077bdea38e08ee4da01`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 22 Nov 2025 21:51:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:9e592ded610a658bb788aebd62d933a07876ce0d2dff630e8511ac1eda3d0dbb`  
		Last Modified: Thu, 20 Nov 2025 22:32:10 GMT  
		Size: 66.7 MB (66660961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0946283142630ddc0be55b717109fdc10f4f3806b47ec32301b162ca5d92b2`  
		Last Modified: Sat, 22 Nov 2025 22:12:30 GMT  
		Size: 322.9 MB (322888286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:75ee133f6111e2bbc3553c6980b5fa030df94ca09a9d7d43bb2058d5c4499a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17273928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c6c43fdc5b05c3088412895faae5002e375732ec0085011761add5424dc54f`

```dockerfile
```

-	Layers:
	-	`sha256:d661b87bfa681bd291b891154fdf86cedf9c68dd6b7b4d3733af059d8c8ccdf5`  
		Last Modified: Sat, 22 Nov 2025 23:20:46 GMT  
		Size: 17.3 MB (17263429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:587298e8a410b17a6cdc3f0bba8f4349f874b41ac8224196a16b792a10fa6347`  
		Last Modified: Sat, 22 Nov 2025 23:20:47 GMT  
		Size: 10.5 KB (10499 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:018c48c80cb905be1cf2f2df9964ae22d660a3f234195cc04e2160c83540c87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351230211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3415d5beacff61861a1f502e2cbd6b2262d42a7580efe1a610c65f0ee234d46c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:57:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 07:29:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:d4530c943529730620c01f6bab681e114e8a52bebc697a9164bab0bee08dc992`  
		Last Modified: Tue, 18 Nov 2025 05:58:03 GMT  
		Size: 68.6 MB (68624056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac50f1d81c5e7e8663edcaac3894486402190c64a8bddf0d22e71c268724934`  
		Last Modified: Tue, 18 Nov 2025 08:14:52 GMT  
		Size: 206.5 MB (206473602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d832ac11636c4eb6dafaf30b58e365356b883df58a870226853b6bfebfddc2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16994986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8b817345a37cb46332f94c6f339385703270c22bd048a749a9619ca9c3efcc`

```dockerfile
```

-	Layers:
	-	`sha256:152e7759a7fb8c6c6901ec437b7880f1a949efab02bcff08e7aa0744f2a494ed`  
		Last Modified: Tue, 18 Nov 2025 08:23:12 GMT  
		Size: 17.0 MB (16984524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6260e76ec54d0733ef42572e935350f44d49a1b8a0f17de916992388ec6782f6`  
		Last Modified: Tue, 18 Nov 2025 08:23:13 GMT  
		Size: 10.5 KB (10462 bytes)  
		MIME: application/vnd.in-toto+json
