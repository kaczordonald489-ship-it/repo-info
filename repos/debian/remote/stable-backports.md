## `debian:stable-backports`

```console
$ docker pull debian@sha256:f389657cf2ece204b2fc72ef8d01af60df79170617e9041f071e142c7df37fdb
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:6f6ad55cab781ddd0d430496575d6bb50a7e088a87a277e9b8b5bc7bb517dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49293171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b77f9b1165f0ef5c0d318989e39298efb687eeb406b770082240f6642a410af`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1769990400'
# Tue, 03 Feb 2026 02:16:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0574969c4299360b5686cb62891a11df37e4d6dde6d0930a94c889b5aa6659dd`  
		Last Modified: Tue, 03 Feb 2026 01:15:52 GMT  
		Size: 49.3 MB (49292949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467c609231da0d60bd8f0cbb246f6e2e6053dc6be58dcd7f43904705b3d8c434`  
		Last Modified: Tue, 03 Feb 2026 02:16:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:840f870a1cf566398c46b94024afde30868d3317e68da755443c4acf97a60425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c297ae05cf8e322f685983c204b2d9b07768d35ff0286c24c18d24a2b813e813`

```dockerfile
```

-	Layers:
	-	`sha256:5d41dcff2ed9ef75d8216a754833303f7e59a4860a7f8780f62790cf4420e737`  
		Last Modified: Tue, 03 Feb 2026 02:16:06 GMT  
		Size: 3.2 MB (3170877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32ebc76f50341bc055f3b20ffd69f71cfdb498e58aa7e3c90276383c90b0b686`  
		Last Modified: Tue, 03 Feb 2026 02:16:06 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8b11e6ea6309e73c98c0a7ef8397f24cd851a04dd93f803cca06671e43231eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47454224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90f5cd8fd3c45389ad7c0575c4455d1fc2d5636be9148846cb0511b5d11a061`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1769990400'
# Tue, 03 Feb 2026 02:15:36 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:128158efd6db09b3630d064b0679691b6f665efd49ef712573a53897df9d4017`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 47.5 MB (47454000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78c2937b3dc05a2ca5e1889417d3ab4950021dc3ec389c92dd023fa0eb0e922`  
		Last Modified: Tue, 03 Feb 2026 02:15:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ff31f4f3b5dfe17fdf36bfc9665683843e87d3b41dbaabaa951bda5e25c3c776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f626077d2da8bfe2d23f222377393e4d2dfc45def3238a4893a78e155bfb63`

```dockerfile
```

-	Layers:
	-	`sha256:ae2562127abc59ec1423be0875da7d63614db2334359a534cdf45af014874fcf`  
		Last Modified: Tue, 03 Feb 2026 02:15:42 GMT  
		Size: 3.2 MB (3173814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:942a70f4d10266db6d9d1e2e507d49f26e8b95718c83dcba571da1f707ce225b`  
		Last Modified: Tue, 03 Feb 2026 02:15:42 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:bc023c74cae4286162bb6fc712468a542ca390dd38599855ed64ffd0551e18f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45725187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f37f97a96d4ca6e5b31242db9c25f8743150092c49c40899d4da28ed5a6559e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1769990400'
# Tue, 03 Feb 2026 02:15:38 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2566b71ba1f63352cf667eabeded32f0b07950f18e5016891d0c5594ad672394`  
		Last Modified: Tue, 03 Feb 2026 01:14:21 GMT  
		Size: 45.7 MB (45724965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab7810977a0bb6fe9c586a2e26848324b671aac1c6aae1c6f8dfb43c2dde17`  
		Last Modified: Tue, 03 Feb 2026 02:15:44 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1f1c20021f678925cbe086f6546c3961a250ab401ab1ddffc04d945d5019e3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3012c6a19403ffbe47a3a549741628bc9146aff57ca17a953c97215c3e660d27`

```dockerfile
```

-	Layers:
	-	`sha256:889ce89350d84d2ceeb8990ab3ce32eea6ec8342d9be78a614731b19a12d2ce8`  
		Last Modified: Tue, 03 Feb 2026 02:15:44 GMT  
		Size: 3.2 MB (3172251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e50bd0ad0cbb1e2c7d207edb0ceb2e6405e5781354bc4badb5a404b48347d18d`  
		Last Modified: Tue, 03 Feb 2026 02:15:44 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:44c349fb11dedad17b20ec707104c6fe7db6cccfdf84fd47536a0f959f35acb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49652240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503cdaa861a37f9f1fcd5cd3e9b1170863943c7d853258a74b9f81a8bedf7c22`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1769990400'
# Tue, 03 Feb 2026 02:15:48 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3b9d816367de2da14a4116d32309ecd25d26f2d6ccead5f55f8a9eb119fef8e3`  
		Last Modified: Tue, 03 Feb 2026 01:16:02 GMT  
		Size: 49.7 MB (49652016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbb7f6b181d11a34996f67d296d2e07c7c519eee5fdc52bd21b06b4575dc389`  
		Last Modified: Tue, 03 Feb 2026 02:15:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b446bc72744228a7322005ea5188d3eaf13ff49ab2aa9152eac0bcb146657e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e09d6f2f06db4f13bf811d1500dafad0139bdb1eca61a8f1c2215fdea1f83e3`

```dockerfile
```

-	Layers:
	-	`sha256:214cc1e4b36cb49d954c8514e667a3e3895d98419776c9628727f65ebe16609a`  
		Last Modified: Tue, 03 Feb 2026 02:15:55 GMT  
		Size: 3.2 MB (3172358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19632e68eb9bd9dd5e64030e312c3d975545074d4342d54405a0e80226868929`  
		Last Modified: Tue, 03 Feb 2026 02:15:55 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:ebc6c03041dfd0fc00f51435b486a513784c0688a2f486f32cc0a6fc7f4ade25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50805359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d05440ff88166759d53160b8796468f075410328c57833249b27ef46cdd755`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1769990400'
# Tue, 03 Feb 2026 02:15:26 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a60034dae7e4f40cb6647e8eb4a1b1662915f79c3387891486e1215cde0a7799`  
		Last Modified: Tue, 03 Feb 2026 01:14:14 GMT  
		Size: 50.8 MB (50805135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60846766635a997e38280598f6bbb6730c3b31868e31a578ed8d1ebb77fa569`  
		Last Modified: Tue, 03 Feb 2026 02:15:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:93a4e995a6bf87857dfc66d49f44f0526c7d0a6e0bef5cffaa9baf064f1c4da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fe094f53da95bf9e854feecc17bacd2b89ec5b1df28e82c47aabce0501c15d`

```dockerfile
```

-	Layers:
	-	`sha256:0a773daffb2069d598803325ce533204b13ab0b22f6a02c617c9207bcb4a4693`  
		Last Modified: Tue, 03 Feb 2026 02:15:33 GMT  
		Size: 3.2 MB (3168079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e06b937c2cdad4bdf0ef25c50f0538176fac2ebe9fd16a5fe5c3aa77605c7d57`  
		Last Modified: Tue, 03 Feb 2026 02:15:32 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2905ed8324e496b977238cbf41a39e66da0e97894c1829ac566aabb845c58391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53112334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ec8f99eaea62c051e8719083333653d7c8bee6d0c7f754533237142a7d9c11`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1769990400'
# Tue, 03 Feb 2026 02:14:50 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5c8b380ecb87d47ac996f1a70a987e11fe441952f4f6638ad1d15d3a152bde73`  
		Last Modified: Tue, 03 Feb 2026 01:15:15 GMT  
		Size: 53.1 MB (53112111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05420295c2c61e394568c3790fdf8ad992e1eefdca9c8a1f261853d21310a4c7`  
		Last Modified: Tue, 03 Feb 2026 02:15:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:35888a1c514e6e26a084c3f5b33def9114d49264a281595309e0c054f7fb9bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15975737118299b9f6ca951f70f577e4842b7587d01059a3b3e099b05173b6d7`

```dockerfile
```

-	Layers:
	-	`sha256:e03143da0a931a2695536a373ecf36535434113f5e48632d225b4fd71fc05839`  
		Last Modified: Tue, 03 Feb 2026 02:15:04 GMT  
		Size: 3.2 MB (3174390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1651ebeb989887fa573c79273791ac6d349aa4e0612957865fe616f0b21850e`  
		Last Modified: Tue, 03 Feb 2026 02:15:03 GMT  
		Size: 5.8 KB (5808 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:514eaa12d0ce458049394705debd48274e2202b5f5b7802114cf8088788aeaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54266151e43e33c6e9c8b5128f82a24297156480b6faa52983655033fe0638da`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1768176000'
# Wed, 14 Jan 2026 04:05:26 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0930ad1b8ab3a1854b92ab0f18f171a0353703da550999d7645775e9b4a3b85e`  
		Last Modified: Tue, 13 Jan 2026 00:59:23 GMT  
		Size: 47.8 MB (47770846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c49fa9f9ed21003e5ae3b6f5935920402908267fd93de22fd363e8aa042be2`  
		Last Modified: Wed, 14 Jan 2026 04:06:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3d0f3fc7e0a90565272dd0a66a41e93449d3cfa576b12e8f0963056a15f98f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800c5f5ac912e54e07edbac90ae1a3596ea4b70ee4119ac250f01cab9da55568`

```dockerfile
```

-	Layers:
	-	`sha256:700580e410e119a76c05b45db560485e5994ca5c59cff769c721de1b93dc2dab`  
		Last Modified: Wed, 14 Jan 2026 04:06:21 GMT  
		Size: 3.2 MB (3163202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f9790b56535ebecae14e6beac52f97d9c61189ad5ca6f8ec8ccf44093c8886c`  
		Last Modified: Wed, 14 Jan 2026 04:06:21 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:48e506e44b56b3fd1f5faa69be35ca3b22190820225516ad56f73d83ccc1e6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49354600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad329ce4f0c35e00de6e12ff9952ca49dd6af99716694b9fd46fa022c86c583a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1769990400'
# Tue, 03 Feb 2026 02:15:14 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6ac2806337079959c7eae76d2dc53dca1a641ede5b263984390def1d773a1181`  
		Last Modified: Tue, 03 Feb 2026 01:13:44 GMT  
		Size: 49.4 MB (49354377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec94af45a6f29e31d3703522be516287ffe6ee0ffd5190b315f4cf191969152`  
		Last Modified: Tue, 03 Feb 2026 02:15:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:013056b19349b2b38e61a2089ce2168691af2128e37f616dccd3a8a9dd611626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1118d2120c3d2ec6c34005b1442c44f2f45f634e85e8ec54afbcdb8a72f218`

```dockerfile
```

-	Layers:
	-	`sha256:c2ed6fd9cf645676524161443be459f7d9c77d67148af65552b36ec1e7eaf338`  
		Last Modified: Tue, 03 Feb 2026 02:15:25 GMT  
		Size: 3.2 MB (3172324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ec9cd6d4556c590aa3e4eff8d372f911b588b0a182735f41f86eee61a5401e`  
		Last Modified: Tue, 03 Feb 2026 02:15:25 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
