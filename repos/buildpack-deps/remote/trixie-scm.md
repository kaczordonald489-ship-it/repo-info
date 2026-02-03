## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:f631bf9350714f68434d1e59476ed861b0511cb095d07210713434b1f2b76260
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

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5c5b5da89cdd86faf7ff0c6e8bb50810243de0d29637e5e3631aaf47ae5e0e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142694327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842eb5a29781a9a10657f19a02947411ad712c3a28e3a22146978b4b936597d5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a801a197b98d08220fd2a305594ef7cbf648d9ddde72d2527770ba6a7efd85c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008073465692f101a2358345e4c0616d4669e89e8e9d23bbcd90ce564f60379d`

```dockerfile
```

-	Layers:
	-	`sha256:1fb65264ebca1e5a8048e81fb69d7acf9249e59a056fb8f2a352854f334a4d02`  
		Last Modified: Tue, 03 Feb 2026 03:29:15 GMT  
		Size: 7.8 MB (7768137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ab5b1e13baac6d66f0a02dfa0f3284fb47aafac367f01b742edbda5ea96fc0a`  
		Last Modified: Tue, 03 Feb 2026 03:29:14 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c5c55cd655a8fae099ebc471570380ac70dbc6071eb1a8c4eb4a33c25576ecdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137127956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04bb7166728deba532b567265b8bedabc44a23154e7c348ce01ef0afca04d66f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:17:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ba31dc65cf53cae37b5517f251f4d408e91109de491cbd8816a9f21c33a05203`  
		Last Modified: Tue, 03 Feb 2026 01:14:09 GMT  
		Size: 47.5 MB (47453997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91afe525ee94a6eec8f0285b6d37bd019b53a0d3e972edf130127870dbcc171e`  
		Last Modified: Tue, 03 Feb 2026 03:26:40 GMT  
		Size: 24.4 MB (24355517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648cbf60fd3bc74c2c5bd50ba637a7b59518c4e57992aeed5e381e96d894fe6e`  
		Last Modified: Tue, 03 Feb 2026 05:17:31 GMT  
		Size: 65.3 MB (65318442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a5f026523b38dd8d8d67271d8307b92251767a0ae84b532c212b0be280fed5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f99a263c302837df177a91994283d7c72f5c7d31e295609a21bf63c7d3f01db`

```dockerfile
```

-	Layers:
	-	`sha256:cdf538eed5337c25982de0eebf6745ffdf2de024c80562e4f000ff17dd3aaf54`  
		Last Modified: Tue, 03 Feb 2026 05:17:30 GMT  
		Size: 7.8 MB (7769175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8eda677236205e1833c35968fc08f61c33b7b78fc7981596dc0ae70d7e72a32`  
		Last Modified: Tue, 03 Feb 2026 05:17:29 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8549daf1a1e941fa81a5a86b661a6eb23bacc0dc5adae38ff2b801a868f7c85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132066852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c6db34e411fe8655f5031eb77bc2b5f21a417de771eba6b430e1869fdb3c29`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:32:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:01:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e712004ad7e72ac7b512e7e067d08c1f627b7b81a230302cbad4864b08acbdff`  
		Last Modified: Tue, 03 Feb 2026 01:14:45 GMT  
		Size: 45.7 MB (45724966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db74387350d2cb71494f8cd51684a1223fa4d67c2770958430649aa3d99f0d84`  
		Last Modified: Tue, 03 Feb 2026 03:32:37 GMT  
		Size: 23.6 MB (23628323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27eaf2b8f43157ee85fb0c9ace18005d09181f51842f1543a4a0e4d1072f633e`  
		Last Modified: Tue, 03 Feb 2026 05:01:35 GMT  
		Size: 62.7 MB (62713563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5c1ae6bfa1d528ec9579008b9b2adeb11df279da6a20561e52e90e47c190243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ac56f766b0b65a62659351e266163cbcc89bd8172917d4f4dc60c28c877685`

```dockerfile
```

-	Layers:
	-	`sha256:927305f03fc29e5ea0a2a8bc8ef5f3ee31b07084d978501dfd64388d637370f6`  
		Last Modified: Tue, 03 Feb 2026 05:01:33 GMT  
		Size: 7.8 MB (7768644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:995c8fa5731296690898d55a372fedef03e40518a75135b8459d130ec29a45b3`  
		Last Modified: Tue, 03 Feb 2026 05:01:33 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8ed7c2fa5019586f755d65e9da0acbf49ebde0388e5f990afdc3969bf598e473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142267710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1356403f84aecc7f753af882c9c66206218fb30f5b68fc277f048b16e409ccf8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f4f46007d9ad27f99c60569b770189c0639f72b4b86e88cdd8a230f7178b8d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e675231b240c951054a7c9d63a189fb1a8f6bff5814a1cc9b6736f9356e387`

```dockerfile
```

-	Layers:
	-	`sha256:3c87d7725f1c3548471006345233f92086669122832aa65b33d073cec0c04445`  
		Last Modified: Tue, 03 Feb 2026 03:47:29 GMT  
		Size: 7.8 MB (7775812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c62bfc31a01cc28a9ac46a9a6183985ebce864ff817cb746debd8a746a885a13`  
		Last Modified: Tue, 03 Feb 2026 03:47:28 GMT  
		Size: 7.7 KB (7669 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7e2365f8a185772bc039ad0cdd79c61ec586f89a43e3b12410154b88bff1b9cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147386699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891820f0cc8bda38b0b4334e92e2e91047afe53bbd28fbf81f28a9a94b935cb6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b536877d3c0a030ad79a6593cd07fd6d9d694a4ee908632c85159f47caa880c2`  
		Last Modified: Tue, 03 Feb 2026 01:15:09 GMT  
		Size: 50.8 MB (50805135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82aa8569021d347e27d65aa0b48a5747ad08b2dd9fedb936660291f168eeed9`  
		Last Modified: Tue, 03 Feb 2026 02:49:59 GMT  
		Size: 26.8 MB (26778421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa32f4c52b58b9468e88e7cde44c8447ca98c8e3cdb99900c08bada90da980a`  
		Last Modified: Tue, 03 Feb 2026 03:25:16 GMT  
		Size: 69.8 MB (69803143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a133febfa9433ee6723f0638968ef9d69e924006716a8e668298a100c13dbf5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53cab7c16106394b710d8fdb50298aced4868a454a289bfb3b1210d4485174e4`

```dockerfile
```

-	Layers:
	-	`sha256:0590dcee78dcad0783853e164e0f274f3a6f96f45c6abf63829da7bbef963312`  
		Last Modified: Tue, 03 Feb 2026 03:25:14 GMT  
		Size: 7.8 MB (7764271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc1c1f25fc3d9e72bdb0196939cde72a09483683c268f27b33e54a69cfa44507`  
		Last Modified: Tue, 03 Feb 2026 03:25:14 GMT  
		Size: 7.5 KB (7549 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e9ef3588e582d716036b46b3cea0a0ef3087d286c7b815803b0decbb02d08f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153142622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724533d97ca88754dd019fe93718b23914a53eb407cddf2cbfd6c8e4e0f3297a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 09:15:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 15:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21554c0ffe7aa9121703873815aca94dbbdf6352a46266dc923fc9e36d0d58a`  
		Last Modified: Tue, 13 Jan 2026 09:18:01 GMT  
		Size: 27.0 MB (26998052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb58d20828d54df35a08218c574236606c9e3ab14d0f2ddf036e12abcf8c85d6`  
		Last Modified: Tue, 13 Jan 2026 15:19:44 GMT  
		Size: 73.0 MB (73037608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:79133d6ea3b15bd38b4ddf35b938acebe8833849debdc608b764df6811a75141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e29c3dc2fecd5f53fe5ecaec87a106a215037149db7ed8b9034c2d62dd0fdf`

```dockerfile
```

-	Layers:
	-	`sha256:680bd22d091af24ea8e1f849f1fba33a962ac2b424501d61c1bdc3fc28f47180`  
		Last Modified: Tue, 13 Jan 2026 15:19:42 GMT  
		Size: 7.8 MB (7775262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a21380fddd3f94a0c3c6b267d13cf32f3b935972d834a641f6dd56c9e8b264fc`  
		Last Modified: Tue, 13 Jan 2026 15:19:41 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:53e1918b4deac0b4598e1fdfbc88769a8f0924d91eac8915b7b22b3a57c21203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139384293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb34c3f8fb6ebda9e1cb3c71c7e8eae5dec197cde055e4c9c0f454c5afc829a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:47:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 18 Jan 2026 22:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:14 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7f36a5fa281a3384abd9a90a26442f28edb507f1b9c537a07e1f5aaeb769a1`  
		Last Modified: Fri, 16 Jan 2026 06:49:07 GMT  
		Size: 25.0 MB (24952736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11f745939b2d13a20bc5767dafb02ca8b86a288cc70e3062fa70de76ce5b598`  
		Last Modified: Sun, 18 Jan 2026 23:01:52 GMT  
		Size: 66.7 MB (66660714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2845c2c3ccb02dbec66ac5d9fbade10de664b74c2d072f324623f748e495c74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7765590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6255002d2707a250f316d37c2b44f689b25717cf0696a16821b21f73cc8c084`

```dockerfile
```

-	Layers:
	-	`sha256:9b842e6b5610b0727d6bdf7f25e7ca60c625e25d3fcd9ed1cd3561529bd9326f`  
		Last Modified: Sun, 18 Jan 2026 23:01:44 GMT  
		Size: 7.8 MB (7757975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ae934fa04e1af77b7b48d655ea57c1540bde0086341b5a6b4b64c284991b19f`  
		Last Modified: Sun, 18 Jan 2026 23:01:42 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1273ac48e517d3e53cdb6672baf95adb567d8733ae867cc73e84852f71c12db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144772210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588717059e6f395a752b2375a1cb6d5752511b5d5189348b05fbdb1420b89d6b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:29:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef24c0cb82fa1ab6f1887f140586ec94ae060d22e6053b5747ce4acc96547b39`  
		Last Modified: Tue, 03 Feb 2026 03:45:31 GMT  
		Size: 26.8 MB (26794717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec3c6a3ae754d274216ffbec3754da469ace4e7c5b6e8e123969f0516b4a968`  
		Last Modified: Tue, 03 Feb 2026 05:29:44 GMT  
		Size: 68.6 MB (68623115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e1560589c3986e63d5cb16738fe663a91dcadc5c60127bcde34d5d045c9bbdc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bb9facd52c9bfddc170fbbeca2cf0899e728de2a767ddd677bcab56e8efa15`

```dockerfile
```

-	Layers:
	-	`sha256:296cf597549da352641e169c8052352ec5eaacd53a4dba74b4269c6e7272b631`  
		Last Modified: Tue, 03 Feb 2026 05:29:42 GMT  
		Size: 7.8 MB (7769050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6903e7b5d9f04544ae90e406c6085e66d899da93f1017ebf0dab9db72f5b5566`  
		Last Modified: Tue, 03 Feb 2026 05:29:42 GMT  
		Size: 7.6 KB (7576 bytes)  
		MIME: application/vnd.in-toto+json
