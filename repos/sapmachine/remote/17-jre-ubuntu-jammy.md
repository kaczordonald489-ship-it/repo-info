## `sapmachine:17-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:3319db67c51c371f7847ef9636e3f750cc52760823173a8135927ab1199d5530
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:bb4c488c4cf058b1d6c7d80322fb3346d46488c4ad345920035cba01a750f083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83920308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77fe65d6e23c56815c5e501a4d13b220b8aadd40ba1f3d80e1607b641dc2d7e`
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
# Wed, 21 Jan 2026 20:04:43 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:04:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:04:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf263d7e8d2e078db7ecf4629567a91ba87f0de46ab9b02291e34693f0f84dd`  
		Last Modified: Wed, 21 Jan 2026 20:04:55 GMT  
		Size: 54.4 MB (54383641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:23e6162b8d533c522145ad3918e7eb61c614ed4d80645103f6f465345510c091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812f8c71ac26fa64f59c3ed53ae8af283bb32d4e1171fd15c12b338a96c20e6e`

```dockerfile
```

-	Layers:
	-	`sha256:abf7abe199347a6b31d634dee403edaf7a603ee3d8346ddfc3ef24d698d9c031`  
		Last Modified: Wed, 21 Jan 2026 20:04:54 GMT  
		Size: 2.5 MB (2546015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e886b05b54ca9d866d492d75e1e4f4536187143b51c61d9303d6a66d319f704a`  
		Last Modified: Wed, 21 Jan 2026 20:04:54 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:fe67c88de883c1e509918e76f160dd417810766c154a9d524a0698cf01f0b1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81141066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75d39eeb956bec57507967133bf539e22c23abfb2bef1fcf39cf2f67f69f384`
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
# Wed, 21 Jan 2026 20:10:39 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:10:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:10:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f996159be1f3c9169bde5c6622835b01951e1077c16d7e44a97a9a6ba769de1`  
		Last Modified: Wed, 21 Jan 2026 20:10:52 GMT  
		Size: 53.8 MB (53757569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:00f604ffc4da5956e0a6a4b08067bc7c78e0cb9c1fc6adba62f1f16efc862edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90352d1051791f039a8b655c30a523bd68a465632dcd2186d02e4a8ebe19aaed`

```dockerfile
```

-	Layers:
	-	`sha256:b146302f2efaf3177a0045554e45086d98b9db0c9adfa7802afad89af64782d6`  
		Last Modified: Wed, 21 Jan 2026 20:10:51 GMT  
		Size: 2.5 MB (2545697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2425b0f12ca98a0d69dff3e5b2a41d0615adeca336b51714550b58a1136134b5`  
		Last Modified: Wed, 21 Jan 2026 20:10:50 GMT  
		Size: 8.9 KB (8876 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a4dd8451431c66d9408cc8aec41ec7de7848572314a164975521747b8cdbb139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90018945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b216eff0aea6ef9b39e27e1d4a6b612cdb853ee03afc860b0a840e6fb8adf09`
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
# Wed, 21 Jan 2026 21:34:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:34:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 21:34:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7b9fb85db2b483376d6e0804e6d4494dad402c47c8fdfbdfb7890c563478ed`  
		Last Modified: Wed, 21 Jan 2026 21:34:35 GMT  
		Size: 55.6 MB (55571983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d085bfffdeddaef049f94942a0af874e8d3638a4694c20a713c6606af5012e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2278e0c964ef41bb86590822fd0b518558beba1541467fd6b6b8930621de99a2`

```dockerfile
```

-	Layers:
	-	`sha256:adbdd0a1e0bec22a8ae433fc13d81ff2993758f9be663266cc9110b6b17efc58`  
		Last Modified: Wed, 21 Jan 2026 21:34:33 GMT  
		Size: 2.5 MB (2545547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e98042722b5979e8c061a027dce3c55d6481405cb215f04cc19187ca2e1ab1`  
		Last Modified: Wed, 21 Jan 2026 21:34:33 GMT  
		Size: 8.8 KB (8818 bytes)  
		MIME: application/vnd.in-toto+json
