## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:3084807a4d9b04eea7ec6095e8797e327fb415eddae610218d9df96c4972a339
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

### `buildpack-deps:jammy` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4b81340dfaee2f4422505d4d328b1171a825c7a317da94ebda1732299467a066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249058053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a4d00cff0bcd73007a67825025ea3eb33a381cd8332aa9003c4d0c0733fe8f`
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
# Fri, 14 Nov 2025 01:12:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:6cb8d60cc9242e2b1f5b2d3684a03fd52d3e51132e6cc4c28707d6d27e3c01ec`  
		Last Modified: Fri, 14 Nov 2025 02:22:59 GMT  
		Size: 172.9 MB (172928244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:963e95d1a7c07dc1efe7a04ad5beb1f795f910e8598ffa77a6af6fde97edf1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11849710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb9af68654605e59de78db6c3e74d4462a6aa237fe018283ea99701304ec00d`

```dockerfile
```

-	Layers:
	-	`sha256:548c1910d4280a77dd52b34dee8736052d8baa7da1948f3f191c2b06644a4e12`  
		Last Modified: Fri, 14 Nov 2025 02:21:53 GMT  
		Size: 11.8 MB (11839550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37af7cb03f1c85b08fb186c5153294e6d1dc0aa287ee9b245ff47e95b37cbd64`  
		Last Modified: Fri, 14 Nov 2025 02:21:54 GMT  
		Size: 10.2 KB (10160 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:91a2518ed21d54217ee315bebeb8e5a68c67c86aa42678278833f58ce161998c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216285412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e20393e7ac5596002cd7b07971f37d6e6f0f6d672646466d987fdab8360148f`
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
# Fri, 14 Nov 2025 00:25:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:f7c06e700a1c224055f382220cf862287b7adec3ced875b565416517825b8126`  
		Last Modified: Fri, 14 Nov 2025 03:24:00 GMT  
		Size: 140.4 MB (140380189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c17e3d0cb7161e6a6db1624a983a7db527881c95d362483fb777ff092b87150f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11638982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57af8160ab07bcc633f2bacd78663289144b797b0d84fd371e2532969dae9a32`

```dockerfile
```

-	Layers:
	-	`sha256:bd298e48fb77b28ac44f5a412c080e8e4ac96d23407ffb14198b34d09015ec25`  
		Last Modified: Fri, 14 Nov 2025 02:20:08 GMT  
		Size: 11.6 MB (11628759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6acee81c13fa45f8291e744aff0f83f1584b6ea8c70646ceb2b9bcd18e6b4c53`  
		Last Modified: Fri, 14 Nov 2025 02:20:09 GMT  
		Size: 10.2 KB (10223 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6350cb25613c0b0fb5d81dfc218e3fcbbe21805fc990305ea8bc5bd39a10d4c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240295531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d88a7299c72acf4930898c4a077ed53ed1dc526c961b39245e956e3e9abffa5`
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
# Fri, 14 Nov 2025 01:27:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:53ae177613e78424f0ed3fb90ff122d6d62244b029af23e58b5d00f66a281e6e`  
		Last Modified: Fri, 14 Nov 2025 03:23:52 GMT  
		Size: 166.5 MB (166476602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:799058122575ac78d3d864c728650f83778a6e759579c5e5987bf71ecd4df664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11845457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8183a653dcc925bc2e50434652399fcc2b0d622c613e0e68892ae27e70df384f`

```dockerfile
```

-	Layers:
	-	`sha256:8ac873eaf4fe738a27fa6e8b6c005c669b923ebac24dd13fa3a3455ca84b2ce6`  
		Last Modified: Fri, 14 Nov 2025 02:20:18 GMT  
		Size: 11.8 MB (11835217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6583d0ac53bb9760e6eca95caef803428167d061885c89d72ad19048d18d13a`  
		Last Modified: Fri, 14 Nov 2025 02:20:20 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cfbd5ad07520b8dd896916810dfbafb596aaf4305daecbdb8f65fb0c9655ee17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269798659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43424e0836a89379e1c6b0be377da8bd95618665de885643db02f64597c44cca`
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
# Fri, 14 Nov 2025 07:55:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:48ae70bf79f2fe483e6b16bff202ad51526130dec34de2974c429e328bee503d`  
		Last Modified: Fri, 14 Nov 2025 12:59:45 GMT  
		Size: 183.4 MB (183406909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:659ca15014e81212cbd2aa301cea9ea6eea7cd6f79bbf9ff7920aee0ca4fadb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11809107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e6f950220a5a3241a9b1b96be2757eafc0c171fce1a3b652b6287688707c7d`

```dockerfile
```

-	Layers:
	-	`sha256:08507597b66a6b4830132d357ae62432917c4e8fae823f75377212c66b253634`  
		Last Modified: Fri, 14 Nov 2025 08:19:49 GMT  
		Size: 11.8 MB (11798915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cf82ee508784e711b4afabf30a5e020dd3179a70ba077219ea319177f2f232e`  
		Last Modified: Fri, 14 Nov 2025 08:19:50 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:46a58a255ebc09a773f0ba2106b104a7157a57aa86e3ba5541669012b1ee6108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274272061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1d5a386ca4316e44597d8b4a5b47a1b930a2546249c8bfaafa7d51282430e6`
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
# Sat, 15 Nov 2025 23:05:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b5f7cced600f8d6f7406cf88fe979fb4c95a4d3d0d6aab2822c74306d06dcbe3`  
		Last Modified: Sun, 16 Nov 2025 03:28:20 GMT  
		Size: 197.8 MB (197806144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e305b632d893d900799c174b6330c5ec8a5ed67cb9f61eead0c91746d90dc6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11790091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645ee963023dcfd9aafa4faa06ff3405b4b1dd82ec57786d49270ceae98a5f38`

```dockerfile
```

-	Layers:
	-	`sha256:e81e761de2eab0f908a9f4a7b132b4f0dcde3cbd30e6722d994b88d573a0d906`  
		Last Modified: Sun, 16 Nov 2025 02:19:48 GMT  
		Size: 11.8 MB (11779899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc6b7045e773ec5c914a00794bd39c68d01bd17627ed4a6b0b8b084456ecafa5`  
		Last Modified: Sun, 16 Nov 2025 02:19:49 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c91a8e51f18421f9450b6e351c77788e303bd217f68cfa78fd25cf9c6579121f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223017245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e26625e1eeda130643f1b0e22365b8edde469e6fccc2d18a608a43d838a4788`
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
# Fri, 14 Nov 2025 01:37:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:0ef4eddfd758bb399de0e7d09f3f491729e18647900df0b5fd8a608f5dce3565`  
		Last Modified: Fri, 14 Nov 2025 03:23:51 GMT  
		Size: 148.6 MB (148576243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:748b086ed88be3b5073f42d787c8c3f8d092d6504f864100aca5591f9e7134d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11663585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25aeae1b3e7bd3a5058ba43081b74d8561fdaf7479943de1ac8b0ed31755c973`

```dockerfile
```

-	Layers:
	-	`sha256:91d11bb1e9fe6bab6bf8ad43413c17adbc481ff126f601f0845e65c5de2f0aa7`  
		Last Modified: Fri, 14 Nov 2025 02:20:47 GMT  
		Size: 11.7 MB (11653427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6199404d7f1f3e5607d3f86fbe96e6027e251f4bfe5caf5bdb4ac158dc5eab`  
		Last Modified: Fri, 14 Nov 2025 02:20:48 GMT  
		Size: 10.2 KB (10158 bytes)  
		MIME: application/vnd.in-toto+json
