## `debian:trixie-backports`

```console
$ docker pull debian@sha256:8fb5f156c57361a9ab6208140873957ff61ad85dd18c190afd4f7f0c799447f8
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:c8f2b5eb071968ad7f86f52052966587a659bf14ffd8aa1f3e1bb52505dbad1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49293176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71220c88179cea7aee801f9ef8d75371b0143ab796c255cb90efd659de5c4343`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:16:08 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0190c28b9e941691d0b19e5f5f2812ac2421a1a2639cd384a0bed04209415b`  
		Last Modified: Tue, 03 Feb 2026 02:16:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:90984fec8136babc6267198499306aa18b46c44bb7b88eaa53465665e3a57e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3a212b368748b57e1cfc3c92bc2ade61bf79cc29668fa3a805400b607fb241`

```dockerfile
```

-	Layers:
	-	`sha256:f195dfcb8559825aef49118e7a673193ff1c8912a2615584078c9ace7b85843e`  
		Last Modified: Tue, 03 Feb 2026 02:16:14 GMT  
		Size: 3.2 MB (3170877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13fff96955d7c25dd331c49acbe92735381ba056dc4bdb2a52573ca865b5dc1b`  
		Last Modified: Tue, 03 Feb 2026 02:16:14 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8143c0b9240ae9be8adfbdeb9bcda0777dddfabf5bb4f1e3be94861d136353ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47454221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8108e1568c105d0599320fa5206cafae09e0b2efa3cac3b8bfb9922baf35730`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:52 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ba31dc65cf53cae37b5517f251f4d408e91109de491cbd8816a9f21c33a05203`  
		Last Modified: Tue, 03 Feb 2026 01:14:09 GMT  
		Size: 47.5 MB (47453997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f4cc758b75dad698d8ff526648bda8d62ff994372b8ffb4aa67db5ce2c1032`  
		Last Modified: Tue, 03 Feb 2026 02:15:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1e22fd3ba83f7cc23d58ef2e3b6dd400cb80cb59c6af3f99a8a82b35472cb812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3005ca20e93ab1c240a7680aa396ebbb16263483931fa6ed961bfcd384f1634b`

```dockerfile
```

-	Layers:
	-	`sha256:c76e9bea7f72ec250e28118d8f981fc5039765e2fa0b46b607ece21804c2823a`  
		Last Modified: Tue, 03 Feb 2026 02:15:59 GMT  
		Size: 3.2 MB (3173814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c326ecd32654d1a6e005ae31ee26448c6e7732d509a0cf5257df0193978b6d8`  
		Last Modified: Tue, 03 Feb 2026 02:15:58 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e0c0e854afee379ae6e09e1c6c5a9630a076080603e844c3bc2ed86e76b9350a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45725191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fafb59a76f13724cbec99529cae3d577536c59503d743a07da33380243b03d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:54 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e712004ad7e72ac7b512e7e067d08c1f627b7b81a230302cbad4864b08acbdff`  
		Last Modified: Tue, 03 Feb 2026 01:14:45 GMT  
		Size: 45.7 MB (45724966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecf3b9cb4820be535119578368377553e8da908fa9282e39f4ae98a45174713`  
		Last Modified: Tue, 03 Feb 2026 02:16:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a8201724224f650995bb63b57048e1b86c85eed1969f9969ca2ab79db44efa1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a752a7ea787942fd1ecb78f662fbec68efaf14afdbf17947e638a306da1305c9`

```dockerfile
```

-	Layers:
	-	`sha256:999bb0224fc4c98392d2fabde741a8bee3f0649daa54b35ed15a997236fbc0a3`  
		Last Modified: Tue, 03 Feb 2026 02:16:01 GMT  
		Size: 3.2 MB (3172251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:646dd9cd4b2b55b804a7e5b81add57fd6749fc8532a114f8ecec0473fca10714`  
		Last Modified: Tue, 03 Feb 2026 02:16:00 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:2d2a4a63795f5fd3dd6dd528bff7829aa1c8a5c1b7aa253a2e57d27cbf369bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49652242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da65e49591bdd3076346dff462b22b3b559cf42eaf2cbaef2fcdeefe6020659d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:16:05 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3afce3997a6e75772643323220f10e59a939ffb301b25ffa1e515728c7fe88a9`  
		Last Modified: Tue, 03 Feb 2026 02:16:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e0625d558f0f08969eba872ec51b893228f4044e22d62b1364aa060ccf20adfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a693881403803172793c7dd874c288e856f0b1a1825bd405c9f2653be30ededf`

```dockerfile
```

-	Layers:
	-	`sha256:d5014eec612d26e3b71bde06e3c6f7fcf3f1c1ed326b8174244e4218d38384d6`  
		Last Modified: Tue, 03 Feb 2026 02:16:12 GMT  
		Size: 3.2 MB (3172358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dc668e2e490b5005cd0c8b26fd12d553394bf610ca7a9ae4b5a35d032c7e58c`  
		Last Modified: Tue, 03 Feb 2026 02:16:12 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:d79db31cb384d7f58265abd185c0858509d841ee75302bb40e55d777b0b57c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50805359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299eaf9389ce7e3aa9fde5411274642b634321d3781a391e57e96cd93ae78f31`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:16:25 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b536877d3c0a030ad79a6593cd07fd6d9d694a4ee908632c85159f47caa880c2`  
		Last Modified: Tue, 03 Feb 2026 01:15:09 GMT  
		Size: 50.8 MB (50805135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494e9b9c666eca6ffacbdf547233f24fd7af4a46b478a81949a56ee59dad6da6`  
		Last Modified: Tue, 03 Feb 2026 02:16:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:155d94591e7aa559af0b4a7213d89535b226ebbccead84ef511361db95baed19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d1c6de94cb17a6c882ce4fd968e4dff458cc63a9cfdc7f99040444c988062d`

```dockerfile
```

-	Layers:
	-	`sha256:c7f5268e2c518429962ea76ec46d95022b9d956a3d817bdbceb99f9224033ddd`  
		Last Modified: Tue, 03 Feb 2026 02:16:32 GMT  
		Size: 3.2 MB (3168079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c734928be54f6d73c38f59e7ae35ae13363f1ab02a7d302985f812c16e35737`  
		Last Modified: Tue, 03 Feb 2026 02:16:32 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a5446515087a8af0ef49eb8d8a352edca2dd9f5950963f3dabb90b5c80c3b564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53112340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299f7d10c9fa893da13dae709afa1cff5c4bc0078298c7e8066cfe33460c9a5a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:22 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ba2d005d228b6e5baa8cf039e948417198fc943600b9c36c46538f422a505`  
		Last Modified: Tue, 03 Feb 2026 02:15:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0b86c7c5020df3b2610c27a23da05a2d2dde73b0c482521b6742f63f543488c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6902a8b037483ffcb0e50808df560cec23e56c7debdc9bcf0b8fdc6eabfc6ec`

```dockerfile
```

-	Layers:
	-	`sha256:bf484b22e26c5da244215a70471bee2fdbb0ad7ba2edf456195c00aad5ea1ecf`  
		Last Modified: Tue, 03 Feb 2026 02:15:35 GMT  
		Size: 3.2 MB (3174390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f0470da5e993c6eddc143c42e2a7e14887062b411a543bce6b065cbd2fa358c`  
		Last Modified: Tue, 03 Feb 2026 02:15:35 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:e3c507c476dc21fa48706fecf0509666929fdedad797f77387adba595a541286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fdc07dd72781394805910843d78b196c5f5bfa3a7bcf9f2e2fa42178461cbe5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 04:09:24 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:14 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71d02f0dc09f1e2ea78ca7e76a13a5438a033af0e825c9cc572062d365d58ee`  
		Last Modified: Wed, 14 Jan 2026 04:10:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:94e24be6c811c9716c4e5d1d27895cd8647a0c468d68f7d377e985f5b1915d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44c01bd87fff2359cf88f9b175598a719b91e45f06ee6bbfe868cfc60696a9e`

```dockerfile
```

-	Layers:
	-	`sha256:9bcf00fdac5abce660dcc7a5680b3077c909c245e57f3089d288417828a4e812`  
		Last Modified: Wed, 14 Jan 2026 04:10:19 GMT  
		Size: 3.2 MB (3163202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1733f600103c0a065ac2373b7e7a546c0b57f51c76466b4f1ce323ef66deafdd`  
		Last Modified: Wed, 14 Jan 2026 04:10:19 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:bf03821004c54071af0406c3a806a56b014719e3d907959119d1098db2611a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49354603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6b7829e7f337963cffdfaa89651be7b576ad536a5b0269ad7a169d3f421c27`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:45 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae09594acaa53f8dd35d9ebbf603935bdff0d0b5001c8d06409aeefdfc3e8649`  
		Last Modified: Tue, 03 Feb 2026 02:15:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:451f89f04445b11afc29a084645363933bcfc90d0c94d1abe1defaece499ab77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f26d0fcdb1313eef0203c78758806f525f7dabbaa867c466080b8027b45983`

```dockerfile
```

-	Layers:
	-	`sha256:bfe96903ba1f0a4b0681e81cb413f00675a34d257b4d4e957d521cfa20d1af15`  
		Last Modified: Tue, 03 Feb 2026 02:15:54 GMT  
		Size: 3.2 MB (3172324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9109c13534a81b2cf08edcf0f69241b4e6f88df34997daef772cd8e03d23fee`  
		Last Modified: Tue, 03 Feb 2026 02:15:54 GMT  
		Size: 5.8 KB (5783 bytes)  
		MIME: application/vnd.in-toto+json
