## `sapmachine:11-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:27414d5072a2112a9153a6b683e8ac3f1d8a8583a2a43c298141123ead5d26bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:3cb209d2b37b225bc354f42e3a379ca6c1440e4b3f2db88b2fbc1308c49c3a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229845758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b72546d6bd7286dadd1a79aeb8071cbf7c1da8771116e7585b5feaa85946593`
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
# Wed, 21 Jan 2026 20:06:03 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.30 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:06:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 21 Jan 2026 20:06:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b69cbee612c680cf9070bfa0ac2ca3136b195044570fe0a2fad664021ac19dc`  
		Last Modified: Wed, 21 Jan 2026 20:07:26 GMT  
		Size: 200.3 MB (200309091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:97ffdedc48a3945e77f991cdf859ddd5c8c5e4a5a74e17fd11452be045c2f1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2650708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7dc3225cb828e4f41aca58c910e98ad1acabaa4e10fab6fa89dc106317e04d`

```dockerfile
```

-	Layers:
	-	`sha256:96a0c5ffb2a45d4d0feff2fb026f277cdbadd9ebbd349622148dd76e5585628a`  
		Last Modified: Wed, 21 Jan 2026 20:06:20 GMT  
		Size: 2.6 MB (2640615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1474100a6b9cd1467f37ca4b2498b505f22cb31b3c13f4d240c220154a8b3c5`  
		Last Modified: Wed, 21 Jan 2026 20:06:20 GMT  
		Size: 10.1 KB (10093 bytes)  
		MIME: application/vnd.in-toto+json
