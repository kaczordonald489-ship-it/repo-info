## `golang:bookworm`

```console
$ docker pull golang@sha256:75c31c9595563297055cea3ded8a3ec346a08e28f62d8cebfcc8ccad431dbe56
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

### `golang:bookworm` - linux; amd64

```console
$ docker pull golang@sha256:3c6d396d2248ce87bf47a45a418d44f899b27c225dcc34acf57a219ee850c375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289503776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa4affaa97b8f2ac6c9395a818712044c04d45197c9ebe645aa26322ef0e201`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:17:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:17:48 GMT
ENV GOLANG_VERSION=1.25.6
# Tue, 03 Feb 2026 04:17:48 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 04:17:48 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 04:17:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:17:48 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 04:17:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 04:17:52 GMT
WORKDIR /go
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
	-	`sha256:c3d56898ffd4e809d7eb4012ec17a3668dfb9a3aaa78b457b5d1f5149128a2e8`  
		Last Modified: Tue, 03 Feb 2026 04:18:18 GMT  
		Size: 92.4 MB (92433428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c503e035cd5c1ea67986d21ed1fb2f4305f801555c52f9f16ce0f0f5cf2e16`  
		Last Modified: Thu, 15 Jan 2026 19:31:09 GMT  
		Size: 60.2 MB (60154290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7694fe2a66e86ff2eba641217bc6eac8c9e4f1c67400806d393b7dbf0bd9bde0`  
		Last Modified: Tue, 03 Feb 2026 04:18:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fba4f0fa2ae9f1696617445541cb476bfcc1eaf6396c3b4132492d87f3f332f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5515d18f7587e435b8655de4df158e2a0ccad338433decb1feef6f517d3f1f99`

```dockerfile
```

-	Layers:
	-	`sha256:616604797a79a61a178326185ad17c6e923bd810d3a2c601cc9a34a67de54de1`  
		Last Modified: Tue, 03 Feb 2026 04:18:16 GMT  
		Size: 10.5 MB (10496383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:746b5e3e1868cf843ed76f6286c73aac06bccf4e0506f59ae5c2e4be21364ce3`  
		Last Modified: Tue, 03 Feb 2026 04:18:15 GMT  
		Size: 27.8 KB (27797 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:cb4fa8ab1510d8d9ad1f746de47dadcd5f61ea9df0df8faba3d0ede193f5fcfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251155515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf37e48b495b381dcdb3e6085e876d58bd186562525d047c368fb9a1dc3e2c5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:21:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:21:32 GMT
ENV GOLANG_VERSION=1.25.6
# Tue, 03 Feb 2026 05:21:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 05:21:32 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 05:21:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:21:32 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 05:21:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 05:21:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:424cab4c9a6a41cd57ee6de8e95726c4d76fe3e913bd9c7731865fd244771971`  
		Last Modified: Tue, 03 Feb 2026 01:13:26 GMT  
		Size: 44.2 MB (44198733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7fc27aeb6b79b5764735a819c5fdf5feb13c904bdffa0dee2b4c1c5f3935e7`  
		Last Modified: Tue, 03 Feb 2026 03:30:05 GMT  
		Size: 21.9 MB (21942045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb0551578bad740c3a20b6a29166ce3ad8980e037c23d30c90a060f62da5338`  
		Last Modified: Tue, 03 Feb 2026 05:00:10 GMT  
		Size: 59.7 MB (59651962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f8f217b1a3c7fdec789b773e5361c31ebf97ab562cd30f44b6bc8038127213`  
		Last Modified: Tue, 03 Feb 2026 05:21:59 GMT  
		Size: 66.3 MB (66288807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9858bd230951a4669967b265976b2f7dbd9f374059998fadb8d8956bf7de2a2`  
		Last Modified: Thu, 15 Jan 2026 19:30:05 GMT  
		Size: 59.1 MB (59073810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c115a06cfcfe320e7c5171f48193ae6e9269c23b5b7f84893900aa19e12746`  
		Last Modified: Tue, 03 Feb 2026 05:21:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:904b11a3e8ee80bc5e9498403efe0d9a609cff34257a8f4accc798d113d06005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6eef8f0f8c0f0c758dd83602adf1b8cace3ea365a462160ed5ee70952411a2b`

```dockerfile
```

-	Layers:
	-	`sha256:ce6091e87acd41a3b2b7bfc58e33a5fa4cf1b279bd3fb14ad61dc9b329ded732`  
		Last Modified: Tue, 03 Feb 2026 05:21:58 GMT  
		Size: 10.3 MB (10303097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0dea420bc1fee1e8532aa237415ef486af8431c39903175d0f5f2e820ce10a8`  
		Last Modified: Tue, 03 Feb 2026 05:21:57 GMT  
		Size: 27.9 KB (27903 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1efabe7cb767b0153c5aaff88b290d582ff9bdad452e1240e7a0dc8ead18d476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280616183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b642dc8c5cd54eb4f4219e85aaf215cb47ae316ef381ce374d69535e88cd821d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:21:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:21:55 GMT
ENV GOLANG_VERSION=1.25.6
# Tue, 03 Feb 2026 04:21:55 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 04:21:55 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 04:21:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:21:55 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 04:22:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 04:22:00 GMT
WORKDIR /go
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
	-	`sha256:d461d84e8690415ec23828f563fc5f68b5877bb57f6ffcc1207c622da4e44952`  
		Last Modified: Tue, 03 Feb 2026 04:22:24 GMT  
		Size: 86.5 MB (86506345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a2f381e4cd3963e3af5194953e3e2807c452e833bf69397dee70610e428e6`  
		Last Modified: Thu, 15 Jan 2026 19:30:21 GMT  
		Size: 57.7 MB (57659196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910f998782dbdf00fc18bca12bacfe89d896caf70c4e4e63b737d48ff1e49131`  
		Last Modified: Tue, 03 Feb 2026 04:22:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b2376b5248c239b5cfc641ad94dadb0e249f0897f589ad9c62854db6b4a74884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059f45f4374526742b333b716d31ac5408b2a275f96539e12c1ec7d83c7c4c1f`

```dockerfile
```

-	Layers:
	-	`sha256:0bddb42a78941243a5122cd11d30746f598c5a3cd77275075c332c2dd179ddad`  
		Last Modified: Tue, 03 Feb 2026 04:22:23 GMT  
		Size: 10.5 MB (10524231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f35126a1cae809f6aec75560a9205c891e7946c5b08a00b9c8b424272de0faa`  
		Last Modified: Tue, 03 Feb 2026 04:22:22 GMT  
		Size: 27.9 KB (27931 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; 386

```console
$ docker pull golang@sha256:187a5857d8b6a9ee8eb0e93969eeb2715c7286f4622c68e528355d4c41be15df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289305963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef2104b909cd4004bbf2e0e128c60fd9c6f67a16c891bf16797f7b09ac2eed9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:17:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:18:00 GMT
ENV GOLANG_VERSION=1.25.6
# Tue, 03 Feb 2026 04:18:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 04:18:00 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 04:18:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:18:00 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 04:18:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 04:18:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a7f977a794a5fd56ece19f51541cec3b8ba447f10234ab001213bf850f92f64d`  
		Last Modified: Tue, 03 Feb 2026 01:13:34 GMT  
		Size: 49.5 MB (49468454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50ea552b26a58c13b4166d933269500891fb4897db09bc72d932372276b158f`  
		Last Modified: Tue, 03 Feb 2026 02:49:31 GMT  
		Size: 24.9 MB (24872100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc15e0cd687cd62190081200fbe30ab5102ae840cc68b0386259c387aef2b9a`  
		Last Modified: Tue, 03 Feb 2026 03:25:00 GMT  
		Size: 66.2 MB (66234564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92308300c1b24e54a7f5b55d39c976a9c5cbf6f0fd1eb61286662908ac212185`  
		Last Modified: Tue, 03 Feb 2026 04:18:27 GMT  
		Size: 89.9 MB (89858933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd402dbe928e14f69063c85f23dc6c9bbceb27e04cff93cac6dc77cf1a8f6be`  
		Last Modified: Thu, 15 Jan 2026 19:32:08 GMT  
		Size: 58.9 MB (58871754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5550b8e6e97bffe020cc934346a98a28f39dabc0a8f047889bc08d4fe005a0a`  
		Last Modified: Tue, 03 Feb 2026 04:18:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0b966bc28412ca1b74ce9e934590461e4b3216222cf6dd3ccad9668bcda0bfb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10503716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b000711ea78811b56263d5c890686988bf3b309a0b7a8b2a554ee63aeab548e`

```dockerfile
```

-	Layers:
	-	`sha256:70391717d824d61aef8ae6b46cfc463fc72c91571fceeb1712604d5d653792a8`  
		Last Modified: Tue, 03 Feb 2026 04:18:24 GMT  
		Size: 10.5 MB (10475955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb1a024465f7272e4d222b6836f03840c5e3f9201d2554047728793a6f40fe8`  
		Last Modified: Tue, 03 Feb 2026 04:18:24 GMT  
		Size: 27.8 KB (27761 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:f49ab1bd4f10a29db5addaf55136d10cefd9b240f2553a21373f8f00fd3506a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262284479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ed3958199c0f4a8c9930b3937a8bfbdb9da27da450e634669cb784dd7e91ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 16:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 21:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 22:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:33:52 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:33:52 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:33:52 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:33:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:33:52 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:34:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:34:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b4c94e33bcdbce9a62a95be51a6e5f8ed2efc653e4be8f8f6722aa13d9d65461`  
		Last Modified: Tue, 13 Jan 2026 00:40:12 GMT  
		Size: 48.8 MB (48763393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3ebdc0d40ea56bd8ca0e23bf6a7db8ca22ab77cacf0ba126e24eb42d35c708`  
		Last Modified: Tue, 13 Jan 2026 16:17:52 GMT  
		Size: 23.6 MB (23614652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ee435e05dd9c53ddee45b81a8f55939374cd926a0e00239c752bb0832a5f8b`  
		Last Modified: Tue, 13 Jan 2026 21:22:59 GMT  
		Size: 63.3 MB (63309962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659edd573efc55ccb964dda4fd8e0b2b02903c5753a704b10ec114e6a6fa5f32`  
		Last Modified: Tue, 13 Jan 2026 22:44:42 GMT  
		Size: 70.0 MB (70021799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b0400b5590e7fd7237d1225e0e47e6e763d192b132b6948f11a5446ebd37c3`  
		Last Modified: Thu, 15 Jan 2026 19:35:44 GMT  
		Size: 56.6 MB (56574515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd1f6047cc8072073792326b5b21badb078d245c83d8173ebbebe9ad6556a0`  
		Last Modified: Thu, 15 Jan 2026 19:35:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:08e9f2f70f9173eae9a4e9a4846d505e9c6133939c48e654a39e93a241bdee3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28451948111c8ed874d77f66ff9f23da491425679b6a46838a25730f5d037987`

```dockerfile
```

-	Layers:
	-	`sha256:0747dafc38fae97d41bc64e8c09ce9c8e4a93e29d59718d614d78b552e9ac000`  
		Last Modified: Thu, 15 Jan 2026 19:35:38 GMT  
		Size: 27.7 KB (27654 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:3b9873e6c4b2723741c92a7d144af325016d009e6aa1e7d30eb95bfd6a4d63b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296408181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35124ab37ac0630c089fcd26a9860180357d33f5c201e033d64dfd82e33c3a0b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 06:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 08:53:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:31:15 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:15 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:15 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:32:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:32:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2769c4ec4b4d67e8059086401477839f8b9d5a5026dd27df50a3c7ce33b9db`  
		Last Modified: Tue, 13 Jan 2026 03:35:30 GMT  
		Size: 25.7 MB (25670703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5fcb80ea7d84a82ea96c11045a4f40d0943808d5c5334ea90de2f7ed44f4c4`  
		Last Modified: Tue, 13 Jan 2026 06:38:28 GMT  
		Size: 69.8 MB (69846016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39324acd74abd8d66fc3636cdba0cabcab5132ff369ae8d34e56255bdb262d35`  
		Last Modified: Tue, 13 Jan 2026 08:55:17 GMT  
		Size: 90.4 MB (90428658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de1d7ce58974e33ace56f0654af975ba4e29402893e2d90d191005bed4dae95`  
		Last Modified: Thu, 15 Jan 2026 19:32:22 GMT  
		Size: 58.1 MB (58135270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0444d9bd6f0b9ba3eaaa9bd81499e0db3b792afbec3d2bf626160d3e07f6b0`  
		Last Modified: Thu, 15 Jan 2026 19:32:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ed2ffa667c433be1c47a5203b870cd726c320175602a1d5de29319df12ea547a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42c7116a534b8f6b6282fb4aef04032c492ac62f465980a8f321856615d5f58`

```dockerfile
```

-	Layers:
	-	`sha256:694dcd24620fe569ecf90d16d9b221c061b032c2a5b72d5494f3c32bd8216156`  
		Last Modified: Thu, 15 Jan 2026 19:32:58 GMT  
		Size: 10.5 MB (10468878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca3cd90760a972c440c8b14f97e999f1eda3f7fffaadf8c4ea15b4f9ec9924cf`  
		Last Modified: Thu, 15 Jan 2026 19:32:58 GMT  
		Size: 27.8 KB (27845 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; s390x

```console
$ docker pull golang@sha256:2d4a32f0e0215d2d63577593b32851dee1094fbc04627927efd1f3265038e0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263183377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae509841942c72ce089dc5043159eb2572ac1d38de30d7628df7dd98401017ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:28:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 06:15:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:31:09 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:09 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:09 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:09 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 06:16:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 06:16:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3072e3eb8c224dc593a4e18a3785b06d51467102b1cd9dd426d3d31d0e6831b8`  
		Last Modified: Tue, 03 Feb 2026 03:44:33 GMT  
		Size: 24.0 MB (24033633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61724404ca7e7ee67a943113b2e679af71546a07f66af094570e811bbc9fa743`  
		Last Modified: Tue, 03 Feb 2026 05:29:11 GMT  
		Size: 63.5 MB (63501320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ed33b56c85899c1cf962e6995242864b8e86ffe5adfb45db579f323fbff37c`  
		Last Modified: Tue, 03 Feb 2026 06:16:50 GMT  
		Size: 69.0 MB (69018751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb26ceadf9d37827849921e4f034b2107b0a7ec09f97f2b6301929ee5e50569`  
		Last Modified: Thu, 15 Jan 2026 19:31:35 GMT  
		Size: 59.5 MB (59491172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528670d07c14c00508a3ee304716906fcd0595940ad1fd170ec8cd3e5b0a2a6a`  
		Last Modified: Tue, 03 Feb 2026 06:16:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3555506e8664424e38b1d58f216703f719b6dcfaf399a07af57c359090d1eca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10355763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ae6ad47fabf15dffebbe8d2b69e73a129f5e3f356e861cf58627994c7c81e4`

```dockerfile
```

-	Layers:
	-	`sha256:480dcf6607905d614548042134a2283fb7e3cba754d3d6c64f42e4a609851e5a`  
		Last Modified: Tue, 03 Feb 2026 06:16:49 GMT  
		Size: 10.3 MB (10328141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15e6b5e366b2ca17ed88dfc227d67597300d085ac37e97a068fb6f100ee72271`  
		Last Modified: Tue, 03 Feb 2026 06:16:48 GMT  
		Size: 27.6 KB (27622 bytes)  
		MIME: application/vnd.in-toto+json
