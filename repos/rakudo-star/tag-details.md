<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2026.01-alpine`](#rakudo-star202601-alpine)
-	[`rakudo-star:2026.01-bookworm`](#rakudo-star202601-bookworm)
-	[`rakudo-star:2026.01-trixie`](#rakudo-star202601-trixie)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)
-	[`rakudo-star:trixie`](#rakudo-startrixie)

## `rakudo-star:2026.01-alpine`

```console
$ docker pull rakudo-star@sha256:78a228970ec5e9b42567b9d6da6629b1a49c3f6175f2e7a52b1afdbdaef0b31f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.01-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a5bff11023898fb0a4aea0041a2914ae3088ab11afd6965cb5fa4e8382531b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51337346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9dfeb15cf9dd0010a9ddd7e4938e03a6c544adb4a84edc2b3ebf14219bbe3f`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:03:04 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 02 Feb 2026 19:19:20 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:19:20 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:19:20 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 02 Feb 2026 19:19:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:19:20 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3060884c0be28f953f468c7201d683ba6c0e82dddfc2564c09b2d3b821b4e4fb`  
		Last Modified: Mon, 02 Feb 2026 19:19:31 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe45a1b0764dd266b786344adcb3b4c60c26489d59bdf104692f0849be7c390c`  
		Last Modified: Mon, 02 Feb 2026 19:19:36 GMT  
		Size: 47.5 MB (47474577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:4658d3cab6fd635f2f098ac62c80fcda5ce29fc291cf7e04be980103cf93a655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5115d4e0288db5efbf0f47419b95453d7567d45a1c64368a45ad162f8ed98d33`

```dockerfile
```

-	Layers:
	-	`sha256:cbd4c48955e5af20ebde87c4430550e568b58e1e4da10059a9e7a37b8991b3b5`  
		Last Modified: Mon, 02 Feb 2026 19:19:31 GMT  
		Size: 187.0 KB (186973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd9039c43e0e55fadf6c78efbca2ca8533cfb57e7ac6a2962c6cc8d85aeb6ee`  
		Last Modified: Mon, 02 Feb 2026 19:19:31 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.01-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:e23968cc99cf3d7329dffb6df4a788bbff56e8660ba05b60140cb3dc85415aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51410918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44523c43bffe91994ab0d41cac40b9586c81063423cf08a6095b4b47039f3df`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:03:53 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 02 Feb 2026 19:23:15 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:23:15 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:23:15 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 02 Feb 2026 19:23:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:23:15 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637aa627dfc01bebed15028112f215606ab0f1cd1d25c2a41fdd2ab88fc60530`  
		Last Modified: Mon, 02 Feb 2026 19:23:27 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52008d4f177e3efc234c3aaabeaf66f73e9add81659a303f773a078438c24ee`  
		Last Modified: Mon, 02 Feb 2026 19:23:28 GMT  
		Size: 47.2 MB (47212880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:212cd58719d10575eec5bbc600a315b36c9171b8d70d6117876511f7caa74d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588030a4c73d35971132596be85090e56b1d035c0f1fdc39cabcb3371f47e6ec`

```dockerfile
```

-	Layers:
	-	`sha256:f57e8b7aa80eafc12962eb9f7d1a3d01a9e49ce3dd50381059874a3017cd2e83`  
		Last Modified: Mon, 02 Feb 2026 19:23:27 GMT  
		Size: 186.4 KB (186355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ee180b9438495f5dd822ac0813970d7a53c6fc36cc9b2cf00d14ecfa17f2b9b`  
		Last Modified: Mon, 02 Feb 2026 19:23:27 GMT  
		Size: 11.8 KB (11813 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2026.01-bookworm`

```console
$ docker pull rakudo-star@sha256:21c283befc61083d78dc4027188aafa9239c1c98af593fd32ce1d031d6df7ed7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.01-bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:077553d0fd50f384ede19e6c61ccc945f7f50e1d172cbcf1f3ff15d4aee3710e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177810307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ebc8654c4e6f124f6af4b3adc790351c2f65e508521171fbd34b2c58d7ef2a`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:20:37 GMT
MAINTAINER Rob Hoelz
# Tue, 03 Feb 2026 04:20:37 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 03 Feb 2026 04:20:37 GMT
ARG rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:20:37 GMT
ENV rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:39:01 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 04:39:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 03 Feb 2026 04:39:01 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbceb003542957cee7df7b79249eaf0a71d21c5203d086969b565fb6dec85d86`  
		Last Modified: Tue, 03 Feb 2026 03:28:33 GMT  
		Size: 64.4 MB (64395971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e859d02565b788af041df24fb00a6c0bd5359daae5324ab67ffd92ee04614f9c`  
		Last Modified: Tue, 03 Feb 2026 04:39:16 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c874acd37ac24abf8298b689d950304171077010bc9dc1ddf320b7519cd11ef6`  
		Last Modified: Tue, 03 Feb 2026 04:39:17 GMT  
		Size: 40.9 MB (40891166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:bdfd11098f60ae1d0cc7b513aeaca4eac7b462de81f121fb9dfaff2f0dd5711d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd6ec891b93bfd52f59898e15aedabcaa8fae601913d96c9bb8621c6f5dda19`

```dockerfile
```

-	Layers:
	-	`sha256:4dc75e5353932f13675e6ad4ebce354f9e7c3b7d18d6893a1563b264b3124be2`  
		Last Modified: Tue, 03 Feb 2026 04:39:16 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:239392665af5f87726f9fa2ecd296e18ae7377b978e3a9586d8d01e997d05749`  
		Last Modified: Tue, 03 Feb 2026 04:39:16 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.01-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:7dde5c13225f42a63317ab94500c46a31ebab0e6e18787ced803d28de3bf142b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175378836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d3dba9f588ca54fba4812af0fbbe2d0a8b7e02bcbd0bbe46315e4b7abee56b`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:25:20 GMT
MAINTAINER Rob Hoelz
# Tue, 03 Feb 2026 04:25:20 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 03 Feb 2026 04:25:20 GMT
ARG rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:25:20 GMT
ENV rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:45:10 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 04:45:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 03 Feb 2026 04:45:10 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e9aa4982c2a67e202ea283fc3760e94d8d8b16966c616e01ad0238abbaac82`  
		Last Modified: Tue, 03 Feb 2026 03:46:50 GMT  
		Size: 64.5 MB (64479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71458e8d50b23b754bd7ebe72c5e53705472972dd48505136c3ec2039317ed5a`  
		Last Modified: Tue, 03 Feb 2026 04:45:24 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f65902ac3b3cebe71523640d58edbc4f70ca73f26c4878ce1bab9bce247d677`  
		Last Modified: Tue, 03 Feb 2026 04:45:26 GMT  
		Size: 38.9 MB (38925111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:e32b0a7a3a6fd467d9f7520dc60c998f9970168833a943eef2604b239ead816a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4ed13300b4480f06eda174c34ba6d3d37367a7f0584e58d31d42b025b22816`

```dockerfile
```

-	Layers:
	-	`sha256:a5bfca375ad24f6f367f545e8d8b38cb45895d877fb3d98e6a4b33a88db93651`  
		Last Modified: Tue, 03 Feb 2026 04:45:25 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efbd4c68d14352f2b544cd712994c4bdf4603b3a83f8738049cf3cdeb7b3e888`  
		Last Modified: Tue, 03 Feb 2026 04:45:24 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2026.01-trixie`

```console
$ docker pull rakudo-star@sha256:bcf2fd12de5bec2decc5cbb832fa1de03e436241e9f01936fab4da8c9e3afb7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.01-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:d597733daa458d2be0ac00a5f21b25474b2e56bf4560599e1790eb89f39cebf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183610396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c615bdde4974aab2417b4bbdb6ce1cc232114ca3903c1aa7fe60062c2487f976`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:20:33 GMT
MAINTAINER AntonOks
# Tue, 03 Feb 2026 04:20:33 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 03 Feb 2026 04:20:33 GMT
ARG rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:20:33 GMT
ENV rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:34:57 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 04:34:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 03 Feb 2026 04:34:57 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954d6059ca7bdbb9ceb566ca2239e01ef312165659d656753d7dbace7771a591`  
		Last Modified: Tue, 03 Feb 2026 02:43:06 GMT  
		Size: 25.6 MB (25614010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e2021c4c8bd1a46b34d9608a9381afdc333600ee1ef3c94306ecf7373e1956`  
		Last Modified: Tue, 03 Feb 2026 03:29:16 GMT  
		Size: 67.8 MB (67787365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61bc89fcfa1f4cef3fe5888f359dcec0fb0e1d4475a1b2e4a25d224d7aef213`  
		Last Modified: Tue, 03 Feb 2026 04:35:11 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74013ac19fc7d038f9f635e164c3477cd227f2038fca20f70b2078582e1d09`  
		Last Modified: Tue, 03 Feb 2026 04:35:12 GMT  
		Size: 40.9 MB (40912827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:01328201575826c9c3cf42daf1041dd58f42c7dafc24b9e998c5d8fb31708252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169b07796296850f4a8fc576802310a72b2401d45ed571bdb8288d59a0d90158`

```dockerfile
```

-	Layers:
	-	`sha256:da350bb0f56c3c41d847a0cbe584c83c3f1d15b4730c60dc2c4b0aba9e441e8d`  
		Last Modified: Tue, 03 Feb 2026 04:35:11 GMT  
		Size: 7.8 MB (7770538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b2c4659e6b07daff8f2feec2d3dab6fd136ecff5a9adb7245fdf09ba619be50`  
		Last Modified: Tue, 03 Feb 2026 04:35:10 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.01-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:7d57dc49a5217f886fe9e64ad742938e0b4208b59822dd9acd9f238720ef77ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.2 MB (181212595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21cfafa26e885449f91db35fe686cfaa6f53bdebba93e6abad527332da337f5`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:24:19 GMT
MAINTAINER AntonOks
# Tue, 03 Feb 2026 04:24:19 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 03 Feb 2026 04:24:19 GMT
ARG rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:24:19 GMT
ENV rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:42:47 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 04:42:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 03 Feb 2026 04:42:47 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cace8fbd9245d4cb1b11d410baa101c40f315e70bee7d3ba014bb966a4da4517`  
		Last Modified: Tue, 03 Feb 2026 02:46:11 GMT  
		Size: 25.0 MB (25022688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8128ce97ccffb1094b6eafc78b5827499d0496944f3d357e222bfc29f01968`  
		Last Modified: Tue, 03 Feb 2026 03:47:30 GMT  
		Size: 67.6 MB (67593005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a5185d1da7673ccb797db75912598a5255b966a4c5463d8bd39f1f3fcc3c15`  
		Last Modified: Tue, 03 Feb 2026 04:43:02 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6c106cf3cd6a0bd2145828cd47d79d9f00e28c9228f2756dbfaa89b0e52f9b`  
		Last Modified: Tue, 03 Feb 2026 04:43:03 GMT  
		Size: 38.9 MB (38941644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:501afc66446f0c9f7d6bc46fade5c657f9e631510e9bd3e266fbb1b5a31fb9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1628c3906176558fd6b72ddcb4a182861113200977245f7f643cb6390c703e8b`

```dockerfile
```

-	Layers:
	-	`sha256:a4c1dd21b4fd31fb9dc7e969b78592840aa8390334c8702131e2c2cb51c6c75f`  
		Last Modified: Tue, 03 Feb 2026 04:43:02 GMT  
		Size: 7.8 MB (7778213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bd01d370fd5aac5dc889a7ba66c02183150e29f21bbb55b099d6abcc998e448`  
		Last Modified: Tue, 03 Feb 2026 04:43:02 GMT  
		Size: 13.1 KB (13099 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:78a228970ec5e9b42567b9d6da6629b1a49c3f6175f2e7a52b1afdbdaef0b31f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a5bff11023898fb0a4aea0041a2914ae3088ab11afd6965cb5fa4e8382531b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51337346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9dfeb15cf9dd0010a9ddd7e4938e03a6c544adb4a84edc2b3ebf14219bbe3f`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:03:04 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 02 Feb 2026 19:19:20 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:19:20 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:19:20 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 02 Feb 2026 19:19:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:19:20 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3060884c0be28f953f468c7201d683ba6c0e82dddfc2564c09b2d3b821b4e4fb`  
		Last Modified: Mon, 02 Feb 2026 19:19:31 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe45a1b0764dd266b786344adcb3b4c60c26489d59bdf104692f0849be7c390c`  
		Last Modified: Mon, 02 Feb 2026 19:19:36 GMT  
		Size: 47.5 MB (47474577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:4658d3cab6fd635f2f098ac62c80fcda5ce29fc291cf7e04be980103cf93a655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5115d4e0288db5efbf0f47419b95453d7567d45a1c64368a45ad162f8ed98d33`

```dockerfile
```

-	Layers:
	-	`sha256:cbd4c48955e5af20ebde87c4430550e568b58e1e4da10059a9e7a37b8991b3b5`  
		Last Modified: Mon, 02 Feb 2026 19:19:31 GMT  
		Size: 187.0 KB (186973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd9039c43e0e55fadf6c78efbca2ca8533cfb57e7ac6a2962c6cc8d85aeb6ee`  
		Last Modified: Mon, 02 Feb 2026 19:19:31 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:e23968cc99cf3d7329dffb6df4a788bbff56e8660ba05b60140cb3dc85415aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51410918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44523c43bffe91994ab0d41cac40b9586c81063423cf08a6095b4b47039f3df`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:03:53 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 02 Feb 2026 19:23:15 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:23:15 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:23:15 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 02 Feb 2026 19:23:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:23:15 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637aa627dfc01bebed15028112f215606ab0f1cd1d25c2a41fdd2ab88fc60530`  
		Last Modified: Mon, 02 Feb 2026 19:23:27 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52008d4f177e3efc234c3aaabeaf66f73e9add81659a303f773a078438c24ee`  
		Last Modified: Mon, 02 Feb 2026 19:23:28 GMT  
		Size: 47.2 MB (47212880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:212cd58719d10575eec5bbc600a315b36c9171b8d70d6117876511f7caa74d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588030a4c73d35971132596be85090e56b1d035c0f1fdc39cabcb3371f47e6ec`

```dockerfile
```

-	Layers:
	-	`sha256:f57e8b7aa80eafc12962eb9f7d1a3d01a9e49ce3dd50381059874a3017cd2e83`  
		Last Modified: Mon, 02 Feb 2026 19:23:27 GMT  
		Size: 186.4 KB (186355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ee180b9438495f5dd822ac0813970d7a53c6fc36cc9b2cf00d14ecfa17f2b9b`  
		Last Modified: Mon, 02 Feb 2026 19:23:27 GMT  
		Size: 11.8 KB (11813 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:21c283befc61083d78dc4027188aafa9239c1c98af593fd32ce1d031d6df7ed7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:077553d0fd50f384ede19e6c61ccc945f7f50e1d172cbcf1f3ff15d4aee3710e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177810307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ebc8654c4e6f124f6af4b3adc790351c2f65e508521171fbd34b2c58d7ef2a`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:20:37 GMT
MAINTAINER Rob Hoelz
# Tue, 03 Feb 2026 04:20:37 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 03 Feb 2026 04:20:37 GMT
ARG rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:20:37 GMT
ENV rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:39:01 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 04:39:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 03 Feb 2026 04:39:01 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbceb003542957cee7df7b79249eaf0a71d21c5203d086969b565fb6dec85d86`  
		Last Modified: Tue, 03 Feb 2026 03:28:33 GMT  
		Size: 64.4 MB (64395971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e859d02565b788af041df24fb00a6c0bd5359daae5324ab67ffd92ee04614f9c`  
		Last Modified: Tue, 03 Feb 2026 04:39:16 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c874acd37ac24abf8298b689d950304171077010bc9dc1ddf320b7519cd11ef6`  
		Last Modified: Tue, 03 Feb 2026 04:39:17 GMT  
		Size: 40.9 MB (40891166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:bdfd11098f60ae1d0cc7b513aeaca4eac7b462de81f121fb9dfaff2f0dd5711d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd6ec891b93bfd52f59898e15aedabcaa8fae601913d96c9bb8621c6f5dda19`

```dockerfile
```

-	Layers:
	-	`sha256:4dc75e5353932f13675e6ad4ebce354f9e7c3b7d18d6893a1563b264b3124be2`  
		Last Modified: Tue, 03 Feb 2026 04:39:16 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:239392665af5f87726f9fa2ecd296e18ae7377b978e3a9586d8d01e997d05749`  
		Last Modified: Tue, 03 Feb 2026 04:39:16 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:7dde5c13225f42a63317ab94500c46a31ebab0e6e18787ced803d28de3bf142b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175378836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d3dba9f588ca54fba4812af0fbbe2d0a8b7e02bcbd0bbe46315e4b7abee56b`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:25:20 GMT
MAINTAINER Rob Hoelz
# Tue, 03 Feb 2026 04:25:20 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 03 Feb 2026 04:25:20 GMT
ARG rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:25:20 GMT
ENV rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:45:10 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 04:45:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 03 Feb 2026 04:45:10 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e9aa4982c2a67e202ea283fc3760e94d8d8b16966c616e01ad0238abbaac82`  
		Last Modified: Tue, 03 Feb 2026 03:46:50 GMT  
		Size: 64.5 MB (64479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71458e8d50b23b754bd7ebe72c5e53705472972dd48505136c3ec2039317ed5a`  
		Last Modified: Tue, 03 Feb 2026 04:45:24 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f65902ac3b3cebe71523640d58edbc4f70ca73f26c4878ce1bab9bce247d677`  
		Last Modified: Tue, 03 Feb 2026 04:45:26 GMT  
		Size: 38.9 MB (38925111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:e32b0a7a3a6fd467d9f7520dc60c998f9970168833a943eef2604b239ead816a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4ed13300b4480f06eda174c34ba6d3d37367a7f0584e58d31d42b025b22816`

```dockerfile
```

-	Layers:
	-	`sha256:a5bfca375ad24f6f367f545e8d8b38cb45895d877fb3d98e6a4b33a88db93651`  
		Last Modified: Tue, 03 Feb 2026 04:45:25 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efbd4c68d14352f2b544cd712994c4bdf4603b3a83f8738049cf3cdeb7b3e888`  
		Last Modified: Tue, 03 Feb 2026 04:45:24 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:bcf2fd12de5bec2decc5cbb832fa1de03e436241e9f01936fab4da8c9e3afb7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:d597733daa458d2be0ac00a5f21b25474b2e56bf4560599e1790eb89f39cebf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183610396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c615bdde4974aab2417b4bbdb6ce1cc232114ca3903c1aa7fe60062c2487f976`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:20:33 GMT
MAINTAINER AntonOks
# Tue, 03 Feb 2026 04:20:33 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 03 Feb 2026 04:20:33 GMT
ARG rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:20:33 GMT
ENV rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:34:57 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 04:34:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 03 Feb 2026 04:34:57 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954d6059ca7bdbb9ceb566ca2239e01ef312165659d656753d7dbace7771a591`  
		Last Modified: Tue, 03 Feb 2026 02:43:06 GMT  
		Size: 25.6 MB (25614010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e2021c4c8bd1a46b34d9608a9381afdc333600ee1ef3c94306ecf7373e1956`  
		Last Modified: Tue, 03 Feb 2026 03:29:16 GMT  
		Size: 67.8 MB (67787365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61bc89fcfa1f4cef3fe5888f359dcec0fb0e1d4475a1b2e4a25d224d7aef213`  
		Last Modified: Tue, 03 Feb 2026 04:35:11 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74013ac19fc7d038f9f635e164c3477cd227f2038fca20f70b2078582e1d09`  
		Last Modified: Tue, 03 Feb 2026 04:35:12 GMT  
		Size: 40.9 MB (40912827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:01328201575826c9c3cf42daf1041dd58f42c7dafc24b9e998c5d8fb31708252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169b07796296850f4a8fc576802310a72b2401d45ed571bdb8288d59a0d90158`

```dockerfile
```

-	Layers:
	-	`sha256:da350bb0f56c3c41d847a0cbe584c83c3f1d15b4730c60dc2c4b0aba9e441e8d`  
		Last Modified: Tue, 03 Feb 2026 04:35:11 GMT  
		Size: 7.8 MB (7770538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b2c4659e6b07daff8f2feec2d3dab6fd136ecff5a9adb7245fdf09ba619be50`  
		Last Modified: Tue, 03 Feb 2026 04:35:10 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:7d57dc49a5217f886fe9e64ad742938e0b4208b59822dd9acd9f238720ef77ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.2 MB (181212595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21cfafa26e885449f91db35fe686cfaa6f53bdebba93e6abad527332da337f5`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:24:19 GMT
MAINTAINER AntonOks
# Tue, 03 Feb 2026 04:24:19 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 03 Feb 2026 04:24:19 GMT
ARG rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:24:19 GMT
ENV rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:42:47 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 04:42:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 03 Feb 2026 04:42:47 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cace8fbd9245d4cb1b11d410baa101c40f315e70bee7d3ba014bb966a4da4517`  
		Last Modified: Tue, 03 Feb 2026 02:46:11 GMT  
		Size: 25.0 MB (25022688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8128ce97ccffb1094b6eafc78b5827499d0496944f3d357e222bfc29f01968`  
		Last Modified: Tue, 03 Feb 2026 03:47:30 GMT  
		Size: 67.6 MB (67593005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a5185d1da7673ccb797db75912598a5255b966a4c5463d8bd39f1f3fcc3c15`  
		Last Modified: Tue, 03 Feb 2026 04:43:02 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6c106cf3cd6a0bd2145828cd47d79d9f00e28c9228f2756dbfaa89b0e52f9b`  
		Last Modified: Tue, 03 Feb 2026 04:43:03 GMT  
		Size: 38.9 MB (38941644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:501afc66446f0c9f7d6bc46fade5c657f9e631510e9bd3e266fbb1b5a31fb9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1628c3906176558fd6b72ddcb4a182861113200977245f7f643cb6390c703e8b`

```dockerfile
```

-	Layers:
	-	`sha256:a4c1dd21b4fd31fb9dc7e969b78592840aa8390334c8702131e2c2cb51c6c75f`  
		Last Modified: Tue, 03 Feb 2026 04:43:02 GMT  
		Size: 7.8 MB (7778213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bd01d370fd5aac5dc889a7ba66c02183150e29f21bbb55b099d6abcc998e448`  
		Last Modified: Tue, 03 Feb 2026 04:43:02 GMT  
		Size: 13.1 KB (13099 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:bcf2fd12de5bec2decc5cbb832fa1de03e436241e9f01936fab4da8c9e3afb7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:d597733daa458d2be0ac00a5f21b25474b2e56bf4560599e1790eb89f39cebf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183610396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c615bdde4974aab2417b4bbdb6ce1cc232114ca3903c1aa7fe60062c2487f976`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:20:33 GMT
MAINTAINER AntonOks
# Tue, 03 Feb 2026 04:20:33 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 03 Feb 2026 04:20:33 GMT
ARG rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:20:33 GMT
ENV rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:34:57 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 04:34:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 03 Feb 2026 04:34:57 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954d6059ca7bdbb9ceb566ca2239e01ef312165659d656753d7dbace7771a591`  
		Last Modified: Tue, 03 Feb 2026 02:43:06 GMT  
		Size: 25.6 MB (25614010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e2021c4c8bd1a46b34d9608a9381afdc333600ee1ef3c94306ecf7373e1956`  
		Last Modified: Tue, 03 Feb 2026 03:29:16 GMT  
		Size: 67.8 MB (67787365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61bc89fcfa1f4cef3fe5888f359dcec0fb0e1d4475a1b2e4a25d224d7aef213`  
		Last Modified: Tue, 03 Feb 2026 04:35:11 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74013ac19fc7d038f9f635e164c3477cd227f2038fca20f70b2078582e1d09`  
		Last Modified: Tue, 03 Feb 2026 04:35:12 GMT  
		Size: 40.9 MB (40912827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:01328201575826c9c3cf42daf1041dd58f42c7dafc24b9e998c5d8fb31708252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169b07796296850f4a8fc576802310a72b2401d45ed571bdb8288d59a0d90158`

```dockerfile
```

-	Layers:
	-	`sha256:da350bb0f56c3c41d847a0cbe584c83c3f1d15b4730c60dc2c4b0aba9e441e8d`  
		Last Modified: Tue, 03 Feb 2026 04:35:11 GMT  
		Size: 7.8 MB (7770538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b2c4659e6b07daff8f2feec2d3dab6fd136ecff5a9adb7245fdf09ba619be50`  
		Last Modified: Tue, 03 Feb 2026 04:35:10 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:7d57dc49a5217f886fe9e64ad742938e0b4208b59822dd9acd9f238720ef77ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.2 MB (181212595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21cfafa26e885449f91db35fe686cfaa6f53bdebba93e6abad527332da337f5`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:24:19 GMT
MAINTAINER AntonOks
# Tue, 03 Feb 2026 04:24:19 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 03 Feb 2026 04:24:19 GMT
ARG rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:24:19 GMT
ENV rakudo_version=2026.01-01
# Tue, 03 Feb 2026 04:42:47 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 04:42:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 03 Feb 2026 04:42:47 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cace8fbd9245d4cb1b11d410baa101c40f315e70bee7d3ba014bb966a4da4517`  
		Last Modified: Tue, 03 Feb 2026 02:46:11 GMT  
		Size: 25.0 MB (25022688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8128ce97ccffb1094b6eafc78b5827499d0496944f3d357e222bfc29f01968`  
		Last Modified: Tue, 03 Feb 2026 03:47:30 GMT  
		Size: 67.6 MB (67593005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a5185d1da7673ccb797db75912598a5255b966a4c5463d8bd39f1f3fcc3c15`  
		Last Modified: Tue, 03 Feb 2026 04:43:02 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6c106cf3cd6a0bd2145828cd47d79d9f00e28c9228f2756dbfaa89b0e52f9b`  
		Last Modified: Tue, 03 Feb 2026 04:43:03 GMT  
		Size: 38.9 MB (38941644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:501afc66446f0c9f7d6bc46fade5c657f9e631510e9bd3e266fbb1b5a31fb9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1628c3906176558fd6b72ddcb4a182861113200977245f7f643cb6390c703e8b`

```dockerfile
```

-	Layers:
	-	`sha256:a4c1dd21b4fd31fb9dc7e969b78592840aa8390334c8702131e2c2cb51c6c75f`  
		Last Modified: Tue, 03 Feb 2026 04:43:02 GMT  
		Size: 7.8 MB (7778213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bd01d370fd5aac5dc889a7ba66c02183150e29f21bbb55b099d6abcc998e448`  
		Last Modified: Tue, 03 Feb 2026 04:43:02 GMT  
		Size: 13.1 KB (13099 bytes)  
		MIME: application/vnd.in-toto+json
