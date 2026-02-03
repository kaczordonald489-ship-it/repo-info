## `sapmachine:lts-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:51744ca1680b036702a56a4f1896c0bd2d55e6a559e5dda790a4d551ececb10f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:f379f00345e4911030dea6057ddad69a6c7fbd2e6f34c12512b1db4a835a89a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86884506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbbac21b5805dad30e62a898408fef3529997c42252d79bb69403b747017fab`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 20:02:31 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:02:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 20:02:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3527b1a030dd541d736f4c920c261d8d2f190c46afdbd74a4735467be3a1be1d`  
		Last Modified: Wed, 21 Jan 2026 20:02:45 GMT  
		Size: 57.3 MB (57347839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f74e00f69e270da51d900b96161d854b9d69889e3275a5a44c2bcdc0b847e253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2563810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f310bc42cd53447737a6a4283f5fa3f33e3ed3f600f732bff5ffa453b42a494c`

```dockerfile
```

-	Layers:
	-	`sha256:1089dc38a751f01f7a2ffa427f2aaab50ec8fad230e431c20712fbbbd11bdf5e`  
		Last Modified: Wed, 21 Jan 2026 20:02:43 GMT  
		Size: 2.6 MB (2553721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c09698f4d67da6c8996642de425021c27ec2af201f4cdf42b3cd999ffde3c75c`  
		Last Modified: Wed, 21 Jan 2026 20:02:43 GMT  
		Size: 10.1 KB (10089 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:42d079317171b7d5b324ce3c925036c458645df80240b717927fb02cbc64b9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83638385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5da167c2401e5e9e97c554d95a08298410e113d36f9cadcf168a32f6dbfb4fa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 20:08:33 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:08:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 20:08:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6b1d3f94980d9e86cbf5f1261205c8643067226ce77f0a54e92abe336a0fd9`  
		Last Modified: Wed, 21 Jan 2026 20:08:50 GMT  
		Size: 56.3 MB (56254888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:96168748c2f3fe79a8657d0dd8a1e959fb51a257abae74cf38598fdcf0ffd52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2563689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ec6145ded8563bfe0863c7f9d6b38e3977f464b6e78ca483dd68d44da69fe7`

```dockerfile
```

-	Layers:
	-	`sha256:4474a5942482dba1d850d83990c87c224f3f6330587973e27f386144c36910e3`  
		Last Modified: Wed, 21 Jan 2026 20:08:46 GMT  
		Size: 2.6 MB (2553448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d05b84aabeb20a14e3f7dee3ff5ea9a549e176e2f2fd6a731407ecee35ec0288`  
		Last Modified: Wed, 21 Jan 2026 20:08:45 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a7256a01637efcfec9b208b33719a0eeba1595aabeadb741f8f1dafbebb61b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92676177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55a16bbc2910a757cfed8c3aab8f3b68aef2ac5b96423237eb942ba50d09b7a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 21:16:28 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:16:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 21:16:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94527ed8814314d2a70f5ee92a99866dbbe6731be5da30690e563d3cc47a493e`  
		Last Modified: Wed, 21 Jan 2026 21:17:05 GMT  
		Size: 58.2 MB (58229215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d402442a1a7db6f00684e419d0d5db8ff992fa71de8374fe9957332fd1951749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2562804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f93c5dee3060fe2d73d29798c29946f49d38f638647f931588e493cc2f02d99`

```dockerfile
```

-	Layers:
	-	`sha256:c5a2ccf6c19d0cb486b5613fd13a5a9abe3d0ca968807abc42897c1887678d6d`  
		Last Modified: Wed, 21 Jan 2026 21:17:03 GMT  
		Size: 2.6 MB (2552647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:214b7b8ea9b635e115a2060d4484553ff2e829235243ea7e1307a907bc8be5e3`  
		Last Modified: Wed, 21 Jan 2026 21:17:02 GMT  
		Size: 10.2 KB (10157 bytes)  
		MIME: application/vnd.in-toto+json
