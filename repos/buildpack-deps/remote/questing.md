## `buildpack-deps:questing`

```console
$ docker pull buildpack-deps@sha256:b66d1cc6e349fa315cdf6e3a966cfbca34901f57a859b60efbf666fe9fc47cf2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:questing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:46b920c1be1e29adc68cefb239f0b0ba5dcd243bb989e4e9224d468d6c859c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272726028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30df2f241d32fdf521f9783e6d0ff9e3b5390832675292fd3458f7ce56a42162`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Dec 2025 06:59:16 GMT
ARG RELEASE
# Wed, 17 Dec 2025 06:59:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Dec 2025 06:59:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Dec 2025 06:59:16 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 17 Dec 2025 06:59:18 GMT
ADD file:3c9ad2247c67ca346f1495dbb4344056bebc791542d36d1ebce89d87dd34cf5a in / 
# Wed, 17 Dec 2025 06:59:19 GMT
CMD ["/bin/bash"]
# Fri, 02 Jan 2026 23:11:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 23:59:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 03 Jan 2026 00:10:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:16c195d4c5e9683ea3bd3e3afc1a4bd00392028211586424d551a9b2f20d6978`  
		Last Modified: Wed, 17 Dec 2025 12:02:21 GMT  
		Size: 34.4 MB (34398943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06f1a682b53d1c6d4a0735aac90e148cdf81808cfa81597a3e80c76257e4db4`  
		Last Modified: Fri, 02 Jan 2026 23:12:06 GMT  
		Size: 19.0 MB (18959458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339df752a36c7658bd49a504949a2d8bc6cfe2a54b5abeaf5bbd68260e35668d`  
		Last Modified: Fri, 02 Jan 2026 23:59:22 GMT  
		Size: 48.1 MB (48081918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b244071c31f568605c04464fea3a244521e42abaac4000b2d5defbc38ab7cf`  
		Last Modified: Sat, 03 Jan 2026 00:11:03 GMT  
		Size: 171.3 MB (171285709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db251dd9396c038310ed5a38fc39670661e21fd5542c03ef4ca9c85b2fba4cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11718917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39c5ca0e60f3ef6c7f5de465648958b5cb64242cbf072100b870e45b7c28c4c`

```dockerfile
```

-	Layers:
	-	`sha256:2899063931da6c28667798999ffb087a4125721fa4ced4689cebc1f8af70ecf7`  
		Last Modified: Sat, 03 Jan 2026 00:11:00 GMT  
		Size: 11.7 MB (11708757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c807edd03588d21f6da9417dfc27ea1bef6c5cb972482788f256196587a756a6`  
		Last Modified: Sat, 03 Jan 2026 00:10:59 GMT  
		Size: 10.2 KB (10160 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9297f1ab4c615ab6d0940901cd85d6ed985a964937cc4803003cadd5bd8ff756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225267212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44797cb2d3b717857a243d59a19f0189b099fee546c1037e4c859e9010d72c06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Dec 2025 07:01:56 GMT
ARG RELEASE
# Wed, 17 Dec 2025 07:01:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Dec 2025 07:01:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Dec 2025 07:01:56 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 17 Dec 2025 07:02:00 GMT
ADD file:c83f623082e6ef905d41888c626749887537e060207ac8b3be34f68d4a2f2378 in / 
# Wed, 17 Dec 2025 07:02:00 GMT
CMD ["/bin/bash"]
# Fri, 02 Jan 2026 23:10:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Sat, 03 Jan 2026 00:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 03 Jan 2026 01:10:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:86605e7f0af274af97c473f49e185f0ab72cde1b9e84f77330df2dae244554c6`  
		Last Modified: Wed, 17 Dec 2025 12:02:36 GMT  
		Size: 31.8 MB (31835257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1295d0d4e354b24cb382d32bb25b18ee9fb2791fcce4ff37e94032d41712e152`  
		Last Modified: Fri, 02 Jan 2026 23:10:58 GMT  
		Size: 17.3 MB (17337141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae84d2db8c69686c175c095f00380c344b5b7fa343ac6a1ac4f78024f1e4bd3`  
		Last Modified: Sat, 03 Jan 2026 00:15:28 GMT  
		Size: 50.6 MB (50578364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7bee3f3538d1bd93cc5780ee3a83b4ed2b40c42d2e7602a1a23271e3678233`  
		Last Modified: Sat, 03 Jan 2026 01:11:25 GMT  
		Size: 125.5 MB (125516450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ea99ac6e055c298500b65b9571cb532f99342bd65d01f3c3f0550ffb46ffa49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11460512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae20bf8779dc7d9385d02878e096c2197f3232de9d80dbe19b6818b1cc942a4`

```dockerfile
```

-	Layers:
	-	`sha256:c2df91e418beb8d475eae875529b56666e88521058cab1ba39ce3631be88f0cb`  
		Last Modified: Sat, 03 Jan 2026 01:11:23 GMT  
		Size: 11.5 MB (11450289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb09ff408bdaf0107ad6b8307cf49a54f07047dab5076c6320a46bece0263e6`  
		Last Modified: Sat, 03 Jan 2026 01:11:22 GMT  
		Size: 10.2 KB (10223 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2a3420983a22f149f2d066c38fa228af47badddeb4e046eaa6d5881c3fcb6721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261009454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d9ce700185e7519232697f6569dde8c539653880cd1026f22aa972ca07729c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Dec 2025 07:00:53 GMT
ARG RELEASE
# Wed, 17 Dec 2025 07:00:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Dec 2025 07:00:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Dec 2025 07:00:53 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 17 Dec 2025 07:00:55 GMT
ADD file:ce0ed2b1633c632fb10a1612e64252af75b1f5aeb73b4ae5c99aa52229614cc7 in / 
# Wed, 17 Dec 2025 07:00:56 GMT
CMD ["/bin/bash"]
# Sat, 03 Jan 2026 00:02:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Sat, 03 Jan 2026 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 03 Jan 2026 01:11:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:541fbd16e24de6ddea2b3b83a1222babc323c253520a32ce10c104edd3ed55be`  
		Last Modified: Wed, 17 Dec 2025 12:02:29 GMT  
		Size: 34.0 MB (33977137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664dc6d8a8c5821f7e8bf6beaef5f8ea3f3184cd4a76048ef4388651120842c5`  
		Last Modified: Sat, 03 Jan 2026 00:03:06 GMT  
		Size: 18.5 MB (18517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7cc1ad17a7f679dca34acdbbc77064b8f3c32b20c018d9204f1d8d65bfb5bd`  
		Last Modified: Sat, 03 Jan 2026 00:12:08 GMT  
		Size: 47.7 MB (47743522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f45766a7902935754105138eafab06bc92ce8fd62c4fe6594fc1a56be71bb3`  
		Last Modified: Sat, 03 Jan 2026 01:11:50 GMT  
		Size: 160.8 MB (160771058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:61192453d785182a1b73255fa2275f1a9c3276b05e5ba6fcff2e781d923742b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11773173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656a0a9abf2eb0e4d82a7625ed263cf66b494bba64a6f5b0323348a37b292b4a`

```dockerfile
```

-	Layers:
	-	`sha256:df90ee7d8a7a89a4b05715997817f29de58765d528b79e05c7e78e21201d60d1`  
		Last Modified: Sat, 03 Jan 2026 01:11:47 GMT  
		Size: 11.8 MB (11762933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f4a71e21053cadb2bad2cc3196f83426b21227ed0e984d54f6dfbf34b89b74f`  
		Last Modified: Sat, 03 Jan 2026 01:11:46 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1166d73deaf808dcdd3473c8593142e593c0b3649de7d4f72c1ab4937effbe23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280559987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ec7290bb81d1affbe3ea1dce5b430be89851f4ea8b00eeec66a4a73d3e512d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Dec 2025 07:01:13 GMT
ARG RELEASE
# Wed, 17 Dec 2025 07:01:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Dec 2025 07:01:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Dec 2025 07:01:13 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 17 Dec 2025 07:01:18 GMT
ADD file:80e51c252850cfc8712206404b1b9c24f10094c17f18f1925c33418780e67cc3 in / 
# Wed, 17 Dec 2025 07:01:18 GMT
CMD ["/bin/bash"]
# Sat, 03 Jan 2026 03:24:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Sat, 03 Jan 2026 04:10:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 03 Jan 2026 05:13:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ade432f435a67472df639da16a96659dc7c3849f8d5ede58cf5b95e186dec925`  
		Last Modified: Wed, 17 Dec 2025 12:02:43 GMT  
		Size: 39.6 MB (39596922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce71414238d174b7eed1a6544437609f0c9edabbc444ce584c9f4a94f03835e0`  
		Last Modified: Sat, 03 Jan 2026 03:24:51 GMT  
		Size: 21.0 MB (20961715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7e65121f0a6548b5fdd015ace0c6df36c83802207d4364d814251d24dc0f62`  
		Last Modified: Sat, 03 Jan 2026 04:11:05 GMT  
		Size: 53.6 MB (53555934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607cb3de241c7deded00a2491e88d2038996e9ed5d0b2d8dbb4964c48abce271`  
		Last Modified: Sat, 03 Jan 2026 05:14:46 GMT  
		Size: 166.4 MB (166445416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:443982280d092463ae5e6cc93cd92fbad0f39f3c15b098acd81b3afb26bb683f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11691331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd783c87bf268035d0e0d6f1cb05492e67880668998f1ac4a25aaf9d1461367d`

```dockerfile
```

-	Layers:
	-	`sha256:94a29caa3b957a498cd426d8208a4739ddade2f86ebfa23c4bfdd8ae94e8b76f`  
		Last Modified: Sat, 03 Jan 2026 05:14:41 GMT  
		Size: 11.7 MB (11681139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25422fe4480108ab76230c16223604ef5ad359bebd8267dce851432ef20dba9`  
		Last Modified: Sat, 03 Jan 2026 05:14:41 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0c26bdb425b71978b357ba34a24361510aaf58472e95d0ee7d269d4a34722a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241697495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fef1e2f5b46bf8bb320057e5532df1fd76ca1afcc0cddecf6d68ee4cf3825e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Dec 2025 07:00:12 GMT
ARG RELEASE
# Wed, 17 Dec 2025 07:00:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Dec 2025 07:00:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Dec 2025 07:00:12 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 17 Dec 2025 07:00:14 GMT
ADD file:730b8ac9cb4f3bfd36411b840b2d63e882b37e8ad20a45f3a02b3e6c861c8e31 in / 
# Wed, 17 Dec 2025 07:00:14 GMT
CMD ["/bin/bash"]
# Fri, 02 Jan 2026 23:11:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Sat, 03 Jan 2026 00:35:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 03 Jan 2026 01:11:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8e1aa813c1657f48b7291cc09d13191de87f8108febddf3d8484783665856c5e`  
		Last Modified: Wed, 17 Dec 2025 12:02:57 GMT  
		Size: 34.1 MB (34098575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3649778224895380b989840d5456da4cef6185e70ed1b3ef42d9544a1b97a41`  
		Last Modified: Fri, 02 Jan 2026 23:11:26 GMT  
		Size: 21.0 MB (20977437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce434fbbf6c750ddd674ac232ed482a18a2ad1dd800ccb988ae5a3f66709ad1`  
		Last Modified: Sat, 03 Jan 2026 00:35:34 GMT  
		Size: 49.0 MB (48968374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7221d4c41d96f62d4e5e98ca8ca958f5d63ec5699028b0af8110466cc5f2e2e6`  
		Last Modified: Sat, 03 Jan 2026 01:12:14 GMT  
		Size: 137.7 MB (137653109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3db9cd2f67fd52e04fabda3dfb47dc54542e839984aa8c2034d64d9f3a77edb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11494444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2359d9f197f2275ba1e641adc4d355c0fe5bf5c4537ea8fb9222069449ffaa`

```dockerfile
```

-	Layers:
	-	`sha256:a4ef8ef2d319c0f312126c5859b6263ccc5b946166d487e5ce9ef913675bdd0d`  
		Last Modified: Sat, 03 Jan 2026 01:12:12 GMT  
		Size: 11.5 MB (11484284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb93f9c35a4ad6c86a0ebb8d11d06e93ff5309769b1f71deb424a473511f425`  
		Last Modified: Sat, 03 Jan 2026 01:12:11 GMT  
		Size: 10.2 KB (10160 bytes)  
		MIME: application/vnd.in-toto+json
