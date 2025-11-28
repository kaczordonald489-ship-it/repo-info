## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:b0af56945b4f38e6add4998f31f514904b594055eb8eacb2fa4c4a944d14e3c4
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:1668b53c103d486daa1e5706c72fdb09dd45d82282ea99ddc1b74429199cc1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48480989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e96bf105bd4574278cf1ffaeaec74c81fc679c08dd9650c5a288312f5cddd1c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1763337600'
# Tue, 18 Nov 2025 03:56:09 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:883948e3c226127aebf5df5a86918602a745b91c14b36d5b2dcb12881ec26d0b`  
		Last Modified: Tue, 18 Nov 2025 02:31:50 GMT  
		Size: 48.5 MB (48480765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaecb793eb9ce3f3fe5b043228376adc77d888c5e5bb82f0c4b5583905cce737`  
		Last Modified: Tue, 18 Nov 2025 03:56:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d3ad518a645d054f93dad3e6d920f0634017c0fef75abe24d701bdca2d573ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ab3861c108d7c6391fe679a85711fe80ccf40f34c3d91aeffb014ea5d2849f`

```dockerfile
```

-	Layers:
	-	`sha256:b66afebbfe0dc14ce45366a78e7e98e2024d45b34d524f434a956e1c7ee0dffe`  
		Last Modified: Tue, 18 Nov 2025 04:29:30 GMT  
		Size: 3.7 MB (3733433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d8317840ae01063b65084f4fe164270e38716eb395c3b219991d7cbeed38cc8`  
		Last Modified: Tue, 18 Nov 2025 04:29:31 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:dd0159dc70ba99ff4ffafcd6ad5b68818ed37bfa46407cca2528e7d7071d1b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46016063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13c6947514851ed67167899d8278e2e9cc711c68726e2c1ebca67153cfb94bb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1763337600'
# Tue, 18 Nov 2025 02:16:57 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c31b6c5043e82226644ebd83040a826de44b35f97b37c4fb4970b4f366ff9d11`  
		Last Modified: Tue, 18 Nov 2025 01:13:58 GMT  
		Size: 46.0 MB (46015840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370137f0fe144e0e64e6fd5148f0022f0ce20188412f0b402bb26322a7499ac1`  
		Last Modified: Tue, 18 Nov 2025 02:17:10 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:50174bc69384490d6287bfafd95031939b1f334054c3ca47c89802691511d577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3709f0725a6b56b4f9ea05d6b974eea48ebda343664a09d1421c48257d6ab86`

```dockerfile
```

-	Layers:
	-	`sha256:4eff1556e35c5bfaf3ae5e43aeed344efb527fe04aefb9a1b3f118b7fc4fc344`  
		Last Modified: Tue, 18 Nov 2025 04:29:36 GMT  
		Size: 3.7 MB (3733634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8db490ca6a85ba47f44ba1cb8354e87e046f4c8a3028a63341e8405891d95b05`  
		Last Modified: Tue, 18 Nov 2025 04:29:37 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e21f1be7dfa3943e6efecb2a18ee1cedbaf30ba87c8ae917ec23971ffe3209ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44196353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95a7dccc1c0aa9f883ed49962031c70677e205db4125d37862d04c4d4caabfd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1763337600'
# Tue, 18 Nov 2025 02:18:03 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a0314049bc3db3505d41273e438af638b2db0b1521acd80219d0164d20e74b96`  
		Last Modified: Tue, 18 Nov 2025 01:14:27 GMT  
		Size: 44.2 MB (44196128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04457f475284c8423e05eeefc26d316f24b52184ce62f341b1ad21a45c4a4f40`  
		Last Modified: Tue, 18 Nov 2025 02:18:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8e9bcd133325f96c2e19844420003b8fefccdea0c1facc8d72ff074b24040917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c75962c9af4bcba0163a3dc41c7064cbb3e4632d1ac8d20e758add24183e80`

```dockerfile
```

-	Layers:
	-	`sha256:3200a58cfaadd833b9c089b86c04b97a288e8dfe878c4a2a8f86b38f061c6a40`  
		Last Modified: Tue, 18 Nov 2025 04:29:41 GMT  
		Size: 3.7 MB (3735612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27950208c90592e1e3b805e304105f3f518e4c0fbf3e05febb4a7ab2af01b156`  
		Last Modified: Tue, 18 Nov 2025 04:29:42 GMT  
		Size: 5.9 KB (5865 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7a9f7ad8e659b4b239b36f0d2bd3069b875c016142c2393397c766c2df02975b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48359365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2c11630546670fdb424c8695402bc46c2783de4efefa2bd88978784c1fb71a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1763337600'
# Tue, 18 Nov 2025 02:16:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f3f6bdca5da76c82ee8cfbb6a9bedef6980e43921cedab834f0b3b953bb48d00`  
		Last Modified: Tue, 18 Nov 2025 01:13:51 GMT  
		Size: 48.4 MB (48359141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0354759d7e91a4e89f77a10af25e4c2c791b90c5ce5fe583a78f6350ac163d`  
		Last Modified: Tue, 18 Nov 2025 02:16:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:20f1f307f9bb82e121345361c122f2f9d551af0205756f17038c54cc0121d90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4d59127f51922a702c1121d9bbac0e6c04ad177c650d55d1aae10666f1223e`

```dockerfile
```

-	Layers:
	-	`sha256:63926640c3132a1d6a06024dfc008fff29f7ca98873f054cc1ed0822a74b5fa2`  
		Last Modified: Tue, 18 Nov 2025 04:29:46 GMT  
		Size: 3.7 MB (3733648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a3ed219febb25b4e3c32a8d1e75b291f4d8ed108c7aff2a5e09d484174e9a2c`  
		Last Modified: Tue, 18 Nov 2025 04:29:46 GMT  
		Size: 5.9 KB (5877 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:f68880836d7887aac0693116c2124515c2b314d765285f54695fad34a666928f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49467091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd355897e7c53bbf0e297322a5b87b8b366cc7fecf84d3b19f9985cd0c42b9b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1763337600'
# Tue, 18 Nov 2025 02:15:34 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0ca4696a0e54fad0efe939c1b67848492de0be2d9eb67c2e1d26651af5ee6b0c`  
		Last Modified: Tue, 18 Nov 2025 01:12:41 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b4091a6833ce3c3d6dd279644e03588c65cc69d8d71edb7076773afbcba21a`  
		Last Modified: Tue, 18 Nov 2025 02:15:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a1f8e5c25fd25954a25c131c278eb3eff0c194bf615115c48fd1370de699da76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f81b501f978ebd095d5df8f4e966f9dc8d98f41f07a29b6d7465c34601fea1`

```dockerfile
```

-	Layers:
	-	`sha256:176b0768cce8baf01ca8f8a6616a55737c4893344ea89d25590194826433a667`  
		Last Modified: Tue, 18 Nov 2025 04:29:50 GMT  
		Size: 3.7 MB (3730630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb3c5f4012cc31cd58df1950bd6de5445f5fce1b24aa4d09911d934db359e1e2`  
		Last Modified: Tue, 18 Nov 2025 04:29:51 GMT  
		Size: 5.8 KB (5793 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:632b05d241fbed1c6fb7427b957685e43b58460cf7c25a89fb3786a769752aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48761179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441e91725071b4a9d1f5209ed4c161c2983840b06c1f68023f9c2f8f6e4697c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1763337600'
# Tue, 18 Nov 2025 02:15:31 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c5031a40fc6dfffb5fa4089b63f7cf6d308972d2fbd829581fbc842d1462b9b3`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.8 MB (48760957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8385dcdc6d21cfcb2a2499bd6f400b13d46c718734eba0a8493bea16916609f`  
		Last Modified: Tue, 18 Nov 2025 02:15:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7f72aad5032f32bbaf5b25ce0f4fa28c259670f9d089d57ccaed4892745a1608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c0800b9bdea4a42d2a86d93f1ab165e3d9c9f78f9071ef0c9f9971add7a121`

```dockerfile
```

-	Layers:
	-	`sha256:9107856e762928e438b53afc28151645ee4e958c03ced4e58f20a839a2ed836e`  
		Last Modified: Tue, 18 Nov 2025 04:29:54 GMT  
		Size: 5.6 KB (5634 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:27f33d4fc8cbf977e2c3b7613e2520b072d4661b9d191fa7bcabc8f53f6d66f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e019068cf367fe2e40e840f6af9ecd78eb351c96d357d8b1050920df7ba20f87`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1763337600'
# Wed, 19 Nov 2025 01:05:46 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6625cc1237175104f415e105f66606071d01619e3291ca567b5dd70a683ea1da`  
		Last Modified: Wed, 19 Nov 2025 00:19:38 GMT  
		Size: 52.3 MB (52326967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4352a36924e04b021b0c2f4c21f67ed6bf09b2b07b89d9c978c75939034780c4`  
		Last Modified: Wed, 19 Nov 2025 01:06:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ddb1ea5972a4d5e4f9512c80f5772175b84b32de65ebcbf2e88b7d8a03fa47eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f06db71f7d2c66faede487345a40d78b2b24b395d817174e82000027dfb2d8f`

```dockerfile
```

-	Layers:
	-	`sha256:cbdd57beea99c781a3ff9124faa0058669226b85750f851791ba17b561850b05`  
		Last Modified: Wed, 19 Nov 2025 01:24:26 GMT  
		Size: 3.7 MB (3737789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d42f5b987ae1b0cf090679c9c496a1f83bd9eabcb098011ae5b13cacfee54b8`  
		Last Modified: Wed, 19 Nov 2025 01:24:28 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:98eb659df31747f71b69e36c2465ea1cf75a08da6592039e010a21577767ad78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47137870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0557b8af38af2d6bfad12ccd601bdd7872b9cadf89403115f81b9b94eb64cd3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1763337600'
# Tue, 18 Nov 2025 02:13:23 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2809b292ddebb006dfe594389f6e9c1f72104847ade5a50fda030a5621939c4c`  
		Last Modified: Tue, 18 Nov 2025 01:19:59 GMT  
		Size: 47.1 MB (47137645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dbedcd3edd401c91dd3b28c453f5f244c5604425135f6cbebe369fe26de614`  
		Last Modified: Tue, 18 Nov 2025 02:13:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:033ebcc581b207f15b9ea4afeffc990882dad4b62a664247da1b3bafd79903e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c856c594fb3b9aa11e25d21f6de201cc2c414e5a15920b2902e1bd67cae5138`

```dockerfile
```

-	Layers:
	-	`sha256:3528ac663dab35c321d10ad3200bf40e251ca0fe90d66ee9d312ae935f879f72`  
		Last Modified: Tue, 18 Nov 2025 04:30:00 GMT  
		Size: 3.7 MB (3730271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f47f2e1fb6d4e61dd2bc9f1bac35226ead54aad394d77f126a91e17db3921f07`  
		Last Modified: Tue, 18 Nov 2025 04:30:01 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json
