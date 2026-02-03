## `sapmachine:17-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:533b6ab4092afaa62f907d3eae6741b3448ff862587d3741eccdbbf2a59665e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:43824094bb5a92468d610e18728ad9fbd36c2a37ea14784870838639bcd9fb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230835502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b851940d54d4d7e2bf22cda1fac742c37bd9d13bdc926d5e3569b8e0111af6`
-	Default Command: `["jshell"]`

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
# Wed, 21 Jan 2026 20:04:53 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:04:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:04:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277b5d86c1fbcbb1bc7712032c3427cc052d94f88ea3bbe9451338d94eae508e`  
		Last Modified: Wed, 21 Jan 2026 20:05:13 GMT  
		Size: 201.3 MB (201298835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:997a85fbfd92a0e7a0eca01369079efe46882f058658ef3113d037ee796c68d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d52db201d97286f1c79abc51942187f577c37ef15e8ca89cdeaaee331fc354`

```dockerfile
```

-	Layers:
	-	`sha256:3ebbde7e16f36de0b5f8817cf4447c64c4d33f771b7d238c5d4e7635677f25ae`  
		Last Modified: Wed, 21 Jan 2026 20:05:09 GMT  
		Size: 2.6 MB (2630239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2613e6e68920a3a4119d62f875b29bb630d7cdb757733390ad834cf471bfcdca`  
		Last Modified: Wed, 21 Jan 2026 20:05:09 GMT  
		Size: 10.1 KB (10094 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1279b2a5422d8f1d5b9a1146ca67ccac19d0d908aa43d16d305e0a3d57c8bd5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227363090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e037bfb68a1277ec1c6ac28f27eec4253d7f64841bdc6683ead5cb57f7075d5d`
-	Default Command: `["jshell"]`

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
# Wed, 21 Jan 2026 20:10:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:10:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:10:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b27fdc297d2a5cc19ac583ec7348b1680112837ec25e0f389d0c44b56ceebb`  
		Last Modified: Wed, 21 Jan 2026 20:10:53 GMT  
		Size: 200.0 MB (199979593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:47ca942bac3428a6ce1d0081f54a92d678fbf631cd5cb582f42b111e9f46bbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4903d102689ceb759e65fdb46c263c1c0203e800d174cd30906824cd41e7848`

```dockerfile
```

-	Layers:
	-	`sha256:91663e428e626889ab9cd82eb804f25087680a4921002d13494cd58183f8c52d`  
		Last Modified: Wed, 21 Jan 2026 20:10:47 GMT  
		Size: 2.6 MB (2629969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23574d0364aa7ed5c2a3763498adcb491843bce62556e9d7be52b93b5b98ee93`  
		Last Modified: Wed, 21 Jan 2026 20:10:46 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8ff0db5e3aeaa2cd11b0ec61ac4d64db25cb3cbc57973a9805e74329300de8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236518420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ab689462ca84a1dad9cb34c8a875425055b1d7b4fe90eeaf2b13c36b0249b9`
-	Default Command: `["jshell"]`

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
# Wed, 21 Jan 2026 21:32:01 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:32:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 21:32:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f42294ecc856ee3b0a2958ad24758e7252df21b7acaea27bb0955d09c2690b1`  
		Last Modified: Wed, 21 Jan 2026 21:32:44 GMT  
		Size: 202.1 MB (202071458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:98e672dc46059e86502c02b971a603f1f27a76450e262d0a152119fd7e500561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55227b9127b1b1b06971118a4c1e524328a6905fff811e42e57243e096742457`

```dockerfile
```

-	Layers:
	-	`sha256:0f5b958ec03a31d9d132fa7a875e6aebc441ea34b77e242ee4cbe34b70a902fa`  
		Last Modified: Wed, 21 Jan 2026 21:32:40 GMT  
		Size: 2.6 MB (2627849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7550b5d28b076cab8f6aa667aa852b387568c26784d2e0694f3d9c79e4dbb463`  
		Last Modified: Wed, 21 Jan 2026 21:32:39 GMT  
		Size: 10.2 KB (10163 bytes)  
		MIME: application/vnd.in-toto+json
