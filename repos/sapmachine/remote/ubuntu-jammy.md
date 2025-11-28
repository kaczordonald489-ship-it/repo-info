## `sapmachine:ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:2d3ef270490f19985bc1112644a9d59a1722f611bf9eebab3d1e797c5ed7a0ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:e8201ad99869ebf480c936a9c81b511bab086f436bccc76e1011c45b613bceb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249581960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a93a753f5781815fbf35a91697bb75dd4394d7749f4f298b47fdd199b1175f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:37:27 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:37:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c144a970a672f500175f70ed7879fe258ad46dd60d3b5bbe5e20052c0d409229`  
		Last Modified: Fri, 14 Nov 2025 08:18:22 GMT  
		Size: 220.0 MB (220045162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8db816d15ccf975b6b9627cde4306f993d0a31a5109fc7949f1fdfa005493e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cd659e34649b468efca6c520091e3256d3ea60d1e1bc7b4ac6978be8c16632`

```dockerfile
```

-	Layers:
	-	`sha256:dd52dba61e916cf2d57424299096100b6073ed703109fb5cefa80371ec04c99b`  
		Last Modified: Fri, 14 Nov 2025 01:13:03 GMT  
		Size: 2.6 MB (2621784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9f2186e9d4fe365dad1a6f274af82d922fa734f42de5cb339d4c37d4d9a480d`  
		Last Modified: Fri, 14 Nov 2025 01:13:04 GMT  
		Size: 12.7 KB (12690 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:07445e432a5996ff7104cfefa86e7347f0609a0c3f86279dab1b2b225fbad156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245124989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452b77dbbcc628238dcf527c4b6622826a068590a4419564abff184c268e22cd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:36:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e503216fd6d44139ad105d7dfdc85dba611f1778cb3df872fa2fbeda9f3711`  
		Last Modified: Fri, 14 Nov 2025 23:38:01 GMT  
		Size: 217.7 MB (217741112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:efb8ca5c468f6d50790c9b03930bb66171d68cccc8f8bd69d9a4a26571c2766c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af7eb5d01a43337cde7b5eb5019c343ae1836b4c63e2095813b542de5d7d544`

```dockerfile
```

-	Layers:
	-	`sha256:d528ac22a41bf8360835ab4d123bb171c22aecdc5c87121c3b63fa5859a81b4d`  
		Last Modified: Fri, 14 Nov 2025 01:13:08 GMT  
		Size: 2.6 MB (2621607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c419eacfd6275d749a259380832b0dc617b4f79d0541948f18dd2e97f6a9dac`  
		Last Modified: Fri, 14 Nov 2025 01:13:09 GMT  
		Size: 12.9 KB (12938 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:54a4f45e469ea6591e896788a2d7d02175c8d876e0b91408418965aef59f59c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 MB (255217814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0ed6fa2e076a64f3b8fbefc768598de791b2455fe205dec1052da308c4ca49`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:17:49 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:17:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 14 Nov 2025 01:17:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0dd83cae0549c577fb20382a37da37821a2be601b70432168264ecbd8307ff`  
		Last Modified: Fri, 14 Nov 2025 23:38:10 GMT  
		Size: 220.8 MB (220771092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e3aa0ef1386616c29a3bc2c6164d858b81e3fa8781787b921dfa2e8d45ccc891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2630213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83463bae11b91848d210eedf328c701637864a523b8c2ee957d57982e059f18`

```dockerfile
```

-	Layers:
	-	`sha256:fc8a392c3c0061910127f33cee37e951f6890ce03155fbfd79704e72d32bae53`  
		Last Modified: Fri, 14 Nov 2025 04:10:42 GMT  
		Size: 2.6 MB (2617407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afd7cd4df7881fd46b4b0735b86413e7a9986a9f03f5bbe205b0ea6c0acf5c57`  
		Last Modified: Fri, 14 Nov 2025 04:10:43 GMT  
		Size: 12.8 KB (12806 bytes)  
		MIME: application/vnd.in-toto+json
