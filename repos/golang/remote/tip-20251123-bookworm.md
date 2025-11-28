## `golang:tip-20251123-bookworm`

```console
$ docker pull golang@sha256:257b60211231fc17690126857fac551fc8defa33614cc566e31ad3118dbf06a2
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20251123-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:7378012e6a092d7bfa645da1ab525869d1c15abce67d1befd5f39eb13394184a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321752229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4903cb827fb383d92f9ff87d01aa7e02933efc763c87dfd747421a2f6bcb2fd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:35:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:37:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:01 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:01 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:37:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:37:04 GMT
WORKDIR /go
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
	-	`sha256:23898ea9e95d38a7fa26a740eec7a5f29644e93dfe7705a105cf79d71f1af091`  
		Last Modified: Tue, 25 Nov 2025 01:03:10 GMT  
		Size: 92.4 MB (92410470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5d9efbcfd700910b298e2e1f088186b48b23d603a67b46866474897785fcf4`  
		Last Modified: Mon, 24 Nov 2025 23:12:20 GMT  
		Size: 92.4 MB (92435230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ce91da475b9718dda9e5bdc9194ec5bb56902ff7f580b2f3d5a6fb24408a33`  
		Last Modified: Mon, 24 Nov 2025 22:37:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251123-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:bbe07079e606c1e9835da28f501a23e620b83829264201f1c8b9ef42cb3119cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72466f3c11bd3a8cfeae392984ff3c3380cb035d4a8f81f1dc054f9b9b2b8746`

```dockerfile
```

-	Layers:
	-	`sha256:eac092b67f9d5778dbcfa7cadf2f1867d3f99772a4ae9c23f54515a3d76a201b`  
		Last Modified: Tue, 25 Nov 2025 00:24:50 GMT  
		Size: 10.5 MB (10496388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b9edc92e04bb47df6b033b0e45cf828e45dac7a528574970eb2794712c93f0`  
		Last Modified: Tue, 25 Nov 2025 00:24:50 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251123-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:85565310405a58c1fa70e58920f72741c56abc1ec1d12d4f9ae182fbfad5b230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280613435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef4ae85b21ae43e44c2bb8938041c0114452c92d2f3862b05bdce53b936e177`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:35:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:38:06 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:38:06 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:38:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:38:06 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:38:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:38:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b6eb0fb27a6d99b6b7a2a32ab126d30b16ebd113a3a3e174d37a032cde9bd1`  
		Last Modified: Tue, 18 Nov 2025 05:28:17 GMT  
		Size: 59.7 MB (59652137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985ebc4fe1044c31691cbecf94f64c02923ed320124138fecd032457ead267cc`  
		Last Modified: Mon, 24 Nov 2025 22:38:59 GMT  
		Size: 66.3 MB (66276370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84acd51792b44af9faab6b3fd0d7f172d2f21a4324de65288c305f1fa5a5cb15`  
		Last Modified: Mon, 24 Nov 2025 22:38:11 GMT  
		Size: 88.6 MB (88553959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951a3038821d0891d3651c3c75f9a7aef8c9448c2a8b230df9ac7fcb03b1ea6a`  
		Last Modified: Mon, 24 Nov 2025 22:38:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251123-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:eb06b64ef237a4cf411965d09ceb8c9e91797d48a08ce2e310ab57227881f304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05201895d523d0aedf4b3059e6121f75467f2385f17c86125919ec4752bbd10c`

```dockerfile
```

-	Layers:
	-	`sha256:00450687b040dbfcf73d3648ac508e4384f6ab02074381920f700041307d48e0`  
		Last Modified: Tue, 25 Nov 2025 00:24:59 GMT  
		Size: 10.3 MB (10303084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbc1e72dce2a8959802bbf42f8c73b134f0845762078322b9e7f63769a25850f`  
		Last Modified: Tue, 25 Nov 2025 00:25:00 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251123-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:0b537cd36e396244fd409c9781611913bc51ba3b05c46215ff89be3a69c0e37e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310439818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d65fad141cd0ba1bae8666617541236123bbe4b4f48ac6666b053ad9beda9b4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:34:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:36:28 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:36:28 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:36:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:36:28 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:36:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:36:31 GMT
WORKDIR /go
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
	-	`sha256:1ff9524becb8880f3a3779f1782f9fe4f78b9e1576ac91a59bb6421f006b45bc`  
		Last Modified: Mon, 24 Nov 2025 22:37:33 GMT  
		Size: 86.5 MB (86490928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c063ea817571a2589abbf80a2044e326fd503e0a108dc319a7ad8231dbc1d73`  
		Last Modified: Mon, 24 Nov 2025 22:37:19 GMT  
		Size: 87.6 MB (87619860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6082f3a763cb2670efd00a60646d9eb6ed2a73f36215c1739c2a505be8fc2bed`  
		Last Modified: Mon, 24 Nov 2025 22:37:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251123-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7beb598f60c92069868ea5a09eeda996170e0e2fc64cf3b9b64cc3971f1fa60a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1128d0b2a2685b49724b7e9fad78cc261171f124501e76f28c48b8add488abcd`

```dockerfile
```

-	Layers:
	-	`sha256:a8deb517d086deddb938672f5252c680cccd70bc3ececbf065dd50accbd1ade6`  
		Last Modified: Tue, 25 Nov 2025 00:25:13 GMT  
		Size: 10.5 MB (10524212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:582b354a9d6738ece07c4a77f061e11e35fcf51edd942e3fe59bb1c40f8f695e`  
		Last Modified: Tue, 25 Nov 2025 00:25:14 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251123-bookworm` - linux; 386

```console
$ docker pull golang@sha256:a60622fa662fd0b721e1017fa7bf398a41171c01157318b274b3b470e6b8f1f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320768439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8a0f1d23ae3c6474e06133de819e6ebeae5a7b349c7b3ce60acc3daa53344a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:56:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:08:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:36:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:38:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:38:01 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:38:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:38:01 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:38:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:38:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1ac37f50532a7306717e1be2f4760a581740981b55bfee41fb74edf971bbbb`  
		Last Modified: Tue, 18 Nov 2025 02:56:28 GMT  
		Size: 24.9 MB (24864418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931488dec4785216610c9f2c064b20b308e9839859b58a6fb0171606dd6f0514`  
		Last Modified: Tue, 18 Nov 2025 04:08:56 GMT  
		Size: 66.2 MB (66233867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3064790412fb3ad4c94fd92eefd086558ab407d5bf5b13c4fa587d36d83ec9c7`  
		Last Modified: Mon, 24 Nov 2025 22:38:46 GMT  
		Size: 89.8 MB (89839841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba70aedae48e82029642c62322f6ff74fb35e5b6234375d05c3be6a27f83fa3f`  
		Last Modified: Tue, 25 Nov 2025 02:11:57 GMT  
		Size: 90.4 MB (90363290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7613fd06032541683f88630b9eb324b36308e015d863b8a94557befc67c30df`  
		Last Modified: Mon, 24 Nov 2025 22:38:37 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251123-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:05041ac8bb1c9a9dcf9bf1e270348db07baec9fb72e37924fc46834274b67a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85c4b3188dfb922de49d03813ed488dc11ed1472bfe464459467c6eb02f75a9`

```dockerfile
```

-	Layers:
	-	`sha256:819fbefc30d98d2212fd6cb8765012243718131637db93258bee6d964ae288fa`  
		Last Modified: Tue, 25 Nov 2025 00:25:24 GMT  
		Size: 10.5 MB (10475969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3ccafeff8a7ca8629137f7ed39b2c403fe3a1ca7c6586a553d3b2bb7c8d619e`  
		Last Modified: Tue, 25 Nov 2025 00:25:25 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251123-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:6cf4cd42ee23beb198e4dc4b55a6edca44da60e4b98d9647fe178169d15681a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (292030751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc22087a3dfb013453acd41829d1e4f605b474257e9f2083202f6ae089458537`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 19:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:11:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 23:35:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:53:38 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:53:38 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:53:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:53:38 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:53:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:53:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6d4a3f53f449c0e9b84d889c71d1f21df5764d821465bd1337060660aa78c65e`  
		Last Modified: Tue, 18 Nov 2025 01:11:17 GMT  
		Size: 48.8 MB (48760956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754bf41c56cb3beefc6b6211c26bdc048d41c337f12bc0bbfcfa89dfb5de99b7`  
		Last Modified: Tue, 18 Nov 2025 19:40:58 GMT  
		Size: 23.6 MB (23614038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7a4cb619dbd7fcb3e0be3246f973ccbe692039c1fd01a193751c60045de0d3`  
		Last Modified: Tue, 18 Nov 2025 22:12:34 GMT  
		Size: 63.3 MB (63309296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870c654cc97051b29e543234a565ca86980db6e2499d45b06d4424741a820d98`  
		Last Modified: Tue, 18 Nov 2025 23:38:02 GMT  
		Size: 70.0 MB (70016928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0621f3d4859af91aa14414a2d03a825e3e47b57f35ed253c9c6eaa391e1a81`  
		Last Modified: Mon, 24 Nov 2025 22:56:12 GMT  
		Size: 86.3 MB (86329376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193e0c2cbc65bbc299d93902ea15e9bfbf9eadd7b1cf4c77b682db37f4d01e77`  
		Last Modified: Mon, 24 Nov 2025 22:56:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251123-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:22c3cad0c559a293cea942c098d20b9a625e2a5b04a9b6482e5acb14f9e60fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e545d49a6f5e9a5bf82474e87fd90d5a4289d354ab013df06b396a70172f9b5e`

```dockerfile
```

-	Layers:
	-	`sha256:69fcf7d0ae9512d3d41ac8b0f8b03e5dbd89e1798b92a41ef3ff37519c3a2bd8`  
		Last Modified: Tue, 25 Nov 2025 00:25:32 GMT  
		Size: 27.1 KB (27124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251123-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:138ae099e07d1b1be820f3f72ba484f07b0719b6622463575dcbd8b841a167c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327337163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543d661cdad5023f68a5ebbd345477563879fea66b5c6bbc3146b62a6ff4d08b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:51:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:37:36 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:36 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:36 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:38:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:38:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17787af1df16ce560e48a9be892094ace19b1aecc7f06ca1e97a2e20987822a5`  
		Last Modified: Tue, 18 Nov 2025 04:05:05 GMT  
		Size: 25.7 MB (25672018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4d717b62eb888bb16cb77af768613d5d676b28f09ab1cb591a5130af4b846f`  
		Last Modified: Tue, 18 Nov 2025 06:52:50 GMT  
		Size: 69.8 MB (69845622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88994869d0f332cc70ccbb2ca7f72eb4c56d6ad96b9820d58b6d3da3c3f1260c`  
		Last Modified: Mon, 24 Nov 2025 22:40:06 GMT  
		Size: 90.4 MB (90419974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c192b4221bdae7479c6a0a0cefbefa83b4b143b2a4b40e323ae02e100ce6102`  
		Last Modified: Mon, 24 Nov 2025 22:46:59 GMT  
		Size: 89.1 MB (89072428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097e949bcbfe658730f43f435da764411835bba10bb200a335dbd8e2af9a3f19`  
		Last Modified: Mon, 24 Nov 2025 22:38:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251123-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:41bddaf61c92f70df304d64bf1d9fa719419f76de9ca758080e89caf4955b735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c4518fbbdb50f6ba1e8ee72b402447dee282b5f14515fa8bea103bd154acd3`

```dockerfile
```

-	Layers:
	-	`sha256:ad8a529c3f3f8326f63fe2b77df347a0af21d19dc02f15cd367f1e26960bf12d`  
		Last Modified: Tue, 25 Nov 2025 00:25:42 GMT  
		Size: 10.5 MB (10468871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44945b5084ff32c49ec8b74999c0ef7190701e2b12b489d0d2f8adc3e06ef15c`  
		Last Modified: Tue, 25 Nov 2025 00:25:42 GMT  
		Size: 28.3 KB (28259 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251123-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:1ad10fde60a72bdc54fc195528ef46d2d81f1d8b5ca5cfa4e2ac16306c23510c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.3 MB (294301499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e3a0013f56016767c970c0519b34d49617382350de2368796a59fd4ee57f8d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:56:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:38:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:37:54 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:54 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:54 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:38:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:38:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f80247bcc58a5a903807561f3aad626158855a07b7817a9ed9975e9775ae2`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 24.0 MB (24027180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b099f215b279a7199da193e9e90d7e8e46ea9dfcda3ebe6c6379eb56d436eeae`  
		Last Modified: Tue, 18 Nov 2025 05:57:22 GMT  
		Size: 63.5 MB (63501447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071a07a79185a61d38508c944e9242334a0616777b127368548ba02277054991`  
		Last Modified: Mon, 24 Nov 2025 22:39:03 GMT  
		Size: 69.0 MB (69011120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c00d64c48f24f624221defe9715cae4847baad7ac3f98d927259b00270c75f2`  
		Last Modified: Tue, 25 Nov 2025 02:17:38 GMT  
		Size: 90.6 MB (90623953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c52bb7878853e705659ea4a48b6af8c3e6e202638de0e226391e3da8f5aa9ff`  
		Last Modified: Mon, 24 Nov 2025 22:38:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251123-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c06bd753fea82eb8637a812dd64865cd566bd560cbb239e10f52bf3e12445f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10356358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af9f89b88f9db06624b4ef010eb344c8a15b2d457e5910b1b8ce244dca157a1`

```dockerfile
```

-	Layers:
	-	`sha256:79c540a09414651eb0b6aff508db78bc62375b7c22eb20c8bbddc849e200d6c4`  
		Last Modified: Tue, 25 Nov 2025 00:25:52 GMT  
		Size: 10.3 MB (10328146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:816439250af92c1858a12f6c84e6016ce804c10c6b25b4b910b0f62e7d46d1c8`  
		Last Modified: Tue, 25 Nov 2025 00:25:53 GMT  
		Size: 28.2 KB (28212 bytes)  
		MIME: application/vnd.in-toto+json
