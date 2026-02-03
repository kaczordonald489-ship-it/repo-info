## `sapmachine:17-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:83f73c941ea1cab8e0f069c0ec9089286a10600aca1751946cf6a5cf85150e43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:061ec343b3b042dfdb27fef46a5b704cd31458faa146d6a45e88b5076f6a1680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230233719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314af09588349a6b491c8bc5346ed6dcc1c79ee1fa784ba6bab3f33370faa656`
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
# Wed, 21 Jan 2026 20:04:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:04:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:04:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a999314ff55852a604b28cbd1ed153cbefd3a06e15f787c5af178b562e80c8`  
		Last Modified: Wed, 21 Jan 2026 20:04:42 GMT  
		Size: 200.5 MB (200507708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dedbf98201133fd003dd34cb8dfccbd361fa220101f321f0b69751919171dd62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58978b81e42092f1b74c4ccbe38fdcd2dc6153c436fdfa4753b9e9955e4f88f`

```dockerfile
```

-	Layers:
	-	`sha256:14b97e576ffeb5dc4c5582e9e50af4bcf32c2cf2f0a0a91837c5f0026b13c478`  
		Last Modified: Wed, 21 Jan 2026 20:04:37 GMT  
		Size: 2.4 MB (2356848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbd16c2c8a5787698bdedc42ef8a6a9467fe710127196c96306ffbe7548195d7`  
		Last Modified: Wed, 21 Jan 2026 20:04:37 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a2faf1244a6dac3deb7ac7fbf9068ca13f88976e4b8af1366cf79a9edd5b5fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 MB (228089321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2448be2c73bb2022c65f5c894783c0c5684fa5e57d2c811e7e2678306396cff8`
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
# Wed, 21 Jan 2026 20:10:24 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:10:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:10:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcff709154741083bdf1ff7edc52e24513c4211694e2532a43a2dae26a4f73a`  
		Last Modified: Wed, 21 Jan 2026 20:10:47 GMT  
		Size: 199.2 MB (199225497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8f452e1d4b87deef397e1c1565af0a76cca3143e90f2e69e95e72e4bd4d99866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e3943a559f78f159a05ee572d3ff39372eba710a30fdf835307622e90d575d`

```dockerfile
```

-	Layers:
	-	`sha256:ff88acb799927cb46b987311643429bf06ef4d122724909c752d0c8a1cd5f8ef`  
		Last Modified: Wed, 21 Jan 2026 20:10:43 GMT  
		Size: 2.4 MB (2357355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91df9adfca01f2f53f9eead840f08f7c321a3d56523a520ed63a3442b3e43e6d`  
		Last Modified: Wed, 21 Jan 2026 20:10:42 GMT  
		Size: 10.4 KB (10386 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:23a701024aa6b43e68614cedd34622d13704b705800edf93065f3010659b4078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235501231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc2e969e572974377b66b602566597c63b30570d4b0d238125ec2cea8dad528`
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
# Wed, 21 Jan 2026 21:27:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:27:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 21:27:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6d3a3e5e5f2410b5925b5091044afa922b99c72a863566e3211fa0071e5f61`  
		Last Modified: Wed, 21 Jan 2026 21:28:42 GMT  
		Size: 201.2 MB (201195072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:699c307385996203621e8b18120c5d3c2542d4fc0a3ce5754b3d76aa4cd0fc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1a723d53e4812e46cb824c8abd22bf5d94d1864408a93ceac18f172aa70d31`

```dockerfile
```

-	Layers:
	-	`sha256:ef23ec1dafbb564e858600648587237c46792d0d116e011f69e316ca68445c44`  
		Last Modified: Wed, 21 Jan 2026 21:28:37 GMT  
		Size: 2.4 MB (2354319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10a855c751dda8181dd15631b3bc0529a86e624b2881f7ecb34dc12cd6eaab`  
		Last Modified: Wed, 21 Jan 2026 21:28:37 GMT  
		Size: 10.3 KB (10302 bytes)  
		MIME: application/vnd.in-toto+json
