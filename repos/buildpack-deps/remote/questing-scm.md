## `buildpack-deps:questing-scm`

```console
$ docker pull buildpack-deps@sha256:46ada0756c58b507caba9675efd61a5f166d66d6fb2ccc8117164f006256bb20
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

### `buildpack-deps:questing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e6fe1f299934f79ebc9554d9181ea143a4dfb5244a3e5c3cc75beacada1637af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101440319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137b3e4b6885968c6d217ecbf9660ceee00c7a3bbeedb48d44fbef9afd7e0a17`
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
# Fri, 02 Jan 2026 23:59:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:339df752a36c7658bd49a504949a2d8bc6cfe2a54b5abeaf5bbd68260e35668d`  
		Last Modified: Fri, 02 Jan 2026 23:59:22 GMT  
		Size: 48.1 MB (48081918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a72140e371a570d1db79c48f8c3f437e9c9fdca533a82c2f82574359b218c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5775400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4898ca50c162c4db9b8a009bf74fe997650c4e2f29540dcdbb849d780e637b06`

```dockerfile
```

-	Layers:
	-	`sha256:94f105bdea4c7e43cbc37cbdd7c43073624a168588a9e0873559101b9265a18c`  
		Last Modified: Fri, 02 Jan 2026 23:59:21 GMT  
		Size: 5.8 MB (5768119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37496cc952b24e06f1077208486ecf39fef5fb09b678a674b0f1a5b37dbc6438`  
		Last Modified: Fri, 02 Jan 2026 23:59:20 GMT  
		Size: 7.3 KB (7281 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3ee7b3769fe8da3fa50005d54deacaddebb90a389f40e93f49e4827c0c803ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99750762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c0a6f300e9888734e68aefc5e86656165184c6e366e6d2bf204a52daa6c100`
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
# Sat, 03 Jan 2026 00:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:eae84d2db8c69686c175c095f00380c344b5b7fa343ac6a1ac4f78024f1e4bd3`  
		Last Modified: Sat, 03 Jan 2026 00:15:28 GMT  
		Size: 50.6 MB (50578364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bccebb8f93330b1e1cbda54f6a319c372cd05ebf1ffdd0a8373e1960a5a6666c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5775963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf39eaebc70170aaa86db609cfb91334820e0a9554307550a1f55ebef6e938f8`

```dockerfile
```

-	Layers:
	-	`sha256:482dbba09d1653ca57ac90af6d28d40e14d2e720d9d37b14d9a8f4bca2d2b13f`  
		Last Modified: Sat, 03 Jan 2026 00:15:27 GMT  
		Size: 5.8 MB (5768618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5618d6ff6a4526ebb9117db9d0715ab9b8f3d88bdd253fe8df31742ebcd14a13`  
		Last Modified: Sat, 03 Jan 2026 00:15:26 GMT  
		Size: 7.3 KB (7345 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6a7fff11fde8c2150b26b891a16e39ae14ae5ab7e639beb07dcad4ccae6f1837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100238396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5c504381ceef1f3f6d21425bed67e0f0ec9168f222eccc1663dfda3e4ce77e`
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
# Sat, 03 Jan 2026 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:6a7cc1ad17a7f679dca34acdbbc77064b8f3c32b20c018d9204f1d8d65bfb5bd`  
		Last Modified: Sat, 03 Jan 2026 00:12:08 GMT  
		Size: 47.7 MB (47743522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e6b7e8e50514243ae6cd11edae6da0de31aa15e03662beac1962052a846932b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5781868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586bb5cc56009f0c9b905e80f66edebf85c2051234e36867250d2d399455ac0f`

```dockerfile
```

-	Layers:
	-	`sha256:dd2c69d552123ab9f76dadf9a26df6a3938a2bef6a2d21656bfd45b9113c9d72`  
		Last Modified: Sat, 03 Jan 2026 00:12:07 GMT  
		Size: 5.8 MB (5774507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:347d279e26b07a2371af0f05397ce3e90c6db0ecc31ae1d1329ea3b153803399`  
		Last Modified: Sat, 03 Jan 2026 00:12:06 GMT  
		Size: 7.4 KB (7361 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5e115ad43471da16d13ce2fc29437e70292982be3f09e8dc0f2823639f1a7195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 MB (114114571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4d8acfab1d2e9a0c19507f2834eba13c6026cde1bd36259c798480c231df2f`
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
# Sat, 03 Jan 2026 04:10:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:7f7e65121f0a6548b5fdd015ace0c6df36c83802207d4364d814251d24dc0f62`  
		Last Modified: Sat, 03 Jan 2026 04:11:05 GMT  
		Size: 53.6 MB (53555934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d722681a991da1367a96f240768aefc32f85ee1387f4626d525da6131b5fedb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5782495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8536691e805da046900ff25b1d397f3dff1af1b2332e034f8915b62ae119ab6`

```dockerfile
```

-	Layers:
	-	`sha256:5c034bd891a208fd08294951797e04bc4a162ff2998745a3ab3be2cb86b95f9b`  
		Last Modified: Sat, 03 Jan 2026 04:11:04 GMT  
		Size: 5.8 MB (5775182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd0ab1f30306cf83864d647b0827f441399c3a25da36ce6c1a06801bcba5444`  
		Last Modified: Sat, 03 Jan 2026 04:11:03 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:61da1fdbe2951ae8ee373d02fe903c19d7e08874e0972d844101884d5fc1291d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104044386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19fbfce21215d3026e66181f1f9da99be69d0e9d816321ecbd5a1bc86119c2fd`
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
# Sat, 03 Jan 2026 00:35:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:cce434fbbf6c750ddd674ac232ed482a18a2ad1dd800ccb988ae5a3f66709ad1`  
		Last Modified: Sat, 03 Jan 2026 00:35:34 GMT  
		Size: 49.0 MB (48968374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:75609e148c8c06c5cfc90d07daa642d866fa6722fdcef514feee0d9d3e3afc3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396a707dcddcb79bff9e43be4d9f998ef828e5c293cb70826ce3ce6a27810077`

```dockerfile
```

-	Layers:
	-	`sha256:8d791b3a38b067ba5312da65550307f02d2478c27266e4c8c1998cd7f7ea42f6`  
		Last Modified: Sat, 03 Jan 2026 00:35:33 GMT  
		Size: 5.8 MB (5769656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37594993f9bfa93b80250df50ab8662dc09cfe74cdcb7c3149653e6cb493de6b`  
		Last Modified: Sat, 03 Jan 2026 00:35:33 GMT  
		Size: 7.3 KB (7280 bytes)  
		MIME: application/vnd.in-toto+json
