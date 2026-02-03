## `sapmachine:11-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:ca1a1c2f6a613d25dd4ff875677eb73c8d738cc86bc1fec5dfe32acdca61120a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:4ac6257e4ecde464c7fefd548fb362bef802192860d14266939c117a84585531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78026183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b44609104c56ec0435c45db6b5c3457a3f7638d623c51a02d8fac6cb4252bd`
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
# Wed, 21 Jan 2026 20:05:48 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.30 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:05:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 21 Jan 2026 20:05:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5da394f35c68e4f26cf8ef69c225ff0e7345568cb5caac34669699b27cc338`  
		Last Modified: Wed, 21 Jan 2026 20:05:59 GMT  
		Size: 48.5 MB (48489516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4380abf2dee5d16e0adab1323d264223b8f7f6bcef985790876feed840d9d808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb153e7ad93cb34a884feabb1ad3d906ea3574471e7b4032ba4091e9e8cce45`

```dockerfile
```

-	Layers:
	-	`sha256:bea7878bd70b3b1406cca8f1575535ad71a923bbd69dee2f4aec60ac3bc8264d`  
		Last Modified: Wed, 21 Jan 2026 20:05:58 GMT  
		Size: 2.3 MB (2299118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f81c065fb9a5709c6383d9ee22ea0d0a102693f6668a84ea2e528c06688e05c3`  
		Last Modified: Wed, 21 Jan 2026 20:05:58 GMT  
		Size: 8.9 KB (8885 bytes)  
		MIME: application/vnd.in-toto+json
