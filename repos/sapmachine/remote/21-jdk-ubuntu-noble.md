## `sapmachine:21-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:de13424fa7c25204975ee23302248362112f29433e487f01587ea862582e4b14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:2e6ed654d9509687d92910d44c57c1b6fb4588cf5099c672498e5a7dd6dc8423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246106403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd1e9599384aa32fe590fa91b780116119d256108b4a93dfac09448ca7714fd`
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
# Wed, 21 Jan 2026 20:03:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:03:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 21 Jan 2026 20:03:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231628878931cb2e916a9a678eb219b283e31fcf07667b01271007b0ac0f8193`  
		Last Modified: Wed, 21 Jan 2026 20:03:59 GMT  
		Size: 216.4 MB (216380392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2ccb89f99852936701d24f880873fdfa8710b55ac86e854bd8148ef6033dd89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2619704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08807238eff1911ab85afb1be490fb8d555304c814b599d546b8b9eee5e8e354`

```dockerfile
```

-	Layers:
	-	`sha256:02c06499251050c94193ba23e24c0c0a4d7274a5e982af10b2488a90e0c1bc3e`  
		Last Modified: Wed, 21 Jan 2026 20:03:55 GMT  
		Size: 2.6 MB (2607097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:645fce9ab1d9e808f6a0060a5a2bb26bb566ee0a7370942d00e23d0cebf88926`  
		Last Modified: Wed, 21 Jan 2026 20:03:54 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:224d171e69f2f7ce805c83877e75b1c26fb47811fe154966678fae09f65984ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243500894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e61ede3559719293276d6cb88ee144195376a2f7f6b0a5db8977a2d35f69d6d`
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
# Wed, 21 Jan 2026 20:08:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:08:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 21 Jan 2026 20:08:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17aed308a18be2682cf6747a9bb1dd7d30e1cc7149e7d58d69df0423dbd2bdae`  
		Last Modified: Wed, 21 Jan 2026 20:09:37 GMT  
		Size: 214.6 MB (214637070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c1839396a4ac263667f72e60d12b5a2e64a414f425d99e9f9f5d7fef9a0b897b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2620563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9094e51bea6bb49902c51a857eaebc270933be48553f93c7b207279bc5d318`

```dockerfile
```

-	Layers:
	-	`sha256:561ed60f09dcf194df9c97e69fb72fae1bef25323f9d6b2be759d03b22ded63b`  
		Last Modified: Wed, 21 Jan 2026 20:09:04 GMT  
		Size: 2.6 MB (2607709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c569ee751a84b52cfdec751351be2d43bbc5554d0a709bd86dace18653f5a4`  
		Last Modified: Wed, 21 Jan 2026 20:09:04 GMT  
		Size: 12.9 KB (12854 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c32dc5be44e8babc5dc3396de69e471fe5ea020e69e980b456eecc0950238a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251727367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d36f80ddb5c883c6956e70f79f75a01011fd6470e3691e870bb1ed7faa162a`
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
# Wed, 21 Jan 2026 21:19:10 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:19:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 21 Jan 2026 21:19:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a634db121cb7f6686c4bcd6d6270267ca72f83f4fd8798790d329df147ca0630`  
		Last Modified: Wed, 21 Jan 2026 21:20:07 GMT  
		Size: 217.4 MB (217421208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5ef5ca807bf4b11573890d2a11bef1e4f56d52c8473254e233d5794366a7ea76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb29881bb4383619db2ed9f575ff9f5d523d3fd6eb04b85178cbc958ad71e21`

```dockerfile
```

-	Layers:
	-	`sha256:d2bebac82d5b905a6950f15d57ebc656bedc6dcd2a7d7130771b5e7c957aef27`  
		Last Modified: Wed, 21 Jan 2026 21:20:00 GMT  
		Size: 2.6 MB (2604697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2c0812639412c4c0ebb658178d523dd452e722e4147bee6b58c7ae5cce292d4`  
		Last Modified: Wed, 21 Jan 2026 21:20:00 GMT  
		Size: 12.7 KB (12723 bytes)  
		MIME: application/vnd.in-toto+json
