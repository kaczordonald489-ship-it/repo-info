## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:613bda756a2e5d81566fbb51894596db68330bbfab65ac79dd08f9d67a218930
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

### `golang:tip-alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:29a4dd4fac557b11d9f845b361a1cb5d2884abdae14d6c6056ccbc033aba38be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96369083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa4ccadb24ddc058c8dd7b5bf9194697dbf18c2775f5c5aa6d972cb9b0da53e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:36:09 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Nov 2025 22:37:51 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:51 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:51 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:37:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:37:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190d670ea41423b1eac5bbd64807902df38fb4b53ee313e77c90d85c3475cead`  
		Last Modified: Mon, 24 Nov 2025 22:38:18 GMT  
		Size: 291.1 KB (291127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5d9efbcfd700910b298e2e1f088186b48b23d603a67b46866474897785fcf4`  
		Last Modified: Mon, 24 Nov 2025 23:12:20 GMT  
		Size: 92.4 MB (92435230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040111fa309acac95e40468c095eba887ed9e8186b8a7c3e3f29e2cacb4e79af`  
		Last Modified: Mon, 24 Nov 2025 22:38:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:5ac7635d2b8b3adba813ad831a6991dccffcabb8dc738524bbb0676da50a7a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa5045362a1a7d79761386d4f713ee9c8ff9f251e81e766dcd249d86452a507`

```dockerfile
```

-	Layers:
	-	`sha256:ce77acba98ebecf0eacb5014365340716e29ed1a78ae0bef8ea91108aaa6e52c`  
		Last Modified: Tue, 25 Nov 2025 02:33:24 GMT  
		Size: 194.2 KB (194205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2803d263bee406fd16cda4857e26a48b30b418590e7d427c90484cfe1783cf44`  
		Last Modified: Tue, 25 Nov 2025 00:24:15 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:504daade5a7b03f445cc6025e8c96ac7b6791f22216de33c4ad9bb7642f5ae7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92465458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a558194057a36edc70b08cccd7e3b59368adab3e24407d42a106c055067cbe9a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:35:52 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Nov 2025 22:38:22 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:38:22 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:38:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:38:22 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:38:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:38:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d98b92b4f7e87ff4c1d7f4e341a8760d982a7b2cc8b5918f2898716bfffd10`  
		Last Modified: Mon, 24 Nov 2025 22:38:42 GMT  
		Size: 292.3 KB (292256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c12680c1c52d1e09ba628f5cc41f89b03d667d07dc7b9428bda229f05fc1f69`  
		Last Modified: Mon, 24 Nov 2025 22:37:53 GMT  
		Size: 88.8 MB (88807576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e31a81b18fda853eb696c9b3f181e49010e3637506d225a890bb11ca1bf1dc`  
		Last Modified: Mon, 24 Nov 2025 22:38:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:1452e934a8a7c5b928a972bcfed90dcede7ed81b0e1463c760e95705d506fb5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507e5a2ddddb4822b6ceb12379ba7e24c59a2e13f62a5553e40dad2740360f7d`

```dockerfile
```

-	Layers:
	-	`sha256:7c8486d13da928e425404b21bff8ef9bd9daeaf952e158efb200c5176504e909`  
		Last Modified: Tue, 25 Nov 2025 00:24:19 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:2915829035e2e47612451a30fc7843533734fec6c27841480bb3d52e4f71dfd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91943889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6a41841727592236d5447c68e61387785dc5a7656310e13fb8bbc627018edf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:36:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Nov 2025 22:39:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:39:25 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:39:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:25 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:39:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:39:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba89bd71f3640b5db1142464d08d4f434bac9436822e6eb7f56f20c9abcd9bbe`  
		Last Modified: Mon, 24 Nov 2025 22:39:48 GMT  
		Size: 291.2 KB (291161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84acd51792b44af9faab6b3fd0d7f172d2f21a4324de65288c305f1fa5a5cb15`  
		Last Modified: Mon, 24 Nov 2025 22:38:11 GMT  
		Size: 88.6 MB (88553959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03cc3e003030c8ba9bff9beafcad2149036b41f4b4bf000d29913d547d6359b`  
		Last Modified: Mon, 24 Nov 2025 22:39:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:a8f45528d8c55fa70267c38a960efb8edc77a98aa79dfee8ce12a6fa5cc25fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0393c8e98b3e681e73f1b36b3f6ee1c599e37ece2e3df50333dbf6f246134f`

```dockerfile
```

-	Layers:
	-	`sha256:135c0ca0cef18acb9e9051c6144fe788827841d3712f9b35b2187d84b37dde98`  
		Last Modified: Tue, 25 Nov 2025 00:24:24 GMT  
		Size: 194.2 KB (194209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a2726723d9fa2b0311f5971af700e81eab04269cad5d6f08d53d28159eceda`  
		Last Modified: Tue, 25 Nov 2025 00:24:24 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1dac3045db6f08eeecf75689a3e54a259cc0e6f0f111783690e358b12e6d3760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91906436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621f55554144b6cf310556183fca1e12870f1566577b3c1bd86f6cbd8bb23624`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:36:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Nov 2025 22:38:10 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:38:10 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:38:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:38:10 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:38:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:38:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0dfa2f9a418b0f7c7fb0668f997edfb46429d911e4c863984f54648599b73b`  
		Last Modified: Mon, 24 Nov 2025 22:38:34 GMT  
		Size: 294.1 KB (294066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c063ea817571a2589abbf80a2044e326fd503e0a108dc319a7ad8231dbc1d73`  
		Last Modified: Mon, 24 Nov 2025 22:37:19 GMT  
		Size: 87.6 MB (87619860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4fa3f2fd7cc601df2993cda24e9d58025864fd3eed9d9bf6950bd0a2f13e82`  
		Last Modified: Mon, 24 Nov 2025 22:38:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:97f7512246ee2afae9a371f147b2ac144ae3d60e5a58b10c2bc996bd11cbd6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181528e50c8a40ee5d198e4176d54df21fd243f2114a04a60bad02240c4567fb`

```dockerfile
```

-	Layers:
	-	`sha256:ac6dc3e39ac149ac55f78422d23496377cd35b7a6e1d1e6a3959fd6011cd13c3`  
		Last Modified: Tue, 25 Nov 2025 00:24:27 GMT  
		Size: 194.2 KB (194237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cdcea1e1454149e837f08aa17a21baf2f69006e05b19a54377a7e2817f5553d`  
		Last Modified: Tue, 25 Nov 2025 02:33:42 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:eb8e2d84887985de7486b3b5d577e4b1aa28f294c2626ebc2337f450404a9c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94119748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221fea73b65c86ecb690f9f5e390749e77d4605122abf2f02d9ae8bce0acbaef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:37:55 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Nov 2025 22:37:15 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:15 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:15 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:39:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:39:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e474d229f0eb7e68456b51b195a32899e8afb8c62dcf25de17cbb702bdd3991b`  
		Last Modified: Mon, 24 Nov 2025 22:40:17 GMT  
		Size: 291.6 KB (291598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba70aedae48e82029642c62322f6ff74fb35e5b6234375d05c3be6a27f83fa3f`  
		Last Modified: Tue, 25 Nov 2025 02:11:57 GMT  
		Size: 90.4 MB (90363290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0750eca204e6347b4c975ca9aaae716b2f1d29f7d82ee457897b24199c299b46`  
		Last Modified: Mon, 24 Nov 2025 22:40:18 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:60d2947db3b09d320b97007714fa613d4c21a9b75bdb217e995ad5789472f381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 KB (218606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5f72bfab960926bfafb1d5dbbdd0b92e759065bf3b4e8438d0df64442ea482`

```dockerfile
```

-	Layers:
	-	`sha256:58c57f8207c58776d47bbcae9e56306aee11ee2efa15356d5a02f6adb45d6a94`  
		Last Modified: Tue, 25 Nov 2025 00:24:31 GMT  
		Size: 194.2 KB (194174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f6de620a0fe8433ead068147cac702674451f931060838c61b91aae3a5f018`  
		Last Modified: Tue, 25 Nov 2025 00:24:32 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:0b4ecb81ecf78d15d8b7fb23723306c42ff079cda5975be840c73c8a70053fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92941197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8e3e6a3fb712b5edae561f47a9a7e07a250cef981fae0c35eb92955fee58ea`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:43:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Nov 2025 22:37:36 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:36 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:36 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:43:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:43:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d14bc2600d22e26b66141fbf5771e98d7b9f0ed471d3d19e6d7cdec0462ee2`  
		Last Modified: Mon, 24 Nov 2025 22:43:59 GMT  
		Size: 294.5 KB (294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c192b4221bdae7479c6a0a0cefbefa83b4b143b2a4b40e323ae02e100ce6102`  
		Last Modified: Mon, 24 Nov 2025 22:46:59 GMT  
		Size: 89.1 MB (89072428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffbc2d7039984d94a77e9b320cd0fd8a3c9788c2e99a130e0eaec0d654f1ac9`  
		Last Modified: Mon, 24 Nov 2025 22:43:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:374d227b9d6507f4b55eaf663757a957507be5e42dea3d32d1699f5ba0978550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b7dd85a5f73ea42a5569c579ff35b2d6fee9d46fa9bcdacb2d2e6f8f7368a1`

```dockerfile
```

-	Layers:
	-	`sha256:0352afbc0c98770edd028dcbdb5ecc5de5684f2bbf06fb1b8f5e450f308c6dc5`  
		Last Modified: Tue, 25 Nov 2025 02:33:50 GMT  
		Size: 192.3 KB (192292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f7ec628c3a51c91bcab8acf268de725a07f8c3350df1d250e594b8eedc691a9`  
		Last Modified: Tue, 25 Nov 2025 00:24:36 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:3d1f18e741aa60b3aec64329955e7a90e9b634764aae84a4789ffb20aef3efda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93321378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74cd4a12ef9028def496aed427cbc7b14357d5ad4ab4ea02ed68b4846a30c05`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 07:57:08 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 25 Nov 2025 06:38:29 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Nov 2025 06:38:29 GMT
ENV GOPATH=/go
# Tue, 25 Nov 2025 06:38:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Nov 2025 06:38:29 GMT
COPY /target/ / # buildkit
# Tue, 25 Nov 2025 07:57:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Nov 2025 07:57:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f874295bfcd01a87ee99265d45f0786d35242cd9d53bc2744cb330bf3be277f5`  
		Last Modified: Wed, 08 Oct 2025 21:19:05 GMT  
		Size: 3.4 MB (3351001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18712178673f08c74f02c4b24f31fd1452a6014b2c1769c0702341368bb31984`  
		Last Modified: Tue, 25 Nov 2025 07:58:45 GMT  
		Size: 291.5 KB (291482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d737de4a2a89a200a514c4bb9d33946647ec30322b982a3272843e60840a135c`  
		Last Modified: Tue, 25 Nov 2025 06:45:54 GMT  
		Size: 89.7 MB (89678738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7ad0e7f2b75e21f9b22906f57019eeaca4c6f9572fc3b2f212fbd0c5596247`  
		Last Modified: Tue, 25 Nov 2025 07:58:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:dbacbb802f3e8120f6c64de8744658de6ca253957c71bff9afcfa98bfddb6390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583118d7aeec1c4572acbc2057c64efaa83e110dded3f43d3d5d2503cab7f8fd`

```dockerfile
```

-	Layers:
	-	`sha256:5b70292d23cfff0883e41d095fce036f12f5defcecd2aa7bfafc9c0b7962122e`  
		Last Modified: Tue, 25 Nov 2025 09:23:33 GMT  
		Size: 192.3 KB (192288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f11c36c08354c82f603ce277eab8192425e68533253af26c5ab48241f99d09a`  
		Last Modified: Tue, 25 Nov 2025 09:23:34 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:9dae1682fc54595d27d769efb91ff3ad866ef7c042b106ec0e9d475560053eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94382649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455d377139bbf9c44b576f9f864cdbff9e15751d9684be270eb2e330fc2efbe1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:37:38 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Nov 2025 22:37:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Nov 2025 22:37:19 GMT
ENV GOPATH=/go
# Mon, 24 Nov 2025 22:37:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:37:19 GMT
COPY /target/ / # buildkit
# Mon, 24 Nov 2025 22:37:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Nov 2025 22:37:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d509e219c5ad3999bec42645217672b0ca85b22769fdf4a1dfd591af7e5d05`  
		Last Modified: Mon, 24 Nov 2025 22:38:18 GMT  
		Size: 292.1 KB (292104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c00d64c48f24f624221defe9715cae4847baad7ac3f98d927259b00270c75f2`  
		Last Modified: Tue, 25 Nov 2025 02:17:38 GMT  
		Size: 90.6 MB (90623953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1167cc0262584509824c3a00b9d64b816e50588d16c2d2a88c75522c587bc20`  
		Last Modified: Mon, 24 Nov 2025 22:38:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:8bd1502a957639659d0b52f64c2176a3b18d9f7465036737bdfc81f1bd86dd9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 KB (216546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2758e9967ca85f11e51199a2874956ad3ab41ba87cb08791ecf34ee22eca9789`

```dockerfile
```

-	Layers:
	-	`sha256:56a81aa9d6f99746be2bd35cb69688439f991df2d7b137ae5c8218a1cfae7e5c`  
		Last Modified: Tue, 25 Nov 2025 00:24:40 GMT  
		Size: 192.3 KB (192254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bce863ecd2e0be6081d53002cf4e1b4d86a86bf520a730c04a2961c4101eaea`  
		Last Modified: Tue, 25 Nov 2025 00:24:41 GMT  
		Size: 24.3 KB (24292 bytes)  
		MIME: application/vnd.in-toto+json
