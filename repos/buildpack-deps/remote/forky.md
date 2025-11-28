## `buildpack-deps:forky`

```console
$ docker pull buildpack-deps@sha256:ef09d8a61d14ccb40874982a5e7fd44244f10d439c1b110010db2b905eea5a2b
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

### `buildpack-deps:forky` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:91b41191b494a1b9e62364b51f72bee2aaa4a94c26206a82f8ef781af00864f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343241892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14a77cc65a813a9f91f29177ba0364e4332878834729d79cedd3ff2289623e0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 05:10:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 10:25:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76694dc296168bbffa890c84fb372e9c250bf33e0ad63a6146b169a57d983e2f`  
		Last Modified: Tue, 18 Nov 2025 02:29:31 GMT  
		Size: 48.5 MB (48500434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cde0e5673dcde1a0a75a6006c0aa8bc722df9feeb622b9a6bf212e2f178a04`  
		Last Modified: Tue, 18 Nov 2025 05:10:46 GMT  
		Size: 27.2 MB (27217534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2932c8b98dae86ed0b1c8a1e3e5c71392f9692dc656a3abbb9118c188f27292f`  
		Last Modified: Tue, 18 Nov 2025 06:38:41 GMT  
		Size: 68.4 MB (68399882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b66fcc9027d1f0a63ef99cb7a3bd581ed110e9921145bee6e6369da1eff7006`  
		Last Modified: Tue, 18 Nov 2025 14:29:53 GMT  
		Size: 199.1 MB (199124042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:67d7abcede767762c87b12e5b47a7664bf03d5cee80955da4b3060a1f10f8c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16262128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a783ea0d7537735401c5e059c95466719ef12d76a7c50dca98479dfb512e1c`

```dockerfile
```

-	Layers:
	-	`sha256:5626d4d28fdf088588b5ecf4e495cf082d5b78836805eada5318101d35ffeee0`  
		Last Modified: Tue, 18 Nov 2025 11:20:58 GMT  
		Size: 16.3 MB (16251984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68c5b134f81ce6f50ac745f20892a3b5d8e236653ceff956d4e4e2a34c9b6075`  
		Last Modified: Tue, 18 Nov 2025 11:21:00 GMT  
		Size: 10.1 KB (10144 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:41b4680dba08ee5a9c065f037606fa86662abe1908ccc441796e2ff95437e9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291474151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f544d724c61e5a226eccc2520a37442bf55466852471f0c151a5589301df8a81`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:27:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:22:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1dd1fa3a56d87bf4dcae80a33b02589ad31d81e866bca9f061ada67db33c8854`  
		Last Modified: Tue, 18 Nov 2025 01:12:58 GMT  
		Size: 45.0 MB (45003762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6f4451a2be0f51c6d1714f46485883bd5db54f8b6d9217e249d632dee61a5d`  
		Last Modified: Tue, 18 Nov 2025 03:59:12 GMT  
		Size: 24.9 MB (24945403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e16a5a4071f52927a7f28d9d0587c256392be28c985fb8945c4f1d6790bca96`  
		Last Modified: Tue, 18 Nov 2025 05:28:19 GMT  
		Size: 63.3 MB (63308752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cbe5c11882528e8f9627e30208203a19d58c8da1755066a995908bfead1e66`  
		Last Modified: Tue, 18 Nov 2025 14:29:43 GMT  
		Size: 158.2 MB (158216234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ad7538cc80c3f08de34467d17ec74f1bb4773271874a25a8f1bdbf899fde8c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16019141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a297ea6b8f073ce53515a4bc042d3c782f47c2ef46958c0b4ba568ec3c7e1495`

```dockerfile
```

-	Layers:
	-	`sha256:3bec70ab8801ea2d5ac8440779cbdca55495b13ff32f95131ae60a0e1eba656d`  
		Last Modified: Tue, 18 Nov 2025 08:21:22 GMT  
		Size: 16.0 MB (16008932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c54f300edca5a0f2d5926e6a07a200c66ad69af8df767d48c9067d6b19788e88`  
		Last Modified: Tue, 18 Nov 2025 08:21:23 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1776c548eeabcb2088d0907306330c6d3d50067fb9ecd558925cc693ca52607d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332322565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9ef9ef61cec08b0f508e8e918e043be0928c452dd03200a8587f5ac21f2a6c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:25:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:38:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:33:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:25dea15c4ffeb70e1112f1ee06dd948a8ab9dfc3b79ef239cb96080cc27ff1be`  
		Last Modified: Tue, 18 Nov 2025 01:13:47 GMT  
		Size: 48.6 MB (48591184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e989d2e0e09f298fb48c4d6ff3605064bc05169f4e2b9891ccb3261afe85988e`  
		Last Modified: Tue, 18 Nov 2025 03:25:51 GMT  
		Size: 26.4 MB (26444649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d766a3fcd99b3870f8097a1cba056eadc6327b86dc0436d4998b4bd42fba2bf`  
		Last Modified: Tue, 18 Nov 2025 05:39:16 GMT  
		Size: 68.1 MB (68117647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3638c589b2e540bc3e5e4fb95ccf8b07f498d0e3cf8da94b42f3f5e0e1da8852`  
		Last Modified: Tue, 18 Nov 2025 14:29:38 GMT  
		Size: 189.2 MB (189169085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2edd9c2f2cbc79777fa0515fd9ddf7904f4bf05fc4397f4760b7a5f7aaffb85e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16336758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806c994bd8674a3370342cbb654cbbd8d0ca434aa616a449f19f55930392fed1`

```dockerfile
```

-	Layers:
	-	`sha256:99efb76c9dbf3ed90d20e15a944b03d17f1b4c5297006f6633f72bb88690d0f8`  
		Last Modified: Tue, 18 Nov 2025 08:21:37 GMT  
		Size: 16.3 MB (16326533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52e4a833dbe51979fe8c54cca62a2fe4856371b51983d64be2c8cf8d29a4a2c4`  
		Last Modified: Tue, 18 Nov 2025 08:21:38 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; 386

```console
$ docker pull buildpack-deps@sha256:097c5cc87b8af1310d5cef6954026b1466dc10e53793f76b8d91e244d58ca6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351156720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10e362c286e52b2780eeb73e9103f95b6e7a8fde6240460a1c955115f147578`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 02:56:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:09:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:19:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:898cf630ac245ec9ad865c96204520b86bb7b8760d5bd2f14bd02745e43d82f4`  
		Last Modified: Tue, 18 Nov 2025 01:13:40 GMT  
		Size: 49.8 MB (49832238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2307ec487a47570033147c5c7a8c176eb531df9120f57bf768d32ef164c1efb5`  
		Last Modified: Tue, 18 Nov 2025 02:57:08 GMT  
		Size: 28.4 MB (28443569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afe2397c32fb7c8e88a8fb46c9042ce37ea62165c0c00b13dd2c00d1596507f`  
		Last Modified: Tue, 18 Nov 2025 04:10:32 GMT  
		Size: 70.4 MB (70405644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19b951fe881d50c4e7f59c86893ae5fb480ecb4ae291d4f383a9576c8ccd39d`  
		Last Modified: Tue, 18 Nov 2025 14:29:33 GMT  
		Size: 202.5 MB (202475269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ee021964edf9eba055a778cab771675659cad020c02932043a8a548eb6252f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16231886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d85667c0a37ccd6ead9f6169bba180aa8577aeface412664f5a40fcc46e33bd`

```dockerfile
```

-	Layers:
	-	`sha256:2aa944b3c4eef6b5c6b94cd1757d9e2c7eb2289fe8b9380f8917fb831e800894`  
		Last Modified: Tue, 18 Nov 2025 08:21:55 GMT  
		Size: 16.2 MB (16221764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:037ecaf73e4465ab6a14d97f4b024c4e94a377470686363fd9603e0fceea6b62`  
		Last Modified: Tue, 18 Nov 2025 08:21:56 GMT  
		Size: 10.1 KB (10122 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d6fc593ae8b4741ecc8cea0c1248d15fb1dc46575e2507bcf6cb57cf933bca60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.9 MB (347867079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbb1b1fa3b1d8e2efa4a7e445c4d51a9fb5bc5634e48ae7d5d8ac2539e533c7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 16:55:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 22:32:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 19 Nov 2025 01:16:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:56aec8ed2c7425bd4d962ece466e2022cf4900d838eb52bfdf10fe6e2569b4bf`  
		Last Modified: Tue, 18 Nov 2025 12:56:44 GMT  
		Size: 53.3 MB (53334632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2237e36f3e4c10c1103d8ec79492c7f36c02c01d9c3a6f4fce75f5099f037ed`  
		Last Modified: Tue, 18 Nov 2025 16:55:33 GMT  
		Size: 28.8 MB (28835816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa59b5d54bba5249b3ca4ddb8dc710a01ab4a524393b264f4c0040d80e6ca0d`  
		Last Modified: Tue, 18 Nov 2025 22:33:27 GMT  
		Size: 73.9 MB (73870832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00166576592277f6f9005afaf19562b86db3b744ed9cfbe17e4c3d6660c1c563`  
		Last Modified: Wed, 19 Nov 2025 03:18:59 GMT  
		Size: 191.8 MB (191825799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:86673b497443ecacffea5473e3cee3f913c5adb50bea99982366728572d21b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16236306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdd64a164489d7c5edf817a5497226743a4bd519891813d1a4f78f7306f0a98`

```dockerfile
```

-	Layers:
	-	`sha256:c3c6e2c0199b1e9cb5a4503c42800f550518a8133c6286dabfeb4b43394a671d`  
		Last Modified: Wed, 19 Nov 2025 02:20:36 GMT  
		Size: 16.2 MB (16226130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b30d69219094db4204b74b8176a4cdaaec194a06a47ff2cca6e9e2b977101a29`  
		Last Modified: Wed, 19 Nov 2025 02:20:40 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f47c003c173d4114297220ef0bb185cfb50c6fd0b6fcb3419ae5b2bf21352fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.6 MB (447572006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afbcc0adb46d7e348caa0b8c9a04140fa32574c6ec78e4bee56daa98b54e7dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1763337600'
# Wed, 19 Nov 2025 19:29:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 22:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 22 Nov 2025 21:10:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5f062c29e53f6114ba8255e90dca3ce517e3e0563bbe15af71540ba740a9253d`  
		Last Modified: Tue, 18 Nov 2025 01:31:28 GMT  
		Size: 46.8 MB (46806333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7e03bce6d0d0951954641ed6a59e64caf78431003e1f4dc54250fb69de83f0`  
		Last Modified: Wed, 19 Nov 2025 19:31:39 GMT  
		Size: 26.4 MB (26395035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad59f169a4e1e4b9c77d43a5b3ff4ee02106901fff4136734ffd774f5d61be05`  
		Last Modified: Thu, 20 Nov 2025 22:19:28 GMT  
		Size: 67.2 MB (67204332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f9563ee43ebee5e6699d4335551883c7ee06ee797305af6c55c91ccb4c5d8`  
		Last Modified: Sat, 22 Nov 2025 21:29:23 GMT  
		Size: 307.2 MB (307166306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1fe5ad6a12d98808ee12adcbc10b7d86c2e3fc1c8b140b06fb510ddef87178d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16310495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d663d2633452b434ab76a7b39b5adf3183377949820da8f8dba0b0b2f38510bf`

```dockerfile
```

-	Layers:
	-	`sha256:0ff8146e576efcc37335b21d66210c331db3cdc7e5fae668a7434ab5fc59a82b`  
		Last Modified: Sat, 22 Nov 2025 23:20:49 GMT  
		Size: 16.3 MB (16300318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e879c4fb00e06858042fa4dbd1cd565317c3b66cc3cb3db2fd3606c785fa9dd5`  
		Last Modified: Sat, 22 Nov 2025 23:20:51 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:84010350ab56067b5dfa46014ee6b9e4c216760248f7854426e87675a93940a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311510787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59de4189af3c9e9a43931f0afca3330bdce84ad22f23e82bc72225c986e48333`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 08:14:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 11:51:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 15:15:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bb1941d24f39dbf96b6d3045499ee523d7b760b1ecc1834da461428a6b3f02c0`  
		Last Modified: Tue, 18 Nov 2025 07:24:21 GMT  
		Size: 48.4 MB (48370930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f46e464db90bd7a8600e77f0c0366b640edbb2b0782938b210f31a5e2ef6ff`  
		Last Modified: Tue, 18 Nov 2025 08:14:56 GMT  
		Size: 28.3 MB (28338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9c4bf85cad5d8349484042a06ef15142b47542819e7b1d09fa9fc067e727ee`  
		Last Modified: Tue, 18 Nov 2025 11:52:16 GMT  
		Size: 69.2 MB (69183346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faae51b4bd652fa22d80421f0b8ece640fce9558779efe83bb7653fc4f952d99`  
		Last Modified: Tue, 18 Nov 2025 15:15:56 GMT  
		Size: 165.6 MB (165617659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:29ecc6c5e8ab25b50c8b2abebec42287f49089995e023c8209f1e544592b033f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16028792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86bbf3dbe080d0ad3f200fd1ac1f8cc1db7acdfe2727bce406b42ca9a721d1c`

```dockerfile
```

-	Layers:
	-	`sha256:63a60382bf7e3d85ea61cc5d4e5cbbf8f38057bd3243b6a9c6f6c2a4aa3c2b8b`  
		Last Modified: Tue, 18 Nov 2025 17:21:36 GMT  
		Size: 16.0 MB (16018648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a0c92c207d0970b57173a1a76e6cf7242dfa3a7c9e603946fd3f2fd9b79b13e`  
		Last Modified: Tue, 18 Nov 2025 17:21:37 GMT  
		Size: 10.1 KB (10144 bytes)  
		MIME: application/vnd.in-toto+json
