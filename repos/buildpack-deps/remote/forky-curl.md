## `buildpack-deps:forky-curl`

```console
$ docker pull buildpack-deps@sha256:85cb03807363ae05c17860ebe40ad51cee8bd2b5713574ed09e25bace45160b3
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
$ docker pull buildpack-deps@sha256:d9ff8e8955804b4282990c08995450454f588d8f1ee7bbed2b5638070d816d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75851863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99974cbf54138953877466d67f8afbfcdd3912dd849a9d385dd79779c5c57fd1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:42:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e7ee730174f13176a4a2ca706f251743bedcb5459da1b8f275d5b6bcc67c0aef`  
		Last Modified: Tue, 03 Feb 2026 01:14:19 GMT  
		Size: 48.7 MB (48655735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8e2c9590f8317f5d54b9d2db2e9be22b3330f9ceb6219eb4096cfb413265a8`  
		Last Modified: Tue, 03 Feb 2026 02:42:39 GMT  
		Size: 27.2 MB (27196128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6212dd6b20cebd33bbb963252d4b7bb972b49964870288643aba954b707bd521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4138580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbd7466f77dccaa83247edcfa1a8e65604b9398954580539fd5caf1c5034eec`

```dockerfile
```

-	Layers:
	-	`sha256:c3c63c65c2de86d3fb94a63476c6944d12fd95c98ca3b6f7bb8a13997ff8f275`  
		Last Modified: Tue, 03 Feb 2026 02:42:38 GMT  
		Size: 4.1 MB (4131807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f24cd9f09d0b3add02094a411dc94a45ee35d439e2f4b7af713604fb6468492`  
		Last Modified: Tue, 03 Feb 2026 02:42:38 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d21bb8a0e2b7848d0c8ba3f79b067076bf931d35c1a4cbe25776ad552f107caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70529635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10d510b0dd4a41fa17df041c7570023612a92c40f3cb117c666989e10e72de8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 03:31:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8ad4a919778d324780b6dee51af6abcf1139f6d57c0ba625c1995bf19d763478`  
		Last Modified: Tue, 03 Feb 2026 01:14:27 GMT  
		Size: 45.6 MB (45620616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70526fc33f5a0e4c0788e8433d79a8b805fd260b73e79eaf814e95eb7da57f6c`  
		Last Modified: Tue, 03 Feb 2026 03:31:37 GMT  
		Size: 24.9 MB (24909019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f7da725553ae63e00173699d29f91fd8b66c69217f0ca41188f4ba00c7341916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ce094307f59ab81fefa2de627df9fdd813dab0cd694fb105f327ee2dc094d6`

```dockerfile
```

-	Layers:
	-	`sha256:aa91fbc62f8e6b3c88a0b6191de566392bc80f6bae25cd7059cb2951056ace08`  
		Last Modified: Tue, 03 Feb 2026 03:31:37 GMT  
		Size: 4.1 MB (4133303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:310482d2ba99894e781b63bcfa60ad8b982ff61cae14083616aa6b81ed774dae`  
		Last Modified: Tue, 03 Feb 2026 03:31:36 GMT  
		Size: 6.8 KB (6837 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4f6124df070eb23f96ae730622ae502ced53e726eb91567d17a282887febc9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75192036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f09759d00e09908e16b082b839958059de703aa11dddc6a68b178f08f80b0d7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2309f92dd0c61c985b2d0f865b8d146291a99f7a179b5a243da4f72d2cb33817`  
		Last Modified: Tue, 03 Feb 2026 01:14:24 GMT  
		Size: 48.7 MB (48678525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5e89716ddee93a128c0808e16d7143a2c6bbe2184dc60f5736259c43d5203b`  
		Last Modified: Tue, 03 Feb 2026 02:45:45 GMT  
		Size: 26.5 MB (26513511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b04b4eca318b04bdd54d46b4ab68609d40813c74ade9e7d4b5306883840aaf1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268e4146c8b2e34ccbc8e09d59b851847abbf9fd3d7ddf72623da1381f5ee3d0`

```dockerfile
```

-	Layers:
	-	`sha256:9192c10a69239baacab9d834ebed67791065195004998611e563858f90ea8461`  
		Last Modified: Tue, 03 Feb 2026 02:45:44 GMT  
		Size: 4.1 MB (4142000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d16ca3c2532a3deb8aad59e061ca47a5285ec42243b1380d5a391469483c6c`  
		Last Modified: Tue, 03 Feb 2026 02:45:44 GMT  
		Size: 6.9 KB (6852 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:29d495b79d8b13cf06ee944b789964558d704a9b8a1dad8d72fa1d75762a1a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78462554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8ad12de69fbb4b47d91f4d874385e322e9f569b0213e8a7c4b4e2d8d77e4eb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:49:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bd6304d6e56f66e13385dc7464436c6e3933118a9e5b697acc2b57e9b6d5e5cc`  
		Last Modified: Tue, 03 Feb 2026 01:14:23 GMT  
		Size: 50.0 MB (49981936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1219332a3ab84c1a8edc635c16cc9d1b762a36e8636831f5a2cc5683909cd520`  
		Last Modified: Tue, 03 Feb 2026 02:49:49 GMT  
		Size: 28.5 MB (28480618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:034662e9c560dfe17e75628455e18ee3f3c2f58524e93c1079d136de4992137a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4135650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ac07af1ab46224cb500676f8cbdceff4226de4026708693f29aca5b82471ad`

```dockerfile
```

-	Layers:
	-	`sha256:4857d8212d9eacf55ed2e98bb8ccce36579452e31bf91eec928121dc9ba1127c`  
		Last Modified: Tue, 03 Feb 2026 02:49:49 GMT  
		Size: 4.1 MB (4128899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ea5a5d74b751e140077cd918e6a53d714112da0086ce858a4be1b5ceaf7c8e`  
		Last Modified: Tue, 03 Feb 2026 02:49:49 GMT  
		Size: 6.8 KB (6751 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:501e56b3b252337e77cb54a2a156ba963b6c31442badd50dca90788cf943e6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83065837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac7fca5db4398b0d636478ee232b68a0f7fae9fe4c1eac863bb7d8867fcc5a5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 05:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3a0a026d4bb771de47d622d680861a5062bd4e0c02e6c2d817a503a12b7411ab`  
		Last Modified: Tue, 03 Feb 2026 01:13:26 GMT  
		Size: 53.6 MB (53582665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f4250e1c3eb2c2760041ecc5b52913cec79884bf114b72d39c757b1f167fd2`  
		Last Modified: Tue, 03 Feb 2026 05:23:27 GMT  
		Size: 29.5 MB (29483172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:853e780f8d93a65a905ddffcc9ad98be4490d7490db5b7cbbcfdbefc171e3029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4142503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78199af839a3966b99c5120651aa5e2f702eadc76ec179bf22940574b2c42e03`

```dockerfile
```

-	Layers:
	-	`sha256:55e329efeb51fe255a446f9ac0fc1aa04d5e7057e38002bb9fc14ed8204e6e03`  
		Last Modified: Tue, 03 Feb 2026 05:23:26 GMT  
		Size: 4.1 MB (4135698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3661bbe9cfce8867faf4a57a19fca07880a9f348e3cac65d441b980d68cd1116`  
		Last Modified: Tue, 03 Feb 2026 05:23:26 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:026cf6fa99395d5d2ef8f97b64774c7632093f2d0490df262b3317532777a839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73586837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50abe52e9256a092275477e0e30f48a2d950030c714330502095feaf2d87a3de`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1768176000'
# Fri, 16 Jan 2026 06:40:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0d152d1dcac9b1a7bbc763f3f2f3b2328b12317f387036c0ef1af1b70d3cf327`  
		Last Modified: Tue, 13 Jan 2026 00:52:30 GMT  
		Size: 46.9 MB (46854463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2df243ee2ea0a1e6a943f1e15516b1ef52c050634f2ee4c2fb36ff3ea6ef909`  
		Last Modified: Fri, 16 Jan 2026 06:42:09 GMT  
		Size: 26.7 MB (26732374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:905c78d215d821788692318c4e793f90c242ba1b28747c67f08e195e29e36347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d01c3f9ec0f64a45cc7953e0ca9e8a1bd9f0c56c3e4b33f861fb3d5efb0ebc3`

```dockerfile
```

-	Layers:
	-	`sha256:76e0438407c15b1049e0953f18500b3d861a88dce72652f9a542473cfd1ee78c`  
		Last Modified: Fri, 16 Jan 2026 06:42:05 GMT  
		Size: 4.1 MB (4104988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:989cffc41e4f292f03a72b84e3d9f079e59191feeeb7dac734c1ec52a5b6f17f`  
		Last Modified: Fri, 16 Jan 2026 06:42:04 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:66bd9ace036703a6dda7b4d62f2d8925773572ff93174e581a08402f6549f7f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75429721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1d0df4b668de4fc3df62d506449e2e877aa1677c4ab166884ee39dc54e2efd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 03:44:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:616d765aba14d266e800a78cc4d0cdbfd95c5d967a141135b80d41a64ad5ee62`  
		Last Modified: Tue, 03 Feb 2026 01:12:49 GMT  
		Size: 48.4 MB (48429330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc16728429c562a41c48a34a273412791fb028a15a3f8cb028d1c50e5d9cdd3a`  
		Last Modified: Tue, 03 Feb 2026 03:44:50 GMT  
		Size: 27.0 MB (27000391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dd6ee1c08911fc736aae85d5495df910c3576bb1d1c409af2c0fd0bf10fdbd2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4139989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54c22bb7f156737aaf0f3e7405a1cc902af1561a00132c560c44c9ef5943015`

```dockerfile
```

-	Layers:
	-	`sha256:7acee276d166ecfd32b4c3adab2ef9820de1d374961008aac07f0a7d88653d30`  
		Last Modified: Tue, 03 Feb 2026 03:44:49 GMT  
		Size: 4.1 MB (4133216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e91ef0b0c0617d5a953032cdc9c3822b61baa0aa069d256d9de3f9115bf5e3ea`  
		Last Modified: Tue, 03 Feb 2026 03:44:49 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json
