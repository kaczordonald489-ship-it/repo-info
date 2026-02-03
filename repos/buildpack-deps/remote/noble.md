## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:67c3e3031425e74b85332eecb4377f313e77f995e62c4ddfe6d5454425685cfe
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

### `buildpack-deps:noble` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c54c6a964cd590d143c06540078e1bda83af7591c36ffcf9ea98fb21986e578a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274764989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddad8460c06635493fc117bdc53e27a79209e98ce896656f2d2a5983e93a18da`
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
# Thu, 15 Jan 2026 23:06:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 23:57:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:0e63a736e4b98228fe7119a5b87ac497c4d83bc620c97c1eae8af51da8a56683`  
		Last Modified: Thu, 15 Jan 2026 23:06:35 GMT  
		Size: 45.3 MB (45326988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d3b7ac6f02a00fe40d42d6dc80df228e364094971ea866787e826682284355`  
		Last Modified: Thu, 15 Jan 2026 23:57:36 GMT  
		Size: 186.1 MB (186086508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a8484d16e44a5941b7342c2b7fdf1f7a108c31a81960bc5928e1bcfdb3e34139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11743756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dfd228a8adeeceb83a2a32cc3a368443ff9e2f14932a17ca7a28ef5eeae8f5`

```dockerfile
```

-	Layers:
	-	`sha256:6240ac6459455118710a53cca162d8f65bc265e3eb4abe185d920fbd01a2939b`  
		Last Modified: Thu, 15 Jan 2026 23:57:33 GMT  
		Size: 11.7 MB (11733615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e99566f78b9779707f4283cb279c565a93033e5bfa8af414dcb99d79f9331bea`  
		Last Modified: Thu, 15 Jan 2026 23:57:32 GMT  
		Size: 10.1 KB (10141 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:00ff6ac91510feb8e2979eaa76ac14a0cc93edf6216b12c19b22b81e7f9481c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236844452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589fdfccae8bf00200cc831c280a8296ee5256343954afa21b624f1d228ab7a9`
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
# Thu, 15 Jan 2026 22:34:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 23:28:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:f3c8afe3dc2552f88b1b7914a937da45531923f90c57cd50f28de3eab1e67005`  
		Last Modified: Thu, 15 Jan 2026 22:34:55 GMT  
		Size: 48.9 MB (48868500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc901ccd3a2634b216c789acaa88c236eb6c7fbab141c51ffcf7506955e397d`  
		Last Modified: Thu, 15 Jan 2026 23:28:31 GMT  
		Size: 148.3 MB (148337329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a1fb326b70ee23ca126ea272f9e835ba8c317605fcb29a17846f8a6e6f894872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11069521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54be61dcff90d0efaffaec3596768dcbcdecbff06f07167d0f3388d142836490`

```dockerfile
```

-	Layers:
	-	`sha256:e52eeb6b66854e7f26e532f96a9df15fac588f960ce0842b834842dc2886c859`  
		Last Modified: Thu, 15 Jan 2026 23:28:28 GMT  
		Size: 11.1 MB (11059316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31e224842484376309b5aa8a80ef0352bdee9c05d6fc2e424cc66c0cc1a0d81`  
		Last Modified: Thu, 15 Jan 2026 23:28:28 GMT  
		Size: 10.2 KB (10205 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:15f560bb111a863fa952bd97583fef818619ee5b33cd6ab504536ff492991071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264348232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50f9a9bf336ba21adccae1ef168117ff2a7f5d19a130c03663f6a756a7cc7df`
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
# Thu, 15 Jan 2026 23:12:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 16 Jan 2026 02:34:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:d8bdaf459df2fe5312d39bcfd87fd35052fceaebb842c7e30c2113e0e6a9b4d5`  
		Last Modified: Thu, 15 Jan 2026 23:12:59 GMT  
		Size: 45.3 MB (45276515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a7b36eaec4347afe61a1840fa00310c8d476eba73dd4ae0d3a7fddfc8b29f7`  
		Last Modified: Fri, 16 Jan 2026 02:35:00 GMT  
		Size: 176.7 MB (176747689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:92eb98b6f87c3bff76f7efd0cc96e6ddd61c4b3199de1af0166a8f89bd488ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11293305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a16baa80cd598fc0c136fb6dc317e62590ff9b20e11d4ecf733addac0e4f9c6`

```dockerfile
```

-	Layers:
	-	`sha256:082e622826d0271b8d4616ea3c1e048c96fa29d8cf49938437c2609574e96266`  
		Last Modified: Fri, 16 Jan 2026 02:34:54 GMT  
		Size: 11.3 MB (11283084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a26e937f40a9ef650a96ceb12e47c62070223ffd2f3b731d1e4b2d71856ced6d`  
		Last Modified: Fri, 16 Jan 2026 02:34:53 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e0ff6638a0ea42325742ddbb125e926b0b7731980c26fe6c481e28e54e4f1351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.3 MB (290348449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb79915367a5cafff1b86db971bdb9a955fea2d5e6abfa310454f2cdf88feb3`
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
# Fri, 16 Jan 2026 00:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 16 Jan 2026 04:17:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:d22b520ce44b4a094fb8217063a7cf2415586a5a115fb5c153dd6d346e7ed811`  
		Last Modified: Fri, 16 Jan 2026 00:28:42 GMT  
		Size: 50.4 MB (50387122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43814580ae0b43d470e10ed2b558d2e9cd86668d8dbf02d7900d7238a83b0225`  
		Last Modified: Fri, 16 Jan 2026 04:19:24 GMT  
		Size: 189.7 MB (189701237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:860109c2dfbe32759e8d6bef8a876e06d70b4e6c5514ff4a6f4dbc19126df9dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11240694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56308ad56f6c25d00ad72417a78bd1ea84d9125b21f76a0519a2b0835a1a4939`

```dockerfile
```

-	Layers:
	-	`sha256:015d7bb13e620c25a04e5a7799ef34739c1f2b6bd332449747d1936e247cef24`  
		Last Modified: Fri, 16 Jan 2026 04:19:19 GMT  
		Size: 11.2 MB (11230521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44fdc00fd401255c9bfea5ca13ca418a38b1abc2bd8e88a7d59ef8d97178dc98`  
		Last Modified: Fri, 16 Jan 2026 04:19:18 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:fd3d0326f9afcb631284d9a013ed5ffc8e0638b1cb514e286d7657409c9f2db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330446115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2080a4b44fe51ea95ad38bcf4ed19f77ce08d821adcf3b905d42c178f182c42b`
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
# Tue, 20 Jan 2026 14:41:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 22 Jan 2026 05:56:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:1dafa63c982ccb6c692e1e05cfd12ed9263e9ecf6d93e52b51783e4d8dd6ae0f`  
		Last Modified: Tue, 20 Jan 2026 14:44:02 GMT  
		Size: 53.9 MB (53875613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36210f70da4605504cba8c997c5e2642a1df25d6cb68c0ebe626944fd5a96bb7`  
		Last Modified: Thu, 22 Jan 2026 06:07:10 GMT  
		Size: 231.3 MB (231286473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f9e792f3c3964ddfe84714c7a41d47fd2cf52cf168ad4b156e8078b5044ecb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11233935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e0d9c6d11daf0a0da985122ada0baaf9848d511cb5094a54013627792ccdbd`

```dockerfile
```

-	Layers:
	-	`sha256:784549636393bb3f0a4a42cff0c6baa9c49bcbe551c5d8863508c27da74400b3`  
		Last Modified: Thu, 22 Jan 2026 06:06:37 GMT  
		Size: 11.2 MB (11223762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:237cc5b0a6081177871a64d8502c68ded0322efe9e37de3ca58a16c68f0ff496`  
		Last Modified: Thu, 22 Jan 2026 06:06:34 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b99dd8e41bd37bb548526c896bdb0eb078f6bb27420328fb45380ba7d208172a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253044488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754bccdb92b59b3d8e6cdfbc0d509bdf7d45b79bfc75943bb4e161479fa7b917`
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
# Thu, 15 Jan 2026 22:45:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 23:33:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:d1367c10ac265d048da5237db9dab8a587604691a2352f8707a36063b6f33fa4`  
		Last Modified: Thu, 15 Jan 2026 22:45:57 GMT  
		Size: 46.8 MB (46751639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d85d6172291205fb73a14b069a97644963bce275ef50f874be00f666846d34`  
		Last Modified: Thu, 15 Jan 2026 23:34:44 GMT  
		Size: 161.4 MB (161445659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cd5f50292b229ae656bfd8caa52b1631ee6c210d3f5ef677592b9e37ed0a107d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11084507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f3060d0335c2e886421c4f6b7bfb24411dfd993567006db81954b5eea923f4`

```dockerfile
```

-	Layers:
	-	`sha256:cf9d86ba53186124ae40c1f2dc0fc785b8247e655d2616ac16adcb6a63a92dc7`  
		Last Modified: Thu, 15 Jan 2026 23:34:41 GMT  
		Size: 11.1 MB (11074368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb37ca520c56605488c65fb0b0e05c4db2e229db50c237de4b58a0b9d64aa53`  
		Last Modified: Thu, 15 Jan 2026 23:34:41 GMT  
		Size: 10.1 KB (10139 bytes)  
		MIME: application/vnd.in-toto+json
