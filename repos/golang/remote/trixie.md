## `golang:trixie`

```console
$ docker pull golang@sha256:a02d35efc036053fdf0da8c15919276bf777a80cbfda6a35c5e9f087e652adfc
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

### `golang:trixie` - linux; amd64

```console
$ docker pull golang@sha256:406139dc5f8e5d79c709b8e637a0c1fc5907ed1521964b3ae419d4ecb002560e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304943301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a14b4331ccfa06f64ae6f1ef82fea31a0af3a8792e62473e770745f87444120`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 10:25:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:25:16 GMT
ENV GOLANG_VERSION=1.25.4
# Tue, 18 Nov 2025 10:25:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 10:25:16 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 10:25:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 10:25:16 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 10:25:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 10:25:22 GMT
WORKDIR /go
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
	-	`sha256:640989307fdd100137c7737c7f5e3a500b556c52e0270eb54eee3cd2862a1e73`  
		Last Modified: Tue, 18 Nov 2025 10:26:08 GMT  
		Size: 102.1 MB (102108813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9d4a4eea0de466b378fec1876ea74acd9465fc6a1d15368a117eeacaa21b7d`  
		Last Modified: Wed, 05 Nov 2025 20:18:32 GMT  
		Size: 60.2 MB (60151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65722e576e26f93f6cfbc2982f965aea739a47d43bea194a2dd0f4b344e01d82`  
		Last Modified: Tue, 18 Nov 2025 10:25:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:bd770eaa287a6bec343f701009ea1547141d68db98e3841f059b74a340053845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90be697b90a3e798d859ab96c7d63ad58afb944d2c34283ab88aa9e2fa96865a`

```dockerfile
```

-	Layers:
	-	`sha256:4db5fdb864ec76aca75bed22036e3ec279c315aa27af57b66030b518afec7739`  
		Last Modified: Tue, 18 Nov 2025 12:22:52 GMT  
		Size: 10.8 MB (10784428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce8b3e3e3f5c62f0d335b1e5991941f5fb340ada76579a26cbd00ba54a793eb9`  
		Last Modified: Tue, 18 Nov 2025 12:22:53 GMT  
		Size: 29.0 KB (28953 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:e6367b33e85b40767e3106b2da0d64c6fabef3ca97ae9482a933a1e77a12a9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263878114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590abe8ba6291bd7447a9677884becd7a7cf6b8c0cec745c6d07059a62c06e35`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:28:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:24:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:24:23 GMT
ENV GOLANG_VERSION=1.25.4
# Tue, 18 Nov 2025 06:24:23 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 06:24:23 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 06:24:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:24:23 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 06:24:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 06:24:25 GMT
WORKDIR /go
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
	-	`sha256:37e0a63864ca80e7942ea761325f349abb8b4b309eafbe10dd3105ea909b55a3`  
		Last Modified: Tue, 18 Nov 2025 06:24:57 GMT  
		Size: 72.8 MB (72754060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005e5e3f870b603812d4e2b76f2d3cd35fb32a7d8a09fbbc4d31d3610a5033ab`  
		Last Modified: Wed, 05 Nov 2025 20:17:33 GMT  
		Size: 59.1 MB (59072180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7590b46145589ccfd22987844ddfbff2fbed7c714c1107d1432f7787f1ac6d11`  
		Last Modified: Tue, 18 Nov 2025 06:24:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:afbe98e7863dfbdada14449aa0502f4b32a07f6b5f9961c6d74a5c57149d115a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26eea0909017fe5996d777add7e034f2e3bd95a6fba59dd7b3cb3e356d7bd82`

```dockerfile
```

-	Layers:
	-	`sha256:efe7fcb4faf141cb87d58f20e6c447275427e4fc2e31566846543d81e04d70d9`  
		Last Modified: Tue, 18 Nov 2025 09:23:18 GMT  
		Size: 10.6 MB (10580349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ac6e5cd5f98b45dd5316cd2e581067124ad3d29cbf2ebe13690b8f8c0e1fafe`  
		Last Modified: Tue, 18 Nov 2025 09:23:19 GMT  
		Size: 29.1 KB (29087 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c7ee8d25524e30768e961bdb5517733bb0264c244690dc4656d4b85b24b70585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298162511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0de0889c37cc2daffaba4cb46266ff04db79547b6e76fdcccbccbe690e15373`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:37:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:37:04 GMT
ENV GOLANG_VERSION=1.25.4
# Tue, 18 Nov 2025 06:37:04 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 06:37:04 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 06:37:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:37:04 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 06:37:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 06:37:14 GMT
WORKDIR /go
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
	-	`sha256:5fef2a450d16c14f1dc353a6d3e767c0939d1ce7f8cf2394af3527781ab0f9fc`  
		Last Modified: Tue, 18 Nov 2025 06:38:02 GMT  
		Size: 98.3 MB (98254676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0cd0526a95aa822822b8c4a246e8d3cb0ad0abd58b11c3ff2e34a74e1ffe9b`  
		Last Modified: Wed, 05 Nov 2025 20:19:33 GMT  
		Size: 57.7 MB (57651672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fc2dbf5ce4381111c2f99df86c349e1d420e6e01bf206fca7dc9be8633d6df`  
		Last Modified: Tue, 18 Nov 2025 06:37:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:60ea12e790a4a5323e2b19dfb55a23faf8823db37ed44da90c0871558d210396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d021af3bd3824ea8c070b1d4643f4e6d65c2d8e9054f6a0d766b697e3d1ebbca`

```dockerfile
```

-	Layers:
	-	`sha256:4d48a7a8bb407d77856f0e584215533d17dc07b1842a44f93cb6f5d2c4f1ac2c`  
		Last Modified: Tue, 18 Nov 2025 09:23:28 GMT  
		Size: 10.9 MB (10904931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da5d00d6454d94c4c846118b37ad9ef2ccd61150c9f68f1902bd95df92a7325b`  
		Last Modified: Tue, 18 Nov 2025 09:23:29 GMT  
		Size: 29.1 KB (29131 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; 386

```console
$ docker pull golang@sha256:d73427e3fdffa766d34a4b5287cef021c68288767e8ae455d3fc4e222c378222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.8 MB (306807504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae2ecbca33af88f0a27724fcec65ef955f1a0adad26b18f8acde66b26bfc887`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:11:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:59:15 GMT
ENV GOLANG_VERSION=1.25.4
# Tue, 18 Nov 2025 05:59:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 05:59:15 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 05:59:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:59:15 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 05:59:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 05:59:17 GMT
WORKDIR /go
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
	-	`sha256:ac26e1b09bd09fabe70981f3b4005383215b9162fa6d5f4b7dd6e9ffbc7367c6`  
		Last Modified: Tue, 18 Nov 2025 05:59:57 GMT  
		Size: 100.6 MB (100555044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb3e80f5b54e127a93e5c4d633621083cf9b0a94288cc3bff72b650fbb53f1c`  
		Last Modified: Wed, 05 Nov 2025 20:16:54 GMT  
		Size: 58.9 MB (58871003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d0156fb0d83a929e46160cfa5a2d99bf8b7367f27198791b6a5e2d37d5e769`  
		Last Modified: Tue, 18 Nov 2025 05:59:47 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:e32a47a7eab6fb84a20e3371c2e46ce1d12a29749090ac098ff2a5a77f899081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9a3c57b4017da11f7f578573c879979c1fcf5279243c871a6bc2275086441c`

```dockerfile
```

-	Layers:
	-	`sha256:f8db30156fd6aa82edf40048380d1839d58c92f86d06b8f2af826881da36f87c`  
		Last Modified: Tue, 18 Nov 2025 06:26:30 GMT  
		Size: 10.8 MB (10755674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b566613b53e2d57c533de8a5b98d7fda8d3f768a87dab57251897a2cff61c0f4`  
		Last Modified: Tue, 18 Nov 2025 06:26:31 GMT  
		Size: 28.9 KB (28897 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:a85948c777964ed0951da3601094c39024039737314537a9a221ba8bf4eec749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304076384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2238847e4a2dd2acdbc63a53498867c8a66cfd77f9ba488867e40506f90b69`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 08:20:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 08:19:57 GMT
ENV GOLANG_VERSION=1.25.4
# Tue, 18 Nov 2025 08:19:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 08:19:57 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 08:19:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 08:19:57 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 08:20:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 08:20:20 GMT
WORKDIR /go
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
	-	`sha256:d7756cae789e79571b10ebdde577e95b06e8789c77b7c86e1f13d466fd5e8d9d`  
		Last Modified: Tue, 18 Nov 2025 08:21:51 GMT  
		Size: 92.8 MB (92815805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2470fe8e729e39478adbcf0e2206e2b0fe316cbf8e73d84d0bf464e839a1aa00`  
		Last Modified: Wed, 05 Nov 2025 20:16:13 GMT  
		Size: 58.1 MB (58133115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893e8805340cb72b16eeac8c18a60b1c31cfbaeddc4476159dc0e2d5764d3582`  
		Last Modified: Tue, 18 Nov 2025 08:21:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:b3a70f4ede9b71e6fb806d844b1fdd2e16b7f2fc5eb0489914d00b06e735f977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f621aeed000aa3f501f501784e65f49875cbcd31fd61f66d43420e9716bbf4`

```dockerfile
```

-	Layers:
	-	`sha256:2ea0c1db937376324bf1bf41c33fd22c908dcf7ca07fc44da4027fb63e3fa6a2`  
		Last Modified: Tue, 18 Nov 2025 09:23:42 GMT  
		Size: 10.8 MB (10780236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b24005d08cef3b25b4de4aebe3bf683ad0683cdbbdecf3256d60a3985abea0d5`  
		Last Modified: Tue, 18 Nov 2025 09:23:43 GMT  
		Size: 29.0 KB (29021 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; riscv64

```console
$ docker pull golang@sha256:92d56f20e5c32392049fdbd984efc601f7d752a01ae0f6941415cb20787a4477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329649511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592848a8c299d1f13d7d23c62e7022c09decd28fc79e6d4ac360c928e222a095`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 22 Nov 2025 22:09:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 22 Nov 2025 22:09:00 GMT
ENV GOLANG_VERSION=1.25.4
# Sat, 22 Nov 2025 22:09:00 GMT
ENV GOTOOLCHAIN=local
# Sat, 22 Nov 2025 22:09:00 GMT
ENV GOPATH=/go
# Sat, 22 Nov 2025 22:09:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 22 Nov 2025 22:09:00 GMT
COPY /target/ / # buildkit
# Sat, 22 Nov 2025 22:09:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 22 Nov 2025 22:09:35 GMT
WORKDIR /go
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
	-	`sha256:4b8d0f17fde453d9cf0b99bedd3dfac5dd06317d587dd69852c68ca1441ce0e8`  
		Last Modified: Sat, 22 Nov 2025 22:24:09 GMT  
		Size: 131.6 MB (131594403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4cca360a3248a39ae972bdd0361d5418adbfd7b32f2db3f769eda57df020d0`  
		Last Modified: Thu, 06 Nov 2025 10:44:12 GMT  
		Size: 58.7 MB (58669059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c7a1e141d28fbf759b0b16931be9204e8bb9e0451c60e2e1834f620f8ba4f2`  
		Last Modified: Sat, 22 Nov 2025 22:17:36 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:2d2fe5c2f2fdeec389f433368547d49e7a7c7ed5f8571c2540b69154dfb39aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8560bb531100c2b756098dcca7dfe429e83374c2b3e0b046d0d71ea4db9938d5`

```dockerfile
```

-	Layers:
	-	`sha256:66e81147fe9df77d207494d8dffae3c46eb2df40ece247fbd6a21e80ae6ded72`  
		Last Modified: Sun, 23 Nov 2025 00:22:53 GMT  
		Size: 10.9 MB (10854069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:166a439db363ac7e1c759040bb5eab6e799f0a83b4498a83fff926d136251943`  
		Last Modified: Sun, 23 Nov 2025 00:22:53 GMT  
		Size: 29.0 KB (29025 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; s390x

```console
$ docker pull golang@sha256:ac5081bf277109fbb5ca71b575c4dbfb4e25aa4297c906a24e20f21cedcfbd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280160146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d60ecfb9aaf632936035e9c4b5fb65ccc08027d32c47a4ff81e68f9f9b9d97`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:57:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 07:29:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:29:25 GMT
ENV GOLANG_VERSION=1.25.4
# Tue, 18 Nov 2025 07:29:25 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 07:29:25 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 07:29:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 07:29:25 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 07:29:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 07:29:30 GMT
WORKDIR /go
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
	-	`sha256:a481d00827be55e12947c2019e1ed38bcd021b127ca4508bc3947dfbe02dae50`  
		Last Modified: Tue, 18 Nov 2025 07:30:25 GMT  
		Size: 75.9 MB (75919725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fe2a4ea5a438feafc93392d55b50ea8eee2e47563087161685963824d4cb40`  
		Last Modified: Wed, 05 Nov 2025 20:16:44 GMT  
		Size: 59.5 MB (59483654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff7da1bcfe7618d0f751633df213a8418256cc87269b3f3bd16089b926fa075`  
		Last Modified: Tue, 18 Nov 2025 07:30:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:2b49943a6c9352646e83d1add4483471976b859d3ad597db27350b559f64ddad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d0ea14ad9500a27c86c20ea3af341e41686002827e2855a75c3eb704495f14`

```dockerfile
```

-	Layers:
	-	`sha256:a717f911a3779be6e9b36e4fdb9df53382f4bfd5f79f00d7e9a2fd02fb4f6ae8`  
		Last Modified: Tue, 18 Nov 2025 09:23:56 GMT  
		Size: 10.6 MB (10594828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c8027e24068878c9894fce7dd0cba2ff4317dca2cab3f4c5ccd40693249c9f`  
		Last Modified: Tue, 18 Nov 2025 09:23:57 GMT  
		Size: 28.9 KB (28948 bytes)  
		MIME: application/vnd.in-toto+json
