## `sapmachine:11-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:1cb72abac24be3b3262a66bdc1c6452fdacaadd4322685935e63b6ffe4510794
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:125454742c23c3b8bbe60613611354ece704630fe133a78204cee9b8541cbaa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228620232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7222d5862c8ff6dbcc950c1f981c38f56f4485e240e6eb0438ebbd340f20cd73`
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
# Wed, 21 Jan 2026 20:06:01 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.30 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:06:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 21 Jan 2026 20:06:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f63906695def30e5811ca97dd273613fe3aa746cf8b67648ab502502eba87ae`  
		Last Modified: Wed, 21 Jan 2026 20:06:22 GMT  
		Size: 199.1 MB (199083565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:99be20cd4f75d52a70d919cfc7737dd0af928c0258ac1c058d3bf606116b9c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee9c0e5c067bad67bdb05fb7d833bcdda6d6aa4184d9696a8c7c5252ad7a05c`

```dockerfile
```

-	Layers:
	-	`sha256:dff5380f22df5c952c1b729b658e1df9958b5071771e9c39cd1eb3cf24a72bd3`  
		Last Modified: Wed, 21 Jan 2026 20:06:17 GMT  
		Size: 2.4 MB (2388519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f303d2472e535e06589cf2a9d9eaf727d423bef10141f30747d707ca927d999a`  
		Last Modified: Wed, 21 Jan 2026 20:06:17 GMT  
		Size: 8.9 KB (8890 bytes)  
		MIME: application/vnd.in-toto+json
