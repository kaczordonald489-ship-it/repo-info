## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:8c64b75dcb596da2dd83af333682f19854503ae7adf86f2eadbefa9ec7c0959b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f7504b47e56d4a394ffb4be2f4f41be4b9976220129e373796edde0aac16250f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142682459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139b7538c8cedf40fe106254b98760a17472bd62b383c1be3d6a912eb5cefccf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:05e7463d35a640281fa7b2d0e13b71033526a3ef0c4558442cec9b4a76212ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a5f3c5542b5e1b22f1c73c519b2bd7bf10ee0326281febd1bffed4be2589d0`

```dockerfile
```

-	Layers:
	-	`sha256:fdb97658eb26008939c970c83b3ee589952f919d9f3f4174b2ec93a5c2f6a381`  
		Last Modified: Tue, 18 Nov 2025 08:22:26 GMT  
		Size: 7.8 MB (7767098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52025aad70b87df05844e89b6d699f4c4e590822a0884321969c5628af4382b`  
		Last Modified: Tue, 18 Nov 2025 08:22:27 GMT  
		Size: 7.6 KB (7576 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:3c5349ddc66cf26aa904fe60d8d1c3dee89e7250b4345c3934313c7326a54f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137113161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d017d60aabc3a37c08a45c11283ed275ce991e788e15d6c7a8c2d9795cc4263d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:08:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d5c9e476f1b8d1f67ce6ab99ac45c57bfe3b7cbada7b61c1dbd969f0656bfff9`  
		Last Modified: Tue, 18 Nov 2025 01:14:11 GMT  
		Size: 47.4 MB (47448757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a9b3c9a263aa4b01f8e95a9864f401b11f5c835e6ef84b9a950304c2fcaf86`  
		Last Modified: Tue, 18 Nov 2025 03:26:45 GMT  
		Size: 24.3 MB (24345818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3022b8716a9c6d6658073ff4323d54625cb7957fc65a6802c9c4662674ae4d`  
		Last Modified: Tue, 18 Nov 2025 05:08:56 GMT  
		Size: 65.3 MB (65318586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e0427a6c109da15d0974de4080800140e468bc2229cedc6964717684506cbd5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38f786dabd23e8b977c5fbab5f650ebb70f6bcfa109cfdccefa73c662115448`

```dockerfile
```

-	Layers:
	-	`sha256:ee60055e679f8f2ec8fc0e82bcb66fad624feff28b45b2ec7386885d1d87d21c`  
		Last Modified: Tue, 18 Nov 2025 05:23:48 GMT  
		Size: 7.8 MB (7768136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4ab97ee27b5c35969e476ae721318dec1aef4ec5842d50e6626f4647d06379`  
		Last Modified: Tue, 18 Nov 2025 05:23:50 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c73a613228c3263a8df11d534643bba09bfb7a13c2953270ec53aaf838d3944d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132051717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045a8e7aba009fdedb70053d0affe816f74d0ff573327f2038f9c6a8b2d93cae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:28:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7fcec123a6a2e24d64f8dd8d3ff01f16ba0839656e71d971698d0e8151a28a21`  
		Last Modified: Tue, 18 Nov 2025 01:14:26 GMT  
		Size: 45.7 MB (45718279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebfeb92d3792e2087594f2ee9ee695fe97cc51ccaf846f755d71e0b58f7f78c`  
		Last Modified: Tue, 18 Nov 2025 04:00:39 GMT  
		Size: 23.6 MB (23620000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c45847805af09aa76d6ba7f34b42945f6767f5c3049e5027681335f35a18d5`  
		Last Modified: Tue, 18 Nov 2025 05:29:07 GMT  
		Size: 62.7 MB (62713438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7c5445d8625517ce62100970b611b5f145aaeccc6ce67bd37aa83a05878e1e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed647a205aa0c3756351e583a878836bc56dd58b2ca457157d49960a1f43fb1`

```dockerfile
```

-	Layers:
	-	`sha256:db24447a3a92bf65e9c3b7b406eda52220cb53943169149a96b62809bf355718`  
		Last Modified: Tue, 18 Nov 2025 08:22:38 GMT  
		Size: 7.8 MB (7767605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:968a6ebf002cfb3d7709e5b7c6d8e91b326e18bc0791b11317d7d578b63b07a0`  
		Last Modified: Tue, 18 Nov 2025 08:22:39 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2082675f8200ec3e813d2b879c951599acd992e804474c3fa890f32c8868120f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142256005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8bb37f8ef118943faee16135695230ccbb2f3285d9364560a5f93053b20fb7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a2057de3ad656df413711072abfa0315a1bea04f4e5ebe4d37def284860f03d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2370f9316268ff0f1d3c6345cc49d8981ba331555ed90fb29d762654d86486`

```dockerfile
```

-	Layers:
	-	`sha256:6b90abba9004b0c666c768f7afa5e6648513c094ffaadf84d3fbf4f2a4796b4d`  
		Last Modified: Tue, 18 Nov 2025 07:25:59 GMT  
		Size: 7.8 MB (7774773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13bc2c6b1fb0bc5b66745214d0c70b210e3b6b261460ab4402c860cc4318bfa8`  
		Last Modified: Tue, 18 Nov 2025 07:26:00 GMT  
		Size: 7.7 KB (7667 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e43447a9dc36a8dbd59d2398b0f6fa54938aa79c7585f3b6e16627b954a25f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147381300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d0333b66ec3e076546598ec8c5d9fc29fa0e22011f29b045e99fbe5f1bad29`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:11:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bf2a49c122745d1757b9ecb1c9b1d8252491e66b62d1c279080155aaa530a615`  
		Last Modified: Tue, 18 Nov 2025 01:13:10 GMT  
		Size: 50.8 MB (50801744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cfb736286179e6858e8b04a47a815f4071567b3b6f8b36ca52b15e872e6cea`  
		Last Modified: Tue, 18 Nov 2025 02:57:24 GMT  
		Size: 26.8 MB (26776415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c892592b339e9b2ca91d682c607a5e915b21a67ae25c1c71d1f3ef8ea35c2f`  
		Last Modified: Tue, 18 Nov 2025 04:11:31 GMT  
		Size: 69.8 MB (69803141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ecfe8678ae1eb55755576bbddd3f37f909725400a81483df5eb0bb12a34fc352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b63eec5f067ddbe011e27582427f2e054e092f205101eb25a1a638fc408e7c`

```dockerfile
```

-	Layers:
	-	`sha256:50b50977440e8328cbf379a840b446017044007247084dc18e932e535db6b678`  
		Last Modified: Tue, 18 Nov 2025 06:29:36 GMT  
		Size: 7.8 MB (7763233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f0679acabae42cb265606a66e592ba139e5a65a5866aa0c3aaf4d3b029ff7a`  
		Last Modified: Tue, 18 Nov 2025 06:29:37 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1a99f5c83d8fbddea17d00c4e9380178fab7e833e7d2934479906f5398daabb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153127307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6112f12909ae70305bcf7f1fb4ab5fefe35ffcfbaa00856920f8bce886807537`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a859b52534a1e3522c593c1835bd1bee34ff20a865f32f140257d45048a18099`  
		Last Modified: Tue, 18 Nov 2025 04:09:23 GMT  
		Size: 27.0 MB (26996919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba2b1a22ff6e7093fdd1dd2648adedf5202ef1304de7d17f711c19601d3a80e`  
		Last Modified: Tue, 18 Nov 2025 06:54:27 GMT  
		Size: 73.0 MB (73021903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:44d54013654f423b30611286dc39d13685cfb0a612d7316791f74361fee98f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7781835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796087633620ab195c4f5de5ee7e12d5157f002c12e332874ae4b9d7772d9319`

```dockerfile
```

-	Layers:
	-	`sha256:5c8ad47d2395a36a42430517e855c0b07f3e55e2150c087a7cb213bcf21dbb6b`  
		Last Modified: Tue, 18 Nov 2025 08:23:30 GMT  
		Size: 7.8 MB (7774221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61782dfb82b59570fd6e0aa6ff2c8a00fa86da489a71fdc3667b014657fd7456`  
		Last Modified: Tue, 18 Nov 2025 08:23:31 GMT  
		Size: 7.6 KB (7614 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:924ffd884e01570727de703d26ae0dea0dd1604f3e9c85e4ceb91612cc677e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139385892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5796e5655ad623f7799014b6935d28f268f08adb711c694472e5bbae988eadb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccc0dcc6b4231d5f1f223a1330c6630cb9406136f8e738cb2b0e628d1b35022`  
		Last Modified: Wed, 19 Nov 2025 19:38:34 GMT  
		Size: 25.0 MB (24953736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e592ded610a658bb788aebd62d933a07876ce0d2dff630e8511ac1eda3d0dbb`  
		Last Modified: Thu, 20 Nov 2025 22:32:10 GMT  
		Size: 66.7 MB (66660961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bfcb8c69548df6a7f74340a2d4163b0ea23b8f6f69ce6d00fa3f37caa2144035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7764548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1314230f267dc253ea996c17b9922b8946650ed819a259a6ad145660b87d7775`

```dockerfile
```

-	Layers:
	-	`sha256:a2e089966829390c0f9637532002fc0265450b99a5671c839ed9fad083615930`  
		Last Modified: Thu, 20 Nov 2025 23:20:58 GMT  
		Size: 7.8 MB (7756934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:246b2716222c918bd3f89389468a0a47e0077dc1012b81410c53a506f9457f6f`  
		Last Modified: Thu, 20 Nov 2025 23:20:59 GMT  
		Size: 7.6 KB (7614 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0a7a33d7eb4553375570116b5616d7761dc4d6e134d9c24900f1207bc54476b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144756609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd11f2ffaf6dd2bf261d3af758ab25ae16f2d013f989fc2ccda214682fe5ba1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:57:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f811fd500c593f696ff4afefd96c823d7f8788d50f510057207bfc40b4a405ca`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 26.8 MB (26786539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4530c943529730620c01f6bab681e114e8a52bebc697a9164bab0bee08dc992`  
		Last Modified: Tue, 18 Nov 2025 05:58:03 GMT  
		Size: 68.6 MB (68624056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:768d572c83de365a61358fa92ec594649dae312db41d516d8f03b727ebd5fa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2e626729d72d471e736047d9d196850c2cd8100e0bb3b4e26a47494851d2ed`

```dockerfile
```

-	Layers:
	-	`sha256:547c90bd31c78643ef1e73b5db9671a894bc6ab3f8ce6117e2eabcf4df3beb31`  
		Last Modified: Tue, 18 Nov 2025 08:23:45 GMT  
		Size: 7.8 MB (7768011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c23a9c5cb095ddc343ac0b2712073d4ea32905896e7967e16930154ff4fd19f3`  
		Last Modified: Tue, 18 Nov 2025 08:23:45 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json
