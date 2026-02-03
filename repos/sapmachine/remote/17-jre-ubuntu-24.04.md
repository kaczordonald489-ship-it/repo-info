## `sapmachine:17-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:ac7173c1efe6c8791b92c2e188f1c3a937a900866d1c276ad2f193763c7eb1fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:3232ea7dcb6bb92405b6a6477847a5e7a451650b300426634a6f5cd85c3cf251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84491242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3758b5d3e7503f2f5923da425b7e426cfc7ec723f971c03bf51f55efc8a6f88`
-	Default Command: `["bash"]`

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
# Wed, 21 Jan 2026 20:04:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:04:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:04:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1199fb66e8df6430938b020875c01a9049b85eaec7184d0cd8d12cae6298061`  
		Last Modified: Wed, 21 Jan 2026 20:06:01 GMT  
		Size: 54.8 MB (54765231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fe87f410caa3dfd08ee1e7f6a606a349a1dec3fe001d4d3bf7944e3858c53693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2529808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad4b1dc5af87689e16663186b7ea1a8e14cfd79f71e9482373c85af32ecb39b`

```dockerfile
```

-	Layers:
	-	`sha256:dab9e50e26f44533c73a3e231339a49740c38b05c2dfae835cfa5051ed23ce4b`  
		Last Modified: Wed, 21 Jan 2026 20:04:51 GMT  
		Size: 2.5 MB (2519762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92bce2d9ac0a4fad21dff6a3351be8b1d7e81dd22a28280359c75a0480542a7a`  
		Last Modified: Wed, 21 Jan 2026 20:04:49 GMT  
		Size: 10.0 KB (10046 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:215bb25c5c8e214d14b959244a477bd222cfb63ab2ab0192c11d4a368ab81078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83061782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5095f42034065065d7b10f322af5b3b36c4fd9eb93cbcb19661358f155cf21c0`
-	Default Command: `["bash"]`

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
# Wed, 21 Jan 2026 20:10:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:10:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:10:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6dfa858f099da3b1a960f39ebd827add1b37a158499fccc727207ce34a2d6d`  
		Last Modified: Wed, 21 Jan 2026 20:10:32 GMT  
		Size: 54.2 MB (54197958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:50f07a1c2d6d5068b998e345f3eae68afc82208bcbc4e83d841d14157ee16ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab06940c3cbf04c65de80cf8c80ad3271655ab4211b9a18797efe2eab2a4c6a`

```dockerfile
```

-	Layers:
	-	`sha256:3ab5decd171f87507035c5ebeda59a11b4b8bca97d7cdfbc185cca6e132dbf0b`  
		Last Modified: Wed, 21 Jan 2026 20:10:31 GMT  
		Size: 2.5 MB (2520278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba9f2ac02258ef8d6036be733fe6bedddbf8eaef8641e35b66f95498bdfe7a5a`  
		Last Modified: Wed, 21 Jan 2026 20:10:31 GMT  
		Size: 10.2 KB (10198 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:526a092ca8a2b97a83bef660a1f90a1a677a81b37ab45edc1aa9bcd7b11de7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.4 MB (90363561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5cbfd809921232d492c8a34b0dac68be5ba067e84f90f37c797d729a6b2939`
-	Default Command: `["bash"]`

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
# Wed, 21 Jan 2026 21:29:55 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:29:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 21:29:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c8ac04ef801ae143d62624b1769318646f872e7cbd7fe98143c318d4ececb3`  
		Last Modified: Wed, 21 Jan 2026 21:30:25 GMT  
		Size: 56.1 MB (56057402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0c1a900cb8d02f5688ff618ccba6d338f235a3460c58c837cac1727cb3176e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2529374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a510f00635c03b1eb737de4e3ccb2e19ccf13ccfba7ce11f2d7b52abe36404f`

```dockerfile
```

-	Layers:
	-	`sha256:387db5ab0d4a1fe35a3887f80a04184f138ed2ca5283f4bf44a0a12b054f1d96`  
		Last Modified: Wed, 21 Jan 2026 21:30:24 GMT  
		Size: 2.5 MB (2519260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9912e8a7f167a6dca3f702c25beb274bdf48446d731337685bb18f734bdcabc0`  
		Last Modified: Wed, 21 Jan 2026 21:30:23 GMT  
		Size: 10.1 KB (10114 bytes)  
		MIME: application/vnd.in-toto+json
