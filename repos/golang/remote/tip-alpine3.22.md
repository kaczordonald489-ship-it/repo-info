## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:8492c84a843987811f9cb27d572a0644d871927e8cfc9ac4b88f97501002b45d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `golang:tip-alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:1cc32e015c3599539b0212e7bf27ba51f6e280d6678d9c7eaaf48d0b2111650b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97429606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38f89301ebf3f808352195e0dc6548845a40e3c45e148c14f39a4d83b8642c3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:28:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:30:37 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:30:37 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:30:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:30:37 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:30:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:30:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81605a72f6afadcd3bdb8d572f943b39af74277d75c13252c08a984cab7c0051`  
		Last Modified: Mon, 02 Feb 2026 19:30:54 GMT  
		Size: 291.2 KB (291164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ca55bbd490d4f215c5420355c680b71279036da5d7c91d2d678e32c231a9c9`  
		Last Modified: Mon, 02 Feb 2026 19:30:41 GMT  
		Size: 93.3 MB (93333409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fded54f5e20ad6d0a2f8023a8de18b4cd710d9ce2ef4d9eeb51085b94d0556d`  
		Last Modified: Mon, 02 Feb 2026 19:30:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:84096b4cee7a4a23aa01a14b14013c610971021775ae74cc1b7ab407fbb1759a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2252b63c4e01e438af772a14de0436a838360957b582f4318b29334c0de157c`

```dockerfile
```

-	Layers:
	-	`sha256:86fbb02ebde5e0fe4cfa5e029a9dc04bddd4efba341d761c4e641034d7d77c91`  
		Last Modified: Mon, 02 Feb 2026 19:30:54 GMT  
		Size: 195.0 KB (194982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2b44c1b7b17f63b59f7638d62138c40ce0a5281c479a8a102b4c21f875c79a6`  
		Last Modified: Mon, 02 Feb 2026 19:30:54 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:271659f7bf8d3c94295dbaf10f5340c31addb891f127350ec5e8bef4966873ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93553363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0225cfc0cc507bd9ac6682fa08f298c550f4a6213c4e30b337ef76bfd7181e28`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:25:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:27:51 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:27:51 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:27:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:27:51 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:27:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:27:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfd84987e4909b0f2db6d1447025ac625a44c2ebb22f0eef8a0b95d1f46d25f`  
		Last Modified: Mon, 02 Feb 2026 19:28:05 GMT  
		Size: 292.3 KB (292320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e0df2db5a6de63ae56b2b7ac54a7918fd9414ba7652c1dadac1bfb31d63c9e`  
		Last Modified: Mon, 02 Feb 2026 19:28:08 GMT  
		Size: 89.8 MB (89755840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6367de96c46909dc7dbfd16b7beee1679bfa69b5fc37ec675d73c3fed36d1b97`  
		Last Modified: Mon, 02 Feb 2026 19:28:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:147c74e63addd03fc9ff053691742f9309f89b84155db1918d02306c3ea5057a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8463607d8085caa3366a45f171292e8beaaaef49abbd43347521e5d8b828ea1c`

```dockerfile
```

-	Layers:
	-	`sha256:f8c6e70c0551440c4eaea7903960ed8a60b30ee744e8d7fa2efc25bd862fe80b`  
		Last Modified: Mon, 02 Feb 2026 19:28:05 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:68cca5c0605dcf0e48b4b5ae28d401df829b6c98cbe5f08a90ad81829275a6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (92991427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb7eba6d4c82bd38ca086187f11127dcff9cabd85973d37cbef1a2fece4811c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:28:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:31:11 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:31:11 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:31:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:31:11 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:31:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:31:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa896de4429c30af7c66dddf04f0f428fb42e6f68c868fb434a04a0f156edc00`  
		Last Modified: Mon, 02 Feb 2026 19:31:29 GMT  
		Size: 291.2 KB (291213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c4d8d165092e2ffa5f6928ecd151df0b8f3dc1362c8f59dcd6d9b09df5017`  
		Last Modified: Mon, 02 Feb 2026 19:30:25 GMT  
		Size: 89.5 MB (89476429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6d1bbbeaae0aaf3f898904dd46c45f285b046cd430e81e4757280c4bf1ca8c`  
		Last Modified: Mon, 02 Feb 2026 19:31:29 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:12fb9aad9a9f63dee780a35ad047d194bc04239f61335404e0f92347296020c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56259c517922ff26e5f329262b0fb14d7dc5372d423e387ab4fb1a5531c24cd0`

```dockerfile
```

-	Layers:
	-	`sha256:ff691523df3894d0badd17f5d6fa5013d70909b286a1568fa3d098e32d037f11`  
		Last Modified: Mon, 02 Feb 2026 19:31:29 GMT  
		Size: 195.0 KB (194986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feb6173d55199d027ad7a36398590508901aeb8f548dcda4918f63ec8202f0a7`  
		Last Modified: Mon, 02 Feb 2026 19:31:29 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:6c2e591d9089caf447a323763b0592c7e57b577cbd81bdc70ca7542e30b74fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92809468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b3fcdde5360f566091d3a8631c7995dafc22038145879743c1c7a20303931a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:26:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:26:05 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:26:05 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:26:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:26:05 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:28:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:28:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e120abc00ef22d0b6d723f3bda4f1063b06852cd638295c36898d6e1649c143`  
		Last Modified: Mon, 02 Feb 2026 19:28:33 GMT  
		Size: 294.1 KB (294091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6a2a8a6cfc628c3f67b49421d89d0e853e9d214495c3cea23b3d909be150cb`  
		Last Modified: Mon, 02 Feb 2026 19:26:36 GMT  
		Size: 88.4 MB (88375700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2001a16cb0ce0714b521c6602b34aabf923b2fc1324947c9bbe23b57e6b905d`  
		Last Modified: Mon, 02 Feb 2026 19:28:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:0f7b4bd5e4ce15ac4853e859e70b9bc46a6cb9be2eb3cf4d299645acb63656de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a235e8e0e3d014f0e71cbddb65ffc4ebd25d26b2e6acb96ef3d7a1302eeb1ff`

```dockerfile
```

-	Layers:
	-	`sha256:02aec68f7b67d601585365eb70521ee2ae1a5e07cafbfb65538d7dfeb510552b`  
		Last Modified: Mon, 02 Feb 2026 19:28:33 GMT  
		Size: 195.0 KB (195014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee560483df55cd2c08abd4f1d97ebf54f8699100b9b8be5e15946e6dbff68c71`  
		Last Modified: Mon, 02 Feb 2026 19:28:33 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:d83eaaab5c4a2aabb12b7dcbe15d4983be5b22cb92f90d95583cacb80cfb985b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95318748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf78f115178f8cd4fb5113d3db301968e57762ad7ba43a7776ca2d7de7fea19b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:27:28 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:26:49 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:26:49 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:26:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:26:49 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:29:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:29:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3033a2ce45f26565babe698ddda6f9e1693f85b9ced3321e4f2acf6167838042`  
		Last Modified: Mon, 02 Feb 2026 19:29:30 GMT  
		Size: 291.6 KB (291622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4604cae1ff047094cf665f2719aaf0543d71e670a699786143900320f6ba300`  
		Last Modified: Mon, 02 Feb 2026 19:27:18 GMT  
		Size: 91.4 MB (91406236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd19bbc256fac3791ff8436a486b5ba4fded8da791f6da053bc517af2427fd2`  
		Last Modified: Mon, 02 Feb 2026 19:29:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:2edeb1f1162bfd26e2c06bf2b61d49c24cd7feddbda5cedff738b2ad0d950e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552c6ca9131a7791f6c89355033d4a10fad42caf1a4c857d4614052ee15a160b`

```dockerfile
```

-	Layers:
	-	`sha256:da332896cabd84c0fe89512182efba9a7c9adaf8ec93012a5f864359f2dd9c60`  
		Last Modified: Mon, 02 Feb 2026 19:29:30 GMT  
		Size: 195.0 KB (194951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3372d480736ea38948071ea9bed6547a469ab1877cb0c81ee231f087b7918b25`  
		Last Modified: Mon, 02 Feb 2026 19:29:30 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:71c0d151596da0e415d1f7ff563a923943974accee7df59ced38d6acbb4e1ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94036393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77927a02aa2578f6cfdfe0e9fa6361b82e1e9e55418c960db1486428019b5d9c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:06:40 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:27:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:27:20 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:27:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:27:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:32:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:32:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5da64929a546b25e151c7b89cac4fd99dc41033a2fc1973779548ea5121f99`  
		Last Modified: Wed, 28 Jan 2026 04:07:07 GMT  
		Size: 294.6 KB (294573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e432b6dca22e637a3a25408001c269ffda0f2c5d9306b2f7174d2a31051778`  
		Last Modified: Mon, 02 Feb 2026 19:28:34 GMT  
		Size: 90.0 MB (90007365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bee5cd9c137bea619e34d92f5c2da5d2d9a445fb38582ee9af5aa8663b51962`  
		Last Modified: Mon, 02 Feb 2026 19:32:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:95d3d436c28d995ada41e0957785936e3ab2514c13de7bbfe0d576d988ec40f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c314edd8ff4f02e87e05d4e475f9a92d41749adee4d270462fcfebd7d3c48ba`

```dockerfile
```

-	Layers:
	-	`sha256:ed32bc92c9a2655ab1dced39a0cd10e8c45bdcc4770fe7dd7740a2cfc7dcd0ee`  
		Last Modified: Mon, 02 Feb 2026 19:32:49 GMT  
		Size: 193.1 KB (193069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c25b21f686cc0be9117630b2d9b5f6ce640ff9f143064987f57312d72ddfd04c`  
		Last Modified: Mon, 02 Feb 2026 19:32:49 GMT  
		Size: 24.3 KB (24338 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:3ff62abcbe5eceda1b0dfe7fee8355029470a0ba2c3cf4c46e232faad7c0cb37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94366378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783fb47f38c8db94687bf53a9f6ec04b721a045bfa26a7cb8610b3a25f1a5262`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:15:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Feb 2026 08:03:08 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 08:03:08 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 08:03:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 08:03:08 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 08:43:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 08:43:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dcab0b270d631ffdfee1c090f676984c71b03f87fc76005b512418b2ec110c`  
		Last Modified: Thu, 29 Jan 2026 19:17:49 GMT  
		Size: 291.5 KB (291499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3c8f3022c37addebb7f3bba04877b6aa3acbe5feb276f525d0db506f58caad`  
		Last Modified: Tue, 03 Feb 2026 08:06:29 GMT  
		Size: 90.6 MB (90557299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b778cd0b2a4c3c8e4c3a23411f4ef01ef3e19c5f4068684d7c99ea603a26270`  
		Last Modified: Tue, 03 Feb 2026 08:44:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:986f4289cb7437888caa34dc5b51eb527f0268a058cf98f26d2595587609351d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfb7bdb7af9197b90b0d71413b27d45466f72a6b8b3edd335f601d086f21abc`

```dockerfile
```

-	Layers:
	-	`sha256:50935fda1c10d08ecb2ceba18269fee75bea6fd7a5c419c040a1eeed4fe39b6d`  
		Last Modified: Tue, 03 Feb 2026 08:44:57 GMT  
		Size: 193.1 KB (193065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbf89932344bfb76bfaff09565b544e01409094e6bfede40d411fdc1e8b9ba51`  
		Last Modified: Tue, 03 Feb 2026 08:44:57 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:7a4e9e94418999c3b505449acf10cab780bc734d51059ded3480b5c78e629345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96513176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd2197ce07de3d06a3367fb680e4d2ca0482d90e8896bacc5f64fb746f31833`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 07:11:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:28:52 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:28:52 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:28:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:28:52 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:28:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:28:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83b6b4e7826d3ddebd9c48a75091c1c37e104afa456d3507b2ce5beab9301e2`  
		Last Modified: Wed, 28 Jan 2026 07:14:36 GMT  
		Size: 292.1 KB (292142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7062bfc50107a913a5fd7c0d090af1366da08b74147cf71ec4490488730775`  
		Last Modified: Mon, 02 Feb 2026 19:29:23 GMT  
		Size: 92.6 MB (92570442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5c96bc5ce39fde8e48af7552ffeafc272c948a63d413ab11c236f84ab96fad`  
		Last Modified: Mon, 02 Feb 2026 19:29:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:1049b96bd3e8778fc3f521b6f3d1610fa34c782d64c08534db5e906bdda23f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 KB (217496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662eb086819b45e74ff74ec9d90820428881a46f6db71e7659dd396ee28065fc`

```dockerfile
```

-	Layers:
	-	`sha256:fca573219ef957f57c2eefdcf5bfd88554395b594a083fb9bcc90e41a16cb70b`  
		Last Modified: Mon, 02 Feb 2026 19:29:21 GMT  
		Size: 193.0 KB (193031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe5a6df4ceef881d8da1de00c0cdf140d80f5689d5eda516952576446e057b89`  
		Last Modified: Mon, 02 Feb 2026 19:29:21 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json
