## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:7e572bc4b8567beba626f884df37bae678c198d3b7a3ea6fca9ddc59829e9952
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
$ docker pull debian@sha256:0671c7810d136ce7a35c841cf7d4c9e2766a5dc676c056f2877298352df37b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48481709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c8fab7a29d032c9769d3d6ae26998aceada8e0b96526b6f95730cdbf0628db`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:15:15 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb1c12abcb72ede9ea401710a4c1f6426cc4b0761b4fe7eb4cf0bfbb6302824`  
		Last Modified: Tue, 03 Feb 2026 02:15:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:cd827e16e0f95eed0718a6724626e4ea54cc523cc11fe1ef5df025feaeac0cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b96d28b92fdf75d0a866364bb3aa213987009a571db2f4a5152351e12749b09`

```dockerfile
```

-	Layers:
	-	`sha256:cbf8a36352da951e4fad4a03766073018cbff8aea7d7380bd583c876abb3bb4e`  
		Last Modified: Tue, 03 Feb 2026 02:15:23 GMT  
		Size: 3.7 MB (3734074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6919f851cb6b5617463514eb7521cc9b600b75148b79e9e216d97952e005dd1e`  
		Last Modified: Tue, 03 Feb 2026 02:15:22 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:3078b6f4aeccd4a9b399be93d91aaea6e8c91c9c37ca1dac73a47a61b23bd1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46016890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9d87be55e3dd8cbfa90d31d8aeba96bc73a6b3f5b351fcc702ac0ca6cfdaff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:14:58 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:48989bca0bd1f08c49cfd2a8eae58c5ffcacc0f005e701953d88f28a5e398ee1`  
		Last Modified: Tue, 03 Feb 2026 01:13:21 GMT  
		Size: 46.0 MB (46016664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b354fa238de1d49fce8eed795b91e211a89ed3fe7daba979b8de1b5b17e8274`  
		Last Modified: Tue, 03 Feb 2026 02:15:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ad4b5d1f7c688aaf4c5fd803a1ff76b3ea48450fe44328b517184c2f160da029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c351951edf24606d0bcf0329474e9767df9c6b6cc3eb3e28e29c93733e2e43c`

```dockerfile
```

-	Layers:
	-	`sha256:63d67c2b3eabce85e4cbb64ee3f7d472ab4e820e3765c964fe8f3c6f3136f28c`  
		Last Modified: Tue, 03 Feb 2026 02:15:05 GMT  
		Size: 3.7 MB (3734275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074dd2d10c61dbdf254117f1ad62d8cb5107ea66a4674a4b2ff54175b00b7003`  
		Last Modified: Tue, 03 Feb 2026 02:15:04 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:35bc203fcc08a232427483607064f909f8494199d9d09b1c401c1dec40a21368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44199070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2cc8b7d0e071ee01587601d02a73f58c03f16c56b67fed29869728a5dc2a28`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:17:30 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac5d530195f102fee7fdef0edb5d3b439a9285d966c2f2c4200c53952bbeb25`  
		Last Modified: Tue, 13 Jan 2026 01:17:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5ef928fca366eb54bbec65fa561f6860287442d04ec1dc69011f40e5f41c1f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a51eb7981323751b0e504a6bb4bd592782874f63761a0f31d56bc237a52b2e`

```dockerfile
```

-	Layers:
	-	`sha256:af5140998cba43cd8a35667fdf88267e6870a2cad9b71302a9f0dc348d7be3c7`  
		Last Modified: Tue, 13 Jan 2026 01:17:37 GMT  
		Size: 3.7 MB (3736253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:758bac7b2921efcda0ee3e8d97fcc4f41a11c504c8a895a74b010d165ff2d59d`  
		Last Modified: Tue, 13 Jan 2026 01:17:37 GMT  
		Size: 5.9 KB (5859 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e6af6650c385d37a6e21cf8b450f5ba80bfb0a2ee278a23518a440ed200fd2d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48366183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71780d0c2c58aa76f9f37bc843e665e42a77e3e4ce9aee156c222b7b58c40a83`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:14:55 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3597965ddf3ef59835cacdcc98832c75cb5c029c724138050f0957050a138334`  
		Last Modified: Tue, 03 Feb 2026 02:15:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9d5358765b11d21203760097d7f1f970b63cea9fd2641783083c6ac71377f588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcd6e3ed9279640f290498ae5ec3624a8a95d56d412aca79428da4a7dfdf587`

```dockerfile
```

-	Layers:
	-	`sha256:84780cc3b98f6be3d51840ce9595e2524f5670fa13e76f2d7756918e0948c77c`  
		Last Modified: Tue, 03 Feb 2026 02:15:02 GMT  
		Size: 3.7 MB (3734289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bea8d99d6cf9b6057dae46c0b06b130ed7db7ad84ae5d99f1474aa202ad492b`  
		Last Modified: Tue, 03 Feb 2026 02:15:02 GMT  
		Size: 5.9 KB (5872 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:6fcdd7245a658c6190b4e71fa5e142e1c0f88bfea7e8326ca985ed33e08b1f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49468678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b72d41ae39d9e6dbde69fb0bb09d533882c1807a024129fd7fced1b8559d95`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:15:09 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a7f977a794a5fd56ece19f51541cec3b8ba447f10234ab001213bf850f92f64d`  
		Last Modified: Tue, 03 Feb 2026 01:13:34 GMT  
		Size: 49.5 MB (49468454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f96a618d943fea693e51308974d18c0ae7a3a83e962b60b0550f5b601d04417`  
		Last Modified: Tue, 03 Feb 2026 02:15:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:235659d9998bcfc8638b6a323d73585a9fb73f4a614eb7348ab3c2f10b01982b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed9f5746deb87c934cb9a0c9c7a465d6a9461656eeba7462ddc14395aa53a2a`

```dockerfile
```

-	Layers:
	-	`sha256:3bea0f7649cad2c01916e60716247272f9414267ff0582e5895a7a48230401f6`  
		Last Modified: Tue, 03 Feb 2026 02:15:17 GMT  
		Size: 3.7 MB (3731270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eb03f792b6cef2e46cf3298b46e67f88ee956278712cbafd210a334c98f906d`  
		Last Modified: Tue, 03 Feb 2026 02:15:16 GMT  
		Size: 5.8 KB (5787 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:0c103808d2301a5a89e6b39b68555f28dcf5c5cc0762e2a550edb637e63a4ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48763483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3637643b372d3a94b8788c86599f2bfbf374777be7cc686da501717c6d4b7175`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:15:03 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:001d31ce76be3df3174382025b0b9e2985ddc96d785143497e14a46cdcdcf951`  
		Last Modified: Tue, 03 Feb 2026 01:12:32 GMT  
		Size: 48.8 MB (48763257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20129f18c108304653aa74b14d24c6bd25a13d173b3704b42df6b962d4f656be`  
		Last Modified: Tue, 03 Feb 2026 02:15:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:083f92205128e675c4efb254cd5f7c8d03f4b67cd562ef0565e1ee685bf11a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3a9410390502b4edef2069dc8fe70c78802534718153e80ff550ee7d25e860`

```dockerfile
```

-	Layers:
	-	`sha256:48d1d10402974730979e555350a178cb0a67fcc34591faa1f9a92e6e723b227f`  
		Last Modified: Tue, 03 Feb 2026 02:15:20 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:071d2d3a88c43a1ae4fec0ddb1f5ec26d83d4c92ec583810c433a13d60f4887e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1565aa8602ea89cbabd53dbc5e6434cb0f9e2defca7a736019cda99314f0ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:14:18 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a528c6a97a5963dae4c114685d71af00cb7ac5ab50fcb9ae9700e78f8c835deb`  
		Last Modified: Tue, 03 Feb 2026 02:14:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:edaa1b442a3e7a4cba102a0b8d9f226f2c0dbdca293f921f183fa71bf4096c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60c34f7212bb84fdc9780eacc00cd82c71240361558d45c3f0aa71bcd183aca`

```dockerfile
```

-	Layers:
	-	`sha256:2c6cd4c62d1b54ae4715fa912f9bc7ec5e4b42210de55bbd70781287c6348ab7`  
		Last Modified: Tue, 03 Feb 2026 02:14:31 GMT  
		Size: 3.7 MB (3738432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e814b1ffb65c732b04902d2690ab1970ca9f911011250650f0b1bf68da59eb4b`  
		Last Modified: Tue, 03 Feb 2026 02:14:31 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:8694b15f5c97d72d1d980e30f7683791c76d18de14f925cc95ee0eb182752242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47138569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c788e8d73f5d1f097994143bfcded714a7f13ab23a83726ff5b8c5096a42f84`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:15:14 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb1c12abcb72ede9ea401710a4c1f6426cc4b0761b4fe7eb4cf0bfbb6302824`  
		Last Modified: Tue, 03 Feb 2026 02:15:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f7dfeeb66f10fde693499cf602a2753998cebeb2780b83333281ec25a41a4cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e83dfc30e70720b4895b11e259d750b6b41e8e52642550e09e6c50d2d2067c`

```dockerfile
```

-	Layers:
	-	`sha256:c708da8dad9ac1b0b59b60324eb825230ef575f7c89ffa6d304f03d9b00e4164`  
		Last Modified: Tue, 03 Feb 2026 02:15:25 GMT  
		Size: 3.7 MB (3730912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97035bc32d6b741afafc577438804a33ebc6e41cf19c8ff8e3956cec32df66b8`  
		Last Modified: Tue, 03 Feb 2026 02:15:25 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json
