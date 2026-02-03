## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:6a80688f0a5b731e8b5dd62acbaadea0bdf316d3f3fbc93872e4a31be29b87b7
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
$ docker pull debian@sha256:de9c4f0eecd33fa2a116d75fd4148810a5c5d9c0bcb1eb5500bd17e2b975cbed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48481713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e790aa65146ec560dd27dbd4b469218063e5c07fcfb5423f98e6f23384fd02`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1769990400'
# Tue, 03 Feb 2026 02:15:59 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:df15f195ee0d72d279cc46eb774ad62d104e474d9facef01b531175464baf2e4`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 48.5 MB (48481489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdf7eac074414506d83e54d6b565929f710cd5bfbf92fe4ae3c864887591f24`  
		Last Modified: Tue, 03 Feb 2026 02:16:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ced732ecccaaf892a0ac51c6fa9b9a364bcbf4550587f168ee30223ecaada939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3aa0bdde514b21d35ba8bf377c36c22e7e52bb7c152bfc0db08a337001387c`

```dockerfile
```

-	Layers:
	-	`sha256:3bed4c5ab203889178224d21351dc66d9abbbf1fba19684b172a4c71832cb0ca`  
		Last Modified: Tue, 03 Feb 2026 02:16:06 GMT  
		Size: 3.7 MB (3734076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ffa892f2f290f12dbc09283554ce5b1398ba6c9d49be2d87d8a347444536d00`  
		Last Modified: Tue, 03 Feb 2026 02:16:06 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:9fa251c744a2d644485404a514a67f9b06a943dadd217ec93993d0185cc08abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46016892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1ead86511898834166c950562d66f7c22a315e90436b9f508bcfb8fa8e727b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1769990400'
# Tue, 03 Feb 2026 02:14:55 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6b8d9d8da429c22ece8e9db14e33c70ba99ef6b87849675c5402b6b3162de82b`  
		Last Modified: Tue, 03 Feb 2026 01:13:53 GMT  
		Size: 46.0 MB (46016666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f4ea4ae4dc25fd01129caf44a86163a5b6181fc8e3fd63d63772a9cf536252`  
		Last Modified: Tue, 03 Feb 2026 02:15:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2f0d0498da433edc0bccf70cda525837e7cfd421b506affccf916049828475b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef107ed0beb268cfba72061254fedc7f1288bc13ddd389c7b36b2cf8c98985d`

```dockerfile
```

-	Layers:
	-	`sha256:108a50f7ea40809be831fc9cd887c1995c682232dc41e14ea838e7bc71dc4e86`  
		Last Modified: Tue, 03 Feb 2026 02:15:02 GMT  
		Size: 3.7 MB (3734277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f7ef8f4d55427b036dbfb0f3a695d3c3ed355b1278753f5f6e3a8c569fe096d`  
		Last Modified: Tue, 03 Feb 2026 02:15:02 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a3dc936c48f573312413f141b81128ff69db3e4a2b59b9430d3b363e963184ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44198963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d828d00dabe5b2c57a6381af32a1decf286244bc1d13bb53e5f24e3992f56796`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1769990400'
# Tue, 03 Feb 2026 02:15:46 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ee365600080a10925f64bab0b0422827bd7e9b6faccb23d8019e6b59ef633e08`  
		Last Modified: Tue, 03 Feb 2026 01:14:27 GMT  
		Size: 44.2 MB (44198737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7311528353ffcfe744a9aa58346ab0c49685957ec15b831091ba06e8a7f817`  
		Last Modified: Tue, 03 Feb 2026 02:15:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:23ebe5bdc8ba6d024b67241de28af44f5746796f7353bdf8daf7d4822cc5471f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908eac8f516ade7c9fc154478e31724d490dea52058eec95fa203df626c00b8a`

```dockerfile
```

-	Layers:
	-	`sha256:4562ac18656f7f693b649629e7d4be8525f26bca629fd17b46932e3530718138`  
		Last Modified: Tue, 03 Feb 2026 02:15:53 GMT  
		Size: 3.7 MB (3736255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16b531e431cd0f80338c8c5460fdc32b6481e01f42c5d9254ed5c44b63ab7e2d`  
		Last Modified: Tue, 03 Feb 2026 02:15:53 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8535dc668100b7620c4acd35c1069ca0cbe0ff6fa189317db0d19f4ca2103802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48366184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb5f267150c795a44a5f67391a1b82989be1e5dd292d2aa4f83da3f46082d5b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1769990400'
# Tue, 03 Feb 2026 02:15:45 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f085c6c6f1487d07d5c642ce2b048ca170755501a3bbf66dc721ce8c274861b7`  
		Last Modified: Tue, 03 Feb 2026 01:15:51 GMT  
		Size: 48.4 MB (48365960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c6c20cc2e35f1effe95818d9fc82cca5a878ddf66c4e9a78905a9d777c980`  
		Last Modified: Tue, 03 Feb 2026 02:15:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e08639e6412db8b3ae436dd7ea8cf09e16d74fc09aff9642c4c04d0326292f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20f097f466d4c4f5d7298fba4ea07dcc7916e2964143af1cee4827016e11a44`

```dockerfile
```

-	Layers:
	-	`sha256:4841d106f6671377bd830a2337b47ac822776f4a905473c6302745723a91d417`  
		Last Modified: Tue, 03 Feb 2026 02:15:52 GMT  
		Size: 3.7 MB (3734291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79e211ee68becda6fa6b89603aba9f54ec182c16872ca81d765aa4f786bba09`  
		Last Modified: Tue, 03 Feb 2026 02:15:52 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:eae414a36627b5ca0e2d17eeb97c1ac2badc4118cc54a2452719bcbb84e23081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49468681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdc2431f710109d2c1c8b53ce18d8e8b99c8b70b9480a08b1cae4db2af50af1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1769990400'
# Tue, 03 Feb 2026 02:16:05 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7583b5221701df42e113bac4a5c496a6d0451c0ab5b1bbe29fca1e1b873df3c3`  
		Last Modified: Tue, 03 Feb 2026 01:14:35 GMT  
		Size: 49.5 MB (49468456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0382fd0902b8f85631e49d9e30d38c0c5c9d237f1183a8bc2f0df41a05ad06ad`  
		Last Modified: Tue, 03 Feb 2026 02:16:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6f1c0e0fcea33390b017d53e6f7fcd85b9d2687d9442d6a41c355d282a82ae60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f65303698b46778b002fdfebdcbc89f00cef434565e79b8726dad7cd8976d16`

```dockerfile
```

-	Layers:
	-	`sha256:99246b6506eada4442ff4dd50c77ed89f3c928e4923b6444d99e3743aaa85444`  
		Last Modified: Tue, 03 Feb 2026 02:16:12 GMT  
		Size: 3.7 MB (3731272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3a0b49bf0349df9d7041865f3e4dfdf3f0ae8b63c975a338e34f94153ae9cc8`  
		Last Modified: Tue, 03 Feb 2026 02:16:11 GMT  
		Size: 5.8 KB (5793 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:ac18cf7a35c623486745ed01888534ee9e66451ea2e4835b5aefa3c3c9f9d24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48763485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581a5ad84a200abcba403af47e338d0a3c5f83db29bf9891036ebd301eea3850`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1769990400'
# Tue, 03 Feb 2026 02:16:15 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:35c59722c959fd9d60a7dfb5956b0e344c5d40af352101814fa06b50da5b1f7c`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 48.8 MB (48763261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6233612c79facabd1d044bbe97739b953353205a79dd6ae3ba1e88511c30cc9`  
		Last Modified: Tue, 03 Feb 2026 02:16:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c789cba0dee6477af4c5eab6636256a9ae2021d67ea8d7cbf4136e04c5f999dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435e03eb2814cf8fee6168dead4d84c3addaab6fd0ddd3ab0ddb89b5ca1e89eb`

```dockerfile
```

-	Layers:
	-	`sha256:42345c0ee9a00209568d8f1ef34dd77884cf5f90cd43ffe4aff86641a0a18b8d`  
		Last Modified: Tue, 03 Feb 2026 02:16:33 GMT  
		Size: 5.6 KB (5633 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:082705accb72b45b6ef7ea9c6f1535463ea74fbb086e892ee657bcb8746c7b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78715193065dee45fe1f07c694c802cc298070aa64edda1467516f7ac252d760`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1769990400'
# Tue, 03 Feb 2026 02:14:48 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fa322c9888557dceee3004049315081e51d7742c7dcbe992cf4823c89612553a`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 52.3 MB (52327290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784df06bfd2f6fe56d97682505082deecae85beaf6a58bb9b9b7f16f80494022`  
		Last Modified: Tue, 03 Feb 2026 02:15:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:94b688a5b3eadd169111c2cab1affe0853e18306d4f0eec704772b1eff28e6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7234ce1e1b0a4198480a139afa579b59edd8358c36b6f090ec35c0dbc6b266ae`

```dockerfile
```

-	Layers:
	-	`sha256:abab25158618602644a443a43da1e180c35654dc617f57862f6c366b2182bd8b`  
		Last Modified: Tue, 03 Feb 2026 02:15:03 GMT  
		Size: 3.7 MB (3738434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52cf2dd993fe5d240de6008c7f3e3917c12532a899539beeba95ffe30c759d27`  
		Last Modified: Tue, 03 Feb 2026 02:15:02 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:bc48c7f51ce3c9c168145343aa7e0a4f6f593f6d0016a150a6c752eab11b8236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47138571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8ebaf149a744e86c9c29bafc63048fe8828b485ab89a9513d4ac457d26ddb0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1769990400'
# Tue, 03 Feb 2026 02:15:19 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a59a0aca3d5f7f5181deb3b3393bd059b96d8154e5eecb729404a2a46d13ec67`  
		Last Modified: Tue, 03 Feb 2026 01:13:16 GMT  
		Size: 47.1 MB (47138347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce9eb69440571fb6cac45ffd72db23b62b40b36598a2ebb35508e75ab2e5d3`  
		Last Modified: Tue, 03 Feb 2026 02:15:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a8906e7fa3d75195952d0452fb5c24be6003f863b62ddab9b0542370b4fb7ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d314b9e32e47099dd4e68a2c290d17e48e2570bc3a57dc0f69a7117db22040a3`

```dockerfile
```

-	Layers:
	-	`sha256:99c88ea01725bf98c383381431a51110cc39029b0cd0575c0c52c7004b28fff0`  
		Last Modified: Tue, 03 Feb 2026 02:15:29 GMT  
		Size: 3.7 MB (3730914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc83c3edf286707ea7a570ce42da67d43fb56416fcd2b7535bb39ee1d3e295e`  
		Last Modified: Tue, 03 Feb 2026 02:15:29 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json
