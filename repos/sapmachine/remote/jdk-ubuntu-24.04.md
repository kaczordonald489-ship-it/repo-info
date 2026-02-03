## `sapmachine:jdk-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:e2306fd91014bb7a4901e0c4cf107f1c2decbb78adb792209e1c453c6b33ba8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:ef2f7b0699297a6abbcf7b5fe3b2273c581579e8ee9e8c457ee15f4a78c750e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251175072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52918a8917321b9b1a7e9147647a282924a44339223644ed3e5814ca83ba1fa`
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
# Wed, 21 Jan 2026 20:02:43 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:02:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 20:02:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166a188c954e02cb107f6f7af69649f2eb170ffdf79a4a1df2f2e7dfe512ea7f`  
		Last Modified: Wed, 21 Jan 2026 20:03:04 GMT  
		Size: 221.4 MB (221449061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d90ad1829f39dfea5606d5b73faccdedc10694c7f5cb0478bc30fa5bbc8e8e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9561c99fcd45a4bf9783b7afa595150db84cdd710eabd25c6dc7cc972ee0451`

```dockerfile
```

-	Layers:
	-	`sha256:83bba3656f93b08a79eb069b5cc032ffaf61bd15e1d4a64fce17c8c39bcd5539`  
		Last Modified: Wed, 21 Jan 2026 20:03:00 GMT  
		Size: 2.6 MB (2601301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06abec3fef64dbb56e2c53f97ef914af11bf4a069408f8dfe34ef6a0f06a1e91`  
		Last Modified: Wed, 21 Jan 2026 20:03:00 GMT  
		Size: 17.4 KB (17356 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:fe92ace1f069ddb091da8175edf74f0e97880a1ccfb1babd1c8e369444f67a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248127171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da2f20213f399ef91f83e4d6e6f268b83e93b86e325661a83ff7d0ad6f9d16f`
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
# Wed, 21 Jan 2026 20:05:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:05:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 20:05:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc36bb5ef69434c4feef5be6306492cf245860d3dded017911c99182ab4f9b2`  
		Last Modified: Wed, 21 Jan 2026 20:09:00 GMT  
		Size: 219.3 MB (219263347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:68e04425a166b85749aec80377727fddf3bf211f23d7aa2d3e6d59107b3a4e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2619874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f8f5a3f4acd87a0b083dbc7b8f88d820c67287ced3f4f10d3866073bac2ca4`

```dockerfile
```

-	Layers:
	-	`sha256:f674af1a50a329e13a77b5d15334d5315d7a232b2faf688c96fe73f60b6781d9`  
		Last Modified: Wed, 21 Jan 2026 20:05:54 GMT  
		Size: 2.6 MB (2602090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:863f9bae80a30a5156b034e643c6408a618ab42035feb210c450d4f067c635e5`  
		Last Modified: Wed, 21 Jan 2026 20:05:54 GMT  
		Size: 17.8 KB (17784 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7e543f2a9dce09cefb33c92896b3f9f57f97fe793c7d052f6446d07020f9e6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256673775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9bedc80ca8271606c14abe82accdacec3c77e49ee42df99a9c0014081a45c3`
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
# Wed, 21 Jan 2026 21:08:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:08:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 21:08:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9785c838943c455dacbd1904b35930cbf043e7af6e17b5ee6873ee451b8864e`  
		Last Modified: Wed, 21 Jan 2026 21:09:39 GMT  
		Size: 222.4 MB (222367616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b3ba2eee9e347eb6c48e8b1d7127fe0c258e6b1cefb35126cb7f6886739081a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3492c0d716285ce78049a10d84213792734cbf0468197edf802a439816bedab`

```dockerfile
```

-	Layers:
	-	`sha256:7ac369a9a6bbd0fb3fc10d59800bc618cd274ab99ea06ae02aec2dcdd2f35364`  
		Last Modified: Wed, 21 Jan 2026 21:09:34 GMT  
		Size: 2.6 MB (2598373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbbbf06fcedd97e06f800bc24295900830b0d9623ff1e21a3e92dd6981d52f78`  
		Last Modified: Wed, 21 Jan 2026 21:09:34 GMT  
		Size: 17.6 KB (17562 bytes)  
		MIME: application/vnd.in-toto+json
