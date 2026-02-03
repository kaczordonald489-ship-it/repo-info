## `buildpack-deps:resolute`

```console
$ docker pull buildpack-deps@sha256:bc5f8b74d22335e9de520e6b906a2e74874919142d644fdecb17b3bb6906a173
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

### `buildpack-deps:resolute` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4ce5387b8265b1f09c5f792209e3697a170439565dde25b7df356c4d645e1b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272860700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4e3abf7ee4bf856cd276b6418fb2052ed3a866c7a2b3fb8078e5b08d0f0223`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 06 Jan 2026 16:11:45 GMT
ARG RELEASE
# Tue, 06 Jan 2026 16:11:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Jan 2026 16:11:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Jan 2026 16:11:45 GMT
LABEL org.opencontainers.image.version=26.04
# Tue, 06 Jan 2026 16:11:47 GMT
ADD file:3beef3c47f24f3196246a7dbc25d20ba42394f35ed72b8ba8b86c3d4d13a83f2 in / 
# Tue, 06 Jan 2026 16:11:47 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 23:06:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 16 Jan 2026 02:49:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f784408d7713470603ec446172f85c9a5ae57032b804583cc37631eb6bb6b75c`  
		Last Modified: Tue, 06 Jan 2026 17:09:06 GMT  
		Size: 33.7 MB (33726347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2773b72b93134db036b076a720d2feda581b3d29f4f2c5877e3beb834e1bf3`  
		Last Modified: Thu, 15 Jan 2026 22:11:06 GMT  
		Size: 19.5 MB (19487730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8f410391db24d0e4edaf07c5f57cc1f57b7b6bcfae71d358ae20e9ec7591f5`  
		Last Modified: Thu, 15 Jan 2026 23:06:49 GMT  
		Size: 48.2 MB (48192868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ed9c3ce80365c11e39ca416709cd12a6a23e6b336e6405aa8c757d3f157d7f`  
		Last Modified: Fri, 16 Jan 2026 02:50:06 GMT  
		Size: 171.5 MB (171453755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e05102146fbb7fbd78805fe2e305e50b392dfa71520e7807b926ac55471d71cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11689823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a83b4a47aac26c51e64a5731aa71f2003e1e301cc510a58f1e35a9adb9ae3c`

```dockerfile
```

-	Layers:
	-	`sha256:e698b321dc731a04b80c90d3f858f09a1a183b8ea2ef9fc2d91dc516c094379f`  
		Last Modified: Fri, 16 Jan 2026 02:50:03 GMT  
		Size: 11.7 MB (11679664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1eba4581e64e1f88dd152f23be75841e775ba386925f708b9af1e05f8c0c74f`  
		Last Modified: Fri, 16 Jan 2026 02:50:02 GMT  
		Size: 10.2 KB (10159 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:76d60c02eea8d0bffe9116312b486d7d62cf47b860f703c0fc54941e4f6e5d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227562699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc8a119a2d3715c5b2625400b49cbf5ff20e4f192d2b341398b89318aceb3e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 06 Jan 2026 16:12:47 GMT
ARG RELEASE
# Tue, 06 Jan 2026 16:12:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Jan 2026 16:12:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Jan 2026 16:12:47 GMT
LABEL org.opencontainers.image.version=26.04
# Tue, 06 Jan 2026 16:12:52 GMT
ADD file:2badcd83b204d640ccedc4ace52673007514f420a84bd8c139cdf292ab0fd3e4 in / 
# Tue, 06 Jan 2026 16:12:53 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 22:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 23:28:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a9ee0a3989db9dc297303b58491eba6d69952baa6b2827fc54ee64ce18e07032`  
		Last Modified: Tue, 06 Jan 2026 17:09:22 GMT  
		Size: 31.2 MB (31161903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afba882eabc4fb690fa94f15129818fcf2958502ce348f72e1f4978f4fb0a975`  
		Last Modified: Thu, 15 Jan 2026 22:07:55 GMT  
		Size: 17.8 MB (17784528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e787e849e38a2c06b825e1d0dc7a2ac35b36e530488241b0cd53030551589a46`  
		Last Modified: Thu, 15 Jan 2026 22:35:22 GMT  
		Size: 50.7 MB (50699858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c60a3745aea0029daeac7dc9464a0a54de49ff5a90c0e01daa6645af99d12e8`  
		Last Modified: Thu, 15 Jan 2026 23:28:40 GMT  
		Size: 127.9 MB (127916410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:980716e8637414ba224406a03157de07f5432a1682ed642dd0ecbc042ed5fe72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11430784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82fa41577aa4f2af7517af4575470fc0e0248461c507d109c8c3cd8d158a3fab`

```dockerfile
```

-	Layers:
	-	`sha256:0df0eb80c9c69a19ce24e85da7206c23c83b6e1f8a7122aed54ca9996ac1e639`  
		Last Modified: Thu, 15 Jan 2026 23:28:38 GMT  
		Size: 11.4 MB (11420560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e8a21dc38d39102ebdff5ece344e381566611febed05347ace3b290db2aa65`  
		Last Modified: Thu, 15 Jan 2026 23:28:37 GMT  
		Size: 10.2 KB (10224 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f0901608cb7ad8b87614a2217ce905f32d37193e11d70ab283761bb995ec959f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.9 MB (261903528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a0201004860c63e3e40c391979d295553ecd3974cabc13cbc45e1f4e59be43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 06 Jan 2026 16:13:27 GMT
ARG RELEASE
# Tue, 06 Jan 2026 16:13:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Jan 2026 16:13:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Jan 2026 16:13:27 GMT
LABEL org.opencontainers.image.version=26.04
# Tue, 06 Jan 2026 16:13:30 GMT
ADD file:0380efe36c0196e2c2ade7e5f2cca6433adfd8d1710d937744979e52eda4b70a in / 
# Tue, 06 Jan 2026 16:13:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 23:12:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 16 Jan 2026 02:34:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e2404e3282be0ee5ef4dc11f1068759836b240597e5a2df39be9b0eb4f3aba04`  
		Last Modified: Tue, 06 Jan 2026 17:09:14 GMT  
		Size: 33.3 MB (33273501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bb422c70ec76440334ab3551c565c88bff89c2dddb0e89e2997bda52f8846f`  
		Last Modified: Thu, 15 Jan 2026 22:10:43 GMT  
		Size: 19.0 MB (19028324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fec8b38941860e9735baae5103376c355a6ad7f7142b648b4bd886f11a27a94`  
		Last Modified: Thu, 15 Jan 2026 23:12:57 GMT  
		Size: 47.9 MB (47853057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afb8bc6cb22c239854dc7f730cec84ad1bcbe0db7c030aac422722e8193796e`  
		Last Modified: Fri, 16 Jan 2026 02:35:18 GMT  
		Size: 161.7 MB (161748646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b1b07d3ffe1b019546bd6adfdc42055ce15fe2b6964d77d0e2854043aa04940c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11744077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913ff669b8a1f455e91bbcaf75d7587df5eb89bee9a1e14e534be435f595b9e1`

```dockerfile
```

-	Layers:
	-	`sha256:fe85d6360636f5eeca6e2ce92c29f376bfbf35c2492d763d4e1cc87091b92f9e`  
		Last Modified: Fri, 16 Jan 2026 02:35:15 GMT  
		Size: 11.7 MB (11733838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2b6df93d70a7e46c87164f0ed3c3621dad76e4477a217e5b4b14bed0ba31224`  
		Last Modified: Fri, 16 Jan 2026 02:35:15 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e31be3c951122875339641ea12ee776155e0c4f9ae681717f4c76e4d8a4c344c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.8 MB (282828281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f87091655a61bec5cd86ccb94155325d13a1f8a1a455980ddee4e995cae4f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 06 Jan 2026 16:14:48 GMT
ARG RELEASE
# Tue, 06 Jan 2026 16:14:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Jan 2026 16:14:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Jan 2026 16:14:48 GMT
LABEL org.opencontainers.image.version=26.04
# Tue, 06 Jan 2026 16:14:52 GMT
ADD file:7ec9d39d1fd01988d51557953b0733de4e61b4fa324869a68521dfd338f7718e in / 
# Tue, 06 Jan 2026 16:14:52 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 16 Jan 2026 00:28:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 16 Jan 2026 04:25:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8dc6edd0e713b64ebd7f5a4fb903e2ab2bc713a37543e118356f779bec06e387`  
		Last Modified: Tue, 06 Jan 2026 17:09:30 GMT  
		Size: 38.8 MB (38811703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2a9a9613d4b4de22dc7933a7a061b9dc4f14dce73e75f090032381eac28b4f`  
		Last Modified: Thu, 15 Jan 2026 22:09:25 GMT  
		Size: 21.9 MB (21931701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cd4f3b0a52ec5238fb2f82df00b265971511e09a4dbfa4c444765523ac69e9`  
		Last Modified: Fri, 16 Jan 2026 00:29:12 GMT  
		Size: 53.8 MB (53828470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255231781f9426352b1558638cde45ec6d7229331cb10880b8e820c923712ec`  
		Last Modified: Fri, 16 Jan 2026 04:27:12 GMT  
		Size: 168.3 MB (168256407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:928db2466d9ec3b0793077bb80a39d735a262cc0ea83e34aa32eee10244f3b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11662415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec0da06914beebb7a7607dc35487019d017212ed630571d91345916a759a0717`

```dockerfile
```

-	Layers:
	-	`sha256:d95db644aa6dd648af5c6fc7bbba6a148d4151029af68ee44de1ff2c498fd451`  
		Last Modified: Fri, 16 Jan 2026 04:27:06 GMT  
		Size: 11.7 MB (11652223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0858a97e93c12e51774fe5d789a204e78ad9f5e1b87f608eb4ee53552cba8864`  
		Last Modified: Fri, 16 Jan 2026 04:27:05 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:82ce5450420248246ebd8463f4e883daaf88dd5ba382a803b009f7e5d545df29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241575223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c043265394b231cd35e3f2e63493f0fc50124fdbec848736c2b26126f3651023`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 06 Jan 2026 16:12:54 GMT
ARG RELEASE
# Tue, 06 Jan 2026 16:12:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Jan 2026 16:12:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Jan 2026 16:12:54 GMT
LABEL org.opencontainers.image.version=26.04
# Tue, 06 Jan 2026 16:12:55 GMT
ADD file:9266e4011fb5ad8a3df9e390fc8165ed1fd44560192a8470907993912a77df90 in / 
# Tue, 06 Jan 2026 16:12:55 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 22:46:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 23:34:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f779d014bea281c13f5bd15e791164db36f27117b06bcc6a0832c49e20ca6c3f`  
		Last Modified: Tue, 06 Jan 2026 17:09:45 GMT  
		Size: 33.4 MB (33397954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66829f85ee6a4ac10cb285e12e8d836204a87759cfb752c0e2b65010651a3b0f`  
		Last Modified: Thu, 15 Jan 2026 22:06:38 GMT  
		Size: 19.9 MB (19947648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00ffb09829df0d3df34b27f7b2ec620dde52eb10796d930fa7f7a852d0ed178`  
		Last Modified: Thu, 15 Jan 2026 22:47:12 GMT  
		Size: 49.0 MB (49048827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb9bf8b30164b2679272d12502f081a0a0a0b4a9c65b4b9172bf619397046c5`  
		Last Modified: Thu, 15 Jan 2026 23:34:56 GMT  
		Size: 139.2 MB (139180794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:83007234cc1538df42015e21c188462f10d89976951c35c932fce7c2e8a0c8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11464717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4304bcbf9bdbf833f5159eddf7ed22c8ddfd42dc14fe72164e5c65070f79a163`

```dockerfile
```

-	Layers:
	-	`sha256:8c40a5082b2435bff849fc7b3d0f631fdc2d3d34802fa3f6dbe2501744821319`  
		Last Modified: Thu, 15 Jan 2026 23:34:54 GMT  
		Size: 11.5 MB (11454557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76b848637ee36ea5fc1f5a6332da887545e53b7311c10d3cc1530f064a783dd8`  
		Last Modified: Thu, 15 Jan 2026 23:34:53 GMT  
		Size: 10.2 KB (10160 bytes)  
		MIME: application/vnd.in-toto+json
