## `golang:1-trixie`

```console
$ docker pull golang@sha256:ff83f3762390c2cccb53618ccc18af23e556aff9b1db4428637e9f63287c8171
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

### `golang:1-trixie` - linux; amd64

```console
$ docker pull golang@sha256:96323c4aa0ea9064c4a4ac0cee942c235173d2674daa641cccbbc021fec18b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304987300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c267f0be74944e2fe67963c84cea922c9c23757e785a12b9cf851086bc298a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:17:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:17:26 GMT
ENV GOLANG_VERSION=1.25.6
# Tue, 03 Feb 2026 04:17:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 04:17:26 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 04:17:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:17:26 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 04:17:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 04:17:33 GMT
WORKDIR /go
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
	-	`sha256:abc43c4e3173ba2cd968f6e889b506fc8f4e183ea39be9714dca61955ffff3ca`  
		Last Modified: Tue, 03 Feb 2026 04:18:02 GMT  
		Size: 102.1 MB (102138525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c503e035cd5c1ea67986d21ed1fb2f4305f801555c52f9f16ce0f0f5cf2e16`  
		Last Modified: Thu, 15 Jan 2026 19:31:09 GMT  
		Size: 60.2 MB (60154290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925eebba20a5d033fa64abf408c3bbc85f4fcc7a017b3d01c09a48806af09888`  
		Last Modified: Tue, 03 Feb 2026 04:17:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:14b7f7c7968e7c3738bbdce2bd72ce35cf2ad7cbdd11ebcb106412f2aa34db02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63404a949eb6f6ea6cf138adf05116f38eb92a85e7bd89680ae88c529e1127a7`

```dockerfile
```

-	Layers:
	-	`sha256:14646da1294ac7246edbc6eb09820e814983cce52e22bd360b101dd52e51c56c`  
		Last Modified: Tue, 03 Feb 2026 04:17:59 GMT  
		Size: 10.8 MB (10785503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:154798a4bbe16b1826fdf0ea892f9b9432e4c1a120f12e02bcd7e9fa029e7374`  
		Last Modified: Tue, 03 Feb 2026 04:17:59 GMT  
		Size: 29.0 KB (28952 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:964b6f22daf783143607dc426a3dde81e83334f625b927387e5a120fb83e5a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263924251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3329a77d4c7763e76b29c831a4dd7cf53948d22fa43e36a8b277e58c9ee79e6a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:32:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:01:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:21:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:21:22 GMT
ENV GOLANG_VERSION=1.25.6
# Tue, 03 Feb 2026 05:21:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 05:21:22 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 05:21:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:21:22 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 05:21:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 05:21:24 GMT
WORKDIR /go
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
	-	`sha256:20b16e015711128cb0596658dd8882d511bb154c4df3bed8fc7445abb943b5cf`  
		Last Modified: Tue, 03 Feb 2026 05:21:48 GMT  
		Size: 72.8 MB (72783431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9858bd230951a4669967b265976b2f7dbd9f374059998fadb8d8956bf7de2a2`  
		Last Modified: Thu, 15 Jan 2026 19:30:05 GMT  
		Size: 59.1 MB (59073810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4bf766050b111734fd4e948c5b7a755064bb2a944561d77f0522005dcbc30`  
		Last Modified: Tue, 03 Feb 2026 05:21:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:83d83d4b1f0f43f92bd4ee564fe0bdca58d2ce27571b56e41a088384e76550e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d856773088cb4fdd6a2ace126ba71d8c5b8a0f7dd3040e15e1c5a31229e497c9`

```dockerfile
```

-	Layers:
	-	`sha256:f11a4c25efddd7b2592c762147456a0e4df81b4a5e946a623680435d5821960e`  
		Last Modified: Tue, 03 Feb 2026 05:21:46 GMT  
		Size: 10.6 MB (10581424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b90eeccbfd377211eb78bf15cbe97562496cfc75564115b6d864148024b528`  
		Last Modified: Tue, 03 Feb 2026 05:21:46 GMT  
		Size: 29.1 KB (29087 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:9ecbe158f9fac2103a00bf7cc851b2c1ae1639db5cf43b1f05f212df92d52705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298210405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055c3ee40d024e37f6e94e7662bfed85fd1b0dfba73efe5a888d16261d85c6a6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:22:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:21:53 GMT
ENV GOLANG_VERSION=1.25.6
# Tue, 03 Feb 2026 04:21:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 04:21:53 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 04:21:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:21:53 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 04:22:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 04:22:02 GMT
WORKDIR /go
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
	-	`sha256:a515acb5ad94563671a7e74192a421f77ce3a07bc328920ba5755289f5a7dbd0`  
		Last Modified: Tue, 03 Feb 2026 04:22:29 GMT  
		Size: 98.3 MB (98283340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a2f381e4cd3963e3af5194953e3e2807c452e833bf69397dee70610e428e6`  
		Last Modified: Thu, 15 Jan 2026 19:30:21 GMT  
		Size: 57.7 MB (57659196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabda1d417ced27e7abddd012cefb10691cd8ebbde95580978ef70ab5e7d1829`  
		Last Modified: Tue, 03 Feb 2026 04:22:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:8b2a0c3ffa9eae36623ad1ee70ad2918a5c9826f85b302e3feb39fff23908816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5116f66393301f7e7ece6f1882749185feb700823015eec63995d5103d148c0`

```dockerfile
```

-	Layers:
	-	`sha256:00eecba0eac60c74fbab1d91c128612896316eb45bf4d81e0b04f4fa7c6a5725`  
		Last Modified: Tue, 03 Feb 2026 04:22:27 GMT  
		Size: 10.9 MB (10906006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6634967755d098795988885d28efba482366e6f41d79c0d4778b37c0362e06c`  
		Last Modified: Tue, 03 Feb 2026 04:22:26 GMT  
		Size: 29.1 KB (29130 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; 386

```console
$ docker pull golang@sha256:ec7c2cd6dd9cf3bd9cc734dae38f698a641b8c4ecb05eb00d6e9796722ea04d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.8 MB (306841390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f88bb6f5db878c97ef0f9d4e072b66f439a60bb52b48e87b2c6f7fa06fe2fb4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:17:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:17:37 GMT
ENV GOLANG_VERSION=1.25.6
# Tue, 03 Feb 2026 04:17:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 04:17:37 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 04:17:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:17:37 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 04:17:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 04:17:39 GMT
WORKDIR /go
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
	-	`sha256:14980d8d5bafa97dff9441bb2c9ee04f441ad3befd512dc9341ca21621f8ac73`  
		Last Modified: Tue, 03 Feb 2026 04:18:04 GMT  
		Size: 100.6 MB (100582779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd402dbe928e14f69063c85f23dc6c9bbceb27e04cff93cac6dc77cf1a8f6be`  
		Last Modified: Thu, 15 Jan 2026 19:32:08 GMT  
		Size: 58.9 MB (58871754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3691779f3ca801bb4ea4db71ca03f128f06b1b39988ae03c4b6c7b923d1e2aa`  
		Last Modified: Tue, 03 Feb 2026 04:18:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:614a367ffac689864d0a1c5b9bddf2ac3d85211aabc0a790440ba1c0ab4b4dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782d9b57a50a04e0bc6b404043ff496ee7f6961bd30ddb601074b6542632ad99`

```dockerfile
```

-	Layers:
	-	`sha256:06bf7bf3ff5eabaea3b202d8b3ea411691ec727d2549b82a13e3a795126f1aa9`  
		Last Modified: Tue, 03 Feb 2026 04:18:02 GMT  
		Size: 10.8 MB (10756748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01a1004258cdb28a6d751243d4fada178f5c18d1b7846f1e13a847f96ad27b48`  
		Last Modified: Tue, 03 Feb 2026 04:18:01 GMT  
		Size: 28.9 KB (28897 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:a495aa757a91b8031418f46c61f3d1ab2fe157ce4bd8db6a0ca896fb9ea27611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304122648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d69eeef418a6b98839011ea5fd74f67e27d7221d269dd4fd898202ea98b866`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 09:15:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 15:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 16:13:00 GMT
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
# Thu, 15 Jan 2026 19:31:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:31:21 GMT
WORKDIR /go
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
	-	`sha256:a6963c45fc75dae1c69a32ad6c3270c86fd5157751391796c0d838607e88acc0`  
		Last Modified: Tue, 13 Jan 2026 16:14:26 GMT  
		Size: 92.8 MB (92844600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de1d7ce58974e33ace56f0654af975ba4e29402893e2d90d191005bed4dae95`  
		Last Modified: Thu, 15 Jan 2026 19:32:22 GMT  
		Size: 58.1 MB (58135270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1718e0e8b3469607a4f3444c04539e164bf8911fca14caf1a1103766bdf84f`  
		Last Modified: Thu, 15 Jan 2026 19:32:20 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:eaf423f08545df568f64c2f4036b7384b45c1c0641d8c277ebd6a1d92181d321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93fd9ee042a475b3d674f7d7058bde5c6f2a400000bc8ea7b7a0744941d19a9b`

```dockerfile
```

-	Layers:
	-	`sha256:3cbe35f9becefd0da0bb5eb6c88e5b26fdc99807180611087cfb9fd1451865cd`  
		Last Modified: Thu, 15 Jan 2026 19:32:21 GMT  
		Size: 10.8 MB (10781313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49fc4a9cdf8c275e31e9ef1c6653cc31120a87dc1b81d93316a50ae7a297ee8c`  
		Last Modified: Thu, 15 Jan 2026 19:32:20 GMT  
		Size: 29.0 KB (29020 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:eaf774b17f5de007277ed8a891e838feec74d98c8d7a13389538e5897b581a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329682990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741a865cda10e5cd37d8f790109cfa17ca7babe3e076e3872bc2935a94c07aa3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:47:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 18 Jan 2026 22:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 Jan 2026 20:40:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 18 Jan 2026 23:11:45 GMT
ENV GOLANG_VERSION=1.25.6
# Sun, 18 Jan 2026 23:11:45 GMT
ENV GOTOOLCHAIN=local
# Sun, 18 Jan 2026 23:11:45 GMT
ENV GOPATH=/go
# Sun, 18 Jan 2026 23:11:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Jan 2026 23:11:45 GMT
COPY /target/ / # buildkit
# Mon, 19 Jan 2026 20:49:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 Jan 2026 20:49:51 GMT
WORKDIR /go
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
	-	`sha256:13b6ae4171d4a5e53813caeec0fed4e819700c3a0b1ae7031301cbd179639a4c`  
		Last Modified: Mon, 19 Jan 2026 20:48:15 GMT  
		Size: 131.6 MB (131626895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76383bda51f6d2301c4d245b282d3ec6e006fd6e4d52961e3dd0dba3364c9182`  
		Last Modified: Sun, 18 Jan 2026 23:14:35 GMT  
		Size: 58.7 MB (58671645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ce3a7064671db6af53faab519b9c5576be791225c917043b2a010d21fa4518`  
		Last Modified: Mon, 19 Jan 2026 20:54:32 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:eb2d9ff7c734ff3896f819192ffba026a820e03cbc305a81beb97ca520b212e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae5803995ae5e5263208ad27d1d4e879cb76c8163b59aea068b2793e7a426ca`

```dockerfile
```

-	Layers:
	-	`sha256:8dd89e7c8db28bb4552d6bcdcb6e522395d8e0040044f95b3b33a203bc7459d6`  
		Last Modified: Mon, 19 Jan 2026 20:54:33 GMT  
		Size: 10.9 MB (10855146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f94aac16989691ca3cea76c38d1f7b81c1c42035c01f78d9bcdddf3d00dc6b1`  
		Last Modified: Mon, 19 Jan 2026 20:54:32 GMT  
		Size: 29.0 KB (29025 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; s390x

```console
$ docker pull golang@sha256:8e73bf6764f94a316c56dde7ce927a3528ec9403438b3cbe03bf7055e52fe4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280213179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9106670a4cba44eb753f39417f2ca3b65d90d37d67e001f8086c8e01ae105380`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:29:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
# Tue, 03 Feb 2026 06:16:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 06:16:02 GMT
WORKDIR /go
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
	-	`sha256:a6078524cd185e4d8445473f4f9ab3575f38e333017f9ef2b71b7e61ae17c554`  
		Last Modified: Tue, 03 Feb 2026 06:16:40 GMT  
		Size: 75.9 MB (75949639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb26ceadf9d37827849921e4f034b2107b0a7ec09f97f2b6301929ee5e50569`  
		Last Modified: Thu, 15 Jan 2026 19:31:35 GMT  
		Size: 59.5 MB (59491172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cd854b88c0b46ce9c0ce47b1431b99d1b4c3d557b5bd60b15ebbc4c8e6d21a`  
		Last Modified: Tue, 03 Feb 2026 06:16:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:2fbf22d5bf9143a6a5551ba9a1777aab5c22df0523e20346b40cca8d24860faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10624852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a64560c047ce060b31095cfabb8b73965ca370ee1fac327810601dccdf72b3`

```dockerfile
```

-	Layers:
	-	`sha256:0beffdcdd7d27e9b46ffe63344835c87fa5a60a484a4be860ea9287e56a449c8`  
		Last Modified: Tue, 03 Feb 2026 06:16:38 GMT  
		Size: 10.6 MB (10595903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d8316ed01171ec3fab490ea4d6ba5bab27c35487d9fdd45508968f368751113`  
		Last Modified: Tue, 03 Feb 2026 06:16:38 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json
