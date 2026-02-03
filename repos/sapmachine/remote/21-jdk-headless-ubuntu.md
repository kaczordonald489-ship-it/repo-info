## `sapmachine:21-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:d47d39bd33785c14af9d85ee42683f51d40b1517756a19f04364f3eb8ae18aa7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:244c35234b1dd53171e5c746f0537f07a67047f1553b2bfa6ff39dd1d9b4fb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244920689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba3c1fe2a9f755fa6d85a6d67b257cb0c60e9cc3760da1b84ff5b3a7477824a`
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
# Wed, 21 Jan 2026 20:03:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:03:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 21 Jan 2026 20:03:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84f2beaef1bc14992068b4e7ebc6415f5227b315f43e37022affe8d0cebccfd`  
		Last Modified: Wed, 21 Jan 2026 20:04:35 GMT  
		Size: 215.2 MB (215194678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ec6e72c50fe1cec24f986b9bd57cf4fb7bda5dbf6c5efae0c130e8dde73fa95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2368953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf165775d3ba319347ccc907e42fd0ac2c4d84db4df999c20f4e2b88bee58e2`

```dockerfile
```

-	Layers:
	-	`sha256:3947a650b7855fc4163e12e94919896b1d17739ea6f63668314773f0c1128619`  
		Last Modified: Wed, 21 Jan 2026 20:03:50 GMT  
		Size: 2.4 MB (2358719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cff9aeaf32c32030a00666e4dad97068660a3299e50ff04c49e59f49a3976d54`  
		Last Modified: Wed, 21 Jan 2026 20:03:50 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4715f926460d741fa5b59c8b2a30c348ab6a205e9b637cf2ffc9a42069ac5a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242302701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca41a242072239f91cf18dc28e7dcfa8b12d306d00d00ad1b6cbdc34c16ab99`
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
# Wed, 21 Jan 2026 20:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 21 Jan 2026 20:09:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d18392c054ac1b3239ba9ad360902544067027e4c6aeb93610e17a2684a462`  
		Last Modified: Wed, 21 Jan 2026 20:09:58 GMT  
		Size: 213.4 MB (213438877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ce0d41733cf8faec11a7057efa2e03cf19c5d4ba4c3ae45d5251304efcf13bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7700a29d5a2a95f82715e9a4a1aa1776579f95341cfa562db8ddd98e78f99063`

```dockerfile
```

-	Layers:
	-	`sha256:b4c372103609ae40be58c364d12c3b717914cf8a96a1d1090f5437f6333dfa03`  
		Last Modified: Wed, 21 Jan 2026 20:09:54 GMT  
		Size: 2.4 MB (2359226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b8c815fa71d8bc9d2d8230847089f38087347bda1315142f752cb3e70d37ef`  
		Last Modified: Wed, 21 Jan 2026 20:09:54 GMT  
		Size: 10.4 KB (10386 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3beea52df6a10ae0d116137e444b02520867dd82cb1b0ab41af43897cba02d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250336853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9bdb014712223898f98c187a52f9b3e061b2c8751ab1f0519989ae43e02fafc`
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
# Wed, 21 Jan 2026 21:19:05 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:19:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 21 Jan 2026 21:19:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99aff77964468e1b26156d88bb453ac66a2f9c2ccba99da62287393c9f474ac`  
		Last Modified: Wed, 21 Jan 2026 21:19:52 GMT  
		Size: 216.0 MB (216030694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7428b090e6275ea4a7bb240566151e94909c1577dad039e24a5c6345dd4a68e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61df97dbf9c32abaee2aca4761e276e1684184759310a1cbd546f370ffb4fc2c`

```dockerfile
```

-	Layers:
	-	`sha256:4cb65b86c09d95cf1d8a5c7b630f96879d53135bc8d3e706d0dc988c361d1d0c`  
		Last Modified: Wed, 21 Jan 2026 21:19:47 GMT  
		Size: 2.4 MB (2356190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d8bfd5afda63679b107e9fa6bc26348bb7f848697611e47011b86a6de132c16`  
		Last Modified: Wed, 21 Jan 2026 21:19:47 GMT  
		Size: 10.3 KB (10300 bytes)  
		MIME: application/vnd.in-toto+json
