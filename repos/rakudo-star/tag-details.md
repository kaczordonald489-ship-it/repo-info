<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2025.10-alpine`](#rakudo-star202510-alpine)
-	[`rakudo-star:2025.10-bookworm`](#rakudo-star202510-bookworm)
-	[`rakudo-star:2025.10-trixie`](#rakudo-star202510-trixie)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)
-	[`rakudo-star:trixie`](#rakudo-startrixie)

## `rakudo-star:2025.10-alpine`

```console
$ docker pull rakudo-star@sha256:60f630c763fe053a4fbb90a877964f17d8021043b8b31e36abe4e0ba9203e862
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.10-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:f608fe8aae34343c8a52fbc9ba0e3ab0aec156b3547db71d69dc2acee6ae4da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52898044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c394f4de6f740f7e91e05c6ef8a0e2c4949864c2d6b047ade93082e31715395`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 03:12:19 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94ae187876b8dfd9796c6a5e83b3fd4df758dab43d6e470d4b3e2b0e8e699ef`  
		Last Modified: Thu, 23 Oct 2025 23:46:46 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479dd71f79409ea180e1088f9824b93c21d4c109f800a05baef9ffaf1b948035`  
		Last Modified: Thu, 23 Oct 2025 23:46:49 GMT  
		Size: 49.1 MB (49094643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:771edf5e119637bd6e29891909c6e22a41bf60b6cc4c956f170592d07fd7e1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 KB (197780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6e06b7417bc34fb3651e11bc883f341b3ac83727b269273649d67b1ce09942`

```dockerfile
```

-	Layers:
	-	`sha256:da1fe5c8cdce4abdd95d12d29185b6bd74c1cc4ee40fff1c14afe654a98db351`  
		Last Modified: Fri, 24 Oct 2025 01:33:20 GMT  
		Size: 186.0 KB (186020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:702e025402ada9b8eeba1897b6a64f0bdfa61551086096a3d5aea7ef06c12e7d`  
		Last Modified: Fri, 24 Oct 2025 01:33:21 GMT  
		Size: 11.8 KB (11760 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.10-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:a550cebb99664a9633d897c98c89899f51d8f9435ef5b614eb545fba93995bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52925677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1445c061ae404b4788a5178c6db3e7339ec2789e163e26d90c7fb4940e352b6`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 03:12:19 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f354594890fce8d86fccc0efd95519674214696b4d7be96e258f4608cd8935`  
		Last Modified: Thu, 23 Oct 2025 22:30:49 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea0230fc82455718c52d3c89e277ef1cf39d85f33ab447bccb2d125194cb203`  
		Last Modified: Thu, 23 Oct 2025 22:30:53 GMT  
		Size: 48.8 MB (48786660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:5321a6a3a5400198193ec57dd6da13c6ab29c95dcd6acaec789d0bbbf8573dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 KB (197907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0a76bc0ad9780a1dfd9b03748bb412e60acbd0726a1e8445c9e17dd01e5839`

```dockerfile
```

-	Layers:
	-	`sha256:a7d61e7b14327a9149659f2cc4dd38b50e46d7c5b2f272ec0a135c79719380a4`  
		Last Modified: Fri, 24 Oct 2025 01:33:24 GMT  
		Size: 186.1 KB (186052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:119a5fd04ebf8a2ee4f6476233145b8923f667a97a8c22c43bcf7bac0df4c3ca`  
		Last Modified: Fri, 24 Oct 2025 01:33:25 GMT  
		Size: 11.9 KB (11855 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.10-bookworm`

```console
$ docker pull rakudo-star@sha256:77dd16df83d00b104ba3f05930e302d169d1be25b96d00a7dd290f1423a2dc76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.10-bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:98335761b953078ac4afd292f050aebf93df4c00cd213961b6de73954fe9fca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179633081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6f3ca5c630261ec762c220a077321e585bda1dce15c24598bb762d112ccf77`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:28:09 GMT
MAINTAINER Rob Hoelz
# Tue, 18 Nov 2025 10:28:09 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 18 Nov 2025 10:28:09 GMT
ARG rakudo_version=2025.10-01
# Tue, 18 Nov 2025 10:28:09 GMT
ENV rakudo_version=2025.10-01
# Tue, 18 Nov 2025 10:42:56 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 10:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 18 Nov 2025 10:42:56 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078b2eece9b24f617524f986db4dd04f977e3e7d6fe15a9088a584147bc6ba05`  
		Last Modified: Tue, 18 Nov 2025 06:38:36 GMT  
		Size: 64.4 MB (64396262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5c0951e8b4c2f1d17d2e4ab379115d975e164d01661a59d8881e5e7f737ad7`  
		Last Modified: Tue, 18 Nov 2025 10:43:18 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d78d1381257d040cec62a151d1ef1d2571d993db5dd7fc9a2e2492019240aa5`  
		Last Modified: Tue, 18 Nov 2025 10:43:24 GMT  
		Size: 42.7 MB (42723470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3a0b66f1fa6e3d7ead887e3c33c609b5286cac10b4d07711f500777728c831f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbbe6bc234759d2e12ab943084c449355bbb5cd844771f018f0a09414d8de0a`

```dockerfile
```

-	Layers:
	-	`sha256:81187ba7370c7cc5376cfcd00a06354351bd5d5f899eecbd1c1b268171629e7e`  
		Last Modified: Tue, 18 Nov 2025 11:34:19 GMT  
		Size: 8.0 MB (7967804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea50bf1319a8a01f10c72dca26faa0be6f95146b82577fab0a447fcc7fae8be0`  
		Last Modified: Tue, 18 Nov 2025 11:34:20 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:368420af7d0faa09b4fa195da19abe29c3c05ec37b4632dfc56eb95da42b554c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (177037798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e74491ed48760a1b101d7bf1b6cb09ccea7de015598101173d566e98e70d284`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:42:55 GMT
MAINTAINER Rob Hoelz
# Tue, 18 Nov 2025 06:42:55 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 18 Nov 2025 06:42:55 GMT
ARG rakudo_version=2025.10-01
# Tue, 18 Nov 2025 06:42:55 GMT
ENV rakudo_version=2025.10-01
# Tue, 18 Nov 2025 07:02:26 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 07:02:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 18 Nov 2025 07:02:26 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25d805ffe4d6247a3ab7494e663f6ae84d04e36c5270a200f1d1d34db32a26c`  
		Last Modified: Tue, 18 Nov 2025 05:38:35 GMT  
		Size: 64.4 MB (64371414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2c1c1b725841787fd7038584369f950d375aedcf4cc13643e935cf8c171d07`  
		Last Modified: Tue, 18 Nov 2025 07:02:50 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300a50301ff18d06ad0ffe79237a9e1529ebb67a00bdb4a4bc1b50226557f615`  
		Last Modified: Tue, 18 Nov 2025 07:02:54 GMT  
		Size: 40.7 MB (40705685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:1e6c5dde9f23ada08e21de637bc6c0faab6d2b5432de3baabcce658f65f8aa58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035fbbb62f94bffdc2007c1a9c1f3fc38f7c7a9b952c8978919e34889fc1b393`

```dockerfile
```

-	Layers:
	-	`sha256:ace36da9f2459ea443ce6c0948d677de8f41c5b57b729c3fd61f4a8920252e9e`  
		Last Modified: Tue, 18 Nov 2025 08:33:43 GMT  
		Size: 8.0 MB (7974197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d5463174acd51aa000f9f914dab27d1741bad86910b652e4f6fb696e92a888`  
		Last Modified: Tue, 18 Nov 2025 08:33:43 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.10-trixie`

```console
$ docker pull rakudo-star@sha256:1d88bce148d5fb10b55194d6271c8ccc3420cc8c16cab0cc609fd8580f909405
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.10-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:b229ed29a825f1ed51226e3190924be2bbf6501ba5c17af269c66c6046d1acf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185432999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3fbaf9c94fb1ce43ddb308a5fbc940e1dfdcafdaec0e33884068ff708400af`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 10:27:50 GMT
MAINTAINER AntonOks
# Tue, 18 Nov 2025 10:27:50 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 18 Nov 2025 10:27:50 GMT
ARG rakudo_version=2025.10-01
# Tue, 18 Nov 2025 10:27:50 GMT
ENV rakudo_version=2025.10-01
# Tue, 18 Nov 2025 10:40:41 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 10:40:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 18 Nov 2025 10:40:41 GMT
CMD ["raku"]
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
	-	`sha256:a1ab97d0d94a8ba61e6aba1de589ad44a54344141242394b98cb66a65aebe7be`  
		Last Modified: Tue, 18 Nov 2025 10:41:02 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af0b6dd061a95a27af05560f55aa4debe9549a8e0dd6e5ec3683c0a43d7905e`  
		Last Modified: Tue, 18 Nov 2025 10:41:10 GMT  
		Size: 42.7 MB (42747298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:7b5ce24990765fe8a19f11a80e9cf8500d895010abbdb89b2c7ea541c726a01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3967969156a362ee53f7247640782bcf2dfdaae0c489d3fceb57c90fba029c66`

```dockerfile
```

-	Layers:
	-	`sha256:487c75ed8893341f9a8a8a566ec8951533e671c213b733fb4c85de9b11509e67`  
		Last Modified: Tue, 18 Nov 2025 11:34:25 GMT  
		Size: 7.8 MB (7769499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67dc3a14a44210abae2295e8a4b54e98bb4319bdc69ee589cdfe9a64856e4b48`  
		Last Modified: Tue, 18 Nov 2025 11:34:25 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.10-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:25468224abbc2e32aee53f05248dea53ed0d32e327d9383a5ae0c423fb2c023f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182964743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3c02669e673ade7194607a141bc72bd300566c7f6c91ab7cac23f09e2d028b`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:42:56 GMT
MAINTAINER AntonOks
# Tue, 18 Nov 2025 06:42:56 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 18 Nov 2025 06:42:56 GMT
ARG rakudo_version=2025.10-01
# Tue, 18 Nov 2025 06:42:56 GMT
ENV rakudo_version=2025.10-01
# Tue, 18 Nov 2025 07:01:48 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 07:01:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 18 Nov 2025 07:01:48 GMT
CMD ["raku"]
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
	-	`sha256:7c1925aa376fcb1a7162d40d27685f7d752f9d7c57f07ba5774f5e02dee95c95`  
		Last Modified: Tue, 18 Nov 2025 07:02:27 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fc607bdb37f40b856cd79db20616896d0a315358c7d5387bed8595d25138ad`  
		Last Modified: Tue, 18 Nov 2025 07:02:31 GMT  
		Size: 40.7 MB (40705496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0bdadf93684c38f6c33be22b3dcfdbcf518d1c99047ba873707002a1553f7a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c05f82fecc6daaf2316b3eb10b83cb203f62d544a248acd69a3435668ecad4`

```dockerfile
```

-	Layers:
	-	`sha256:4f6b3900ff2c89fc3eb95492eda4ef5a7c18003a9e50edc78a7de1cb29e7c1d2`  
		Last Modified: Tue, 18 Nov 2025 08:33:46 GMT  
		Size: 7.8 MB (7777174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61dd882ab499de310fba89d437fbeef70a85cb89869a18c92296c43291513082`  
		Last Modified: Tue, 18 Nov 2025 08:33:46 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:60f630c763fe053a4fbb90a877964f17d8021043b8b31e36abe4e0ba9203e862
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:f608fe8aae34343c8a52fbc9ba0e3ab0aec156b3547db71d69dc2acee6ae4da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52898044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c394f4de6f740f7e91e05c6ef8a0e2c4949864c2d6b047ade93082e31715395`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 03:12:19 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94ae187876b8dfd9796c6a5e83b3fd4df758dab43d6e470d4b3e2b0e8e699ef`  
		Last Modified: Thu, 23 Oct 2025 23:46:46 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479dd71f79409ea180e1088f9824b93c21d4c109f800a05baef9ffaf1b948035`  
		Last Modified: Thu, 23 Oct 2025 23:46:49 GMT  
		Size: 49.1 MB (49094643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:771edf5e119637bd6e29891909c6e22a41bf60b6cc4c956f170592d07fd7e1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 KB (197780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6e06b7417bc34fb3651e11bc883f341b3ac83727b269273649d67b1ce09942`

```dockerfile
```

-	Layers:
	-	`sha256:da1fe5c8cdce4abdd95d12d29185b6bd74c1cc4ee40fff1c14afe654a98db351`  
		Last Modified: Fri, 24 Oct 2025 01:33:20 GMT  
		Size: 186.0 KB (186020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:702e025402ada9b8eeba1897b6a64f0bdfa61551086096a3d5aea7ef06c12e7d`  
		Last Modified: Fri, 24 Oct 2025 01:33:21 GMT  
		Size: 11.8 KB (11760 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:a550cebb99664a9633d897c98c89899f51d8f9435ef5b614eb545fba93995bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52925677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1445c061ae404b4788a5178c6db3e7339ec2789e163e26d90c7fb4940e352b6`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 03:12:19 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f354594890fce8d86fccc0efd95519674214696b4d7be96e258f4608cd8935`  
		Last Modified: Thu, 23 Oct 2025 22:30:49 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea0230fc82455718c52d3c89e277ef1cf39d85f33ab447bccb2d125194cb203`  
		Last Modified: Thu, 23 Oct 2025 22:30:53 GMT  
		Size: 48.8 MB (48786660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:5321a6a3a5400198193ec57dd6da13c6ab29c95dcd6acaec789d0bbbf8573dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 KB (197907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0a76bc0ad9780a1dfd9b03748bb412e60acbd0726a1e8445c9e17dd01e5839`

```dockerfile
```

-	Layers:
	-	`sha256:a7d61e7b14327a9149659f2cc4dd38b50e46d7c5b2f272ec0a135c79719380a4`  
		Last Modified: Fri, 24 Oct 2025 01:33:24 GMT  
		Size: 186.1 KB (186052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:119a5fd04ebf8a2ee4f6476233145b8923f667a97a8c22c43bcf7bac0df4c3ca`  
		Last Modified: Fri, 24 Oct 2025 01:33:25 GMT  
		Size: 11.9 KB (11855 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:77dd16df83d00b104ba3f05930e302d169d1be25b96d00a7dd290f1423a2dc76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:98335761b953078ac4afd292f050aebf93df4c00cd213961b6de73954fe9fca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179633081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6f3ca5c630261ec762c220a077321e585bda1dce15c24598bb762d112ccf77`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:28:09 GMT
MAINTAINER Rob Hoelz
# Tue, 18 Nov 2025 10:28:09 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 18 Nov 2025 10:28:09 GMT
ARG rakudo_version=2025.10-01
# Tue, 18 Nov 2025 10:28:09 GMT
ENV rakudo_version=2025.10-01
# Tue, 18 Nov 2025 10:42:56 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 10:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 18 Nov 2025 10:42:56 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078b2eece9b24f617524f986db4dd04f977e3e7d6fe15a9088a584147bc6ba05`  
		Last Modified: Tue, 18 Nov 2025 06:38:36 GMT  
		Size: 64.4 MB (64396262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5c0951e8b4c2f1d17d2e4ab379115d975e164d01661a59d8881e5e7f737ad7`  
		Last Modified: Tue, 18 Nov 2025 10:43:18 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d78d1381257d040cec62a151d1ef1d2571d993db5dd7fc9a2e2492019240aa5`  
		Last Modified: Tue, 18 Nov 2025 10:43:24 GMT  
		Size: 42.7 MB (42723470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3a0b66f1fa6e3d7ead887e3c33c609b5286cac10b4d07711f500777728c831f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbbe6bc234759d2e12ab943084c449355bbb5cd844771f018f0a09414d8de0a`

```dockerfile
```

-	Layers:
	-	`sha256:81187ba7370c7cc5376cfcd00a06354351bd5d5f899eecbd1c1b268171629e7e`  
		Last Modified: Tue, 18 Nov 2025 11:34:19 GMT  
		Size: 8.0 MB (7967804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea50bf1319a8a01f10c72dca26faa0be6f95146b82577fab0a447fcc7fae8be0`  
		Last Modified: Tue, 18 Nov 2025 11:34:20 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:368420af7d0faa09b4fa195da19abe29c3c05ec37b4632dfc56eb95da42b554c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (177037798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e74491ed48760a1b101d7bf1b6cb09ccea7de015598101173d566e98e70d284`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:42:55 GMT
MAINTAINER Rob Hoelz
# Tue, 18 Nov 2025 06:42:55 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 18 Nov 2025 06:42:55 GMT
ARG rakudo_version=2025.10-01
# Tue, 18 Nov 2025 06:42:55 GMT
ENV rakudo_version=2025.10-01
# Tue, 18 Nov 2025 07:02:26 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 07:02:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 18 Nov 2025 07:02:26 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25d805ffe4d6247a3ab7494e663f6ae84d04e36c5270a200f1d1d34db32a26c`  
		Last Modified: Tue, 18 Nov 2025 05:38:35 GMT  
		Size: 64.4 MB (64371414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2c1c1b725841787fd7038584369f950d375aedcf4cc13643e935cf8c171d07`  
		Last Modified: Tue, 18 Nov 2025 07:02:50 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300a50301ff18d06ad0ffe79237a9e1529ebb67a00bdb4a4bc1b50226557f615`  
		Last Modified: Tue, 18 Nov 2025 07:02:54 GMT  
		Size: 40.7 MB (40705685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:1e6c5dde9f23ada08e21de637bc6c0faab6d2b5432de3baabcce658f65f8aa58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035fbbb62f94bffdc2007c1a9c1f3fc38f7c7a9b952c8978919e34889fc1b393`

```dockerfile
```

-	Layers:
	-	`sha256:ace36da9f2459ea443ce6c0948d677de8f41c5b57b729c3fd61f4a8920252e9e`  
		Last Modified: Tue, 18 Nov 2025 08:33:43 GMT  
		Size: 8.0 MB (7974197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d5463174acd51aa000f9f914dab27d1741bad86910b652e4f6fb696e92a888`  
		Last Modified: Tue, 18 Nov 2025 08:33:43 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:1d88bce148d5fb10b55194d6271c8ccc3420cc8c16cab0cc609fd8580f909405
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:b229ed29a825f1ed51226e3190924be2bbf6501ba5c17af269c66c6046d1acf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185432999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3fbaf9c94fb1ce43ddb308a5fbc940e1dfdcafdaec0e33884068ff708400af`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 10:27:50 GMT
MAINTAINER AntonOks
# Tue, 18 Nov 2025 10:27:50 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 18 Nov 2025 10:27:50 GMT
ARG rakudo_version=2025.10-01
# Tue, 18 Nov 2025 10:27:50 GMT
ENV rakudo_version=2025.10-01
# Tue, 18 Nov 2025 10:40:41 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 10:40:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 18 Nov 2025 10:40:41 GMT
CMD ["raku"]
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
	-	`sha256:a1ab97d0d94a8ba61e6aba1de589ad44a54344141242394b98cb66a65aebe7be`  
		Last Modified: Tue, 18 Nov 2025 10:41:02 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af0b6dd061a95a27af05560f55aa4debe9549a8e0dd6e5ec3683c0a43d7905e`  
		Last Modified: Tue, 18 Nov 2025 10:41:10 GMT  
		Size: 42.7 MB (42747298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:7b5ce24990765fe8a19f11a80e9cf8500d895010abbdb89b2c7ea541c726a01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3967969156a362ee53f7247640782bcf2dfdaae0c489d3fceb57c90fba029c66`

```dockerfile
```

-	Layers:
	-	`sha256:487c75ed8893341f9a8a8a566ec8951533e671c213b733fb4c85de9b11509e67`  
		Last Modified: Tue, 18 Nov 2025 11:34:25 GMT  
		Size: 7.8 MB (7769499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67dc3a14a44210abae2295e8a4b54e98bb4319bdc69ee589cdfe9a64856e4b48`  
		Last Modified: Tue, 18 Nov 2025 11:34:25 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:25468224abbc2e32aee53f05248dea53ed0d32e327d9383a5ae0c423fb2c023f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182964743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3c02669e673ade7194607a141bc72bd300566c7f6c91ab7cac23f09e2d028b`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:42:56 GMT
MAINTAINER AntonOks
# Tue, 18 Nov 2025 06:42:56 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 18 Nov 2025 06:42:56 GMT
ARG rakudo_version=2025.10-01
# Tue, 18 Nov 2025 06:42:56 GMT
ENV rakudo_version=2025.10-01
# Tue, 18 Nov 2025 07:01:48 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 07:01:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 18 Nov 2025 07:01:48 GMT
CMD ["raku"]
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
	-	`sha256:7c1925aa376fcb1a7162d40d27685f7d752f9d7c57f07ba5774f5e02dee95c95`  
		Last Modified: Tue, 18 Nov 2025 07:02:27 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fc607bdb37f40b856cd79db20616896d0a315358c7d5387bed8595d25138ad`  
		Last Modified: Tue, 18 Nov 2025 07:02:31 GMT  
		Size: 40.7 MB (40705496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0bdadf93684c38f6c33be22b3dcfdbcf518d1c99047ba873707002a1553f7a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c05f82fecc6daaf2316b3eb10b83cb203f62d544a248acd69a3435668ecad4`

```dockerfile
```

-	Layers:
	-	`sha256:4f6b3900ff2c89fc3eb95492eda4ef5a7c18003a9e50edc78a7de1cb29e7c1d2`  
		Last Modified: Tue, 18 Nov 2025 08:33:46 GMT  
		Size: 7.8 MB (7777174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61dd882ab499de310fba89d437fbeef70a85cb89869a18c92296c43291513082`  
		Last Modified: Tue, 18 Nov 2025 08:33:46 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:1d88bce148d5fb10b55194d6271c8ccc3420cc8c16cab0cc609fd8580f909405
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:b229ed29a825f1ed51226e3190924be2bbf6501ba5c17af269c66c6046d1acf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185432999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3fbaf9c94fb1ce43ddb308a5fbc940e1dfdcafdaec0e33884068ff708400af`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 10:27:50 GMT
MAINTAINER AntonOks
# Tue, 18 Nov 2025 10:27:50 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 18 Nov 2025 10:27:50 GMT
ARG rakudo_version=2025.10-01
# Tue, 18 Nov 2025 10:27:50 GMT
ENV rakudo_version=2025.10-01
# Tue, 18 Nov 2025 10:40:41 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 10:40:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 18 Nov 2025 10:40:41 GMT
CMD ["raku"]
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
	-	`sha256:a1ab97d0d94a8ba61e6aba1de589ad44a54344141242394b98cb66a65aebe7be`  
		Last Modified: Tue, 18 Nov 2025 10:41:02 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af0b6dd061a95a27af05560f55aa4debe9549a8e0dd6e5ec3683c0a43d7905e`  
		Last Modified: Tue, 18 Nov 2025 10:41:10 GMT  
		Size: 42.7 MB (42747298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:7b5ce24990765fe8a19f11a80e9cf8500d895010abbdb89b2c7ea541c726a01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3967969156a362ee53f7247640782bcf2dfdaae0c489d3fceb57c90fba029c66`

```dockerfile
```

-	Layers:
	-	`sha256:487c75ed8893341f9a8a8a566ec8951533e671c213b733fb4c85de9b11509e67`  
		Last Modified: Tue, 18 Nov 2025 11:34:25 GMT  
		Size: 7.8 MB (7769499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67dc3a14a44210abae2295e8a4b54e98bb4319bdc69ee589cdfe9a64856e4b48`  
		Last Modified: Tue, 18 Nov 2025 11:34:25 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:25468224abbc2e32aee53f05248dea53ed0d32e327d9383a5ae0c423fb2c023f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182964743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3c02669e673ade7194607a141bc72bd300566c7f6c91ab7cac23f09e2d028b`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:42:56 GMT
MAINTAINER AntonOks
# Tue, 18 Nov 2025 06:42:56 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 18 Nov 2025 06:42:56 GMT
ARG rakudo_version=2025.10-01
# Tue, 18 Nov 2025 06:42:56 GMT
ENV rakudo_version=2025.10-01
# Tue, 18 Nov 2025 07:01:48 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 07:01:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 18 Nov 2025 07:01:48 GMT
CMD ["raku"]
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
	-	`sha256:7c1925aa376fcb1a7162d40d27685f7d752f9d7c57f07ba5774f5e02dee95c95`  
		Last Modified: Tue, 18 Nov 2025 07:02:27 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fc607bdb37f40b856cd79db20616896d0a315358c7d5387bed8595d25138ad`  
		Last Modified: Tue, 18 Nov 2025 07:02:31 GMT  
		Size: 40.7 MB (40705496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0bdadf93684c38f6c33be22b3dcfdbcf518d1c99047ba873707002a1553f7a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c05f82fecc6daaf2316b3eb10b83cb203f62d544a248acd69a3435668ecad4`

```dockerfile
```

-	Layers:
	-	`sha256:4f6b3900ff2c89fc3eb95492eda4ef5a7c18003a9e50edc78a7de1cb29e7c1d2`  
		Last Modified: Tue, 18 Nov 2025 08:33:46 GMT  
		Size: 7.8 MB (7777174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61dd882ab499de310fba89d437fbeef70a85cb89869a18c92296c43291513082`  
		Last Modified: Tue, 18 Nov 2025 08:33:46 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
