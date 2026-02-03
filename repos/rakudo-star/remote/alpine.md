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
