## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:1f0cc53eb0bffa1ea9a9bd1bcd58cffff2fee3eb71a53aca1aaf7389a4332402
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

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b49b93348b6d92983ce9aa729f59867fddb8dc08dda034b86452d34d4b84a895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.2 MB (348175147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a133db6d304e7e8a8ecacad7c551a1c488501453995f434960961238b92adc80`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:17:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:cf0d05af547976908822e26949c650e99fea79152721cc84f93278fcedf70faf`  
		Last Modified: Tue, 03 Feb 2026 03:29:13 GMT  
		Size: 68.5 MB (68514183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e03892a9aa640971f201de20b44c103d86d1ac07d61ceafca3aa4141de012c`  
		Last Modified: Tue, 03 Feb 2026 04:18:06 GMT  
		Size: 203.8 MB (203780145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e11f53185d2e290e4a99626da596b5900fa5fcd6c50a8f6ba86899a621a515f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16371796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0b236d0ce73d003320f4829be1d8d04c4d54e26edf9ee3666e4524973006b2`

```dockerfile
```

-	Layers:
	-	`sha256:701ae10dc402d150be82b074fff073876a9c8f2894639cf1a08a6026857d8c7b`  
		Last Modified: Tue, 03 Feb 2026 04:18:02 GMT  
		Size: 16.4 MB (16361663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec44fa280e4e33940b5af512052e2cbbd02d6d2e884576abb9d74cba26418dd8`  
		Last Modified: Tue, 03 Feb 2026 04:18:02 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3666d6b9948525fb4f4ff4ed4d123228ca266c698a466e234b168a459e2b34b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297054891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5feabf53567bfe4dff7ac0db6846f14b151b11b5322427ef172ff896f06406`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 03:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:00:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:21:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:426290709456e99fd9663e54c2566f480e6c006819bb369d8169614f425f8cd0`  
		Last Modified: Tue, 03 Feb 2026 05:01:01 GMT  
		Size: 63.3 MB (63348709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d19cda7502ce7d0fd94cec7fcb20dd7a225ccefea8bc300fbe5e2eb243d69d`  
		Last Modified: Tue, 03 Feb 2026 05:22:35 GMT  
		Size: 163.2 MB (163174288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:009f1cc7b6126dd0d575c13ac08dd87160704b5d136cb73b7f8a4273004d8171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16127541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a43f526d199147ecf9d491b02ba4da4793abdce6eb6d59dabddd30fd0c12363`

```dockerfile
```

-	Layers:
	-	`sha256:3241060ce0e3c0f48bed5c8469fe102f671afe93c9b930fab25d23a2d9b02b22`  
		Last Modified: Tue, 03 Feb 2026 05:22:32 GMT  
		Size: 16.1 MB (16117344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8cad22d8eb05d84e2378c67b0592a1e3528ab3ba28dcfd90c2a69978258fb3`  
		Last Modified: Tue, 03 Feb 2026 05:22:31 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ffbb372e2e9174e69afd1da82947276ca6994a8c74ddd88624ddc91a8224e4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336942940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e2272b72960426c6ee40c5cbd1d9210ae27f4437d7f5ca7b9d5d906f36b94a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:45:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:21:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:af30714032e2382907ddbc5aecb4821586709d9c81d8af4a66dbe020f5684a50`  
		Last Modified: Tue, 03 Feb 2026 03:47:29 GMT  
		Size: 68.0 MB (68012476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf55203b5e22078fee7d8bdbb9b04739095289e37291516577680ea1550d92d`  
		Last Modified: Tue, 03 Feb 2026 04:22:11 GMT  
		Size: 193.7 MB (193728137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d57fbb6d43fdc21cd4762643df0ec593a825ea4fa7180f4dbd9dde4066f09ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16460811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265864f1c034eab377c22f3a6dd9b030d6909a17801585c15dba0b1ffee4f289`

```dockerfile
```

-	Layers:
	-	`sha256:3b87a184242cb4c7aa8e396c468515e74ae26b71ed80e532488a9e2fb22d36b7`  
		Last Modified: Tue, 03 Feb 2026 04:22:07 GMT  
		Size: 16.5 MB (16450599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22d84c3ea64417ac0ad235cd9cf828737e72056749e93caecbf0ecd717211fbb`  
		Last Modified: Tue, 03 Feb 2026 04:22:07 GMT  
		Size: 10.2 KB (10212 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0a7386521262123b9aeac9d2c8243fd9535d3d6d64af25bed4a9d59398571aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.4 MB (355443046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6faea1893f6c11a9ac2dc0f03a111637f2699e9018c52f976b36a600f85fc1a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:49:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:24:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:17:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:b1e21dfd05a9933736cac3a0fa23af6c2a987f95689861f9fa8728170cbee56d`  
		Last Modified: Tue, 03 Feb 2026 03:25:19 GMT  
		Size: 70.5 MB (70467162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bae46d4f0f5b4b9e59c5e970eda10a9c48de40700c784c888772d6b92412a38`  
		Last Modified: Tue, 03 Feb 2026 04:18:18 GMT  
		Size: 206.5 MB (206500631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2c771e871eb15f1e4248a6eec386fe6cd7b39bc663c72c38d3bef7c8759c09b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16341461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7134d01ae02f6b1e10151af4ff730dbb977e8724166634389fdf89993837d9e5`

```dockerfile
```

-	Layers:
	-	`sha256:0876a3733755a702fc3c6d673e86787a6b0b40a181f9749a077d1e535f61a060`  
		Last Modified: Tue, 03 Feb 2026 04:18:14 GMT  
		Size: 16.3 MB (16331350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d26fd6c432da99459a92fcb01511e9e6eb0c46ce665b1952bcc3cfff14ee219d`  
		Last Modified: Tue, 03 Feb 2026 04:18:13 GMT  
		Size: 10.1 KB (10111 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4383467c27bfafbf668b1db595690f03b5bda878f9d61f76b94cda63ce7413bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.1 MB (348116515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37a642ed1bc3fe4142a6a0f01b78ffd7c4121e173f5b1709a051b69d12f4aa0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1768176000'
# Wed, 14 Jan 2026 00:58:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 14 Jan 2026 03:16:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 14 Jan 2026 04:13:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3fc9cd4fe16c3d17cfa9014c31678a58aad75101c0db66189ea08efe999c1a84`  
		Last Modified: Tue, 13 Jan 2026 23:17:49 GMT  
		Size: 53.5 MB (53525434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a197399fa4447d8fa115804ab3b4e02dac8c91312a2de42315098f7ba5379933`  
		Last Modified: Wed, 14 Jan 2026 00:59:10 GMT  
		Size: 29.4 MB (29433893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af34eae56a8f267779d2b4c803a11c3bf71c8a6b9f9a6e12fa12e1722fb4de21`  
		Last Modified: Wed, 14 Jan 2026 03:17:05 GMT  
		Size: 73.9 MB (73938015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5911b038d6e717ed090f9c3461176abfa8af2214f72883ede5a8a73f2ee77db8`  
		Last Modified: Wed, 14 Jan 2026 04:15:00 GMT  
		Size: 191.2 MB (191219173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:534c0f4ec0f12e375a4bb13519ab4dbe6eb4d2d31886f03b4eee924fa711f959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16275956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69829c7894381b8ec3a31a0402526db085ac23afaad5be097a9e691e88fbee4`

```dockerfile
```

-	Layers:
	-	`sha256:f04b2d384e59ed7b9e832d47850f339a57a0bd2585811b19c7bd3bd07b7bf8ca`  
		Last Modified: Wed, 14 Jan 2026 04:14:56 GMT  
		Size: 16.3 MB (16265791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc97153f6cee8fead45aecefffaf7471e1a046ae7f6c130d5f4e5f48942c94d`  
		Last Modified: Wed, 14 Jan 2026 04:14:55 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:fed2e5766c7d55e23771aedc15304dfe5d359ca3c30e7b149ba6ddd61a226c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.4 MB (465407805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ff52b546df7fdc132301f66048354296c1ca9ce73872cb9c607edb52ba654d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1768176000'
# Fri, 16 Jan 2026 06:44:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 18 Jan 2026 22:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 Jan 2026 17:24:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:31a0580cd9ebbfb97fab4dcf3377298f60d306bde5f9bd366da5bb180e819879`  
		Last Modified: Sun, 18 Jan 2026 22:55:43 GMT  
		Size: 67.2 MB (67240639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9ccc9534909fd77b425b0e312766b60b733fb8aa1b2883ed123ecc58b9b58e`  
		Last Modified: Mon, 19 Jan 2026 17:39:45 GMT  
		Size: 324.6 MB (324571129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8eb975f672c1bd39d95dc03b5d1b113593ab7905aa4891800136552591a7f2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16414802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98fe0197c7fdd1454b3976636a6c48fd04b03c825628cc7394fefe4f107c8e2f`

```dockerfile
```

-	Layers:
	-	`sha256:c8bc201c125faac0cdc7070aa7c7b5bddcdd6dd215d3143c0d49422d006b52df`  
		Last Modified: Mon, 19 Jan 2026 17:39:01 GMT  
		Size: 16.4 MB (16404637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f37a5d0cdda8ee34dbdc85bc37c348c7e68b1bd128379ede68ff60bd057da49d`  
		Last Modified: Mon, 19 Jan 2026 17:38:56 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:be162ccf02d71fbbd14582ab3609944f62d4f8695e96c2d7645bf16853dc0ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315736464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36cf126f747e326f2bff9ae95b68602064ec505b5c210488dff0e889d015914f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 03:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 06:14:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:7903e028f5ff83b35a3c307b4e4b9628f0b8429f5ab23010d2101829884a6eeb`  
		Last Modified: Tue, 03 Feb 2026 05:29:41 GMT  
		Size: 69.2 MB (69166722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4aa7c665631817fd69fbb1273f3acc4812270df409f2328ff6218de18832430`  
		Last Modified: Tue, 03 Feb 2026 06:15:30 GMT  
		Size: 171.1 MB (171148813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3b9e16943bd95fe59a3bba4d1b03b2be0758e22eecb0783f785b40362b771e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16144088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baee110c81065679e12eb3d5cc74ed04848a41c664d0a45fe4046dc694f56a8e`

```dockerfile
```

-	Layers:
	-	`sha256:541cc9c25fb9069341e04cc8862898dd403395c943b03a4f4b3d885db82b4f11`  
		Last Modified: Tue, 03 Feb 2026 06:15:27 GMT  
		Size: 16.1 MB (16133955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0449f3641bb0878155226784c40778b28bd307dc98a6d2b9159085b2f1cc276`  
		Last Modified: Tue, 03 Feb 2026 06:15:25 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json
