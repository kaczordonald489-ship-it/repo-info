## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:d4fd69bb99607c2ddb61ffbc9aa1c3fa4110e9bb65d4eb4c9b58d8dc22092664
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
$ docker pull buildpack-deps@sha256:40ee16e3f341497dfd8ae089abe47e60447f714389028726a8c21a75ac405be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274854511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa71cd6ae89dbd75282d20c4fb41a63d96bdb7ea7945b7be39bade127a6135ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 00:17:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 01:12:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c668cd5acbec9ebe075f97945b9bf808fcbaf0ff91d3360a2a75cde58343fef`  
		Last Modified: Thu, 13 Nov 2025 23:09:25 GMT  
		Size: 13.6 MB (13625282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814b5b2bea6de007655a89e52c5edcacaafac6807728baf4570609d0319bcba4`  
		Last Modified: Fri, 14 Nov 2025 00:17:52 GMT  
		Size: 45.3 MB (45334213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5366665d9b099071da40900a418bcbfbfc2528b90e33d6a49fc51af92a45251f`  
		Last Modified: Fri, 14 Nov 2025 02:38:39 GMT  
		Size: 186.2 MB (186170328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:61736f5df92b069a0f1bbe1a5fd07de73b35efaa124830beb3690eff56c544f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11742936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bef6c2c1f09b9237632de39f226a4fc9d768e989f5599f4b7a23826aaf76e0`

```dockerfile
```

-	Layers:
	-	`sha256:dfd2ac79809ee14ed6306cfb647a8eff9a35b8d361627efd455b6a01b3059241`  
		Last Modified: Fri, 14 Nov 2025 02:20:40 GMT  
		Size: 11.7 MB (11732795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5d8ae050c341bcb6f1ab33470213529494bbaa767c5adb1d928be0adac7b039`  
		Last Modified: Fri, 14 Nov 2025 02:20:41 GMT  
		Size: 10.1 KB (10141 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a47a5e983d8bb3e704c6ff7c3bad37468d82dab9651edcd38006aa730fe3dd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236821359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60a3baf8a0b6090ce6815674b9a30348425c07179a7be61deb44c84b4e4a8ab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:17 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:17 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:20 GMT
ADD file:dd3740083ecd2e2b1e178f1771ef73043bc7be6c831492453a755b873d8b531b in / 
# Thu, 16 Oct 2025 19:25:21 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:08:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 00:16:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 00:25:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6cdc0abf996c3192bfbda4018d34c282871d4be33fb369176002cb2199673adf`  
		Last Modified: Fri, 17 Oct 2025 08:06:35 GMT  
		Size: 26.9 MB (26852672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a486cdb97e19941132739589a8ece69d10d8589498cbfe3555a16848bace17d3`  
		Last Modified: Thu, 13 Nov 2025 23:09:04 GMT  
		Size: 12.8 MB (12784335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a347d0b45bec95de51111529201fde2ce88251da35ea7d5a3e292eeae423e24d`  
		Last Modified: Fri, 14 Nov 2025 00:17:03 GMT  
		Size: 48.9 MB (48865617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b6fc9ee718b6d724154fa12e1ee586740c2b002629b6d8afa2d42feb795650`  
		Last Modified: Fri, 14 Nov 2025 03:22:55 GMT  
		Size: 148.3 MB (148318735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e07ec364ba63470265f379a159d8ddcdf65225c6c0cfa47db42c0bb10be44bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11068701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e34c57f86104ba22fce1123cc4681d725e42e58a93a7e7cfc222d8ba6a9aa9b`

```dockerfile
```

-	Layers:
	-	`sha256:59624e9939be658d0440cd3a0bae508bf15a738420e9071071a1435b35790bd7`  
		Last Modified: Fri, 14 Nov 2025 02:20:51 GMT  
		Size: 11.1 MB (11058496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18108effd5c5fa47ddf93b5c5d3c213c88a354bc02ab328471a183d22a5b2a6f`  
		Last Modified: Fri, 14 Nov 2025 02:20:52 GMT  
		Size: 10.2 KB (10205 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:34dad24eeecc4bc8254e5071934042fa6d01a016bd3a4a8b2f006be51c7f615c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264339516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c0bd5f8026b6ba51b753350ce25233e907c53a4fea0ede393dddb39ffa486d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 00:16:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 01:29:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91915e231584f62efaf131bfa0790161480f0edab31b9b19fef69842a47de107`  
		Last Modified: Thu, 13 Nov 2025 23:09:47 GMT  
		Size: 13.5 MB (13460518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51768b66b542a7ace2324cb9ce13ba3af108df1ea0220409010b65ec6b047e6`  
		Last Modified: Fri, 14 Nov 2025 00:16:50 GMT  
		Size: 45.3 MB (45273960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231cc30f5c87fde21a3f8d32db7455be01801b449546deff1dd72809cf643b21`  
		Last Modified: Fri, 14 Nov 2025 03:22:51 GMT  
		Size: 176.7 MB (176743081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3ec62c7bb2c23f3065aeee31a567900b6df9ae6fc8ec4e9f16fc24c7c6d010de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11292485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007f5d2b8ba91fd9f667e77323b7f6602eec34ca6a1a07b1cce30fb979e5a77f`

```dockerfile
```

-	Layers:
	-	`sha256:50d92c604768ea92aa4aefce62a7f131399b0355a679eca3742c9b655b04330d`  
		Last Modified: Fri, 14 Nov 2025 02:21:02 GMT  
		Size: 11.3 MB (11282264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8a1de37109931122dd96eedbf4d273f91dcee7b3afd0b57e22d40ccb15b9f8`  
		Last Modified: Fri, 14 Nov 2025 02:21:03 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:146292e6c70eb3bb645cd368a5463faaa4eeba7090f99e49e5f37e35b8cbaf1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290416313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3103b3c3082054b70c70468d07aa2f8cefd341978f69393a2ef6da6ef92f3ddd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 02:00:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 08:00:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a4a700414b1bee6f9817639ad4680ca4bd340cc27c4f2c808e3c3a79d17c57`  
		Last Modified: Thu, 13 Nov 2025 23:10:21 GMT  
		Size: 16.0 MB (15953323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8c0f0b044214aa736deb91e0391d16d574cad959d8479a7a32cace8ec7eb46`  
		Last Modified: Fri, 14 Nov 2025 02:01:32 GMT  
		Size: 50.4 MB (50434199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ebd5e8971c6d4eb9eb14516fc5cf514d987a5e13b5503985e040f50586408a`  
		Last Modified: Fri, 14 Nov 2025 12:59:21 GMT  
		Size: 189.7 MB (189724367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2a186a7c7e8117016082c7fdb4e83f582d8252e7533442df71a7e7164c11f0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11239874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a8b0a0824be91c4a1b4679f80c5c3334218a0bb416c0011dfba945debacac9`

```dockerfile
```

-	Layers:
	-	`sha256:04c8b0d3fc87bc0f8abd1b840d37b48646127a6023126b015b31df7dbc77b1eb`  
		Last Modified: Fri, 14 Nov 2025 08:19:55 GMT  
		Size: 11.2 MB (11229701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6cb98f4dfc695c1006d00eb3f895e68d84561af8c04a3329e1321364dd1e98`  
		Last Modified: Fri, 14 Nov 2025 08:19:55 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d8e17a6121c6ded02c02303169fe2b2598e48c2995e305f23035c202afa1adbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330422680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4b95ccdfe1cd89ebd7ea3d0a6318bd1c68e646b89b867c570b49e924713317`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:53:04 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:53:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:53:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:53:05 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:53:45 GMT
ADD file:6c2a12ec42d9e6c7e02041a8483a3a93ab9b91131ca66ecb93506ba161a4909d in / 
# Thu, 16 Oct 2025 19:53:49 GMT
CMD ["/bin/bash"]
# Sat, 15 Nov 2025 13:02:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Sat, 15 Nov 2025 18:43:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 15 Nov 2025 23:19:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4f36e1b0a2cc427e5979b49608ef4e52795313f083fdc941cab616d5ab2b861b`  
		Last Modified: Sat, 15 Nov 2025 10:03:37 GMT  
		Size: 31.0 MB (30952148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fe26cbe50b9b2672d6782614926cf465e524a1b183dc6711f86e1a34299eb4`  
		Last Modified: Sat, 15 Nov 2025 13:04:08 GMT  
		Size: 14.3 MB (14330755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a6d18bc2bc7a34a2c5477bff9a019728e87fea3c79b6a3cdb270c69a48afaa`  
		Last Modified: Sat, 15 Nov 2025 18:46:30 GMT  
		Size: 53.9 MB (53876297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456b43676af16a4d9650dc7ac720213433597d611108d1ed4330debb92a49ed3`  
		Last Modified: Sat, 15 Nov 2025 23:44:05 GMT  
		Size: 231.3 MB (231263480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:60739e02ada1d1bff697ccb6bfd9ceeb4fea1ae6609794b9ff6a33bf4f78786c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11233115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab37df2855eca790cae2210679cf19d2cd500711763f34e27e96457f94bd5443`

```dockerfile
```

-	Layers:
	-	`sha256:a44fb1ad53fb46f238cd41cdbf9e73f856cddbfe38b413fae4ab59d742e7865e`  
		Last Modified: Sun, 16 Nov 2025 02:19:55 GMT  
		Size: 11.2 MB (11222942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0286d27df1545172590686091e5f29557fc81ed375627154c90e127b28cb7c1a`  
		Last Modified: Sun, 16 Nov 2025 02:19:56 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:58faa693b377ff619627b20f8a6822c289a622640683e54b80b955faf411819e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253131221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533f224a0c4a090034e9c1c77910591ca8644d3f264c3b3b1469e5c850515e15`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:14 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:16 GMT
ADD file:f7335d462150d31c3c91b13ccd3e927bc9a1b9c6664fa8905ccf68bbe3d86cd3 in / 
# Thu, 16 Oct 2025 19:25:16 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:08:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 00:16:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 01:37:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7d5b0205a5ff16c2b58f20a113b5eb9a80393a644df077beab5d90635153dc66`  
		Last Modified: Thu, 16 Oct 2025 21:17:39 GMT  
		Size: 29.9 MB (29907597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bc6628c4bcc52088bb0b2a5b754dc3a6759ce5956477d6cb69c43c846d8e0a`  
		Last Modified: Thu, 13 Nov 2025 23:09:20 GMT  
		Size: 14.9 MB (14938418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54c83b7a5887c6296a2f898823fd447603b8ba6c4190834f6539d38f5acc91e`  
		Last Modified: Fri, 14 Nov 2025 00:16:44 GMT  
		Size: 46.7 MB (46748115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96199adc425f0739fef48bcb825398d0bee1686192bce268cca838436c8ca095`  
		Last Modified: Fri, 14 Nov 2025 03:22:44 GMT  
		Size: 161.5 MB (161537091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ea0294a76a11e06bf84f9a657525bc7a4ff3cf474ff41dddd7338893b4b64e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11083689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff4d36e9f8ff2bb205d52cf8e21fa71a6a52ca45e4abf2c8177c6cde9337f44`

```dockerfile
```

-	Layers:
	-	`sha256:7849f0f31e2ba5129612d75996615089402c5edd440d31936a0f8acd5e26e2a4`  
		Last Modified: Fri, 14 Nov 2025 02:21:30 GMT  
		Size: 11.1 MB (11073548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fbc773f9d102872da95426f4f2c56ec89d173fcd4c109d9d8e49e4f88734341`  
		Last Modified: Fri, 14 Nov 2025 02:21:31 GMT  
		Size: 10.1 KB (10141 bytes)  
		MIME: application/vnd.in-toto+json
