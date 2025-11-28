## `golang:tip-20251123-alpine`

```console
$ docker pull golang@sha256:c69e7518c5e21d1fe97c46cbb3710073db0405325b7b7407839974b66ff66f2a
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

### `golang:tip-20251123-alpine` - linux; amd64

```console
$ docker pull golang@sha256:c909cc89fe0d05a9c72daf708e7a8496588f7d2a466c07f316487c59e6aaf928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96528993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bdd439844ec0f09a947648c7a4859241ac371a9fa6a1dcabcc74df10c572d4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:36:05 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Nov 2025 22:37:44 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:44 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:44 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:37:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:37:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c696b9eb508574cae54a501bfdc2412c1537518285fea21a82a13588e18b36`  
		Last Modified: Mon, 24 Nov 2025 22:38:06 GMT  
		Size: 291.2 KB (291153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5d9efbcfd700910b298e2e1f088186b48b23d603a67b46866474897785fcf4`  
		Last Modified: Mon, 24 Nov 2025 23:12:20 GMT  
		Size: 92.4 MB (92435230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340b7b613d8833ac6164fee59d162afb2b5e4d6d95684561028c7d39860acf7f`  
		Last Modified: Mon, 24 Nov 2025 22:38:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251123-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:1e6aeb5a415808fe519f411911e71d4ef66d87b8f0a05d8dc4ca3056739ed0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e557dd583a74d52d8ebe751637acfd900ab251499875f813bf20ff2861be55f`

```dockerfile
```

-	Layers:
	-	`sha256:714b7bc78c2485b9acff79a0bf4dcf9edc75770339441c6d2b056c57e3237584`  
		Last Modified: Tue, 25 Nov 2025 00:23:59 GMT  
		Size: 195.6 KB (195612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0093c65f0730fa8cb568ca8cd834bd07e63d912f5648c018801f936e409e61ec`  
		Last Modified: Tue, 25 Nov 2025 00:23:58 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251123-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:05855e230f32d6a22bc864e6a273c30e9d3f88a5fb63c04f8cbacb25bebb8f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92604146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c79071bd618724b409904bf9fa0bbe6defda0a622f3d66e71c5a4e947ec701`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:34:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Nov 2025 22:37:13 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:13 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:13 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:37:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:37:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b4ed8b016bbbc0d3aa4aa662509aa10d7e23087a2e253f92413f17c261f13c`  
		Last Modified: Mon, 24 Nov 2025 22:37:41 GMT  
		Size: 292.3 KB (292332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c12680c1c52d1e09ba628f5cc41f89b03d667d07dc7b9428bda229f05fc1f69`  
		Last Modified: Mon, 24 Nov 2025 22:37:53 GMT  
		Size: 88.8 MB (88807576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc281f87faf60bc56453ac525bb984e8d63582cbdb6e7d3064b32e71d747b764`  
		Last Modified: Mon, 24 Nov 2025 22:37:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251123-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:0527eedd84e81d86536055dbd9e7b2b1b47e1868f19dcca76df5e76eea82efe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b17db66df83aa320077373025a3993c9493bd77444cd5e54d8cd0f877ba1c5`

```dockerfile
```

-	Layers:
	-	`sha256:1eecbdad32c90da9d4e1be18882570e717104adf9962ec409ccb17655f516bb9`  
		Last Modified: Tue, 25 Nov 2025 02:32:54 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251123-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:fad266b30608043f23f77759ee3a1105a064264b36e107a441c61bed49789c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92066884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b341aad302c82c905a0c198a745fc3d1e0e09a73f73a70395888c5cd12fbab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:36:55 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Nov 2025 22:39:32 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:39:32 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:39:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:32 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799f56712d0f153216d2a4f9d10755a1b02791496e1e957f6a723f3bdbfe312b`  
		Last Modified: Mon, 24 Nov 2025 22:39:57 GMT  
		Size: 291.2 KB (291212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84acd51792b44af9faab6b3fd0d7f172d2f21a4324de65288c305f1fa5a5cb15`  
		Last Modified: Mon, 24 Nov 2025 22:38:11 GMT  
		Size: 88.6 MB (88553959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2189d39e443ee78710fe08eecd9dafd071b1851dbafbbe41688ea221dde0860e`  
		Last Modified: Mon, 24 Nov 2025 22:39:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251123-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:7dc289b9f2738f3fd8f8e83935868ac9488fd421e336421c7e7ec13cc264e0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad06610703f3394ccd8644d924915bc8bb628dbf27ec7418111be5dbcdfb406`

```dockerfile
```

-	Layers:
	-	`sha256:ddf13dd0fd34193a6cd3a5ecf7d28f4104169df40dbd5abcc4becad262ed2897`  
		Last Modified: Tue, 25 Nov 2025 00:24:05 GMT  
		Size: 195.6 KB (195632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7bb75bad3b894c278c68e379eeabe7962085b16c2962cc5953b81a3dfb254ce`  
		Last Modified: Tue, 25 Nov 2025 00:24:06 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251123-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:55b88dfd4051c61976fadc45d1629acfbf13d6524d025c7d9933471f2c30fc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92052194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c644d493793924fbcf933050aff69443dff73f85d3b287cdef3ef7d3c618a9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:35:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Nov 2025 22:37:28 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:28 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:28 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:37:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:37:30 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf5573d09747e883179906484a4fed4df310c9189587a307c246083c3b0ee2b`  
		Last Modified: Mon, 24 Nov 2025 22:37:50 GMT  
		Size: 294.1 KB (294107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c063ea817571a2589abbf80a2044e326fd503e0a108dc319a7ad8231dbc1d73`  
		Last Modified: Mon, 24 Nov 2025 22:37:19 GMT  
		Size: 87.6 MB (87619860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8ecf02a8b5bc5aad03154e64e610676710ffcd7cf7de188c9f0cf5d6c6d52b`  
		Last Modified: Mon, 24 Nov 2025 22:37:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251123-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:38c87c337326b55f304e37f0d253ef9d9410ccbd9bf153121908d715a53f482c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76ce5d79fefbd2b58e7fcc23d5a0f4dd03c0e7987608eb2ce8b3dc3daa9a10c`

```dockerfile
```

-	Layers:
	-	`sha256:b488a3089447ae8f0d9fb2d2b519f7ee24da28805a3a0619543f37ee1932174a`  
		Last Modified: Tue, 25 Nov 2025 00:24:10 GMT  
		Size: 195.7 KB (195668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23c4c4a94d7c5e844af60184fdb3aabb2ed256b567b1601c6183699943a0f058`  
		Last Modified: Tue, 25 Nov 2025 00:24:10 GMT  
		Size: 25.3 KB (25254 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251123-alpine` - linux; 386

```console
$ docker pull golang@sha256:bea310cf7d12d553d15cfcfbf9a380fae7b0143b4d820ab47b7f425707a1889e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94274023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd65479e86f2511a21e892209650dcf07b1940d3b23d4d81c4541dc543e16c7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:36:08 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Nov 2025 22:38:15 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:38:15 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:38:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:38:15 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:38:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:38:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b5b68d78469ade24f53439063dd08f9ce2fdcacaff8ecc7752761a37cd9385`  
		Last Modified: Mon, 24 Nov 2025 22:38:38 GMT  
		Size: 291.6 KB (291644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba70aedae48e82029642c62322f6ff74fb35e5b6234375d05c3be6a27f83fa3f`  
		Last Modified: Tue, 25 Nov 2025 02:11:57 GMT  
		Size: 90.4 MB (90363290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097e949bcbfe658730f43f435da764411835bba10bb200a335dbd8e2af9a3f19`  
		Last Modified: Mon, 24 Nov 2025 22:38:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251123-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:34d458bc9c105d697e2e432dfa458dd803bb3acec5e8093bde0abc3e8e007718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809e046efc205c44c5604209a7ae486c44450dca34012c2af92bf803ae8c44d4`

```dockerfile
```

-	Layers:
	-	`sha256:110f031c58237242a716ec43dd229b2c684c49c857624bfec0e1f36b365a71e4`  
		Last Modified: Tue, 25 Nov 2025 00:24:14 GMT  
		Size: 195.6 KB (195571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78a8d6415b56203e4a030cfdcf04caa0d6f8cd8e6986cccc5b2a910a2b90e57d`  
		Last Modified: Tue, 25 Nov 2025 00:24:14 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251123-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:8a3168247d6928be82610060561eee43475a533d92c2e132fb496e6ecfd95919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93099419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a67589f04fc0c3c54a0f7f03e6a7d28f970aa043ce79df5190f693d03afd35`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:43:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Nov 2025 22:37:36 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:36 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:36 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:43:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:43:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64958bce21ae47528776dd8bd6794140e1f5086c72ae8807ba8f48bb37fce769`  
		Last Modified: Mon, 24 Nov 2025 22:43:59 GMT  
		Size: 294.6 KB (294592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c192b4221bdae7479c6a0a0cefbefa83b4b143b2a4b40e323ae02e100ce6102`  
		Last Modified: Mon, 24 Nov 2025 22:46:59 GMT  
		Size: 89.1 MB (89072428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96f85f10c579e3515aef85e4242cce954fc4198af1df0a2adb67e1a1229dd28`  
		Last Modified: Mon, 24 Nov 2025 22:43:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251123-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d420a861887cd2ab0b0a749534546f1bdcae036758134a1e1cdac4713bc9165e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a69ba61a4694ce542354767b29576c6670f0e9d43ba3e94cdd06f63c14638b7`

```dockerfile
```

-	Layers:
	-	`sha256:1badc52f16f92da332bd46df0d6fa19408693ddd6410d957b98fa51a31a82a33`  
		Last Modified: Tue, 25 Nov 2025 00:24:18 GMT  
		Size: 193.7 KB (193711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f9c028adb500f8789cac3b879d94397754fc0ddcbfd2a63e17d912fb7ec6ad`  
		Last Modified: Tue, 25 Nov 2025 00:24:18 GMT  
		Size: 25.0 KB (24980 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251123-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:89ee7fa654e7aaba3761f29a71eda5b7e42e293c2541b3cc170bb87f8b22c095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93485658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c43e3df6c706bd2c2bc06baa6e33574b4f1af4e3ce68721dae2fc3adf3284a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 07:20:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Nov 2025 06:38:29 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Nov 2025 06:38:29 GMT
ENV GOPATH=/go
# Tue, 25 Nov 2025 06:38:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Nov 2025 06:38:29 GMT
COPY /target/ / # buildkit
# Tue, 25 Nov 2025 07:20:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Nov 2025 07:20:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a984176d166c6f9d398140e2c603deed3f1a52311d2a418b830c1cfdaffb3c`  
		Last Modified: Tue, 25 Nov 2025 07:22:38 GMT  
		Size: 291.5 KB (291523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d737de4a2a89a200a514c4bb9d33946647ec30322b982a3272843e60840a135c`  
		Last Modified: Tue, 25 Nov 2025 06:45:54 GMT  
		Size: 89.7 MB (89678738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c6b198d7ab1fcafec20f7a56dfed62dc07de66bc50d2dc83c90a2b97fa7c4a`  
		Last Modified: Tue, 25 Nov 2025 07:22:38 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251123-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:9c9393f6cf5ba4a74fe09030fbb9a473773a88c6ad451601bb66737db2f9ed5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a1f625e14eb9b5d031f7aa0a317eea09fae59e954dc210e307f18b78f2979a`

```dockerfile
```

-	Layers:
	-	`sha256:2713188e5e934129b909cf0818dc4f63b7a411b95431cdbdc33229de22b850e3`  
		Last Modified: Tue, 25 Nov 2025 09:23:28 GMT  
		Size: 193.7 KB (193707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1692df96fdc1ecdfc72d431bedc6ec909d026edee14a0a0a99795b5ca33939fb`  
		Last Modified: Tue, 25 Nov 2025 09:23:29 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251123-alpine` - linux; s390x

```console
$ docker pull golang@sha256:c10574c882c8235b2bd9b904f1ba3675720de2a0d5110dd91ac6125c6084b4bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94565505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750365b752e8e821592dc6aa69965161a0aa58c9187f85089cbf52df02589e93`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:37:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Nov 2025 22:37:54 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:54 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:54 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:37:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:37:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94177cc1b10be488b5d187dad00f1ccc030bc5cd416e55c943d85498ded2fbfe`  
		Last Modified: Mon, 24 Nov 2025 22:38:27 GMT  
		Size: 292.1 KB (292150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c00d64c48f24f624221defe9715cae4847baad7ac3f98d927259b00270c75f2`  
		Last Modified: Tue, 25 Nov 2025 02:17:38 GMT  
		Size: 90.6 MB (90623953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5972f3f34169707e5c58e3df4a5be77c45f4684c08dbe468461feac27f0c83`  
		Last Modified: Mon, 24 Nov 2025 22:38:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251123-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6c402ee5a1c6b60dcfc85399aa86c9a3df37ed4b47c1e2af670e740aaa5bcd86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6f8fc47251cfc4b5aeeacef43a99e06df0010b9576a7b65221cea24fefe33f`

```dockerfile
```

-	Layers:
	-	`sha256:db34393df4e0e3e8f4e877cd165c7cc140b859f820526916f640e03653a39fc8`  
		Last Modified: Tue, 25 Nov 2025 02:33:18 GMT  
		Size: 193.7 KB (193661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f983bb0674d81d42917523e40310510dfbebf3db9c49680d3996002768ddd58`  
		Last Modified: Tue, 25 Nov 2025 00:24:22 GMT  
		Size: 25.1 KB (25093 bytes)  
		MIME: application/vnd.in-toto+json
