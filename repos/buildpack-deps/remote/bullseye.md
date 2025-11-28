## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:aebe8a3e652fdef3ec477e9a1c36c1bd9f57509eaf5e15c8db921e35e423cc10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b8a0e6f52c1f4f9cc2a6531860e92515d8dc3fd51b00bf74e97340925f3fbbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321480897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699366889cdfe765002698b71427e172ad3a42b9c9587338860b961aa011618a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:10:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:22:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5b6134fa8a3ac5c0189f873bc3e294ab88c8b51487dbaf69fa8590338d4f47`  
		Last Modified: Tue, 18 Nov 2025 05:10:17 GMT  
		Size: 15.8 MB (15764186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01293af2d4fcbec34a6cc04059bc54793a02a3f35097767fa8f319055caf4917`  
		Last Modified: Tue, 18 Nov 2025 06:38:35 GMT  
		Size: 54.8 MB (54755074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da21e19920be3ae928a2305b1c12e689cf00c96a0099d81973e3b18f90828fa`  
		Last Modified: Tue, 18 Nov 2025 11:14:46 GMT  
		Size: 197.2 MB (197205206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:535cc72328c940faa1a3b8c1e50d514b63b12d03444c373f2e09ac9472d394c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15472367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1eeed1cf21d7b758c3c6bf37d4208ab31b224a875ad7658807fb71b9f64d2f`

```dockerfile
```

-	Layers:
	-	`sha256:3b8db8e61e03c183ede6f602e5f7682747531688c45a7d1777722809b9db14ee`  
		Last Modified: Tue, 18 Nov 2025 11:20:49 GMT  
		Size: 15.5 MB (15462172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2d531473aa256973c789a506ef36b4923f426025627e67f54ee0bf673d75852`  
		Last Modified: Tue, 18 Nov 2025 11:20:50 GMT  
		Size: 10.2 KB (10195 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5a772830cea6a52b85d6284f7e1a5d747c53fdbc90181032c0e1a9531d45eb78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.5 MB (282530947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84c4bc6c9c3dea17f74a72bf0a6d2ab138cf8afe60e66f37ef7de14dc44091f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:57:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:27:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:22:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:516616c63b11e5af36116ed0b70c230c2287eab3b74b11a00eb299cc4575af64`  
		Last Modified: Tue, 18 Nov 2025 01:14:16 GMT  
		Size: 49.0 MB (49046365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2280342788a66a44d1f2e4bd1eaf8389d9bef9428e09fa0ae948652bfaeee4b8`  
		Last Modified: Tue, 18 Nov 2025 03:58:13 GMT  
		Size: 14.9 MB (14879454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f566f1ab80bd353b42ed837b52fe4ec496dfff10630b53797d35c9eb72bc27`  
		Last Modified: Tue, 18 Nov 2025 05:28:17 GMT  
		Size: 50.6 MB (50629469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae163b8147549b72151eb921eaef5a03a6a925fe675fbadbf871e2bfc1097c32`  
		Last Modified: Tue, 18 Nov 2025 07:35:47 GMT  
		Size: 168.0 MB (167975659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d8f6154508cf8b0113f9bce86522e4d3e3f4a4051c2d754d8811246a11fea02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eedde2be4b647bb59585487e7098dbdf2e356f74a475f0d7e6c74771b3b4590`

```dockerfile
```

-	Layers:
	-	`sha256:9dd18b1fe2c941a444a632347aa4a0eeb153ad5fadc956bc7aaa9c0ff4bec162`  
		Last Modified: Tue, 18 Nov 2025 08:20:43 GMT  
		Size: 15.3 MB (15261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a537d729a48dccb830b83fcaa27a4018deefc2d3cd581717159a7331690124`  
		Last Modified: Tue, 18 Nov 2025 08:20:44 GMT  
		Size: 10.3 KB (10259 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:838fb83000d4a50402f612e5a9234170fc27bdb895f621dc28a525d4507ea3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312974997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b8c5cfcf4d82e8e3df4812f3e6d8d32f7629a784703747a547bc7410a57e8be`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:23:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:14:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 08:17:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf5c6e26abbf2d346305acdea26f4c77227ae8be9882711816b29b75df95827`  
		Last Modified: Tue, 18 Nov 2025 06:23:37 GMT  
		Size: 15.7 MB (15749561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cbea18607285d70f010e2ba402394373534fadffb00b880a34f03b4cba581f`  
		Last Modified: Tue, 18 Nov 2025 07:15:27 GMT  
		Size: 54.9 MB (54865154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195c5566d8037d8b54b239588b83dd1faec060ba39679db65c2b1da016b183c1`  
		Last Modified: Tue, 18 Nov 2025 09:10:52 GMT  
		Size: 190.1 MB (190102587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bc7356b21ab2d1bf04fd9f80818394e8a355a33033129ae8275e42264cc20ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15474392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd6b3e253ec9373387b0b6a2565e048fcac1c0459e544040a64bbdd1be070b0`

```dockerfile
```

-	Layers:
	-	`sha256:9de2d683504cbc09e916d1c4de83c1eed1fff62b0909c1e3326f1744f7fbdbe3`  
		Last Modified: Tue, 18 Nov 2025 10:42:48 GMT  
		Size: 15.5 MB (15464117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:686a859bc0ff914f42129a880339c0edbc259189364a9e50ccdd35c5c6c9b25d`  
		Last Modified: Tue, 18 Nov 2025 10:42:49 GMT  
		Size: 10.3 KB (10275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3695555f1eef2580134d09056f5e7f37d7594b47576e608afbd6c8a7632077ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327119815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929a8dfebe2ed71a50932f6e9b06dc02300fe370e975faaa53895e8b5ebc972f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 02:56:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:09:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:17:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ff276d829f31f5253bbd1b7f53ddf75bfd6004f7fcc06ea8ad1b23a242b12d3b`  
		Last Modified: Tue, 18 Nov 2025 01:13:28 GMT  
		Size: 54.7 MB (54699599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91162d93e41e901767fb0ecc9c7694fbbb7b80a5384451f5ee29e2889d7672be`  
		Last Modified: Tue, 18 Nov 2025 02:56:26 GMT  
		Size: 16.3 MB (16267715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d157624c72b4d56de915d1a1b7dc5753760ddee0f8443f1fea29deb51353623`  
		Last Modified: Tue, 18 Nov 2025 04:10:00 GMT  
		Size: 56.0 MB (56048948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacb42e4f564ea211f0c952153987cf04f1026b7ff7de4c09f7bb3a8688b84ef`  
		Last Modified: Tue, 18 Nov 2025 06:21:07 GMT  
		Size: 200.1 MB (200103553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8d8d1eec9b54e560680555990571751f142bc9ed3601d0e31c0af1759045ded5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c889a8900669783c1f25142e0266e78fc93b964966681c2f9fc74093f95451`

```dockerfile
```

-	Layers:
	-	`sha256:1a6b59e9d486f747bfcda7b9039a520a0f5f634d263233fedbdcb455edcd3bfe`  
		Last Modified: Tue, 18 Nov 2025 08:21:02 GMT  
		Size: 15.5 MB (15450187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adc4820f6845096ad608b16dcc002eb5b7f8039c464abcf5733acbb04f21d250`  
		Last Modified: Tue, 18 Nov 2025 08:21:03 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json
