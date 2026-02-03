## `golang:tip-20260131-alpine`

```console
$ docker pull golang@sha256:73664d1ebb91c7813c230c25fb38c41112a73dfdd0c9cc524e63e5e35754d48a
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

### `golang:tip-20260131-alpine` - linux; amd64

```console
$ docker pull golang@sha256:79f94ebd9d819feba248c489b3c9ba9462a1efa902172e0d117de694859bad03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97491462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5a7b69a6e78562f4a917a56bceabf153f42f33e35f393bc1a9622a826840ec`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:28:40 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:30:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:30:23 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:30:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:30:23 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:30:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:30:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e68306766aa04bd4a0131b705c7f278d14b4404df913ab2c6283d5c898f46e`  
		Last Modified: Mon, 02 Feb 2026 19:30:39 GMT  
		Size: 296.1 KB (296074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ca55bbd490d4f215c5420355c680b71279036da5d7c91d2d678e32c231a9c9`  
		Last Modified: Mon, 02 Feb 2026 19:30:41 GMT  
		Size: 93.3 MB (93333409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146c40f4be31c7e1f1ef0653134167ad0b9d8f61bdcd6fe2bd5ef23ec16cb699`  
		Last Modified: Mon, 02 Feb 2026 19:30:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c64f4b4a0d8fedc6cb2bf5d491155ba421ed1c9baf5b5ca02df1607d58cf2212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be4b1c5bcd94e3c692fa6202ef6ff9af5006ecadd32a277d130f1bb84084d6e`

```dockerfile
```

-	Layers:
	-	`sha256:799c76a5079aa6305f45d6916460d0599c8e4d129833942a826ee044c645894c`  
		Last Modified: Mon, 02 Feb 2026 19:30:39 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91546c535c9c0f7de584b4e58ede5533ea4a9afcd450cba08f8eeb853cdce170`  
		Last Modified: Mon, 02 Feb 2026 19:30:39 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:8b3aad708469e53e46471dc7fe1cfd97ef4f07ccf2f27aa40ec58c06a11e3543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93623087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afaa893dc05f0de9c78af5732129f8ebafbbd6d84c1048db693983644b6e5ef0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:25:34 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:28:22 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:28:22 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:28:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:28:22 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:28:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:28:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51285428f26f6cb7d23cd4f95bb49f0af5b02163caae1a198291110464713924`  
		Last Modified: Mon, 02 Feb 2026 19:28:36 GMT  
		Size: 297.3 KB (297268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e0df2db5a6de63ae56b2b7ac54a7918fd9414ba7652c1dadac1bfb31d63c9e`  
		Last Modified: Mon, 02 Feb 2026 19:28:08 GMT  
		Size: 89.8 MB (89755840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc1018f1551a137ee43fa9b351e72d09aa91af6d4375f1c6ba9d0f5b492beb6`  
		Last Modified: Mon, 02 Feb 2026 19:28:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a075ff0480a0ae6be36bb7a5b42896bf5b72f177963b85b490e81b75bcc9ff61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049d2f26753d3ef7f6696234ade7a5812874bffa9d21865e110186c30daaf282`

```dockerfile
```

-	Layers:
	-	`sha256:bc5735f435dc2cb82479fb361920fecc0203627061b9878cbf060479471ed7f1`  
		Last Modified: Mon, 02 Feb 2026 19:28:36 GMT  
		Size: 25.0 KB (25007 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:b0b3f14f3117fff84c2b79f0719aa9389e289355b39fba11d989f37f8c211ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93054509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d39f4304a5c49d7dd85a7eb8de1eb2b924189f6a3e54ee7878653d96d4eeeb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:28:22 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:31:07 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:31:07 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:31:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:31:07 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:31:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:31:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b928d407745357bfb289eaa3909a660bc334dfb2c0eb242035a95354d1d92690`  
		Last Modified: Mon, 02 Feb 2026 19:31:25 GMT  
		Size: 296.2 KB (296198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c4d8d165092e2ffa5f6928ecd151df0b8f3dc1362c8f59dcd6d9b09df5017`  
		Last Modified: Mon, 02 Feb 2026 19:30:25 GMT  
		Size: 89.5 MB (89476429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a212b493bd5b6bde8fab205d01be43e8a8ee292993da2acc391cd18f29b5c70`  
		Last Modified: Mon, 02 Feb 2026 19:31:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:7c0b240c4307ec110dee08ece5cd40e5b7c9df64f989f597f99739e0fad023b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9adb0626593dab6df2ce3760700f1b7e4d6e9d58c963707404189c73ae0176a`

```dockerfile
```

-	Layers:
	-	`sha256:d17a719bf7c5d5d86db55914156e1fc5dc1b725dd9861bad930db46114944092`  
		Last Modified: Mon, 02 Feb 2026 19:31:24 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5770da8785b55abc67ada6460bf29eecfda976a7ea79cfbe6f170fca6c31104b`  
		Last Modified: Mon, 02 Feb 2026 19:31:24 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:46fbb71948b48e013573c7c4a9dbae5dd2d5a78d9440ddbabce967dfbce65689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92871782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5346d2e2eed97e845ef4e15e54ce5f050807502009febdbe06bb774a88831a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:25:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:27:07 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:27:07 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:27:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:27:07 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:27:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:27:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad6ebfcd7078f536e3f32b242f0089d55846dfb54e181d6edd0c5602634b25f`  
		Last Modified: Mon, 02 Feb 2026 19:27:24 GMT  
		Size: 298.8 KB (298833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6a2a8a6cfc628c3f67b49421d89d0e853e9d214495c3cea23b3d909be150cb`  
		Last Modified: Mon, 02 Feb 2026 19:26:36 GMT  
		Size: 88.4 MB (88375700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d7adc0bb6e991ba362b2a1595c29157f302fc1531693028f657fd186d4aa38`  
		Last Modified: Mon, 02 Feb 2026 19:27:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:0a2db3e5062446bb2a538ca5e3125428f043685dc0ddeba1ea96cc6389342809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad350e19fe64c0d2c65d09971a77481495a659c2abe2dc2d75fa8b556cd9cd80`

```dockerfile
```

-	Layers:
	-	`sha256:bad6b081a7dc2a2ac1663e24adc8dd00a8ffe8b14130a9991b555f948b571304`  
		Last Modified: Mon, 02 Feb 2026 19:27:24 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b88819acb6c6dcd9ebf077309b6efbc134f98a57fe05e4706d7a044e9ceb0a8d`  
		Last Modified: Mon, 02 Feb 2026 19:27:24 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-alpine` - linux; 386

```console
$ docker pull golang@sha256:1e3eb8522e49e69bcacd57dde8bb7d948ebf62b267f6aa36f4c1accece413207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95390059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c77779b903197da4b9fca637f675ab9f03afdbed6f1f027aa9a0c1416463c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:26:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:28:04 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:28:04 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:28:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:28:04 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:28:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:28:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb53a7ef72df007d48f228e03c12f50cbde092bd6634f723046f676dd9629d2`  
		Last Modified: Mon, 02 Feb 2026 19:28:19 GMT  
		Size: 296.7 KB (296667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4604cae1ff047094cf665f2719aaf0543d71e670a699786143900320f6ba300`  
		Last Modified: Mon, 02 Feb 2026 19:27:18 GMT  
		Size: 91.4 MB (91406236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db3688368bd76b52b60fa12686cc12d1aa99b1ea37748869112a7a7b94a8cd2`  
		Last Modified: Mon, 02 Feb 2026 19:28:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:657fff1adbbc7ac51566fce2e382708397d85806bb721a3a99a50f873d05ef36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9ebed2cb5217d4cf73513d409b9c44334ea61bbdff75f93e7232bff468f701`

```dockerfile
```

-	Layers:
	-	`sha256:d4b4f994609f4370624f564c3776a6eb9ef13022b064435b3c627466da9406d8`  
		Last Modified: Mon, 02 Feb 2026 19:28:19 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12b4a7db5d3c04a00df8c128089847d2f4b22f182b2aacdbfe6679f0922fc94f`  
		Last Modified: Mon, 02 Feb 2026 19:28:19 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:fb69beb42a18bc112b4c8a4f5e98a696d6a56d7fe46023bec96b51df349bba6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94136426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33afc20d1a4e387489ab411ad09c18c2168a6a9a8c128b27488b4b52b8b30d92`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:05:09 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:27:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:27:20 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:27:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:27:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:32:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:32:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd73d3916f2fedeed1c534628f9a66641a5e1350de62984f598c99fe3383aaf`  
		Last Modified: Wed, 28 Jan 2026 04:06:04 GMT  
		Size: 299.3 KB (299261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e432b6dca22e637a3a25408001c269ffda0f2c5d9306b2f7174d2a31051778`  
		Last Modified: Mon, 02 Feb 2026 19:28:34 GMT  
		Size: 90.0 MB (90007365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7785ae9d9380fa199f7810cdb0026f491fefbdc050bda3f571675bc494177882`  
		Last Modified: Mon, 02 Feb 2026 19:32:47 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d8c14440cc8a6352157a3cad0e257fb590c4ce3eda40d03e9bbbc27ce9fb59a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df954ac56749fe976e30d7f8aa9833917de761fac4a34fab6acfd6d6e26e0459`

```dockerfile
```

-	Layers:
	-	`sha256:bf1ed92502cc4e6c228902270cb5f41f8c85c852e49eb9b20a6fbdc836e6a1fc`  
		Last Modified: Mon, 02 Feb 2026 19:32:47 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04e71f86bef20c12b85706ee5f370b51b36d68426171f4370f65f02b3e8b6181`  
		Last Modified: Mon, 02 Feb 2026 19:32:47 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:599a8cdf5e8e0a1f8ebd3e86c5ffd714a8cd2048ffd4d6b88a32a5cbd0623634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94439249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51a2a0c919fdf90c3c6d0365278a9016f6e2ff9a1ff18c1d6f28d77a02a13c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:12:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Feb 2026 08:03:08 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 08:03:08 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 08:03:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 08:03:08 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 08:03:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 08:03:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f6a28a44ff91c18ab295ffef6822bbaccafe002bd1f4a117c179d363e86328`  
		Last Modified: Thu, 29 Jan 2026 19:14:45 GMT  
		Size: 296.5 KB (296505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3c8f3022c37addebb7f3bba04877b6aa3acbe5feb276f525d0db506f58caad`  
		Last Modified: Tue, 03 Feb 2026 08:06:29 GMT  
		Size: 90.6 MB (90557299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc906b07f89304c50db3daf7c402a93d81433a57a8d9e6c6cf3cf17e83e43249`  
		Last Modified: Tue, 03 Feb 2026 08:06:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:53a827781e309b0cb5d418ed8eba36a80fe91d3f783a6e6d8fb467d63e546383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8289624fc52a58a88451c69054ca366723d42c930471ef002d7742ecf5b36a52`

```dockerfile
```

-	Layers:
	-	`sha256:5cc86a795a0368deeaaeab977d302c3fc316bb272f31f4b746d27527d6cc0825`  
		Last Modified: Tue, 03 Feb 2026 08:06:15 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12e9edebde42a744649e8a9cbb42272ebbfd02270925992c898955bbbc51225`  
		Last Modified: Tue, 03 Feb 2026 08:06:15 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-alpine` - linux; s390x

```console
$ docker pull golang@sha256:dc0601a3a0df7c311347a2a9bb67886f98a9a2efa1fbf3b198f201d6e4206c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96593108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c47da78328661ff183a40a5c7b20880d74e2876e2250788fb550f50d612935`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:07:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Feb 2026 19:29:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:29:01 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:29:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:29:01 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:29:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:29:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b19da3a82072794d62dde7afbbfd822a592c5dfe5b82c058d3ec326c23cca53`  
		Last Modified: Wed, 28 Jan 2026 03:07:58 GMT  
		Size: 297.2 KB (297176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7062bfc50107a913a5fd7c0d090af1366da08b74147cf71ec4490488730775`  
		Last Modified: Mon, 02 Feb 2026 19:29:23 GMT  
		Size: 92.6 MB (92570442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac69d7edf0460e394ef50874b082a893a820797f552ff91067306772b0c1002d`  
		Last Modified: Mon, 02 Feb 2026 19:29:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:3ed9dea2ebcb0af38d17c22ef6ce3e230d4633093c42a04d0cda223c1ff6d9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 KB (219872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d111ed6abd9b61cf74c186f85c1bdaa3ad84310ddd9d441fb37ffe9c0916f007`

```dockerfile
```

-	Layers:
	-	`sha256:73f4e9ba24ae4c78f159665b299d293f0e235b97af146553e1f20e6c3f91303a`  
		Last Modified: Mon, 02 Feb 2026 19:29:40 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48aa3a2c94e41c6642aedfad1dccf3780ca696b233b50a9c2ff4d4b0601ce688`  
		Last Modified: Mon, 02 Feb 2026 19:29:39 GMT  
		Size: 24.9 KB (24922 bytes)  
		MIME: application/vnd.in-toto+json
