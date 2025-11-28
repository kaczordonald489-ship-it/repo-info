## `debian:testing-backports`

```console
$ docker pull debian@sha256:f1708ba198f4638aa66662b3988ca805b62a1e16288e2f6e21bb288e8cd6d28b
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:4d67233b377c97dbc503f1e0b4762c6dad94d5589129bb753bb1762a575a9fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48500658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27015aa9e3f32168bb96173becc046fa764c0a2dfd2252df202a9864c2ffb084`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 03:57:49 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a9f04603368790b1114219c73b70b85fe6a8ccd82e5a3648b0b0ccaeb92a19a5`  
		Last Modified: Tue, 18 Nov 2025 02:33:33 GMT  
		Size: 48.5 MB (48500435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296cd40c80b1be2b2e813b205fee7cb7afb1aa951dd6ffbbb8b35b20825787b9`  
		Last Modified: Tue, 18 Nov 2025 03:58:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:34bffb298f39f2fee3c8428479f00e7bffce24d737507d05eaff4c4b831d0cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3135331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48461353737a2acb3d4c3bc31c304cbba1034a94ea68d372c7bd81086707d9e`

```dockerfile
```

-	Layers:
	-	`sha256:5a06e3c281fdd6d41dd4f5ae4b0aac9ad9b9a9e0f4d3ae6eedd5621942ecb79c`  
		Last Modified: Tue, 18 Nov 2025 04:32:13 GMT  
		Size: 3.1 MB (3129537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3634d95663ca6c1b69c55c6d5a78d998563a575e9ecf6def82c79e3c7850b45d`  
		Last Modified: Tue, 18 Nov 2025 04:32:14 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:db5fdf8ba67d08c4cbc8651997beefa028bfdaaee2492fee79d01fb896dd3c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45003985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b025a07e9f4a0183ebddc22a4c78015808bbccd2d7581ce2501ee588533ef21`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 02:20:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:33a39ef1a30f6b8cb59d8128b717055eafd7e59a223a3ad134f0261080c409c5`  
		Last Modified: Tue, 18 Nov 2025 01:14:15 GMT  
		Size: 45.0 MB (45003763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f01db803efa0cd8bc423930beed6153c2c3e5155680709a4b7a9863a0ba9cbf`  
		Last Modified: Tue, 18 Nov 2025 02:20:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d4b441958c9255d88aeb6e0f05012bea8780e4ecd324a4a10abf9162fdbebf89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfce1e9281c30d14243301733a552aff737639e313e7f18ac912d5d2f6e931ca`

```dockerfile
```

-	Layers:
	-	`sha256:080713917ec4762a34a1d034fe5b7cab67ff8afba1abb2623d9ee8c1d8348810`  
		Last Modified: Tue, 18 Nov 2025 04:32:18 GMT  
		Size: 3.1 MB (3130905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e5882b8fafc2972e01e38641910b41598bb6b2a284514cba343a9bfd2c1d75e`  
		Last Modified: Tue, 18 Nov 2025 04:32:19 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b6b2d7dad3c77f4263e2c2e298f9fbece7f0cb270470d86ae6566613df5f815c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48591407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155e6aa604301fe2aaa206bab1a008057bc635e4c9a61fef7b3596671eae8f5a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 02:16:27 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f49467d8cd4539a9c64ea7b5c2157fdb7eda1d57099abd6444b4b6f73295cf55`  
		Last Modified: Tue, 18 Nov 2025 01:14:22 GMT  
		Size: 48.6 MB (48591185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163b10a474e460b1baddc6abc01d45d038bb5c3398467528ef8dcf1c25e15e35`  
		Last Modified: Tue, 18 Nov 2025 02:16:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1fac0ddbcd6a62fab008272bc55043da267ebfa6bb6797912beb3a93740ab647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98a2b15c6ec3c15a010883d6091a5d1915709895ff643a0bb352e2c765489a0`

```dockerfile
```

-	Layers:
	-	`sha256:5bd4a1d62879cf8f88ea734066bdf3f6c601d178584dc64f862aab0fd71e2941`  
		Last Modified: Tue, 18 Nov 2025 04:32:23 GMT  
		Size: 3.1 MB (3130378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12314b085f95802c3a239574bdd2cf0c138dd83dc25d97e8dfff9c3321f95a7`  
		Last Modified: Tue, 18 Nov 2025 04:32:24 GMT  
		Size: 5.9 KB (5862 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:09ba48a6aab45a51318eab71dd701e7847ba7d278b40aa4dcce2815ad758fdd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49832460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9745d5765fc7ae82243c0d3ddfe8e030217bd004adfd11a90a318e977ba594`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 02:15:39 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1404c940473e44843d0b36ed588f649ad241384074679bfc06befc51812e1934`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 49.8 MB (49832239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b87437df145cbf84bbcb510fa2d35ae25944af5cac0e24c5789d0284b6cbf6e`  
		Last Modified: Tue, 18 Nov 2025 02:15:50 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a30791fcf045296efccc5d2981f4e6e3d540c7c7e9817ad5981ff3b3149ad473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a44c1220ff4cdd0a62bf250e4ea3c486c792622e095518e6b8ab213d835c7bb`

```dockerfile
```

-	Layers:
	-	`sha256:d5f93f707763fff4256fccd50d9efdf230b30cc9a0fd30c073cf669b0201a980`  
		Last Modified: Tue, 18 Nov 2025 04:32:27 GMT  
		Size: 3.1 MB (3126746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:423fdea617bfb3b637490330ab79f0bfb8ba8c465fffc4b0954e691e44a43c96`  
		Last Modified: Tue, 18 Nov 2025 04:32:28 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:295be79e3092feeeab461db25d78aef96d05cfe4dd003c9a94deeeb913d5d95e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53334856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89f37edc759c065cc1dd9d7c0b6ba12ebbd8b7aeb79733f8448259cba2210a5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1763337600'
# Wed, 19 Nov 2025 08:09:40 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3415dbe8c9fa5c426374b6be2cb753ee1cd73c4fc4d9120de95ac3d35fa936f1`  
		Last Modified: Wed, 19 Nov 2025 07:09:23 GMT  
		Size: 53.3 MB (53334633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85d4c881c65aa04f06c620630f6c099db2a51bd358dd9ada781e88197e6d026`  
		Last Modified: Wed, 19 Nov 2025 08:10:16 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ef3d0e0932538306298b171388221b2d465908929a0d091828c351f31849054a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b14d083166d695413852457d402c5a248b3396bf9a3cc2bb3b5b91b4e3077b`

```dockerfile
```

-	Layers:
	-	`sha256:a3773fc524abe8e0d7188668b80e3865eafbd72f5705f8cfa397faf08006c2c5`  
		Last Modified: Thu, 20 Nov 2025 00:02:08 GMT  
		Size: 3.1 MB (3133026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b54694d9946b7e0e6668045be46aa8809a6fc98583f613048485ef5fb6c8c0cb`  
		Last Modified: Thu, 20 Nov 2025 00:02:08 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:1f55c36b71e141ac8bb3de7b6b3edf0e546399731eadf4f200f2729dbaf324ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46806558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9448999da3259639bb002fc304b133cf1b9562574ccc54da22a76732d4fe2ff5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 07:58:27 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:57bd4f7d65060f5143ea57714f6e69a3a375d12220b4dc8eeb59fabbd8adf6b4`  
		Last Modified: Tue, 18 Nov 2025 01:41:39 GMT  
		Size: 46.8 MB (46806334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f77aba92446c6925147878b80c551cf5200ba268d8f65926abf20d1de006737`  
		Last Modified: Tue, 18 Nov 2025 07:59:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5e901a2c52b8d98454eff20a6dc1163daeceed564a675a8d7f125a3c265a7dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32af2e04b2ff66e7a321a20d1917720c1b15bf8491a95d3a4467ad04d913bcbb`

```dockerfile
```

-	Layers:
	-	`sha256:cad6781940f210967a7aaf44f5ac0a131f1c8767ecf560019933e4f47b9d522e`  
		Last Modified: Tue, 18 Nov 2025 10:26:40 GMT  
		Size: 3.1 MB (3121836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24894d17fd589e0c6e842c478f9ecedc0c7e823f0ab339ace60e255b15d8179e`  
		Last Modified: Tue, 18 Nov 2025 10:26:41 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:ad296c806592971f4ea15861e245699a087bd1f24bbad1f4d2a4c7f2fa0ec93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48371154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad89214ad53d60a89f7be873f8deb3133d75a17bccce7368de822715ca05b659`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 17:12:47 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:963b067f9eecc96262cd77759b1e1e10770c29e86028729532e1addf32185ef1`  
		Last Modified: Tue, 18 Nov 2025 16:21:20 GMT  
		Size: 48.4 MB (48370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725624363fc75d05347d2cff8f50eb0a33274b698d84ca7a925a78a089545e1d`  
		Last Modified: Tue, 18 Nov 2025 17:13:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e690c7667f3a0316deb777f4df690e9fd734740ecb07a4531715a72fbcd7cd10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93dc4d8921ea4ce411e46dc02866ef42b263be12fdab23cfa0580db8c68bad9`

```dockerfile
```

-	Layers:
	-	`sha256:64af50c72e111c473b7b166565f873f63b7c6a0ebcf68188c906bf07e2511b8f`  
		Last Modified: Tue, 18 Nov 2025 19:25:16 GMT  
		Size: 3.1 MB (3130986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb05a514c43f1a758b1f9475f30ce0589f11da60ae73d5f9cbefd63e072f44db`  
		Last Modified: Tue, 18 Nov 2025 19:25:17 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json
