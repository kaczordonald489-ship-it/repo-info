## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:cd059bdaa9c7cd3def69f7499946290c69fd8fade0f79aa385943eca38db3a1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:a87bf0356e7145b7f256ae2ee576582c825e425245a3799617e59119b0654374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48480985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48dbc8d1ea8b83663f84c5ce6970914b111b618b9f2b96aebb14f6e3510b33a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:54:14 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf76e85fdd6083fc6b4521046c82a076504c6be1713e7cda1d752199db2015db`  
		Last Modified: Tue, 18 Nov 2025 03:54:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:71e68eaece1ff99c224fdb861417129d28083914a7e183342e2f520413f82815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167a8a338695afd5652231c332494dc9201ea03c9feebcd976b32e673abfbbd6`

```dockerfile
```

-	Layers:
	-	`sha256:b1b17400674e6f99ee60f72fd278254e44a521933bffd5f814918b9a0487e1ab`  
		Last Modified: Tue, 18 Nov 2025 04:26:56 GMT  
		Size: 3.7 MB (3733431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91923206e1bb2b5de6d393abb4d3efd74192ec87add3b35053eec8c2d1a3f715`  
		Last Modified: Tue, 18 Nov 2025 04:26:57 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:0256e6ea0664ea3f97e31a45e16adf12209bf9f434a4f71c9e5b0d4627fff137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46016053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef8f39337ca64be1abb0f1f9630429bc03b0382463dd6cca993d62dfb01384b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:15:54 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e9ddcd7a1b6dfd5162ea10e9d236186eb8c814b710fa53b95a5a543a21573b38`  
		Last Modified: Tue, 18 Nov 2025 01:13:58 GMT  
		Size: 46.0 MB (46015831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314640f36c80eeb14c55c39db4840b0ec4b65e12f3818749f24052c7d6af8e8f`  
		Last Modified: Tue, 18 Nov 2025 02:16:07 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:52f7fc615147d4c9b1055722f0509993d6c06184165eaf8568b8ec47000537f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ed60c87479a8a5edeb01386892ba73fd6ce09a4c0a7bde971c963208d27e66`

```dockerfile
```

-	Layers:
	-	`sha256:2dd0630af74eaf9d37c48d92880d10ea2e961126d4f823b090f1d7cf96fa08e1`  
		Last Modified: Tue, 18 Nov 2025 04:27:01 GMT  
		Size: 3.7 MB (3733632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4043dc5b0107734d3a89cfec44b3700e30b64d6959fa39e485d1a3b85e8a3e0a`  
		Last Modified: Tue, 18 Nov 2025 04:27:02 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:d19c66400318ef6827b4317b56f58733f5cb902dfca99d46ebf337554c0a872c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44196349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f465f8ec14ff20ce2f046cf260107687f48e756220f8f67c0068aea0ef2dfd8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:14:34 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846403c93d7b76f6425856e22e5634c67162a9080c85696bce124a036f5bf258`  
		Last Modified: Tue, 18 Nov 2025 02:14:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e8f110937fe3b379fae4cd2ea72d975d87090a3b1ac112081449df82200c52ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c510a10159e38bdfdba3522d5b13675cfd01b72b317392b8a31b3020f8b16a`

```dockerfile
```

-	Layers:
	-	`sha256:fe1b498cd96b270693d50bb5c5a10446345a16c3213be385a9763bb9f2f741b9`  
		Last Modified: Tue, 18 Nov 2025 04:27:06 GMT  
		Size: 3.7 MB (3735610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69ff36036dd516c53f68f7b5a965eefe17b890c7b49a9ee31e6b584b67092264`  
		Last Modified: Tue, 18 Nov 2025 04:27:07 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:02ea231ffcbbf0803f558d9f057a67871e56f612a8f23e35632e00bc74960b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48359362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0916cf701d6c0221cdd2b7101dae780bedb173243518a674ddcfe8eaa4dd51f7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:15:37 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f423a264c9c7036e5f8eaec8691938446cd0de8912b25ee42ac49fbeaf8d0b`  
		Last Modified: Tue, 18 Nov 2025 02:15:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:33804cd19f2b33e42a4c18bbf551e90d848b7d141745ff1e792cbf3b822b1bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3151f555f34faad38dbccb5ea2835137bcc62363b3c3ad66b53a1c86517e0468`

```dockerfile
```

-	Layers:
	-	`sha256:6e5b1a9e88887425c812e14cfff8670dead4f40e3b3f7b725f213673360570ac`  
		Last Modified: Tue, 18 Nov 2025 04:27:11 GMT  
		Size: 3.7 MB (3733646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdd7d5cfe9f6933b730e30ebf36efc199450b1aec23261fa120f63da1e9155a1`  
		Last Modified: Tue, 18 Nov 2025 04:27:12 GMT  
		Size: 5.9 KB (5871 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:74dc1547728ce0dbf4d48718abcd76ee2da69959b00de8ad8674a92e9bb2beda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49467091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dcc448778597ee90ac5d0f1dc0cd143977d4e4fb771c2604f09f983f85b60d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:15:33 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dfcf57e0d2ee31dee0f227e523205ddac54ed173f85d5cc862a62fed7c1f23`  
		Last Modified: Tue, 18 Nov 2025 02:15:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bbbcd4ebfaa002d024c9cf9bcde688f65a14f6dd591b45db6a231e588329f5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1bc829d22ba69cc920bcec3877566e9120fffc9566059ff20646d3215edfe4`

```dockerfile
```

-	Layers:
	-	`sha256:91d935453d1ed6f969f8f1f79ae8cf9eba5931e9821bdcffe9dcd37d36bc9f6d`  
		Last Modified: Tue, 18 Nov 2025 04:27:16 GMT  
		Size: 3.7 MB (3730628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5191b6e6997799766733ea503f7cdf73e3dfc0337c1fd9fd3f70b2eb523ea9d`  
		Last Modified: Tue, 18 Nov 2025 04:27:17 GMT  
		Size: 5.8 KB (5787 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:3db3d2de5f294ff48ed8f042abc652f79fe08fe44c754646e5ebf22608a9daf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48761178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c03e0c617207d25a973f949d79c3893a456a3c0ca043a5c0e235014ba8cd24a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:13:51 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6d4a3f53f449c0e9b84d889c71d1f21df5764d821465bd1337060660aa78c65e`  
		Last Modified: Tue, 18 Nov 2025 01:11:17 GMT  
		Size: 48.8 MB (48760956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04b0e0c610cdcc2052900263713a5aba4414be9cadf3589a4f8619ed8155df8`  
		Last Modified: Tue, 18 Nov 2025 02:14:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b0c223a3f5d2cd42ab643d006643b0e50ab24b5ed97a6351c14b57d991569e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6045de3d48b5e57bcc825b9590ea6e29914044096a1496c9bf9406c0c11d9f6`

```dockerfile
```

-	Layers:
	-	`sha256:6b552ca2fe984e8023798f01eb7bd3a1e54ceac884bc44f6f9e9edc3016acd48`  
		Last Modified: Tue, 18 Nov 2025 04:27:21 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:19de903dd6cc9c929c3bff9a458fb1c870f8e6123bf3f72c9ace09f48612ab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132d1b170a91f8e03822ab7bfaa5b53d92672e9167c65c3785e7b6b2cccbd391`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:13:18 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f318c8a73acae0b9f1e2714149744fc54b8fb3506e2d117191ea7bd2471f6d`  
		Last Modified: Tue, 18 Nov 2025 02:13:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4f10b5f882b68e46b15f42919fd986455604d15e6b912e0f15a51638d0d30c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc6605f4a51d54148e45d41a376c2d0f42d5b88cb463826c6d3ad275215b3ca`

```dockerfile
```

-	Layers:
	-	`sha256:8f315b31c50737333a4b3ba0aa706c3c3cd78c30f7973e73afe78d3fa45472c3`  
		Last Modified: Tue, 18 Nov 2025 04:27:24 GMT  
		Size: 3.7 MB (3737787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecdcff6cc11e8381ab6ff773bffc31a1bed424ec1100b98c1379482a5d200799`  
		Last Modified: Tue, 18 Nov 2025 04:27:25 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:ce33f6b7d0f9c2d2b6bebda5474faf225d595b8d4d3b17a3f9f13cd44b996dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47137867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf6a3a5b9814ca92fb88dc01c238b4ed6a07eebb03585956a4e568051724d86`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:13:02 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb06a5d4ff1b94ab5f38e7ba507fb2abd15e7c3b07ca752560b1fe5c7aec1cb`  
		Last Modified: Tue, 18 Nov 2025 02:13:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1eec6b2aa44faeab99a084bb91f20306a7f1b561280ac8f57364a806058e139b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1e2d78b8ba934e7c09cb01505f368635b30d10698574c9dff33c30ab4e2f73`

```dockerfile
```

-	Layers:
	-	`sha256:6d1373f592dcda8f95328f4c93000c5ecb201d23375efe999f2fed7279d023f3`  
		Last Modified: Tue, 18 Nov 2025 04:27:29 GMT  
		Size: 3.7 MB (3730269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5534b0be38aa250854a84b82c4bfbaecf180e0836cfdfe7ce91d3e67cb624efe`  
		Last Modified: Tue, 18 Nov 2025 04:28:17 GMT  
		Size: 5.8 KB (5803 bytes)  
		MIME: application/vnd.in-toto+json
