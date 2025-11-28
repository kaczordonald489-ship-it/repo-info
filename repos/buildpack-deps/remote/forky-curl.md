## `buildpack-deps:forky-curl`

```console
$ docker pull buildpack-deps@sha256:bc7cfa89a342830458d8af700dc2994ba0701a15c525b20f54b034d778aabc06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:forky-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5523f0fecdd43c619da806834620782bc00d9d63ae355a5902bbbe6772be1e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75717968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbe96a3d8293e0d0e8d5fa7301b467d940a2e4882e544836d9917d3693db8fb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 05:10:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76694dc296168bbffa890c84fb372e9c250bf33e0ad63a6146b169a57d983e2f`  
		Last Modified: Tue, 18 Nov 2025 02:29:31 GMT  
		Size: 48.5 MB (48500434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cde0e5673dcde1a0a75a6006c0aa8bc722df9feeb622b9a6bf212e2f178a04`  
		Last Modified: Tue, 18 Nov 2025 05:10:46 GMT  
		Size: 27.2 MB (27217534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aafb615598ea65eea995ca1eaad3d411764331170d9bce17eb70b6ce97bceb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4105064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36afcc6d40295756ea9af49bda84c274aaedba7c10d719dcebab232b6f0f6169`

```dockerfile
```

-	Layers:
	-	`sha256:62c0888d4d38f28e94269c2fe229d70d9fd38834dd6a5e360a1373b470486ffe`  
		Last Modified: Tue, 18 Nov 2025 08:21:11 GMT  
		Size: 4.1 MB (4098291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b81fd0960f1eefd2440d9e0f83cd3ac3a95d4a3e3a2427df54ef0a049e874869`  
		Last Modified: Tue, 18 Nov 2025 08:21:12 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fa5e322efcb3664078e5f02c61dcc7b22eac747b120540176f32f94798ea0583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69949165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80679a11624cd159278585320d75ce9346c0ee2ded312cf77dcde8528ad3a0b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1dd1fa3a56d87bf4dcae80a33b02589ad31d81e866bca9f061ada67db33c8854`  
		Last Modified: Tue, 18 Nov 2025 01:12:58 GMT  
		Size: 45.0 MB (45003762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6f4451a2be0f51c6d1714f46485883bd5db54f8b6d9217e249d632dee61a5d`  
		Last Modified: Tue, 18 Nov 2025 03:59:12 GMT  
		Size: 24.9 MB (24945403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6ef8510853eeffe9b7ff42ff917aec9d27d83a11f21b34c1c47777ad9fb4545a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11cc2a3941ff48dd0d1a245aa3dcdbaef122cf798762f0981a3c6974ffbafcb`

```dockerfile
```

-	Layers:
	-	`sha256:5954ef63def5dbb9baf36a8103240aff1da6f9adf226a062b37e48fc72618cd1`  
		Last Modified: Tue, 18 Nov 2025 05:23:03 GMT  
		Size: 4.1 MB (4099787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04d224584f1ea9d1bc56473b4a1f47819aae0436a4205e7a1f5c3679116e7472`  
		Last Modified: Tue, 18 Nov 2025 05:23:04 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:51283ca85308f946d24854b18932775dd39002ef4d51a627111799898a0bd083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75035833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c968711be079e65bdf24106e9db039767ac98ec05790bb054bdfa9b4348763`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:25:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:25dea15c4ffeb70e1112f1ee06dd948a8ab9dfc3b79ef239cb96080cc27ff1be`  
		Last Modified: Tue, 18 Nov 2025 01:13:47 GMT  
		Size: 48.6 MB (48591184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e989d2e0e09f298fb48c4d6ff3605064bc05169f4e2b9891ccb3261afe85988e`  
		Last Modified: Tue, 18 Nov 2025 03:25:51 GMT  
		Size: 26.4 MB (26444649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5265c4dfb4112f15190ad9e22dd0b1fb3c795dbfeaad1ebcdc64f7837f4a29a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cfb31dbcf79747982e0ce247bd32724b31658dba49a7e669bfaae92b6a33208`

```dockerfile
```

-	Layers:
	-	`sha256:e4986222764a6abb025524d916ae549a5a4cc65bb83520859c2c6f5ae2555698`  
		Last Modified: Tue, 18 Nov 2025 05:23:08 GMT  
		Size: 4.1 MB (4099184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbf0b3f09dde9583e56a1c4e28830a1d75a70644c072c1f1c642e30942e2acd1`  
		Last Modified: Tue, 18 Nov 2025 05:23:09 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f379a216572a161849bdb97112c14c2c83210a44c286c833fe152f17fce9466a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78275807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2d56d797841d485b3da5954a8109a4a4d608b7416806ae840b1abc8dd5a8e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 02:56:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:898cf630ac245ec9ad865c96204520b86bb7b8760d5bd2f14bd02745e43d82f4`  
		Last Modified: Tue, 18 Nov 2025 01:13:40 GMT  
		Size: 49.8 MB (49832238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2307ec487a47570033147c5c7a8c176eb531df9120f57bf768d32ef164c1efb5`  
		Last Modified: Tue, 18 Nov 2025 02:57:08 GMT  
		Size: 28.4 MB (28443569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2fbcbb0578af7d44792efb77143dc075ef1aeb1c6c708bcdcca7e92fac27ed2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91660a87ae5c95280d0cbe70fbcf9e72fb1dd346c66861a8f6f1c6b44298ff22`

```dockerfile
```

-	Layers:
	-	`sha256:40ca005418d30d78606920db06891f3afa0c53c7650afc8b3c1fbf823d13cb65`  
		Last Modified: Tue, 18 Nov 2025 05:23:13 GMT  
		Size: 4.1 MB (4095410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c667a52c8e98f86af9e920e26325d132fff98c1e740209b12a9bac640a179c1`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 6.8 KB (6751 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c0f2223b511f814a16a2c9260c3586bc499a003d19a951b616be7c92f9e1f39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82170448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76327eb287ffceb923ea0798d02ce16fc00ce502ee9c8717b004ed6bc873107`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 16:55:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:56aec8ed2c7425bd4d962ece466e2022cf4900d838eb52bfdf10fe6e2569b4bf`  
		Last Modified: Tue, 18 Nov 2025 12:56:44 GMT  
		Size: 53.3 MB (53334632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2237e36f3e4c10c1103d8ec79492c7f36c02c01d9c3a6f4fce75f5099f037ed`  
		Last Modified: Tue, 18 Nov 2025 16:55:33 GMT  
		Size: 28.8 MB (28835816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:17f91e25e99b15cb94af695dcd57ad8a50c889bec8160f53fb8eca9044b7a02a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b3f6836902715c98812766b1aa4a8abafde4c1fcba8b8ef5d949ad854ddd1a`

```dockerfile
```

-	Layers:
	-	`sha256:11c75d74c146e2c89f4b9cf18a7c0c4789faf4e3a921db4836781cb5b76f361f`  
		Last Modified: Tue, 18 Nov 2025 17:21:30 GMT  
		Size: 4.1 MB (4102124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b581d7dccd7680a9747e166990b1246491ae326019466716dee1f688a4548b1`  
		Last Modified: Tue, 18 Nov 2025 17:21:31 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8caeb160a69c812ae54bc1277c0746a406a39b6b31c42e13cb99c81e29bffa56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73201368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d53ccb4ec9ed83a6ffb34e6f287fe110f5e755e501bf8e675d65512d9da0325`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1763337600'
# Wed, 19 Nov 2025 19:29:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5f062c29e53f6114ba8255e90dca3ce517e3e0563bbe15af71540ba740a9253d`  
		Last Modified: Tue, 18 Nov 2025 01:31:28 GMT  
		Size: 46.8 MB (46806333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7e03bce6d0d0951954641ed6a59e64caf78431003e1f4dc54250fb69de83f0`  
		Last Modified: Wed, 19 Nov 2025 19:31:39 GMT  
		Size: 26.4 MB (26395035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1439ec7041af855fc76bbffb603a296e49b5b532a32a0fa8248155e6b5aa29fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4097579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9287ef59b25a39d7555b6197c69711059a0ec0f87825e178dec60265409d9d`

```dockerfile
```

-	Layers:
	-	`sha256:cc363b7e0744a9e9ea1091a0784c305e0c1c22b0acb16e57b60c1f1cf57a3680`  
		Last Modified: Wed, 19 Nov 2025 20:20:08 GMT  
		Size: 4.1 MB (4090774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8efdef3d20390c11ce2e31756133bcbd98227b183de0566a5652a9f4fa9795d`  
		Last Modified: Wed, 19 Nov 2025 20:20:09 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:425815a870666c3d7b44fc90bb87e461756b3d7ff3f03b738a7d592d48aa5398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76709782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50ff7837592c1cfe7a9ceba77fe83e192667a0ea2b2f965c084c9845221d191`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 08:14:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bb1941d24f39dbf96b6d3045499ee523d7b760b1ecc1834da461428a6b3f02c0`  
		Last Modified: Tue, 18 Nov 2025 07:24:21 GMT  
		Size: 48.4 MB (48370930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f46e464db90bd7a8600e77f0c0366b640edbb2b0782938b210f31a5e2ef6ff`  
		Last Modified: Tue, 18 Nov 2025 08:14:56 GMT  
		Size: 28.3 MB (28338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ff91964bb774edc25dbdfcfa6525cf2f635232c7cb0ea03c37689caadbd984b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de023375f06bd7734129942de1515a587c01c1d3a11ece0b7acd1c2cf5172897`

```dockerfile
```

-	Layers:
	-	`sha256:05f214576df5609f4c4c61c1454d2f9d26363e53ea672cd8d2b2540141217310`  
		Last Modified: Tue, 18 Nov 2025 11:21:19 GMT  
		Size: 4.1 MB (4099700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53dc64ece52a670f47789bd0887afc359d002fb0c2f00aa90ed982ae63d4190d`  
		Last Modified: Tue, 18 Nov 2025 11:21:19 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json
