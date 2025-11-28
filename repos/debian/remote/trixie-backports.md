## `debian:trixie-backports`

```console
$ docker pull debian@sha256:1310b9ad530d8a0a9a15a4174b1438a24e063d496649b063da10b801c2e84049
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
$ docker pull debian@sha256:1d5f6ba47880ae7235e499d0c5531acebff114a1a5ff499087ffcfa7a95780fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49289770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce57dcac51b348761d24f6d8c64a7f59284884f1d5ed57f303aa3b3c0c7d4df4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:58:50 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8792a6987c19b8753356281a73de387f3b1da7c09b30f3a8c5424942926e03e`  
		Last Modified: Tue, 18 Nov 2025 03:59:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8956ea3d399a77ec6e31b9c55d38cfb94eb4772a5beddd3a2b99a0a0a8124ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a8e06312d3822a57f8aae7e6e17b438752f348fe0875ab2214c9d6b12207ca`

```dockerfile
```

-	Layers:
	-	`sha256:13650d3f872636af118633e150cc15399a8cd21cf34ad035841732ebcc6c3f8b`  
		Last Modified: Tue, 18 Nov 2025 04:32:44 GMT  
		Size: 3.2 MB (3170018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df755bbd1bbce6322e546d889bff55313a5ce2f2ec98d112731748435d5da5dd`  
		Last Modified: Tue, 18 Nov 2025 04:32:45 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:e0ef55361800255ff6bf1dfcd582979aec7638b5e357faab1de8b178b6386fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47448980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6012a41b9e0401bc1774a5418cbe5087d0769b783e43cd1b1a8e42e04e5d0c45`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:04 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d5c9e476f1b8d1f67ce6ab99ac45c57bfe3b7cbada7b61c1dbd969f0656bfff9`  
		Last Modified: Tue, 18 Nov 2025 01:14:11 GMT  
		Size: 47.4 MB (47448757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa61168e90d0a4811c75e14c9e803e9c87f0fc4f9f6e5d7dcfa3f1c812368dd1`  
		Last Modified: Tue, 18 Nov 2025 02:19:16 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e2cfed693d2986f7bd657c525191a9aa5cf2650e43cc6351343a40fcfbaca5d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d035be222331c7c91731dc80d98cf4820ef046c9fe632b1a3458f5def449a9df`

```dockerfile
```

-	Layers:
	-	`sha256:f60ba0274380b65ba060c24a7f27318425c67dc4450d85e7aee37588faf65e78`  
		Last Modified: Tue, 18 Nov 2025 04:32:49 GMT  
		Size: 3.2 MB (3172955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dacfa53357869e00691a39695211cb675f79a8b65a03873144e65b7d838a0e8`  
		Last Modified: Tue, 18 Nov 2025 04:32:50 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:edd447e958425b17abff4f570294536f267576d02b2ef71f2057707a4580b2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45718502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f96461df4367d287f0336dd3bc3f50cb7f6a139927115f313d409a3125ad8c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:20:46 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7fcec123a6a2e24d64f8dd8d3ff01f16ba0839656e71d971698d0e8151a28a21`  
		Last Modified: Tue, 18 Nov 2025 01:14:26 GMT  
		Size: 45.7 MB (45718279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e62d2242f92673db6c13f5e379c742c2524798b59fcbf66caa1ec173049a3a6`  
		Last Modified: Tue, 18 Nov 2025 02:21:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9f5f8ee2e0493e479dd236dc53fd3405b96b61cbbe6c97ed5c22f03a01a489c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0018d02ff80fb24299320d5d982cec258ade783046fc8893b4596af2c58fdaf`

```dockerfile
```

-	Layers:
	-	`sha256:85aaaadebbe90a6e2a6871bbfdea0a70abb95e3d71524151e4d71fb393f42282`  
		Last Modified: Tue, 18 Nov 2025 04:32:56 GMT  
		Size: 3.2 MB (3171392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b1de4af75f3bcbf6849e01f805384875704c24207f8b743172a74e9c9a8aaad`  
		Last Modified: Tue, 18 Nov 2025 04:32:57 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:34bc623d3ec14ce63dc4f47ed26d74450af39f992c8420f6aa4bd8cb7be24587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49650456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4704ecaa8214750f95a86ebcb0e2a4af2cf9867c51a619e9661bd66b9bc45f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:52 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f696b366d11a19d530a657760f592f663b623870a69a75bdcf531591f1b049`  
		Last Modified: Tue, 18 Nov 2025 02:17:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0a7a86080f63e014763d7b6f4c6268b287060a01f276c0d6710ce3aa521eeb2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5597f10dcce2b0b35b9eae3fbba7d31ea11364c48db9684113c054c885458045`

```dockerfile
```

-	Layers:
	-	`sha256:4f8a3aba4bbdb098e543539f8ab823cf904f60cb6050bbf437df91b4ccd8f05f`  
		Last Modified: Tue, 18 Nov 2025 04:33:01 GMT  
		Size: 3.2 MB (3171499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba966c2641d57c316f9a217beb95d3b3f96eb518d8e4598db1f7431b5399f554`  
		Last Modified: Tue, 18 Nov 2025 04:33:02 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:8bc5825c89e534a192ecb8ed84150820a09ed934eda33850acd92ed688ed25a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50801968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed175a06e9cb5b5c58570a7656b4f4a5c10d2d425bbde912bdd0b7c74cbbc86b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:15:25 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bf2a49c122745d1757b9ecb1c9b1d8252491e66b62d1c279080155aaa530a615`  
		Last Modified: Tue, 18 Nov 2025 01:13:10 GMT  
		Size: 50.8 MB (50801744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce74e8574488e8a881d67fbc9951ab79544aade5823822ca370a0ee4b49802d`  
		Last Modified: Tue, 18 Nov 2025 02:15:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b5aca43790fe219d51dba7f00b9d498f7f18102fada588b22e59a12c7684b37e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921f8535719193fbf6c1ef20272c46af413897f87f6673b6b14e566c9af8d4ea`

```dockerfile
```

-	Layers:
	-	`sha256:1f2c3c4330a481546967aa596bb7568d289228a5607d6e9368e3850d62139241`  
		Last Modified: Tue, 18 Nov 2025 04:33:06 GMT  
		Size: 3.2 MB (3167221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0884d92f8f36a3f886653e5a795698bed2363b55b7d4ba3502ea51ba6e41150a`  
		Last Modified: Tue, 18 Nov 2025 04:33:07 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:5698da772c88f0b415e0e73c1918e12f76eb1170ef62e9f7cc4ef57504887d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53108709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a047b47bd4821e5074533d512589cafb0399d269b37bae982a2fbb1a6da43f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:13:18 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d435636ecaa9d314da3b9526ce8ffb915df1d1d123d0c89c4b4ccaa11ac080`  
		Last Modified: Tue, 18 Nov 2025 02:13:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6f07fa5d109121e07b49d6a4051519e472ac053917bcc65a4f1d5704a6ecdafa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af48c926e2c226f2446a2f0369b035e5e8f43956643a77d30e6bd9bd261ce41`

```dockerfile
```

-	Layers:
	-	`sha256:57b7ebc89908e0352f42dc04de1fac30177cee872feb55b341f09f785afdcaa0`  
		Last Modified: Tue, 18 Nov 2025 04:33:12 GMT  
		Size: 3.2 MB (3173529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:432fba6335d79bf21caf45dc10805614f8a4ab1df8e9206e1b716a307bb523c2`  
		Last Modified: Tue, 18 Nov 2025 04:33:12 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:ec4cee843308ac62557c227654970042ed57d48efe4123d7b1db9883e0744609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbd4a9a7852ad1c5ff35e6df4802084692d8398e42d6174e109bc50c4f90249`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 08:00:33 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65078450b0c90df182859d37d74acbf895300f65d491a75601dd557e9e6b9e5`  
		Last Modified: Tue, 18 Nov 2025 08:01:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:520d4e69c7cece580390e175b78e19544b944ccce34a44688c1fe73b7443a890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3168151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c1bfde24af6f009b73378a3dd740b11342d99fc9f0fc2242523dbd5da17e6e`

```dockerfile
```

-	Layers:
	-	`sha256:97aa38817f842c339a06a0868e4eb8bf0b0cedaa97627c67eed244656b6b84fc`  
		Last Modified: Tue, 18 Nov 2025 23:03:42 GMT  
		Size: 3.2 MB (3162341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f67e1e8fd563d0ec7f572d119d5e53043e66e0815c9dca569c56415d74e0615`  
		Last Modified: Tue, 18 Nov 2025 23:03:43 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:46557db7318a5d9494c152bbc2339c097f93234aa3a975e5de1c8599ec402ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49346237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa5bce47833fc057e81860eaa5af2bda0cb5074bc3a69b4fa3448152a3b8a56`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:13:05 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f63b7305b5e8a89431e1cf525f281f1996f378a5ecd2cec21d7bed7a43a35d1`  
		Last Modified: Tue, 18 Nov 2025 02:13:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bf1bcec38666f05a45e155b1bccc2c78a34cf404a7ff203503911a96088e49e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec2dd6192cfc6166180d8eef848bf1623b7ea1a0003dba7fe4ceb1071167323`

```dockerfile
```

-	Layers:
	-	`sha256:af49e3cb29215aef0c0eb71699c5ff85b9759f4056d449a6afe7074c3ddf805a`  
		Last Modified: Tue, 18 Nov 2025 04:33:20 GMT  
		Size: 3.2 MB (3171465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56eb88240bbf55ec1ea28e7f227be47f6c11b169f4b50ed81a9edcc90612107f`  
		Last Modified: Tue, 18 Nov 2025 04:33:21 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
