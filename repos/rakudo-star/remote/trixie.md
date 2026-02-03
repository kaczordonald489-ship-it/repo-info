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
