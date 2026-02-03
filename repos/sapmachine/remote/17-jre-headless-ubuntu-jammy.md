## `sapmachine:17-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:9e93404e47ca54af45899a8a3884124c02dd25b01e248ca357778f2d65f514fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:333503a2082af4341093d7463373789b9c85b38bf9d787f158e37b48b893a512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82695929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c8b4b7fd6b9815b9aa3610282ed487a914d6abea5f485e06bc8ab313bf4e2d`
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
# Wed, 21 Jan 2026 20:05:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:05:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:05:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92789d6673db923eb3c0328026df934fad7ea81bcc1532ad122f4162e8e3998`  
		Last Modified: Wed, 21 Jan 2026 20:05:19 GMT  
		Size: 53.2 MB (53159262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5aa5a5edad88e94493408f18e51ca186c6083e6c4affabecc06985436bfb02a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b76d8cc79e2fee32a7fa74fd029d6321ca53c1fa0191c155503b69cf8ace2e7`

```dockerfile
```

-	Layers:
	-	`sha256:5f820ea9491f07a2c045ba2551bcdc56410bc255594e52d2021f804f4c1d9053`  
		Last Modified: Wed, 21 Jan 2026 20:05:17 GMT  
		Size: 2.3 MB (2295235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:277bc6f5ac5c3b904798206008e386ff5d26553fdd03d0769405322c0bf9fbf4`  
		Last Modified: Wed, 21 Jan 2026 20:05:17 GMT  
		Size: 8.9 KB (8885 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:865941408661a8711e6d9189f36483afdf36d774fe89ddff5d4ea6f60c84157a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79932375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d133388b4a9b5d1e21a9840a11c6e16bc431c1656668146b68c8c225ba136fb0`
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
# Wed, 21 Jan 2026 20:03:28 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:03:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:03:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a208ffa118fecaf964854c464cc89ab6853de1d18c0680b721b6fa8162e84194`  
		Last Modified: Wed, 21 Jan 2026 20:04:51 GMT  
		Size: 52.5 MB (52548878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:42b7a1892a64b06a06941c78520cb0692d749435d2db881fa5b883cdd4e60884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cd71d983434313403d1ed58dc1b9c200b65172f8c082f1ddec00cb14dc9a37`

```dockerfile
```

-	Layers:
	-	`sha256:8ca03306b7287dd76fcb4df850a8f0c59058e84ae8188cb33775a9eb0e6f8b9e`  
		Last Modified: Wed, 21 Jan 2026 20:03:44 GMT  
		Size: 2.3 MB (2294907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4245971dcd6f5277da6084f3e22f3c61fbc13513b738c3aa50e983e03483efd`  
		Last Modified: Wed, 21 Jan 2026 20:03:44 GMT  
		Size: 9.0 KB (8988 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:337ebe0cf36d3f275e28b8eb615879030b775e14855a6e85e29e904b54ffaf08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88617423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed8793e6e9f1def1ab4b2d86dc8306ee17645fc14535444755fb458b6d25ee1`
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
# Wed, 21 Jan 2026 21:34:01 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:34:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 21:34:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556745b2d2ad97c4d3cc32a77c14d2fab3f7b268cd53e35b9aae1740a2d1b44a`  
		Last Modified: Wed, 21 Jan 2026 21:34:30 GMT  
		Size: 54.2 MB (54170461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:841155592f3bc311dc82a51688c42d11d4817be988d9e42bfe57f4aeef273f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cee141630fd5e89cf70b4358be1afca46c5e4d424c17529e57b1c1bcae6c5b`

```dockerfile
```

-	Layers:
	-	`sha256:318fc1fbe59c90e4365cf52b9f290db4a2f32f17d808f932c28feb367e070c3e`  
		Last Modified: Wed, 21 Jan 2026 21:34:28 GMT  
		Size: 2.3 MB (2294677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec473070ea54483bfc0341f8028bcdc5fa98b996b2ea456254dee2ca1863487b`  
		Last Modified: Wed, 21 Jan 2026 21:34:27 GMT  
		Size: 8.9 KB (8928 bytes)  
		MIME: application/vnd.in-toto+json
