## `sapmachine:25-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:3fcba0f4e29d266e3f8e29ea62dfc313a8852f8c7a43d942ff9f0c29149b7296
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:7070b4d975f6a27948009fbe6dd182118d9753496dc55251696927b88e9b0e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (250005284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1779713abef6a0c59bf6a1c526aae6a6f7970c7259fbebf8ecc1108ed578756e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 20:02:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:02:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 20:02:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2f8c164b32c76b3f0f14474820a85eeb99459dd84068e86d49782e9f58006b`  
		Last Modified: Wed, 21 Jan 2026 20:03:04 GMT  
		Size: 220.3 MB (220279273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0a5246890335f16fc1252abd0cdfb5b0a5fdcd94f732b5c0df99942ea491b659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2363164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc39201322b781a800d7b41719f45c87369031a1235247d80e7db9e24151494a`

```dockerfile
```

-	Layers:
	-	`sha256:1b6de354f9403a48d4bf5f6a974d742027869705496020a5448555f9a2c57b46`  
		Last Modified: Wed, 21 Jan 2026 20:03:00 GMT  
		Size: 2.4 MB (2350561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af357d83f2fefa63d5aeb1219db005bbcc5c1c7e807d56d401e2dcb9710f974`  
		Last Modified: Wed, 21 Jan 2026 20:03:00 GMT  
		Size: 12.6 KB (12603 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ed99c2097197e8c661ccee46377a6c8518388def5da5c618ae8f09ae88c0ecfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246928625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b938ec37e260d100a71205f88556396c68144b703048f67892adfa9b40ceb32`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 20:08:40 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:08:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 20:08:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04432412fd380b3fe5e6646dfa400736846602c2da995f0dc0134d8e4783079d`  
		Last Modified: Wed, 21 Jan 2026 20:09:44 GMT  
		Size: 218.1 MB (218064801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b65a3062022ddfdbe80a91dd8247991ec07f71cc1d79707882459fda33d54798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2363988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dce5d4d3594337672535f510e0f85b3c800af672d485d2f7e915f05ab221781`

```dockerfile
```

-	Layers:
	-	`sha256:c6b425936e92c0592f878ecd4b51c98d550d7b9b592e6c2711151732c5535659`  
		Last Modified: Wed, 21 Jan 2026 20:09:00 GMT  
		Size: 2.4 MB (2351149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c0de27a2815fc75ebf3daac50c121f0b85746f10ff994d72cadba521cf739d8`  
		Last Modified: Wed, 21 Jan 2026 20:08:59 GMT  
		Size: 12.8 KB (12839 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:298f83a56e951ffae5d85a67b7b4596ab1a2031f5a12c556930da6982f35b36b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255294355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b49fc5fd0ec7d0d8751abf98d95c5607a1a74d7b42a81444f83b4e20e60115c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 21:08:43 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:08:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 21:08:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0ec3be54a11029b9cfddec7d65cf9ec84e2da7b532d5dfe31016fd8ff4b40a`  
		Last Modified: Wed, 21 Jan 2026 21:09:40 GMT  
		Size: 221.0 MB (220988196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d8d70cc3a11b3fb5e5ad9ebdf87df4ea3b038da27d3d188f04fab2829b8ca048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810291fca64177265aed2cf785a4a0db268ef65d24a5f0721b9edcdff28dc1f3`

```dockerfile
```

-	Layers:
	-	`sha256:6367a6fb0c3e78d53247075c9e7f3a5c8356d7366cb1063e18e1ec73ef1826f9`  
		Last Modified: Wed, 21 Jan 2026 21:09:34 GMT  
		Size: 2.3 MB (2347456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:743f61189cc7001802469f5b05585f3f7d698185f1575d3b30956e85ef74be91`  
		Last Modified: Wed, 21 Jan 2026 21:09:34 GMT  
		Size: 12.7 KB (12713 bytes)  
		MIME: application/vnd.in-toto+json
