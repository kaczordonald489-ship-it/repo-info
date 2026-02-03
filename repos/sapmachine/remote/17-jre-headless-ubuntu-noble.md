## `sapmachine:17-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:5e627ee54851956ab5f54a14b3c94840db4e067052683bd517af98642db6f561
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:64440fcc8b9b084f04978959dd7448b244011e5b61e3300f99fcc9df6d683730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83308558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed523ac134050ab72567285ca6bec33e66b100ddced249f4776d9d9c3f897a4b`
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
# Wed, 21 Jan 2026 20:04:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:04:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:04:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c364fbfd0d9f0d730600db6f19efb4a7956b4e4e7d31dc71d8b4f6dc64a5c5`  
		Last Modified: Wed, 21 Jan 2026 20:04:46 GMT  
		Size: 53.6 MB (53582547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:23c840c1025dcf37f59641ab0cf0c2e591f7c293f545691630a8882bd460d410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2284168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64be4b1d94eb311cfd7ca7d920f05c01fab1ad496e6dabc45f195a6975a55985`

```dockerfile
```

-	Layers:
	-	`sha256:b14068f620c20658f4b7f0d858745ce207eba11f8692cc218f256e42387de136`  
		Last Modified: Wed, 21 Jan 2026 20:04:44 GMT  
		Size: 2.3 MB (2273940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12df753923df8c9e5d733df08b2f3480a69f9fb3e4e4e169bf641888b4b932c0`  
		Last Modified: Wed, 21 Jan 2026 20:04:44 GMT  
		Size: 10.2 KB (10228 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a3c9f2867ce907efd24020c5940332d460f740e865350f3cdf51f18fc111740a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81868310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e634ed458ff27765138740f32553b97ede65fc60279813fd7f8497621105dee1`
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
# Wed, 21 Jan 2026 20:10:18 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:10:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:10:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337d4c68cd7c5d30883348fc3798ecce68d5119fa2b2bdc7e606fddab57ae591`  
		Last Modified: Wed, 21 Jan 2026 20:10:30 GMT  
		Size: 53.0 MB (53004486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:564774b763882f2514f790c76d5a30b5f01802006613bb4bfd07f8a06b90361b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2284827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ade356cfa2df3a6247464ba7d3a7d5c410458f5d5d2d4d5fd177d5dc0d7088`

```dockerfile
```

-	Layers:
	-	`sha256:f5e58f3addd51b43420b63afa773eb17b419634d3bf7fb29995b4ba5dfebd12d`  
		Last Modified: Wed, 21 Jan 2026 20:10:29 GMT  
		Size: 2.3 MB (2274447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57777ead853eda1aee5d16cf744b5781dbae670e1b435b79597133cc8a018299`  
		Last Modified: Wed, 21 Jan 2026 20:10:29 GMT  
		Size: 10.4 KB (10380 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d7e34b3ad4ef3cbaa5ad51c982719170321fc54a127145c6d27316d8c2b94ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88988780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77950130a64492d7eb58508f47c6de741b64d3bb96a40b14973dd40deb2fd3c6`
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
# Wed, 21 Jan 2026 21:29:51 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:29:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 21:29:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb77fd1ef0e731fdc736e3172c610e82ebefb20e0334493090332363fd9a73b`  
		Last Modified: Wed, 21 Jan 2026 21:30:22 GMT  
		Size: 54.7 MB (54682621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0c0371724b2b08e4d990ebf8a4dfd60bbbfb2323b83d6aa4db9163fa3e27b075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e97d9e54495ae429f1c46ad61c4686166d00b167576665561a2f093777dc5f1`

```dockerfile
```

-	Layers:
	-	`sha256:06eb03b24f5b8f5755c62f4bb2afea35397e488343a6944b247a9743fca23896`  
		Last Modified: Wed, 21 Jan 2026 21:30:20 GMT  
		Size: 2.3 MB (2273357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6966228b12c5d37073b09acb7c813ef738eebd5dfd8967c2b3738d5490c59047`  
		Last Modified: Wed, 21 Jan 2026 21:30:20 GMT  
		Size: 10.3 KB (10297 bytes)  
		MIME: application/vnd.in-toto+json
