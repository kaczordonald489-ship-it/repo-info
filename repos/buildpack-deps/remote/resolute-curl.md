## `buildpack-deps:resolute-curl`

```console
$ docker pull buildpack-deps@sha256:4371f97be1ae79a0bb71a31bf25a57ace12a76829303ff463093490df59ea074
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

### `buildpack-deps:resolute-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2c3222d18c4f721218ad16265ca2998336b4017f6f0ac13169e4bf4f494ce475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53214077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8af99a41fdb60c263b3c073a5d1928a961f3f5ce3e8105aebf582cea6053bb5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 06 Jan 2026 16:11:45 GMT
ARG RELEASE
# Tue, 06 Jan 2026 16:11:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Jan 2026 16:11:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Jan 2026 16:11:45 GMT
LABEL org.opencontainers.image.version=26.04
# Tue, 06 Jan 2026 16:11:47 GMT
ADD file:3beef3c47f24f3196246a7dbc25d20ba42394f35ed72b8ba8b86c3d4d13a83f2 in / 
# Tue, 06 Jan 2026 16:11:47 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f784408d7713470603ec446172f85c9a5ae57032b804583cc37631eb6bb6b75c`  
		Last Modified: Tue, 06 Jan 2026 17:09:06 GMT  
		Size: 33.7 MB (33726347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2773b72b93134db036b076a720d2feda581b3d29f4f2c5877e3beb834e1bf3`  
		Last Modified: Thu, 15 Jan 2026 22:11:06 GMT  
		Size: 19.5 MB (19487730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:95bcb51ca595f441f9f29fc5eb748ef3a21d3b8e20d798ffd83ec137a576674d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fe10777520f37afe6a27e292af9b70035f9bcb380c5552474429c393320e13`

```dockerfile
```

-	Layers:
	-	`sha256:181c9578da36b5e9b52f3bb1d48bbfde7017d55934183b254da57bf716051b48`  
		Last Modified: Thu, 15 Jan 2026 22:11:06 GMT  
		Size: 3.0 MB (2950039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9b808a587fd620e027b8e94bb07572297444feaefc3c2fec49504204df78c9`  
		Last Modified: Thu, 15 Jan 2026 22:11:06 GMT  
		Size: 6.9 KB (6935 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:57c99cfdd33ba2bf0d3be843ac28f942748a1f451acd8729069f7c7eb5461f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48946431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93053de3ed22af5408ca739bf7ed3f9e85964cedea3a23a142268a75fb079f86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 06 Jan 2026 16:12:47 GMT
ARG RELEASE
# Tue, 06 Jan 2026 16:12:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Jan 2026 16:12:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Jan 2026 16:12:47 GMT
LABEL org.opencontainers.image.version=26.04
# Tue, 06 Jan 2026 16:12:52 GMT
ADD file:2badcd83b204d640ccedc4ace52673007514f420a84bd8c139cdf292ab0fd3e4 in / 
# Tue, 06 Jan 2026 16:12:53 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a9ee0a3989db9dc297303b58491eba6d69952baa6b2827fc54ee64ce18e07032`  
		Last Modified: Tue, 06 Jan 2026 17:09:22 GMT  
		Size: 31.2 MB (31161903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afba882eabc4fb690fa94f15129818fcf2958502ce348f72e1f4978f4fb0a975`  
		Last Modified: Thu, 15 Jan 2026 22:07:55 GMT  
		Size: 17.8 MB (17784528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0aa87ca920c9b86517f68738197e9d61f15bfdecf2d065ddecbbd2b8501dcf41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e6c0c7853c540861bfe949574a9fcddaa95942272ed4eab734dbd1b44f406d`

```dockerfile
```

-	Layers:
	-	`sha256:cbf3a8af9457b696417a2e641c65fe6c591ce5426e62bd1f015904b11401f77b`  
		Last Modified: Thu, 15 Jan 2026 22:07:55 GMT  
		Size: 3.0 MB (2951541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e194ec1babfc0e1968d794b15b5e9ba67be9f418d6751300f853cde1b0908dd`  
		Last Modified: Thu, 15 Jan 2026 22:07:55 GMT  
		Size: 7.0 KB (6999 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:daf53a97905f4bc3552816ffe65dd90bdac1691fbde79427e1c1a8d33fce047d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52301825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac935c1bf3e1a4196c1ac57fa8aa564bbfac30b977a9ebcb247314192125866`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 06 Jan 2026 16:13:27 GMT
ARG RELEASE
# Tue, 06 Jan 2026 16:13:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Jan 2026 16:13:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Jan 2026 16:13:27 GMT
LABEL org.opencontainers.image.version=26.04
# Tue, 06 Jan 2026 16:13:30 GMT
ADD file:0380efe36c0196e2c2ade7e5f2cca6433adfd8d1710d937744979e52eda4b70a in / 
# Tue, 06 Jan 2026 16:13:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e2404e3282be0ee5ef4dc11f1068759836b240597e5a2df39be9b0eb4f3aba04`  
		Last Modified: Tue, 06 Jan 2026 17:09:14 GMT  
		Size: 33.3 MB (33273501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bb422c70ec76440334ab3551c565c88bff89c2dddb0e89e2997bda52f8846f`  
		Last Modified: Thu, 15 Jan 2026 22:10:43 GMT  
		Size: 19.0 MB (19028324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d6eecd2d1b67ca66822c0c25c11c96514b9674a92c9dfe11b0f82327401c205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09753c980f081bb49030b8f08b73ac8947a0a3c4efeaa06d98990bfb45297e92`

```dockerfile
```

-	Layers:
	-	`sha256:3df9a3c3472a2a36cdf3a71174aac93d4bd22897c1a50dd741deab84f3208022`  
		Last Modified: Thu, 15 Jan 2026 22:10:43 GMT  
		Size: 3.0 MB (2950297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa1029ad484acd17953fe48aea6e494ceaf4357c2f5241b612e2737bca305c23`  
		Last Modified: Thu, 15 Jan 2026 22:10:43 GMT  
		Size: 7.0 KB (7015 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4eaf46c8032707758ddd954badde545b1f151eb531893672c81206c74199a8c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60743404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ec64093d0d4cdbcfbfdd6b032ca7fa444cbb4a03d50134a115ebdd7c72bdb0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 06 Jan 2026 16:14:48 GMT
ARG RELEASE
# Tue, 06 Jan 2026 16:14:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Jan 2026 16:14:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Jan 2026 16:14:48 GMT
LABEL org.opencontainers.image.version=26.04
# Tue, 06 Jan 2026 16:14:52 GMT
ADD file:7ec9d39d1fd01988d51557953b0733de4e61b4fa324869a68521dfd338f7718e in / 
# Tue, 06 Jan 2026 16:14:52 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8dc6edd0e713b64ebd7f5a4fb903e2ab2bc713a37543e118356f779bec06e387`  
		Last Modified: Tue, 06 Jan 2026 17:09:30 GMT  
		Size: 38.8 MB (38811703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2a9a9613d4b4de22dc7933a7a061b9dc4f14dce73e75f090032381eac28b4f`  
		Last Modified: Thu, 15 Jan 2026 22:09:25 GMT  
		Size: 21.9 MB (21931701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:be0067944a5163a284ca1613d8faaf156da8d117356abe087c48858a05986d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c11be94426a8f81acebb3611b81b6513228b34ae6a5e05dcf452a9208be593b`

```dockerfile
```

-	Layers:
	-	`sha256:4db5ec51d0737447bea1609a1048a8129669c6f99f794e303d56a16a6ddde1d9`  
		Last Modified: Thu, 15 Jan 2026 22:09:25 GMT  
		Size: 3.0 MB (2953862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b8293253fc564a99432dc1bc4279b6c7df7337beab3b56985440b1da319d09`  
		Last Modified: Thu, 15 Jan 2026 22:09:24 GMT  
		Size: 7.0 KB (6967 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:154b30f26817b77ae8556ba86593b50443d80ee436d13d5d3facac561e3239f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53345602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92922d6f97ddd9db1f2b1d1936fe41c786d951bafad0455ef7dad90e93d0cbfe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 06 Jan 2026 16:12:54 GMT
ARG RELEASE
# Tue, 06 Jan 2026 16:12:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Jan 2026 16:12:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Jan 2026 16:12:54 GMT
LABEL org.opencontainers.image.version=26.04
# Tue, 06 Jan 2026 16:12:55 GMT
ADD file:9266e4011fb5ad8a3df9e390fc8165ed1fd44560192a8470907993912a77df90 in / 
# Tue, 06 Jan 2026 16:12:55 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f779d014bea281c13f5bd15e791164db36f27117b06bcc6a0832c49e20ca6c3f`  
		Last Modified: Tue, 06 Jan 2026 17:09:45 GMT  
		Size: 33.4 MB (33397954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66829f85ee6a4ac10cb285e12e8d836204a87759cfb752c0e2b65010651a3b0f`  
		Last Modified: Thu, 15 Jan 2026 22:06:38 GMT  
		Size: 19.9 MB (19947648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1e59cee56eb813deab44aa1d22ab2546353db466b10714d6620b6932ccc37eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc4d0d8513434ec8539c8bbdb1e77b38d63425593747eb79388a20ef5ff24a6`

```dockerfile
```

-	Layers:
	-	`sha256:84774458344d397d021ef93c2e0149d76623ff2bd56a7a9ffbb9a099d4d22175`  
		Last Modified: Thu, 15 Jan 2026 22:06:38 GMT  
		Size: 3.0 MB (2952070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:585324765f956afc20f524cd8c83adb39117898c061d8b3a00241f751be69600`  
		Last Modified: Thu, 15 Jan 2026 22:06:38 GMT  
		Size: 6.9 KB (6935 bytes)  
		MIME: application/vnd.in-toto+json
