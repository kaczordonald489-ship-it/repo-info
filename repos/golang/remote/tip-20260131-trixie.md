## `golang:tip-20260131-trixie`

```console
$ docker pull golang@sha256:a297b4804b32fd26eab00c39a991b9b2be88a1a75340a48c70e1d0b7901c00b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20260131-trixie` - linux; amd64

```console
$ docker pull golang@sha256:926d7654bca6926bf2d8f124e3c6fba2fd738c7c19f0e22b97d2fef2538fbe3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 MB (338166455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368b1db19f53b0517668d38a6fa272535c87ba6c03933d72b9f700f588f64a83`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:15:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:16:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 05:16:53 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 05:16:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:16:53 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 05:16:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 05:16:56 GMT
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
	-	`sha256:118ec5a5efad0631f147d09aecf662ae036337120defc36a25cedcb67b36289a`  
		Last Modified: Tue, 03 Feb 2026 05:17:24 GMT  
		Size: 102.1 MB (102138561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ca55bbd490d4f215c5420355c680b71279036da5d7c91d2d678e32c231a9c9`  
		Last Modified: Mon, 02 Feb 2026 19:30:41 GMT  
		Size: 93.3 MB (93333409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003ca574083ee19f98c73bfa302e930155800afd3060d26c41897f2cf1954dba`  
		Last Modified: Tue, 03 Feb 2026 05:17:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:ec7f9b9b42a1bacd8b3630e09507c756a4af7977acd233aa624b51a292b9972a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f3b6fecd6bfb8544b14ad1e0e88368b43f0f1c09429b34db8bbba88cb57a4a`

```dockerfile
```

-	Layers:
	-	`sha256:ef441782df83771093600e84311a5aea93c682ef271c584e7fdf488ccf5a92e5`  
		Last Modified: Tue, 03 Feb 2026 05:17:22 GMT  
		Size: 10.8 MB (10785583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea68e09be4c21a688c42bde8b947614f06a232d7c0ae2f61c261542d593c66`  
		Last Modified: Tue, 03 Feb 2026 05:17:21 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:c569072f0b070a7872b2c1acdc0275e7316f043e246a21ff77eb74574033e449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.3 MB (294326880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07428fe3f886cf96405a619c130de4f4822f0c0def9d61458306be76e5277a93`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:32:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:01:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 06:17:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 06:20:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 06:20:22 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 06:20:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 06:20:22 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 06:20:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 06:20:24 GMT
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
	-	`sha256:3fd3dab913329e0568510a999f0ce5f19bb957e29015af65172dcbe2a822e2c2`  
		Last Modified: Tue, 03 Feb 2026 06:20:48 GMT  
		Size: 72.8 MB (72783441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c4d8d165092e2ffa5f6928ecd151df0b8f3dc1362c8f59dcd6d9b09df5017`  
		Last Modified: Mon, 02 Feb 2026 19:30:25 GMT  
		Size: 89.5 MB (89476429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a541979c81aaf9e56af1cf5ac9070545bea41bb16b1df84183aac40f687b24`  
		Last Modified: Tue, 03 Feb 2026 06:20:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:6e7e706572937b731ac9057ec0845bb32e462d68b67dd01eae0dfd36c3e9e2ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded33a03674167b7ca6f52199062ff6f73b370fd77f9b3cfb92df8dc7dac0038`

```dockerfile
```

-	Layers:
	-	`sha256:3ed00da2f81a12861f67a46698615bf813a0b3da24010946c8fa0e302eb01a13`  
		Last Modified: Tue, 03 Feb 2026 06:20:47 GMT  
		Size: 10.6 MB (10581470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:025812bc82e230f4b88221fc5a8f152416ee66d8a5001cf14a09d0420d8cd016`  
		Last Modified: Tue, 03 Feb 2026 06:20:46 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:0cf52bc91a860e01743a8f244e478145919803c62cbf046aae49f786ca633bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.9 MB (328926681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af5c2e9e796ff91c2af6f3878145956c8b88951d88d42332c60cb4fd38b47e0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:19:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 05:19:46 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 05:19:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:19:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 05:19:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 05:19:49 GMT
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
	-	`sha256:855987e288f69de67bbed221b7c7b57ec1042c541b7383630d1ebf56d76adccc`  
		Last Modified: Tue, 03 Feb 2026 05:20:14 GMT  
		Size: 98.3 MB (98283113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6a2a8a6cfc628c3f67b49421d89d0e853e9d214495c3cea23b3d909be150cb`  
		Last Modified: Mon, 02 Feb 2026 19:26:36 GMT  
		Size: 88.4 MB (88375700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c020d175dfc41379afec7f05433bf9bdc194b73268c9aef5d12bbc72d61fe487`  
		Last Modified: Tue, 03 Feb 2026 05:20:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:375c51cc754d5c8313f96f8f4630f4244b520e56b4bd700a09ecf8c6641c7775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0161d3fec64d59c9c7c41c5b698d19c5c99809a05b70477232892928202067`

```dockerfile
```

-	Layers:
	-	`sha256:b0f087e3cdb086c03abf620da3bdb281bd4744ff486e9641a49ec4174476c7f7`  
		Last Modified: Tue, 03 Feb 2026 05:20:12 GMT  
		Size: 10.9 MB (10906038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49ead1bb2c7ebbacf14d6591d459271dcc3f688efba281c665082b7463f08b6d`  
		Last Modified: Tue, 03 Feb 2026 05:20:12 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-trixie` - linux; 386

```console
$ docker pull golang@sha256:d03cc95bf2618a959c9b48d6430e411ddd0dc300e202cdde9bb386a416458174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.4 MB (339375774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c837c2871bd4582e495d52b29a4d40de37252fd251a359844e17841c4919a1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:16:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 05:16:51 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 05:16:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:16:51 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 05:16:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 05:16:53 GMT
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
	-	`sha256:27d363864531f96be8e947dfdbf233b5cf97b095170679c47431df96b44a5607`  
		Last Modified: Tue, 03 Feb 2026 05:17:17 GMT  
		Size: 100.6 MB (100582681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4604cae1ff047094cf665f2719aaf0543d71e670a699786143900320f6ba300`  
		Last Modified: Mon, 02 Feb 2026 19:27:18 GMT  
		Size: 91.4 MB (91406236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c094e9d84780dcaad2fc10f9fd557a3a5fdfdb5a863c880975c8169f2bdcdb`  
		Last Modified: Tue, 03 Feb 2026 05:17:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:d451ed9c90a8cc80ce63f46cab1f45813ff6dea19cabcd811cbce490eae86bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c29c2ff3541e2bb3df9579eebf23578736053cda592e00367a10eacb157e0e2`

```dockerfile
```

-	Layers:
	-	`sha256:6a30cef9e7c74f33b1575631028b42d319763fcf55d24222d2fadaa208727a49`  
		Last Modified: Tue, 03 Feb 2026 05:17:15 GMT  
		Size: 10.8 MB (10756846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e28da03c7eb9cb083715f5fdabdf510a7982e8e408ef4d9197243448432dd590`  
		Last Modified: Tue, 03 Feb 2026 05:17:15 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:69d187695ba65969e9f916c8ab8c226a13997933e21078dd54cd25dbabb41a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335994859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e036de1d0d8b944b980fc96369ae26109d84b4bf683c097e1d9c6e9e2036ff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 09:15:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 15:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 02 Feb 2026 19:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Feb 2026 19:27:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:27:20 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:27:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:27:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:27:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:27:31 GMT
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
	-	`sha256:1c2bb998e0f9c58baa6cf42968de7d2eec57564cdd98362062f705fa7c8a2166`  
		Last Modified: Mon, 02 Feb 2026 19:28:35 GMT  
		Size: 92.8 MB (92844714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e432b6dca22e637a3a25408001c269ffda0f2c5d9306b2f7174d2a31051778`  
		Last Modified: Mon, 02 Feb 2026 19:28:34 GMT  
		Size: 90.0 MB (90007365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3cd8f45024cbdfb4cc5b9e4dc9514bdbab1462877d936e5fc3db66c9576c7a`  
		Last Modified: Mon, 02 Feb 2026 19:28:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:0ce7251fcd9b35ba3c1e457aad25f9bed8888a293a4fb88250462b7b4278566c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18111901d1472aee23d3a954d6504038bfd4f7bda8400ae464a543658c849e9f`

```dockerfile
```

-	Layers:
	-	`sha256:bc93e117de295ce7038fa06dc12fba3aa7ffcbfad6b3ed79e1d4489f816a44f4`  
		Last Modified: Mon, 02 Feb 2026 19:28:32 GMT  
		Size: 10.8 MB (10781371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2cb478e166dc92250ca1b6911d8a5fbb3482e3d53085a7065fe96912d1555ff`  
		Last Modified: Mon, 02 Feb 2026 19:28:31 GMT  
		Size: 28.8 KB (28849 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-trixie` - linux; s390x

```console
$ docker pull golang@sha256:a5d9547cca0178e934a4edf45c13820a6823c5be794e18237f20a041c288918f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.3 MB (313292448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7852031e59e16fc60b6ad8fbcea4ccad5e28c8c2d70d3945dd54647a36295ffd`
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
# Mon, 02 Feb 2026 19:29:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:29:01 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:29:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:29:01 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 08:54:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 08:54:14 GMT
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
	-	`sha256:3a7062bfc50107a913a5fd7c0d090af1366da08b74147cf71ec4490488730775`  
		Last Modified: Mon, 02 Feb 2026 19:29:23 GMT  
		Size: 92.6 MB (92570442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3df5dfdba7ecad722345a6ac8cd0432174a7789c441befa4b5f99d49b92537`  
		Last Modified: Tue, 03 Feb 2026 08:55:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:9b768e5282f8f5595074cd1c3afde0112e7d6fefc2e1fd057f6f5cb5ef62d978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10624947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0747ee0df7efb82f392d003cf9a87189180f07a3b582e60d764596908a8406`

```dockerfile
```

-	Layers:
	-	`sha256:d6f638f49a031421a08dd6a9bb0cef4b7d8c564194fb08c9c7d0dd72e770a2f3`  
		Last Modified: Tue, 03 Feb 2026 08:55:08 GMT  
		Size: 10.6 MB (10595983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dabad5dfa0a437f7dfe832f25af8cad0fe7867b328450a47df6e54afab17efe7`  
		Last Modified: Tue, 03 Feb 2026 08:55:07 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
