<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2-bookworm-slim`](#rethinkdb2-bookworm-slim)
-	[`rethinkdb:2.4`](#rethinkdb24)
-	[`rethinkdb:2.4-bookworm-slim`](#rethinkdb24-bookworm-slim)
-	[`rethinkdb:2.4.3`](#rethinkdb243)
-	[`rethinkdb:2.4.4-bookworm-slim`](#rethinkdb244-bookworm-slim)
-	[`rethinkdb:bookworm-slim`](#rethinkdbbookworm-slim)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:c6a11bceb61f7d9b4976b807f7ce1d2ae94f6b93e4c4f81382180ffaf81cf8db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bb8d3c0b307874a1cdb16b88a3c202a2ecea806e6e4e69250c47cdcb715f46fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48023894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeb349107efd20d96bb1473fd9b0e716472599786f16a17a430fa583cd4d6cb`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:40:31 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:32 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 02:40:38 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 02:40:38 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:38 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 02:40:38 GMT
WORKDIR /data
# Tue, 03 Feb 2026 02:40:38 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 02:40:38 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76584a18922b33caf3e0ab6a2adb8da577ddb7a1d5e623b11349d566bf963b5e`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 9.8 MB (9799474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b0dc3cc1df7db043f57e1fde5ca5a3e719a540c34af1f26789e5595698b6c8`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca02345d6ab7c33392f64382c0f1123c6cb743f5022fc23c3de475eb4277038`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 10.0 MB (9993172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332584b7efe5b08f842b7d8571dbbef8185cefd28f87373f2fdadb3bb624c6f9`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:1691ab5159cc30b0f58b0a66267aed165355b571476e6f31bd1fb4bb42fab92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d2359f47811513844aa661c5839654da68fa3e72215ab71f5c3da03058dab3`

```dockerfile
```

-	Layers:
	-	`sha256:92a14570fbcbc56bbabbf1a1238f55ac220c050608af29d01ed4826d8a1f5015`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a6fe0111f47e8406504e6d532d6a50d126d7e41fb1a2a306ac7169dbde889d`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:adcab62dc2e22e1b98c65ec91c5a4ac213bdc3e4fa8d97dac798e2c4a50caafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47101884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad2eb9c737a0a9498bfd0017077f5cf517be29aab1457f31abf8049695f51ac`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:37 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:38 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 02:43:43 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 02:43:43 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:43 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 02:43:43 GMT
WORKDIR /data
# Tue, 03 Feb 2026 02:43:43 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 02:43:43 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbc10cb2738437dcc2105fe19fff70b6e7438c59e9e1d31a2394a42cdbfd586`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 9.6 MB (9628338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e10e670cc527932fd596f8646ab519eb533d0f3283a26678ae5a92fd34ff94`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9eac2d9ec334e448f085dd8db4d1e023f6e36ae772a1440b6706e53bf145c7`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 9.4 MB (9362962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0befb76a73a88e59fd9b4280da24358113cfe916dc7071a277229055370eb`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:8b31298b4b927edb669c3fd6729f079e815019d028d877df7f11f3a4a80e191f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dad9f79fa67f52cc1a6af10757a7d0b7b95687eefc9ee710290a8f6c8615f6`

```dockerfile
```

-	Layers:
	-	`sha256:26f2b02e3d73edfadb873e2b61ec6ac72327486c26398e7f5bce3f28fec0319c`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a00bf135a7be0d6c85feb64408db7cadc5b9efbc8c9f30ae2965ae171282ee0b`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; s390x

```console
$ docker pull rethinkdb@sha256:0ae1b63653164d6b1069c30b4d2a5f454779ffbbcdb107912433a2b50968fb05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e1facdd9903d94317b91ba0ba221c3db9c27f6309e56b5c14c477fa85e1ee9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:43:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 03:43:41 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 03:43:41 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:41 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 03:43:41 GMT
WORKDIR /data
# Tue, 03 Feb 2026 03:43:41 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 03:43:41 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcabe115ba46de236b43e5dc6f2fa1fd1a28049dd628abf044f12d247f198a37`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 9.3 MB (9297517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c65a6bd3dabfeaf03a74dff1f91adef77f8963659ed1b957e6adf02e1cf54f0`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777c76dd2c81b2ca0420a8f102d5c43bc9679b7fcc4b224b8ad0657b25955634`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 9.3 MB (9303778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b13967361fcf6a2da266c76659603b1b68316005ccf699a3b4d1e7d1eae54d5`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c80df3a3bec480a33b10fcf04856b0f3e5ce11a156a7cda300492f30bc7d82b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef471627305c82e838741dd50ed4482629e11f13decb9599a6c9b2ded1141bcb`

```dockerfile
```

-	Layers:
	-	`sha256:01528faed76290a7dd5628fe2b1754737aff13913e47e9e4d4685bd74258b810`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d0400974caee94984086af17b5cd62cd4cbb8c8567be23e45ca15e8f1238e1`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:c6a11bceb61f7d9b4976b807f7ce1d2ae94f6b93e4c4f81382180ffaf81cf8db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bb8d3c0b307874a1cdb16b88a3c202a2ecea806e6e4e69250c47cdcb715f46fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48023894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeb349107efd20d96bb1473fd9b0e716472599786f16a17a430fa583cd4d6cb`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:40:31 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:32 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 02:40:38 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 02:40:38 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:38 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 02:40:38 GMT
WORKDIR /data
# Tue, 03 Feb 2026 02:40:38 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 02:40:38 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76584a18922b33caf3e0ab6a2adb8da577ddb7a1d5e623b11349d566bf963b5e`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 9.8 MB (9799474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b0dc3cc1df7db043f57e1fde5ca5a3e719a540c34af1f26789e5595698b6c8`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca02345d6ab7c33392f64382c0f1123c6cb743f5022fc23c3de475eb4277038`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 10.0 MB (9993172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332584b7efe5b08f842b7d8571dbbef8185cefd28f87373f2fdadb3bb624c6f9`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:1691ab5159cc30b0f58b0a66267aed165355b571476e6f31bd1fb4bb42fab92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d2359f47811513844aa661c5839654da68fa3e72215ab71f5c3da03058dab3`

```dockerfile
```

-	Layers:
	-	`sha256:92a14570fbcbc56bbabbf1a1238f55ac220c050608af29d01ed4826d8a1f5015`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a6fe0111f47e8406504e6d532d6a50d126d7e41fb1a2a306ac7169dbde889d`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:adcab62dc2e22e1b98c65ec91c5a4ac213bdc3e4fa8d97dac798e2c4a50caafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47101884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad2eb9c737a0a9498bfd0017077f5cf517be29aab1457f31abf8049695f51ac`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:37 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:38 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 02:43:43 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 02:43:43 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:43 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 02:43:43 GMT
WORKDIR /data
# Tue, 03 Feb 2026 02:43:43 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 02:43:43 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbc10cb2738437dcc2105fe19fff70b6e7438c59e9e1d31a2394a42cdbfd586`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 9.6 MB (9628338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e10e670cc527932fd596f8646ab519eb533d0f3283a26678ae5a92fd34ff94`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9eac2d9ec334e448f085dd8db4d1e023f6e36ae772a1440b6706e53bf145c7`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 9.4 MB (9362962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0befb76a73a88e59fd9b4280da24358113cfe916dc7071a277229055370eb`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:8b31298b4b927edb669c3fd6729f079e815019d028d877df7f11f3a4a80e191f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dad9f79fa67f52cc1a6af10757a7d0b7b95687eefc9ee710290a8f6c8615f6`

```dockerfile
```

-	Layers:
	-	`sha256:26f2b02e3d73edfadb873e2b61ec6ac72327486c26398e7f5bce3f28fec0319c`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a00bf135a7be0d6c85feb64408db7cadc5b9efbc8c9f30ae2965ae171282ee0b`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:0ae1b63653164d6b1069c30b4d2a5f454779ffbbcdb107912433a2b50968fb05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e1facdd9903d94317b91ba0ba221c3db9c27f6309e56b5c14c477fa85e1ee9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:43:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 03:43:41 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 03:43:41 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:41 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 03:43:41 GMT
WORKDIR /data
# Tue, 03 Feb 2026 03:43:41 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 03:43:41 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcabe115ba46de236b43e5dc6f2fa1fd1a28049dd628abf044f12d247f198a37`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 9.3 MB (9297517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c65a6bd3dabfeaf03a74dff1f91adef77f8963659ed1b957e6adf02e1cf54f0`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777c76dd2c81b2ca0420a8f102d5c43bc9679b7fcc4b224b8ad0657b25955634`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 9.3 MB (9303778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b13967361fcf6a2da266c76659603b1b68316005ccf699a3b4d1e7d1eae54d5`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c80df3a3bec480a33b10fcf04856b0f3e5ce11a156a7cda300492f30bc7d82b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef471627305c82e838741dd50ed4482629e11f13decb9599a6c9b2ded1141bcb`

```dockerfile
```

-	Layers:
	-	`sha256:01528faed76290a7dd5628fe2b1754737aff13913e47e9e4d4685bd74258b810`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d0400974caee94984086af17b5cd62cd4cbb8c8567be23e45ca15e8f1238e1`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:c6a11bceb61f7d9b4976b807f7ce1d2ae94f6b93e4c4f81382180ffaf81cf8db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bb8d3c0b307874a1cdb16b88a3c202a2ecea806e6e4e69250c47cdcb715f46fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48023894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeb349107efd20d96bb1473fd9b0e716472599786f16a17a430fa583cd4d6cb`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:40:31 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:32 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 02:40:38 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 02:40:38 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:38 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 02:40:38 GMT
WORKDIR /data
# Tue, 03 Feb 2026 02:40:38 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 02:40:38 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76584a18922b33caf3e0ab6a2adb8da577ddb7a1d5e623b11349d566bf963b5e`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 9.8 MB (9799474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b0dc3cc1df7db043f57e1fde5ca5a3e719a540c34af1f26789e5595698b6c8`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca02345d6ab7c33392f64382c0f1123c6cb743f5022fc23c3de475eb4277038`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 10.0 MB (9993172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332584b7efe5b08f842b7d8571dbbef8185cefd28f87373f2fdadb3bb624c6f9`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:1691ab5159cc30b0f58b0a66267aed165355b571476e6f31bd1fb4bb42fab92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d2359f47811513844aa661c5839654da68fa3e72215ab71f5c3da03058dab3`

```dockerfile
```

-	Layers:
	-	`sha256:92a14570fbcbc56bbabbf1a1238f55ac220c050608af29d01ed4826d8a1f5015`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a6fe0111f47e8406504e6d532d6a50d126d7e41fb1a2a306ac7169dbde889d`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:adcab62dc2e22e1b98c65ec91c5a4ac213bdc3e4fa8d97dac798e2c4a50caafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47101884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad2eb9c737a0a9498bfd0017077f5cf517be29aab1457f31abf8049695f51ac`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:37 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:38 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 02:43:43 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 02:43:43 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:43 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 02:43:43 GMT
WORKDIR /data
# Tue, 03 Feb 2026 02:43:43 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 02:43:43 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbc10cb2738437dcc2105fe19fff70b6e7438c59e9e1d31a2394a42cdbfd586`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 9.6 MB (9628338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e10e670cc527932fd596f8646ab519eb533d0f3283a26678ae5a92fd34ff94`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9eac2d9ec334e448f085dd8db4d1e023f6e36ae772a1440b6706e53bf145c7`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 9.4 MB (9362962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0befb76a73a88e59fd9b4280da24358113cfe916dc7071a277229055370eb`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:8b31298b4b927edb669c3fd6729f079e815019d028d877df7f11f3a4a80e191f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dad9f79fa67f52cc1a6af10757a7d0b7b95687eefc9ee710290a8f6c8615f6`

```dockerfile
```

-	Layers:
	-	`sha256:26f2b02e3d73edfadb873e2b61ec6ac72327486c26398e7f5bce3f28fec0319c`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a00bf135a7be0d6c85feb64408db7cadc5b9efbc8c9f30ae2965ae171282ee0b`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; s390x

```console
$ docker pull rethinkdb@sha256:0ae1b63653164d6b1069c30b4d2a5f454779ffbbcdb107912433a2b50968fb05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e1facdd9903d94317b91ba0ba221c3db9c27f6309e56b5c14c477fa85e1ee9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:43:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 03:43:41 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 03:43:41 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:41 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 03:43:41 GMT
WORKDIR /data
# Tue, 03 Feb 2026 03:43:41 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 03:43:41 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcabe115ba46de236b43e5dc6f2fa1fd1a28049dd628abf044f12d247f198a37`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 9.3 MB (9297517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c65a6bd3dabfeaf03a74dff1f91adef77f8963659ed1b957e6adf02e1cf54f0`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777c76dd2c81b2ca0420a8f102d5c43bc9679b7fcc4b224b8ad0657b25955634`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 9.3 MB (9303778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b13967361fcf6a2da266c76659603b1b68316005ccf699a3b4d1e7d1eae54d5`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c80df3a3bec480a33b10fcf04856b0f3e5ce11a156a7cda300492f30bc7d82b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef471627305c82e838741dd50ed4482629e11f13decb9599a6c9b2ded1141bcb`

```dockerfile
```

-	Layers:
	-	`sha256:01528faed76290a7dd5628fe2b1754737aff13913e47e9e4d4685bd74258b810`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d0400974caee94984086af17b5cd62cd4cbb8c8567be23e45ca15e8f1238e1`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:c6a11bceb61f7d9b4976b807f7ce1d2ae94f6b93e4c4f81382180ffaf81cf8db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bb8d3c0b307874a1cdb16b88a3c202a2ecea806e6e4e69250c47cdcb715f46fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48023894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeb349107efd20d96bb1473fd9b0e716472599786f16a17a430fa583cd4d6cb`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:40:31 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:32 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 02:40:38 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 02:40:38 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:38 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 02:40:38 GMT
WORKDIR /data
# Tue, 03 Feb 2026 02:40:38 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 02:40:38 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76584a18922b33caf3e0ab6a2adb8da577ddb7a1d5e623b11349d566bf963b5e`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 9.8 MB (9799474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b0dc3cc1df7db043f57e1fde5ca5a3e719a540c34af1f26789e5595698b6c8`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca02345d6ab7c33392f64382c0f1123c6cb743f5022fc23c3de475eb4277038`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 10.0 MB (9993172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332584b7efe5b08f842b7d8571dbbef8185cefd28f87373f2fdadb3bb624c6f9`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:1691ab5159cc30b0f58b0a66267aed165355b571476e6f31bd1fb4bb42fab92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d2359f47811513844aa661c5839654da68fa3e72215ab71f5c3da03058dab3`

```dockerfile
```

-	Layers:
	-	`sha256:92a14570fbcbc56bbabbf1a1238f55ac220c050608af29d01ed4826d8a1f5015`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a6fe0111f47e8406504e6d532d6a50d126d7e41fb1a2a306ac7169dbde889d`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:adcab62dc2e22e1b98c65ec91c5a4ac213bdc3e4fa8d97dac798e2c4a50caafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47101884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad2eb9c737a0a9498bfd0017077f5cf517be29aab1457f31abf8049695f51ac`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:37 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:38 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 02:43:43 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 02:43:43 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:43 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 02:43:43 GMT
WORKDIR /data
# Tue, 03 Feb 2026 02:43:43 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 02:43:43 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbc10cb2738437dcc2105fe19fff70b6e7438c59e9e1d31a2394a42cdbfd586`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 9.6 MB (9628338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e10e670cc527932fd596f8646ab519eb533d0f3283a26678ae5a92fd34ff94`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9eac2d9ec334e448f085dd8db4d1e023f6e36ae772a1440b6706e53bf145c7`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 9.4 MB (9362962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0befb76a73a88e59fd9b4280da24358113cfe916dc7071a277229055370eb`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:8b31298b4b927edb669c3fd6729f079e815019d028d877df7f11f3a4a80e191f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dad9f79fa67f52cc1a6af10757a7d0b7b95687eefc9ee710290a8f6c8615f6`

```dockerfile
```

-	Layers:
	-	`sha256:26f2b02e3d73edfadb873e2b61ec6ac72327486c26398e7f5bce3f28fec0319c`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a00bf135a7be0d6c85feb64408db7cadc5b9efbc8c9f30ae2965ae171282ee0b`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:0ae1b63653164d6b1069c30b4d2a5f454779ffbbcdb107912433a2b50968fb05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e1facdd9903d94317b91ba0ba221c3db9c27f6309e56b5c14c477fa85e1ee9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:43:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 03:43:41 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 03:43:41 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:41 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 03:43:41 GMT
WORKDIR /data
# Tue, 03 Feb 2026 03:43:41 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 03:43:41 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcabe115ba46de236b43e5dc6f2fa1fd1a28049dd628abf044f12d247f198a37`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 9.3 MB (9297517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c65a6bd3dabfeaf03a74dff1f91adef77f8963659ed1b957e6adf02e1cf54f0`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777c76dd2c81b2ca0420a8f102d5c43bc9679b7fcc4b224b8ad0657b25955634`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 9.3 MB (9303778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b13967361fcf6a2da266c76659603b1b68316005ccf699a3b4d1e7d1eae54d5`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c80df3a3bec480a33b10fcf04856b0f3e5ce11a156a7cda300492f30bc7d82b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef471627305c82e838741dd50ed4482629e11f13decb9599a6c9b2ded1141bcb`

```dockerfile
```

-	Layers:
	-	`sha256:01528faed76290a7dd5628fe2b1754737aff13913e47e9e4d4685bd74258b810`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d0400974caee94984086af17b5cd62cd4cbb8c8567be23e45ca15e8f1238e1`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4.3`

```console
$ docker pull rethinkdb@sha256:c6a11bceb61f7d9b4976b807f7ce1d2ae94f6b93e4c4f81382180ffaf81cf8db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4.3` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bb8d3c0b307874a1cdb16b88a3c202a2ecea806e6e4e69250c47cdcb715f46fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48023894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeb349107efd20d96bb1473fd9b0e716472599786f16a17a430fa583cd4d6cb`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:40:31 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:32 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 02:40:38 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 02:40:38 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:38 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 02:40:38 GMT
WORKDIR /data
# Tue, 03 Feb 2026 02:40:38 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 02:40:38 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76584a18922b33caf3e0ab6a2adb8da577ddb7a1d5e623b11349d566bf963b5e`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 9.8 MB (9799474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b0dc3cc1df7db043f57e1fde5ca5a3e719a540c34af1f26789e5595698b6c8`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca02345d6ab7c33392f64382c0f1123c6cb743f5022fc23c3de475eb4277038`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 10.0 MB (9993172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332584b7efe5b08f842b7d8571dbbef8185cefd28f87373f2fdadb3bb624c6f9`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:1691ab5159cc30b0f58b0a66267aed165355b571476e6f31bd1fb4bb42fab92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d2359f47811513844aa661c5839654da68fa3e72215ab71f5c3da03058dab3`

```dockerfile
```

-	Layers:
	-	`sha256:92a14570fbcbc56bbabbf1a1238f55ac220c050608af29d01ed4826d8a1f5015`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a6fe0111f47e8406504e6d532d6a50d126d7e41fb1a2a306ac7169dbde889d`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:adcab62dc2e22e1b98c65ec91c5a4ac213bdc3e4fa8d97dac798e2c4a50caafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47101884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad2eb9c737a0a9498bfd0017077f5cf517be29aab1457f31abf8049695f51ac`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:37 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:38 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 02:43:43 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 02:43:43 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:43 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 02:43:43 GMT
WORKDIR /data
# Tue, 03 Feb 2026 02:43:43 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 02:43:43 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbc10cb2738437dcc2105fe19fff70b6e7438c59e9e1d31a2394a42cdbfd586`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 9.6 MB (9628338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e10e670cc527932fd596f8646ab519eb533d0f3283a26678ae5a92fd34ff94`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9eac2d9ec334e448f085dd8db4d1e023f6e36ae772a1440b6706e53bf145c7`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 9.4 MB (9362962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0befb76a73a88e59fd9b4280da24358113cfe916dc7071a277229055370eb`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:8b31298b4b927edb669c3fd6729f079e815019d028d877df7f11f3a4a80e191f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dad9f79fa67f52cc1a6af10757a7d0b7b95687eefc9ee710290a8f6c8615f6`

```dockerfile
```

-	Layers:
	-	`sha256:26f2b02e3d73edfadb873e2b61ec6ac72327486c26398e7f5bce3f28fec0319c`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a00bf135a7be0d6c85feb64408db7cadc5b9efbc8c9f30ae2965ae171282ee0b`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; s390x

```console
$ docker pull rethinkdb@sha256:0ae1b63653164d6b1069c30b4d2a5f454779ffbbcdb107912433a2b50968fb05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e1facdd9903d94317b91ba0ba221c3db9c27f6309e56b5c14c477fa85e1ee9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:43:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 03:43:41 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 03:43:41 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:41 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 03:43:41 GMT
WORKDIR /data
# Tue, 03 Feb 2026 03:43:41 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 03:43:41 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcabe115ba46de236b43e5dc6f2fa1fd1a28049dd628abf044f12d247f198a37`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 9.3 MB (9297517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c65a6bd3dabfeaf03a74dff1f91adef77f8963659ed1b957e6adf02e1cf54f0`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777c76dd2c81b2ca0420a8f102d5c43bc9679b7fcc4b224b8ad0657b25955634`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 9.3 MB (9303778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b13967361fcf6a2da266c76659603b1b68316005ccf699a3b4d1e7d1eae54d5`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c80df3a3bec480a33b10fcf04856b0f3e5ce11a156a7cda300492f30bc7d82b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef471627305c82e838741dd50ed4482629e11f13decb9599a6c9b2ded1141bcb`

```dockerfile
```

-	Layers:
	-	`sha256:01528faed76290a7dd5628fe2b1754737aff13913e47e9e4d4685bd74258b810`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d0400974caee94984086af17b5cd62cd4cbb8c8567be23e45ca15e8f1238e1`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:c6a11bceb61f7d9b4976b807f7ce1d2ae94f6b93e4c4f81382180ffaf81cf8db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4.4-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bb8d3c0b307874a1cdb16b88a3c202a2ecea806e6e4e69250c47cdcb715f46fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48023894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeb349107efd20d96bb1473fd9b0e716472599786f16a17a430fa583cd4d6cb`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:40:31 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:32 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 02:40:38 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 02:40:38 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:38 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 02:40:38 GMT
WORKDIR /data
# Tue, 03 Feb 2026 02:40:38 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 02:40:38 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76584a18922b33caf3e0ab6a2adb8da577ddb7a1d5e623b11349d566bf963b5e`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 9.8 MB (9799474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b0dc3cc1df7db043f57e1fde5ca5a3e719a540c34af1f26789e5595698b6c8`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca02345d6ab7c33392f64382c0f1123c6cb743f5022fc23c3de475eb4277038`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 10.0 MB (9993172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332584b7efe5b08f842b7d8571dbbef8185cefd28f87373f2fdadb3bb624c6f9`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:1691ab5159cc30b0f58b0a66267aed165355b571476e6f31bd1fb4bb42fab92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d2359f47811513844aa661c5839654da68fa3e72215ab71f5c3da03058dab3`

```dockerfile
```

-	Layers:
	-	`sha256:92a14570fbcbc56bbabbf1a1238f55ac220c050608af29d01ed4826d8a1f5015`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a6fe0111f47e8406504e6d532d6a50d126d7e41fb1a2a306ac7169dbde889d`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:adcab62dc2e22e1b98c65ec91c5a4ac213bdc3e4fa8d97dac798e2c4a50caafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47101884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad2eb9c737a0a9498bfd0017077f5cf517be29aab1457f31abf8049695f51ac`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:37 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:38 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 02:43:43 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 02:43:43 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:43 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 02:43:43 GMT
WORKDIR /data
# Tue, 03 Feb 2026 02:43:43 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 02:43:43 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbc10cb2738437dcc2105fe19fff70b6e7438c59e9e1d31a2394a42cdbfd586`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 9.6 MB (9628338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e10e670cc527932fd596f8646ab519eb533d0f3283a26678ae5a92fd34ff94`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9eac2d9ec334e448f085dd8db4d1e023f6e36ae772a1440b6706e53bf145c7`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 9.4 MB (9362962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0befb76a73a88e59fd9b4280da24358113cfe916dc7071a277229055370eb`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:8b31298b4b927edb669c3fd6729f079e815019d028d877df7f11f3a4a80e191f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dad9f79fa67f52cc1a6af10757a7d0b7b95687eefc9ee710290a8f6c8615f6`

```dockerfile
```

-	Layers:
	-	`sha256:26f2b02e3d73edfadb873e2b61ec6ac72327486c26398e7f5bce3f28fec0319c`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a00bf135a7be0d6c85feb64408db7cadc5b9efbc8c9f30ae2965ae171282ee0b`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:0ae1b63653164d6b1069c30b4d2a5f454779ffbbcdb107912433a2b50968fb05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e1facdd9903d94317b91ba0ba221c3db9c27f6309e56b5c14c477fa85e1ee9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:43:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 03:43:41 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 03:43:41 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:41 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 03:43:41 GMT
WORKDIR /data
# Tue, 03 Feb 2026 03:43:41 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 03:43:41 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcabe115ba46de236b43e5dc6f2fa1fd1a28049dd628abf044f12d247f198a37`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 9.3 MB (9297517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c65a6bd3dabfeaf03a74dff1f91adef77f8963659ed1b957e6adf02e1cf54f0`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777c76dd2c81b2ca0420a8f102d5c43bc9679b7fcc4b224b8ad0657b25955634`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 9.3 MB (9303778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b13967361fcf6a2da266c76659603b1b68316005ccf699a3b4d1e7d1eae54d5`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c80df3a3bec480a33b10fcf04856b0f3e5ce11a156a7cda300492f30bc7d82b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef471627305c82e838741dd50ed4482629e11f13decb9599a6c9b2ded1141bcb`

```dockerfile
```

-	Layers:
	-	`sha256:01528faed76290a7dd5628fe2b1754737aff13913e47e9e4d4685bd74258b810`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d0400974caee94984086af17b5cd62cd4cbb8c8567be23e45ca15e8f1238e1`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:c6a11bceb61f7d9b4976b807f7ce1d2ae94f6b93e4c4f81382180ffaf81cf8db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bb8d3c0b307874a1cdb16b88a3c202a2ecea806e6e4e69250c47cdcb715f46fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48023894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeb349107efd20d96bb1473fd9b0e716472599786f16a17a430fa583cd4d6cb`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:40:31 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:32 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 02:40:38 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 02:40:38 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:38 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 02:40:38 GMT
WORKDIR /data
# Tue, 03 Feb 2026 02:40:38 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 02:40:38 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76584a18922b33caf3e0ab6a2adb8da577ddb7a1d5e623b11349d566bf963b5e`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 9.8 MB (9799474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b0dc3cc1df7db043f57e1fde5ca5a3e719a540c34af1f26789e5595698b6c8`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca02345d6ab7c33392f64382c0f1123c6cb743f5022fc23c3de475eb4277038`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 10.0 MB (9993172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332584b7efe5b08f842b7d8571dbbef8185cefd28f87373f2fdadb3bb624c6f9`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:1691ab5159cc30b0f58b0a66267aed165355b571476e6f31bd1fb4bb42fab92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d2359f47811513844aa661c5839654da68fa3e72215ab71f5c3da03058dab3`

```dockerfile
```

-	Layers:
	-	`sha256:92a14570fbcbc56bbabbf1a1238f55ac220c050608af29d01ed4826d8a1f5015`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a6fe0111f47e8406504e6d532d6a50d126d7e41fb1a2a306ac7169dbde889d`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:adcab62dc2e22e1b98c65ec91c5a4ac213bdc3e4fa8d97dac798e2c4a50caafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47101884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad2eb9c737a0a9498bfd0017077f5cf517be29aab1457f31abf8049695f51ac`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:37 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:38 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 02:43:43 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 02:43:43 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:43 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 02:43:43 GMT
WORKDIR /data
# Tue, 03 Feb 2026 02:43:43 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 02:43:43 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbc10cb2738437dcc2105fe19fff70b6e7438c59e9e1d31a2394a42cdbfd586`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 9.6 MB (9628338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e10e670cc527932fd596f8646ab519eb533d0f3283a26678ae5a92fd34ff94`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9eac2d9ec334e448f085dd8db4d1e023f6e36ae772a1440b6706e53bf145c7`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 9.4 MB (9362962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0befb76a73a88e59fd9b4280da24358113cfe916dc7071a277229055370eb`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:8b31298b4b927edb669c3fd6729f079e815019d028d877df7f11f3a4a80e191f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dad9f79fa67f52cc1a6af10757a7d0b7b95687eefc9ee710290a8f6c8615f6`

```dockerfile
```

-	Layers:
	-	`sha256:26f2b02e3d73edfadb873e2b61ec6ac72327486c26398e7f5bce3f28fec0319c`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a00bf135a7be0d6c85feb64408db7cadc5b9efbc8c9f30ae2965ae171282ee0b`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:0ae1b63653164d6b1069c30b4d2a5f454779ffbbcdb107912433a2b50968fb05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e1facdd9903d94317b91ba0ba221c3db9c27f6309e56b5c14c477fa85e1ee9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:43:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 03:43:41 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 03:43:41 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:41 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 03:43:41 GMT
WORKDIR /data
# Tue, 03 Feb 2026 03:43:41 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 03:43:41 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcabe115ba46de236b43e5dc6f2fa1fd1a28049dd628abf044f12d247f198a37`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 9.3 MB (9297517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c65a6bd3dabfeaf03a74dff1f91adef77f8963659ed1b957e6adf02e1cf54f0`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777c76dd2c81b2ca0420a8f102d5c43bc9679b7fcc4b224b8ad0657b25955634`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 9.3 MB (9303778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b13967361fcf6a2da266c76659603b1b68316005ccf699a3b4d1e7d1eae54d5`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c80df3a3bec480a33b10fcf04856b0f3e5ce11a156a7cda300492f30bc7d82b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef471627305c82e838741dd50ed4482629e11f13decb9599a6c9b2ded1141bcb`

```dockerfile
```

-	Layers:
	-	`sha256:01528faed76290a7dd5628fe2b1754737aff13913e47e9e4d4685bd74258b810`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d0400974caee94984086af17b5cd62cd4cbb8c8567be23e45ca15e8f1238e1`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:c6a11bceb61f7d9b4976b807f7ce1d2ae94f6b93e4c4f81382180ffaf81cf8db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bb8d3c0b307874a1cdb16b88a3c202a2ecea806e6e4e69250c47cdcb715f46fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48023894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeb349107efd20d96bb1473fd9b0e716472599786f16a17a430fa583cd4d6cb`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:40:31 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:32 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 02:40:38 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 02:40:38 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:38 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 02:40:38 GMT
WORKDIR /data
# Tue, 03 Feb 2026 02:40:38 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 02:40:38 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76584a18922b33caf3e0ab6a2adb8da577ddb7a1d5e623b11349d566bf963b5e`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 9.8 MB (9799474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b0dc3cc1df7db043f57e1fde5ca5a3e719a540c34af1f26789e5595698b6c8`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca02345d6ab7c33392f64382c0f1123c6cb743f5022fc23c3de475eb4277038`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 10.0 MB (9993172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332584b7efe5b08f842b7d8571dbbef8185cefd28f87373f2fdadb3bb624c6f9`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:1691ab5159cc30b0f58b0a66267aed165355b571476e6f31bd1fb4bb42fab92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d2359f47811513844aa661c5839654da68fa3e72215ab71f5c3da03058dab3`

```dockerfile
```

-	Layers:
	-	`sha256:92a14570fbcbc56bbabbf1a1238f55ac220c050608af29d01ed4826d8a1f5015`  
		Last Modified: Tue, 03 Feb 2026 02:40:46 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a6fe0111f47e8406504e6d532d6a50d126d7e41fb1a2a306ac7169dbde889d`  
		Last Modified: Tue, 03 Feb 2026 02:40:45 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:adcab62dc2e22e1b98c65ec91c5a4ac213bdc3e4fa8d97dac798e2c4a50caafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47101884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad2eb9c737a0a9498bfd0017077f5cf517be29aab1457f31abf8049695f51ac`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:37 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:38 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 02:43:43 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 02:43:43 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:43:43 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 02:43:43 GMT
WORKDIR /data
# Tue, 03 Feb 2026 02:43:43 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 02:43:43 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbc10cb2738437dcc2105fe19fff70b6e7438c59e9e1d31a2394a42cdbfd586`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 9.6 MB (9628338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e10e670cc527932fd596f8646ab519eb533d0f3283a26678ae5a92fd34ff94`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9eac2d9ec334e448f085dd8db4d1e023f6e36ae772a1440b6706e53bf145c7`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 9.4 MB (9362962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0befb76a73a88e59fd9b4280da24358113cfe916dc7071a277229055370eb`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:8b31298b4b927edb669c3fd6729f079e815019d028d877df7f11f3a4a80e191f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dad9f79fa67f52cc1a6af10757a7d0b7b95687eefc9ee710290a8f6c8615f6`

```dockerfile
```

-	Layers:
	-	`sha256:26f2b02e3d73edfadb873e2b61ec6ac72327486c26398e7f5bce3f28fec0319c`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a00bf135a7be0d6c85feb64408db7cadc5b9efbc8c9f30ae2965ae171282ee0b`  
		Last Modified: Tue, 03 Feb 2026 02:43:51 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:0ae1b63653164d6b1069c30b4d2a5f454779ffbbcdb107912433a2b50968fb05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e1facdd9903d94317b91ba0ba221c3db9c27f6309e56b5c14c477fa85e1ee9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:43:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 03 Feb 2026 03:43:41 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 03 Feb 2026 03:43:41 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:41 GMT
VOLUME [/data]
# Tue, 03 Feb 2026 03:43:41 GMT
WORKDIR /data
# Tue, 03 Feb 2026 03:43:41 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 03 Feb 2026 03:43:41 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcabe115ba46de236b43e5dc6f2fa1fd1a28049dd628abf044f12d247f198a37`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 9.3 MB (9297517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c65a6bd3dabfeaf03a74dff1f91adef77f8963659ed1b957e6adf02e1cf54f0`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777c76dd2c81b2ca0420a8f102d5c43bc9679b7fcc4b224b8ad0657b25955634`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 9.3 MB (9303778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b13967361fcf6a2da266c76659603b1b68316005ccf699a3b4d1e7d1eae54d5`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c80df3a3bec480a33b10fcf04856b0f3e5ce11a156a7cda300492f30bc7d82b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef471627305c82e838741dd50ed4482629e11f13decb9599a6c9b2ded1141bcb`

```dockerfile
```

-	Layers:
	-	`sha256:01528faed76290a7dd5628fe2b1754737aff13913e47e9e4d4685bd74258b810`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d0400974caee94984086af17b5cd62cd4cbb8c8567be23e45ca15e8f1238e1`  
		Last Modified: Tue, 03 Feb 2026 03:43:53 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json
