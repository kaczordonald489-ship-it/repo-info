## `sapmachine:lts-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:2ccffdb34f2ebc70c53121d296b94c3376029755efe552b98cffdecd6b2f4f34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:abd115879c8c24f020c75af1d1d027282a08a2ad337577ae849e2cbc601e03fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85665831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e223f165f824240f65d96e580250504ee157dd9e0a46d1800166fc34496ad7`
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
# Wed, 21 Jan 2026 20:02:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:02:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 20:02:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d6d9814161a09f351e776dd5d7520554278fab62472a2febcd7f2f13bf45b1`  
		Last Modified: Wed, 21 Jan 2026 20:02:54 GMT  
		Size: 56.1 MB (56129164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4fb1a854b4fb6685c43da1d501534e1bca8bdd76274484350817c0c242b59c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2313303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c4b7c677002a3e6c1d39938444b63cfec171f1a00e6faf607bd2a1022bb807`

```dockerfile
```

-	Layers:
	-	`sha256:e3c040c918f56746b38fa2d7f5cacd62aeb15c6df5cb0bd9b04d967ea78cd68b`  
		Last Modified: Wed, 21 Jan 2026 20:02:52 GMT  
		Size: 2.3 MB (2303031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23addef01b1cc902ac9297701975ef351d2c287b505b9c79b1eede6bed355a77`  
		Last Modified: Wed, 21 Jan 2026 20:02:52 GMT  
		Size: 10.3 KB (10272 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c139e924f6c661e3c46d9bc21fc66eb371e7ac9c5b9f4c93018cd0423f77bc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82424533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960f61eaa50f2681a2346911c256205be373d4c1fd987f07123c01f8b9ff348b`
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
# Wed, 21 Jan 2026 20:08:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:08:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 20:08:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d9b985aa2f0ba7a0a08536d06183d899e37d5dc94bf027d8b6b1cd7ac4ae4e`  
		Last Modified: Wed, 21 Jan 2026 20:09:35 GMT  
		Size: 55.0 MB (55041036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2a1109abc59e80885bd1b1f512e9e1260b8bb1666cc46f04d3844f8720c2a907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2313171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5437de0e619fd7b0ebe580783e4d483294da273d553746a6f16a08f600c2a0d`

```dockerfile
```

-	Layers:
	-	`sha256:b8b3316a0e47c8c40ae7b1897282ab2d38e0893ea618f2eed0e522b6f1847e3a`  
		Last Modified: Wed, 21 Jan 2026 20:08:48 GMT  
		Size: 2.3 MB (2302748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b56faa68168d6b7f062c04fb27d83f176f15f5a50f353043ff5f67916e56d66b`  
		Last Modified: Wed, 21 Jan 2026 20:08:48 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5a0e15c87e0cd88c86117e13d2565a255e3f74c33a00bbabda8637f1e35f1ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91284179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807af6b47bfc7ce7ce516ff230d330d036e0132eef3305f55acfad6c30504db6`
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
# Wed, 21 Jan 2026 21:16:27 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:16:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 21:16:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0159c8c076a5f6316bd42808a626d76edeb59614fed705a11113c28ac394fb7`  
		Last Modified: Wed, 21 Jan 2026 21:17:03 GMT  
		Size: 56.8 MB (56837217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eebccabb60d1ac571b6b9dc5338372e934149a1a348cb79ce1d8896218a1f442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d9a237d6fd1f0249e93037cbabc2d38ea351993f1ed8646ab962d8fe1bc159`

```dockerfile
```

-	Layers:
	-	`sha256:88d3e5dbb7983eea69a3fccec402b50d7710466ad592a1d08755c58f8238ff50`  
		Last Modified: Wed, 21 Jan 2026 21:17:01 GMT  
		Size: 2.3 MB (2301867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11bebbe39bba05c02bee8dba3485112041fdb033e3a30e7aff8891bdb51aee28`  
		Last Modified: Wed, 21 Jan 2026 21:17:00 GMT  
		Size: 10.3 KB (10339 bytes)  
		MIME: application/vnd.in-toto+json
