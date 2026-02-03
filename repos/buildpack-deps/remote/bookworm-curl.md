## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:27002dd0e96bc92b6a0169de991eab53df622b211a63782efef685336917f085
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
$ docker pull buildpack-deps@sha256:d8879bc728ac7c0764e308f22ba436f8bad2b5bfa0b463684dd1d641706928c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72519929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60f9f0ae8eeb825aa6b8a15a2ea60bc7b7139f7e72a695a8217a45e196d1d21`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:952bc903af6d7a9b5a7dd19afab8cc73d8170dedeb009c0f034b0b32521ea484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ee624a8f11b76d72ccfe31f4fb375e92e46d54edc8316a067060788a2c25b7`

```dockerfile
```

-	Layers:
	-	`sha256:256816d9208ebc4ad765cfdfae623b751d228d5e69bed7d06b0e3b397685c86c`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 4.5 MB (4514334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:902762d96a20fe2435a3f137a7d9873b01a3be076223d73bf8b713861bc1e341`  
		Last Modified: Tue, 03 Feb 2026 02:41:48 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4b3d1a3c35d0c2a8feae491795861cb3cf0942b8457b83a5ca828053db0539dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68730571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83ffb1d7d4120e075c1964d643ff0e3533f8252f66336752a0186aa4e0734b6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:48989bca0bd1f08c49cfd2a8eae58c5ffcacc0f005e701953d88f28a5e398ee1`  
		Last Modified: Tue, 03 Feb 2026 01:13:21 GMT  
		Size: 46.0 MB (46016664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8c031851c0852eda9cc103afa92ccd1ccefa07dd936a71f291d45de349d70b`  
		Last Modified: Tue, 03 Feb 2026 03:26:08 GMT  
		Size: 22.7 MB (22713907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:870a33044461421739ff5b4a869a872fbefc691cefd8696372286869f9180980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e8bcfd0f3724cf56727bbcf05b5fb45363544d8d193f0136a25f8e88d32e0b`

```dockerfile
```

-	Layers:
	-	`sha256:3f8096c1937d1063e8269f60b806128f1088b5c0dabf4ee38d808c835466d57b`  
		Last Modified: Tue, 03 Feb 2026 03:26:07 GMT  
		Size: 4.5 MB (4518150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeda3a98452b7687e4f2084744f06111fdc68632c7f6acca7828484391283a95`  
		Last Modified: Tue, 03 Feb 2026 03:26:07 GMT  
		Size: 6.9 KB (6879 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4683071ee2c83e0b81fd6b5cc54628f345dfa7df4968ce11fc73729fcb8a31da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66140778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137b19127b5cf8dedc180a48f2e5ccdb6b44ee49bb859e45929e69a0053e7c0f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:424cab4c9a6a41cd57ee6de8e95726c4d76fe3e913bd9c7731865fd244771971`  
		Last Modified: Tue, 03 Feb 2026 01:13:26 GMT  
		Size: 44.2 MB (44198733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7fc27aeb6b79b5764735a819c5fdf5feb13c904bdffa0dee2b4c1c5f3935e7`  
		Last Modified: Tue, 03 Feb 2026 03:30:05 GMT  
		Size: 21.9 MB (21942045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1bbdd8b2db3c22211586a6fe8bdc18bf401dac93ed1795b433e3cfb288c9c528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4523504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7213706585a09064cc5dd8f733dd3374c1822cd2ea2eab3ff0a10f6d912c9b4f`

```dockerfile
```

-	Layers:
	-	`sha256:1aef014e9d378a39c3bd45b82ae0bcacf66a141410af2b2b32195dec88663d82`  
		Last Modified: Tue, 03 Feb 2026 03:30:04 GMT  
		Size: 4.5 MB (4516623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17f3a8a92a5aac7a45cfde3a96d28c3afe023fbc6812979d0eca2d6849af09dc`  
		Last Modified: Tue, 03 Feb 2026 03:30:04 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2407c0f5c4c6c01eb497c8ca4bca6466a77e5d69b6017f50b4ab59d20c08fb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71970798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128a6daaa0cde75fb4c34c24f4e97652f08fcce31ed7367511293044aed54ee4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d7a6aa1f8fb92ae1a088f5d7cb7784b13181cbf8968cb1325a3739ec97051565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c0f0698a7f34235e3b373d7b1c241c6350b0e294e83cf9cc598871ac4d0c0e`

```dockerfile
```

-	Layers:
	-	`sha256:9b34e245b87859b9607ee17be45c3636f2fdd606f4f1d57fa67438cf44e04186`  
		Last Modified: Tue, 03 Feb 2026 02:44:53 GMT  
		Size: 4.5 MB (4514595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:419332d39e37182165d004b660ea31ab093f750dbe12f31a7b4510ba7eb8eacc`  
		Last Modified: Tue, 03 Feb 2026 02:44:53 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:af63db409bb4748b44226169453e1bf00c31cf84e9e581d68607cafc277ac3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74340554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059e7fd9544251e6bd64411b7b15c067710c0422bfa6002d67bc17e53801aa74`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a7f977a794a5fd56ece19f51541cec3b8ba447f10234ab001213bf850f92f64d`  
		Last Modified: Tue, 03 Feb 2026 01:13:34 GMT  
		Size: 49.5 MB (49468454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50ea552b26a58c13b4166d933269500891fb4897db09bc72d932372276b158f`  
		Last Modified: Tue, 03 Feb 2026 02:49:31 GMT  
		Size: 24.9 MB (24872100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a475521c52511c30c300ed83e56fd747960ea9ea2db8edd75d7f61055c63a6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4518248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acec3d688dad578a14f84818b9d6964e1f0afdde054e198ccada240912313014`

```dockerfile
```

-	Layers:
	-	`sha256:d6a8326c1f20f2195894a080d78bf52a2b907a52e58b6ba9b4cee8c8c051fe52`  
		Last Modified: Tue, 03 Feb 2026 02:49:30 GMT  
		Size: 4.5 MB (4511453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeceff45d8cac053d2b59a8c19d53efe0f3c19e684664fc550e5fd6517a12b1d`  
		Last Modified: Tue, 03 Feb 2026 02:49:30 GMT  
		Size: 6.8 KB (6795 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:700a0d81a40eab7f328b882d254e1abbe3a4d6a319daa9ad44fe516728610bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72378045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb42b3606274f54ba866bf682c4e725aa68479f07a82057fddb5ca9566419ec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 16:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b4c94e33bcdbce9a62a95be51a6e5f8ed2efc653e4be8f8f6722aa13d9d65461`  
		Last Modified: Tue, 13 Jan 2026 00:40:12 GMT  
		Size: 48.8 MB (48763393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3ebdc0d40ea56bd8ca0e23bf6a7db8ca22ab77cacf0ba126e24eb42d35c708`  
		Last Modified: Tue, 13 Jan 2026 16:17:52 GMT  
		Size: 23.6 MB (23614652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6e984defad129c8a78b4262cb42159c2f9e281150aa15b2038dcf0f1543753a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fde7f297e821ab224eaec637513c02abc29a436f2e14a99ed04be0ba579413f`

```dockerfile
```

-	Layers:
	-	`sha256:c5470282f056a988706b5b9a8c9d3aad0653e23d3dc22cb5a4a3e5a186de779a`  
		Last Modified: Tue, 13 Jan 2026 16:17:50 GMT  
		Size: 6.7 KB (6650 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:60cd2ace15854048bcea8b8d7dce6c6050a61ac2178fdc033f596989d6f6b563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77998632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35e3c08d4a980488642dbfac556bd0704d122d3dac918a3c28a9338cf0e5b30`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:22:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1311f6670d65067c1adb8d518ab8836a9d3d42058afdd776824845f91935c9`  
		Last Modified: Tue, 03 Feb 2026 05:22:25 GMT  
		Size: 25.7 MB (25671343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7243c4f1edf7dd4847ca8c3b4eda8b6dc2ca6ed954e328da89ce128b580d5c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b9f18a4d6e8ec3e2ebd5c35992b40eb6c176feb47e499d5b54debbb5225fba`

```dockerfile
```

-	Layers:
	-	`sha256:b56c04fa2553097bbd8bf48b766a006f1d18464c21923ef2135a6cec87288e8c`  
		Last Modified: Tue, 03 Feb 2026 05:22:24 GMT  
		Size: 4.5 MB (4518960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0292e20d9ba5a3186c9f9bded2bf5836dc4d49527456be0af6da05f7e2d1ab31`  
		Last Modified: Tue, 03 Feb 2026 05:22:24 GMT  
		Size: 6.8 KB (6849 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:051c6df271106c663f36f059f90f7d1fda18978fd91bb431a9c91135e25028fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71171976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fcacc610a385c3e9cc46470e493d709dc8f36d692bce3ad8e477fca012471d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3072e3eb8c224dc593a4e18a3785b06d51467102b1cd9dd426d3d31d0e6831b8`  
		Last Modified: Tue, 03 Feb 2026 03:44:33 GMT  
		Size: 24.0 MB (24033633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2429be608bcc29adcf5c17641a47ba78b0d37a9f22bc24f66651f887fb42048a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cae194b262b784f67b07d1ce638abdbbac2fd60acddf1d85e52dffda32007df`

```dockerfile
```

-	Layers:
	-	`sha256:0eb34adfff78af64648b5457a9dc47c9d3a5103970c0bd5c5a92d2b6156696ed`  
		Last Modified: Tue, 03 Feb 2026 03:44:32 GMT  
		Size: 4.5 MB (4511138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e589c51cce89fd7922fe52b471df7049b467cf36b7567887cceb12fb3d8d81f1`  
		Last Modified: Tue, 03 Feb 2026 03:44:32 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json
