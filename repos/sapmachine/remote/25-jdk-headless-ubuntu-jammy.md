## `sapmachine:25-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:11c520e91e85d12d5a4faf61108f2904957649829b4d27a0a4efdfb87ebb0030
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:546b035037fec12cf3c2bcd82b11c94b32d1b9c9ca376da85009221e07358e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248355957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eff6a1a8ced2678a16055895c6ccf51d7d4f34dc6608d35554d3b661246d3f0`
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
# Thu, 13 Nov 2025 23:37:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:37:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e585790b3db4e68f7a4675a2fed47e05f182c19d091f73ffae776749fb406944`  
		Last Modified: Fri, 14 Nov 2025 21:07:59 GMT  
		Size: 218.8 MB (218819159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:831f6630540aeeb9813c3f9f8b427d1e9a9552d7bf1ae304c0ab15676f5ee6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec90c189612be0d9ecb99b80e4b7bfcf701dc28a1bcc67c61be9230f0d0ad0e`

```dockerfile
```

-	Layers:
	-	`sha256:fc3fffff3de0ab331958ab8653cfc8a605118e251e368b818a0cafe2b1365963`  
		Last Modified: Fri, 14 Nov 2025 01:12:42 GMT  
		Size: 2.4 MB (2368494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbbf9d0b04510c97715be3934d03972fea1cb078a41944d71d8344f5a27b0e3d`  
		Last Modified: Fri, 14 Nov 2025 01:12:43 GMT  
		Size: 10.3 KB (10273 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c7f5e4a429b33448d09c83e1f0b40475c229afba349f38e0d23c06b5d3da4159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243909008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff8b353ce274e728006ec8479c09d6a9f6474dfb58fb39382d5bacecd4b9f99`
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
# Thu, 13 Nov 2025 23:37:18 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:37:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70807707472a928f850a76f4ce6fe431f9981789f4257cc1b1541649e0118e1`  
		Last Modified: Fri, 14 Nov 2025 23:32:44 GMT  
		Size: 216.5 MB (216525131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6f333701da17c9f1fc6cb705bd91696c538bfb4b377415cc6d022e081c1e5ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd0f9f0f14cc8c857988c0d95fbccc185a3fdb66b01398bff6e1df780ff9118`

```dockerfile
```

-	Layers:
	-	`sha256:74d26ac69855dd5a30f4488c27e837e8cc2eee17cf87ab3e0b7435a5fd11dbad`  
		Last Modified: Fri, 14 Nov 2025 01:12:47 GMT  
		Size: 2.4 MB (2368211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd8c98983584dfdb9cac0b8b8ddf891aa0631e3478204c5b5c42e43e4770ecb3`  
		Last Modified: Fri, 14 Nov 2025 01:12:48 GMT  
		Size: 10.4 KB (10425 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1ae23903331e60f312cd819a542e53b76f50af1fe5d967aecba1abec36b7408d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253811701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2f936cc0ad7a0e6d60e80003c5bc6611a2d7caf880ded0938136a5e5c1cfb9`
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
# Fri, 14 Nov 2025 01:20:09 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:20:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 14 Nov 2025 01:20:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dbbc0ca3622a8a195cc6d8684565b26286e85633bed968eb540ce313c4d595`  
		Last Modified: Fri, 14 Nov 2025 23:38:09 GMT  
		Size: 219.4 MB (219364979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ed178f6338f0ac9fe4f73001c88e8e946df653eb90baa85680ae84b9fdffcc7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd51712660a3151d8f0774300eaffe7d3b7537be9cc2446c31f863d82d7e55d`

```dockerfile
```

-	Layers:
	-	`sha256:23bb3c2fd61e8a8bc513ca387423290e5ed50d81f4740e3eff4db8951d0dd5d9`  
		Last Modified: Fri, 14 Nov 2025 04:10:27 GMT  
		Size: 2.4 MB (2363979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b63484c9068b3c47b28da411b1079846b828954804e959f0f805492261b489d2`  
		Last Modified: Fri, 14 Nov 2025 04:10:28 GMT  
		Size: 10.3 KB (10341 bytes)  
		MIME: application/vnd.in-toto+json
