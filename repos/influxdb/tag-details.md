<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.11`](#influxdb111)
-	[`influxdb:1.11-alpine`](#influxdb111-alpine)
-	[`influxdb:1.11-data`](#influxdb111-data)
-	[`influxdb:1.11-data-alpine`](#influxdb111-data-alpine)
-	[`influxdb:1.11-meta`](#influxdb111-meta)
-	[`influxdb:1.11-meta-alpine`](#influxdb111-meta-alpine)
-	[`influxdb:1.11.8`](#influxdb1118)
-	[`influxdb:1.11.8-alpine`](#influxdb1118-alpine)
-	[`influxdb:1.11.9-data`](#influxdb1119-data)
-	[`influxdb:1.11.9-data-alpine`](#influxdb1119-data-alpine)
-	[`influxdb:1.11.9-meta`](#influxdb1119-meta)
-	[`influxdb:1.11.9-meta-alpine`](#influxdb1119-meta-alpine)
-	[`influxdb:1.12`](#influxdb112)
-	[`influxdb:1.12-alpine`](#influxdb112-alpine)
-	[`influxdb:1.12-data`](#influxdb112-data)
-	[`influxdb:1.12-data-alpine`](#influxdb112-data-alpine)
-	[`influxdb:1.12-meta`](#influxdb112-meta)
-	[`influxdb:1.12-meta-alpine`](#influxdb112-meta-alpine)
-	[`influxdb:1.12.2`](#influxdb1122)
-	[`influxdb:1.12.2-alpine`](#influxdb1122-alpine)
-	[`influxdb:1.12.2-data`](#influxdb1122-data)
-	[`influxdb:1.12.2-data-alpine`](#influxdb1122-data-alpine)
-	[`influxdb:1.12.2-meta`](#influxdb1122-meta)
-	[`influxdb:1.12.2-meta-alpine`](#influxdb1122-meta-alpine)
-	[`influxdb:2`](#influxdb2)
-	[`influxdb:2-alpine`](#influxdb2-alpine)
-	[`influxdb:2.7`](#influxdb27)
-	[`influxdb:2.7-alpine`](#influxdb27-alpine)
-	[`influxdb:2.7.12`](#influxdb2712)
-	[`influxdb:2.7.12-alpine`](#influxdb2712-alpine)
-	[`influxdb:3-core`](#influxdb3-core)
-	[`influxdb:3-enterprise`](#influxdb3-enterprise)
-	[`influxdb:3.7-core`](#influxdb37-core)
-	[`influxdb:3.7-enterprise`](#influxdb37-enterprise)
-	[`influxdb:3.7.0-core`](#influxdb370-core)
-	[`influxdb:3.7.0-enterprise`](#influxdb370-enterprise)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:core`](#influxdbcore)
-	[`influxdb:enterprise`](#influxdbenterprise)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.11`

```console
$ docker pull influxdb@sha256:36c2374e78efeaca24a2bfed44afbd6871cf84d8108b2e70fee2c802fe64b970
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:c2b366b430f98e0194e16cf4f67cc7390de65deffa0ca61034d3ce37ef198c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116168161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a06c938f78256db0353879791f56034e0d1a8b95014f7aa0a5dbcaa2ba24fa3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:50:58 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 18 Nov 2025 06:51:06 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 18 Nov 2025 06:51:06 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:51:06 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 18 Nov 2025 06:51:06 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 06:51:06 GMT
VOLUME [/var/lib/influxdb]
# Tue, 18 Nov 2025 06:51:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:51:06 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 18 Nov 2025 06:51:06 GMT
USER influxdb
# Tue, 18 Nov 2025 06:51:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:51:06 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e79607692bfb29cca325f2e4292c2e3d9edf3581a2efc5c68c2f711d5f2c88a`  
		Last Modified: Tue, 18 Nov 2025 06:51:27 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7b788e35df5dd6d4a5af8bd26f78c6c6e5bc3b526aedde23084aee045fca50`  
		Last Modified: Tue, 18 Nov 2025 06:51:32 GMT  
		Size: 43.7 MB (43655142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6873e98f8cd6eb50b36fcc8227e34ff5c453ea8ec1cc22c3a0ee37635dff27fe`  
		Last Modified: Tue, 18 Nov 2025 06:51:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239703040732db39fde643721f71e2f0f7d668543f1832d67338664b0445e8ad`  
		Last Modified: Tue, 18 Nov 2025 06:51:27 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a93dd8d7c2a4fdb21c07aeacd52c4a872f50723d89a011dec9f9ab167f48db`  
		Last Modified: Tue, 18 Nov 2025 06:51:27 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:b073b12164ecc52b23b3ccce51b200d012ad34d3cc772ce3b7682497d9bbf217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0ee7d0d1c11f02061e4e307534da47d2ff995e635fbffe161d45539d10bf79`

```dockerfile
```

-	Layers:
	-	`sha256:b9ff1d94d03f470005dec62ab3b00a26f2d297cbc7e8941566f1fe1eb0549043`  
		Last Modified: Tue, 18 Nov 2025 09:21:03 GMT  
		Size: 5.1 MB (5078620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b91416e04606ab58b984abc653ed97ceb515e21c5eb0c034b3aab9d1c7cf7ad`  
		Last Modified: Tue, 18 Nov 2025 09:21:04 GMT  
		Size: 15.5 KB (15484 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c4d1e44c2bffbb360711a142267078c409ddfe0e79460a0af4490c16757b5147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113079076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5fd97432b016ef887f963ef3ea3dca521fd54831592edb236918c91c6196c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:00:34 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 18 Nov 2025 06:00:41 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 18 Nov 2025 06:00:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:00:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 18 Nov 2025 06:00:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 06:00:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 18 Nov 2025 06:00:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:00:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 18 Nov 2025 06:00:41 GMT
USER influxdb
# Tue, 18 Nov 2025 06:00:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:00:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e34ec02293f88935df799c3b6efaea5693c33b00f09b88401e7675ab973e60`  
		Last Modified: Tue, 18 Nov 2025 06:01:06 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca47f57f85921dc534feb3b0f295009dc86f22b574478b9e228f02db985e008`  
		Last Modified: Tue, 18 Nov 2025 06:01:12 GMT  
		Size: 41.1 MB (41118708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf065288802b5e66cc0074df18c8023601bf8797e018d7a0cc758cdde346a93`  
		Last Modified: Tue, 18 Nov 2025 06:01:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7575a9c39c5ea58ec78a0cd832a16a9adae2268896b8a028c157c038d988067`  
		Last Modified: Tue, 18 Nov 2025 06:01:06 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a929091c56f1757b395c6554b04c53f4b3ccdf5c66c2850604b37dc0d1c029fa`  
		Last Modified: Tue, 18 Nov 2025 06:01:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:1b07fb30c00a770809c8414c838579ce2bbb0a673d15c7b3a5de96098fc9ee29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c844325b9cf72787ab9c4880782548c1a3695ee6b2ec8383dd8b522b9ac9ae4`

```dockerfile
```

-	Layers:
	-	`sha256:99d829cba51ea3d72ad78377ef1fd1b9658b1306833876fc81a65b90c97f367a`  
		Last Modified: Tue, 18 Nov 2025 06:25:09 GMT  
		Size: 5.1 MB (5078085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9f0ba3a161b9a50ae653b4375140218c993157aaa7e8a13acb3b84cbe6b8cb4`  
		Last Modified: Tue, 18 Nov 2025 06:25:09 GMT  
		Size: 15.6 KB (15581 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-alpine`

```console
$ docker pull influxdb@sha256:9bb0359a467ca7b5c184a717ae2c82f04e445afa639aa4d4929fc92900321b77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:48f02098c2e15b7148d5b0452a712bffc11409db9f3ffef5cd047afc6fcbbd86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42924335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd87858dca357f6e0d56e0a56ce27b47c250fffde09e3dff67f271a6ad895f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c266adf412b1887190bc0baa2363569b9d17f4e6d5ef01303411eeece661fe2`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 1.2 MB (1224596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2286d3bdb9b240a8e73a50cc45ff08cac484d9bd916b7c2731d29c6781731f1`  
		Last Modified: Wed, 08 Oct 2025 23:10:32 GMT  
		Size: 38.1 MB (38069965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd812bdffaf5a51fdc5ad2690ccb55dec4a092395243bf366e01cf45511ac7`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccae7d91ef8bb0ea37a95450db36eaa796c974b09f7a0589106acf87072085a`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 1.0 KB (1004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce755337386479f3084609d415719dae3d4f17e49deeb6a099a77ddeca8e2cb`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e2d3d495f76618c744d89e0710cd06db610e65e6019e022899e6a4de4fc2e2`  
		Last Modified: Wed, 08 Oct 2025 23:10:25 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fa2d956e3f54c6a408c1f5844bf99a56f23140b31f97da560a8f5eb12da7bddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.4 KB (760359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8057230e97272f215cdf8d5d7c57b1a6ab77033334af884fc23310fb7652f99`

```dockerfile
```

-	Layers:
	-	`sha256:310a89661a2fc7900bdde751ff701074d5950205f4b15a793563694b2d2d013f`  
		Last Modified: Thu, 09 Oct 2025 02:20:19 GMT  
		Size: 742.5 KB (742482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c6fe293831b00cc186f0ab8fd0030085d57e84e8eeb22c232095ac36d6ccd8`  
		Last Modified: Thu, 09 Oct 2025 02:20:19 GMT  
		Size: 17.9 KB (17877 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:76c208171d828df5113ba044462bf2933fadb76114351a273eeb8cd5cdb4fd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40942247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a57d65ac967a56f76b479c24877794c880ecede170f3fe1259774dff1d98b69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f28be0243b3bb965b6c9b2e07c70b019eb69070fb075e2cc8660b856e4efba`  
		Last Modified: Wed, 08 Oct 2025 21:55:23 GMT  
		Size: 1.3 MB (1304645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f38f6a643f7a256b8eaf81222d2fb2520d2be7423f755c8fa2624e6324abf87`  
		Last Modified: Wed, 08 Oct 2025 21:55:25 GMT  
		Size: 35.5 MB (35545508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbc3962e590201f79eb734b9201590ddc739436a716accc9e14fb795530a3aa`  
		Last Modified: Wed, 08 Oct 2025 21:55:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7483ae23f176c3e011cc9c62d96dc29c2b740b7113fe61fb024b8c9201e25f6`  
		Last Modified: Wed, 08 Oct 2025 21:55:22 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3334a00d999c2ee2e76dd34dda278c84adead0715ce0da308c6c627e7c6e61`  
		Last Modified: Wed, 08 Oct 2025 21:55:22 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59987b4485557de9f3528ce3b0b97ae5391e16364283ca810e800de91ba5af0`  
		Last Modified: Wed, 08 Oct 2025 21:55:22 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:bad00ca3dd4f80fb8c42eef78284b891a27277bb112cd9a2028841c0fee80707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.7 KB (759696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e822c342492bed1b5c9e1f180e332588366ece7da2b01ca6523ba5d9cbdeaf43`

```dockerfile
```

-	Layers:
	-	`sha256:2bbf5af7d695b365d53f9e9e0967e03275a14f77264f696ccb72a7b0a5d9de27`  
		Last Modified: Wed, 08 Oct 2025 23:20:22 GMT  
		Size: 741.7 KB (741709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a79558e16dbe151165e5e7ba57ab7f1e7e4b481fd539ff01a4ba11dc4c7e52`  
		Last Modified: Wed, 08 Oct 2025 23:20:23 GMT  
		Size: 18.0 KB (17987 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:12d0520d7a971d348d9b788f9c720a78031faaadd24be46120345298c0d4204d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:69322361283759c84ec00fb4c08c0a47e1bf089f829de64c1cdc76368a607a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114681033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df5d0f123abb667728feba396018436f9c1929fd03d5024bfe4d4ad659f6056`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:51:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 06:51:12 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 18 Nov 2025 06:51:12 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 18 Nov 2025 06:51:12 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 18 Nov 2025 06:51:12 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 06:51:12 GMT
VOLUME [/var/lib/influxdb]
# Tue, 18 Nov 2025 06:51:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:51:12 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 18 Nov 2025 06:51:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:51:12 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e897a00b8ad82d0bb7c3adf4b471ef87ff147e8b58b63b36d5a5aa9a10799176`  
		Last Modified: Tue, 18 Nov 2025 06:51:33 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533a66f0ea906c15cf815b4f3506a1482c46ebbefa486f6a8d583a6f296fb29f`  
		Last Modified: Tue, 18 Nov 2025 06:51:36 GMT  
		Size: 42.2 MB (42165709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3c4c01a515cebd113c5abacd505ad34c8ea0bcc1ac7bf2a6762ca5697f2d1e`  
		Last Modified: Tue, 18 Nov 2025 06:51:33 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d670e3fdaa5fd8b14d152e37724c0cb5253ec2a7c99575ab5e62dbaf7307e870`  
		Last Modified: Tue, 18 Nov 2025 06:51:33 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a89a14105d1c1f267b1c17452d1eab53c0da7a2be7026ebe8805f6597412276`  
		Last Modified: Tue, 18 Nov 2025 06:51:33 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:e53e93f6bd71bf2a8e36dbdd6968e06b9d7a31e16fee98516261fb5c58a2cf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4698428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20bf738415a96a355642a4b1c1f7e365e4969348860744c25b153a1fcbbb82b`

```dockerfile
```

-	Layers:
	-	`sha256:d08c99119f2424122250a8479a13bacb0a17508755d5efe6c978befb06a4ad1f`  
		Last Modified: Tue, 18 Nov 2025 09:21:08 GMT  
		Size: 4.7 MB (4683763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7021d2495ce5bf70b95f004fcb448e36e53d4ab4a3449be4b522c903dbdb91`  
		Last Modified: Tue, 18 Nov 2025 09:21:09 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:7d22b120047d2262986edb6e3fc053cf7bd34118239f4bc4843f4dd9541dacca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e19598cc857486b7eb06bd5b360851040766115ed76d0c619905728a5fb45244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46959618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706cdd4b67ccf9beb18d1345a260789466ed4d29b5324f0dc892f55571615da4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 30 Sep 2025 13:56:01 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b7c681266c61781b5e9483f43fa6ad59b0acafe3c400aa10ba1e43ec0963a0`  
		Last Modified: Wed, 08 Oct 2025 23:10:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b114d197f0b29a6932d8b9d445b0628a19b4157668f6eb76571600ecaf25723`  
		Last Modified: Wed, 08 Oct 2025 23:10:23 GMT  
		Size: 1.2 MB (1224592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3358124fd2820053c690bcf986afef42d2564531fcff8ba0b814614bc23b3bbe`  
		Last Modified: Wed, 08 Oct 2025 23:10:30 GMT  
		Size: 42.1 MB (42105919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63d4466a6a2e285d8482d3dce7c47f8f5a2bbdf6c366916cfb45ea2790337a9`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e120ca154a1d12d672fecfc7212adcc4973d001dce2328028c3ab256b7f20b9`  
		Last Modified: Wed, 08 Oct 2025 23:10:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a0d8b4e8d0cf5b5a88b2dc5d203d42a530f015d833f41790286c1098b9be04`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:34ac15f902b8907e65c3ec4432f28b3de55ac12f03c7b79ed9632454675063bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.6 KB (785632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a0fd5325de66f35f4367c4e1892be82ff21cf5a48e19fabc9888a783ba6cdc`

```dockerfile
```

-	Layers:
	-	`sha256:42b8f7363028d21427e8f398bac58ecff5c02cec3eac379e0dce85371a26fb2a`  
		Last Modified: Thu, 09 Oct 2025 02:20:24 GMT  
		Size: 769.0 KB (768993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95c8c2a7537102693c04e00ab640a007908a8cdec2fa3201d77b6b835d83c362`  
		Last Modified: Thu, 09 Oct 2025 02:20:25 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:de5e99a4f2acb5150632411f4cb4f7a042d59e50692bd14c41639a69a03f9b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:81f42f0b6f323dd7417325fce8e27d62fe67a9432416f5778b9aac4557559114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91110243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d58ca3313c698a382e53165a687498384fab09a9dec7ee1657d1661c54caa6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:51:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 06:51:17 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 18 Nov 2025 06:51:17 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 18 Nov 2025 06:51:17 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 18 Nov 2025 06:51:17 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 18 Nov 2025 06:51:17 GMT
VOLUME [/var/lib/influxdb]
# Tue, 18 Nov 2025 06:51:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:51:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:51:17 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a573f5e7bc25206a564d42e9d32b4e71798ed7c9df1b77ea52e936fd1f628b`  
		Last Modified: Tue, 18 Nov 2025 06:51:33 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089b2c41f237dc4505ed6aa144c3dbb187cdee512481ef78c88993b2e41b2f14`  
		Last Modified: Tue, 18 Nov 2025 06:51:35 GMT  
		Size: 18.6 MB (18596125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd9cef287baa77b822637da8d9ca310165ee598d054ec7fc9e7d2946a2073de`  
		Last Modified: Tue, 18 Nov 2025 06:51:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0274799f37abf173991c92870e7c21f37e19ecd9cd0d653af9782c32e577196`  
		Last Modified: Tue, 18 Nov 2025 06:51:33 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:977b696cb15767fe9c4ad5cfd7450d7bbfe0646a40b0fd61166967e044d2784d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4603630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d849f039aaab0728693c5f06e58f796de89b5fe074aa2411b3961a6a19e4dd5f`

```dockerfile
```

-	Layers:
	-	`sha256:d81ff87a04274357b6e47cb0929cdbbe9c1da999c86cc40cc853e5696ad0712f`  
		Last Modified: Tue, 18 Nov 2025 09:21:14 GMT  
		Size: 4.6 MB (4590606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c418d5626429eaca69259fc4a5f83c890460130e89a383b6be87cd0f5374ff10`  
		Last Modified: Tue, 18 Nov 2025 09:21:15 GMT  
		Size: 13.0 KB (13024 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:3786c85254cdf499b874b247ec0b7fdd5ef8af5fbd719df6e5ee06f066500955
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6c020578fb9c06bd21f4356170c21bd5ef4274dc05fa08e82e63e8d94f4d3c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23402378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcd086cb1f86062412478c7ed47e21bae8a3aba6b6d2e9ea20d2fed8e1988b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 30 Sep 2025 13:56:01 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be22d087a3e55404f6a8b32177effbd6c3829e421c0b5ef02b11b38be4785b3`  
		Last Modified: Wed, 08 Oct 2025 23:10:28 GMT  
		Size: 1.2 MB (1224606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d72c9781c814dfaa052605afbb9e8d8be20811f6843ddb55b2cc0645fd96a7`  
		Last Modified: Wed, 08 Oct 2025 23:10:30 GMT  
		Size: 18.5 MB (18549871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66e2e10d6786167404e416ab04e6d4485db03583db3118244df06813625bad4`  
		Last Modified: Wed, 08 Oct 2025 23:10:28 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1362d7c20d172d913583e0a7dd8615a994bb4d5c13a7df7265d4dd009dfdbe`  
		Last Modified: Wed, 08 Oct 2025 23:10:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f5c20e593d6fa019a8d711341d1462f293da3418f4c51358c6c7711eca95aa56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 KB (691632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4aaa72e275158f64bdb7a0e14b89336f3793f64bf51dbab7320f83a05f3d8d`

```dockerfile
```

-	Layers:
	-	`sha256:0ad0a9d5310a18e73a4f13e3fe81fc690a2e3fa594fdf23fba47d3e7b5528e9f`  
		Last Modified: Thu, 09 Oct 2025 02:20:30 GMT  
		Size: 676.6 KB (676622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24dde11f34792d696d7baefa980d47a9bb0ec06c1640475e5f37e93aa05a49ae`  
		Last Modified: Thu, 09 Oct 2025 02:20:30 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8`

```console
$ docker pull influxdb@sha256:36c2374e78efeaca24a2bfed44afbd6871cf84d8108b2e70fee2c802fe64b970
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:c2b366b430f98e0194e16cf4f67cc7390de65deffa0ca61034d3ce37ef198c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116168161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a06c938f78256db0353879791f56034e0d1a8b95014f7aa0a5dbcaa2ba24fa3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:50:58 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 18 Nov 2025 06:51:06 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 18 Nov 2025 06:51:06 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:51:06 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 18 Nov 2025 06:51:06 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 06:51:06 GMT
VOLUME [/var/lib/influxdb]
# Tue, 18 Nov 2025 06:51:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:51:06 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 18 Nov 2025 06:51:06 GMT
USER influxdb
# Tue, 18 Nov 2025 06:51:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:51:06 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e79607692bfb29cca325f2e4292c2e3d9edf3581a2efc5c68c2f711d5f2c88a`  
		Last Modified: Tue, 18 Nov 2025 06:51:27 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7b788e35df5dd6d4a5af8bd26f78c6c6e5bc3b526aedde23084aee045fca50`  
		Last Modified: Tue, 18 Nov 2025 06:51:32 GMT  
		Size: 43.7 MB (43655142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6873e98f8cd6eb50b36fcc8227e34ff5c453ea8ec1cc22c3a0ee37635dff27fe`  
		Last Modified: Tue, 18 Nov 2025 06:51:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239703040732db39fde643721f71e2f0f7d668543f1832d67338664b0445e8ad`  
		Last Modified: Tue, 18 Nov 2025 06:51:27 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a93dd8d7c2a4fdb21c07aeacd52c4a872f50723d89a011dec9f9ab167f48db`  
		Last Modified: Tue, 18 Nov 2025 06:51:27 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:b073b12164ecc52b23b3ccce51b200d012ad34d3cc772ce3b7682497d9bbf217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0ee7d0d1c11f02061e4e307534da47d2ff995e635fbffe161d45539d10bf79`

```dockerfile
```

-	Layers:
	-	`sha256:b9ff1d94d03f470005dec62ab3b00a26f2d297cbc7e8941566f1fe1eb0549043`  
		Last Modified: Tue, 18 Nov 2025 09:21:03 GMT  
		Size: 5.1 MB (5078620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b91416e04606ab58b984abc653ed97ceb515e21c5eb0c034b3aab9d1c7cf7ad`  
		Last Modified: Tue, 18 Nov 2025 09:21:04 GMT  
		Size: 15.5 KB (15484 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c4d1e44c2bffbb360711a142267078c409ddfe0e79460a0af4490c16757b5147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113079076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5fd97432b016ef887f963ef3ea3dca521fd54831592edb236918c91c6196c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:00:34 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 18 Nov 2025 06:00:41 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 18 Nov 2025 06:00:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:00:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 18 Nov 2025 06:00:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 06:00:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 18 Nov 2025 06:00:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:00:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 18 Nov 2025 06:00:41 GMT
USER influxdb
# Tue, 18 Nov 2025 06:00:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:00:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e34ec02293f88935df799c3b6efaea5693c33b00f09b88401e7675ab973e60`  
		Last Modified: Tue, 18 Nov 2025 06:01:06 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca47f57f85921dc534feb3b0f295009dc86f22b574478b9e228f02db985e008`  
		Last Modified: Tue, 18 Nov 2025 06:01:12 GMT  
		Size: 41.1 MB (41118708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf065288802b5e66cc0074df18c8023601bf8797e018d7a0cc758cdde346a93`  
		Last Modified: Tue, 18 Nov 2025 06:01:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7575a9c39c5ea58ec78a0cd832a16a9adae2268896b8a028c157c038d988067`  
		Last Modified: Tue, 18 Nov 2025 06:01:06 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a929091c56f1757b395c6554b04c53f4b3ccdf5c66c2850604b37dc0d1c029fa`  
		Last Modified: Tue, 18 Nov 2025 06:01:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:1b07fb30c00a770809c8414c838579ce2bbb0a673d15c7b3a5de96098fc9ee29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c844325b9cf72787ab9c4880782548c1a3695ee6b2ec8383dd8b522b9ac9ae4`

```dockerfile
```

-	Layers:
	-	`sha256:99d829cba51ea3d72ad78377ef1fd1b9658b1306833876fc81a65b90c97f367a`  
		Last Modified: Tue, 18 Nov 2025 06:25:09 GMT  
		Size: 5.1 MB (5078085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9f0ba3a161b9a50ae653b4375140218c993157aaa7e8a13acb3b84cbe6b8cb4`  
		Last Modified: Tue, 18 Nov 2025 06:25:09 GMT  
		Size: 15.6 KB (15581 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-alpine`

```console
$ docker pull influxdb@sha256:9bb0359a467ca7b5c184a717ae2c82f04e445afa639aa4d4929fc92900321b77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:48f02098c2e15b7148d5b0452a712bffc11409db9f3ffef5cd047afc6fcbbd86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42924335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd87858dca357f6e0d56e0a56ce27b47c250fffde09e3dff67f271a6ad895f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c266adf412b1887190bc0baa2363569b9d17f4e6d5ef01303411eeece661fe2`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 1.2 MB (1224596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2286d3bdb9b240a8e73a50cc45ff08cac484d9bd916b7c2731d29c6781731f1`  
		Last Modified: Wed, 08 Oct 2025 23:10:32 GMT  
		Size: 38.1 MB (38069965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd812bdffaf5a51fdc5ad2690ccb55dec4a092395243bf366e01cf45511ac7`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccae7d91ef8bb0ea37a95450db36eaa796c974b09f7a0589106acf87072085a`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 1.0 KB (1004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce755337386479f3084609d415719dae3d4f17e49deeb6a099a77ddeca8e2cb`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e2d3d495f76618c744d89e0710cd06db610e65e6019e022899e6a4de4fc2e2`  
		Last Modified: Wed, 08 Oct 2025 23:10:25 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fa2d956e3f54c6a408c1f5844bf99a56f23140b31f97da560a8f5eb12da7bddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.4 KB (760359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8057230e97272f215cdf8d5d7c57b1a6ab77033334af884fc23310fb7652f99`

```dockerfile
```

-	Layers:
	-	`sha256:310a89661a2fc7900bdde751ff701074d5950205f4b15a793563694b2d2d013f`  
		Last Modified: Thu, 09 Oct 2025 02:20:19 GMT  
		Size: 742.5 KB (742482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c6fe293831b00cc186f0ab8fd0030085d57e84e8eeb22c232095ac36d6ccd8`  
		Last Modified: Thu, 09 Oct 2025 02:20:19 GMT  
		Size: 17.9 KB (17877 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:76c208171d828df5113ba044462bf2933fadb76114351a273eeb8cd5cdb4fd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40942247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a57d65ac967a56f76b479c24877794c880ecede170f3fe1259774dff1d98b69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f28be0243b3bb965b6c9b2e07c70b019eb69070fb075e2cc8660b856e4efba`  
		Last Modified: Wed, 08 Oct 2025 21:55:23 GMT  
		Size: 1.3 MB (1304645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f38f6a643f7a256b8eaf81222d2fb2520d2be7423f755c8fa2624e6324abf87`  
		Last Modified: Wed, 08 Oct 2025 21:55:25 GMT  
		Size: 35.5 MB (35545508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbc3962e590201f79eb734b9201590ddc739436a716accc9e14fb795530a3aa`  
		Last Modified: Wed, 08 Oct 2025 21:55:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7483ae23f176c3e011cc9c62d96dc29c2b740b7113fe61fb024b8c9201e25f6`  
		Last Modified: Wed, 08 Oct 2025 21:55:22 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3334a00d999c2ee2e76dd34dda278c84adead0715ce0da308c6c627e7c6e61`  
		Last Modified: Wed, 08 Oct 2025 21:55:22 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59987b4485557de9f3528ce3b0b97ae5391e16364283ca810e800de91ba5af0`  
		Last Modified: Wed, 08 Oct 2025 21:55:22 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:bad00ca3dd4f80fb8c42eef78284b891a27277bb112cd9a2028841c0fee80707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.7 KB (759696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e822c342492bed1b5c9e1f180e332588366ece7da2b01ca6523ba5d9cbdeaf43`

```dockerfile
```

-	Layers:
	-	`sha256:2bbf5af7d695b365d53f9e9e0967e03275a14f77264f696ccb72a7b0a5d9de27`  
		Last Modified: Wed, 08 Oct 2025 23:20:22 GMT  
		Size: 741.7 KB (741709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a79558e16dbe151165e5e7ba57ab7f1e7e4b481fd539ff01a4ba11dc4c7e52`  
		Last Modified: Wed, 08 Oct 2025 23:20:23 GMT  
		Size: 18.0 KB (17987 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-data`

```console
$ docker pull influxdb@sha256:12d0520d7a971d348d9b788f9c720a78031faaadd24be46120345298c0d4204d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:69322361283759c84ec00fb4c08c0a47e1bf089f829de64c1cdc76368a607a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114681033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df5d0f123abb667728feba396018436f9c1929fd03d5024bfe4d4ad659f6056`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:51:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 06:51:12 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 18 Nov 2025 06:51:12 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 18 Nov 2025 06:51:12 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 18 Nov 2025 06:51:12 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 06:51:12 GMT
VOLUME [/var/lib/influxdb]
# Tue, 18 Nov 2025 06:51:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:51:12 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 18 Nov 2025 06:51:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:51:12 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e897a00b8ad82d0bb7c3adf4b471ef87ff147e8b58b63b36d5a5aa9a10799176`  
		Last Modified: Tue, 18 Nov 2025 06:51:33 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533a66f0ea906c15cf815b4f3506a1482c46ebbefa486f6a8d583a6f296fb29f`  
		Last Modified: Tue, 18 Nov 2025 06:51:36 GMT  
		Size: 42.2 MB (42165709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3c4c01a515cebd113c5abacd505ad34c8ea0bcc1ac7bf2a6762ca5697f2d1e`  
		Last Modified: Tue, 18 Nov 2025 06:51:33 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d670e3fdaa5fd8b14d152e37724c0cb5253ec2a7c99575ab5e62dbaf7307e870`  
		Last Modified: Tue, 18 Nov 2025 06:51:33 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a89a14105d1c1f267b1c17452d1eab53c0da7a2be7026ebe8805f6597412276`  
		Last Modified: Tue, 18 Nov 2025 06:51:33 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:e53e93f6bd71bf2a8e36dbdd6968e06b9d7a31e16fee98516261fb5c58a2cf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4698428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20bf738415a96a355642a4b1c1f7e365e4969348860744c25b153a1fcbbb82b`

```dockerfile
```

-	Layers:
	-	`sha256:d08c99119f2424122250a8479a13bacb0a17508755d5efe6c978befb06a4ad1f`  
		Last Modified: Tue, 18 Nov 2025 09:21:08 GMT  
		Size: 4.7 MB (4683763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7021d2495ce5bf70b95f004fcb448e36e53d4ab4a3449be4b522c903dbdb91`  
		Last Modified: Tue, 18 Nov 2025 09:21:09 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-data-alpine`

```console
$ docker pull influxdb@sha256:7d22b120047d2262986edb6e3fc053cf7bd34118239f4bc4843f4dd9541dacca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e19598cc857486b7eb06bd5b360851040766115ed76d0c619905728a5fb45244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46959618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706cdd4b67ccf9beb18d1345a260789466ed4d29b5324f0dc892f55571615da4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 30 Sep 2025 13:56:01 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b7c681266c61781b5e9483f43fa6ad59b0acafe3c400aa10ba1e43ec0963a0`  
		Last Modified: Wed, 08 Oct 2025 23:10:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b114d197f0b29a6932d8b9d445b0628a19b4157668f6eb76571600ecaf25723`  
		Last Modified: Wed, 08 Oct 2025 23:10:23 GMT  
		Size: 1.2 MB (1224592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3358124fd2820053c690bcf986afef42d2564531fcff8ba0b814614bc23b3bbe`  
		Last Modified: Wed, 08 Oct 2025 23:10:30 GMT  
		Size: 42.1 MB (42105919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63d4466a6a2e285d8482d3dce7c47f8f5a2bbdf6c366916cfb45ea2790337a9`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e120ca154a1d12d672fecfc7212adcc4973d001dce2328028c3ab256b7f20b9`  
		Last Modified: Wed, 08 Oct 2025 23:10:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a0d8b4e8d0cf5b5a88b2dc5d203d42a530f015d833f41790286c1098b9be04`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:34ac15f902b8907e65c3ec4432f28b3de55ac12f03c7b79ed9632454675063bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.6 KB (785632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a0fd5325de66f35f4367c4e1892be82ff21cf5a48e19fabc9888a783ba6cdc`

```dockerfile
```

-	Layers:
	-	`sha256:42b8f7363028d21427e8f398bac58ecff5c02cec3eac379e0dce85371a26fb2a`  
		Last Modified: Thu, 09 Oct 2025 02:20:24 GMT  
		Size: 769.0 KB (768993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95c8c2a7537102693c04e00ab640a007908a8cdec2fa3201d77b6b835d83c362`  
		Last Modified: Thu, 09 Oct 2025 02:20:25 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-meta`

```console
$ docker pull influxdb@sha256:de5e99a4f2acb5150632411f4cb4f7a042d59e50692bd14c41639a69a03f9b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:81f42f0b6f323dd7417325fce8e27d62fe67a9432416f5778b9aac4557559114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91110243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d58ca3313c698a382e53165a687498384fab09a9dec7ee1657d1661c54caa6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:51:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 06:51:17 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 18 Nov 2025 06:51:17 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 18 Nov 2025 06:51:17 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 18 Nov 2025 06:51:17 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 18 Nov 2025 06:51:17 GMT
VOLUME [/var/lib/influxdb]
# Tue, 18 Nov 2025 06:51:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:51:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:51:17 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a573f5e7bc25206a564d42e9d32b4e71798ed7c9df1b77ea52e936fd1f628b`  
		Last Modified: Tue, 18 Nov 2025 06:51:33 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089b2c41f237dc4505ed6aa144c3dbb187cdee512481ef78c88993b2e41b2f14`  
		Last Modified: Tue, 18 Nov 2025 06:51:35 GMT  
		Size: 18.6 MB (18596125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd9cef287baa77b822637da8d9ca310165ee598d054ec7fc9e7d2946a2073de`  
		Last Modified: Tue, 18 Nov 2025 06:51:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0274799f37abf173991c92870e7c21f37e19ecd9cd0d653af9782c32e577196`  
		Last Modified: Tue, 18 Nov 2025 06:51:33 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:977b696cb15767fe9c4ad5cfd7450d7bbfe0646a40b0fd61166967e044d2784d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4603630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d849f039aaab0728693c5f06e58f796de89b5fe074aa2411b3961a6a19e4dd5f`

```dockerfile
```

-	Layers:
	-	`sha256:d81ff87a04274357b6e47cb0929cdbbe9c1da999c86cc40cc853e5696ad0712f`  
		Last Modified: Tue, 18 Nov 2025 09:21:14 GMT  
		Size: 4.6 MB (4590606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c418d5626429eaca69259fc4a5f83c890460130e89a383b6be87cd0f5374ff10`  
		Last Modified: Tue, 18 Nov 2025 09:21:15 GMT  
		Size: 13.0 KB (13024 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-meta-alpine`

```console
$ docker pull influxdb@sha256:3786c85254cdf499b874b247ec0b7fdd5ef8af5fbd719df6e5ee06f066500955
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6c020578fb9c06bd21f4356170c21bd5ef4274dc05fa08e82e63e8d94f4d3c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23402378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcd086cb1f86062412478c7ed47e21bae8a3aba6b6d2e9ea20d2fed8e1988b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 30 Sep 2025 13:56:01 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be22d087a3e55404f6a8b32177effbd6c3829e421c0b5ef02b11b38be4785b3`  
		Last Modified: Wed, 08 Oct 2025 23:10:28 GMT  
		Size: 1.2 MB (1224606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d72c9781c814dfaa052605afbb9e8d8be20811f6843ddb55b2cc0645fd96a7`  
		Last Modified: Wed, 08 Oct 2025 23:10:30 GMT  
		Size: 18.5 MB (18549871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66e2e10d6786167404e416ab04e6d4485db03583db3118244df06813625bad4`  
		Last Modified: Wed, 08 Oct 2025 23:10:28 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1362d7c20d172d913583e0a7dd8615a994bb4d5c13a7df7265d4dd009dfdbe`  
		Last Modified: Wed, 08 Oct 2025 23:10:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f5c20e593d6fa019a8d711341d1462f293da3418f4c51358c6c7711eca95aa56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 KB (691632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4aaa72e275158f64bdb7a0e14b89336f3793f64bf51dbab7320f83a05f3d8d`

```dockerfile
```

-	Layers:
	-	`sha256:0ad0a9d5310a18e73a4f13e3fe81fc690a2e3fa594fdf23fba47d3e7b5528e9f`  
		Last Modified: Thu, 09 Oct 2025 02:20:30 GMT  
		Size: 676.6 KB (676622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24dde11f34792d696d7baefa980d47a9bb0ec06c1640475e5f37e93aa05a49ae`  
		Last Modified: Thu, 09 Oct 2025 02:20:30 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12`

```console
$ docker pull influxdb@sha256:83e76fb736adb376893be7d8024afbb853f2d81ce845ddcace0dfa28934631f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12` - linux; amd64

```console
$ docker pull influxdb@sha256:a62c78a6982f3d28da8869a30c0d40f3d34de615a52a42fc34d262cbf782d70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113843375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51a7cb240e005b9cdee4fc86a1008a385f27a1835e6ec31c03873e22ccf1533`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:49:06 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 18 Nov 2025 06:49:12 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 18 Nov 2025 06:49:12 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:49:12 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 18 Nov 2025 06:49:12 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 06:49:12 GMT
VOLUME [/var/lib/influxdb]
# Tue, 18 Nov 2025 06:49:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:49:12 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 18 Nov 2025 06:49:12 GMT
USER influxdb
# Tue, 18 Nov 2025 06:49:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:49:12 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d2861080fd4adc2076fca4363e8fb923e950892f91f293a49ebe9d9bc8c50e`  
		Last Modified: Tue, 18 Nov 2025 06:49:30 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c47460bb9088b3e5eec58761077024e3f3e88bd40aa9e0d56c2552a9a2da81`  
		Last Modified: Tue, 18 Nov 2025 06:49:34 GMT  
		Size: 41.3 MB (41330355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9fd32dda21e674757c2cec8ea06c8f793b35792219b568aa888aee1d21ab35`  
		Last Modified: Tue, 18 Nov 2025 06:49:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab298d476392be3bb09ffe26937bf959d3d7c90755b564a14be9f5da7738e76`  
		Last Modified: Tue, 18 Nov 2025 06:49:30 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49090fd9b91cbdbd4cd3b13d8ad7a60da3cd2520d2cbc4fbc1f61d195540c2c5`  
		Last Modified: Tue, 18 Nov 2025 06:49:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:e3bf56d81a5f6cdb75645d92cbeaeebb2033a30a2f52ce754fb48c618fbaaf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1805b79bc4b21982c7bbaa5338abd76c005e13b295457331acf5d921c6ea6902`

```dockerfile
```

-	Layers:
	-	`sha256:5479dc750475651b7f4ca9770cab2e587f805c17e69aa11edd33f3e3e3a37d3d`  
		Last Modified: Tue, 18 Nov 2025 09:21:28 GMT  
		Size: 4.7 MB (4675813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6bf2f2b1005be9d0e2519a4120525289d12b5cef6bcc93d44a2ce4ae83256b0`  
		Last Modified: Tue, 18 Nov 2025 09:21:28 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a763173f998932a7aaf14756f359a9a93147850c05029d7992b26cd2d59f6c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110091216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc871f9b14da79753bfe9d7accf1800146c26f49a00b30439acaf3385077e3e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:59:56 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 18 Nov 2025 06:00:02 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 18 Nov 2025 06:00:02 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:00:02 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 18 Nov 2025 06:00:02 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 06:00:02 GMT
VOLUME [/var/lib/influxdb]
# Tue, 18 Nov 2025 06:00:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:00:02 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 18 Nov 2025 06:00:02 GMT
USER influxdb
# Tue, 18 Nov 2025 06:00:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:00:02 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24f8949d25ec7ac87a513d2ed8f70629382b5837fb819a267bca1e47ac4ef55`  
		Last Modified: Tue, 18 Nov 2025 06:00:25 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5f94cf9e554266f586ec46b0b73187409ff68c6990e4da7c8eac9e535b492c`  
		Last Modified: Tue, 18 Nov 2025 06:00:28 GMT  
		Size: 38.1 MB (38130845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef702c917a04dd40019954e04f0c4f909f74a53992872c51f41de6093a540b0`  
		Last Modified: Tue, 18 Nov 2025 06:00:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f331207af0a2271a1a262f39fe3a8714b8a6b8ec5efbd1f83dc38c06c61d64ad`  
		Last Modified: Tue, 18 Nov 2025 06:00:25 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a04a8e313d7a27f97b0cbe227033881c86916251b9c3598179ec0e403582fd`  
		Last Modified: Tue, 18 Nov 2025 06:00:25 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:ce1bda9392e9ecde99fbae5d135dec8c7e0a72a68fc220fddeb69ef59dc1f831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4691822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b99f5cd11aeca404336482ea6ad1fb26a0004d3c2049aff516091d9645a4b8`

```dockerfile
```

-	Layers:
	-	`sha256:774da3039c5daf9e449e2289de48327c7b2fa0d40302a066c3e7684b40eab17b`  
		Last Modified: Tue, 18 Nov 2025 06:25:20 GMT  
		Size: 4.7 MB (4675271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e22af8c5bb05b8fadb84f41cb86ca8329a86e962b45ce3e8aed228b3440503d3`  
		Last Modified: Tue, 18 Nov 2025 06:25:21 GMT  
		Size: 16.6 KB (16551 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-alpine`

```console
$ docker pull influxdb@sha256:9be6bb8f77c1401e77aca7a95487763c74ceb9e7c969c7d53d8b195a833e3f97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:693d5e087aebfa80ada39aab693673e0006fb092759889dc89a1c22de3d10a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46122314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4580b750c0220e5f38c52cbcaf2a62c48c9110319d6ec9a2d395a04c9b4ff0cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833a534ae7d9b744b01293824d76272ab350ec43a3ea6e2461ff7af8abc50a6a`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 1.2 MB (1225336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c347910584b08baf1a48bdf46c5c50dd24038eb1302b7007f31ce71bc927b592`  
		Last Modified: Wed, 08 Oct 2025 23:09:38 GMT  
		Size: 41.3 MB (41251703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a935c4d2c88a22b2b988a0ccac55421ea76be53d52269f7b632dcf92c515813`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a53405a7e90893d67726045e12be0b8d6c77efc4329d83b02742c7dc703c64`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 993.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559f188f2dcf26e5cc25cbe55a6ec7068097f6735e694bf00a27874305fe66fa`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd7a2e4b50b127938200eed101e836d8f93fbdeeeb0d43f571a379f42a5173`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e81e0d6fcdd78898b7d541628dd5f046c11ade938248deb9bfbab0239e111139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **780.5 KB (780522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062a1e459573f824fd571b3df5adc062fdf691d6b759359c318fc1e4a6f81b99`

```dockerfile
```

-	Layers:
	-	`sha256:5e2652a38eb252eea390f6eb8de70303b2ba32a60a44d0115cc4d95141919caf`  
		Last Modified: Thu, 09 Oct 2025 02:20:56 GMT  
		Size: 761.9 KB (761859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efdc33ff6b4a8b7da52daf4a11c7f9b03b3ba5c78a7c13b748b4e02199fa9284`  
		Last Modified: Thu, 09 Oct 2025 02:20:57 GMT  
		Size: 18.7 KB (18663 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:5da40eb9360fc4761f3503754e978c35db477788533b175a879b3a062c910c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43344488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1669f3cf5d1d56aa7ff084652faf747d2bd3c1d4f6f6971b1438c471cc34e74a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3778cd6b7947fa40773e4d96fb04b28656fd002578dc1ba35152916dba4eab3`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 1.3 MB (1290589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193f43b6c8619cf1483f881f1bdef6dd939ea58e7d495e8416bfda3d15d098c2`  
		Last Modified: Wed, 08 Oct 2025 21:55:08 GMT  
		Size: 38.1 MB (38058839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a6f8e76e4d9c33472e64d72f702c7962ba0b5e4d61db1c648411752212f71`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31e522d0a6aa09c893a40e88167d5532ce096d84694b5970672f058e64bc5d6`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 990.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf7f3756e6d6b4556e7f0ff09c0a747d1b2defff34996459ba9c9fe8623c697`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70fba9b3a8b84fe1ceeacd36df99e6d838298f829348550376de111eaa260c5`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:16b60655d76eb0ee04a4cf31a1dbf45f8b8d2645b730d3ed43ad5ddc9b659b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.9 KB (779859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc24c010c052da3fc8e1ef47a608b08adad9afd5df78f43ec7f7e4052f6c8a1`

```dockerfile
```

-	Layers:
	-	`sha256:191b261bcac32e145613440ef72800622e01c14fb6dc6411b1728ac3dedcb34d`  
		Last Modified: Wed, 08 Oct 2025 23:20:31 GMT  
		Size: 761.1 KB (761088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ee247e175c8dccb7cd34515f34b1749a76fd37134eef6a64643a3885004fe1`  
		Last Modified: Wed, 08 Oct 2025 23:20:32 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-data`

```console
$ docker pull influxdb@sha256:89d025ac5e1373e0eae7831852940d719d39fc890557e5f88a49263561d6b549
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data` - linux; amd64

```console
$ docker pull influxdb@sha256:a20f9b64e2f8e1849fb42287de6e35ef777cae325d621dfc9aad1a4681f59314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114827563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a70b1e535216d32ded6e6f7e2560897a46ad2414d125f54f91aae581698e1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:49:59 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 18 Nov 2025 06:49:59 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:49:59 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 18 Nov 2025 06:49:59 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 06:49:59 GMT
VOLUME [/var/lib/influxdb]
# Tue, 18 Nov 2025 06:49:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:49:59 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 18 Nov 2025 06:49:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:49:59 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80176754e0b662719d98b25cfa05d4d6f94db6792734146f00af52215e297bc3`  
		Last Modified: Tue, 18 Nov 2025 06:50:20 GMT  
		Size: 42.3 MB (42315681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34444ff2529a08e5581159f5705243122b93e619a31b79e25220f6abb076c304`  
		Last Modified: Tue, 18 Nov 2025 06:50:18 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ded10728dd245ee6bbaa1f6c9bfe1d390521bfea3dc0b3ac9ca0ce77fbb7ac`  
		Last Modified: Tue, 18 Nov 2025 06:50:17 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96473e42386f401d412e0f395fb9e382ecc89d5a1cb2b4fdff5ad769d070a95`  
		Last Modified: Tue, 18 Nov 2025 06:50:18 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:ca6d1ee0e7d0d8833642ac2266d246a01bb13a408ee5e1ff85f3a98e6e6de59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8eed35f2d75ecdbd07ea53654b92d16ab26a694af225712d84766545c8c4721`

```dockerfile
```

-	Layers:
	-	`sha256:0c731439e967bb042745e166dde4413bf753f1fe5be0bed30478e68210a1da48`  
		Last Modified: Tue, 18 Nov 2025 09:21:31 GMT  
		Size: 4.7 MB (4685451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250cbebb5ae1be08a9072acacc602a3baa8bd59ebac0676c4869b734c09bbb2f`  
		Last Modified: Tue, 18 Nov 2025 09:21:33 GMT  
		Size: 13.8 KB (13779 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-data-alpine`

```console
$ docker pull influxdb@sha256:ce2ffe52a626e318a7eb9a37591b2dab8918b4b9a2db82d40376d10f49ec655c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a9119ce752787d7bc02d05b19c71cf1c52c3ec36e7d53ffac794bc9e9e856105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47123983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778a4ce21945169b3579e3c00ae06210f014bbaa4c94491ed2d6813ee148bdce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a3788b43dae292831ae0448a5ed504046ffa71fe7a9f09db40713951fbf944`  
		Last Modified: Wed, 08 Oct 2025 23:10:06 GMT  
		Size: 1.2 MB (1225329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e0170f82fea093122d3570e0d358e936d1db98ed05a0d6a48d33037501b351`  
		Last Modified: Wed, 08 Oct 2025 23:10:13 GMT  
		Size: 42.3 MB (42254311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b0661d8dbfc3b43d49ec386e18c197ae353dd5d5c77c548207da941ba2ee68`  
		Last Modified: Wed, 08 Oct 2025 23:10:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39225506d3b8f10fd5e6623059b8c1e0d7efadec626f71dcf9da78fee4f7e2a`  
		Last Modified: Wed, 08 Oct 2025 23:10:06 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d72d987f87daa2925154010870639046590c11fa247eb8c38fdd2ea9c6094b`  
		Last Modified: Wed, 08 Oct 2025 23:10:06 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f218c7220d82f4546bb998858096a34a8dfce6b65860ed72b6874ed1b0a3eb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **791.0 KB (791001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e3605d003749db319aa7f2e79a5cb86a94e980bcb7a857759a1dc3a916e76d`

```dockerfile
```

-	Layers:
	-	`sha256:6aeb326ff9d4e15849772b799e87c132f6edf8dcdfacc3879b8fb8f19a22fca9`  
		Last Modified: Thu, 09 Oct 2025 02:20:47 GMT  
		Size: 775.8 KB (775810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f65ff52ae85ef9fa76b501b5f6ab0974038c20801b32cc1c20d90c94d731471`  
		Last Modified: Thu, 09 Oct 2025 02:20:48 GMT  
		Size: 15.2 KB (15191 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-meta`

```console
$ docker pull influxdb@sha256:23a94a740067dfba0eeee80b44e78614ca8dd3fd282209ce04e2f33147290f5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:b84b5482beab2e44aa86d49a8dffa8ab46256d4d4ada4cdc36468d4358880571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91289695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68db4d6aedb10e640024284bc997fdaa85376019ad03e62c0b50ecccfd4148fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:50:46 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 18 Nov 2025 06:50:46 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:50:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 18 Nov 2025 06:50:46 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 18 Nov 2025 06:50:46 GMT
VOLUME [/var/lib/influxdb]
# Tue, 18 Nov 2025 06:50:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:50:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:50:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04af3d584acc058cd4bdf2362f80a238e99b80a4181a9ad6474900e7892a6c44`  
		Last Modified: Tue, 18 Nov 2025 06:51:03 GMT  
		Size: 18.8 MB (18779020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30702ecc1cbc6d3e4331149b27163d03ac371734c07a2953f9c39a910439e2a`  
		Last Modified: Tue, 18 Nov 2025 06:51:01 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5e52b220eeb5136bd80ec648a6305c14c1ceba3c64c88c250d2468529790b0`  
		Last Modified: Tue, 18 Nov 2025 06:51:01 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:8dcdb8e2742eb114784f5173c475d426afb6427ab0e8533c31a7e67b2caad643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4602907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a05d4956d4f7ef8bfbe05ba6129c68b6210aa51ced0d9456356998cfe77cf6d`

```dockerfile
```

-	Layers:
	-	`sha256:9c75ba8dab638baab0c868f24caded9d9da43a299db327b2a128a27dbb79ce38`  
		Last Modified: Tue, 18 Nov 2025 09:21:36 GMT  
		Size: 4.6 MB (4590614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:405d8e5e4484de4676b7cbba6ef468c5f1f38a476a258894ceac1d85a4660b5b`  
		Last Modified: Tue, 18 Nov 2025 09:21:37 GMT  
		Size: 12.3 KB (12293 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-meta-alpine`

```console
$ docker pull influxdb@sha256:811acdf4664b52af3f6d703e48787e2b4606ae470747606bfa84ebf6e3395179
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:eafc8ce951405cbc7907d39b292cbde2a07e4f8bb20e15f5de12110ff310c811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23590971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a57259f8ac7012ee31aebecf1b6497bcb8758c5d887d973b483ddbdbcf723da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influxd-ctl'             'influxdb-*/usr/bin/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1506a520a1ca51f516d5068e753e243431efab0ef69c7b1634e53985ce44a2`  
		Last Modified: Wed, 08 Oct 2025 23:10:05 GMT  
		Size: 1.2 MB (1225337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8df8f8e418a27917114426b3d245a3728772fe30be9e1b0b609e79b9ccb3b1d`  
		Last Modified: Wed, 08 Oct 2025 23:10:06 GMT  
		Size: 18.7 MB (18722501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96fdeefb85b445c179f78bb53968e8210d7aaa4a30cccb4d6452d9ac4a7b000`  
		Last Modified: Wed, 08 Oct 2025 23:10:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5817ad78e6b46e06d7f07b733f09a0eddd15b789d78398b86fe406d8cd2fdf7`  
		Last Modified: Wed, 08 Oct 2025 23:10:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:7df6901865ed7a906f1c751eba50de606f5f89648541f49d5c79af65530b1190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.3 KB (695336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523ace161067c6e86bd41d82cc97db7e8a4993f3da53f36d6d5629e38bee6daa`

```dockerfile
```

-	Layers:
	-	`sha256:3d4d976d2a8846a9f10e6d2d34d790872d5e7ed7b1b351117c82f8b927502399`  
		Last Modified: Thu, 09 Oct 2025 02:20:59 GMT  
		Size: 681.8 KB (681759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71c697656e9ce6a76bcb04d0f78aff32c9bc6715c511aa163637cbd6c96a2ac`  
		Last Modified: Thu, 09 Oct 2025 02:20:59 GMT  
		Size: 13.6 KB (13577 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2`

```console
$ docker pull influxdb@sha256:83e76fb736adb376893be7d8024afbb853f2d81ce845ddcace0dfa28934631f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.2` - linux; amd64

```console
$ docker pull influxdb@sha256:a62c78a6982f3d28da8869a30c0d40f3d34de615a52a42fc34d262cbf782d70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113843375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51a7cb240e005b9cdee4fc86a1008a385f27a1835e6ec31c03873e22ccf1533`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:49:06 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 18 Nov 2025 06:49:12 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 18 Nov 2025 06:49:12 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:49:12 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 18 Nov 2025 06:49:12 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 06:49:12 GMT
VOLUME [/var/lib/influxdb]
# Tue, 18 Nov 2025 06:49:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:49:12 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 18 Nov 2025 06:49:12 GMT
USER influxdb
# Tue, 18 Nov 2025 06:49:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:49:12 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d2861080fd4adc2076fca4363e8fb923e950892f91f293a49ebe9d9bc8c50e`  
		Last Modified: Tue, 18 Nov 2025 06:49:30 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c47460bb9088b3e5eec58761077024e3f3e88bd40aa9e0d56c2552a9a2da81`  
		Last Modified: Tue, 18 Nov 2025 06:49:34 GMT  
		Size: 41.3 MB (41330355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9fd32dda21e674757c2cec8ea06c8f793b35792219b568aa888aee1d21ab35`  
		Last Modified: Tue, 18 Nov 2025 06:49:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab298d476392be3bb09ffe26937bf959d3d7c90755b564a14be9f5da7738e76`  
		Last Modified: Tue, 18 Nov 2025 06:49:30 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49090fd9b91cbdbd4cd3b13d8ad7a60da3cd2520d2cbc4fbc1f61d195540c2c5`  
		Last Modified: Tue, 18 Nov 2025 06:49:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2` - unknown; unknown

```console
$ docker pull influxdb@sha256:e3bf56d81a5f6cdb75645d92cbeaeebb2033a30a2f52ce754fb48c618fbaaf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1805b79bc4b21982c7bbaa5338abd76c005e13b295457331acf5d921c6ea6902`

```dockerfile
```

-	Layers:
	-	`sha256:5479dc750475651b7f4ca9770cab2e587f805c17e69aa11edd33f3e3e3a37d3d`  
		Last Modified: Tue, 18 Nov 2025 09:21:28 GMT  
		Size: 4.7 MB (4675813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6bf2f2b1005be9d0e2519a4120525289d12b5cef6bcc93d44a2ce4ae83256b0`  
		Last Modified: Tue, 18 Nov 2025 09:21:28 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a763173f998932a7aaf14756f359a9a93147850c05029d7992b26cd2d59f6c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110091216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc871f9b14da79753bfe9d7accf1800146c26f49a00b30439acaf3385077e3e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:59:56 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 18 Nov 2025 06:00:02 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 18 Nov 2025 06:00:02 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:00:02 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 18 Nov 2025 06:00:02 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 06:00:02 GMT
VOLUME [/var/lib/influxdb]
# Tue, 18 Nov 2025 06:00:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:00:02 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 18 Nov 2025 06:00:02 GMT
USER influxdb
# Tue, 18 Nov 2025 06:00:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:00:02 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24f8949d25ec7ac87a513d2ed8f70629382b5837fb819a267bca1e47ac4ef55`  
		Last Modified: Tue, 18 Nov 2025 06:00:25 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5f94cf9e554266f586ec46b0b73187409ff68c6990e4da7c8eac9e535b492c`  
		Last Modified: Tue, 18 Nov 2025 06:00:28 GMT  
		Size: 38.1 MB (38130845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef702c917a04dd40019954e04f0c4f909f74a53992872c51f41de6093a540b0`  
		Last Modified: Tue, 18 Nov 2025 06:00:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f331207af0a2271a1a262f39fe3a8714b8a6b8ec5efbd1f83dc38c06c61d64ad`  
		Last Modified: Tue, 18 Nov 2025 06:00:25 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a04a8e313d7a27f97b0cbe227033881c86916251b9c3598179ec0e403582fd`  
		Last Modified: Tue, 18 Nov 2025 06:00:25 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2` - unknown; unknown

```console
$ docker pull influxdb@sha256:ce1bda9392e9ecde99fbae5d135dec8c7e0a72a68fc220fddeb69ef59dc1f831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4691822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b99f5cd11aeca404336482ea6ad1fb26a0004d3c2049aff516091d9645a4b8`

```dockerfile
```

-	Layers:
	-	`sha256:774da3039c5daf9e449e2289de48327c7b2fa0d40302a066c3e7684b40eab17b`  
		Last Modified: Tue, 18 Nov 2025 06:25:20 GMT  
		Size: 4.7 MB (4675271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e22af8c5bb05b8fadb84f41cb86ca8329a86e962b45ce3e8aed228b3440503d3`  
		Last Modified: Tue, 18 Nov 2025 06:25:21 GMT  
		Size: 16.6 KB (16551 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-alpine`

```console
$ docker pull influxdb@sha256:9be6bb8f77c1401e77aca7a95487763c74ceb9e7c969c7d53d8b195a833e3f97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:693d5e087aebfa80ada39aab693673e0006fb092759889dc89a1c22de3d10a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46122314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4580b750c0220e5f38c52cbcaf2a62c48c9110319d6ec9a2d395a04c9b4ff0cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833a534ae7d9b744b01293824d76272ab350ec43a3ea6e2461ff7af8abc50a6a`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 1.2 MB (1225336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c347910584b08baf1a48bdf46c5c50dd24038eb1302b7007f31ce71bc927b592`  
		Last Modified: Wed, 08 Oct 2025 23:09:38 GMT  
		Size: 41.3 MB (41251703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a935c4d2c88a22b2b988a0ccac55421ea76be53d52269f7b632dcf92c515813`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a53405a7e90893d67726045e12be0b8d6c77efc4329d83b02742c7dc703c64`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 993.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559f188f2dcf26e5cc25cbe55a6ec7068097f6735e694bf00a27874305fe66fa`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd7a2e4b50b127938200eed101e836d8f93fbdeeeb0d43f571a379f42a5173`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e81e0d6fcdd78898b7d541628dd5f046c11ade938248deb9bfbab0239e111139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **780.5 KB (780522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062a1e459573f824fd571b3df5adc062fdf691d6b759359c318fc1e4a6f81b99`

```dockerfile
```

-	Layers:
	-	`sha256:5e2652a38eb252eea390f6eb8de70303b2ba32a60a44d0115cc4d95141919caf`  
		Last Modified: Thu, 09 Oct 2025 02:20:56 GMT  
		Size: 761.9 KB (761859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efdc33ff6b4a8b7da52daf4a11c7f9b03b3ba5c78a7c13b748b4e02199fa9284`  
		Last Modified: Thu, 09 Oct 2025 02:20:57 GMT  
		Size: 18.7 KB (18663 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:5da40eb9360fc4761f3503754e978c35db477788533b175a879b3a062c910c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43344488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1669f3cf5d1d56aa7ff084652faf747d2bd3c1d4f6f6971b1438c471cc34e74a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3778cd6b7947fa40773e4d96fb04b28656fd002578dc1ba35152916dba4eab3`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 1.3 MB (1290589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193f43b6c8619cf1483f881f1bdef6dd939ea58e7d495e8416bfda3d15d098c2`  
		Last Modified: Wed, 08 Oct 2025 21:55:08 GMT  
		Size: 38.1 MB (38058839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a6f8e76e4d9c33472e64d72f702c7962ba0b5e4d61db1c648411752212f71`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31e522d0a6aa09c893a40e88167d5532ce096d84694b5970672f058e64bc5d6`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 990.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf7f3756e6d6b4556e7f0ff09c0a747d1b2defff34996459ba9c9fe8623c697`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70fba9b3a8b84fe1ceeacd36df99e6d838298f829348550376de111eaa260c5`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:16b60655d76eb0ee04a4cf31a1dbf45f8b8d2645b730d3ed43ad5ddc9b659b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.9 KB (779859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc24c010c052da3fc8e1ef47a608b08adad9afd5df78f43ec7f7e4052f6c8a1`

```dockerfile
```

-	Layers:
	-	`sha256:191b261bcac32e145613440ef72800622e01c14fb6dc6411b1728ac3dedcb34d`  
		Last Modified: Wed, 08 Oct 2025 23:20:31 GMT  
		Size: 761.1 KB (761088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ee247e175c8dccb7cd34515f34b1749a76fd37134eef6a64643a3885004fe1`  
		Last Modified: Wed, 08 Oct 2025 23:20:32 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-data`

```console
$ docker pull influxdb@sha256:89d025ac5e1373e0eae7831852940d719d39fc890557e5f88a49263561d6b549
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-data` - linux; amd64

```console
$ docker pull influxdb@sha256:a20f9b64e2f8e1849fb42287de6e35ef777cae325d621dfc9aad1a4681f59314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114827563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a70b1e535216d32ded6e6f7e2560897a46ad2414d125f54f91aae581698e1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:49:59 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 18 Nov 2025 06:49:59 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:49:59 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 18 Nov 2025 06:49:59 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 06:49:59 GMT
VOLUME [/var/lib/influxdb]
# Tue, 18 Nov 2025 06:49:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:49:59 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 18 Nov 2025 06:49:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:49:59 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80176754e0b662719d98b25cfa05d4d6f94db6792734146f00af52215e297bc3`  
		Last Modified: Tue, 18 Nov 2025 06:50:20 GMT  
		Size: 42.3 MB (42315681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34444ff2529a08e5581159f5705243122b93e619a31b79e25220f6abb076c304`  
		Last Modified: Tue, 18 Nov 2025 06:50:18 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ded10728dd245ee6bbaa1f6c9bfe1d390521bfea3dc0b3ac9ca0ce77fbb7ac`  
		Last Modified: Tue, 18 Nov 2025 06:50:17 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96473e42386f401d412e0f395fb9e382ecc89d5a1cb2b4fdff5ad769d070a95`  
		Last Modified: Tue, 18 Nov 2025 06:50:18 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:ca6d1ee0e7d0d8833642ac2266d246a01bb13a408ee5e1ff85f3a98e6e6de59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8eed35f2d75ecdbd07ea53654b92d16ab26a694af225712d84766545c8c4721`

```dockerfile
```

-	Layers:
	-	`sha256:0c731439e967bb042745e166dde4413bf753f1fe5be0bed30478e68210a1da48`  
		Last Modified: Tue, 18 Nov 2025 09:21:31 GMT  
		Size: 4.7 MB (4685451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250cbebb5ae1be08a9072acacc602a3baa8bd59ebac0676c4869b734c09bbb2f`  
		Last Modified: Tue, 18 Nov 2025 09:21:33 GMT  
		Size: 13.8 KB (13779 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-data-alpine`

```console
$ docker pull influxdb@sha256:ce2ffe52a626e318a7eb9a37591b2dab8918b4b9a2db82d40376d10f49ec655c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a9119ce752787d7bc02d05b19c71cf1c52c3ec36e7d53ffac794bc9e9e856105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47123983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778a4ce21945169b3579e3c00ae06210f014bbaa4c94491ed2d6813ee148bdce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a3788b43dae292831ae0448a5ed504046ffa71fe7a9f09db40713951fbf944`  
		Last Modified: Wed, 08 Oct 2025 23:10:06 GMT  
		Size: 1.2 MB (1225329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e0170f82fea093122d3570e0d358e936d1db98ed05a0d6a48d33037501b351`  
		Last Modified: Wed, 08 Oct 2025 23:10:13 GMT  
		Size: 42.3 MB (42254311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b0661d8dbfc3b43d49ec386e18c197ae353dd5d5c77c548207da941ba2ee68`  
		Last Modified: Wed, 08 Oct 2025 23:10:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39225506d3b8f10fd5e6623059b8c1e0d7efadec626f71dcf9da78fee4f7e2a`  
		Last Modified: Wed, 08 Oct 2025 23:10:06 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d72d987f87daa2925154010870639046590c11fa247eb8c38fdd2ea9c6094b`  
		Last Modified: Wed, 08 Oct 2025 23:10:06 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f218c7220d82f4546bb998858096a34a8dfce6b65860ed72b6874ed1b0a3eb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **791.0 KB (791001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e3605d003749db319aa7f2e79a5cb86a94e980bcb7a857759a1dc3a916e76d`

```dockerfile
```

-	Layers:
	-	`sha256:6aeb326ff9d4e15849772b799e87c132f6edf8dcdfacc3879b8fb8f19a22fca9`  
		Last Modified: Thu, 09 Oct 2025 02:20:47 GMT  
		Size: 775.8 KB (775810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f65ff52ae85ef9fa76b501b5f6ab0974038c20801b32cc1c20d90c94d731471`  
		Last Modified: Thu, 09 Oct 2025 02:20:48 GMT  
		Size: 15.2 KB (15191 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-meta`

```console
$ docker pull influxdb@sha256:23a94a740067dfba0eeee80b44e78614ca8dd3fd282209ce04e2f33147290f5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:b84b5482beab2e44aa86d49a8dffa8ab46256d4d4ada4cdc36468d4358880571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91289695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68db4d6aedb10e640024284bc997fdaa85376019ad03e62c0b50ecccfd4148fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:50:46 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 18 Nov 2025 06:50:46 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:50:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 18 Nov 2025 06:50:46 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 18 Nov 2025 06:50:46 GMT
VOLUME [/var/lib/influxdb]
# Tue, 18 Nov 2025 06:50:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:50:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 06:50:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04af3d584acc058cd4bdf2362f80a238e99b80a4181a9ad6474900e7892a6c44`  
		Last Modified: Tue, 18 Nov 2025 06:51:03 GMT  
		Size: 18.8 MB (18779020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30702ecc1cbc6d3e4331149b27163d03ac371734c07a2953f9c39a910439e2a`  
		Last Modified: Tue, 18 Nov 2025 06:51:01 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5e52b220eeb5136bd80ec648a6305c14c1ceba3c64c88c250d2468529790b0`  
		Last Modified: Tue, 18 Nov 2025 06:51:01 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:8dcdb8e2742eb114784f5173c475d426afb6427ab0e8533c31a7e67b2caad643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4602907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a05d4956d4f7ef8bfbe05ba6129c68b6210aa51ced0d9456356998cfe77cf6d`

```dockerfile
```

-	Layers:
	-	`sha256:9c75ba8dab638baab0c868f24caded9d9da43a299db327b2a128a27dbb79ce38`  
		Last Modified: Tue, 18 Nov 2025 09:21:36 GMT  
		Size: 4.6 MB (4590614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:405d8e5e4484de4676b7cbba6ef468c5f1f38a476a258894ceac1d85a4660b5b`  
		Last Modified: Tue, 18 Nov 2025 09:21:37 GMT  
		Size: 12.3 KB (12293 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-meta-alpine`

```console
$ docker pull influxdb@sha256:811acdf4664b52af3f6d703e48787e2b4606ae470747606bfa84ebf6e3395179
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:eafc8ce951405cbc7907d39b292cbde2a07e4f8bb20e15f5de12110ff310c811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23590971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a57259f8ac7012ee31aebecf1b6497bcb8758c5d887d973b483ddbdbcf723da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influxd-ctl'             'influxdb-*/usr/bin/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1506a520a1ca51f516d5068e753e243431efab0ef69c7b1634e53985ce44a2`  
		Last Modified: Wed, 08 Oct 2025 23:10:05 GMT  
		Size: 1.2 MB (1225337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8df8f8e418a27917114426b3d245a3728772fe30be9e1b0b609e79b9ccb3b1d`  
		Last Modified: Wed, 08 Oct 2025 23:10:06 GMT  
		Size: 18.7 MB (18722501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96fdeefb85b445c179f78bb53968e8210d7aaa4a30cccb4d6452d9ac4a7b000`  
		Last Modified: Wed, 08 Oct 2025 23:10:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5817ad78e6b46e06d7f07b733f09a0eddd15b789d78398b86fe406d8cd2fdf7`  
		Last Modified: Wed, 08 Oct 2025 23:10:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:7df6901865ed7a906f1c751eba50de606f5f89648541f49d5c79af65530b1190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.3 KB (695336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523ace161067c6e86bd41d82cc97db7e8a4993f3da53f36d6d5629e38bee6daa`

```dockerfile
```

-	Layers:
	-	`sha256:3d4d976d2a8846a9f10e6d2d34d790872d5e7ed7b1b351117c82f8b927502399`  
		Last Modified: Thu, 09 Oct 2025 02:20:59 GMT  
		Size: 681.8 KB (681759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71c697656e9ce6a76bcb04d0f78aff32c9bc6715c511aa163637cbd6c96a2ac`  
		Last Modified: Thu, 09 Oct 2025 02:20:59 GMT  
		Size: 13.6 KB (13577 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:b548ea6cdd265b4c28b305be5a93c4fc8b0d60583989598156895b80eefe29f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:80d06d6e62e4f1607126bfca0352e2b814ee0d5e2cb0d01b873ea0c3ff212a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157222054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771dee7da05d81f0e813477220d2c1fb328a25c6ed15c784b68ca47e3ae1aea5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:17:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:17:36 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 18 Nov 2025 05:17:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 18 Nov 2025 05:17:38 GMT
ENV GOSU_VER=1.16
# Tue, 18 Nov 2025 05:17:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 18 Nov 2025 05:17:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 18 Nov 2025 05:17:43 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 18 Nov 2025 05:17:43 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 18 Nov 2025 05:17:44 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 18 Nov 2025 05:17:44 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:17:44 GMT
CMD ["influxd"]
# Tue, 18 Nov 2025 05:17:44 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 05:17:44 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 18 Nov 2025 05:17:44 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 18 Nov 2025 05:17:44 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 18 Nov 2025 05:17:44 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c083ac3dd494839df49da730b2ca808788a26c458e07803a53f6000b9914c008`  
		Last Modified: Tue, 18 Nov 2025 05:18:08 GMT  
		Size: 9.8 MB (9796297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe79973373e0984f90d434906b24f59e09d3653e9b0a64ac501163cb06039b5`  
		Last Modified: Tue, 18 Nov 2025 05:18:08 GMT  
		Size: 6.2 MB (6156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1f90322a676f797132f3760313f4ce5fef5e82214cbac2bae818934922be1d`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd91bcec731380dc981617e7e6a27eff809dc77d80c891d64a1c432ea75e4dc`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 1.0 MB (1012036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0259fb23e7f74d9abb6dc12f70cb4d4625fe73b958700025e0ca624e76d431c`  
		Last Modified: Tue, 18 Nov 2025 05:18:22 GMT  
		Size: 100.2 MB (100244553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8513f44a5e4ba9d1fa3379e80a87a2b80fc40cb4f0a6022f49794e9cc6a8d5`  
		Last Modified: Tue, 18 Nov 2025 05:18:08 GMT  
		Size: 11.8 MB (11773792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d86a50f69f7d531e1c2cde43e54ea413d9d7f7799a4e6a3e83f72a22792951`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d57973d13ec346390d99f02c71f99a8a9faad512d116594b4eb34b74cf28d`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7325153cd01147116a63f1716e52cbbfb95cceff1bb7fe9729ee02cbfdbe731b`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:b2e0a09a4a27fb5b377ef84ceba92851b41f9e99cc8d4253bd3dec91337049db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce77c8b808530a8d9ade8789ba9a0d0d6a8774bb8233631d66bfe7f337ba40ae`

```dockerfile
```

-	Layers:
	-	`sha256:35f5b1fc80bf8c5073e3a2e9b72ab62ca38d431e560b90e2c85b0b7521aee48b`  
		Last Modified: Tue, 18 Nov 2025 09:21:49 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3cacf9519ba70a80483d2cb9194cffc0bde6187b2bf9f1f1a534adc089b6de7`  
		Last Modified: Tue, 18 Nov 2025 09:21:49 GMT  
		Size: 33.5 KB (33495 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ebf4fd439730dadc92b3bc3f565966f49e0026098626fa0bbd1bf4dfcd3dc23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efe22d086df7cc3f7292fb6c0bfeb0bfd1e7dfe9b4ab2f531fb9e3cde7a74a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:45:59 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:45:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 18 Nov 2025 03:45:59 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 18 Nov 2025 03:46:01 GMT
ENV GOSU_VER=1.16
# Tue, 18 Nov 2025 03:46:01 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:46:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 18 Nov 2025 03:46:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 18 Nov 2025 03:46:04 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 18 Nov 2025 03:46:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 18 Nov 2025 03:46:06 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 03:46:06 GMT
CMD ["influxd"]
# Tue, 18 Nov 2025 03:46:06 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 18 Nov 2025 03:46:06 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f18804d67ac382eaeac668698515f80ba62f0269c38f762d1afbd6be3db798`  
		Last Modified: Tue, 18 Nov 2025 03:46:34 GMT  
		Size: 9.6 MB (9626374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d00886f89ffaf07d35f7df7c3069dd3afe08bd1dd499c2d3deaddaba64ffad`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 5.8 MB (5790414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e659ab431338c547c1f98f68f92e58b74c5a951004693b9d9c5b87c329da5d`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b59935d05743ffa02ec8f0b55b5ac55704d51555f71109d405d50fbc5e4c9ab`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 938.9 KB (938873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562febceec6f34093da512fc564ef68229e13b9cbc93448890ee3b25d4cba3ba`  
		Last Modified: Tue, 18 Nov 2025 03:46:41 GMT  
		Size: 96.0 MB (96039030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40df32be97c38ea00ccc65fad323f679e2cdbdb0a21bc3401d70f74bcbf63496`  
		Last Modified: Tue, 18 Nov 2025 03:46:31 GMT  
		Size: 11.1 MB (11099988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbff83753ef6903833194bdec45bf87380a34a5c23aa0fc130e0bec7a4eab930`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16fe0dc91a3c9b16f488df0eaa5967b709ea1bb28034bc8e0fd57b84fc6c45b`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80207f266c84c3062586aff91f93c2d37fbd833c2a4e160bb775fb6509c7daa6`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:39b6cf435fde35f43996921bf986e0b8c60bac78e8b3fb7cf079990262481998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6475c2031479b1a92ed17ff24f69f4ce96e1ca85a835d81b9112d15ec2f01be2`

```dockerfile
```

-	Layers:
	-	`sha256:f75d415ae191d84746f95f4d12fa681a914b79864281212c05c5e323c2df000f`  
		Last Modified: Tue, 18 Nov 2025 06:25:29 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fca60a4fb48824c8d0e9b163faaa7aea6a7b0fe39e6e4faf8a38ecf3778f442e`  
		Last Modified: Tue, 18 Nov 2025 06:25:29 GMT  
		Size: 33.7 KB (33678 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:b4dbe25bb8f8be38f9cf5a12cbca453318a1ad3475954e9d37c38f6e5bc5006b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:14226eaac248bf27cf33cb39e93a3ca48e25440df27248181211bc30691e75df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81561836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917cdd480ab4907f6579b8f23e62b3c7ab08bd863de9c46eaad5b7a130b1a916`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Sep 2025 13:56:01 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53835a8d0d20cd34e4a7681b4ff49af99d05ec1c6417ae07f5f2ab28eb1d91d7`  
		Last Modified: Wed, 08 Oct 2025 23:11:06 GMT  
		Size: 9.9 MB (9862172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68829d4164c16e8135e6bf03046861f1566a9d374a3e99a820a143903d7291a`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9072b4a07b3f8dca037d515274838693bb0e168a1fc7b3118370baabde5fb4fb`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7b3f5da15b92af08a9ed64ddc91ab3b683642efb4ab6f3b672da89a0e1e868`  
		Last Modified: Wed, 08 Oct 2025 23:11:08 GMT  
		Size: 50.1 MB (50118379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b2ed5e22ac99676c240cb61c758189300e7929cfc6729851c369529ad53d8d`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 11.8 MB (11773778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68db778755a7a92ab67642d92cc7aa0c820cd21e5943b496d3b32e9fd2403de7`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d366f9033d07efa0b056a0d9362d12bf8f19cf51deec87929bb9a095810b8c21`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a54836f3da745e3ea2b1a54e11d6a3a24d9402e2007b4610da65910613fe2`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:deb2d219dabedf8726ae51cb51e71cbaff4b1141357813c1b7e667a1e586b227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.6 KB (944584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5ef07f0846c1450fa1eea4dc4e9a79f80492233cf1cf149f6ec9c9810e275a`

```dockerfile
```

-	Layers:
	-	`sha256:afb943795c0ce1f504024d5c58671df0aa1345208fa615fb7245377bb6894323`  
		Last Modified: Thu, 09 Oct 2025 02:21:09 GMT  
		Size: 913.8 KB (913815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e562735d7f12f937fbcb209933eb7986ea94c4b843ec47db133b14f1a8a2bc88`  
		Last Modified: Thu, 09 Oct 2025 02:21:09 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c0b4bb9622f30c203d6164e4608265058ec2133de5fecec638a96afe1fc77b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78730374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df955cee3af183aedd38baa540b6cf616ee4e64c4c7704593b9840e7e51c5b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Sep 2025 13:56:01 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e9f8ae4bf7158674e53e799e39195db08dc922549798b1c92b5db881e75950`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db47b23aa319f26ace574a307a140d466205a9c8792ea299825977016c72027`  
		Last Modified: Wed, 08 Oct 2025 21:55:32 GMT  
		Size: 9.8 MB (9822482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e75ad98f92c131cb2c24f50a1f955f559cb081760bb3ebaba411aff5652c0b1`  
		Last Modified: Wed, 08 Oct 2025 21:55:35 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0846ab0df2a8dd47b00f9e08910902bc9137be17fc01ecb2ab92865324a0a692`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee341d51fc6d484c991e3e387ad2bab42cc99f8c5f0c144f3548538763046b7`  
		Last Modified: Wed, 08 Oct 2025 21:55:33 GMT  
		Size: 48.0 MB (48017161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467babbc25c511c880690592c05bf5c8bf7eb3718a0ffcbb6bb66881d449be0`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73275e145aac044b3ee173c0907851a448d495a9d0f964f1d943e707c8a79108`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501e2a94b5ef2caef075bbdb0a7105d248f3f7d5e3a45540947b4843f21e8702`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bc70a0456678acb89ee83669fb653b9be40154e9167dec954aa525d35f87c`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c0855268e95dc31f5a9cac070c75e0c671fb7a46b90288fefc74be913b3869f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.0 KB (944029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f493a124da258c44e6401fe8b1e7f376cd7e326f841643ef5833690bb86f4d0`

```dockerfile
```

-	Layers:
	-	`sha256:0cf6c5db23c7a94944a2efa242d33b1a09e07eed2c284228b76d51eb51068db0`  
		Last Modified: Wed, 08 Oct 2025 23:20:42 GMT  
		Size: 913.1 KB (913066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868968715be1dde5591f2d64233e6a60defbc05776d1a13313f5f018438e6317`  
		Last Modified: Wed, 08 Oct 2025 23:20:44 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:b548ea6cdd265b4c28b305be5a93c4fc8b0d60583989598156895b80eefe29f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:80d06d6e62e4f1607126bfca0352e2b814ee0d5e2cb0d01b873ea0c3ff212a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157222054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771dee7da05d81f0e813477220d2c1fb328a25c6ed15c784b68ca47e3ae1aea5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:17:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:17:36 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 18 Nov 2025 05:17:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 18 Nov 2025 05:17:38 GMT
ENV GOSU_VER=1.16
# Tue, 18 Nov 2025 05:17:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 18 Nov 2025 05:17:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 18 Nov 2025 05:17:43 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 18 Nov 2025 05:17:43 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 18 Nov 2025 05:17:44 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 18 Nov 2025 05:17:44 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:17:44 GMT
CMD ["influxd"]
# Tue, 18 Nov 2025 05:17:44 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 05:17:44 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 18 Nov 2025 05:17:44 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 18 Nov 2025 05:17:44 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 18 Nov 2025 05:17:44 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c083ac3dd494839df49da730b2ca808788a26c458e07803a53f6000b9914c008`  
		Last Modified: Tue, 18 Nov 2025 05:18:08 GMT  
		Size: 9.8 MB (9796297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe79973373e0984f90d434906b24f59e09d3653e9b0a64ac501163cb06039b5`  
		Last Modified: Tue, 18 Nov 2025 05:18:08 GMT  
		Size: 6.2 MB (6156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1f90322a676f797132f3760313f4ce5fef5e82214cbac2bae818934922be1d`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd91bcec731380dc981617e7e6a27eff809dc77d80c891d64a1c432ea75e4dc`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 1.0 MB (1012036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0259fb23e7f74d9abb6dc12f70cb4d4625fe73b958700025e0ca624e76d431c`  
		Last Modified: Tue, 18 Nov 2025 05:18:22 GMT  
		Size: 100.2 MB (100244553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8513f44a5e4ba9d1fa3379e80a87a2b80fc40cb4f0a6022f49794e9cc6a8d5`  
		Last Modified: Tue, 18 Nov 2025 05:18:08 GMT  
		Size: 11.8 MB (11773792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d86a50f69f7d531e1c2cde43e54ea413d9d7f7799a4e6a3e83f72a22792951`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d57973d13ec346390d99f02c71f99a8a9faad512d116594b4eb34b74cf28d`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7325153cd01147116a63f1716e52cbbfb95cceff1bb7fe9729ee02cbfdbe731b`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:b2e0a09a4a27fb5b377ef84ceba92851b41f9e99cc8d4253bd3dec91337049db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce77c8b808530a8d9ade8789ba9a0d0d6a8774bb8233631d66bfe7f337ba40ae`

```dockerfile
```

-	Layers:
	-	`sha256:35f5b1fc80bf8c5073e3a2e9b72ab62ca38d431e560b90e2c85b0b7521aee48b`  
		Last Modified: Tue, 18 Nov 2025 09:21:49 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3cacf9519ba70a80483d2cb9194cffc0bde6187b2bf9f1f1a534adc089b6de7`  
		Last Modified: Tue, 18 Nov 2025 09:21:49 GMT  
		Size: 33.5 KB (33495 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ebf4fd439730dadc92b3bc3f565966f49e0026098626fa0bbd1bf4dfcd3dc23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efe22d086df7cc3f7292fb6c0bfeb0bfd1e7dfe9b4ab2f531fb9e3cde7a74a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:45:59 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:45:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 18 Nov 2025 03:45:59 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 18 Nov 2025 03:46:01 GMT
ENV GOSU_VER=1.16
# Tue, 18 Nov 2025 03:46:01 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:46:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 18 Nov 2025 03:46:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 18 Nov 2025 03:46:04 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 18 Nov 2025 03:46:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 18 Nov 2025 03:46:06 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 03:46:06 GMT
CMD ["influxd"]
# Tue, 18 Nov 2025 03:46:06 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 18 Nov 2025 03:46:06 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f18804d67ac382eaeac668698515f80ba62f0269c38f762d1afbd6be3db798`  
		Last Modified: Tue, 18 Nov 2025 03:46:34 GMT  
		Size: 9.6 MB (9626374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d00886f89ffaf07d35f7df7c3069dd3afe08bd1dd499c2d3deaddaba64ffad`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 5.8 MB (5790414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e659ab431338c547c1f98f68f92e58b74c5a951004693b9d9c5b87c329da5d`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b59935d05743ffa02ec8f0b55b5ac55704d51555f71109d405d50fbc5e4c9ab`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 938.9 KB (938873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562febceec6f34093da512fc564ef68229e13b9cbc93448890ee3b25d4cba3ba`  
		Last Modified: Tue, 18 Nov 2025 03:46:41 GMT  
		Size: 96.0 MB (96039030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40df32be97c38ea00ccc65fad323f679e2cdbdb0a21bc3401d70f74bcbf63496`  
		Last Modified: Tue, 18 Nov 2025 03:46:31 GMT  
		Size: 11.1 MB (11099988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbff83753ef6903833194bdec45bf87380a34a5c23aa0fc130e0bec7a4eab930`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16fe0dc91a3c9b16f488df0eaa5967b709ea1bb28034bc8e0fd57b84fc6c45b`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80207f266c84c3062586aff91f93c2d37fbd833c2a4e160bb775fb6509c7daa6`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:39b6cf435fde35f43996921bf986e0b8c60bac78e8b3fb7cf079990262481998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6475c2031479b1a92ed17ff24f69f4ce96e1ca85a835d81b9112d15ec2f01be2`

```dockerfile
```

-	Layers:
	-	`sha256:f75d415ae191d84746f95f4d12fa681a914b79864281212c05c5e323c2df000f`  
		Last Modified: Tue, 18 Nov 2025 06:25:29 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fca60a4fb48824c8d0e9b163faaa7aea6a7b0fe39e6e4faf8a38ecf3778f442e`  
		Last Modified: Tue, 18 Nov 2025 06:25:29 GMT  
		Size: 33.7 KB (33678 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:b4dbe25bb8f8be38f9cf5a12cbca453318a1ad3475954e9d37c38f6e5bc5006b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:14226eaac248bf27cf33cb39e93a3ca48e25440df27248181211bc30691e75df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81561836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917cdd480ab4907f6579b8f23e62b3c7ab08bd863de9c46eaad5b7a130b1a916`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Sep 2025 13:56:01 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53835a8d0d20cd34e4a7681b4ff49af99d05ec1c6417ae07f5f2ab28eb1d91d7`  
		Last Modified: Wed, 08 Oct 2025 23:11:06 GMT  
		Size: 9.9 MB (9862172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68829d4164c16e8135e6bf03046861f1566a9d374a3e99a820a143903d7291a`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9072b4a07b3f8dca037d515274838693bb0e168a1fc7b3118370baabde5fb4fb`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7b3f5da15b92af08a9ed64ddc91ab3b683642efb4ab6f3b672da89a0e1e868`  
		Last Modified: Wed, 08 Oct 2025 23:11:08 GMT  
		Size: 50.1 MB (50118379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b2ed5e22ac99676c240cb61c758189300e7929cfc6729851c369529ad53d8d`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 11.8 MB (11773778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68db778755a7a92ab67642d92cc7aa0c820cd21e5943b496d3b32e9fd2403de7`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d366f9033d07efa0b056a0d9362d12bf8f19cf51deec87929bb9a095810b8c21`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a54836f3da745e3ea2b1a54e11d6a3a24d9402e2007b4610da65910613fe2`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:deb2d219dabedf8726ae51cb51e71cbaff4b1141357813c1b7e667a1e586b227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.6 KB (944584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5ef07f0846c1450fa1eea4dc4e9a79f80492233cf1cf149f6ec9c9810e275a`

```dockerfile
```

-	Layers:
	-	`sha256:afb943795c0ce1f504024d5c58671df0aa1345208fa615fb7245377bb6894323`  
		Last Modified: Thu, 09 Oct 2025 02:21:09 GMT  
		Size: 913.8 KB (913815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e562735d7f12f937fbcb209933eb7986ea94c4b843ec47db133b14f1a8a2bc88`  
		Last Modified: Thu, 09 Oct 2025 02:21:09 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c0b4bb9622f30c203d6164e4608265058ec2133de5fecec638a96afe1fc77b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78730374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df955cee3af183aedd38baa540b6cf616ee4e64c4c7704593b9840e7e51c5b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Sep 2025 13:56:01 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e9f8ae4bf7158674e53e799e39195db08dc922549798b1c92b5db881e75950`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db47b23aa319f26ace574a307a140d466205a9c8792ea299825977016c72027`  
		Last Modified: Wed, 08 Oct 2025 21:55:32 GMT  
		Size: 9.8 MB (9822482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e75ad98f92c131cb2c24f50a1f955f559cb081760bb3ebaba411aff5652c0b1`  
		Last Modified: Wed, 08 Oct 2025 21:55:35 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0846ab0df2a8dd47b00f9e08910902bc9137be17fc01ecb2ab92865324a0a692`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee341d51fc6d484c991e3e387ad2bab42cc99f8c5f0c144f3548538763046b7`  
		Last Modified: Wed, 08 Oct 2025 21:55:33 GMT  
		Size: 48.0 MB (48017161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467babbc25c511c880690592c05bf5c8bf7eb3718a0ffcbb6bb66881d449be0`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73275e145aac044b3ee173c0907851a448d495a9d0f964f1d943e707c8a79108`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501e2a94b5ef2caef075bbdb0a7105d248f3f7d5e3a45540947b4843f21e8702`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bc70a0456678acb89ee83669fb653b9be40154e9167dec954aa525d35f87c`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c0855268e95dc31f5a9cac070c75e0c671fb7a46b90288fefc74be913b3869f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.0 KB (944029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f493a124da258c44e6401fe8b1e7f376cd7e326f841643ef5833690bb86f4d0`

```dockerfile
```

-	Layers:
	-	`sha256:0cf6c5db23c7a94944a2efa242d33b1a09e07eed2c284228b76d51eb51068db0`  
		Last Modified: Wed, 08 Oct 2025 23:20:42 GMT  
		Size: 913.1 KB (913066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868968715be1dde5591f2d64233e6a60defbc05776d1a13313f5f018438e6317`  
		Last Modified: Wed, 08 Oct 2025 23:20:44 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12`

```console
$ docker pull influxdb@sha256:b548ea6cdd265b4c28b305be5a93c4fc8b0d60583989598156895b80eefe29f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:80d06d6e62e4f1607126bfca0352e2b814ee0d5e2cb0d01b873ea0c3ff212a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157222054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771dee7da05d81f0e813477220d2c1fb328a25c6ed15c784b68ca47e3ae1aea5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:17:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:17:36 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 18 Nov 2025 05:17:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 18 Nov 2025 05:17:38 GMT
ENV GOSU_VER=1.16
# Tue, 18 Nov 2025 05:17:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 18 Nov 2025 05:17:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 18 Nov 2025 05:17:43 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 18 Nov 2025 05:17:43 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 18 Nov 2025 05:17:44 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 18 Nov 2025 05:17:44 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:17:44 GMT
CMD ["influxd"]
# Tue, 18 Nov 2025 05:17:44 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 05:17:44 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 18 Nov 2025 05:17:44 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 18 Nov 2025 05:17:44 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 18 Nov 2025 05:17:44 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c083ac3dd494839df49da730b2ca808788a26c458e07803a53f6000b9914c008`  
		Last Modified: Tue, 18 Nov 2025 05:18:08 GMT  
		Size: 9.8 MB (9796297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe79973373e0984f90d434906b24f59e09d3653e9b0a64ac501163cb06039b5`  
		Last Modified: Tue, 18 Nov 2025 05:18:08 GMT  
		Size: 6.2 MB (6156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1f90322a676f797132f3760313f4ce5fef5e82214cbac2bae818934922be1d`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd91bcec731380dc981617e7e6a27eff809dc77d80c891d64a1c432ea75e4dc`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 1.0 MB (1012036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0259fb23e7f74d9abb6dc12f70cb4d4625fe73b958700025e0ca624e76d431c`  
		Last Modified: Tue, 18 Nov 2025 05:18:22 GMT  
		Size: 100.2 MB (100244553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8513f44a5e4ba9d1fa3379e80a87a2b80fc40cb4f0a6022f49794e9cc6a8d5`  
		Last Modified: Tue, 18 Nov 2025 05:18:08 GMT  
		Size: 11.8 MB (11773792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d86a50f69f7d531e1c2cde43e54ea413d9d7f7799a4e6a3e83f72a22792951`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d57973d13ec346390d99f02c71f99a8a9faad512d116594b4eb34b74cf28d`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7325153cd01147116a63f1716e52cbbfb95cceff1bb7fe9729ee02cbfdbe731b`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:b2e0a09a4a27fb5b377ef84ceba92851b41f9e99cc8d4253bd3dec91337049db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce77c8b808530a8d9ade8789ba9a0d0d6a8774bb8233631d66bfe7f337ba40ae`

```dockerfile
```

-	Layers:
	-	`sha256:35f5b1fc80bf8c5073e3a2e9b72ab62ca38d431e560b90e2c85b0b7521aee48b`  
		Last Modified: Tue, 18 Nov 2025 09:21:49 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3cacf9519ba70a80483d2cb9194cffc0bde6187b2bf9f1f1a534adc089b6de7`  
		Last Modified: Tue, 18 Nov 2025 09:21:49 GMT  
		Size: 33.5 KB (33495 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ebf4fd439730dadc92b3bc3f565966f49e0026098626fa0bbd1bf4dfcd3dc23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efe22d086df7cc3f7292fb6c0bfeb0bfd1e7dfe9b4ab2f531fb9e3cde7a74a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:45:59 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:45:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 18 Nov 2025 03:45:59 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 18 Nov 2025 03:46:01 GMT
ENV GOSU_VER=1.16
# Tue, 18 Nov 2025 03:46:01 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:46:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 18 Nov 2025 03:46:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 18 Nov 2025 03:46:04 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 18 Nov 2025 03:46:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 18 Nov 2025 03:46:06 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 03:46:06 GMT
CMD ["influxd"]
# Tue, 18 Nov 2025 03:46:06 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 18 Nov 2025 03:46:06 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f18804d67ac382eaeac668698515f80ba62f0269c38f762d1afbd6be3db798`  
		Last Modified: Tue, 18 Nov 2025 03:46:34 GMT  
		Size: 9.6 MB (9626374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d00886f89ffaf07d35f7df7c3069dd3afe08bd1dd499c2d3deaddaba64ffad`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 5.8 MB (5790414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e659ab431338c547c1f98f68f92e58b74c5a951004693b9d9c5b87c329da5d`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b59935d05743ffa02ec8f0b55b5ac55704d51555f71109d405d50fbc5e4c9ab`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 938.9 KB (938873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562febceec6f34093da512fc564ef68229e13b9cbc93448890ee3b25d4cba3ba`  
		Last Modified: Tue, 18 Nov 2025 03:46:41 GMT  
		Size: 96.0 MB (96039030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40df32be97c38ea00ccc65fad323f679e2cdbdb0a21bc3401d70f74bcbf63496`  
		Last Modified: Tue, 18 Nov 2025 03:46:31 GMT  
		Size: 11.1 MB (11099988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbff83753ef6903833194bdec45bf87380a34a5c23aa0fc130e0bec7a4eab930`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16fe0dc91a3c9b16f488df0eaa5967b709ea1bb28034bc8e0fd57b84fc6c45b`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80207f266c84c3062586aff91f93c2d37fbd833c2a4e160bb775fb6509c7daa6`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:39b6cf435fde35f43996921bf986e0b8c60bac78e8b3fb7cf079990262481998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6475c2031479b1a92ed17ff24f69f4ce96e1ca85a835d81b9112d15ec2f01be2`

```dockerfile
```

-	Layers:
	-	`sha256:f75d415ae191d84746f95f4d12fa681a914b79864281212c05c5e323c2df000f`  
		Last Modified: Tue, 18 Nov 2025 06:25:29 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fca60a4fb48824c8d0e9b163faaa7aea6a7b0fe39e6e4faf8a38ecf3778f442e`  
		Last Modified: Tue, 18 Nov 2025 06:25:29 GMT  
		Size: 33.7 KB (33678 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12-alpine`

```console
$ docker pull influxdb@sha256:b4dbe25bb8f8be38f9cf5a12cbca453318a1ad3475954e9d37c38f6e5bc5006b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:14226eaac248bf27cf33cb39e93a3ca48e25440df27248181211bc30691e75df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81561836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917cdd480ab4907f6579b8f23e62b3c7ab08bd863de9c46eaad5b7a130b1a916`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Sep 2025 13:56:01 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53835a8d0d20cd34e4a7681b4ff49af99d05ec1c6417ae07f5f2ab28eb1d91d7`  
		Last Modified: Wed, 08 Oct 2025 23:11:06 GMT  
		Size: 9.9 MB (9862172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68829d4164c16e8135e6bf03046861f1566a9d374a3e99a820a143903d7291a`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9072b4a07b3f8dca037d515274838693bb0e168a1fc7b3118370baabde5fb4fb`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7b3f5da15b92af08a9ed64ddc91ab3b683642efb4ab6f3b672da89a0e1e868`  
		Last Modified: Wed, 08 Oct 2025 23:11:08 GMT  
		Size: 50.1 MB (50118379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b2ed5e22ac99676c240cb61c758189300e7929cfc6729851c369529ad53d8d`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 11.8 MB (11773778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68db778755a7a92ab67642d92cc7aa0c820cd21e5943b496d3b32e9fd2403de7`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d366f9033d07efa0b056a0d9362d12bf8f19cf51deec87929bb9a095810b8c21`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a54836f3da745e3ea2b1a54e11d6a3a24d9402e2007b4610da65910613fe2`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:deb2d219dabedf8726ae51cb51e71cbaff4b1141357813c1b7e667a1e586b227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.6 KB (944584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5ef07f0846c1450fa1eea4dc4e9a79f80492233cf1cf149f6ec9c9810e275a`

```dockerfile
```

-	Layers:
	-	`sha256:afb943795c0ce1f504024d5c58671df0aa1345208fa615fb7245377bb6894323`  
		Last Modified: Thu, 09 Oct 2025 02:21:09 GMT  
		Size: 913.8 KB (913815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e562735d7f12f937fbcb209933eb7986ea94c4b843ec47db133b14f1a8a2bc88`  
		Last Modified: Thu, 09 Oct 2025 02:21:09 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c0b4bb9622f30c203d6164e4608265058ec2133de5fecec638a96afe1fc77b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78730374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df955cee3af183aedd38baa540b6cf616ee4e64c4c7704593b9840e7e51c5b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Sep 2025 13:56:01 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e9f8ae4bf7158674e53e799e39195db08dc922549798b1c92b5db881e75950`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db47b23aa319f26ace574a307a140d466205a9c8792ea299825977016c72027`  
		Last Modified: Wed, 08 Oct 2025 21:55:32 GMT  
		Size: 9.8 MB (9822482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e75ad98f92c131cb2c24f50a1f955f559cb081760bb3ebaba411aff5652c0b1`  
		Last Modified: Wed, 08 Oct 2025 21:55:35 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0846ab0df2a8dd47b00f9e08910902bc9137be17fc01ecb2ab92865324a0a692`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee341d51fc6d484c991e3e387ad2bab42cc99f8c5f0c144f3548538763046b7`  
		Last Modified: Wed, 08 Oct 2025 21:55:33 GMT  
		Size: 48.0 MB (48017161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467babbc25c511c880690592c05bf5c8bf7eb3718a0ffcbb6bb66881d449be0`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73275e145aac044b3ee173c0907851a448d495a9d0f964f1d943e707c8a79108`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501e2a94b5ef2caef075bbdb0a7105d248f3f7d5e3a45540947b4843f21e8702`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bc70a0456678acb89ee83669fb653b9be40154e9167dec954aa525d35f87c`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c0855268e95dc31f5a9cac070c75e0c671fb7a46b90288fefc74be913b3869f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.0 KB (944029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f493a124da258c44e6401fe8b1e7f376cd7e326f841643ef5833690bb86f4d0`

```dockerfile
```

-	Layers:
	-	`sha256:0cf6c5db23c7a94944a2efa242d33b1a09e07eed2c284228b76d51eb51068db0`  
		Last Modified: Wed, 08 Oct 2025 23:20:42 GMT  
		Size: 913.1 KB (913066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868968715be1dde5591f2d64233e6a60defbc05776d1a13313f5f018438e6317`  
		Last Modified: Wed, 08 Oct 2025 23:20:44 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:30b4d9ef09745d70f4f1cfd3ecd16d0c1aadadf0b34512d26f203b5b545548ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:0c0b5c6f96799a0bd0a086199285fad1d8c637634d67c173de9a21dbc5652268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117798310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7a6e3e40bf58195f9ecf98e1b7fd7d49a105084867c4a2211338f003cf2fb1`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:09:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:09:02 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:09:05 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:09:05 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:09:05 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:09:05 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:09:05 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:09:05 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:09:05 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:09:05 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ec602172e261977575f11d467ce7288f5db05528add2c6687ed88115e4566d`  
		Last Modified: Fri, 21 Nov 2025 01:09:30 GMT  
		Size: 6.7 MB (6666106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a22f257fc04204500973a158da995dc0be631c882769bc2133d99ec614904`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5e77ec82a3e50264190d5ac3d943d7434fbacce7e8203882161228c1c91767`  
		Last Modified: Fri, 21 Nov 2025 01:09:37 GMT  
		Size: 81.4 MB (81403380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e43a523c0cc8655643f6b3f71777ef7f186469137b5cb16901b1fc520c93aa`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0a5644436ddcf98d3602d6cb46dec2a5ea78b914c37405af86509f233760a9`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:e81451fc027dc60632f39599eb065bb3d14b9878c3e74c054be5d36bfd64f97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cccfffbbf148460d65f81365c677d80d9b1c031008b76cae70562cde6368a617`

```dockerfile
```

-	Layers:
	-	`sha256:344f4388c9b3b3f833718304abe74f178fb3aaf01ac7835c375e6f1b24f2a83f`  
		Last Modified: Fri, 21 Nov 2025 03:20:32 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb6dc0f9df70a16e8997d58114fc03147b9dd521222c37f768ee215af11966c9`  
		Last Modified: Fri, 21 Nov 2025 03:20:33 GMT  
		Size: 17.6 KB (17616 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:7260dfe34b2b33c35a701e509a9599cda61cb893044635a1f823cfa043989163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108280455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f44ba383ea849284873eb74761a0d3c8d298cff6b002646aa64c3df015374f4`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:10:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:10:36 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:10:42 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:10:42 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:10:42 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:10:42 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:10:42 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:10:42 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:10:42 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:10:42 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b215b3151b300b2deec4daf8615f7ecb4bc96eb27db8209830dd66e00903c`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 6.7 MB (6676577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e25c4f8d48f3e4d9c23f68e350c0afbd64652ae03ebf6b59a98a95ddf691d25`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdf1ddee975088a0b59fa6be7d34c0c06d3b5c49ea7fcd8fd85aa2c0acbfb8c`  
		Last Modified: Fri, 21 Nov 2025 01:11:46 GMT  
		Size: 72.7 MB (72737790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd7330f8db15a09cbd0ec6ea99de8cee1f0093e94ccd8d77fc6c2a4cfdac039`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7b5a51040b95bc9176fdaede6fe14a044c1a9a04b65046b8ad3b3cabd53397`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:3b08b19939e095fd96bd8de0ca0212d28b32a13f4ab012e3fdb85de379c04699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71af086f6a3eadee982d10b453f92171306f0f4727846d35ee769c13c7919189`

```dockerfile
```

-	Layers:
	-	`sha256:f21daeef3b10baf18efce0296ea52b2da6913a6f4948a95ace4841db5dbdc62b`  
		Last Modified: Fri, 21 Nov 2025 03:20:37 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:649d1730362c0877602a9c4c7f8da89127bf88ecd1208fe0efd0b06c9b6f10e2`  
		Last Modified: Fri, 21 Nov 2025 03:20:38 GMT  
		Size: 17.8 KB (17765 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:d505d356938a25e2e15a8b2dadf2218b738da021d2ed7392004a817a1de52b20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:e29b41f14d7ad157cbcf017650e4f6dac627554c2d924f9e7ae57884971e1fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125281476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b2acb59bf6a3c5f51048608de0ddb03ce8b1ea1b6a3c7be429cc2228e7a8cd`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:09:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:09:02 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:09:36 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:09:36 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:09:36 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:09:36 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ec602172e261977575f11d467ce7288f5db05528add2c6687ed88115e4566d`  
		Last Modified: Fri, 21 Nov 2025 01:09:30 GMT  
		Size: 6.7 MB (6666106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a22f257fc04204500973a158da995dc0be631c882769bc2133d99ec614904`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e633feb1122d323a9eb9cb94f723b7ad8d87cd51101808c25cd5bbb60281774`  
		Last Modified: Fri, 21 Nov 2025 01:10:10 GMT  
		Size: 88.9 MB (88886351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094d85b5cca2f3812331aaae16d49f65afb45edd2d0b9df16c424053b115082f`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77620888035321ce666dd8db02345ec637bd5a5049483f28c2de8982a5004f6`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:525301679e2494bb0c0463ecbc3f21ca1537fe80ba004d612683ea46f86f772e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9303d33e2ca892f135c5953d369eb916df97424dd830393dc0467f589286511`

```dockerfile
```

-	Layers:
	-	`sha256:0e3e1236d677c014e3b16c3fd1ebf921a7360ffcdfe9cf29eec7c130ce059033`  
		Last Modified: Fri, 21 Nov 2025 03:20:40 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3683ae9634c5647b18930425cbfea200fc9c2f7cbfbbcb6f782bf146448dd451`  
		Last Modified: Fri, 21 Nov 2025 03:20:41 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ef0f1b8579a522489edca19bc7f616955496bdd5ee86066034eacbd6b21af53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115463993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0693736329ed32d1736000731a7dc106ae021eddabca28959c72e2ded72fc6bd`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:10:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:10:36 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:11:13 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:11:13 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:11:13 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:11:13 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b215b3151b300b2deec4daf8615f7ecb4bc96eb27db8209830dd66e00903c`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 6.7 MB (6676577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e25c4f8d48f3e4d9c23f68e350c0afbd64652ae03ebf6b59a98a95ddf691d25`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468b79c8366daaff07e38012ca6581d1aee98e31cecfe08b475184ceb20d4d34`  
		Last Modified: Fri, 21 Nov 2025 01:11:54 GMT  
		Size: 79.9 MB (79921134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b10e43e65b0618999012821ca464275048f96d3c3b0c6ef07b99bdd200161c`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cfb6bcaf92a99d2c342aa44899f9a76113610e142d349c264dd6def810c715`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:dd577be3b08e4279db3fffc19d22238ef18b07f075369b5ff90308c7338fc21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9e6074b38338411e63bc4d131cc4ec4f561ef77707bf0044ece1c652855c35`

```dockerfile
```

-	Layers:
	-	`sha256:0bac5d7414f7aa16b6033522b5e7e3ad2f6cc6663403d6eb92656f00d4046d09`  
		Last Modified: Fri, 21 Nov 2025 03:20:45 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3fd085a2d753c505f26f533794ef16eded8d10389faa4beca71a35c4f978fae`  
		Last Modified: Fri, 21 Nov 2025 03:20:46 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.7-core`

```console
$ docker pull influxdb@sha256:30b4d9ef09745d70f4f1cfd3ecd16d0c1aadadf0b34512d26f203b5b545548ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.7-core` - linux; amd64

```console
$ docker pull influxdb@sha256:0c0b5c6f96799a0bd0a086199285fad1d8c637634d67c173de9a21dbc5652268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117798310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7a6e3e40bf58195f9ecf98e1b7fd7d49a105084867c4a2211338f003cf2fb1`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:09:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:09:02 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:09:05 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:09:05 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:09:05 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:09:05 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:09:05 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:09:05 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:09:05 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:09:05 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ec602172e261977575f11d467ce7288f5db05528add2c6687ed88115e4566d`  
		Last Modified: Fri, 21 Nov 2025 01:09:30 GMT  
		Size: 6.7 MB (6666106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a22f257fc04204500973a158da995dc0be631c882769bc2133d99ec614904`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5e77ec82a3e50264190d5ac3d943d7434fbacce7e8203882161228c1c91767`  
		Last Modified: Fri, 21 Nov 2025 01:09:37 GMT  
		Size: 81.4 MB (81403380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e43a523c0cc8655643f6b3f71777ef7f186469137b5cb16901b1fc520c93aa`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0a5644436ddcf98d3602d6cb46dec2a5ea78b914c37405af86509f233760a9`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.7-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:e81451fc027dc60632f39599eb065bb3d14b9878c3e74c054be5d36bfd64f97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cccfffbbf148460d65f81365c677d80d9b1c031008b76cae70562cde6368a617`

```dockerfile
```

-	Layers:
	-	`sha256:344f4388c9b3b3f833718304abe74f178fb3aaf01ac7835c375e6f1b24f2a83f`  
		Last Modified: Fri, 21 Nov 2025 03:20:32 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb6dc0f9df70a16e8997d58114fc03147b9dd521222c37f768ee215af11966c9`  
		Last Modified: Fri, 21 Nov 2025 03:20:33 GMT  
		Size: 17.6 KB (17616 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.7-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:7260dfe34b2b33c35a701e509a9599cda61cb893044635a1f823cfa043989163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108280455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f44ba383ea849284873eb74761a0d3c8d298cff6b002646aa64c3df015374f4`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:10:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:10:36 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:10:42 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:10:42 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:10:42 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:10:42 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:10:42 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:10:42 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:10:42 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:10:42 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b215b3151b300b2deec4daf8615f7ecb4bc96eb27db8209830dd66e00903c`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 6.7 MB (6676577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e25c4f8d48f3e4d9c23f68e350c0afbd64652ae03ebf6b59a98a95ddf691d25`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdf1ddee975088a0b59fa6be7d34c0c06d3b5c49ea7fcd8fd85aa2c0acbfb8c`  
		Last Modified: Fri, 21 Nov 2025 01:11:46 GMT  
		Size: 72.7 MB (72737790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd7330f8db15a09cbd0ec6ea99de8cee1f0093e94ccd8d77fc6c2a4cfdac039`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7b5a51040b95bc9176fdaede6fe14a044c1a9a04b65046b8ad3b3cabd53397`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.7-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:3b08b19939e095fd96bd8de0ca0212d28b32a13f4ab012e3fdb85de379c04699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71af086f6a3eadee982d10b453f92171306f0f4727846d35ee769c13c7919189`

```dockerfile
```

-	Layers:
	-	`sha256:f21daeef3b10baf18efce0296ea52b2da6913a6f4948a95ace4841db5dbdc62b`  
		Last Modified: Fri, 21 Nov 2025 03:20:37 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:649d1730362c0877602a9c4c7f8da89127bf88ecd1208fe0efd0b06c9b6f10e2`  
		Last Modified: Fri, 21 Nov 2025 03:20:38 GMT  
		Size: 17.8 KB (17765 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.7-enterprise`

```console
$ docker pull influxdb@sha256:d505d356938a25e2e15a8b2dadf2218b738da021d2ed7392004a817a1de52b20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.7-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:e29b41f14d7ad157cbcf017650e4f6dac627554c2d924f9e7ae57884971e1fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125281476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b2acb59bf6a3c5f51048608de0ddb03ce8b1ea1b6a3c7be429cc2228e7a8cd`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:09:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:09:02 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:09:36 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:09:36 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:09:36 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:09:36 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ec602172e261977575f11d467ce7288f5db05528add2c6687ed88115e4566d`  
		Last Modified: Fri, 21 Nov 2025 01:09:30 GMT  
		Size: 6.7 MB (6666106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a22f257fc04204500973a158da995dc0be631c882769bc2133d99ec614904`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e633feb1122d323a9eb9cb94f723b7ad8d87cd51101808c25cd5bbb60281774`  
		Last Modified: Fri, 21 Nov 2025 01:10:10 GMT  
		Size: 88.9 MB (88886351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094d85b5cca2f3812331aaae16d49f65afb45edd2d0b9df16c424053b115082f`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77620888035321ce666dd8db02345ec637bd5a5049483f28c2de8982a5004f6`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.7-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:525301679e2494bb0c0463ecbc3f21ca1537fe80ba004d612683ea46f86f772e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9303d33e2ca892f135c5953d369eb916df97424dd830393dc0467f589286511`

```dockerfile
```

-	Layers:
	-	`sha256:0e3e1236d677c014e3b16c3fd1ebf921a7360ffcdfe9cf29eec7c130ce059033`  
		Last Modified: Fri, 21 Nov 2025 03:20:40 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3683ae9634c5647b18930425cbfea200fc9c2f7cbfbbcb6f782bf146448dd451`  
		Last Modified: Fri, 21 Nov 2025 03:20:41 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.7-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ef0f1b8579a522489edca19bc7f616955496bdd5ee86066034eacbd6b21af53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115463993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0693736329ed32d1736000731a7dc106ae021eddabca28959c72e2ded72fc6bd`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:10:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:10:36 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:11:13 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:11:13 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:11:13 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:11:13 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b215b3151b300b2deec4daf8615f7ecb4bc96eb27db8209830dd66e00903c`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 6.7 MB (6676577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e25c4f8d48f3e4d9c23f68e350c0afbd64652ae03ebf6b59a98a95ddf691d25`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468b79c8366daaff07e38012ca6581d1aee98e31cecfe08b475184ceb20d4d34`  
		Last Modified: Fri, 21 Nov 2025 01:11:54 GMT  
		Size: 79.9 MB (79921134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b10e43e65b0618999012821ca464275048f96d3c3b0c6ef07b99bdd200161c`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cfb6bcaf92a99d2c342aa44899f9a76113610e142d349c264dd6def810c715`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.7-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:dd577be3b08e4279db3fffc19d22238ef18b07f075369b5ff90308c7338fc21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9e6074b38338411e63bc4d131cc4ec4f561ef77707bf0044ece1c652855c35`

```dockerfile
```

-	Layers:
	-	`sha256:0bac5d7414f7aa16b6033522b5e7e3ad2f6cc6663403d6eb92656f00d4046d09`  
		Last Modified: Fri, 21 Nov 2025 03:20:45 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3fd085a2d753c505f26f533794ef16eded8d10389faa4beca71a35c4f978fae`  
		Last Modified: Fri, 21 Nov 2025 03:20:46 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.7.0-core`

```console
$ docker pull influxdb@sha256:30b4d9ef09745d70f4f1cfd3ecd16d0c1aadadf0b34512d26f203b5b545548ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.7.0-core` - linux; amd64

```console
$ docker pull influxdb@sha256:0c0b5c6f96799a0bd0a086199285fad1d8c637634d67c173de9a21dbc5652268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117798310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7a6e3e40bf58195f9ecf98e1b7fd7d49a105084867c4a2211338f003cf2fb1`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:09:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:09:02 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:09:05 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:09:05 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:09:05 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:09:05 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:09:05 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:09:05 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:09:05 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:09:05 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ec602172e261977575f11d467ce7288f5db05528add2c6687ed88115e4566d`  
		Last Modified: Fri, 21 Nov 2025 01:09:30 GMT  
		Size: 6.7 MB (6666106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a22f257fc04204500973a158da995dc0be631c882769bc2133d99ec614904`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5e77ec82a3e50264190d5ac3d943d7434fbacce7e8203882161228c1c91767`  
		Last Modified: Fri, 21 Nov 2025 01:09:37 GMT  
		Size: 81.4 MB (81403380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e43a523c0cc8655643f6b3f71777ef7f186469137b5cb16901b1fc520c93aa`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0a5644436ddcf98d3602d6cb46dec2a5ea78b914c37405af86509f233760a9`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.7.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:e81451fc027dc60632f39599eb065bb3d14b9878c3e74c054be5d36bfd64f97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cccfffbbf148460d65f81365c677d80d9b1c031008b76cae70562cde6368a617`

```dockerfile
```

-	Layers:
	-	`sha256:344f4388c9b3b3f833718304abe74f178fb3aaf01ac7835c375e6f1b24f2a83f`  
		Last Modified: Fri, 21 Nov 2025 03:20:32 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb6dc0f9df70a16e8997d58114fc03147b9dd521222c37f768ee215af11966c9`  
		Last Modified: Fri, 21 Nov 2025 03:20:33 GMT  
		Size: 17.6 KB (17616 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.7.0-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:7260dfe34b2b33c35a701e509a9599cda61cb893044635a1f823cfa043989163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108280455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f44ba383ea849284873eb74761a0d3c8d298cff6b002646aa64c3df015374f4`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:10:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:10:36 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:10:42 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:10:42 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:10:42 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:10:42 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:10:42 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:10:42 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:10:42 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:10:42 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b215b3151b300b2deec4daf8615f7ecb4bc96eb27db8209830dd66e00903c`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 6.7 MB (6676577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e25c4f8d48f3e4d9c23f68e350c0afbd64652ae03ebf6b59a98a95ddf691d25`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdf1ddee975088a0b59fa6be7d34c0c06d3b5c49ea7fcd8fd85aa2c0acbfb8c`  
		Last Modified: Fri, 21 Nov 2025 01:11:46 GMT  
		Size: 72.7 MB (72737790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd7330f8db15a09cbd0ec6ea99de8cee1f0093e94ccd8d77fc6c2a4cfdac039`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7b5a51040b95bc9176fdaede6fe14a044c1a9a04b65046b8ad3b3cabd53397`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.7.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:3b08b19939e095fd96bd8de0ca0212d28b32a13f4ab012e3fdb85de379c04699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71af086f6a3eadee982d10b453f92171306f0f4727846d35ee769c13c7919189`

```dockerfile
```

-	Layers:
	-	`sha256:f21daeef3b10baf18efce0296ea52b2da6913a6f4948a95ace4841db5dbdc62b`  
		Last Modified: Fri, 21 Nov 2025 03:20:37 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:649d1730362c0877602a9c4c7f8da89127bf88ecd1208fe0efd0b06c9b6f10e2`  
		Last Modified: Fri, 21 Nov 2025 03:20:38 GMT  
		Size: 17.8 KB (17765 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.7.0-enterprise`

```console
$ docker pull influxdb@sha256:d505d356938a25e2e15a8b2dadf2218b738da021d2ed7392004a817a1de52b20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.7.0-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:e29b41f14d7ad157cbcf017650e4f6dac627554c2d924f9e7ae57884971e1fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125281476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b2acb59bf6a3c5f51048608de0ddb03ce8b1ea1b6a3c7be429cc2228e7a8cd`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:09:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:09:02 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:09:36 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:09:36 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:09:36 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:09:36 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ec602172e261977575f11d467ce7288f5db05528add2c6687ed88115e4566d`  
		Last Modified: Fri, 21 Nov 2025 01:09:30 GMT  
		Size: 6.7 MB (6666106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a22f257fc04204500973a158da995dc0be631c882769bc2133d99ec614904`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e633feb1122d323a9eb9cb94f723b7ad8d87cd51101808c25cd5bbb60281774`  
		Last Modified: Fri, 21 Nov 2025 01:10:10 GMT  
		Size: 88.9 MB (88886351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094d85b5cca2f3812331aaae16d49f65afb45edd2d0b9df16c424053b115082f`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77620888035321ce666dd8db02345ec637bd5a5049483f28c2de8982a5004f6`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.7.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:525301679e2494bb0c0463ecbc3f21ca1537fe80ba004d612683ea46f86f772e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9303d33e2ca892f135c5953d369eb916df97424dd830393dc0467f589286511`

```dockerfile
```

-	Layers:
	-	`sha256:0e3e1236d677c014e3b16c3fd1ebf921a7360ffcdfe9cf29eec7c130ce059033`  
		Last Modified: Fri, 21 Nov 2025 03:20:40 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3683ae9634c5647b18930425cbfea200fc9c2f7cbfbbcb6f782bf146448dd451`  
		Last Modified: Fri, 21 Nov 2025 03:20:41 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.7.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ef0f1b8579a522489edca19bc7f616955496bdd5ee86066034eacbd6b21af53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115463993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0693736329ed32d1736000731a7dc106ae021eddabca28959c72e2ded72fc6bd`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:10:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:10:36 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:11:13 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:11:13 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:11:13 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:11:13 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b215b3151b300b2deec4daf8615f7ecb4bc96eb27db8209830dd66e00903c`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 6.7 MB (6676577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e25c4f8d48f3e4d9c23f68e350c0afbd64652ae03ebf6b59a98a95ddf691d25`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468b79c8366daaff07e38012ca6581d1aee98e31cecfe08b475184ceb20d4d34`  
		Last Modified: Fri, 21 Nov 2025 01:11:54 GMT  
		Size: 79.9 MB (79921134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b10e43e65b0618999012821ca464275048f96d3c3b0c6ef07b99bdd200161c`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cfb6bcaf92a99d2c342aa44899f9a76113610e142d349c264dd6def810c715`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.7.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:dd577be3b08e4279db3fffc19d22238ef18b07f075369b5ff90308c7338fc21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9e6074b38338411e63bc4d131cc4ec4f561ef77707bf0044ece1c652855c35`

```dockerfile
```

-	Layers:
	-	`sha256:0bac5d7414f7aa16b6033522b5e7e3ad2f6cc6663403d6eb92656f00d4046d09`  
		Last Modified: Fri, 21 Nov 2025 03:20:45 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3fd085a2d753c505f26f533794ef16eded8d10389faa4beca71a35c4f978fae`  
		Last Modified: Fri, 21 Nov 2025 03:20:46 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:b4dbe25bb8f8be38f9cf5a12cbca453318a1ad3475954e9d37c38f6e5bc5006b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:14226eaac248bf27cf33cb39e93a3ca48e25440df27248181211bc30691e75df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81561836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917cdd480ab4907f6579b8f23e62b3c7ab08bd863de9c46eaad5b7a130b1a916`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Sep 2025 13:56:01 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53835a8d0d20cd34e4a7681b4ff49af99d05ec1c6417ae07f5f2ab28eb1d91d7`  
		Last Modified: Wed, 08 Oct 2025 23:11:06 GMT  
		Size: 9.9 MB (9862172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68829d4164c16e8135e6bf03046861f1566a9d374a3e99a820a143903d7291a`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9072b4a07b3f8dca037d515274838693bb0e168a1fc7b3118370baabde5fb4fb`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7b3f5da15b92af08a9ed64ddc91ab3b683642efb4ab6f3b672da89a0e1e868`  
		Last Modified: Wed, 08 Oct 2025 23:11:08 GMT  
		Size: 50.1 MB (50118379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b2ed5e22ac99676c240cb61c758189300e7929cfc6729851c369529ad53d8d`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 11.8 MB (11773778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68db778755a7a92ab67642d92cc7aa0c820cd21e5943b496d3b32e9fd2403de7`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d366f9033d07efa0b056a0d9362d12bf8f19cf51deec87929bb9a095810b8c21`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a54836f3da745e3ea2b1a54e11d6a3a24d9402e2007b4610da65910613fe2`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:deb2d219dabedf8726ae51cb51e71cbaff4b1141357813c1b7e667a1e586b227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.6 KB (944584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5ef07f0846c1450fa1eea4dc4e9a79f80492233cf1cf149f6ec9c9810e275a`

```dockerfile
```

-	Layers:
	-	`sha256:afb943795c0ce1f504024d5c58671df0aa1345208fa615fb7245377bb6894323`  
		Last Modified: Thu, 09 Oct 2025 02:21:09 GMT  
		Size: 913.8 KB (913815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e562735d7f12f937fbcb209933eb7986ea94c4b843ec47db133b14f1a8a2bc88`  
		Last Modified: Thu, 09 Oct 2025 02:21:09 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c0b4bb9622f30c203d6164e4608265058ec2133de5fecec638a96afe1fc77b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78730374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df955cee3af183aedd38baa540b6cf616ee4e64c4c7704593b9840e7e51c5b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Sep 2025 13:56:01 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e9f8ae4bf7158674e53e799e39195db08dc922549798b1c92b5db881e75950`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db47b23aa319f26ace574a307a140d466205a9c8792ea299825977016c72027`  
		Last Modified: Wed, 08 Oct 2025 21:55:32 GMT  
		Size: 9.8 MB (9822482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e75ad98f92c131cb2c24f50a1f955f559cb081760bb3ebaba411aff5652c0b1`  
		Last Modified: Wed, 08 Oct 2025 21:55:35 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0846ab0df2a8dd47b00f9e08910902bc9137be17fc01ecb2ab92865324a0a692`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee341d51fc6d484c991e3e387ad2bab42cc99f8c5f0c144f3548538763046b7`  
		Last Modified: Wed, 08 Oct 2025 21:55:33 GMT  
		Size: 48.0 MB (48017161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467babbc25c511c880690592c05bf5c8bf7eb3718a0ffcbb6bb66881d449be0`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73275e145aac044b3ee173c0907851a448d495a9d0f964f1d943e707c8a79108`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501e2a94b5ef2caef075bbdb0a7105d248f3f7d5e3a45540947b4843f21e8702`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bc70a0456678acb89ee83669fb653b9be40154e9167dec954aa525d35f87c`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c0855268e95dc31f5a9cac070c75e0c671fb7a46b90288fefc74be913b3869f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.0 KB (944029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f493a124da258c44e6401fe8b1e7f376cd7e326f841643ef5833690bb86f4d0`

```dockerfile
```

-	Layers:
	-	`sha256:0cf6c5db23c7a94944a2efa242d33b1a09e07eed2c284228b76d51eb51068db0`  
		Last Modified: Wed, 08 Oct 2025 23:20:42 GMT  
		Size: 913.1 KB (913066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868968715be1dde5591f2d64233e6a60defbc05776d1a13313f5f018438e6317`  
		Last Modified: Wed, 08 Oct 2025 23:20:44 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:core`

```console
$ docker pull influxdb@sha256:30b4d9ef09745d70f4f1cfd3ecd16d0c1aadadf0b34512d26f203b5b545548ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:0c0b5c6f96799a0bd0a086199285fad1d8c637634d67c173de9a21dbc5652268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117798310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7a6e3e40bf58195f9ecf98e1b7fd7d49a105084867c4a2211338f003cf2fb1`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:09:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:09:02 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:09:05 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:09:05 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:09:05 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:09:05 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:09:05 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:09:05 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:09:05 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:09:05 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:09:05 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ec602172e261977575f11d467ce7288f5db05528add2c6687ed88115e4566d`  
		Last Modified: Fri, 21 Nov 2025 01:09:30 GMT  
		Size: 6.7 MB (6666106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a22f257fc04204500973a158da995dc0be631c882769bc2133d99ec614904`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5e77ec82a3e50264190d5ac3d943d7434fbacce7e8203882161228c1c91767`  
		Last Modified: Fri, 21 Nov 2025 01:09:37 GMT  
		Size: 81.4 MB (81403380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e43a523c0cc8655643f6b3f71777ef7f186469137b5cb16901b1fc520c93aa`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0a5644436ddcf98d3602d6cb46dec2a5ea78b914c37405af86509f233760a9`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:e81451fc027dc60632f39599eb065bb3d14b9878c3e74c054be5d36bfd64f97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cccfffbbf148460d65f81365c677d80d9b1c031008b76cae70562cde6368a617`

```dockerfile
```

-	Layers:
	-	`sha256:344f4388c9b3b3f833718304abe74f178fb3aaf01ac7835c375e6f1b24f2a83f`  
		Last Modified: Fri, 21 Nov 2025 03:20:32 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb6dc0f9df70a16e8997d58114fc03147b9dd521222c37f768ee215af11966c9`  
		Last Modified: Fri, 21 Nov 2025 03:20:33 GMT  
		Size: 17.6 KB (17616 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:7260dfe34b2b33c35a701e509a9599cda61cb893044635a1f823cfa043989163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108280455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f44ba383ea849284873eb74761a0d3c8d298cff6b002646aa64c3df015374f4`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:10:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:10:36 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:10:42 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:10:42 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:10:42 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:10:42 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:10:42 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:10:42 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:10:42 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:10:42 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:10:42 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b215b3151b300b2deec4daf8615f7ecb4bc96eb27db8209830dd66e00903c`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 6.7 MB (6676577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e25c4f8d48f3e4d9c23f68e350c0afbd64652ae03ebf6b59a98a95ddf691d25`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdf1ddee975088a0b59fa6be7d34c0c06d3b5c49ea7fcd8fd85aa2c0acbfb8c`  
		Last Modified: Fri, 21 Nov 2025 01:11:46 GMT  
		Size: 72.7 MB (72737790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd7330f8db15a09cbd0ec6ea99de8cee1f0093e94ccd8d77fc6c2a4cfdac039`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7b5a51040b95bc9176fdaede6fe14a044c1a9a04b65046b8ad3b3cabd53397`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:3b08b19939e095fd96bd8de0ca0212d28b32a13f4ab012e3fdb85de379c04699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71af086f6a3eadee982d10b453f92171306f0f4727846d35ee769c13c7919189`

```dockerfile
```

-	Layers:
	-	`sha256:f21daeef3b10baf18efce0296ea52b2da6913a6f4948a95ace4841db5dbdc62b`  
		Last Modified: Fri, 21 Nov 2025 03:20:37 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:649d1730362c0877602a9c4c7f8da89127bf88ecd1208fe0efd0b06c9b6f10e2`  
		Last Modified: Fri, 21 Nov 2025 03:20:38 GMT  
		Size: 17.8 KB (17765 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:d505d356938a25e2e15a8b2dadf2218b738da021d2ed7392004a817a1de52b20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:e29b41f14d7ad157cbcf017650e4f6dac627554c2d924f9e7ae57884971e1fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125281476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b2acb59bf6a3c5f51048608de0ddb03ce8b1ea1b6a3c7be429cc2228e7a8cd`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:09:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:09:02 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:09:36 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:09:36 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:09:36 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:09:36 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ec602172e261977575f11d467ce7288f5db05528add2c6687ed88115e4566d`  
		Last Modified: Fri, 21 Nov 2025 01:09:30 GMT  
		Size: 6.7 MB (6666106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a22f257fc04204500973a158da995dc0be631c882769bc2133d99ec614904`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e633feb1122d323a9eb9cb94f723b7ad8d87cd51101808c25cd5bbb60281774`  
		Last Modified: Fri, 21 Nov 2025 01:10:10 GMT  
		Size: 88.9 MB (88886351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094d85b5cca2f3812331aaae16d49f65afb45edd2d0b9df16c424053b115082f`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77620888035321ce666dd8db02345ec637bd5a5049483f28c2de8982a5004f6`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:525301679e2494bb0c0463ecbc3f21ca1537fe80ba004d612683ea46f86f772e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9303d33e2ca892f135c5953d369eb916df97424dd830393dc0467f589286511`

```dockerfile
```

-	Layers:
	-	`sha256:0e3e1236d677c014e3b16c3fd1ebf921a7360ffcdfe9cf29eec7c130ce059033`  
		Last Modified: Fri, 21 Nov 2025 03:20:40 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3683ae9634c5647b18930425cbfea200fc9c2f7cbfbbcb6f782bf146448dd451`  
		Last Modified: Fri, 21 Nov 2025 03:20:41 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ef0f1b8579a522489edca19bc7f616955496bdd5ee86066034eacbd6b21af53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115463993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0693736329ed32d1736000731a7dc106ae021eddabca28959c72e2ded72fc6bd`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:10:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:10:36 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:11:13 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:11:13 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:11:13 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:11:13 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b215b3151b300b2deec4daf8615f7ecb4bc96eb27db8209830dd66e00903c`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 6.7 MB (6676577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e25c4f8d48f3e4d9c23f68e350c0afbd64652ae03ebf6b59a98a95ddf691d25`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468b79c8366daaff07e38012ca6581d1aee98e31cecfe08b475184ceb20d4d34`  
		Last Modified: Fri, 21 Nov 2025 01:11:54 GMT  
		Size: 79.9 MB (79921134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b10e43e65b0618999012821ca464275048f96d3c3b0c6ef07b99bdd200161c`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cfb6bcaf92a99d2c342aa44899f9a76113610e142d349c264dd6def810c715`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:dd577be3b08e4279db3fffc19d22238ef18b07f075369b5ff90308c7338fc21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9e6074b38338411e63bc4d131cc4ec4f561ef77707bf0044ece1c652855c35`

```dockerfile
```

-	Layers:
	-	`sha256:0bac5d7414f7aa16b6033522b5e7e3ad2f6cc6663403d6eb92656f00d4046d09`  
		Last Modified: Fri, 21 Nov 2025 03:20:45 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3fd085a2d753c505f26f533794ef16eded8d10389faa4beca71a35c4f978fae`  
		Last Modified: Fri, 21 Nov 2025 03:20:46 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:b548ea6cdd265b4c28b305be5a93c4fc8b0d60583989598156895b80eefe29f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:80d06d6e62e4f1607126bfca0352e2b814ee0d5e2cb0d01b873ea0c3ff212a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157222054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771dee7da05d81f0e813477220d2c1fb328a25c6ed15c784b68ca47e3ae1aea5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:17:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:17:36 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 18 Nov 2025 05:17:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 18 Nov 2025 05:17:38 GMT
ENV GOSU_VER=1.16
# Tue, 18 Nov 2025 05:17:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 18 Nov 2025 05:17:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 18 Nov 2025 05:17:43 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 18 Nov 2025 05:17:43 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 18 Nov 2025 05:17:44 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 18 Nov 2025 05:17:44 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:17:44 GMT
CMD ["influxd"]
# Tue, 18 Nov 2025 05:17:44 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 05:17:44 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 18 Nov 2025 05:17:44 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 18 Nov 2025 05:17:44 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 18 Nov 2025 05:17:44 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c083ac3dd494839df49da730b2ca808788a26c458e07803a53f6000b9914c008`  
		Last Modified: Tue, 18 Nov 2025 05:18:08 GMT  
		Size: 9.8 MB (9796297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe79973373e0984f90d434906b24f59e09d3653e9b0a64ac501163cb06039b5`  
		Last Modified: Tue, 18 Nov 2025 05:18:08 GMT  
		Size: 6.2 MB (6156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1f90322a676f797132f3760313f4ce5fef5e82214cbac2bae818934922be1d`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd91bcec731380dc981617e7e6a27eff809dc77d80c891d64a1c432ea75e4dc`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 1.0 MB (1012036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0259fb23e7f74d9abb6dc12f70cb4d4625fe73b958700025e0ca624e76d431c`  
		Last Modified: Tue, 18 Nov 2025 05:18:22 GMT  
		Size: 100.2 MB (100244553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8513f44a5e4ba9d1fa3379e80a87a2b80fc40cb4f0a6022f49794e9cc6a8d5`  
		Last Modified: Tue, 18 Nov 2025 05:18:08 GMT  
		Size: 11.8 MB (11773792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d86a50f69f7d531e1c2cde43e54ea413d9d7f7799a4e6a3e83f72a22792951`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d57973d13ec346390d99f02c71f99a8a9faad512d116594b4eb34b74cf28d`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7325153cd01147116a63f1716e52cbbfb95cceff1bb7fe9729ee02cbfdbe731b`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:b2e0a09a4a27fb5b377ef84ceba92851b41f9e99cc8d4253bd3dec91337049db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce77c8b808530a8d9ade8789ba9a0d0d6a8774bb8233631d66bfe7f337ba40ae`

```dockerfile
```

-	Layers:
	-	`sha256:35f5b1fc80bf8c5073e3a2e9b72ab62ca38d431e560b90e2c85b0b7521aee48b`  
		Last Modified: Tue, 18 Nov 2025 09:21:49 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3cacf9519ba70a80483d2cb9194cffc0bde6187b2bf9f1f1a534adc089b6de7`  
		Last Modified: Tue, 18 Nov 2025 09:21:49 GMT  
		Size: 33.5 KB (33495 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ebf4fd439730dadc92b3bc3f565966f49e0026098626fa0bbd1bf4dfcd3dc23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efe22d086df7cc3f7292fb6c0bfeb0bfd1e7dfe9b4ab2f531fb9e3cde7a74a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:45:59 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:45:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 18 Nov 2025 03:45:59 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 18 Nov 2025 03:46:01 GMT
ENV GOSU_VER=1.16
# Tue, 18 Nov 2025 03:46:01 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:46:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 18 Nov 2025 03:46:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 18 Nov 2025 03:46:04 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 18 Nov 2025 03:46:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 18 Nov 2025 03:46:06 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 03:46:06 GMT
CMD ["influxd"]
# Tue, 18 Nov 2025 03:46:06 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 18 Nov 2025 03:46:06 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f18804d67ac382eaeac668698515f80ba62f0269c38f762d1afbd6be3db798`  
		Last Modified: Tue, 18 Nov 2025 03:46:34 GMT  
		Size: 9.6 MB (9626374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d00886f89ffaf07d35f7df7c3069dd3afe08bd1dd499c2d3deaddaba64ffad`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 5.8 MB (5790414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e659ab431338c547c1f98f68f92e58b74c5a951004693b9d9c5b87c329da5d`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b59935d05743ffa02ec8f0b55b5ac55704d51555f71109d405d50fbc5e4c9ab`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 938.9 KB (938873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562febceec6f34093da512fc564ef68229e13b9cbc93448890ee3b25d4cba3ba`  
		Last Modified: Tue, 18 Nov 2025 03:46:41 GMT  
		Size: 96.0 MB (96039030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40df32be97c38ea00ccc65fad323f679e2cdbdb0a21bc3401d70f74bcbf63496`  
		Last Modified: Tue, 18 Nov 2025 03:46:31 GMT  
		Size: 11.1 MB (11099988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbff83753ef6903833194bdec45bf87380a34a5c23aa0fc130e0bec7a4eab930`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16fe0dc91a3c9b16f488df0eaa5967b709ea1bb28034bc8e0fd57b84fc6c45b`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80207f266c84c3062586aff91f93c2d37fbd833c2a4e160bb775fb6509c7daa6`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:39b6cf435fde35f43996921bf986e0b8c60bac78e8b3fb7cf079990262481998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6475c2031479b1a92ed17ff24f69f4ce96e1ca85a835d81b9112d15ec2f01be2`

```dockerfile
```

-	Layers:
	-	`sha256:f75d415ae191d84746f95f4d12fa681a914b79864281212c05c5e323c2df000f`  
		Last Modified: Tue, 18 Nov 2025 06:25:29 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fca60a4fb48824c8d0e9b163faaa7aea6a7b0fe39e6e4faf8a38ecf3778f442e`  
		Last Modified: Tue, 18 Nov 2025 06:25:29 GMT  
		Size: 33.7 KB (33678 bytes)  
		MIME: application/vnd.in-toto+json
