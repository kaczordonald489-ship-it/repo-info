## `sapmachine:21-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:a4eab45e14c3f973f3e366b3fe0eb8e3ce0a664c45313d25d147f4e7b803aa96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:c7d6f1948d262516e413479ae9a647bf85dc010203232a76dd3a4a4340332930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89824318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9002ac0cfa7ac1451b27dc577e4a39e75c284852fbdb92b3d7172ed468b7a029`
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
# Wed, 21 Jan 2026 20:03:49 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:03:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 21 Jan 2026 20:03:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e4596ca123abc9dabf9db634effa5ac9ca99147305662e188d99b0b6e879bf`  
		Last Modified: Wed, 21 Jan 2026 20:04:03 GMT  
		Size: 60.3 MB (60287651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8bd46671e5acbfbfba86ef4158231d14266d6775af474fc0ef49b8f8bf88d8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2556047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5fa591a4eb7e9cc9df8d29f29fd0a57638deafd307d3dad9f58debef7960fe`

```dockerfile
```

-	Layers:
	-	`sha256:a65acdcb159a05d6c27cfdb2bb0915ce76ea2190b0045c831cdac8a82145ae09`  
		Last Modified: Wed, 21 Jan 2026 20:04:01 GMT  
		Size: 2.5 MB (2547273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17e7b3ebf93c78258f042397f053c895bb7424293333b619668e0d8a8f39a90`  
		Last Modified: Wed, 21 Jan 2026 20:04:01 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:5d80f852c0bfdc64fec27b457ec80afbc8786e6c070a33b8c85c194b65493d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86811369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b06c07c9692d74e3a02c58a354dff0cf2249a51ac52b7f7eb6961544b23dde`
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
# Wed, 21 Jan 2026 20:10:10 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:10:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 21 Jan 2026 20:10:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c26ad99b6bc0b0b008081241e1799b19f66238616615792e0092537757dfb8`  
		Last Modified: Wed, 21 Jan 2026 20:10:24 GMT  
		Size: 59.4 MB (59427872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:74e7059db74ad838c7705433e0c7fee8e6fbe5bc56157068db4675353184ce95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2555833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e02c34bb329214e592d355b86f5aa97aa1d6a97dae7a8d132036d1dcdd98a6`

```dockerfile
```

-	Layers:
	-	`sha256:8c5922bf2e19e657a2864a79f6bf6a190394c4e358cd0fe903ebf6dc53450df8`  
		Last Modified: Wed, 21 Jan 2026 20:10:23 GMT  
		Size: 2.5 MB (2546955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b69879ff580b260e8252568f927a1ee364fa322eeeb4d53d89263878bbf398ba`  
		Last Modified: Wed, 21 Jan 2026 20:10:22 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:96b20d24e7f038ce47276f77a67561a970c1d28facb56f25039d62e6d95760d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95946830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3754a2eb70c96968cb52848743aa5c4677e14ceae143f739d30222e168786be5`
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
# Wed, 21 Jan 2026 21:26:10 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:26:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 21 Jan 2026 21:26:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba737098a51c7794c89db81d5a57afca22f1a808b572e38c5455e34e47c2a81`  
		Last Modified: Wed, 21 Jan 2026 21:26:40 GMT  
		Size: 61.5 MB (61499868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d58e157b0a688ada7530ab5a779fa3abd5cfb652f9757935913ff1168cef1977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2555623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a748f3bfb9aae00b59814f24179427856817067b8b82663e4ee0cfb8dc1eb2`

```dockerfile
```

-	Layers:
	-	`sha256:5f2125981bf286607f162ec8b028b38ad9b278824fe9b6c188247ef21de99492`  
		Last Modified: Wed, 21 Jan 2026 21:26:37 GMT  
		Size: 2.5 MB (2546805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa1b2a4fc184472e4082cd1c02b40ee9423cfc23a6456674983fcc7e06483f6`  
		Last Modified: Wed, 21 Jan 2026 21:26:37 GMT  
		Size: 8.8 KB (8818 bytes)  
		MIME: application/vnd.in-toto+json
