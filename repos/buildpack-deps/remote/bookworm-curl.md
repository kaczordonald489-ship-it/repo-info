## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:92ec32f380e42926f126c174542501d8faa78483278300f2f5dec2613a49320e
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

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:79e8e6fd69376ab4ec511cee888e8c5c985b7ab9c26d23ac4cf4dea416c833cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72510109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01cdc78e568ca2f7de3f938e0e365adaa7a13cb063101457219e6f8af59b0669`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:25139977541dfef9ba91071aebf14ca7bc17f3d198989e5af7efacd12ddecb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280dce06a30776417eb50cdfcfbba471344618a59f1f8757123ff95f528cf011`

```dockerfile
```

-	Layers:
	-	`sha256:cbfd9a62cf913d0cc8074c4d87ae81f9b27fe79b675c085ac444fc14562962b0`  
		Last Modified: Tue, 18 Nov 2025 08:10:33 GMT  
		Size: 4.5 MB (4513691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3b8f55e0c4ebfedf270d04fca488707b4ec6c431f0b88a5a587011a1c8a3435`  
		Last Modified: Tue, 18 Nov 2025 08:10:32 GMT  
		Size: 6.8 KB (6814 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:dc3dab9af02acb7909839e7768c04fb36e96655184e8efed0b9f168b6215a18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68721585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b831c14d7118af7c95e503f956ea407ecd9d07d37d0bccf24f28ed96b53faf19`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:26:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e9ddcd7a1b6dfd5162ea10e9d236186eb8c814b710fa53b95a5a543a21573b38`  
		Last Modified: Tue, 18 Nov 2025 01:13:58 GMT  
		Size: 46.0 MB (46015831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad589659a3ab8a5efe8198e1ee9fa790fcf26937e030eba01738a074b5c099d7`  
		Last Modified: Tue, 18 Nov 2025 03:26:40 GMT  
		Size: 22.7 MB (22705754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:25fcac2c2d76d9f7cd03b543c7b293bfa3193f70c978d449a6ea4d01b20799b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:841d7b974ce4fd817bd2f24c9b22c0f00f418d7a764918a8d11cb3912fab463c`

```dockerfile
```

-	Layers:
	-	`sha256:d80ab1f4dc3f801aff84f6339d160884594ac637a6f5be148647cdc37dd69f79`  
		Last Modified: Tue, 18 Nov 2025 05:22:15 GMT  
		Size: 4.5 MB (4517507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3f284f658bd915fb73383629095df8a5af1abc1c8e8b8e3033639b2d1357b8`  
		Last Modified: Tue, 18 Nov 2025 05:22:15 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c30b4c2022447ed44b67d8dc700f803a090ca631e9a427a9046aa3eaf54bb1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66130811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93e60543d352f2ae79ffcac34200f27e6cbf413f29ab4c295627bc002c1c595`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:08b2c968b649416d814d17e039c5613d1dae852705140660d137eb89e6640453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5619715acfa0b1ee727a671df352e6dfb765e9eb93decc247a1f2b8a57cc78`

```dockerfile
```

-	Layers:
	-	`sha256:0847f3145974be0a21ac759e65ec7bf64923e919ff0b6ab6cc711a2669fedaf9`  
		Last Modified: Tue, 18 Nov 2025 04:19:36 GMT  
		Size: 4.5 MB (4515980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cac7c474fddd84d6f470217e5eacb77c3a9094096256f13bbfd97a2166728a7b`  
		Last Modified: Tue, 18 Nov 2025 04:19:35 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a84042e450f341653d4d2b26ea3d7135d53ab21988e68669482b566d4f49ed24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71957458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6446cde1c344cd45bbf84365287b8cfd73021925d1011c59e0c5dd23c1e750f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:249ed850f1dd5b1ad581f158844810e12f2894770c33455514fcf2a7024b372f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbe45b5e5a307507a9c5c03d3c40db837d5d0958df4d0bc6580cd3c5ae358e6`

```dockerfile
```

-	Layers:
	-	`sha256:6d3dc6bae02a1285f8da7e8740b434e6accc3a06ae54f299b6d9e4113348b198`  
		Last Modified: Tue, 18 Nov 2025 04:25:25 GMT  
		Size: 4.5 MB (4513952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb46c124dc41c6b89d593537f753b240a04b99d814fb5c68e34dff702ffe02c5`  
		Last Modified: Tue, 18 Nov 2025 04:25:24 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ee6fb50cf91ecb96664d4f46b07a0aa510051e51599d45e17895e0a7e4081430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74331284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2872d653f98806380fdac58ee24265c0f3f3d7c27fbf1f113185a32d7f8349`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:56:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1ac37f50532a7306717e1be2f4760a581740981b55bfee41fb74edf971bbbb`  
		Last Modified: Tue, 18 Nov 2025 02:56:28 GMT  
		Size: 24.9 MB (24864418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0755e60b4f939f81c0c0feb0f30e455777020fe7ff193c7d5d67f8f021b7a790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee402064df815218bf05ad771fbef2ca2ad21e52a9ad4f7b2605a02e124e2a3`

```dockerfile
```

-	Layers:
	-	`sha256:297090e2da6037cce89df0d5768e5f40edb0f97cd0d3f1f4f3011bceff75249a`  
		Last Modified: Tue, 18 Nov 2025 05:22:26 GMT  
		Size: 4.5 MB (4510811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc2b12042b7a2eb3d7fe391c35b4600e5f504f6ac920d9fd267e1c59e9f42b30`  
		Last Modified: Tue, 18 Nov 2025 05:22:27 GMT  
		Size: 6.8 KB (6795 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:83ded9ef4968670a76f9d5e64355f969ee935dd462a6b0ad16adb78d9a0b7907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72374994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63b109676039624d88643b6458a868a23ffe90d75d030f986bd85bf3babff22`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 19:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6d4a3f53f449c0e9b84d889c71d1f21df5764d821465bd1337060660aa78c65e`  
		Last Modified: Tue, 18 Nov 2025 01:11:17 GMT  
		Size: 48.8 MB (48760956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754bf41c56cb3beefc6b6211c26bdc048d41c337f12bc0bbfcfa89dfb5de99b7`  
		Last Modified: Tue, 18 Nov 2025 19:40:58 GMT  
		Size: 23.6 MB (23614038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:362dbe90e78bb2b9331fe7fca3eeb521e9def9f745a31a823f404552f3da461f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693a69024f6fb205b96ef575e57bf63efa845e8f64bab2912a53d1a21d770931`

```dockerfile
```

-	Layers:
	-	`sha256:9336f6ea30ae6e73fadb64634adbd532bac5df480f63499b2650e25a6eaef946`  
		Last Modified: Tue, 18 Nov 2025 20:20:03 GMT  
		Size: 6.6 KB (6649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1d582b730d05175fa804695cd91feac89840ca99f60352d1253ae1cfd9948b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77998981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5d4763162626ba3718d8a5ab909c788420830a10861d3eb4488a40cd793a74`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17787af1df16ce560e48a9be892094ace19b1aecc7f06ca1e97a2e20987822a5`  
		Last Modified: Tue, 18 Nov 2025 04:05:05 GMT  
		Size: 25.7 MB (25672018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cef966cc031e1450b5ec57e1980e922c69fbba19c34dfbe0f1e4a77df75144e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90fe570aa4d38913841def26761f8a965785b8af00336aee7d335526a56fcfe`

```dockerfile
```

-	Layers:
	-	`sha256:c0e5304d59ab3fca6ca18b88b5d0875f27ee468a871bf51435149ae4fa6b50fe`  
		Last Modified: Tue, 18 Nov 2025 05:22:34 GMT  
		Size: 4.5 MB (4518315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b71c78d23aaad7f602bb20a284f897c4e570aaaef59576f7b23b133797001c7`  
		Last Modified: Tue, 18 Nov 2025 05:22:34 GMT  
		Size: 6.8 KB (6848 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:166b3b250c2d1996da724ed913fcf6fa6130067f7f0aa4a2e083dd2dba4c7200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71164821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5eec6e9f686ea65ca29184e15ee52164b1860b0dabda12383db3f34565e625`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f80247bcc58a5a903807561f3aad626158855a07b7817a9ed9975e9775ae2`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 24.0 MB (24027180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f16ae0686c09031c3054990cfc2d42dad5583f380c7afbc46985db44cb65c41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefd51f9802aa3775c5f41819fbe0782b3cd3c530930cbbb91718426c3686dec`

```dockerfile
```

-	Layers:
	-	`sha256:9b34964e5caebdee9e6ed20b8f79d47951350eecbc9264747514301c594f9963`  
		Last Modified: Tue, 18 Nov 2025 05:22:38 GMT  
		Size: 4.5 MB (4510495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edf2257c81946ebc9660f67f3fc57992a6bf1cb03af326d735501a42a789c031`  
		Last Modified: Tue, 18 Nov 2025 05:22:39 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json
