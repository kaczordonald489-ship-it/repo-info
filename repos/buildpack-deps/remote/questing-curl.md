## `buildpack-deps:questing-curl`

```console
$ docker pull buildpack-deps@sha256:941d68c4f786e3b1ae2968ff51e105cbf74c79c6e06bdd42a2b821d5c4ed64a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:questing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5b40931e69ff106d71fadea5926cabbdce38bcd7e8ae160eb9018285fe4395e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53358401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4706dfd661420b8da360e5a43c5b94e461dc834f5d4132c150a8462426dfa34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Dec 2025 06:59:16 GMT
ARG RELEASE
# Wed, 17 Dec 2025 06:59:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Dec 2025 06:59:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Dec 2025 06:59:16 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 17 Dec 2025 06:59:18 GMT
ADD file:3c9ad2247c67ca346f1495dbb4344056bebc791542d36d1ebce89d87dd34cf5a in / 
# Wed, 17 Dec 2025 06:59:19 GMT
CMD ["/bin/bash"]
# Fri, 02 Jan 2026 23:11:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:16c195d4c5e9683ea3bd3e3afc1a4bd00392028211586424d551a9b2f20d6978`  
		Last Modified: Wed, 17 Dec 2025 12:02:21 GMT  
		Size: 34.4 MB (34398943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06f1a682b53d1c6d4a0735aac90e148cdf81808cfa81597a3e80c76257e4db4`  
		Last Modified: Fri, 02 Jan 2026 23:12:06 GMT  
		Size: 19.0 MB (18959458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e39e95491093bbe3e207a7c983c7cfc7805c07ce42139fd4ba50f5f6dde14758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478f9a1bf1c03b45849322a0f6fa77f176d4dfacc4c45fe11399de327c092c55`

```dockerfile
```

-	Layers:
	-	`sha256:f5c29bdc819528a3329369fb64fc30aeafa4ca10b11583a584c1e7e6568eac50`  
		Last Modified: Fri, 02 Jan 2026 23:12:05 GMT  
		Size: 3.0 MB (2963970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a40b5e3f2e0db99599aa45161f7c48354b0d1f96ccfb8b61f00bcc608470685a`  
		Last Modified: Fri, 02 Jan 2026 23:12:05 GMT  
		Size: 6.9 KB (6935 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ab239733b09dc8558023cf8c115c1928b540fdf284bf4b3390a1b05706a4b6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49172398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1b19aa63e28db52533267afb7c0c9ef46cde4c704ee5aaf213d51fc1851f4b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Dec 2025 07:01:56 GMT
ARG RELEASE
# Wed, 17 Dec 2025 07:01:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Dec 2025 07:01:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Dec 2025 07:01:56 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 17 Dec 2025 07:02:00 GMT
ADD file:c83f623082e6ef905d41888c626749887537e060207ac8b3be34f68d4a2f2378 in / 
# Wed, 17 Dec 2025 07:02:00 GMT
CMD ["/bin/bash"]
# Fri, 02 Jan 2026 23:10:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:86605e7f0af274af97c473f49e185f0ab72cde1b9e84f77330df2dae244554c6`  
		Last Modified: Wed, 17 Dec 2025 12:02:36 GMT  
		Size: 31.8 MB (31835257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1295d0d4e354b24cb382d32bb25b18ee9fb2791fcce4ff37e94032d41712e152`  
		Last Modified: Fri, 02 Jan 2026 23:10:58 GMT  
		Size: 17.3 MB (17337141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:efb267eded056ff3cae1516af6b10f0d33e0a7a76512eacc9acedf65878c81f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2972474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf18a30324973d073dac2919db24a5c21ec3bce17b7e15f219bbaf0a51db653c`

```dockerfile
```

-	Layers:
	-	`sha256:33a5baffdb7576e3d82011050334e7ca3d76350e610d333833d6d49e77f900a6`  
		Last Modified: Fri, 02 Jan 2026 23:10:58 GMT  
		Size: 3.0 MB (2965475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e3882f54ec15d97a4421500c2159e483867c89f17366335da5ef546c688ae8f`  
		Last Modified: Fri, 02 Jan 2026 23:10:57 GMT  
		Size: 7.0 KB (6999 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:874b7b8bbc86da98575f70115c774ef16526e5b71d673ad27e898e072d20db67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52494874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c4c6b11f1657e0c1a52ea81b7fa3777dcafc7db2153ed6a347d1482d0cae21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Dec 2025 07:00:53 GMT
ARG RELEASE
# Wed, 17 Dec 2025 07:00:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Dec 2025 07:00:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Dec 2025 07:00:53 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 17 Dec 2025 07:00:55 GMT
ADD file:ce0ed2b1633c632fb10a1612e64252af75b1f5aeb73b4ae5c99aa52229614cc7 in / 
# Wed, 17 Dec 2025 07:00:56 GMT
CMD ["/bin/bash"]
# Sat, 03 Jan 2026 00:02:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:541fbd16e24de6ddea2b3b83a1222babc323c253520a32ce10c104edd3ed55be`  
		Last Modified: Wed, 17 Dec 2025 12:02:29 GMT  
		Size: 34.0 MB (33977137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664dc6d8a8c5821f7e8bf6beaef5f8ea3f3184cd4a76048ef4388651120842c5`  
		Last Modified: Sat, 03 Jan 2026 00:03:06 GMT  
		Size: 18.5 MB (18517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b67b7e5cb4c50b3132a880382465ae440b1be4ba96efbfcfe59155a46b1aaf55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2971243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20706758efea331e442cfb107393beb1aef5dd672b733ea69fdddcf8de61b7b2`

```dockerfile
```

-	Layers:
	-	`sha256:639bc9602be78e8af71e4ff27232ecf5829a56a972b8bd47f9ef7d162133ac50`  
		Last Modified: Sat, 03 Jan 2026 00:03:06 GMT  
		Size: 3.0 MB (2964229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc16de2d6eea807052829bb513673ade07f5d5158f0e5ef70edde2a7b735d11`  
		Last Modified: Sat, 03 Jan 2026 00:03:06 GMT  
		Size: 7.0 KB (7014 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1171f64debcb400e54fc44b3d8896044797e30c4ff7ba76f146a037df70d2a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60558637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b09e61ec0d1f2a61fb2a416c45504ba643361c507b0a737d8d41bab7613105d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Dec 2025 07:01:13 GMT
ARG RELEASE
# Wed, 17 Dec 2025 07:01:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Dec 2025 07:01:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Dec 2025 07:01:13 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 17 Dec 2025 07:01:18 GMT
ADD file:80e51c252850cfc8712206404b1b9c24f10094c17f18f1925c33418780e67cc3 in / 
# Wed, 17 Dec 2025 07:01:18 GMT
CMD ["/bin/bash"]
# Sat, 03 Jan 2026 03:24:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ade432f435a67472df639da16a96659dc7c3849f8d5ede58cf5b95e186dec925`  
		Last Modified: Wed, 17 Dec 2025 12:02:43 GMT  
		Size: 39.6 MB (39596922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce71414238d174b7eed1a6544437609f0c9edabbc444ce584c9f4a94f03835e0`  
		Last Modified: Sat, 03 Jan 2026 03:24:51 GMT  
		Size: 21.0 MB (20961715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2528b3584a7ebbe69277920093cdae5ce88f5e2ffa7971973f991549ce69d3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b11a42a06b5ee2904c31367ea585e749d8879349e4d2138319e64026be08090`

```dockerfile
```

-	Layers:
	-	`sha256:d199128ed73d2f0ed7f50d29ca7146339a610304ae566cfd6e6f6206731b092d`  
		Last Modified: Sat, 03 Jan 2026 03:24:50 GMT  
		Size: 3.0 MB (2967798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0e865c5108c2eb5d9262e71a9795f5be925ef3c9a584caa13e6def3dd927ac7`  
		Last Modified: Sat, 03 Jan 2026 03:24:50 GMT  
		Size: 7.0 KB (6967 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:91135d77368d581677ba87ce9fdd87aae94af8f167349c747c779eb5db20c901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55076012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759eee2e9627e9b30e154432810694a3742211049b453e7708a5d22de5f7ced5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Dec 2025 07:00:12 GMT
ARG RELEASE
# Wed, 17 Dec 2025 07:00:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Dec 2025 07:00:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Dec 2025 07:00:12 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 17 Dec 2025 07:00:14 GMT
ADD file:730b8ac9cb4f3bfd36411b840b2d63e882b37e8ad20a45f3a02b3e6c861c8e31 in / 
# Wed, 17 Dec 2025 07:00:14 GMT
CMD ["/bin/bash"]
# Fri, 02 Jan 2026 23:11:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8e1aa813c1657f48b7291cc09d13191de87f8108febddf3d8484783665856c5e`  
		Last Modified: Wed, 17 Dec 2025 12:02:57 GMT  
		Size: 34.1 MB (34098575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3649778224895380b989840d5456da4cef6185e70ed1b3ef42d9544a1b97a41`  
		Last Modified: Fri, 02 Jan 2026 23:11:26 GMT  
		Size: 21.0 MB (20977437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:be867c197ec3694349f0361f5447fcc8c375bb8bc5bee1ff65793b01257efd40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2972935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd7c5b8321c25d604a6161caf5a05286815ca47e6fff30c25f75aa97a346b8c`

```dockerfile
```

-	Layers:
	-	`sha256:df03c9528ce8a57dfb76fc2f505e162d8c8725d662b7a4921a5a67eabc14a74d`  
		Last Modified: Fri, 02 Jan 2026 23:11:26 GMT  
		Size: 3.0 MB (2966000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c646a4ee0c25ca72c2aad81c32e49beca05d387cf215c7800c0cae04542236`  
		Last Modified: Fri, 02 Jan 2026 23:11:26 GMT  
		Size: 6.9 KB (6935 bytes)  
		MIME: application/vnd.in-toto+json
