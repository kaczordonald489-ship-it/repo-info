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
-	[`influxdb:2.8`](#influxdb28)
-	[`influxdb:2.8-alpine`](#influxdb28-alpine)
-	[`influxdb:2.8.0`](#influxdb280)
-	[`influxdb:2.8.0-alpine`](#influxdb280-alpine)
-	[`influxdb:3-core`](#influxdb3-core)
-	[`influxdb:3-enterprise`](#influxdb3-enterprise)
-	[`influxdb:3.8-core`](#influxdb38-core)
-	[`influxdb:3.8-enterprise`](#influxdb38-enterprise)
-	[`influxdb:3.8.0-core`](#influxdb380-core)
-	[`influxdb:3.8.0-enterprise`](#influxdb380-enterprise)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:core`](#influxdbcore)
-	[`influxdb:data`](#influxdbdata)
-	[`influxdb:data-alpine`](#influxdbdata-alpine)
-	[`influxdb:enterprise`](#influxdbenterprise)
-	[`influxdb:latest`](#influxdblatest)
-	[`influxdb:meta`](#influxdbmeta)
-	[`influxdb:meta-alpine`](#influxdbmeta-alpine)

## `influxdb:1.11`

```console
$ docker pull influxdb@sha256:1270992fdd55958c0d50192f19853a8b75dd701d3b02cc0f6c9c355052528f60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:e5d5fb560d0b932b0de8cd221157ade81bc14e2364f78c443d132960a688539f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116178834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c52426217cb7fbc11b2906e505b450535febc29e953ee1ee54acb599ce4ff5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:44 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 03 Feb 2026 03:32:52 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 03 Feb 2026 03:32:52 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:52 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 03 Feb 2026 03:32:52 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 03:32:52 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:32:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:32:52 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 03 Feb 2026 03:32:52 GMT
USER influxdb
# Tue, 03 Feb 2026 03:32:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:32:52 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272600fb23793c8c839863aaa8c4697eb0bc8cfafc30b146c58871e8b46017f4`  
		Last Modified: Tue, 03 Feb 2026 03:33:04 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309561655e025ce209bceb171b773d3811793601dabf1b53ed55097eee346624`  
		Last Modified: Tue, 03 Feb 2026 03:33:05 GMT  
		Size: 43.7 MB (43655996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9719041f5a753d1366cf7b5c1b0741b2bb76f3cd25d3629c968f657ada913a`  
		Last Modified: Tue, 03 Feb 2026 03:33:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c2e1c8b6d548ce9d82b692c45565bb85bb634128b798b23edad685f34df83f`  
		Last Modified: Tue, 03 Feb 2026 03:33:04 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d17a9ae042a114d6fbc419f0b4c22becaafe3c89f957bc30763f6e39e92435`  
		Last Modified: Tue, 03 Feb 2026 03:33:05 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:490ae662a0a3b90d1d35abea99c554f9949d85f9849f58d519ed880c7047c466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb85f35073a76626ed62484c098537555af40fb9634708d9d9e3cd63de9ca52`

```dockerfile
```

-	Layers:
	-	`sha256:6706a9685b9c0b1815764910dbd124227d3d4ef18ef17c9e54ebcf6527a60c32`  
		Last Modified: Tue, 03 Feb 2026 03:33:04 GMT  
		Size: 5.1 MB (5079263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c21e9e75bd2e492e880ad8e7ae6ad714a602ccaeb97248e389b128bf28eb55f`  
		Last Modified: Tue, 03 Feb 2026 03:33:04 GMT  
		Size: 15.5 KB (15486 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:320f20d78326bef829dc2323e2c7afcf093fc8cea8cd1aa2886c46582c57b4b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113096185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29d76aa5c58b074639794f5dc16d7fabc974f2fe939ae8d2393c576d21f7690`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:51:31 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 03 Feb 2026 03:51:38 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 03 Feb 2026 03:51:38 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:51:38 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 03 Feb 2026 03:51:38 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 03:51:38 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:51:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:51:38 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 03 Feb 2026 03:51:38 GMT
USER influxdb
# Tue, 03 Feb 2026 03:51:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:51:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20889d03b9df18b1f290c9270a137596b1169bd1ea80bea8e95c09230972301f`  
		Last Modified: Tue, 03 Feb 2026 03:51:50 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb9bc6e202ea3091cf1e8b5cef4fa6706abf3f45e6db372b7dd22ea222cf80b`  
		Last Modified: Tue, 03 Feb 2026 03:51:51 GMT  
		Size: 41.1 MB (41122480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3596729ea83097173c66bf7cfce46640e75c9a9ba756b0f66a155dd24b61be`  
		Last Modified: Tue, 03 Feb 2026 03:51:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a849099d357457af28fde4326b9d4bd496fe21b9377115988559f7f29919cb41`  
		Last Modified: Tue, 03 Feb 2026 03:51:50 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0ea66c8e820638c7f85ae9e3c8316d5bccf2f04de52b6f5a83f958ebc9085f`  
		Last Modified: Tue, 03 Feb 2026 03:51:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:c3c555421bb4ab46a0989f267544ef6670b0eb2e46c852f5c13a40a4775551a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f296b13746247287b4aaf4f3b0c01df25688310ae9a904966251f333ef6115`

```dockerfile
```

-	Layers:
	-	`sha256:83aa348ca2bc5b8e664ff4198a3f6f07d27b06f043ad67e2080765b671e7eb63`  
		Last Modified: Tue, 03 Feb 2026 03:51:50 GMT  
		Size: 5.1 MB (5078728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6872816305b8963c7c2ceb17e9fadcbe5231b2fbb86044f700604a002049ce62`  
		Last Modified: Tue, 03 Feb 2026 03:51:50 GMT  
		Size: 15.6 KB (15579 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-alpine`

```console
$ docker pull influxdb@sha256:8632b2aee90e61d03b25090e60f43291ad8c18961970d2a76ebe170fb9edede1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:18b0e900a9ef7bd527e22efae32fe7540ce10075c94e4704c00595002e0b48e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42931179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f123753da719af7e615849cf60685574ba135c84c07dafc0c4512ae2680e8f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:25:33 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:25:39 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 28 Jan 2026 03:25:39 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:25:39 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:25:39 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 28 Jan 2026 03:25:39 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:25:39 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:25:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:25:40 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:25:40 GMT
USER influxdb
# Wed, 28 Jan 2026 03:25:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:25:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49aaa256c2fea1c8d7b82042abbbe881566d13a774788fc2f2673dadb0be5ade`  
		Last Modified: Wed, 28 Jan 2026 03:25:49 GMT  
		Size: 1.2 MB (1224765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e625ddee2d605bf259f1afe9bfb1a1c019b7499ed66fe5b5709995dc352e039`  
		Last Modified: Wed, 28 Jan 2026 03:25:50 GMT  
		Size: 38.1 MB (38075834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ba877bbd5d6e9300c8f25cf4c64bc21e4768a2f8675f220c0c8618040573ff`  
		Last Modified: Wed, 28 Jan 2026 03:25:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fa8bf86e7bb8232138a820b91ae5f64da53c77a33ec7009ecea62ecb4d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:25:49 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0628ad9b2208773a1caa4b083766abd5edbb2f9bd1c0ebaec5c23e6cb0e1b407`  
		Last Modified: Wed, 28 Jan 2026 03:25:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ee7358201d8d00b5531a19b69e5d44af7f1494147b1242bd02009957592bde`  
		Last Modified: Wed, 28 Jan 2026 03:25:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:594ad6109cea6a457966bd968837e36de65aa4722589a2969b5735fa05d9ff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.3 KB (760316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a4287008743080ecb92eda2534b9170c8b6ab01f3a2a02c55e4994dfa75208`

```dockerfile
```

-	Layers:
	-	`sha256:8f9a0d76d31827559bd06701701b5929317882f4493616d244c1a37de2c34d9a`  
		Last Modified: Wed, 28 Jan 2026 03:25:49 GMT  
		Size: 742.5 KB (742482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c993bbbc918316ab7ddefcdd0dcbea3674931c55da0ef119f9b1673771b7d172`  
		Last Modified: Wed, 28 Jan 2026 03:25:49 GMT  
		Size: 17.8 KB (17834 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:13d98b40f88d68bb9bb24e099c309f0eea5ae527c67128e146fe97e6db0d2039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40945594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fde6b75da97afba60a3df5426d35f696d1bc59f250d2ecc3a83113c26daf17f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:16 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 28 Jan 2026 03:15:23 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:23 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:15:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
USER influxdb
# Wed, 28 Jan 2026 03:15:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259e398369be67daddeb4ff7983b9be6161412ec09dce4a3ea618736039d652a`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 1.3 MB (1304796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43db76d8b85d7162a919f9a4660fa2a439664ab43fe4f6762ad6075b94c1cd3b`  
		Last Modified: Wed, 28 Jan 2026 03:15:33 GMT  
		Size: 35.5 MB (35548123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bee56c9fe82fe02899d828e40db149d5630cb99f8d4b1059da46b27bf916096`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f12a5d75e7f56eea39d82380cbe4a85dffe9c2a569aed233564f2d602d2beb`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4d0c790d6348482dc5ead4b2e098f4a44ad8fedc6d3676b07bb0efd18d3212`  
		Last Modified: Wed, 28 Jan 2026 03:15:33 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9fadd1909545912e8e5a7b4345961fe2a7419e4fccd0bd11177e3314b0fd1e`  
		Last Modified: Wed, 28 Jan 2026 03:15:33 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a3f06b2b71e748389eece6e7ae27a401b4a1ddf6c1b597d025e7bda5bd150779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.7 KB (759653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9527bc42b25341df02b03ea0015db4b21eaece4f3fac0f6aad4216a0eb65076`

```dockerfile
```

-	Layers:
	-	`sha256:8b26a7c1292b91ca48e8fb9e660db26bff0ef5e3cbbe1a2518554ae663de4075`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 741.7 KB (741709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a44a8eaa3f69c139fc2f80d23792c493cb6d37dc65c27016d78067d76cd6e2`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 17.9 KB (17944 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:649d49561ec5dc9b5ecea81e0f6b2f5be880d0595e0c056032d90d4b43e12960
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:3e54158526ef6d58ac83ca560783db87c5c36efd36f9a518869d3dc0267b5fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114692496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f94e6337af63f9d58bdbe07ec5e00f5b96530a458e830ec55171880db92779`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:32:56 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 03 Feb 2026 03:32:56 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 03 Feb 2026 03:32:56 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 03 Feb 2026 03:32:56 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 03:32:56 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:32:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:32:56 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 03 Feb 2026 03:32:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:32:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3342e0c344a48271fae633c4dfcfb346d596bed50e445a32161118064363a6`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7235fdf3c9ec30c6605496ec3dc25adba578b2c81229e85a9e074b0c48c00005`  
		Last Modified: Tue, 03 Feb 2026 03:33:09 GMT  
		Size: 42.2 MB (42165718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94a4a40254cff93c4db8b3513c1223fb865baebd0bec9ebda4d6f2d19abfe4f`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904e172d1f287f5f44b0919de34f01fe7668af75aa89b58ead2a78691f09d5cd`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d36d3908917495c59b40629c824d83a255e896afe6002d656966ddccf20691`  
		Last Modified: Tue, 03 Feb 2026 03:33:09 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:063696b39a6073e19e10620284048eb5583ecb719844a7a36b860500e9c5b66b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a4fbcae227a219d0c7888a61853aa3d0774f59f197757e2d7f555a488009e6`

```dockerfile
```

-	Layers:
	-	`sha256:465f3e547e304dec5c4331f4d87f5f2ef1d3b3a70abb8056ae8d9eb11247a8b8`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 4.7 MB (4684406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ab196cf03d82181dcbddae15361fd0e20175db94410e49fac0450e2d48fa7`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:9d0b51aeab711df34e37e895e2d1469ec43a29095ece120902603c3cf21efa38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:02153a74beabb3f96b259f8507d7421339482549e50cc5d2258f0b2ce9e6c864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46960587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f4d43e203a1a92b5ff368450db5c6fe8325a6b765befd58abf19f686fea967`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:25:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:25:51 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:25:55 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 28 Jan 2026 03:25:55 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:25:56 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:25:56 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:25:56 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:25:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:25:56 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:25:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:25:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0263a1e24ffa0829b1f805a2d6c158c33fea253d7ef254f2494681fa2d006a`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9672fa9124cf983f0543c61ea1dde339b6705eb7d1e2b05d760b6b5938097078`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 1.2 MB (1224754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f2e30e450bd646642d30a6713818d18161df47157ce401b61f69011dc8633f`  
		Last Modified: Wed, 28 Jan 2026 03:26:06 GMT  
		Size: 42.1 MB (42105918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f04de5a1e581d806f89cfbb2942929a3f7241a270158df81e7c34383fd931`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68edddde0b5f46997714b4dde35e1dc7f0e2fc457f720dd8975b0492c124bb0`  
		Last Modified: Wed, 28 Jan 2026 03:26:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80a545e019203b789e56a39b97bb112b148b5a35d4bfa4e5e047435ac01313c`  
		Last Modified: Wed, 28 Jan 2026 03:26:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f1fe57771330dc344971ded307b8c5957352e6c41c6b4052a3a2de810fed9266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.6 KB (785589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a4234b2573554d959bb8763239bdda077e7007d27002de0f9dab694364e51b`

```dockerfile
```

-	Layers:
	-	`sha256:86054862a078c59646ba2b5c08117a00b07c42589123f4297ea77aab085bb20d`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 769.0 KB (768993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f041e72a4e9d944868da8607a414ca998a5a43702d92dd969cde2a705e241ca`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:5f3050cf3558da40896d9849217f5c0e35226808562909cdc9127ea685280d7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:8bc88e165a8c46c42ad22f0ebbeab4c1562a112bf251cde06f9516f2d4b1e76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91121710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5efb0acebd2cc78ce191050ca0ba9fb3f6abe26243071ba03d9537b867642f9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:33:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:33:02 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 03 Feb 2026 03:33:02 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 03 Feb 2026 03:33:02 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 03 Feb 2026 03:33:02 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 03 Feb 2026 03:33:02 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:33:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:33:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:33:02 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6523b81168533bbcd7b027035018575e31ac7f473a62e5be7319a1abd4449a`  
		Last Modified: Tue, 03 Feb 2026 03:33:11 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162da3cefe6da12370d22d65541c5f1cd07c73ebbba298fa4a32b926217deb85`  
		Last Modified: Tue, 03 Feb 2026 03:33:11 GMT  
		Size: 18.6 MB (18596147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac39049d45a69c0b814c812562698c7c60f501f5ba6b5253b3c097987f52c8b`  
		Last Modified: Tue, 03 Feb 2026 03:33:11 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96594ee04fa23dfa7f6118b01a023a0202e589722c5f30a9d94dc434dddf553a`  
		Last Modified: Tue, 03 Feb 2026 03:33:11 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:0bafc3ac5496395ec8876bc4fcbc59b5844e044536c960cf69218b01577dc0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e0cf8fdf0d559f361e7a077440f56472ec44927de2de1b207bfa150bd64f80`

```dockerfile
```

-	Layers:
	-	`sha256:08ee2c14327be46b40fa2fdad146cd31d70f93fbf547714a1caf10b76103a8fc`  
		Last Modified: Tue, 03 Feb 2026 03:33:11 GMT  
		Size: 4.6 MB (4591249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3534eaf431a735ece3d84dc463f0204d1c421d45714c1203417cad4417075d7`  
		Last Modified: Tue, 03 Feb 2026 03:33:11 GMT  
		Size: 13.0 KB (13024 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:249c7bd6c3cb8f7bbba327cf37a3b1005d6cd347d8a692c8ceaff56d18fb7891
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:44ad70f43101c494e4d04ab932049e45759c24ed812f029b96c79c7e18b7f5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23403364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c9203475562a7d8b438ef3bdf218f4cdb0516b9023ca9c4f7beb027b1dd551`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:26:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:26:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:26:49 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 28 Jan 2026 03:26:49 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:26:49 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 28 Jan 2026 03:26:49 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 28 Jan 2026 03:26:49 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:26:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:26:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:26:49 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ce9bebb946b2c426c9224e7360d845b78bd397b82149cb1f1fa0be2b2e876c`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a219cf2dafb437a398f6465d6bb676c776f0a32983a6488d2a5a52da44ff00`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 1.2 MB (1224764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b99563435aacc7f0c7f9f7b4b1850b98aa7b8f25747307c2be2310f2a08d95`  
		Last Modified: Wed, 28 Jan 2026 03:26:57 GMT  
		Size: 18.5 MB (18549891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a807e577681eeebd1dcac3ab7d414179b8fe0902833964ccc7e1f2fc51789`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9608b4806a31ae3e7d94b72f7606acf6161b5a5c2d16ac725d6c236e2b7a93`  
		Last Modified: Wed, 28 Jan 2026 03:26:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:0b3947f754f901b0eee6981e99cd9d177d98f9208d60e99599a2182ee456cb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 KB (691589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf3c479b5f2c96864cbcd1eeccb783380ad8a72539788725799c866d6198c2b`

```dockerfile
```

-	Layers:
	-	`sha256:01b16cc3b5518976d91b8bddbc7009f186a3aef03547cabb60c8a13ddbbc8227`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 676.6 KB (676622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1541f8caff84dbcdb88fbc06c12d3a170bfb849a19f16feb4f4857708b70317a`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 15.0 KB (14967 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8`

```console
$ docker pull influxdb@sha256:1270992fdd55958c0d50192f19853a8b75dd701d3b02cc0f6c9c355052528f60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:e5d5fb560d0b932b0de8cd221157ade81bc14e2364f78c443d132960a688539f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116178834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c52426217cb7fbc11b2906e505b450535febc29e953ee1ee54acb599ce4ff5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:44 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 03 Feb 2026 03:32:52 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 03 Feb 2026 03:32:52 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:52 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 03 Feb 2026 03:32:52 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 03:32:52 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:32:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:32:52 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 03 Feb 2026 03:32:52 GMT
USER influxdb
# Tue, 03 Feb 2026 03:32:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:32:52 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272600fb23793c8c839863aaa8c4697eb0bc8cfafc30b146c58871e8b46017f4`  
		Last Modified: Tue, 03 Feb 2026 03:33:04 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309561655e025ce209bceb171b773d3811793601dabf1b53ed55097eee346624`  
		Last Modified: Tue, 03 Feb 2026 03:33:05 GMT  
		Size: 43.7 MB (43655996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9719041f5a753d1366cf7b5c1b0741b2bb76f3cd25d3629c968f657ada913a`  
		Last Modified: Tue, 03 Feb 2026 03:33:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c2e1c8b6d548ce9d82b692c45565bb85bb634128b798b23edad685f34df83f`  
		Last Modified: Tue, 03 Feb 2026 03:33:04 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d17a9ae042a114d6fbc419f0b4c22becaafe3c89f957bc30763f6e39e92435`  
		Last Modified: Tue, 03 Feb 2026 03:33:05 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:490ae662a0a3b90d1d35abea99c554f9949d85f9849f58d519ed880c7047c466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb85f35073a76626ed62484c098537555af40fb9634708d9d9e3cd63de9ca52`

```dockerfile
```

-	Layers:
	-	`sha256:6706a9685b9c0b1815764910dbd124227d3d4ef18ef17c9e54ebcf6527a60c32`  
		Last Modified: Tue, 03 Feb 2026 03:33:04 GMT  
		Size: 5.1 MB (5079263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c21e9e75bd2e492e880ad8e7ae6ad714a602ccaeb97248e389b128bf28eb55f`  
		Last Modified: Tue, 03 Feb 2026 03:33:04 GMT  
		Size: 15.5 KB (15486 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:320f20d78326bef829dc2323e2c7afcf093fc8cea8cd1aa2886c46582c57b4b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113096185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29d76aa5c58b074639794f5dc16d7fabc974f2fe939ae8d2393c576d21f7690`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:51:31 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 03 Feb 2026 03:51:38 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 03 Feb 2026 03:51:38 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:51:38 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 03 Feb 2026 03:51:38 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 03:51:38 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:51:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:51:38 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 03 Feb 2026 03:51:38 GMT
USER influxdb
# Tue, 03 Feb 2026 03:51:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:51:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20889d03b9df18b1f290c9270a137596b1169bd1ea80bea8e95c09230972301f`  
		Last Modified: Tue, 03 Feb 2026 03:51:50 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb9bc6e202ea3091cf1e8b5cef4fa6706abf3f45e6db372b7dd22ea222cf80b`  
		Last Modified: Tue, 03 Feb 2026 03:51:51 GMT  
		Size: 41.1 MB (41122480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3596729ea83097173c66bf7cfce46640e75c9a9ba756b0f66a155dd24b61be`  
		Last Modified: Tue, 03 Feb 2026 03:51:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a849099d357457af28fde4326b9d4bd496fe21b9377115988559f7f29919cb41`  
		Last Modified: Tue, 03 Feb 2026 03:51:50 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0ea66c8e820638c7f85ae9e3c8316d5bccf2f04de52b6f5a83f958ebc9085f`  
		Last Modified: Tue, 03 Feb 2026 03:51:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:c3c555421bb4ab46a0989f267544ef6670b0eb2e46c852f5c13a40a4775551a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f296b13746247287b4aaf4f3b0c01df25688310ae9a904966251f333ef6115`

```dockerfile
```

-	Layers:
	-	`sha256:83aa348ca2bc5b8e664ff4198a3f6f07d27b06f043ad67e2080765b671e7eb63`  
		Last Modified: Tue, 03 Feb 2026 03:51:50 GMT  
		Size: 5.1 MB (5078728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6872816305b8963c7c2ceb17e9fadcbe5231b2fbb86044f700604a002049ce62`  
		Last Modified: Tue, 03 Feb 2026 03:51:50 GMT  
		Size: 15.6 KB (15579 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-alpine`

```console
$ docker pull influxdb@sha256:8632b2aee90e61d03b25090e60f43291ad8c18961970d2a76ebe170fb9edede1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:18b0e900a9ef7bd527e22efae32fe7540ce10075c94e4704c00595002e0b48e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42931179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f123753da719af7e615849cf60685574ba135c84c07dafc0c4512ae2680e8f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:25:33 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:25:39 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 28 Jan 2026 03:25:39 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:25:39 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:25:39 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 28 Jan 2026 03:25:39 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:25:39 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:25:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:25:40 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:25:40 GMT
USER influxdb
# Wed, 28 Jan 2026 03:25:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:25:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49aaa256c2fea1c8d7b82042abbbe881566d13a774788fc2f2673dadb0be5ade`  
		Last Modified: Wed, 28 Jan 2026 03:25:49 GMT  
		Size: 1.2 MB (1224765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e625ddee2d605bf259f1afe9bfb1a1c019b7499ed66fe5b5709995dc352e039`  
		Last Modified: Wed, 28 Jan 2026 03:25:50 GMT  
		Size: 38.1 MB (38075834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ba877bbd5d6e9300c8f25cf4c64bc21e4768a2f8675f220c0c8618040573ff`  
		Last Modified: Wed, 28 Jan 2026 03:25:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fa8bf86e7bb8232138a820b91ae5f64da53c77a33ec7009ecea62ecb4d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:25:49 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0628ad9b2208773a1caa4b083766abd5edbb2f9bd1c0ebaec5c23e6cb0e1b407`  
		Last Modified: Wed, 28 Jan 2026 03:25:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ee7358201d8d00b5531a19b69e5d44af7f1494147b1242bd02009957592bde`  
		Last Modified: Wed, 28 Jan 2026 03:25:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:594ad6109cea6a457966bd968837e36de65aa4722589a2969b5735fa05d9ff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.3 KB (760316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a4287008743080ecb92eda2534b9170c8b6ab01f3a2a02c55e4994dfa75208`

```dockerfile
```

-	Layers:
	-	`sha256:8f9a0d76d31827559bd06701701b5929317882f4493616d244c1a37de2c34d9a`  
		Last Modified: Wed, 28 Jan 2026 03:25:49 GMT  
		Size: 742.5 KB (742482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c993bbbc918316ab7ddefcdd0dcbea3674931c55da0ef119f9b1673771b7d172`  
		Last Modified: Wed, 28 Jan 2026 03:25:49 GMT  
		Size: 17.8 KB (17834 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:13d98b40f88d68bb9bb24e099c309f0eea5ae527c67128e146fe97e6db0d2039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40945594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fde6b75da97afba60a3df5426d35f696d1bc59f250d2ecc3a83113c26daf17f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:16 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 28 Jan 2026 03:15:23 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:23 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:15:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
USER influxdb
# Wed, 28 Jan 2026 03:15:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259e398369be67daddeb4ff7983b9be6161412ec09dce4a3ea618736039d652a`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 1.3 MB (1304796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43db76d8b85d7162a919f9a4660fa2a439664ab43fe4f6762ad6075b94c1cd3b`  
		Last Modified: Wed, 28 Jan 2026 03:15:33 GMT  
		Size: 35.5 MB (35548123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bee56c9fe82fe02899d828e40db149d5630cb99f8d4b1059da46b27bf916096`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f12a5d75e7f56eea39d82380cbe4a85dffe9c2a569aed233564f2d602d2beb`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4d0c790d6348482dc5ead4b2e098f4a44ad8fedc6d3676b07bb0efd18d3212`  
		Last Modified: Wed, 28 Jan 2026 03:15:33 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9fadd1909545912e8e5a7b4345961fe2a7419e4fccd0bd11177e3314b0fd1e`  
		Last Modified: Wed, 28 Jan 2026 03:15:33 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a3f06b2b71e748389eece6e7ae27a401b4a1ddf6c1b597d025e7bda5bd150779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.7 KB (759653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9527bc42b25341df02b03ea0015db4b21eaece4f3fac0f6aad4216a0eb65076`

```dockerfile
```

-	Layers:
	-	`sha256:8b26a7c1292b91ca48e8fb9e660db26bff0ef5e3cbbe1a2518554ae663de4075`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 741.7 KB (741709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a44a8eaa3f69c139fc2f80d23792c493cb6d37dc65c27016d78067d76cd6e2`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 17.9 KB (17944 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-data`

```console
$ docker pull influxdb@sha256:649d49561ec5dc9b5ecea81e0f6b2f5be880d0595e0c056032d90d4b43e12960
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:3e54158526ef6d58ac83ca560783db87c5c36efd36f9a518869d3dc0267b5fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114692496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f94e6337af63f9d58bdbe07ec5e00f5b96530a458e830ec55171880db92779`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:32:56 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 03 Feb 2026 03:32:56 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 03 Feb 2026 03:32:56 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 03 Feb 2026 03:32:56 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 03:32:56 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:32:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:32:56 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 03 Feb 2026 03:32:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:32:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3342e0c344a48271fae633c4dfcfb346d596bed50e445a32161118064363a6`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7235fdf3c9ec30c6605496ec3dc25adba578b2c81229e85a9e074b0c48c00005`  
		Last Modified: Tue, 03 Feb 2026 03:33:09 GMT  
		Size: 42.2 MB (42165718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94a4a40254cff93c4db8b3513c1223fb865baebd0bec9ebda4d6f2d19abfe4f`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904e172d1f287f5f44b0919de34f01fe7668af75aa89b58ead2a78691f09d5cd`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d36d3908917495c59b40629c824d83a255e896afe6002d656966ddccf20691`  
		Last Modified: Tue, 03 Feb 2026 03:33:09 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:063696b39a6073e19e10620284048eb5583ecb719844a7a36b860500e9c5b66b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a4fbcae227a219d0c7888a61853aa3d0774f59f197757e2d7f555a488009e6`

```dockerfile
```

-	Layers:
	-	`sha256:465f3e547e304dec5c4331f4d87f5f2ef1d3b3a70abb8056ae8d9eb11247a8b8`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 4.7 MB (4684406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ab196cf03d82181dcbddae15361fd0e20175db94410e49fac0450e2d48fa7`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-data-alpine`

```console
$ docker pull influxdb@sha256:9d0b51aeab711df34e37e895e2d1469ec43a29095ece120902603c3cf21efa38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:02153a74beabb3f96b259f8507d7421339482549e50cc5d2258f0b2ce9e6c864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46960587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f4d43e203a1a92b5ff368450db5c6fe8325a6b765befd58abf19f686fea967`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:25:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:25:51 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:25:55 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 28 Jan 2026 03:25:55 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:25:56 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:25:56 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:25:56 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:25:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:25:56 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:25:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:25:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0263a1e24ffa0829b1f805a2d6c158c33fea253d7ef254f2494681fa2d006a`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9672fa9124cf983f0543c61ea1dde339b6705eb7d1e2b05d760b6b5938097078`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 1.2 MB (1224754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f2e30e450bd646642d30a6713818d18161df47157ce401b61f69011dc8633f`  
		Last Modified: Wed, 28 Jan 2026 03:26:06 GMT  
		Size: 42.1 MB (42105918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f04de5a1e581d806f89cfbb2942929a3f7241a270158df81e7c34383fd931`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68edddde0b5f46997714b4dde35e1dc7f0e2fc457f720dd8975b0492c124bb0`  
		Last Modified: Wed, 28 Jan 2026 03:26:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80a545e019203b789e56a39b97bb112b148b5a35d4bfa4e5e047435ac01313c`  
		Last Modified: Wed, 28 Jan 2026 03:26:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f1fe57771330dc344971ded307b8c5957352e6c41c6b4052a3a2de810fed9266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.6 KB (785589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a4234b2573554d959bb8763239bdda077e7007d27002de0f9dab694364e51b`

```dockerfile
```

-	Layers:
	-	`sha256:86054862a078c59646ba2b5c08117a00b07c42589123f4297ea77aab085bb20d`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 769.0 KB (768993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f041e72a4e9d944868da8607a414ca998a5a43702d92dd969cde2a705e241ca`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-meta`

```console
$ docker pull influxdb@sha256:5f3050cf3558da40896d9849217f5c0e35226808562909cdc9127ea685280d7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:8bc88e165a8c46c42ad22f0ebbeab4c1562a112bf251cde06f9516f2d4b1e76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91121710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5efb0acebd2cc78ce191050ca0ba9fb3f6abe26243071ba03d9537b867642f9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:33:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:33:02 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 03 Feb 2026 03:33:02 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 03 Feb 2026 03:33:02 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 03 Feb 2026 03:33:02 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 03 Feb 2026 03:33:02 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:33:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:33:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:33:02 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6523b81168533bbcd7b027035018575e31ac7f473a62e5be7319a1abd4449a`  
		Last Modified: Tue, 03 Feb 2026 03:33:11 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162da3cefe6da12370d22d65541c5f1cd07c73ebbba298fa4a32b926217deb85`  
		Last Modified: Tue, 03 Feb 2026 03:33:11 GMT  
		Size: 18.6 MB (18596147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac39049d45a69c0b814c812562698c7c60f501f5ba6b5253b3c097987f52c8b`  
		Last Modified: Tue, 03 Feb 2026 03:33:11 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96594ee04fa23dfa7f6118b01a023a0202e589722c5f30a9d94dc434dddf553a`  
		Last Modified: Tue, 03 Feb 2026 03:33:11 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:0bafc3ac5496395ec8876bc4fcbc59b5844e044536c960cf69218b01577dc0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e0cf8fdf0d559f361e7a077440f56472ec44927de2de1b207bfa150bd64f80`

```dockerfile
```

-	Layers:
	-	`sha256:08ee2c14327be46b40fa2fdad146cd31d70f93fbf547714a1caf10b76103a8fc`  
		Last Modified: Tue, 03 Feb 2026 03:33:11 GMT  
		Size: 4.6 MB (4591249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3534eaf431a735ece3d84dc463f0204d1c421d45714c1203417cad4417075d7`  
		Last Modified: Tue, 03 Feb 2026 03:33:11 GMT  
		Size: 13.0 KB (13024 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-meta-alpine`

```console
$ docker pull influxdb@sha256:249c7bd6c3cb8f7bbba327cf37a3b1005d6cd347d8a692c8ceaff56d18fb7891
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:44ad70f43101c494e4d04ab932049e45759c24ed812f029b96c79c7e18b7f5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23403364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c9203475562a7d8b438ef3bdf218f4cdb0516b9023ca9c4f7beb027b1dd551`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:26:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:26:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:26:49 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 28 Jan 2026 03:26:49 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:26:49 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 28 Jan 2026 03:26:49 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 28 Jan 2026 03:26:49 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:26:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:26:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:26:49 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ce9bebb946b2c426c9224e7360d845b78bd397b82149cb1f1fa0be2b2e876c`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a219cf2dafb437a398f6465d6bb676c776f0a32983a6488d2a5a52da44ff00`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 1.2 MB (1224764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b99563435aacc7f0c7f9f7b4b1850b98aa7b8f25747307c2be2310f2a08d95`  
		Last Modified: Wed, 28 Jan 2026 03:26:57 GMT  
		Size: 18.5 MB (18549891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a807e577681eeebd1dcac3ab7d414179b8fe0902833964ccc7e1f2fc51789`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9608b4806a31ae3e7d94b72f7606acf6161b5a5c2d16ac725d6c236e2b7a93`  
		Last Modified: Wed, 28 Jan 2026 03:26:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:0b3947f754f901b0eee6981e99cd9d177d98f9208d60e99599a2182ee456cb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 KB (691589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf3c479b5f2c96864cbcd1eeccb783380ad8a72539788725799c866d6198c2b`

```dockerfile
```

-	Layers:
	-	`sha256:01b16cc3b5518976d91b8bddbc7009f186a3aef03547cabb60c8a13ddbbc8227`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 676.6 KB (676622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1541f8caff84dbcdb88fbc06c12d3a170bfb849a19f16feb4f4857708b70317a`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 15.0 KB (14967 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12`

```console
$ docker pull influxdb@sha256:41bdb4c116f8fb7fa23f4c9a8acb18a2f285157470d75aefa0e805ab53ff9ff6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12` - linux; amd64

```console
$ docker pull influxdb@sha256:be548122773cf91bfabe8d8e2e90d65a6922173598be52e5631ae1c4ccadb6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113855989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47373ec902106da5d6dfffaab8193e8ea65dc19b62410839f0dd96387e1be7b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:27 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 03 Feb 2026 03:32:32 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 03 Feb 2026 03:32:32 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:32 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 03 Feb 2026 03:32:32 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 03:32:32 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:32:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:32:32 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 03 Feb 2026 03:32:32 GMT
USER influxdb
# Tue, 03 Feb 2026 03:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:32:32 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac6263366aa57406b33c4f8c233ced7c93d1c91ab49c222420b1f2acd1621c8`  
		Last Modified: Tue, 03 Feb 2026 03:32:46 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196b02c9a5abac782438a583dfaa2ecf6eaeb1cc3798e132d45e9ce300c864d3`  
		Last Modified: Tue, 03 Feb 2026 03:32:47 GMT  
		Size: 41.3 MB (41333146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02c7c3a3bb0d186248525f6970e77448b881e3f3de047305a55f2bebd10da7c`  
		Last Modified: Tue, 03 Feb 2026 03:32:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f0c850a2b81760b41e0bdd36b492ad38042ffed592f6aba79df3b52f288357`  
		Last Modified: Tue, 03 Feb 2026 03:32:46 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d79f54ba6d969c654a4bc6b95c00203a5ac804e36625bccc1234a7d9e58115`  
		Last Modified: Tue, 03 Feb 2026 03:32:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:cf9042ec2f1a4501cc8431eaacaa593276610aa798457c0c28761d8d8982529e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8075eea159aaa3720f825641baa4fcb76388fa215ba187644166d0429c061749`

```dockerfile
```

-	Layers:
	-	`sha256:759b369010259086076c90c705f0edefdfc32a713436d7c6c8c72ccb972a618d`  
		Last Modified: Tue, 03 Feb 2026 03:32:46 GMT  
		Size: 4.7 MB (4676456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:009d9730aa8ccd1a3638dd4c6924b1ec3fc0a3591905549c58429b84e7769a8b`  
		Last Modified: Tue, 03 Feb 2026 03:32:46 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e973eae51bc92d6b143983a5512e755348c7af425d75729db0606951bb049e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110110602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86736c481986c630610eb84a1c3ae8e2f2cc9bbd4101c6412077ace4f98d209a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:51:26 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 03 Feb 2026 03:51:31 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 03 Feb 2026 03:51:31 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:51:31 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 03 Feb 2026 03:51:31 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 03:51:31 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:51:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:51:31 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 03 Feb 2026 03:51:31 GMT
USER influxdb
# Tue, 03 Feb 2026 03:51:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:51:31 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85480bb13923a454c3b68621a22c5bdf4fcc43e83917d924d479ab0c3aa3e8a`  
		Last Modified: Tue, 03 Feb 2026 03:51:43 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdac1e8aa4e8f82f59b4449996ec8d98613c1fa4b1059b1f3cf4453a5e2df38`  
		Last Modified: Tue, 03 Feb 2026 03:51:44 GMT  
		Size: 38.1 MB (38136892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3804ee83b1d3db261e75f3c2d0f5394d35788cea311cee0e1bdc1ab1fd8990`  
		Last Modified: Tue, 03 Feb 2026 03:51:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4c434392f0c37ed4dfbb92c6a7db30d8b7059586ee0752365dac38001b3d6b`  
		Last Modified: Tue, 03 Feb 2026 03:51:43 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e182468fe50014d090ef774ba6dd54c7538cdc465491a6ccc215a063c347c3f9`  
		Last Modified: Tue, 03 Feb 2026 03:51:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:1fe7e04b95bc9a3c6539bb83b845d4b68465934af5214f06afe33c9bc8e99ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8bd53c9a15790803baa2ef9b235233c7493a8c1d8f93b05ea09edcec5521ffa`

```dockerfile
```

-	Layers:
	-	`sha256:3e189e23561963ba28867ce606d673712a4ed82249fc0f08e1dc5b0dcffdd9e4`  
		Last Modified: Tue, 03 Feb 2026 03:51:43 GMT  
		Size: 4.7 MB (4675914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9b135dc5e38ae9f7b90796ac07f5e9ffb53aa6ed8b6f579bd4de04a2ffec587`  
		Last Modified: Tue, 03 Feb 2026 03:51:42 GMT  
		Size: 16.6 KB (16551 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-alpine`

```console
$ docker pull influxdb@sha256:1ed16e0f6a44ab61a30357566845efbb9757556851e6ff97227f939bf9ef9ace
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:697aba0e3c65d5d7bd8c0165468ba9ee24657f504bb4366fece150b28f019a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46124218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb897a5f792495e87d9871b6a4cfc773bd6606d7bc580daf4ff262360e9c04d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:23:21 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 28 Jan 2026 03:23:26 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:23:26 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:23:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
USER influxdb
# Wed, 28 Jan 2026 03:23:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:23:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61ad874caf1ce155d9c06c85c089035ff4b41fea8f68219cb60604fecea628f`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 1.2 MB (1225476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f59042c15009bf41c0b1fa6c4d2d2d13d0250f49e1409fb7b663adc462759b`  
		Last Modified: Wed, 28 Jan 2026 03:23:37 GMT  
		Size: 41.3 MB (41252292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed17935cb0b9555361ea5defc075520b1cdccd69d5a58d7e269415bee692cee`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d76182047c6a6ca57e871f8736596a2ae48b8a3c50277aedeeb7987a622c6f`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 994.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4fb1c6df23e845268a733a445e5db0893ba7589591cadeabba1bdf3adf782c`  
		Last Modified: Wed, 28 Jan 2026 03:23:37 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ba8b159859dfc44049e5332e08c60d8b36b38fc5e1d118748fe8e3e1543924`  
		Last Modified: Wed, 28 Jan 2026 03:23:37 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:af2b5dd8ad0d3b16b3907ff491d74d1f2eff068de322e7489c77bd75466cd8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **780.5 KB (780479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51dc09838f56b2799381d5dd1c3400f40ea2244acca53eabafae485097494bf9`

```dockerfile
```

-	Layers:
	-	`sha256:f39e15f06b57000511387e30703a81694cd535187db4291a2e8f5bcefece88a6`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 761.9 KB (761859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9426c81519fa2e633147ad49e1850cde661e950ff86aefd90f840a0cd91d5c96`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 18.6 KB (18620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a15f5bc8b2ce1d70a31b981c371a1ddd88c6fc05c655c7e01b57eecaf60fbbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43343070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4654f5bc4db16a713150f336f9aac2a58bc3dfb28052ad26fdc2db98f8d1d717`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:34 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 28 Jan 2026 03:15:40 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:40 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:15:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
USER influxdb
# Wed, 28 Jan 2026 03:15:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad49504157754b82690dc411a4cbb1be979c94a1504554cc7508eb53848d9aaa`  
		Last Modified: Wed, 28 Jan 2026 03:15:50 GMT  
		Size: 1.3 MB (1290781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5d1cb0eb9bcf36e7b5a1a4000c5aece49077b899de952de6fdbd89c9c1f44b`  
		Last Modified: Wed, 28 Jan 2026 03:15:51 GMT  
		Size: 38.1 MB (38056702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1137d619a385938b5d7d7306b62a613a6dbb383adfd1ec3a55ce047164213cd1`  
		Last Modified: Wed, 28 Jan 2026 03:15:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef4649756164c4e09b5e20f42da696b65fd206aa9a9e69d940360af42044b28`  
		Last Modified: Wed, 28 Jan 2026 03:15:49 GMT  
		Size: 993.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1622ae5fef1f8a1581c49244f92707dde2199a2db553408fb31beec7b70b181e`  
		Last Modified: Wed, 28 Jan 2026 03:15:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946d050ae0ebead10e2f4ab1c542a8b9ddf94d0784aa98106e5c9bd7dbd02631`  
		Last Modified: Wed, 28 Jan 2026 03:15:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:edfd9ff1eb419bbf315b4102159bb5d501769546111a9c02e7e64d25684fa482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.8 KB (779816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bd24f011bd6bdf62cee047d5433e2b6dba99042b7d6c09aa052a11bb91f17f`

```dockerfile
```

-	Layers:
	-	`sha256:a51c507fdc8870eba3993722731f2c5c18c27320de1587e98a2662a90b734787`  
		Last Modified: Wed, 28 Jan 2026 03:15:49 GMT  
		Size: 761.1 KB (761088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94d21d56468ffa602372ea8026b8acdae37f5ee8aab4afbb5aeda345db5c31f9`  
		Last Modified: Wed, 28 Jan 2026 03:15:49 GMT  
		Size: 18.7 KB (18728 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-data`

```console
$ docker pull influxdb@sha256:6ee054f5264bdf35995032887a42b386ae922ccfe379ea754afecbc2e73bf52a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data` - linux; amd64

```console
$ docker pull influxdb@sha256:bd87962f04b5e5fd56acf0f5935868b4efca456b6fb8d1b3a6174d7151b0a8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114841526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d161b120e02516f0496e96c28167299a89d72e9f3a72d706593bd1360db73bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 03 Feb 2026 03:32:49 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 03:32:49 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:32:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:32:49 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf28d2500a471d1dfc3178dfb606f71b5e9ed292e422655433c53cbe73a6ca`  
		Last Modified: Tue, 03 Feb 2026 03:33:03 GMT  
		Size: 42.3 MB (42319821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13e3563e88a57ac2dbc95ecc269722c6eef212fb6a2aa36dc48ea85181dc9c9`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecebd9eeb3c29a4676848dfc8b528ad9036268a2b9d18f75976e281547931e6`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d318862ee1f525bef0688496e8db3ece435fa6af7bda0b6725f96fe856f198`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:9b708c6661337b3f859fd3a36f053b9ab9a12fbb2cf84b2ca62c18c9b8db5ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4700469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a28e355e551d575ad6a0d1cf2a567adf5be90a12bb7ea104cdd2c409a90c30`

```dockerfile
```

-	Layers:
	-	`sha256:5cafb353c28ab90688350fab88cecccd4ed633f9a275142cfc1fb890ad0925a0`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 4.7 MB (4686392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcaf37ce8ad2d98b4f978727f83d07f5c90f5f2ed44eccf2ffdc8e4769d81d91`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-data-alpine`

```console
$ docker pull influxdb@sha256:230aced0d72a917905c28e8370266348fb49894a4e1d090c47765a1488e94bff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:40d2fef5a316bf72ec0b29c322a7cf01fbd7046fad6e09edef3afd6a2a51f192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47123756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8324e71acc24adb0423f7eb4de13354493b40f765bdb36448d77ce375caa87c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:24:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 28 Jan 2026 03:24:11 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:24:11 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:24:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:24:11 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adc499747d2c1716d5193ed87e0f6684b5f7da3ad6b0d2bdfc84d65ed106d36`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 1.2 MB (1225465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a172153dcef0bec4a9c7bb4c587f4400c9485a79c347dec788239589954f4770`  
		Last Modified: Wed, 28 Jan 2026 03:24:22 GMT  
		Size: 42.3 MB (42252778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b330c6f2273441c4cece26de32b1b56b5641f92928b4b5256a15fd7ef0db1a6`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb3efac6bd9c420eddfe57595ec744fa728401020c9af575cb9cdbe12776f5f`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1f1384e53b8afac073280a7d6b42b05cfeb3ad8ff3c328242a61d8f88d4018`  
		Last Modified: Wed, 28 Jan 2026 03:24:22 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fff49aac562db0793d72005156712fb335c4f0488b91b3f35e434498d2e282a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **791.6 KB (791580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cbe541688ac6e58740d2ecbecb6eaa4446654bb8c3635d47c1614319c2135d`

```dockerfile
```

-	Layers:
	-	`sha256:7746afe39499c0509347119e90a393e2f741f8c2e4a54628af8774335219ffeb`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 776.1 KB (776122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a10bcf68f284ed3ad3af63a4766b3825d0a6fb102c1dc2b1199ddd247f8f9cef`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 15.5 KB (15458 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-meta`

```console
$ docker pull influxdb@sha256:595d3bf0fcbdaa44860691745361c22257a432d7498691e180afec4cf3038ab1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:cf5db12b97a9cff6ccc66d57f091f8e942dec53d549a3c4327f74c5513fb5ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91301354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6d9d34df08484050b015bb39f36ca5833ca36a069fc2521171ac563a18089a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:45 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 03 Feb 2026 03:32:45 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 03 Feb 2026 03:32:45 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 03 Feb 2026 03:32:45 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:32:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:32:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:32:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c301e5663c93730e853c177c2921beb662e8af6fd669efac8f485fcab5976e52`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 18.8 MB (18780858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52acbb2fe909f154b6eea1c07a48fd8e021e522282b1ad8d2d8a0896f8c940a3`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edea7eb3d12825920978031ef043c87591be9a1d18d4da302b7f5f32ef553b3`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:5ae9375a3129de2c571770f01c081367e812da11a7784f6ff1d6d479656df566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a6630862709599dc01c2841fc7a2a536d1fe8edefdb660b018644dda299f27`

```dockerfile
```

-	Layers:
	-	`sha256:741f6b7444af98584961f6b6ddab2d605dc0082a3e1fdc69ad7638fcdab8291e`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 4.6 MB (4591555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:727c7e09de0e967fbf5e91d8496e43c8ff8199c68a6f024a0136754d2fa2e610`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 12.6 KB (12591 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-meta-alpine`

```console
$ docker pull influxdb@sha256:aecaf75c0592866bc0a7c2639bb83f72193dda8ca322e9434210831a02a4857a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:334fda21d7660dabebf415a7630e82d71c49a482457d86edd5a02adf9ade1164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23592932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97dfff6219d548cae54fee570f6f3b37ac16ff0e9424df4cfe959bcf9b715512`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:24:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 28 Jan 2026 03:24:58 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influxd-ctl'             'influxdb-*/usr/bin/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 28 Jan 2026 03:24:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:24:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:24:58 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adc499747d2c1716d5193ed87e0f6684b5f7da3ad6b0d2bdfc84d65ed106d36`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 1.2 MB (1225465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdedda1ccaa8c658e38e6dd03b7ae881fe041e412d88964c2eeb69cacaa9d72`  
		Last Modified: Wed, 28 Jan 2026 03:25:05 GMT  
		Size: 18.7 MB (18723159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c532d4cfc611beb0d944a9d3a0ecb4f69dfd08641f9c026a71b9183ba72aeb`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0374a0e06643bd5572653262d38d90caf085dff084fc64403ebb1555477ec00e`  
		Last Modified: Wed, 28 Jan 2026 03:25:05 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:627437226023c906b3c6b7de5bce011926f537ee0fa9a386d09b87721cc83460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.9 KB (695917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987b431e9e9fe1201a9d3d2a53cbb79bad12a66fe71f7caaa35c13d123e4b70f`

```dockerfile
```

-	Layers:
	-	`sha256:6969b9ff35276f6935e71043cc1ec394f9218dd77481815cd0b8d155f1a4a451`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 682.1 KB (682071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d790fe636454d04353dbcafa3c3eb838b08379bec575783d2659976da7381a07`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 13.8 KB (13846 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2`

```console
$ docker pull influxdb@sha256:41bdb4c116f8fb7fa23f4c9a8acb18a2f285157470d75aefa0e805ab53ff9ff6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.2` - linux; amd64

```console
$ docker pull influxdb@sha256:be548122773cf91bfabe8d8e2e90d65a6922173598be52e5631ae1c4ccadb6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113855989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47373ec902106da5d6dfffaab8193e8ea65dc19b62410839f0dd96387e1be7b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:27 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 03 Feb 2026 03:32:32 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 03 Feb 2026 03:32:32 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:32 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 03 Feb 2026 03:32:32 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 03:32:32 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:32:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:32:32 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 03 Feb 2026 03:32:32 GMT
USER influxdb
# Tue, 03 Feb 2026 03:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:32:32 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac6263366aa57406b33c4f8c233ced7c93d1c91ab49c222420b1f2acd1621c8`  
		Last Modified: Tue, 03 Feb 2026 03:32:46 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196b02c9a5abac782438a583dfaa2ecf6eaeb1cc3798e132d45e9ce300c864d3`  
		Last Modified: Tue, 03 Feb 2026 03:32:47 GMT  
		Size: 41.3 MB (41333146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02c7c3a3bb0d186248525f6970e77448b881e3f3de047305a55f2bebd10da7c`  
		Last Modified: Tue, 03 Feb 2026 03:32:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f0c850a2b81760b41e0bdd36b492ad38042ffed592f6aba79df3b52f288357`  
		Last Modified: Tue, 03 Feb 2026 03:32:46 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d79f54ba6d969c654a4bc6b95c00203a5ac804e36625bccc1234a7d9e58115`  
		Last Modified: Tue, 03 Feb 2026 03:32:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2` - unknown; unknown

```console
$ docker pull influxdb@sha256:cf9042ec2f1a4501cc8431eaacaa593276610aa798457c0c28761d8d8982529e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8075eea159aaa3720f825641baa4fcb76388fa215ba187644166d0429c061749`

```dockerfile
```

-	Layers:
	-	`sha256:759b369010259086076c90c705f0edefdfc32a713436d7c6c8c72ccb972a618d`  
		Last Modified: Tue, 03 Feb 2026 03:32:46 GMT  
		Size: 4.7 MB (4676456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:009d9730aa8ccd1a3638dd4c6924b1ec3fc0a3591905549c58429b84e7769a8b`  
		Last Modified: Tue, 03 Feb 2026 03:32:46 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e973eae51bc92d6b143983a5512e755348c7af425d75729db0606951bb049e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110110602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86736c481986c630610eb84a1c3ae8e2f2cc9bbd4101c6412077ace4f98d209a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:51:26 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 03 Feb 2026 03:51:31 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 03 Feb 2026 03:51:31 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:51:31 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 03 Feb 2026 03:51:31 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 03:51:31 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:51:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:51:31 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 03 Feb 2026 03:51:31 GMT
USER influxdb
# Tue, 03 Feb 2026 03:51:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:51:31 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85480bb13923a454c3b68621a22c5bdf4fcc43e83917d924d479ab0c3aa3e8a`  
		Last Modified: Tue, 03 Feb 2026 03:51:43 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdac1e8aa4e8f82f59b4449996ec8d98613c1fa4b1059b1f3cf4453a5e2df38`  
		Last Modified: Tue, 03 Feb 2026 03:51:44 GMT  
		Size: 38.1 MB (38136892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3804ee83b1d3db261e75f3c2d0f5394d35788cea311cee0e1bdc1ab1fd8990`  
		Last Modified: Tue, 03 Feb 2026 03:51:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4c434392f0c37ed4dfbb92c6a7db30d8b7059586ee0752365dac38001b3d6b`  
		Last Modified: Tue, 03 Feb 2026 03:51:43 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e182468fe50014d090ef774ba6dd54c7538cdc465491a6ccc215a063c347c3f9`  
		Last Modified: Tue, 03 Feb 2026 03:51:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2` - unknown; unknown

```console
$ docker pull influxdb@sha256:1fe7e04b95bc9a3c6539bb83b845d4b68465934af5214f06afe33c9bc8e99ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8bd53c9a15790803baa2ef9b235233c7493a8c1d8f93b05ea09edcec5521ffa`

```dockerfile
```

-	Layers:
	-	`sha256:3e189e23561963ba28867ce606d673712a4ed82249fc0f08e1dc5b0dcffdd9e4`  
		Last Modified: Tue, 03 Feb 2026 03:51:43 GMT  
		Size: 4.7 MB (4675914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9b135dc5e38ae9f7b90796ac07f5e9ffb53aa6ed8b6f579bd4de04a2ffec587`  
		Last Modified: Tue, 03 Feb 2026 03:51:42 GMT  
		Size: 16.6 KB (16551 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-alpine`

```console
$ docker pull influxdb@sha256:1ed16e0f6a44ab61a30357566845efbb9757556851e6ff97227f939bf9ef9ace
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:697aba0e3c65d5d7bd8c0165468ba9ee24657f504bb4366fece150b28f019a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46124218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb897a5f792495e87d9871b6a4cfc773bd6606d7bc580daf4ff262360e9c04d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:23:21 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 28 Jan 2026 03:23:26 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:23:26 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:23:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
USER influxdb
# Wed, 28 Jan 2026 03:23:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:23:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61ad874caf1ce155d9c06c85c089035ff4b41fea8f68219cb60604fecea628f`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 1.2 MB (1225476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f59042c15009bf41c0b1fa6c4d2d2d13d0250f49e1409fb7b663adc462759b`  
		Last Modified: Wed, 28 Jan 2026 03:23:37 GMT  
		Size: 41.3 MB (41252292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed17935cb0b9555361ea5defc075520b1cdccd69d5a58d7e269415bee692cee`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d76182047c6a6ca57e871f8736596a2ae48b8a3c50277aedeeb7987a622c6f`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 994.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4fb1c6df23e845268a733a445e5db0893ba7589591cadeabba1bdf3adf782c`  
		Last Modified: Wed, 28 Jan 2026 03:23:37 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ba8b159859dfc44049e5332e08c60d8b36b38fc5e1d118748fe8e3e1543924`  
		Last Modified: Wed, 28 Jan 2026 03:23:37 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:af2b5dd8ad0d3b16b3907ff491d74d1f2eff068de322e7489c77bd75466cd8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **780.5 KB (780479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51dc09838f56b2799381d5dd1c3400f40ea2244acca53eabafae485097494bf9`

```dockerfile
```

-	Layers:
	-	`sha256:f39e15f06b57000511387e30703a81694cd535187db4291a2e8f5bcefece88a6`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 761.9 KB (761859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9426c81519fa2e633147ad49e1850cde661e950ff86aefd90f840a0cd91d5c96`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 18.6 KB (18620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a15f5bc8b2ce1d70a31b981c371a1ddd88c6fc05c655c7e01b57eecaf60fbbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43343070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4654f5bc4db16a713150f336f9aac2a58bc3dfb28052ad26fdc2db98f8d1d717`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:34 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 28 Jan 2026 03:15:40 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:40 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:15:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
USER influxdb
# Wed, 28 Jan 2026 03:15:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad49504157754b82690dc411a4cbb1be979c94a1504554cc7508eb53848d9aaa`  
		Last Modified: Wed, 28 Jan 2026 03:15:50 GMT  
		Size: 1.3 MB (1290781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5d1cb0eb9bcf36e7b5a1a4000c5aece49077b899de952de6fdbd89c9c1f44b`  
		Last Modified: Wed, 28 Jan 2026 03:15:51 GMT  
		Size: 38.1 MB (38056702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1137d619a385938b5d7d7306b62a613a6dbb383adfd1ec3a55ce047164213cd1`  
		Last Modified: Wed, 28 Jan 2026 03:15:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef4649756164c4e09b5e20f42da696b65fd206aa9a9e69d940360af42044b28`  
		Last Modified: Wed, 28 Jan 2026 03:15:49 GMT  
		Size: 993.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1622ae5fef1f8a1581c49244f92707dde2199a2db553408fb31beec7b70b181e`  
		Last Modified: Wed, 28 Jan 2026 03:15:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946d050ae0ebead10e2f4ab1c542a8b9ddf94d0784aa98106e5c9bd7dbd02631`  
		Last Modified: Wed, 28 Jan 2026 03:15:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:edfd9ff1eb419bbf315b4102159bb5d501769546111a9c02e7e64d25684fa482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.8 KB (779816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bd24f011bd6bdf62cee047d5433e2b6dba99042b7d6c09aa052a11bb91f17f`

```dockerfile
```

-	Layers:
	-	`sha256:a51c507fdc8870eba3993722731f2c5c18c27320de1587e98a2662a90b734787`  
		Last Modified: Wed, 28 Jan 2026 03:15:49 GMT  
		Size: 761.1 KB (761088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94d21d56468ffa602372ea8026b8acdae37f5ee8aab4afbb5aeda345db5c31f9`  
		Last Modified: Wed, 28 Jan 2026 03:15:49 GMT  
		Size: 18.7 KB (18728 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-data`

```console
$ docker pull influxdb@sha256:6ee054f5264bdf35995032887a42b386ae922ccfe379ea754afecbc2e73bf52a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-data` - linux; amd64

```console
$ docker pull influxdb@sha256:bd87962f04b5e5fd56acf0f5935868b4efca456b6fb8d1b3a6174d7151b0a8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114841526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d161b120e02516f0496e96c28167299a89d72e9f3a72d706593bd1360db73bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 03 Feb 2026 03:32:49 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 03:32:49 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:32:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:32:49 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf28d2500a471d1dfc3178dfb606f71b5e9ed292e422655433c53cbe73a6ca`  
		Last Modified: Tue, 03 Feb 2026 03:33:03 GMT  
		Size: 42.3 MB (42319821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13e3563e88a57ac2dbc95ecc269722c6eef212fb6a2aa36dc48ea85181dc9c9`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecebd9eeb3c29a4676848dfc8b528ad9036268a2b9d18f75976e281547931e6`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d318862ee1f525bef0688496e8db3ece435fa6af7bda0b6725f96fe856f198`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:9b708c6661337b3f859fd3a36f053b9ab9a12fbb2cf84b2ca62c18c9b8db5ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4700469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a28e355e551d575ad6a0d1cf2a567adf5be90a12bb7ea104cdd2c409a90c30`

```dockerfile
```

-	Layers:
	-	`sha256:5cafb353c28ab90688350fab88cecccd4ed633f9a275142cfc1fb890ad0925a0`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 4.7 MB (4686392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcaf37ce8ad2d98b4f978727f83d07f5c90f5f2ed44eccf2ffdc8e4769d81d91`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-data-alpine`

```console
$ docker pull influxdb@sha256:230aced0d72a917905c28e8370266348fb49894a4e1d090c47765a1488e94bff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:40d2fef5a316bf72ec0b29c322a7cf01fbd7046fad6e09edef3afd6a2a51f192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47123756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8324e71acc24adb0423f7eb4de13354493b40f765bdb36448d77ce375caa87c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:24:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 28 Jan 2026 03:24:11 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:24:11 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:24:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:24:11 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adc499747d2c1716d5193ed87e0f6684b5f7da3ad6b0d2bdfc84d65ed106d36`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 1.2 MB (1225465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a172153dcef0bec4a9c7bb4c587f4400c9485a79c347dec788239589954f4770`  
		Last Modified: Wed, 28 Jan 2026 03:24:22 GMT  
		Size: 42.3 MB (42252778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b330c6f2273441c4cece26de32b1b56b5641f92928b4b5256a15fd7ef0db1a6`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb3efac6bd9c420eddfe57595ec744fa728401020c9af575cb9cdbe12776f5f`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1f1384e53b8afac073280a7d6b42b05cfeb3ad8ff3c328242a61d8f88d4018`  
		Last Modified: Wed, 28 Jan 2026 03:24:22 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fff49aac562db0793d72005156712fb335c4f0488b91b3f35e434498d2e282a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **791.6 KB (791580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cbe541688ac6e58740d2ecbecb6eaa4446654bb8c3635d47c1614319c2135d`

```dockerfile
```

-	Layers:
	-	`sha256:7746afe39499c0509347119e90a393e2f741f8c2e4a54628af8774335219ffeb`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 776.1 KB (776122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a10bcf68f284ed3ad3af63a4766b3825d0a6fb102c1dc2b1199ddd247f8f9cef`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 15.5 KB (15458 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-meta`

```console
$ docker pull influxdb@sha256:595d3bf0fcbdaa44860691745361c22257a432d7498691e180afec4cf3038ab1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:cf5db12b97a9cff6ccc66d57f091f8e942dec53d549a3c4327f74c5513fb5ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91301354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6d9d34df08484050b015bb39f36ca5833ca36a069fc2521171ac563a18089a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:45 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 03 Feb 2026 03:32:45 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 03 Feb 2026 03:32:45 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 03 Feb 2026 03:32:45 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:32:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:32:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:32:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c301e5663c93730e853c177c2921beb662e8af6fd669efac8f485fcab5976e52`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 18.8 MB (18780858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52acbb2fe909f154b6eea1c07a48fd8e021e522282b1ad8d2d8a0896f8c940a3`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edea7eb3d12825920978031ef043c87591be9a1d18d4da302b7f5f32ef553b3`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:5ae9375a3129de2c571770f01c081367e812da11a7784f6ff1d6d479656df566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a6630862709599dc01c2841fc7a2a536d1fe8edefdb660b018644dda299f27`

```dockerfile
```

-	Layers:
	-	`sha256:741f6b7444af98584961f6b6ddab2d605dc0082a3e1fdc69ad7638fcdab8291e`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 4.6 MB (4591555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:727c7e09de0e967fbf5e91d8496e43c8ff8199c68a6f024a0136754d2fa2e610`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 12.6 KB (12591 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-meta-alpine`

```console
$ docker pull influxdb@sha256:aecaf75c0592866bc0a7c2639bb83f72193dda8ca322e9434210831a02a4857a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:334fda21d7660dabebf415a7630e82d71c49a482457d86edd5a02adf9ade1164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23592932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97dfff6219d548cae54fee570f6f3b37ac16ff0e9424df4cfe959bcf9b715512`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:24:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 28 Jan 2026 03:24:58 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influxd-ctl'             'influxdb-*/usr/bin/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 28 Jan 2026 03:24:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:24:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:24:58 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adc499747d2c1716d5193ed87e0f6684b5f7da3ad6b0d2bdfc84d65ed106d36`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 1.2 MB (1225465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdedda1ccaa8c658e38e6dd03b7ae881fe041e412d88964c2eeb69cacaa9d72`  
		Last Modified: Wed, 28 Jan 2026 03:25:05 GMT  
		Size: 18.7 MB (18723159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c532d4cfc611beb0d944a9d3a0ecb4f69dfd08641f9c026a71b9183ba72aeb`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0374a0e06643bd5572653262d38d90caf085dff084fc64403ebb1555477ec00e`  
		Last Modified: Wed, 28 Jan 2026 03:25:05 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:627437226023c906b3c6b7de5bce011926f537ee0fa9a386d09b87721cc83460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.9 KB (695917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987b431e9e9fe1201a9d3d2a53cbb79bad12a66fe71f7caaa35c13d123e4b70f`

```dockerfile
```

-	Layers:
	-	`sha256:6969b9ff35276f6935e71043cc1ec394f9218dd77481815cd0b8d155f1a4a451`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 682.1 KB (682071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d790fe636454d04353dbcafa3c3eb838b08379bec575783d2659976da7381a07`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 13.8 KB (13846 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:8e911da5f7b482230e61fe4bad9af0697d97a75e087f19f5f0ddfee62c2bd686
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:3e23a8f949851d197977fd09f19d9f1eb026e20c47a7bc50e544342b1271b0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107232786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6152aaa4c9999ec462d1f8603b21da2898ea325d68ea261d6e968c290a56c832`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:46:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:01 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 03 Feb 2026 02:46:01 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 03 Feb 2026 02:46:03 GMT
ENV GOSU_VER=1.19
# Tue, 03 Feb 2026 02:46:03 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:46:03 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 03 Feb 2026 02:46:03 GMT
ENV INFLUXDB_PR=-2
# Tue, 03 Feb 2026 02:46:03 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 03 Feb 2026 02:46:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 03 Feb 2026 02:46:06 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 03 Feb 2026 02:46:07 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 03 Feb 2026 02:46:07 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 03 Feb 2026 02:46:07 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 03 Feb 2026 02:46:07 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 03 Feb 2026 02:46:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:46:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:07 GMT
CMD ["influxd"]
# Tue, 03 Feb 2026 02:46:07 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 02:46:07 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 03 Feb 2026 02:46:07 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 03 Feb 2026 02:46:07 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 03 Feb 2026 02:46:07 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebdc098e5a0cdaffe8ed5d5f890eebd95af1721e8ec4546756ceb4f430163e`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 9.8 MB (9798212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc0e0dd72fbd9e712238621797c89d4cb234ec5d85c98dfe1fdfa0010f6a4f7`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 6.2 MB (6156965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47df6264947c0be6c65a68d2f4c00d24721cdd03025fdef312c8350387ebc07a`  
		Last Modified: Tue, 03 Feb 2026 02:46:17 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8b474650c320c4fa7e427b734045bf8169128440699e3927b8e32a9a46720e`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 811.5 KB (811478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f29d94f894c69cf4f94fcbdd05fcc095c1cd115764b1f9b21c96a218459cee9`  
		Last Modified: Tue, 03 Feb 2026 02:46:20 GMT  
		Size: 50.5 MB (50451811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330889a8676412bd29ad7173684d77e862a32d09fbab87341197870a3a8c50b5`  
		Last Modified: Tue, 03 Feb 2026 02:46:20 GMT  
		Size: 11.8 MB (11775874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fab057e3af09b417219f54c4482818ce2423e4ee80cedada9bd6fdc39524e8`  
		Last Modified: Tue, 03 Feb 2026 02:46:19 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9450d960e36684fe03ebae034923ff3f8f80b333b11fbf3b8996dcbb6f0a178f`  
		Last Modified: Tue, 03 Feb 2026 02:46:19 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b6892e43ed9c1fe84e3e0698e7e9dd360aec039fa0da1b68a8fb16b19fbf4b`  
		Last Modified: Tue, 03 Feb 2026 02:46:20 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:23ff9cf2666d61d899a41d203def14fb121d6b101f6bca36372bce8c1a34bc53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93f9edb8656972ae76c2cefcf23e57f970e6bc60f5f7531dac82e63cae829ae`

```dockerfile
```

-	Layers:
	-	`sha256:dbfd23cb6459150f91cfb4177077668916f88a7be35c73219f97400bf39a4d06`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6395b7f6985faa71e7a46f8563da258ae4074a12952a49080ff153ca8f4fe69e`  
		Last Modified: Tue, 03 Feb 2026 02:46:17 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1e0970c7a78cb343a3fef58c36489265de5dd8d88439da2ac6a0c756aca67314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103631393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a022c65734deebd7ae786beec5d29098b2b7103acd57d628d87ee77742f3712c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 03 Feb 2026 02:49:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 03 Feb 2026 02:49:28 GMT
ENV GOSU_VER=1.19
# Tue, 03 Feb 2026 02:49:28 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:49:28 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 03 Feb 2026 02:49:28 GMT
ENV INFLUXDB_PR=-2
# Tue, 03 Feb 2026 02:49:28 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 03 Feb 2026 02:49:31 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 03 Feb 2026 02:49:31 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 03 Feb 2026 02:49:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 03 Feb 2026 02:49:32 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 03 Feb 2026 02:49:32 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 03 Feb 2026 02:49:32 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 03 Feb 2026 02:49:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:49:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:32 GMT
CMD ["influxd"]
# Tue, 03 Feb 2026 02:49:32 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 02:49:32 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 03 Feb 2026 02:49:32 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 03 Feb 2026 02:49:32 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 03 Feb 2026 02:49:32 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2599dfe8bae66920a40e3330c8606c7ea4abcc1dae7fbe8c78e3cb0384740a3`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 9.6 MB (9626876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2b6f6792b00d9845ba09727292f97ea0b38def2d5575acb1edde6ec88b4df9`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7bb767f96a5889ba29375d4a2389c673c3f2f377d22b768418a970cb8ff0f7`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4d5352f32f1d5f51a290ca3be8a68181981219b1f607ad74d08a8137ae7a74`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 766.4 KB (766371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76584a43b5c55dbff3568ea7892e2d00770e0b0b88ba7ed53250cbe2a9dbfbd1`  
		Last Modified: Tue, 03 Feb 2026 02:49:46 GMT  
		Size: 48.2 MB (48229547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa502af2a66f75b29f67123eae52a712fd333ac4d595a9a0514ca1c20964d939`  
		Last Modified: Tue, 03 Feb 2026 02:49:45 GMT  
		Size: 11.1 MB (11100398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542140838c815e9f34996604794b30f64eb049e7809a6861e89b8d71c6a2d99f`  
		Last Modified: Tue, 03 Feb 2026 02:49:45 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b327a056230cbee6bcb0d43d19548b76ab4e11323d1ac8a58d0b63e2e26940fa`  
		Last Modified: Tue, 03 Feb 2026 02:49:45 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e24463b195d5e6be91b19c2dc72222cf8061412a3290816fd1f159cfbb5f61e`  
		Last Modified: Tue, 03 Feb 2026 02:49:46 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:a88f996b355bb1f02909697223697179d51071968381aae977ba44e7db326e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395e8b237b3dbe15def323a24ab4a042e28fe33b5cb470ba2f7ea581adef2111`

```dockerfile
```

-	Layers:
	-	`sha256:3b9fe95ec4b5730d2670759d109b96e5bc916bce1ebb711599288c70cdd9ce0b`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd1283c7a5a1e2c3bb73e96238f35b072a32efdfdff620b1a9140ba4e26b99e1`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 33.8 KB (33815 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:f15dfc604753f53b180364a331b46c2f4bc5c08a665d025982b301efa69bc2f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e224ef04c67e6587c0b6f9f0d5e125f291bdc080b17e6d498b0fa10f60c9eccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81900321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6866841a1a833e0595336141bd26bc5088eafcd30cd7576f2382ddbfd53eea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:26:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_PR=-2
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 28 Jan 2026 03:26:59 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:27:00 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:27:00 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:00 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:27:00 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:27:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da2f69740401b1208019e15e303957ef5e65950b9f1a7b4939e5fc136f96a3f`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a44134f5fc0c6cdf52aa1278b3f3f6eee8a5c2a452dd4aff61503e192f645e`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 9.9 MB (9863904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005d64a40f5cb225c3bc69263c0469aa02ab005ed8b21e6e7a89b3675ec50b07`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 6.2 MB (6156984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201d3a17f0762d441938d9cd05ad8c611220953a6d8de6a93072a25f16c4692b`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15a968cb865edd4609ac8b32d717b03922a73cb3f7590c30780bad10277e537`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 50.5 MB (50451881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75205be004b2b555f72327c5eb07d199aae883c0df672642e69dfcdc4dab8cf`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 11.8 MB (11775858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f48dd36db7dbb28ea6f0a2d7958ef354180d24d56cf270dc22a547a09111687`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc78f60a45d07493bbb7618a6d38e70f86076b21dc6487f08ed2684b1ee56b8`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b85aa016614d9f14630b36f109832ec79194ab3adcd5994b8868dec4259eef`  
		Last Modified: Wed, 28 Jan 2026 03:27:06 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:47754c46831f8311db55db258098d6bd94c0b23caf15316fd1bb193490033dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.7 KB (946732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8f0be80fc287fb05cf358d3814bac779c2ad698308821166b0c53f73f17340`

```dockerfile
```

-	Layers:
	-	`sha256:aa884cdf050c202632293939e889ccbda051a7d2d9e8139c8fb38b9f0383362f`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 915.9 KB (915886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b43ac4284db4608a9e3f907899268737ae652fd8183dab50b925feb71dbeb7`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 30.8 KB (30846 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ff96fbac0d6cf44eb703e9cd7e5f2a09bfd2f78e814185c58f2a34d9fecd5cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78945372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2200d46793614389922d59d788c241bf4d159c9f22de8fb362b4321d920953e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:15:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_PR=-2
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 28 Jan 2026 03:15:31 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:15:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:15:33 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:33 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:15:33 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:15:33 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6ab2286a7a1f7b2a657fa5f9cd5794c5eaaecea283f7e8ed6df6e1726525eb`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6584e15e052556418670992187d03a8d302b4b08e86a35c3c202d8b763a116`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 9.8 MB (9824174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b868f1d2c50be9be813066470ac1cbfefc67a3ade4ac5caf84ad8f9f92c7b3c0`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13e4c27ec5340b32d6db93325cde6c1a76b1bfb444f82b0281a2afaebc423f`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e19b47fb98adca37cda31bb666000a1068add6e40bc68415d079e0810ba271`  
		Last Modified: Wed, 28 Jan 2026 03:15:46 GMT  
		Size: 48.2 MB (48229537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef6ef542d7aecf40c7fa27129ae016a248041943f6f2cf02e5fbdbf2ec3481a`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 11.1 MB (11100399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728e7d19219b3f2895b7e6f75ee30c3eb1ca3198fc8b91d24484f0d7ae29a970`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feabd2445240c8db64c9188502a45203d8bf4fa862e1facd65af80a0a4a05b90`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988bef482c19d2f614d4ec49ed4b57867cbbe8b263aad5779a7cd1a46621fe9`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:73ce168dd0f62068e66e3be9e245c1622a2cedfa2c9f879b63d105a81e2f4fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.2 KB (946177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1de55895028e279fbba3d674a6062cd263237cc82dedc0669e211c20457f0a`

```dockerfile
```

-	Layers:
	-	`sha256:70ed507d37e4c0a2fb8cca40b6a791937d6585d05bfba4bcc080d71d0ca360f7`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 915.1 KB (915137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26164e792c84253eddb0c7007db1811569868d2bf2dd4d2a7056ec4ae310fca0`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 31.0 KB (31040 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:4633b386dcceff5db21cc4c0683609f1d6675c9ba6c28a2db96bd9e9d5223c69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:c4f8813401048ba6400427334f88af9f4003b5ea5abc9a6d5b969a4d78240817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157227743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513245badad78f9355d0c256ee82191e2878031a7b7a9346cb9ef0a63e6d3d86`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:45:52 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:45:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 03 Feb 2026 02:45:53 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 03 Feb 2026 02:45:55 GMT
ENV GOSU_VER=1.16
# Tue, 03 Feb 2026 02:45:55 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:45:55 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 03 Feb 2026 02:45:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 03 Feb 2026 02:45:58 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 03 Feb 2026 02:45:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 03 Feb 2026 02:45:59 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 03 Feb 2026 02:45:59 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 03 Feb 2026 02:45:59 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 03 Feb 2026 02:45:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:45:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:45:59 GMT
CMD ["influxd"]
# Tue, 03 Feb 2026 02:45:59 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 02:45:59 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 03 Feb 2026 02:45:59 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 03 Feb 2026 02:45:59 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 03 Feb 2026 02:45:59 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55e576761d1d2380c4d59170f39938fcf8092b60af6ed1f8b541af2751a2f77`  
		Last Modified: Tue, 03 Feb 2026 02:46:15 GMT  
		Size: 9.8 MB (9798204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7f7cfaebc111f7a16f39d2b194f5a7ed5284a065cee33709ac726b17cffb78`  
		Last Modified: Tue, 03 Feb 2026 02:46:15 GMT  
		Size: 6.2 MB (6156983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676c9cd70a49857630c021b3f3722692f2245cab288c0821ca2a7af6949c1d32`  
		Last Modified: Tue, 03 Feb 2026 02:46:14 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23ccbf91ea98f5b01d4e5916ccf8907e4f33207b1f5744d285a828a0dcb9f77`  
		Last Modified: Tue, 03 Feb 2026 02:46:15 GMT  
		Size: 1.0 MB (1012040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ca90815528c613b73fc446e49628c7e057e418fe53f0b4a7845fdee086d79b`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 100.2 MB (100246197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c3a2e8eeaab27718e7edbfbac6882188c30edb0884d02eb1fd8dc122a932c2`  
		Last Modified: Tue, 03 Feb 2026 02:46:16 GMT  
		Size: 11.8 MB (11775874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983c0b6d74d9887365376839b331cde5e8e0a9b5ceaa2fc670d911d8b6065531`  
		Last Modified: Tue, 03 Feb 2026 02:46:16 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a02c84bcbd030e6a2d22bc91960f5190cb37a3ab368df616123c23e4bb5cb7f`  
		Last Modified: Tue, 03 Feb 2026 02:46:16 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d12fcedcd884e1f15963cfb12f183526389955f35b23fa89146d5cc2ad7bc75`  
		Last Modified: Tue, 03 Feb 2026 02:46:17 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:c3bee051d4da1a066d827af5051191d9391f1205b39720ebe7a391b59159c1b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5394b0c11ba6508bc9b0188c1915cec2af9f3303377e07cd1494d4880a8e78f`

```dockerfile
```

-	Layers:
	-	`sha256:c52b9bf4a45f411f12d9c7418ffd632bb78d68a49a83ad27377e87866477b53c`  
		Last Modified: Tue, 03 Feb 2026 02:46:15 GMT  
		Size: 3.0 MB (2981484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:391e37a4c692f777e9848e525482d57f7b8b076f027e7b5c701d6d483398000f`  
		Last Modified: Tue, 03 Feb 2026 02:46:14 GMT  
		Size: 32.9 KB (32901 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f96e243c4265f744247367719f259f823abefb817017736892b16b0b7de5c19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151616073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ef7c889a7f348a85aa0f914d82a13fb4cb4051052906f79e5caa8028d70a96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:48:50 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:51 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 03 Feb 2026 02:48:51 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 03 Feb 2026 02:48:53 GMT
ENV GOSU_VER=1.16
# Tue, 03 Feb 2026 02:48:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:48:53 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 03 Feb 2026 02:48:56 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 03 Feb 2026 02:48:56 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 03 Feb 2026 02:48:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 03 Feb 2026 02:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 03 Feb 2026 02:48:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 03 Feb 2026 02:48:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 03 Feb 2026 02:48:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:48:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:48:57 GMT
CMD ["influxd"]
# Tue, 03 Feb 2026 02:48:57 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 02:48:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 03 Feb 2026 02:48:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 03 Feb 2026 02:48:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 03 Feb 2026 02:48:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d898211f8d45670e542c7404e1faa016e0832befb10730495c5e49e1da16f2f`  
		Last Modified: Tue, 03 Feb 2026 02:49:12 GMT  
		Size: 9.6 MB (9626889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e404fb5aa54a8c92b3416e9a47c614403eaa9e66c680920e376901ae611579`  
		Last Modified: Tue, 03 Feb 2026 02:49:12 GMT  
		Size: 5.8 MB (5790430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596250e64223e9c5657905a16c0e21fe2a2e6dbbfe46c741bc568cc583e27444`  
		Last Modified: Tue, 03 Feb 2026 02:49:11 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fad9f19ed5c54e40a869f1489b1817f8320446f5191f2887a629d2dffe9ee0`  
		Last Modified: Tue, 03 Feb 2026 02:49:12 GMT  
		Size: 938.9 KB (938877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5084f696fbc990f3e9fc0815e9150561a408570c1e32832a8ba235a5881a19c`  
		Last Modified: Tue, 03 Feb 2026 02:49:15 GMT  
		Size: 96.0 MB (96041701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351ffd779a577a65b0cf9030e47bd9a84473a0ad4170e4205709e7d636871685`  
		Last Modified: Tue, 03 Feb 2026 02:49:13 GMT  
		Size: 11.1 MB (11100396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8460bc718cdf45415713aacd8fd90a3ef5f0f9c67708a87cf27e3619449d11d`  
		Last Modified: Tue, 03 Feb 2026 02:49:13 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f86b75b8474cb20b2d5d71d949ff6c871bd76fd64a90e31aa5a9c9365b76867`  
		Last Modified: Tue, 03 Feb 2026 02:49:13 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bc00e013bd828201de53c1cdf9ef80ab2e92700b638c90bd88dd14d3d00a06`  
		Last Modified: Tue, 03 Feb 2026 02:49:14 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:d28f2db647a1075354112898960b2259a2ccde0cc3932a09d2c92496f5402bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d00f5c15d858bf567676aa19f425748bdd51b8eb66f48859aca1b8784ebbf2a`

```dockerfile
```

-	Layers:
	-	`sha256:f7d480790eb771749040266a00db84fe5fc17fc6202ee010a9706682f8af7759`  
		Last Modified: Tue, 03 Feb 2026 02:49:12 GMT  
		Size: 3.0 MB (2980688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf355965cb984f598b0d81d56452df4136e8546d575e4cc3296afdeaf918eeae`  
		Last Modified: Tue, 03 Feb 2026 02:49:11 GMT  
		Size: 33.1 KB (33059 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:5455e9b8bb42dcb8aa0b8a0354b5f0758d0b4a01f595b8dc03e3f850aa5829e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:612bcecc00e60a884615b0bd7669b8b331a01c07d112836f5d3f3cad84971230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81569491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a0018b5d72a9c991652b75314e7d9b73175e415b37350cd8eaab65503a2c8d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:26:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:26:47 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:26:48 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:26:48 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:26:52 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 28 Jan 2026 03:26:52 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:26:52 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:26:53 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:26:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:26:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:26:53 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:26:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:26:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:26:53 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:26:53 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:26:53 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:26:53 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:26:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:26:53 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436196594d4787e25464422fdb786add8269452b390137ac52f5f0c3b20fe340`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65542906c81e1ee0ded9601017966688d38e3f3ba962f11243b8a411fd4535ca`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 9.9 MB (9863993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90c50d107939cea71fc35dbf93f01704d677ca32b2051b919eb9136a5f487ad`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 6.2 MB (6156987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fde6197f3551b6d05c09ee7576bc43cf7380140d15febded656f5185fbd790`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54bd449211eb719855d1847f0b0b113acfda9d5ed514fcbcc8f28647044559`  
		Last Modified: Wed, 28 Jan 2026 03:27:06 GMT  
		Size: 50.1 MB (50120944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdb9f2210214e2c0c35256e9c44d4d291216b29b6ff21f59a59bac77b114739`  
		Last Modified: Wed, 28 Jan 2026 03:27:05 GMT  
		Size: 11.8 MB (11775874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d2f24bb888e86c07489b545d9e09c1377251edb528fc8cc88982fee57a3768`  
		Last Modified: Wed, 28 Jan 2026 03:27:04 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f94aa619c7c02f89e7b19a001712c66a63863bed83dd526e2badf77d4560ee`  
		Last Modified: Wed, 28 Jan 2026 03:27:05 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b85aa016614d9f14630b36f109832ec79194ab3adcd5994b8868dec4259eef`  
		Last Modified: Wed, 28 Jan 2026 03:27:06 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:391d0a4a7f2210a76562d45f9b8a72b749d3493384e2594e5d47c4649c51b562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **943.3 KB (943325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36133270ef7c6d804c39b533fd629a82efc6fcb842431934f6c6ceea3a9915d2`

```dockerfile
```

-	Layers:
	-	`sha256:5f45889a2a23271ed96f6449e51d557d7e9860daabd60659a82044c7e9f551b9`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 913.2 KB (913207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2327d640b31f1db13e558b092ae53d65dd362980ace231384d913410b807ca09`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 30.1 KB (30118 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:73f3e9affdb305c04861bf10abfb2fa71e56e1bde5819ec1839a7c5eef6ddb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78733892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45ed053eaae26a5733f93e13d74cf1a800f771b22b2556958ef785f4b80bf7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:15:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 28 Jan 2026 03:15:31 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:15:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:15:33 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:33 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:15:33 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:15:33 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6ab2286a7a1f7b2a657fa5f9cd5794c5eaaecea283f7e8ed6df6e1726525eb`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca9a4aa64e00b6010beac8d9d65eee65d986a04c1e66e51c04fe91ed4293f8c`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 9.8 MB (9824203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbafc709ae0f6eccc66e9b498035cab2fb8cfbebf52a09baececda75ed40a9c2`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 5.8 MB (5790433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13e4c27ec5340b32d6db93325cde6c1a76b1bfb444f82b0281a2afaebc423f`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b3d5de4828e332fd8e67bc21023a4790edaa370cd3b2b93b9b3b185243b251`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 48.0 MB (48018004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbf421b3460db3778b6ef941792140c1a2f05bd3ead30e5d52cd52f861e1422`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 11.1 MB (11100419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728e7d19219b3f2895b7e6f75ee30c3eb1ca3198fc8b91d24484f0d7ae29a970`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feabd2445240c8db64c9188502a45203d8bf4fa862e1facd65af80a0a4a05b90`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988bef482c19d2f614d4ec49ed4b57867cbbe8b263aad5779a7cd1a46621fe9`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f6aa3cd15a9f2092e624e447a80fcbaf5ec708f9439108d58b48beda56ed8d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **942.7 KB (942722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f2c902e2eb2482e9375c138928510fd89d3c1d1c0a05eae47348822ef543f5`

```dockerfile
```

-	Layers:
	-	`sha256:43b1e61f4f7b667e09b16ac67562eb1e3873695e3a201da43cd36bf5e86399d6`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 912.4 KB (912434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cd7104ff5c58dfbd9314d1b3a2d32ee08e317ca67041a22e548bdff47207103`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 30.3 KB (30288 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12`

```console
$ docker pull influxdb@sha256:4633b386dcceff5db21cc4c0683609f1d6675c9ba6c28a2db96bd9e9d5223c69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:c4f8813401048ba6400427334f88af9f4003b5ea5abc9a6d5b969a4d78240817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157227743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513245badad78f9355d0c256ee82191e2878031a7b7a9346cb9ef0a63e6d3d86`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:45:52 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:45:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 03 Feb 2026 02:45:53 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 03 Feb 2026 02:45:55 GMT
ENV GOSU_VER=1.16
# Tue, 03 Feb 2026 02:45:55 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:45:55 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 03 Feb 2026 02:45:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 03 Feb 2026 02:45:58 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 03 Feb 2026 02:45:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 03 Feb 2026 02:45:59 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 03 Feb 2026 02:45:59 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 03 Feb 2026 02:45:59 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 03 Feb 2026 02:45:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:45:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:45:59 GMT
CMD ["influxd"]
# Tue, 03 Feb 2026 02:45:59 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 02:45:59 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 03 Feb 2026 02:45:59 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 03 Feb 2026 02:45:59 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 03 Feb 2026 02:45:59 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55e576761d1d2380c4d59170f39938fcf8092b60af6ed1f8b541af2751a2f77`  
		Last Modified: Tue, 03 Feb 2026 02:46:15 GMT  
		Size: 9.8 MB (9798204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7f7cfaebc111f7a16f39d2b194f5a7ed5284a065cee33709ac726b17cffb78`  
		Last Modified: Tue, 03 Feb 2026 02:46:15 GMT  
		Size: 6.2 MB (6156983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676c9cd70a49857630c021b3f3722692f2245cab288c0821ca2a7af6949c1d32`  
		Last Modified: Tue, 03 Feb 2026 02:46:14 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23ccbf91ea98f5b01d4e5916ccf8907e4f33207b1f5744d285a828a0dcb9f77`  
		Last Modified: Tue, 03 Feb 2026 02:46:15 GMT  
		Size: 1.0 MB (1012040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ca90815528c613b73fc446e49628c7e057e418fe53f0b4a7845fdee086d79b`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 100.2 MB (100246197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c3a2e8eeaab27718e7edbfbac6882188c30edb0884d02eb1fd8dc122a932c2`  
		Last Modified: Tue, 03 Feb 2026 02:46:16 GMT  
		Size: 11.8 MB (11775874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983c0b6d74d9887365376839b331cde5e8e0a9b5ceaa2fc670d911d8b6065531`  
		Last Modified: Tue, 03 Feb 2026 02:46:16 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a02c84bcbd030e6a2d22bc91960f5190cb37a3ab368df616123c23e4bb5cb7f`  
		Last Modified: Tue, 03 Feb 2026 02:46:16 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d12fcedcd884e1f15963cfb12f183526389955f35b23fa89146d5cc2ad7bc75`  
		Last Modified: Tue, 03 Feb 2026 02:46:17 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:c3bee051d4da1a066d827af5051191d9391f1205b39720ebe7a391b59159c1b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5394b0c11ba6508bc9b0188c1915cec2af9f3303377e07cd1494d4880a8e78f`

```dockerfile
```

-	Layers:
	-	`sha256:c52b9bf4a45f411f12d9c7418ffd632bb78d68a49a83ad27377e87866477b53c`  
		Last Modified: Tue, 03 Feb 2026 02:46:15 GMT  
		Size: 3.0 MB (2981484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:391e37a4c692f777e9848e525482d57f7b8b076f027e7b5c701d6d483398000f`  
		Last Modified: Tue, 03 Feb 2026 02:46:14 GMT  
		Size: 32.9 KB (32901 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f96e243c4265f744247367719f259f823abefb817017736892b16b0b7de5c19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151616073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ef7c889a7f348a85aa0f914d82a13fb4cb4051052906f79e5caa8028d70a96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:48:50 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:51 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 03 Feb 2026 02:48:51 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 03 Feb 2026 02:48:53 GMT
ENV GOSU_VER=1.16
# Tue, 03 Feb 2026 02:48:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:48:53 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 03 Feb 2026 02:48:56 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 03 Feb 2026 02:48:56 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 03 Feb 2026 02:48:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 03 Feb 2026 02:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 03 Feb 2026 02:48:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 03 Feb 2026 02:48:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 03 Feb 2026 02:48:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:48:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:48:57 GMT
CMD ["influxd"]
# Tue, 03 Feb 2026 02:48:57 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 02:48:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 03 Feb 2026 02:48:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 03 Feb 2026 02:48:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 03 Feb 2026 02:48:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d898211f8d45670e542c7404e1faa016e0832befb10730495c5e49e1da16f2f`  
		Last Modified: Tue, 03 Feb 2026 02:49:12 GMT  
		Size: 9.6 MB (9626889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e404fb5aa54a8c92b3416e9a47c614403eaa9e66c680920e376901ae611579`  
		Last Modified: Tue, 03 Feb 2026 02:49:12 GMT  
		Size: 5.8 MB (5790430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596250e64223e9c5657905a16c0e21fe2a2e6dbbfe46c741bc568cc583e27444`  
		Last Modified: Tue, 03 Feb 2026 02:49:11 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fad9f19ed5c54e40a869f1489b1817f8320446f5191f2887a629d2dffe9ee0`  
		Last Modified: Tue, 03 Feb 2026 02:49:12 GMT  
		Size: 938.9 KB (938877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5084f696fbc990f3e9fc0815e9150561a408570c1e32832a8ba235a5881a19c`  
		Last Modified: Tue, 03 Feb 2026 02:49:15 GMT  
		Size: 96.0 MB (96041701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351ffd779a577a65b0cf9030e47bd9a84473a0ad4170e4205709e7d636871685`  
		Last Modified: Tue, 03 Feb 2026 02:49:13 GMT  
		Size: 11.1 MB (11100396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8460bc718cdf45415713aacd8fd90a3ef5f0f9c67708a87cf27e3619449d11d`  
		Last Modified: Tue, 03 Feb 2026 02:49:13 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f86b75b8474cb20b2d5d71d949ff6c871bd76fd64a90e31aa5a9c9365b76867`  
		Last Modified: Tue, 03 Feb 2026 02:49:13 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bc00e013bd828201de53c1cdf9ef80ab2e92700b638c90bd88dd14d3d00a06`  
		Last Modified: Tue, 03 Feb 2026 02:49:14 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:d28f2db647a1075354112898960b2259a2ccde0cc3932a09d2c92496f5402bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d00f5c15d858bf567676aa19f425748bdd51b8eb66f48859aca1b8784ebbf2a`

```dockerfile
```

-	Layers:
	-	`sha256:f7d480790eb771749040266a00db84fe5fc17fc6202ee010a9706682f8af7759`  
		Last Modified: Tue, 03 Feb 2026 02:49:12 GMT  
		Size: 3.0 MB (2980688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf355965cb984f598b0d81d56452df4136e8546d575e4cc3296afdeaf918eeae`  
		Last Modified: Tue, 03 Feb 2026 02:49:11 GMT  
		Size: 33.1 KB (33059 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12-alpine`

```console
$ docker pull influxdb@sha256:5455e9b8bb42dcb8aa0b8a0354b5f0758d0b4a01f595b8dc03e3f850aa5829e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:612bcecc00e60a884615b0bd7669b8b331a01c07d112836f5d3f3cad84971230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81569491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a0018b5d72a9c991652b75314e7d9b73175e415b37350cd8eaab65503a2c8d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:26:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:26:47 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:26:48 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:26:48 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:26:52 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 28 Jan 2026 03:26:52 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:26:52 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:26:53 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:26:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:26:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:26:53 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:26:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:26:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:26:53 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:26:53 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:26:53 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:26:53 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:26:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:26:53 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436196594d4787e25464422fdb786add8269452b390137ac52f5f0c3b20fe340`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65542906c81e1ee0ded9601017966688d38e3f3ba962f11243b8a411fd4535ca`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 9.9 MB (9863993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90c50d107939cea71fc35dbf93f01704d677ca32b2051b919eb9136a5f487ad`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 6.2 MB (6156987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fde6197f3551b6d05c09ee7576bc43cf7380140d15febded656f5185fbd790`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54bd449211eb719855d1847f0b0b113acfda9d5ed514fcbcc8f28647044559`  
		Last Modified: Wed, 28 Jan 2026 03:27:06 GMT  
		Size: 50.1 MB (50120944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdb9f2210214e2c0c35256e9c44d4d291216b29b6ff21f59a59bac77b114739`  
		Last Modified: Wed, 28 Jan 2026 03:27:05 GMT  
		Size: 11.8 MB (11775874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d2f24bb888e86c07489b545d9e09c1377251edb528fc8cc88982fee57a3768`  
		Last Modified: Wed, 28 Jan 2026 03:27:04 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f94aa619c7c02f89e7b19a001712c66a63863bed83dd526e2badf77d4560ee`  
		Last Modified: Wed, 28 Jan 2026 03:27:05 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b85aa016614d9f14630b36f109832ec79194ab3adcd5994b8868dec4259eef`  
		Last Modified: Wed, 28 Jan 2026 03:27:06 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:391d0a4a7f2210a76562d45f9b8a72b749d3493384e2594e5d47c4649c51b562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **943.3 KB (943325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36133270ef7c6d804c39b533fd629a82efc6fcb842431934f6c6ceea3a9915d2`

```dockerfile
```

-	Layers:
	-	`sha256:5f45889a2a23271ed96f6449e51d557d7e9860daabd60659a82044c7e9f551b9`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 913.2 KB (913207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2327d640b31f1db13e558b092ae53d65dd362980ace231384d913410b807ca09`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 30.1 KB (30118 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:73f3e9affdb305c04861bf10abfb2fa71e56e1bde5819ec1839a7c5eef6ddb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78733892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45ed053eaae26a5733f93e13d74cf1a800f771b22b2556958ef785f4b80bf7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:15:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 28 Jan 2026 03:15:31 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:15:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:15:33 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:33 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:15:33 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:15:33 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6ab2286a7a1f7b2a657fa5f9cd5794c5eaaecea283f7e8ed6df6e1726525eb`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca9a4aa64e00b6010beac8d9d65eee65d986a04c1e66e51c04fe91ed4293f8c`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 9.8 MB (9824203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbafc709ae0f6eccc66e9b498035cab2fb8cfbebf52a09baececda75ed40a9c2`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 5.8 MB (5790433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13e4c27ec5340b32d6db93325cde6c1a76b1bfb444f82b0281a2afaebc423f`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b3d5de4828e332fd8e67bc21023a4790edaa370cd3b2b93b9b3b185243b251`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 48.0 MB (48018004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbf421b3460db3778b6ef941792140c1a2f05bd3ead30e5d52cd52f861e1422`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 11.1 MB (11100419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728e7d19219b3f2895b7e6f75ee30c3eb1ca3198fc8b91d24484f0d7ae29a970`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feabd2445240c8db64c9188502a45203d8bf4fa862e1facd65af80a0a4a05b90`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988bef482c19d2f614d4ec49ed4b57867cbbe8b263aad5779a7cd1a46621fe9`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f6aa3cd15a9f2092e624e447a80fcbaf5ec708f9439108d58b48beda56ed8d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **942.7 KB (942722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f2c902e2eb2482e9375c138928510fd89d3c1d1c0a05eae47348822ef543f5`

```dockerfile
```

-	Layers:
	-	`sha256:43b1e61f4f7b667e09b16ac67562eb1e3873695e3a201da43cd36bf5e86399d6`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 912.4 KB (912434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cd7104ff5c58dfbd9314d1b3a2d32ee08e317ca67041a22e548bdff47207103`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 30.3 KB (30288 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8`

```console
$ docker pull influxdb@sha256:8e911da5f7b482230e61fe4bad9af0697d97a75e087f19f5f0ddfee62c2bd686
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8` - linux; amd64

```console
$ docker pull influxdb@sha256:3e23a8f949851d197977fd09f19d9f1eb026e20c47a7bc50e544342b1271b0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107232786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6152aaa4c9999ec462d1f8603b21da2898ea325d68ea261d6e968c290a56c832`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:46:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:01 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 03 Feb 2026 02:46:01 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 03 Feb 2026 02:46:03 GMT
ENV GOSU_VER=1.19
# Tue, 03 Feb 2026 02:46:03 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:46:03 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 03 Feb 2026 02:46:03 GMT
ENV INFLUXDB_PR=-2
# Tue, 03 Feb 2026 02:46:03 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 03 Feb 2026 02:46:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 03 Feb 2026 02:46:06 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 03 Feb 2026 02:46:07 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 03 Feb 2026 02:46:07 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 03 Feb 2026 02:46:07 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 03 Feb 2026 02:46:07 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 03 Feb 2026 02:46:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:46:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:07 GMT
CMD ["influxd"]
# Tue, 03 Feb 2026 02:46:07 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 02:46:07 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 03 Feb 2026 02:46:07 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 03 Feb 2026 02:46:07 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 03 Feb 2026 02:46:07 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebdc098e5a0cdaffe8ed5d5f890eebd95af1721e8ec4546756ceb4f430163e`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 9.8 MB (9798212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc0e0dd72fbd9e712238621797c89d4cb234ec5d85c98dfe1fdfa0010f6a4f7`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 6.2 MB (6156965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47df6264947c0be6c65a68d2f4c00d24721cdd03025fdef312c8350387ebc07a`  
		Last Modified: Tue, 03 Feb 2026 02:46:17 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8b474650c320c4fa7e427b734045bf8169128440699e3927b8e32a9a46720e`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 811.5 KB (811478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f29d94f894c69cf4f94fcbdd05fcc095c1cd115764b1f9b21c96a218459cee9`  
		Last Modified: Tue, 03 Feb 2026 02:46:20 GMT  
		Size: 50.5 MB (50451811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330889a8676412bd29ad7173684d77e862a32d09fbab87341197870a3a8c50b5`  
		Last Modified: Tue, 03 Feb 2026 02:46:20 GMT  
		Size: 11.8 MB (11775874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fab057e3af09b417219f54c4482818ce2423e4ee80cedada9bd6fdc39524e8`  
		Last Modified: Tue, 03 Feb 2026 02:46:19 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9450d960e36684fe03ebae034923ff3f8f80b333b11fbf3b8996dcbb6f0a178f`  
		Last Modified: Tue, 03 Feb 2026 02:46:19 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b6892e43ed9c1fe84e3e0698e7e9dd360aec039fa0da1b68a8fb16b19fbf4b`  
		Last Modified: Tue, 03 Feb 2026 02:46:20 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:23ff9cf2666d61d899a41d203def14fb121d6b101f6bca36372bce8c1a34bc53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93f9edb8656972ae76c2cefcf23e57f970e6bc60f5f7531dac82e63cae829ae`

```dockerfile
```

-	Layers:
	-	`sha256:dbfd23cb6459150f91cfb4177077668916f88a7be35c73219f97400bf39a4d06`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6395b7f6985faa71e7a46f8563da258ae4074a12952a49080ff153ca8f4fe69e`  
		Last Modified: Tue, 03 Feb 2026 02:46:17 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1e0970c7a78cb343a3fef58c36489265de5dd8d88439da2ac6a0c756aca67314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103631393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a022c65734deebd7ae786beec5d29098b2b7103acd57d628d87ee77742f3712c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 03 Feb 2026 02:49:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 03 Feb 2026 02:49:28 GMT
ENV GOSU_VER=1.19
# Tue, 03 Feb 2026 02:49:28 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:49:28 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 03 Feb 2026 02:49:28 GMT
ENV INFLUXDB_PR=-2
# Tue, 03 Feb 2026 02:49:28 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 03 Feb 2026 02:49:31 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 03 Feb 2026 02:49:31 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 03 Feb 2026 02:49:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 03 Feb 2026 02:49:32 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 03 Feb 2026 02:49:32 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 03 Feb 2026 02:49:32 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 03 Feb 2026 02:49:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:49:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:32 GMT
CMD ["influxd"]
# Tue, 03 Feb 2026 02:49:32 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 02:49:32 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 03 Feb 2026 02:49:32 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 03 Feb 2026 02:49:32 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 03 Feb 2026 02:49:32 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2599dfe8bae66920a40e3330c8606c7ea4abcc1dae7fbe8c78e3cb0384740a3`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 9.6 MB (9626876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2b6f6792b00d9845ba09727292f97ea0b38def2d5575acb1edde6ec88b4df9`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7bb767f96a5889ba29375d4a2389c673c3f2f377d22b768418a970cb8ff0f7`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4d5352f32f1d5f51a290ca3be8a68181981219b1f607ad74d08a8137ae7a74`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 766.4 KB (766371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76584a43b5c55dbff3568ea7892e2d00770e0b0b88ba7ed53250cbe2a9dbfbd1`  
		Last Modified: Tue, 03 Feb 2026 02:49:46 GMT  
		Size: 48.2 MB (48229547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa502af2a66f75b29f67123eae52a712fd333ac4d595a9a0514ca1c20964d939`  
		Last Modified: Tue, 03 Feb 2026 02:49:45 GMT  
		Size: 11.1 MB (11100398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542140838c815e9f34996604794b30f64eb049e7809a6861e89b8d71c6a2d99f`  
		Last Modified: Tue, 03 Feb 2026 02:49:45 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b327a056230cbee6bcb0d43d19548b76ab4e11323d1ac8a58d0b63e2e26940fa`  
		Last Modified: Tue, 03 Feb 2026 02:49:45 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e24463b195d5e6be91b19c2dc72222cf8061412a3290816fd1f159cfbb5f61e`  
		Last Modified: Tue, 03 Feb 2026 02:49:46 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:a88f996b355bb1f02909697223697179d51071968381aae977ba44e7db326e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395e8b237b3dbe15def323a24ab4a042e28fe33b5cb470ba2f7ea581adef2111`

```dockerfile
```

-	Layers:
	-	`sha256:3b9fe95ec4b5730d2670759d109b96e5bc916bce1ebb711599288c70cdd9ce0b`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd1283c7a5a1e2c3bb73e96238f35b072a32efdfdff620b1a9140ba4e26b99e1`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 33.8 KB (33815 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8-alpine`

```console
$ docker pull influxdb@sha256:f15dfc604753f53b180364a331b46c2f4bc5c08a665d025982b301efa69bc2f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e224ef04c67e6587c0b6f9f0d5e125f291bdc080b17e6d498b0fa10f60c9eccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81900321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6866841a1a833e0595336141bd26bc5088eafcd30cd7576f2382ddbfd53eea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:26:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_PR=-2
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 28 Jan 2026 03:26:59 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:27:00 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:27:00 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:00 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:27:00 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:27:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da2f69740401b1208019e15e303957ef5e65950b9f1a7b4939e5fc136f96a3f`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a44134f5fc0c6cdf52aa1278b3f3f6eee8a5c2a452dd4aff61503e192f645e`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 9.9 MB (9863904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005d64a40f5cb225c3bc69263c0469aa02ab005ed8b21e6e7a89b3675ec50b07`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 6.2 MB (6156984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201d3a17f0762d441938d9cd05ad8c611220953a6d8de6a93072a25f16c4692b`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15a968cb865edd4609ac8b32d717b03922a73cb3f7590c30780bad10277e537`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 50.5 MB (50451881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75205be004b2b555f72327c5eb07d199aae883c0df672642e69dfcdc4dab8cf`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 11.8 MB (11775858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f48dd36db7dbb28ea6f0a2d7958ef354180d24d56cf270dc22a547a09111687`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc78f60a45d07493bbb7618a6d38e70f86076b21dc6487f08ed2684b1ee56b8`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b85aa016614d9f14630b36f109832ec79194ab3adcd5994b8868dec4259eef`  
		Last Modified: Wed, 28 Jan 2026 03:27:06 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:47754c46831f8311db55db258098d6bd94c0b23caf15316fd1bb193490033dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.7 KB (946732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8f0be80fc287fb05cf358d3814bac779c2ad698308821166b0c53f73f17340`

```dockerfile
```

-	Layers:
	-	`sha256:aa884cdf050c202632293939e889ccbda051a7d2d9e8139c8fb38b9f0383362f`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 915.9 KB (915886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b43ac4284db4608a9e3f907899268737ae652fd8183dab50b925feb71dbeb7`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 30.8 KB (30846 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ff96fbac0d6cf44eb703e9cd7e5f2a09bfd2f78e814185c58f2a34d9fecd5cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78945372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2200d46793614389922d59d788c241bf4d159c9f22de8fb362b4321d920953e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:15:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_PR=-2
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 28 Jan 2026 03:15:31 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:15:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:15:33 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:33 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:15:33 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:15:33 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6ab2286a7a1f7b2a657fa5f9cd5794c5eaaecea283f7e8ed6df6e1726525eb`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6584e15e052556418670992187d03a8d302b4b08e86a35c3c202d8b763a116`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 9.8 MB (9824174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b868f1d2c50be9be813066470ac1cbfefc67a3ade4ac5caf84ad8f9f92c7b3c0`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13e4c27ec5340b32d6db93325cde6c1a76b1bfb444f82b0281a2afaebc423f`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e19b47fb98adca37cda31bb666000a1068add6e40bc68415d079e0810ba271`  
		Last Modified: Wed, 28 Jan 2026 03:15:46 GMT  
		Size: 48.2 MB (48229537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef6ef542d7aecf40c7fa27129ae016a248041943f6f2cf02e5fbdbf2ec3481a`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 11.1 MB (11100399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728e7d19219b3f2895b7e6f75ee30c3eb1ca3198fc8b91d24484f0d7ae29a970`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feabd2445240c8db64c9188502a45203d8bf4fa862e1facd65af80a0a4a05b90`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988bef482c19d2f614d4ec49ed4b57867cbbe8b263aad5779a7cd1a46621fe9`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:73ce168dd0f62068e66e3be9e245c1622a2cedfa2c9f879b63d105a81e2f4fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.2 KB (946177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1de55895028e279fbba3d674a6062cd263237cc82dedc0669e211c20457f0a`

```dockerfile
```

-	Layers:
	-	`sha256:70ed507d37e4c0a2fb8cca40b6a791937d6585d05bfba4bcc080d71d0ca360f7`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 915.1 KB (915137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26164e792c84253eddb0c7007db1811569868d2bf2dd4d2a7056ec4ae310fca0`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 31.0 KB (31040 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8.0`

```console
$ docker pull influxdb@sha256:8e911da5f7b482230e61fe4bad9af0697d97a75e087f19f5f0ddfee62c2bd686
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8.0` - linux; amd64

```console
$ docker pull influxdb@sha256:3e23a8f949851d197977fd09f19d9f1eb026e20c47a7bc50e544342b1271b0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107232786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6152aaa4c9999ec462d1f8603b21da2898ea325d68ea261d6e968c290a56c832`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:46:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:01 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 03 Feb 2026 02:46:01 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 03 Feb 2026 02:46:03 GMT
ENV GOSU_VER=1.19
# Tue, 03 Feb 2026 02:46:03 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:46:03 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 03 Feb 2026 02:46:03 GMT
ENV INFLUXDB_PR=-2
# Tue, 03 Feb 2026 02:46:03 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 03 Feb 2026 02:46:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 03 Feb 2026 02:46:06 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 03 Feb 2026 02:46:07 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 03 Feb 2026 02:46:07 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 03 Feb 2026 02:46:07 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 03 Feb 2026 02:46:07 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 03 Feb 2026 02:46:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:46:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:07 GMT
CMD ["influxd"]
# Tue, 03 Feb 2026 02:46:07 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 02:46:07 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 03 Feb 2026 02:46:07 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 03 Feb 2026 02:46:07 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 03 Feb 2026 02:46:07 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebdc098e5a0cdaffe8ed5d5f890eebd95af1721e8ec4546756ceb4f430163e`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 9.8 MB (9798212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc0e0dd72fbd9e712238621797c89d4cb234ec5d85c98dfe1fdfa0010f6a4f7`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 6.2 MB (6156965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47df6264947c0be6c65a68d2f4c00d24721cdd03025fdef312c8350387ebc07a`  
		Last Modified: Tue, 03 Feb 2026 02:46:17 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8b474650c320c4fa7e427b734045bf8169128440699e3927b8e32a9a46720e`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 811.5 KB (811478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f29d94f894c69cf4f94fcbdd05fcc095c1cd115764b1f9b21c96a218459cee9`  
		Last Modified: Tue, 03 Feb 2026 02:46:20 GMT  
		Size: 50.5 MB (50451811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330889a8676412bd29ad7173684d77e862a32d09fbab87341197870a3a8c50b5`  
		Last Modified: Tue, 03 Feb 2026 02:46:20 GMT  
		Size: 11.8 MB (11775874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fab057e3af09b417219f54c4482818ce2423e4ee80cedada9bd6fdc39524e8`  
		Last Modified: Tue, 03 Feb 2026 02:46:19 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9450d960e36684fe03ebae034923ff3f8f80b333b11fbf3b8996dcbb6f0a178f`  
		Last Modified: Tue, 03 Feb 2026 02:46:19 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b6892e43ed9c1fe84e3e0698e7e9dd360aec039fa0da1b68a8fb16b19fbf4b`  
		Last Modified: Tue, 03 Feb 2026 02:46:20 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:23ff9cf2666d61d899a41d203def14fb121d6b101f6bca36372bce8c1a34bc53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93f9edb8656972ae76c2cefcf23e57f970e6bc60f5f7531dac82e63cae829ae`

```dockerfile
```

-	Layers:
	-	`sha256:dbfd23cb6459150f91cfb4177077668916f88a7be35c73219f97400bf39a4d06`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6395b7f6985faa71e7a46f8563da258ae4074a12952a49080ff153ca8f4fe69e`  
		Last Modified: Tue, 03 Feb 2026 02:46:17 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1e0970c7a78cb343a3fef58c36489265de5dd8d88439da2ac6a0c756aca67314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103631393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a022c65734deebd7ae786beec5d29098b2b7103acd57d628d87ee77742f3712c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 03 Feb 2026 02:49:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 03 Feb 2026 02:49:28 GMT
ENV GOSU_VER=1.19
# Tue, 03 Feb 2026 02:49:28 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:49:28 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 03 Feb 2026 02:49:28 GMT
ENV INFLUXDB_PR=-2
# Tue, 03 Feb 2026 02:49:28 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 03 Feb 2026 02:49:31 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 03 Feb 2026 02:49:31 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 03 Feb 2026 02:49:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 03 Feb 2026 02:49:32 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 03 Feb 2026 02:49:32 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 03 Feb 2026 02:49:32 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 03 Feb 2026 02:49:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:49:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:32 GMT
CMD ["influxd"]
# Tue, 03 Feb 2026 02:49:32 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 02:49:32 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 03 Feb 2026 02:49:32 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 03 Feb 2026 02:49:32 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 03 Feb 2026 02:49:32 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2599dfe8bae66920a40e3330c8606c7ea4abcc1dae7fbe8c78e3cb0384740a3`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 9.6 MB (9626876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2b6f6792b00d9845ba09727292f97ea0b38def2d5575acb1edde6ec88b4df9`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7bb767f96a5889ba29375d4a2389c673c3f2f377d22b768418a970cb8ff0f7`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4d5352f32f1d5f51a290ca3be8a68181981219b1f607ad74d08a8137ae7a74`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 766.4 KB (766371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76584a43b5c55dbff3568ea7892e2d00770e0b0b88ba7ed53250cbe2a9dbfbd1`  
		Last Modified: Tue, 03 Feb 2026 02:49:46 GMT  
		Size: 48.2 MB (48229547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa502af2a66f75b29f67123eae52a712fd333ac4d595a9a0514ca1c20964d939`  
		Last Modified: Tue, 03 Feb 2026 02:49:45 GMT  
		Size: 11.1 MB (11100398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542140838c815e9f34996604794b30f64eb049e7809a6861e89b8d71c6a2d99f`  
		Last Modified: Tue, 03 Feb 2026 02:49:45 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b327a056230cbee6bcb0d43d19548b76ab4e11323d1ac8a58d0b63e2e26940fa`  
		Last Modified: Tue, 03 Feb 2026 02:49:45 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e24463b195d5e6be91b19c2dc72222cf8061412a3290816fd1f159cfbb5f61e`  
		Last Modified: Tue, 03 Feb 2026 02:49:46 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:a88f996b355bb1f02909697223697179d51071968381aae977ba44e7db326e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395e8b237b3dbe15def323a24ab4a042e28fe33b5cb470ba2f7ea581adef2111`

```dockerfile
```

-	Layers:
	-	`sha256:3b9fe95ec4b5730d2670759d109b96e5bc916bce1ebb711599288c70cdd9ce0b`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd1283c7a5a1e2c3bb73e96238f35b072a32efdfdff620b1a9140ba4e26b99e1`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 33.8 KB (33815 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8.0-alpine`

```console
$ docker pull influxdb@sha256:f15dfc604753f53b180364a331b46c2f4bc5c08a665d025982b301efa69bc2f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8.0-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e224ef04c67e6587c0b6f9f0d5e125f291bdc080b17e6d498b0fa10f60c9eccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81900321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6866841a1a833e0595336141bd26bc5088eafcd30cd7576f2382ddbfd53eea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:26:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_PR=-2
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 28 Jan 2026 03:26:59 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:27:00 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:27:00 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:00 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:27:00 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:27:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da2f69740401b1208019e15e303957ef5e65950b9f1a7b4939e5fc136f96a3f`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a44134f5fc0c6cdf52aa1278b3f3f6eee8a5c2a452dd4aff61503e192f645e`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 9.9 MB (9863904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005d64a40f5cb225c3bc69263c0469aa02ab005ed8b21e6e7a89b3675ec50b07`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 6.2 MB (6156984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201d3a17f0762d441938d9cd05ad8c611220953a6d8de6a93072a25f16c4692b`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15a968cb865edd4609ac8b32d717b03922a73cb3f7590c30780bad10277e537`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 50.5 MB (50451881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75205be004b2b555f72327c5eb07d199aae883c0df672642e69dfcdc4dab8cf`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 11.8 MB (11775858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f48dd36db7dbb28ea6f0a2d7958ef354180d24d56cf270dc22a547a09111687`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc78f60a45d07493bbb7618a6d38e70f86076b21dc6487f08ed2684b1ee56b8`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b85aa016614d9f14630b36f109832ec79194ab3adcd5994b8868dec4259eef`  
		Last Modified: Wed, 28 Jan 2026 03:27:06 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:47754c46831f8311db55db258098d6bd94c0b23caf15316fd1bb193490033dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.7 KB (946732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8f0be80fc287fb05cf358d3814bac779c2ad698308821166b0c53f73f17340`

```dockerfile
```

-	Layers:
	-	`sha256:aa884cdf050c202632293939e889ccbda051a7d2d9e8139c8fb38b9f0383362f`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 915.9 KB (915886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b43ac4284db4608a9e3f907899268737ae652fd8183dab50b925feb71dbeb7`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 30.8 KB (30846 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8.0-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ff96fbac0d6cf44eb703e9cd7e5f2a09bfd2f78e814185c58f2a34d9fecd5cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78945372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2200d46793614389922d59d788c241bf4d159c9f22de8fb362b4321d920953e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:15:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_PR=-2
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 28 Jan 2026 03:15:31 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:15:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:15:33 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:33 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:15:33 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:15:33 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6ab2286a7a1f7b2a657fa5f9cd5794c5eaaecea283f7e8ed6df6e1726525eb`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6584e15e052556418670992187d03a8d302b4b08e86a35c3c202d8b763a116`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 9.8 MB (9824174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b868f1d2c50be9be813066470ac1cbfefc67a3ade4ac5caf84ad8f9f92c7b3c0`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13e4c27ec5340b32d6db93325cde6c1a76b1bfb444f82b0281a2afaebc423f`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e19b47fb98adca37cda31bb666000a1068add6e40bc68415d079e0810ba271`  
		Last Modified: Wed, 28 Jan 2026 03:15:46 GMT  
		Size: 48.2 MB (48229537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef6ef542d7aecf40c7fa27129ae016a248041943f6f2cf02e5fbdbf2ec3481a`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 11.1 MB (11100399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728e7d19219b3f2895b7e6f75ee30c3eb1ca3198fc8b91d24484f0d7ae29a970`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feabd2445240c8db64c9188502a45203d8bf4fa862e1facd65af80a0a4a05b90`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988bef482c19d2f614d4ec49ed4b57867cbbe8b263aad5779a7cd1a46621fe9`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:73ce168dd0f62068e66e3be9e245c1622a2cedfa2c9f879b63d105a81e2f4fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.2 KB (946177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1de55895028e279fbba3d674a6062cd263237cc82dedc0669e211c20457f0a`

```dockerfile
```

-	Layers:
	-	`sha256:70ed507d37e4c0a2fb8cca40b6a791937d6585d05bfba4bcc080d71d0ca360f7`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 915.1 KB (915137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26164e792c84253eddb0c7007db1811569868d2bf2dd4d2a7056ec4ae310fca0`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 31.0 KB (31040 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:2757db64af5f331bbfb0e25d6731c8cf65c5a515d027c8bc5a48b258fa008c8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:8f36abf47ed33e424b8f9b238694a7bcc082bd0e74d97cec7d6d7c7db47d6552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119311374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f3d35e10e7aed87113e0a46df8b64bf71b7f74180eee35877ee5d6d4b2fab9`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

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
# Thu, 15 Jan 2026 22:29:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:29:31 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:29:35 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:29:35 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:29:35 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:29:35 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb421340cf49eb838ba5a93e97c5a79263668d6c63b6e2bdec9f12f9cb2bbe70`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 6.7 MB (6666455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c5db002efd1716598d0b566d19a173dfe7126f0914b12e1fdc180f8a7a14e2`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bfc81f68fb579269742625ae883af1e68a469bdc3e47f9cb250ea7d67ceeb1`  
		Last Modified: Thu, 15 Jan 2026 22:29:52 GMT  
		Size: 82.9 MB (82914588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e85a99980b8d4fa689879cdc5ef70054bed61905df3549de46260caf0e47d7b`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51c7ce377562ca9379f5ea9def930b1be0d7d2ec4c48e18fb742a156f46361`  
		Last Modified: Thu, 15 Jan 2026 22:29:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd004e1dab8b1efc281255b5815cb666fe08ed4498b2c7431f2381b9ac7e4d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb254fbbd5847cc94d322f7ef8c2404eddc14d107a5f050d4e3991237a7e23`

```dockerfile
```

-	Layers:
	-	`sha256:93cae582c7522611a439a6c7a2a6faa7e7b2e6675c9c78f5786ffa27d2d6f7fd`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 2.3 MB (2310563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0a5f390a10ab6cf064a1f5fcd498996c18aba1bfb713c33773b1ba72a7f421`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:87433bdbd8e99019e7fc9dfecda86de557a2fc32b4cffa293bc27efb05d6ef27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110028972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1d2cc20717830f048ed113983a79ebf82d22879f31666972296654e226055e`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

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
# Thu, 15 Jan 2026 22:31:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:31:35 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:31:39 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:31:39 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:31:39 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:31:39 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b85d29ef9d1a5b609c04250a98480155038f067e295c06a12bb03a0b163bcb6`  
		Last Modified: Thu, 15 Jan 2026 22:31:53 GMT  
		Size: 6.7 MB (6678025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12879279037976dcf03bcb89fd8ca0258ae28a49fd3fca4e1d918ebf5f58334d`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 3.6 KB (3648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f5a1efb52cbac7d7d853d373b78cb1ba1da5dfb15cf3b70ff94110acc1144`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 74.5 MB (74482805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a655526e5e0376a0214f1b43fa2b17d9d392ec41f8cdc1cb75eb970f43d84d48`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff65ff8d1ea9fed765acd863744a83581bdc65244d1022c09ce2991a129a056`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:92a66a28c2cacf75f73de64fbc20b8f8a5872763b614692db0f69f380c2ce7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910fae9c7c765bca133a238b5b06f22cea8258cae915a0bcf97be00ba26d6b24`

```dockerfile
```

-	Layers:
	-	`sha256:e39d496af0bf62266e9b9be68acf22ce4ea001066b55cf8ed24f202031f749c2`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50900617900957d671f02b3d04cb4b737068c8a4c247e6954ab2762edcfedfae`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:10d40128d7fb12259a57cee239c5dc600f99ab6ddb5d08d7e6bd072fa68011ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6f80d482e72e674d39ff987c9339b71f28341e6a98a6f358a9086f9fe7745051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127592285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6d7e2d453e9995658fa8751f2b6e84a64212eeee685595977f5ff7e512afd5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

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
# Thu, 15 Jan 2026 22:29:53 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:29:53 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:29:58 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:29:58 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:29:58 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:29:58 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d80b8916ac9be25ca39f63d725fbecdb5221cc992a8f8edc501e20aa7f6cdd`  
		Last Modified: Thu, 15 Jan 2026 22:30:15 GMT  
		Size: 6.7 MB (6666466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86baf47ce3b1fa8c7b1d7b1ba023420e80d040d1a773b90f1a3f1444d5398b8`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75782d754446062a195fd74ec4f45355abd9b48844b421553b76d0d92c2e9e6`  
		Last Modified: Thu, 15 Jan 2026 22:30:17 GMT  
		Size: 91.2 MB (91195488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0552eea07c1a62aaa4c8a941aa4d914694ed7a40fa2f205e24255b406514ab`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e9ae2043b745909b42322ca040a8bc78dae54020dbf787084712e77c63a890`  
		Last Modified: Thu, 15 Jan 2026 22:30:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:cb631e30f9aa3075f21e34d43d947684a1e2cf8b6db12b3870f5925ba45592bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0859ea2244b0defc0d27a58cd00c57d441a00b51b6c00983526ef8516503d2`

```dockerfile
```

-	Layers:
	-	`sha256:eb1c0fc56bdfe5de760e79c005402e18989d63559ec2f437944b534243db1c91`  
		Last Modified: Thu, 15 Jan 2026 22:30:15 GMT  
		Size: 2.3 MB (2310611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf90cea5e6b638571c01c3c00fe6a8b6e65cbff58a178ba08a0c4a0f3c9fc4d5`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ad6e83f930d0ab312e7f5a2b347d9b8aa7f6b4132db0409cf404e4bdaa0a67cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118244315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d65a5b3e4ed077bc1ba501bc9ce80427816521ff052532109d778edee858bf2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

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
# Thu, 15 Jan 2026 22:31:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:31:57 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:32:03 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:32:03 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:32:03 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:32:03 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bd4240eafafe3f7fe3f9bc5d3b023ea3b76cd522bea0a947b3358df8986ed0`  
		Last Modified: Thu, 15 Jan 2026 22:32:18 GMT  
		Size: 6.7 MB (6678021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a2eb424397e2fd233b9e3e45d8e2e2ff184ac156d640257caac83c500bd03b`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c9c7ab39edbfbc219f93a01abd342c7aa9ae427a6e3c461e19bc610c55633c`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 82.7 MB (82698149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f15f88b8a4272c18117de13ad2ba7f3853d372748c6fea818c9336b9023fb`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a262b7c40609324279929b50e3eff0cb9505cd033e5cf2e2dc7a38c8c4e0199d`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:0265bf65e9e0e0e1d1997518bf6b88e6df9698f769f086ef60bbaf2e790d4070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9a5cb8b7911fa2587aea0afc1d4c89be70eb8e24cab810c6172cc216e9d911`

```dockerfile
```

-	Layers:
	-	`sha256:9430335ba47f250a06bcaca7da5899e1461955a18254643114311ddb1acedd5f`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 2.3 MB (2311693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e36fbb81eb4a33ce5bfce27a827062a0b8d553c1d9ca2e76dc9b865f51041ac`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.8-core`

```console
$ docker pull influxdb@sha256:2757db64af5f331bbfb0e25d6731c8cf65c5a515d027c8bc5a48b258fa008c8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.8-core` - linux; amd64

```console
$ docker pull influxdb@sha256:8f36abf47ed33e424b8f9b238694a7bcc082bd0e74d97cec7d6d7c7db47d6552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119311374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f3d35e10e7aed87113e0a46df8b64bf71b7f74180eee35877ee5d6d4b2fab9`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

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
# Thu, 15 Jan 2026 22:29:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:29:31 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:29:35 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:29:35 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:29:35 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:29:35 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb421340cf49eb838ba5a93e97c5a79263668d6c63b6e2bdec9f12f9cb2bbe70`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 6.7 MB (6666455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c5db002efd1716598d0b566d19a173dfe7126f0914b12e1fdc180f8a7a14e2`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bfc81f68fb579269742625ae883af1e68a469bdc3e47f9cb250ea7d67ceeb1`  
		Last Modified: Thu, 15 Jan 2026 22:29:52 GMT  
		Size: 82.9 MB (82914588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e85a99980b8d4fa689879cdc5ef70054bed61905df3549de46260caf0e47d7b`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51c7ce377562ca9379f5ea9def930b1be0d7d2ec4c48e18fb742a156f46361`  
		Last Modified: Thu, 15 Jan 2026 22:29:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd004e1dab8b1efc281255b5815cb666fe08ed4498b2c7431f2381b9ac7e4d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb254fbbd5847cc94d322f7ef8c2404eddc14d107a5f050d4e3991237a7e23`

```dockerfile
```

-	Layers:
	-	`sha256:93cae582c7522611a439a6c7a2a6faa7e7b2e6675c9c78f5786ffa27d2d6f7fd`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 2.3 MB (2310563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0a5f390a10ab6cf064a1f5fcd498996c18aba1bfb713c33773b1ba72a7f421`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.8-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:87433bdbd8e99019e7fc9dfecda86de557a2fc32b4cffa293bc27efb05d6ef27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110028972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1d2cc20717830f048ed113983a79ebf82d22879f31666972296654e226055e`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

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
# Thu, 15 Jan 2026 22:31:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:31:35 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:31:39 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:31:39 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:31:39 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:31:39 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b85d29ef9d1a5b609c04250a98480155038f067e295c06a12bb03a0b163bcb6`  
		Last Modified: Thu, 15 Jan 2026 22:31:53 GMT  
		Size: 6.7 MB (6678025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12879279037976dcf03bcb89fd8ca0258ae28a49fd3fca4e1d918ebf5f58334d`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 3.6 KB (3648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f5a1efb52cbac7d7d853d373b78cb1ba1da5dfb15cf3b70ff94110acc1144`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 74.5 MB (74482805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a655526e5e0376a0214f1b43fa2b17d9d392ec41f8cdc1cb75eb970f43d84d48`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff65ff8d1ea9fed765acd863744a83581bdc65244d1022c09ce2991a129a056`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:92a66a28c2cacf75f73de64fbc20b8f8a5872763b614692db0f69f380c2ce7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910fae9c7c765bca133a238b5b06f22cea8258cae915a0bcf97be00ba26d6b24`

```dockerfile
```

-	Layers:
	-	`sha256:e39d496af0bf62266e9b9be68acf22ce4ea001066b55cf8ed24f202031f749c2`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50900617900957d671f02b3d04cb4b737068c8a4c247e6954ab2762edcfedfae`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.8-enterprise`

```console
$ docker pull influxdb@sha256:10d40128d7fb12259a57cee239c5dc600f99ab6ddb5d08d7e6bd072fa68011ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.8-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6f80d482e72e674d39ff987c9339b71f28341e6a98a6f358a9086f9fe7745051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127592285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6d7e2d453e9995658fa8751f2b6e84a64212eeee685595977f5ff7e512afd5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

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
# Thu, 15 Jan 2026 22:29:53 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:29:53 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:29:58 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:29:58 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:29:58 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:29:58 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d80b8916ac9be25ca39f63d725fbecdb5221cc992a8f8edc501e20aa7f6cdd`  
		Last Modified: Thu, 15 Jan 2026 22:30:15 GMT  
		Size: 6.7 MB (6666466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86baf47ce3b1fa8c7b1d7b1ba023420e80d040d1a773b90f1a3f1444d5398b8`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75782d754446062a195fd74ec4f45355abd9b48844b421553b76d0d92c2e9e6`  
		Last Modified: Thu, 15 Jan 2026 22:30:17 GMT  
		Size: 91.2 MB (91195488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0552eea07c1a62aaa4c8a941aa4d914694ed7a40fa2f205e24255b406514ab`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e9ae2043b745909b42322ca040a8bc78dae54020dbf787084712e77c63a890`  
		Last Modified: Thu, 15 Jan 2026 22:30:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:cb631e30f9aa3075f21e34d43d947684a1e2cf8b6db12b3870f5925ba45592bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0859ea2244b0defc0d27a58cd00c57d441a00b51b6c00983526ef8516503d2`

```dockerfile
```

-	Layers:
	-	`sha256:eb1c0fc56bdfe5de760e79c005402e18989d63559ec2f437944b534243db1c91`  
		Last Modified: Thu, 15 Jan 2026 22:30:15 GMT  
		Size: 2.3 MB (2310611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf90cea5e6b638571c01c3c00fe6a8b6e65cbff58a178ba08a0c4a0f3c9fc4d5`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.8-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ad6e83f930d0ab312e7f5a2b347d9b8aa7f6b4132db0409cf404e4bdaa0a67cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118244315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d65a5b3e4ed077bc1ba501bc9ce80427816521ff052532109d778edee858bf2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

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
# Thu, 15 Jan 2026 22:31:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:31:57 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:32:03 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:32:03 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:32:03 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:32:03 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bd4240eafafe3f7fe3f9bc5d3b023ea3b76cd522bea0a947b3358df8986ed0`  
		Last Modified: Thu, 15 Jan 2026 22:32:18 GMT  
		Size: 6.7 MB (6678021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a2eb424397e2fd233b9e3e45d8e2e2ff184ac156d640257caac83c500bd03b`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c9c7ab39edbfbc219f93a01abd342c7aa9ae427a6e3c461e19bc610c55633c`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 82.7 MB (82698149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f15f88b8a4272c18117de13ad2ba7f3853d372748c6fea818c9336b9023fb`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a262b7c40609324279929b50e3eff0cb9505cd033e5cf2e2dc7a38c8c4e0199d`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:0265bf65e9e0e0e1d1997518bf6b88e6df9698f769f086ef60bbaf2e790d4070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9a5cb8b7911fa2587aea0afc1d4c89be70eb8e24cab810c6172cc216e9d911`

```dockerfile
```

-	Layers:
	-	`sha256:9430335ba47f250a06bcaca7da5899e1461955a18254643114311ddb1acedd5f`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 2.3 MB (2311693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e36fbb81eb4a33ce5bfce27a827062a0b8d553c1d9ca2e76dc9b865f51041ac`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.8.0-core`

```console
$ docker pull influxdb@sha256:2757db64af5f331bbfb0e25d6731c8cf65c5a515d027c8bc5a48b258fa008c8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.8.0-core` - linux; amd64

```console
$ docker pull influxdb@sha256:8f36abf47ed33e424b8f9b238694a7bcc082bd0e74d97cec7d6d7c7db47d6552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119311374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f3d35e10e7aed87113e0a46df8b64bf71b7f74180eee35877ee5d6d4b2fab9`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

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
# Thu, 15 Jan 2026 22:29:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:29:31 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:29:35 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:29:35 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:29:35 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:29:35 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb421340cf49eb838ba5a93e97c5a79263668d6c63b6e2bdec9f12f9cb2bbe70`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 6.7 MB (6666455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c5db002efd1716598d0b566d19a173dfe7126f0914b12e1fdc180f8a7a14e2`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bfc81f68fb579269742625ae883af1e68a469bdc3e47f9cb250ea7d67ceeb1`  
		Last Modified: Thu, 15 Jan 2026 22:29:52 GMT  
		Size: 82.9 MB (82914588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e85a99980b8d4fa689879cdc5ef70054bed61905df3549de46260caf0e47d7b`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51c7ce377562ca9379f5ea9def930b1be0d7d2ec4c48e18fb742a156f46361`  
		Last Modified: Thu, 15 Jan 2026 22:29:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd004e1dab8b1efc281255b5815cb666fe08ed4498b2c7431f2381b9ac7e4d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb254fbbd5847cc94d322f7ef8c2404eddc14d107a5f050d4e3991237a7e23`

```dockerfile
```

-	Layers:
	-	`sha256:93cae582c7522611a439a6c7a2a6faa7e7b2e6675c9c78f5786ffa27d2d6f7fd`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 2.3 MB (2310563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0a5f390a10ab6cf064a1f5fcd498996c18aba1bfb713c33773b1ba72a7f421`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.8.0-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:87433bdbd8e99019e7fc9dfecda86de557a2fc32b4cffa293bc27efb05d6ef27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110028972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1d2cc20717830f048ed113983a79ebf82d22879f31666972296654e226055e`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

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
# Thu, 15 Jan 2026 22:31:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:31:35 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:31:39 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:31:39 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:31:39 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:31:39 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b85d29ef9d1a5b609c04250a98480155038f067e295c06a12bb03a0b163bcb6`  
		Last Modified: Thu, 15 Jan 2026 22:31:53 GMT  
		Size: 6.7 MB (6678025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12879279037976dcf03bcb89fd8ca0258ae28a49fd3fca4e1d918ebf5f58334d`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 3.6 KB (3648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f5a1efb52cbac7d7d853d373b78cb1ba1da5dfb15cf3b70ff94110acc1144`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 74.5 MB (74482805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a655526e5e0376a0214f1b43fa2b17d9d392ec41f8cdc1cb75eb970f43d84d48`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff65ff8d1ea9fed765acd863744a83581bdc65244d1022c09ce2991a129a056`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:92a66a28c2cacf75f73de64fbc20b8f8a5872763b614692db0f69f380c2ce7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910fae9c7c765bca133a238b5b06f22cea8258cae915a0bcf97be00ba26d6b24`

```dockerfile
```

-	Layers:
	-	`sha256:e39d496af0bf62266e9b9be68acf22ce4ea001066b55cf8ed24f202031f749c2`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50900617900957d671f02b3d04cb4b737068c8a4c247e6954ab2762edcfedfae`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.8.0-enterprise`

```console
$ docker pull influxdb@sha256:10d40128d7fb12259a57cee239c5dc600f99ab6ddb5d08d7e6bd072fa68011ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.8.0-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6f80d482e72e674d39ff987c9339b71f28341e6a98a6f358a9086f9fe7745051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127592285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6d7e2d453e9995658fa8751f2b6e84a64212eeee685595977f5ff7e512afd5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

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
# Thu, 15 Jan 2026 22:29:53 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:29:53 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:29:58 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:29:58 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:29:58 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:29:58 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d80b8916ac9be25ca39f63d725fbecdb5221cc992a8f8edc501e20aa7f6cdd`  
		Last Modified: Thu, 15 Jan 2026 22:30:15 GMT  
		Size: 6.7 MB (6666466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86baf47ce3b1fa8c7b1d7b1ba023420e80d040d1a773b90f1a3f1444d5398b8`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75782d754446062a195fd74ec4f45355abd9b48844b421553b76d0d92c2e9e6`  
		Last Modified: Thu, 15 Jan 2026 22:30:17 GMT  
		Size: 91.2 MB (91195488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0552eea07c1a62aaa4c8a941aa4d914694ed7a40fa2f205e24255b406514ab`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e9ae2043b745909b42322ca040a8bc78dae54020dbf787084712e77c63a890`  
		Last Modified: Thu, 15 Jan 2026 22:30:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:cb631e30f9aa3075f21e34d43d947684a1e2cf8b6db12b3870f5925ba45592bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0859ea2244b0defc0d27a58cd00c57d441a00b51b6c00983526ef8516503d2`

```dockerfile
```

-	Layers:
	-	`sha256:eb1c0fc56bdfe5de760e79c005402e18989d63559ec2f437944b534243db1c91`  
		Last Modified: Thu, 15 Jan 2026 22:30:15 GMT  
		Size: 2.3 MB (2310611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf90cea5e6b638571c01c3c00fe6a8b6e65cbff58a178ba08a0c4a0f3c9fc4d5`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.8.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ad6e83f930d0ab312e7f5a2b347d9b8aa7f6b4132db0409cf404e4bdaa0a67cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118244315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d65a5b3e4ed077bc1ba501bc9ce80427816521ff052532109d778edee858bf2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

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
# Thu, 15 Jan 2026 22:31:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:31:57 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:32:03 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:32:03 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:32:03 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:32:03 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bd4240eafafe3f7fe3f9bc5d3b023ea3b76cd522bea0a947b3358df8986ed0`  
		Last Modified: Thu, 15 Jan 2026 22:32:18 GMT  
		Size: 6.7 MB (6678021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a2eb424397e2fd233b9e3e45d8e2e2ff184ac156d640257caac83c500bd03b`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c9c7ab39edbfbc219f93a01abd342c7aa9ae427a6e3c461e19bc610c55633c`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 82.7 MB (82698149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f15f88b8a4272c18117de13ad2ba7f3853d372748c6fea818c9336b9023fb`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a262b7c40609324279929b50e3eff0cb9505cd033e5cf2e2dc7a38c8c4e0199d`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:0265bf65e9e0e0e1d1997518bf6b88e6df9698f769f086ef60bbaf2e790d4070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9a5cb8b7911fa2587aea0afc1d4c89be70eb8e24cab810c6172cc216e9d911`

```dockerfile
```

-	Layers:
	-	`sha256:9430335ba47f250a06bcaca7da5899e1461955a18254643114311ddb1acedd5f`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 2.3 MB (2311693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e36fbb81eb4a33ce5bfce27a827062a0b8d553c1d9ca2e76dc9b865f51041ac`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:f15dfc604753f53b180364a331b46c2f4bc5c08a665d025982b301efa69bc2f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e224ef04c67e6587c0b6f9f0d5e125f291bdc080b17e6d498b0fa10f60c9eccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81900321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6866841a1a833e0595336141bd26bc5088eafcd30cd7576f2382ddbfd53eea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:26:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_PR=-2
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 28 Jan 2026 03:26:59 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:27:00 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:27:00 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:00 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:27:00 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:27:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da2f69740401b1208019e15e303957ef5e65950b9f1a7b4939e5fc136f96a3f`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a44134f5fc0c6cdf52aa1278b3f3f6eee8a5c2a452dd4aff61503e192f645e`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 9.9 MB (9863904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005d64a40f5cb225c3bc69263c0469aa02ab005ed8b21e6e7a89b3675ec50b07`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 6.2 MB (6156984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201d3a17f0762d441938d9cd05ad8c611220953a6d8de6a93072a25f16c4692b`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15a968cb865edd4609ac8b32d717b03922a73cb3f7590c30780bad10277e537`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 50.5 MB (50451881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75205be004b2b555f72327c5eb07d199aae883c0df672642e69dfcdc4dab8cf`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 11.8 MB (11775858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f48dd36db7dbb28ea6f0a2d7958ef354180d24d56cf270dc22a547a09111687`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc78f60a45d07493bbb7618a6d38e70f86076b21dc6487f08ed2684b1ee56b8`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b85aa016614d9f14630b36f109832ec79194ab3adcd5994b8868dec4259eef`  
		Last Modified: Wed, 28 Jan 2026 03:27:06 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:47754c46831f8311db55db258098d6bd94c0b23caf15316fd1bb193490033dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.7 KB (946732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8f0be80fc287fb05cf358d3814bac779c2ad698308821166b0c53f73f17340`

```dockerfile
```

-	Layers:
	-	`sha256:aa884cdf050c202632293939e889ccbda051a7d2d9e8139c8fb38b9f0383362f`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 915.9 KB (915886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b43ac4284db4608a9e3f907899268737ae652fd8183dab50b925feb71dbeb7`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 30.8 KB (30846 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ff96fbac0d6cf44eb703e9cd7e5f2a09bfd2f78e814185c58f2a34d9fecd5cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78945372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2200d46793614389922d59d788c241bf4d159c9f22de8fb362b4321d920953e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:15:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_PR=-2
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 28 Jan 2026 03:15:31 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:15:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:15:33 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:33 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:15:33 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:15:33 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6ab2286a7a1f7b2a657fa5f9cd5794c5eaaecea283f7e8ed6df6e1726525eb`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6584e15e052556418670992187d03a8d302b4b08e86a35c3c202d8b763a116`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 9.8 MB (9824174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b868f1d2c50be9be813066470ac1cbfefc67a3ade4ac5caf84ad8f9f92c7b3c0`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13e4c27ec5340b32d6db93325cde6c1a76b1bfb444f82b0281a2afaebc423f`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e19b47fb98adca37cda31bb666000a1068add6e40bc68415d079e0810ba271`  
		Last Modified: Wed, 28 Jan 2026 03:15:46 GMT  
		Size: 48.2 MB (48229537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef6ef542d7aecf40c7fa27129ae016a248041943f6f2cf02e5fbdbf2ec3481a`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 11.1 MB (11100399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728e7d19219b3f2895b7e6f75ee30c3eb1ca3198fc8b91d24484f0d7ae29a970`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feabd2445240c8db64c9188502a45203d8bf4fa862e1facd65af80a0a4a05b90`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988bef482c19d2f614d4ec49ed4b57867cbbe8b263aad5779a7cd1a46621fe9`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:73ce168dd0f62068e66e3be9e245c1622a2cedfa2c9f879b63d105a81e2f4fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.2 KB (946177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1de55895028e279fbba3d674a6062cd263237cc82dedc0669e211c20457f0a`

```dockerfile
```

-	Layers:
	-	`sha256:70ed507d37e4c0a2fb8cca40b6a791937d6585d05bfba4bcc080d71d0ca360f7`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 915.1 KB (915137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26164e792c84253eddb0c7007db1811569868d2bf2dd4d2a7056ec4ae310fca0`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 31.0 KB (31040 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:core`

```console
$ docker pull influxdb@sha256:2757db64af5f331bbfb0e25d6731c8cf65c5a515d027c8bc5a48b258fa008c8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:8f36abf47ed33e424b8f9b238694a7bcc082bd0e74d97cec7d6d7c7db47d6552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119311374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f3d35e10e7aed87113e0a46df8b64bf71b7f74180eee35877ee5d6d4b2fab9`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

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
# Thu, 15 Jan 2026 22:29:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:29:31 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:29:35 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:29:35 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:29:35 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:29:35 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb421340cf49eb838ba5a93e97c5a79263668d6c63b6e2bdec9f12f9cb2bbe70`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 6.7 MB (6666455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c5db002efd1716598d0b566d19a173dfe7126f0914b12e1fdc180f8a7a14e2`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bfc81f68fb579269742625ae883af1e68a469bdc3e47f9cb250ea7d67ceeb1`  
		Last Modified: Thu, 15 Jan 2026 22:29:52 GMT  
		Size: 82.9 MB (82914588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e85a99980b8d4fa689879cdc5ef70054bed61905df3549de46260caf0e47d7b`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51c7ce377562ca9379f5ea9def930b1be0d7d2ec4c48e18fb742a156f46361`  
		Last Modified: Thu, 15 Jan 2026 22:29:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd004e1dab8b1efc281255b5815cb666fe08ed4498b2c7431f2381b9ac7e4d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb254fbbd5847cc94d322f7ef8c2404eddc14d107a5f050d4e3991237a7e23`

```dockerfile
```

-	Layers:
	-	`sha256:93cae582c7522611a439a6c7a2a6faa7e7b2e6675c9c78f5786ffa27d2d6f7fd`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 2.3 MB (2310563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0a5f390a10ab6cf064a1f5fcd498996c18aba1bfb713c33773b1ba72a7f421`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:87433bdbd8e99019e7fc9dfecda86de557a2fc32b4cffa293bc27efb05d6ef27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110028972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1d2cc20717830f048ed113983a79ebf82d22879f31666972296654e226055e`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

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
# Thu, 15 Jan 2026 22:31:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:31:35 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:31:39 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:31:39 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:31:39 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:31:39 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b85d29ef9d1a5b609c04250a98480155038f067e295c06a12bb03a0b163bcb6`  
		Last Modified: Thu, 15 Jan 2026 22:31:53 GMT  
		Size: 6.7 MB (6678025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12879279037976dcf03bcb89fd8ca0258ae28a49fd3fca4e1d918ebf5f58334d`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 3.6 KB (3648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f5a1efb52cbac7d7d853d373b78cb1ba1da5dfb15cf3b70ff94110acc1144`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 74.5 MB (74482805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a655526e5e0376a0214f1b43fa2b17d9d392ec41f8cdc1cb75eb970f43d84d48`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff65ff8d1ea9fed765acd863744a83581bdc65244d1022c09ce2991a129a056`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:92a66a28c2cacf75f73de64fbc20b8f8a5872763b614692db0f69f380c2ce7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910fae9c7c765bca133a238b5b06f22cea8258cae915a0bcf97be00ba26d6b24`

```dockerfile
```

-	Layers:
	-	`sha256:e39d496af0bf62266e9b9be68acf22ce4ea001066b55cf8ed24f202031f749c2`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50900617900957d671f02b3d04cb4b737068c8a4c247e6954ab2762edcfedfae`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:data`

```console
$ docker pull influxdb@sha256:6ee054f5264bdf35995032887a42b386ae922ccfe379ea754afecbc2e73bf52a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:bd87962f04b5e5fd56acf0f5935868b4efca456b6fb8d1b3a6174d7151b0a8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114841526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d161b120e02516f0496e96c28167299a89d72e9f3a72d706593bd1360db73bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 03 Feb 2026 03:32:49 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 03:32:49 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:32:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:32:49 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf28d2500a471d1dfc3178dfb606f71b5e9ed292e422655433c53cbe73a6ca`  
		Last Modified: Tue, 03 Feb 2026 03:33:03 GMT  
		Size: 42.3 MB (42319821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13e3563e88a57ac2dbc95ecc269722c6eef212fb6a2aa36dc48ea85181dc9c9`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecebd9eeb3c29a4676848dfc8b528ad9036268a2b9d18f75976e281547931e6`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d318862ee1f525bef0688496e8db3ece435fa6af7bda0b6725f96fe856f198`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data` - unknown; unknown

```console
$ docker pull influxdb@sha256:9b708c6661337b3f859fd3a36f053b9ab9a12fbb2cf84b2ca62c18c9b8db5ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4700469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a28e355e551d575ad6a0d1cf2a567adf5be90a12bb7ea104cdd2c409a90c30`

```dockerfile
```

-	Layers:
	-	`sha256:5cafb353c28ab90688350fab88cecccd4ed633f9a275142cfc1fb890ad0925a0`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 4.7 MB (4686392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcaf37ce8ad2d98b4f978727f83d07f5c90f5f2ed44eccf2ffdc8e4769d81d91`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:230aced0d72a917905c28e8370266348fb49894a4e1d090c47765a1488e94bff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:40d2fef5a316bf72ec0b29c322a7cf01fbd7046fad6e09edef3afd6a2a51f192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47123756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8324e71acc24adb0423f7eb4de13354493b40f765bdb36448d77ce375caa87c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:24:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 28 Jan 2026 03:24:11 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:24:11 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:24:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:24:11 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adc499747d2c1716d5193ed87e0f6684b5f7da3ad6b0d2bdfc84d65ed106d36`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 1.2 MB (1225465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a172153dcef0bec4a9c7bb4c587f4400c9485a79c347dec788239589954f4770`  
		Last Modified: Wed, 28 Jan 2026 03:24:22 GMT  
		Size: 42.3 MB (42252778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b330c6f2273441c4cece26de32b1b56b5641f92928b4b5256a15fd7ef0db1a6`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb3efac6bd9c420eddfe57595ec744fa728401020c9af575cb9cdbe12776f5f`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1f1384e53b8afac073280a7d6b42b05cfeb3ad8ff3c328242a61d8f88d4018`  
		Last Modified: Wed, 28 Jan 2026 03:24:22 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fff49aac562db0793d72005156712fb335c4f0488b91b3f35e434498d2e282a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **791.6 KB (791580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cbe541688ac6e58740d2ecbecb6eaa4446654bb8c3635d47c1614319c2135d`

```dockerfile
```

-	Layers:
	-	`sha256:7746afe39499c0509347119e90a393e2f741f8c2e4a54628af8774335219ffeb`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 776.1 KB (776122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a10bcf68f284ed3ad3af63a4766b3825d0a6fb102c1dc2b1199ddd247f8f9cef`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 15.5 KB (15458 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:10d40128d7fb12259a57cee239c5dc600f99ab6ddb5d08d7e6bd072fa68011ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6f80d482e72e674d39ff987c9339b71f28341e6a98a6f358a9086f9fe7745051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127592285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6d7e2d453e9995658fa8751f2b6e84a64212eeee685595977f5ff7e512afd5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

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
# Thu, 15 Jan 2026 22:29:53 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:29:53 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:29:58 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:29:58 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:29:58 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:29:58 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d80b8916ac9be25ca39f63d725fbecdb5221cc992a8f8edc501e20aa7f6cdd`  
		Last Modified: Thu, 15 Jan 2026 22:30:15 GMT  
		Size: 6.7 MB (6666466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86baf47ce3b1fa8c7b1d7b1ba023420e80d040d1a773b90f1a3f1444d5398b8`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75782d754446062a195fd74ec4f45355abd9b48844b421553b76d0d92c2e9e6`  
		Last Modified: Thu, 15 Jan 2026 22:30:17 GMT  
		Size: 91.2 MB (91195488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0552eea07c1a62aaa4c8a941aa4d914694ed7a40fa2f205e24255b406514ab`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e9ae2043b745909b42322ca040a8bc78dae54020dbf787084712e77c63a890`  
		Last Modified: Thu, 15 Jan 2026 22:30:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:cb631e30f9aa3075f21e34d43d947684a1e2cf8b6db12b3870f5925ba45592bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0859ea2244b0defc0d27a58cd00c57d441a00b51b6c00983526ef8516503d2`

```dockerfile
```

-	Layers:
	-	`sha256:eb1c0fc56bdfe5de760e79c005402e18989d63559ec2f437944b534243db1c91`  
		Last Modified: Thu, 15 Jan 2026 22:30:15 GMT  
		Size: 2.3 MB (2310611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf90cea5e6b638571c01c3c00fe6a8b6e65cbff58a178ba08a0c4a0f3c9fc4d5`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ad6e83f930d0ab312e7f5a2b347d9b8aa7f6b4132db0409cf404e4bdaa0a67cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118244315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d65a5b3e4ed077bc1ba501bc9ce80427816521ff052532109d778edee858bf2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

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
# Thu, 15 Jan 2026 22:31:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:31:57 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:32:03 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:32:03 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:32:03 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:32:03 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bd4240eafafe3f7fe3f9bc5d3b023ea3b76cd522bea0a947b3358df8986ed0`  
		Last Modified: Thu, 15 Jan 2026 22:32:18 GMT  
		Size: 6.7 MB (6678021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a2eb424397e2fd233b9e3e45d8e2e2ff184ac156d640257caac83c500bd03b`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c9c7ab39edbfbc219f93a01abd342c7aa9ae427a6e3c461e19bc610c55633c`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 82.7 MB (82698149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f15f88b8a4272c18117de13ad2ba7f3853d372748c6fea818c9336b9023fb`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a262b7c40609324279929b50e3eff0cb9505cd033e5cf2e2dc7a38c8c4e0199d`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:0265bf65e9e0e0e1d1997518bf6b88e6df9698f769f086ef60bbaf2e790d4070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9a5cb8b7911fa2587aea0afc1d4c89be70eb8e24cab810c6172cc216e9d911`

```dockerfile
```

-	Layers:
	-	`sha256:9430335ba47f250a06bcaca7da5899e1461955a18254643114311ddb1acedd5f`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 2.3 MB (2311693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e36fbb81eb4a33ce5bfce27a827062a0b8d553c1d9ca2e76dc9b865f51041ac`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:8e911da5f7b482230e61fe4bad9af0697d97a75e087f19f5f0ddfee62c2bd686
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:3e23a8f949851d197977fd09f19d9f1eb026e20c47a7bc50e544342b1271b0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107232786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6152aaa4c9999ec462d1f8603b21da2898ea325d68ea261d6e968c290a56c832`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:46:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:01 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 03 Feb 2026 02:46:01 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 03 Feb 2026 02:46:03 GMT
ENV GOSU_VER=1.19
# Tue, 03 Feb 2026 02:46:03 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:46:03 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 03 Feb 2026 02:46:03 GMT
ENV INFLUXDB_PR=-2
# Tue, 03 Feb 2026 02:46:03 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 03 Feb 2026 02:46:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 03 Feb 2026 02:46:06 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 03 Feb 2026 02:46:07 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 03 Feb 2026 02:46:07 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 03 Feb 2026 02:46:07 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 03 Feb 2026 02:46:07 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 03 Feb 2026 02:46:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:46:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:07 GMT
CMD ["influxd"]
# Tue, 03 Feb 2026 02:46:07 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 02:46:07 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 03 Feb 2026 02:46:07 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 03 Feb 2026 02:46:07 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 03 Feb 2026 02:46:07 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebdc098e5a0cdaffe8ed5d5f890eebd95af1721e8ec4546756ceb4f430163e`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 9.8 MB (9798212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc0e0dd72fbd9e712238621797c89d4cb234ec5d85c98dfe1fdfa0010f6a4f7`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 6.2 MB (6156965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47df6264947c0be6c65a68d2f4c00d24721cdd03025fdef312c8350387ebc07a`  
		Last Modified: Tue, 03 Feb 2026 02:46:17 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8b474650c320c4fa7e427b734045bf8169128440699e3927b8e32a9a46720e`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 811.5 KB (811478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f29d94f894c69cf4f94fcbdd05fcc095c1cd115764b1f9b21c96a218459cee9`  
		Last Modified: Tue, 03 Feb 2026 02:46:20 GMT  
		Size: 50.5 MB (50451811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330889a8676412bd29ad7173684d77e862a32d09fbab87341197870a3a8c50b5`  
		Last Modified: Tue, 03 Feb 2026 02:46:20 GMT  
		Size: 11.8 MB (11775874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fab057e3af09b417219f54c4482818ce2423e4ee80cedada9bd6fdc39524e8`  
		Last Modified: Tue, 03 Feb 2026 02:46:19 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9450d960e36684fe03ebae034923ff3f8f80b333b11fbf3b8996dcbb6f0a178f`  
		Last Modified: Tue, 03 Feb 2026 02:46:19 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b6892e43ed9c1fe84e3e0698e7e9dd360aec039fa0da1b68a8fb16b19fbf4b`  
		Last Modified: Tue, 03 Feb 2026 02:46:20 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:23ff9cf2666d61d899a41d203def14fb121d6b101f6bca36372bce8c1a34bc53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93f9edb8656972ae76c2cefcf23e57f970e6bc60f5f7531dac82e63cae829ae`

```dockerfile
```

-	Layers:
	-	`sha256:dbfd23cb6459150f91cfb4177077668916f88a7be35c73219f97400bf39a4d06`  
		Last Modified: Tue, 03 Feb 2026 02:46:18 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6395b7f6985faa71e7a46f8563da258ae4074a12952a49080ff153ca8f4fe69e`  
		Last Modified: Tue, 03 Feb 2026 02:46:17 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1e0970c7a78cb343a3fef58c36489265de5dd8d88439da2ac6a0c756aca67314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103631393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a022c65734deebd7ae786beec5d29098b2b7103acd57d628d87ee77742f3712c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 03 Feb 2026 02:49:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 03 Feb 2026 02:49:28 GMT
ENV GOSU_VER=1.19
# Tue, 03 Feb 2026 02:49:28 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:49:28 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 03 Feb 2026 02:49:28 GMT
ENV INFLUXDB_PR=-2
# Tue, 03 Feb 2026 02:49:28 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 03 Feb 2026 02:49:31 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 03 Feb 2026 02:49:31 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 03 Feb 2026 02:49:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 03 Feb 2026 02:49:32 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 03 Feb 2026 02:49:32 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 03 Feb 2026 02:49:32 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 03 Feb 2026 02:49:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:49:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:32 GMT
CMD ["influxd"]
# Tue, 03 Feb 2026 02:49:32 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 02:49:32 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 03 Feb 2026 02:49:32 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 03 Feb 2026 02:49:32 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 03 Feb 2026 02:49:32 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2599dfe8bae66920a40e3330c8606c7ea4abcc1dae7fbe8c78e3cb0384740a3`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 9.6 MB (9626876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2b6f6792b00d9845ba09727292f97ea0b38def2d5575acb1edde6ec88b4df9`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7bb767f96a5889ba29375d4a2389c673c3f2f377d22b768418a970cb8ff0f7`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4d5352f32f1d5f51a290ca3be8a68181981219b1f607ad74d08a8137ae7a74`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 766.4 KB (766371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76584a43b5c55dbff3568ea7892e2d00770e0b0b88ba7ed53250cbe2a9dbfbd1`  
		Last Modified: Tue, 03 Feb 2026 02:49:46 GMT  
		Size: 48.2 MB (48229547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa502af2a66f75b29f67123eae52a712fd333ac4d595a9a0514ca1c20964d939`  
		Last Modified: Tue, 03 Feb 2026 02:49:45 GMT  
		Size: 11.1 MB (11100398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542140838c815e9f34996604794b30f64eb049e7809a6861e89b8d71c6a2d99f`  
		Last Modified: Tue, 03 Feb 2026 02:49:45 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b327a056230cbee6bcb0d43d19548b76ab4e11323d1ac8a58d0b63e2e26940fa`  
		Last Modified: Tue, 03 Feb 2026 02:49:45 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e24463b195d5e6be91b19c2dc72222cf8061412a3290816fd1f159cfbb5f61e`  
		Last Modified: Tue, 03 Feb 2026 02:49:46 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:a88f996b355bb1f02909697223697179d51071968381aae977ba44e7db326e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395e8b237b3dbe15def323a24ab4a042e28fe33b5cb470ba2f7ea581adef2111`

```dockerfile
```

-	Layers:
	-	`sha256:3b9fe95ec4b5730d2670759d109b96e5bc916bce1ebb711599288c70cdd9ce0b`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd1283c7a5a1e2c3bb73e96238f35b072a32efdfdff620b1a9140ba4e26b99e1`  
		Last Modified: Tue, 03 Feb 2026 02:49:43 GMT  
		Size: 33.8 KB (33815 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:595d3bf0fcbdaa44860691745361c22257a432d7498691e180afec4cf3038ab1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:cf5db12b97a9cff6ccc66d57f091f8e942dec53d549a3c4327f74c5513fb5ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91301354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6d9d34df08484050b015bb39f36ca5833ca36a069fc2521171ac563a18089a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:45 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 03 Feb 2026 03:32:45 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 03 Feb 2026 03:32:45 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 03 Feb 2026 03:32:45 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:32:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:32:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:32:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c301e5663c93730e853c177c2921beb662e8af6fd669efac8f485fcab5976e52`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 18.8 MB (18780858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52acbb2fe909f154b6eea1c07a48fd8e021e522282b1ad8d2d8a0896f8c940a3`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edea7eb3d12825920978031ef043c87591be9a1d18d4da302b7f5f32ef553b3`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:5ae9375a3129de2c571770f01c081367e812da11a7784f6ff1d6d479656df566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a6630862709599dc01c2841fc7a2a536d1fe8edefdb660b018644dda299f27`

```dockerfile
```

-	Layers:
	-	`sha256:741f6b7444af98584961f6b6ddab2d605dc0082a3e1fdc69ad7638fcdab8291e`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 4.6 MB (4591555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:727c7e09de0e967fbf5e91d8496e43c8ff8199c68a6f024a0136754d2fa2e610`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 12.6 KB (12591 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:aecaf75c0592866bc0a7c2639bb83f72193dda8ca322e9434210831a02a4857a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:334fda21d7660dabebf415a7630e82d71c49a482457d86edd5a02adf9ade1164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23592932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97dfff6219d548cae54fee570f6f3b37ac16ff0e9424df4cfe959bcf9b715512`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:24:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 28 Jan 2026 03:24:58 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influxd-ctl'             'influxdb-*/usr/bin/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 28 Jan 2026 03:24:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:24:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:24:58 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adc499747d2c1716d5193ed87e0f6684b5f7da3ad6b0d2bdfc84d65ed106d36`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 1.2 MB (1225465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdedda1ccaa8c658e38e6dd03b7ae881fe041e412d88964c2eeb69cacaa9d72`  
		Last Modified: Wed, 28 Jan 2026 03:25:05 GMT  
		Size: 18.7 MB (18723159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c532d4cfc611beb0d944a9d3a0ecb4f69dfd08641f9c026a71b9183ba72aeb`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0374a0e06643bd5572653262d38d90caf085dff084fc64403ebb1555477ec00e`  
		Last Modified: Wed, 28 Jan 2026 03:25:05 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:627437226023c906b3c6b7de5bce011926f537ee0fa9a386d09b87721cc83460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.9 KB (695917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987b431e9e9fe1201a9d3d2a53cbb79bad12a66fe71f7caaa35c13d123e4b70f`

```dockerfile
```

-	Layers:
	-	`sha256:6969b9ff35276f6935e71043cc1ec394f9218dd77481815cd0b8d155f1a4a451`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 682.1 KB (682071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d790fe636454d04353dbcafa3c3eb838b08379bec575783d2659976da7381a07`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 13.8 KB (13846 bytes)  
		MIME: application/vnd.in-toto+json
