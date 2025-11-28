## `debian:rc-buggy`

```console
$ docker pull debian@sha256:bdd505b3644db78a6080ec3c6ebe5d59e20a2a1c4a721d9e271a50bee9600884
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:bd647c292f17bf317711f71788bb5429f610eb5bb117853285a8a245b46eeddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48500653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf262991527178c735f648484b42d7d3be8d2d6016f83df1dab8f4a57b8c3c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 04:00:24 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:63fb544511bd02db3b85f4aa7407dbf6c6f5cd7cb1c0c1e65d055477ac245bcf`  
		Last Modified: Tue, 18 Nov 2025 02:31:43 GMT  
		Size: 48.5 MB (48500427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39137479d02eae4604494a742daaaa7d765e55daff1c13efb49e433c073cd08f`  
		Last Modified: Tue, 18 Nov 2025 04:00:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:5b375329ed8e79d29933741ac241384a44c1070de454acc38ac86c659cce1dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3135894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa87a275c9e19ee68d0c96ba8acac8f8460a6f2df95747802b3a6476c0b85c99`

```dockerfile
```

-	Layers:
	-	`sha256:5dbdc284fb83e01267733f418cd49398d218d4c1e46506238608b120ef26c7db`  
		Last Modified: Tue, 18 Nov 2025 04:29:47 GMT  
		Size: 3.1 MB (3129839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c219dd3d9357d2a680eb22d08a91513a4556e4bf15929e623e8589e97860522`  
		Last Modified: Tue, 18 Nov 2025 04:29:47 GMT  
		Size: 6.1 KB (6055 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:f8c272f97b00deea24c83bc03c688da40267882bbb80cfc6ac7e98c78e48d231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45003917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379471c89a3bd8215abe6c1655081b1489b5f75d526c68758621a7a7017bfe0f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 02:21:48 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:249f143dbba2558bd4f87316a884ba0d2b99358af5b3c63e9ac2b9640e6f9846`  
		Last Modified: Tue, 18 Nov 2025 01:12:47 GMT  
		Size: 45.0 MB (45003691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ba5749d163b7e482a505d20e10f16df1acc0de645a1c85af5ed450e68daba9`  
		Last Modified: Tue, 18 Nov 2025 02:22:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:2226ce06f203e86f83e1a2c7851a7403a880e03172a06be52a35d86072eb5c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3137334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61b86f71f46c6a4e5fb900d6ffe379a913c38cfc0dd90945c375cefc8660afd`

```dockerfile
```

-	Layers:
	-	`sha256:9f6989e2b8b4b8a4c52d96b80a272d6e026b00347450a3cf1c65b9a66fe26b8a`  
		Last Modified: Tue, 18 Nov 2025 04:29:51 GMT  
		Size: 3.1 MB (3131215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a6303694e855c4f058a16aee75d0619b7620a33b38ef78e4b9d9e031ab5d73e`  
		Last Modified: Tue, 18 Nov 2025 04:29:52 GMT  
		Size: 6.1 KB (6119 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:10ac7c94fb66d947ea7c23c518d43e91d2c73b54d04dc720d7afd2a99cb6ed10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48591610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a54e48b94be28079b4b38e5e4c8af862293f2c6e66e05c15085465effd0187`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 02:16:32 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:2b90f6fb16dc868101354a233036d6d70e13cd3477e4df5ab59f2ccc8607c1d4`  
		Last Modified: Tue, 18 Nov 2025 01:13:53 GMT  
		Size: 48.6 MB (48591389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f9299c01ffa8c15620946834b5dd254c707df040d1cadda61ee23fb3c0ee67`  
		Last Modified: Tue, 18 Nov 2025 02:16:43 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:b8eb4f652414b9164c765f5ef6c2ed3a68ffac1be1c89d21c2cddc3331a1b1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d05ef5950ad881fca6660c3e9552c7bcb637e5c1a524eb5e8a59c154af51bd4`

```dockerfile
```

-	Layers:
	-	`sha256:842256d27fb09a0e3397c021c8fcca6d1b740fea3125ce864293d8d4a68382ed`  
		Last Modified: Tue, 18 Nov 2025 04:29:57 GMT  
		Size: 3.1 MB (3130692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ee4b6c2bd44ef595f0169cf973cb9c9e789475266b214c5950cd56e7175534e`  
		Last Modified: Tue, 18 Nov 2025 04:29:58 GMT  
		Size: 6.1 KB (6136 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:2f1f3d30d6726f9fdd49d302eb699f316e7762ab973e30c0c6bcadaff2d8d8b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49833387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac66893d6c42bde87e7c8342ef92ea4862a7fa84aecea59b0da2e4bb16d51a9b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 02:14:48 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:b1df74e42eaae76d71bf2c2aa402328d711dcdb63b4080ae4e7050388c00bad0`  
		Last Modified: Tue, 18 Nov 2025 01:12:57 GMT  
		Size: 49.8 MB (49833161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0711459e1370f73d1c6fc10ffe71da63252770da3d0325d621736531a3f16c`  
		Last Modified: Tue, 18 Nov 2025 02:15:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:f2b6eb122386f1644b8964b92960708e840c647d6d0348f08f94275641e65129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7d06eb9e215a237bfa21e91c75af8689538dd6ad1971637129ab4b711b8431`

```dockerfile
```

-	Layers:
	-	`sha256:f617013d0ec074f24361090f5137bc42df4dc597a6fafe63866a6e47a77bfdbc`  
		Last Modified: Tue, 18 Nov 2025 04:30:02 GMT  
		Size: 3.1 MB (3127043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa801a36970c2d45c4eb7258e9bc158f3842125ceb2aa12582dd4e005339078`  
		Last Modified: Tue, 18 Nov 2025 04:30:02 GMT  
		Size: 6.0 KB (6034 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:441c29074bf30d6810db7a977268203e348e52be72cbfea0c397a4a77b8ff2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53335857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5522b1d5a6bf137341e381b03b198c157862d7ddaf65f19aecd3782f60ebd1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 02:14:41 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:233726152393942e1ef6b4533705d6bb3e4142964e6e486a7902cf456eab5151`  
		Last Modified: Tue, 18 Nov 2025 01:56:30 GMT  
		Size: 53.3 MB (53335631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2e2606cb7b301ad67bd7e22874b048f114344efc88ba2cd1d7072f5e4f727c`  
		Last Modified: Tue, 18 Nov 2025 02:15:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:5f4a85cbcb186919586244e1362235730b3ed79f37562eb14db52401ddb63a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3139422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be649a141ed8e4885fef64a26f7c9af96177569d0fe548319c6ddba489937469`

```dockerfile
```

-	Layers:
	-	`sha256:49d7f6b0a32c05f991735dac937b208ba3164b66666448a524e730b151eb373f`  
		Last Modified: Tue, 18 Nov 2025 04:30:06 GMT  
		Size: 3.1 MB (3133334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f112ac99954ad4bb0d72972c6a63504798ee5d06e320e2790cae212e752770dd`  
		Last Modified: Tue, 18 Nov 2025 04:30:07 GMT  
		Size: 6.1 KB (6088 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:4eac0f7736ab2d74142ee9b91d015f0fbc9585b0fa15b005449bde67219c6ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46807458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6aef134a242633797dd194190ed7efbf53adca09bdfce585088ecb58fbbb940`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 08:04:55 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:ed67ff00f4a63ed57f98b299833d8c2bd5b7627bfdca1af20fe366dfb5d9d552`  
		Last Modified: Tue, 18 Nov 2025 01:34:50 GMT  
		Size: 46.8 MB (46807232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039b576dcdb8a638b78d37531acc8c3e28cb9eadba7a7fad8d46859e848834de`  
		Last Modified: Tue, 18 Nov 2025 08:05:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:63df8c251ecc691b8d2ffc2bbf64257d67172c69693042b94ece31d3b4c8d7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd908a935fbedda77e6607186ac86b919bb90ae4dbaf1a1e31e700300a39824`

```dockerfile
```

-	Layers:
	-	`sha256:6e4ea99b795abe5c54346ee4f8bda4f58e031bf99154c96ee1fe419e267166c2`  
		Last Modified: Tue, 18 Nov 2025 10:25:58 GMT  
		Size: 3.1 MB (3122144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ea145ff3f4b3a5139220313439f8463a84b133035d4062bfbdeb1e337c51853`  
		Last Modified: Tue, 18 Nov 2025 10:25:59 GMT  
		Size: 6.1 KB (6088 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:50db247705de5ea098f72eda646ca37a6ca7da37e5a735e3f68b1b28c363992f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48370649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0dbf686f08f19945b9fff901c58d3fd4f676676028503a73fe80e576fd0c95`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 15:14:32 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:3fac6ecee4cd3dcadd720b65cbc3dc0f3dad0b4ed9c8b5d4ab2833f1e8d9ed22`  
		Last Modified: Tue, 18 Nov 2025 11:50:57 GMT  
		Size: 48.4 MB (48370424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95aa5f17292a3d7c65e10817c5a79ff2333413ccde7ba7bdd03950b9f73734a6`  
		Last Modified: Tue, 18 Nov 2025 15:14:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:69b4a020ec24f78cf5c67e55e77ccfa23c8b5771b9471d4fa80b2235b7407dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3137344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c07bbafbc0de7eebe494d0fe6f28101c1046cbe80b0c4cb29c3ddfd13dc3fd`

```dockerfile
```

-	Layers:
	-	`sha256:1519f6029cb07080f90e4aee8b8b0cb39276fb9669bf6882db301e1d826fa578`  
		Last Modified: Tue, 18 Nov 2025 16:25:44 GMT  
		Size: 3.1 MB (3131288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1afeba0e66701cf80248638704d910785dab165065d6fb064b1108630223630`  
		Last Modified: Tue, 18 Nov 2025 16:25:45 GMT  
		Size: 6.1 KB (6056 bytes)  
		MIME: application/vnd.in-toto+json
