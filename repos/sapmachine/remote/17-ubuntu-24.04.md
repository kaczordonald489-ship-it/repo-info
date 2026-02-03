## `sapmachine:17-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:e08151b4f2ed209eee234ba570ac6fe40f5667ba74cafd0581da31c571a3d87b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:abf5388e834f164622f3335a3cf2a5c81ee58a5a6a1831b9935324a938d17362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231408682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18123637056c008157159bf0b131d8bb6e1ce0a0bd5186785a09f4ccca1b4af0`
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
# Wed, 21 Jan 2026 20:04:24 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:04:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:04:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c57dcb4b77b462dfa5c5af8cf55361e84cd11262812016036092715b108a9c`  
		Last Modified: Wed, 21 Jan 2026 20:04:46 GMT  
		Size: 201.7 MB (201682671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7f29c836db9e85c6ccd3c0d9f43542931fbb0581389a66f2dd01b6835ce203d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3fe2251529acd5b0b1f6ec22d6f28e540f32ce011db3d8ba2cd46d975648da`

```dockerfile
```

-	Layers:
	-	`sha256:e273d5e2e106c86b90b57d70016d738bc80b6d56c8b8343833ba07a3a20c1ce5`  
		Last Modified: Wed, 21 Jan 2026 20:04:43 GMT  
		Size: 2.6 MB (2605226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207231a3348d935b65cff13a7b3fd79f1133a84df56c0ba0ed2d211e9cf8ff36`  
		Last Modified: Wed, 21 Jan 2026 20:04:42 GMT  
		Size: 12.6 KB (12606 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:37eab208c71a4626db217dc84ec73f122e6a2d832a432937a21e05655dbb67f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.3 MB (229285423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f09feb3b872eb83b846266eb7d4d47efa51059d1e7372c9f20f90a8397fd5c1`
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
# Wed, 21 Jan 2026 20:10:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:10:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:10:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbd91831faf9988a8f6995050b3ccf7c6fd98ad0cd6b2ca6f3f2fae4dc632af`  
		Last Modified: Wed, 21 Jan 2026 20:10:43 GMT  
		Size: 200.4 MB (200421599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bbf931b6f57fa514c00c1e6c9a37dcacb8ec908c21a1164d3f47612b94f7f7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002d1bb0002621bf7ad53bed354fd0b9b9d13d42b7f727deecdf4fef41d0be8f`

```dockerfile
```

-	Layers:
	-	`sha256:e0c8a4c06f05a01728c09a3090fbf65c41a484b98904e92758090c1c54da61c7`  
		Last Modified: Wed, 21 Jan 2026 20:10:38 GMT  
		Size: 2.6 MB (2605838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a93b71e5fd87f155339141f411b516978d004ae5a011967a52f0e7a01812c88e`  
		Last Modified: Wed, 21 Jan 2026 20:10:38 GMT  
		Size: 12.9 KB (12855 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:03f5082b81e45687697ebc1f2c8605398a283108aecd96d3b775042bce968a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236869447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc0b787037e62a60dacdccb52b36f430fb59defd88a932a933460cf820816381`
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
# Wed, 21 Jan 2026 21:27:53 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:27:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 21:27:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d241a998872d58f4d2154f9c51c95f5d34fe4e4b8a8042d33f5ab59f2a42b9d`  
		Last Modified: Wed, 21 Jan 2026 21:28:42 GMT  
		Size: 202.6 MB (202563288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8388a91f5a2263207b718aaa832aa32a97f2b85803f23d2dc4b0f39abcd9569c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1ffe05645ff91fc2c63742ef19c947d83ed3212d8cc6f7dfd6543d43728993`

```dockerfile
```

-	Layers:
	-	`sha256:e97faf62a95e72fa1b511cfeb94caa652a533f81dbdebe6f718f1c2be7f09e5e`  
		Last Modified: Wed, 21 Jan 2026 21:28:37 GMT  
		Size: 2.6 MB (2602826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74e5a830f2d515bf62e4ea2160bac330ede02ee905554290c18aaea674f671fb`  
		Last Modified: Wed, 21 Jan 2026 21:28:37 GMT  
		Size: 12.7 KB (12723 bytes)  
		MIME: application/vnd.in-toto+json
