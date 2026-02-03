## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:63b86e285aa1c53b8260a18f666845b6f2cf3ae69aee350290064b39c2fa4dfa
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

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8b6b01787f039e30d884795211f4fdd8e23a0edae5f5797a22e754c38275a6df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74906962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2b60a53190ce31b025e13e9dd83c27644fb5cc5eacb2225ccf5734403338c7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954d6059ca7bdbb9ceb566ca2239e01ef312165659d656753d7dbace7771a591`  
		Last Modified: Tue, 03 Feb 2026 02:43:06 GMT  
		Size: 25.6 MB (25614010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c9ea60b555631b25158b68dcf03fabc67cf356f11a9754e3b36c5bc18051247f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f8ccc2fec38c924ecadb39d686cf17b0b1e90cafb1a859cef55c26063dd1fe`

```dockerfile
```

-	Layers:
	-	`sha256:6f12ad5a5d6776035528e3a1c21247b9598145e0843e77b15cf4c2ccc3e0b47b`  
		Last Modified: Tue, 03 Feb 2026 02:43:06 GMT  
		Size: 4.1 MB (4119913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7036b2df6461fe58796f9cbb14e35792a345472a815591af505bc80429b3bb5f`  
		Last Modified: Tue, 03 Feb 2026 02:43:06 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e3f3aa945951224c54755f0426a81afc3b89ba04d8f46a24c787b016fb5a5edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71809514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2486eaa8e6dc97df15b060af079f25473a971352c712e077ab6ee4006ec11f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ba31dc65cf53cae37b5517f251f4d408e91109de491cbd8816a9f21c33a05203`  
		Last Modified: Tue, 03 Feb 2026 01:14:09 GMT  
		Size: 47.5 MB (47453997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91afe525ee94a6eec8f0285b6d37bd019b53a0d3e972edf130127870dbcc171e`  
		Last Modified: Tue, 03 Feb 2026 03:26:40 GMT  
		Size: 24.4 MB (24355517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ca4b0e13585189f900aa4bbc5e0ab45863a35969553a8958aece3d83086dd365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4044e1201e16a9ead6a7f790c5efaa3a2f88c6fa0a83401bf048593181af77`

```dockerfile
```

-	Layers:
	-	`sha256:0464a7a869b77f0c23a35e5b8bbcfaa6544a405705a9547536199d1e9d125e67`  
		Last Modified: Tue, 03 Feb 2026 03:26:39 GMT  
		Size: 4.1 MB (4122903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b302c0a65bb9e78e082dccb602bbea4d3e7858c95202336122e4cdba41b28041`  
		Last Modified: Tue, 03 Feb 2026 03:26:39 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:73452e9ae7a3de4d3b5d982d15404035d968cd76f16b7d7b8155eb9a53ab3909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69353289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703445611d92d1f972da22f39bc3ab22e5ef7c845eeb2d473b0f413e56510f47`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:32:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e712004ad7e72ac7b512e7e067d08c1f627b7b81a230302cbad4864b08acbdff`  
		Last Modified: Tue, 03 Feb 2026 01:14:45 GMT  
		Size: 45.7 MB (45724966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db74387350d2cb71494f8cd51684a1223fa4d67c2770958430649aa3d99f0d84`  
		Last Modified: Tue, 03 Feb 2026 03:32:37 GMT  
		Size: 23.6 MB (23628323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4051e6b48c74b96e983720c91ef3b10a3665ea2257a4dce7bab46b1bb9ae7cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3384112db61c2f9557ac4b40cb639ca0b2b637d39ccfea4605494ea9ed5a2d80`

```dockerfile
```

-	Layers:
	-	`sha256:b2ff0746e3c3f20d93bf95b32f585fac049b50fecbc8cb38c14b247ff3718aa3`  
		Last Modified: Tue, 03 Feb 2026 03:32:36 GMT  
		Size: 4.1 MB (4121414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b511578008af22992f98fedb2ee5c8c6825c70fc1363e1a73eaa6021d3598da`  
		Last Modified: Tue, 03 Feb 2026 03:32:35 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d1a94f797e9c967b3b060373ed5cf8d31239ae9ee02fe22e26574dd64da085f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74674705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882a956188ddf23ddb9770d51471f244f63e87cf66065ac1a4e5088637d82f7d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cace8fbd9245d4cb1b11d410baa101c40f315e70bee7d3ba014bb966a4da4517`  
		Last Modified: Tue, 03 Feb 2026 02:46:11 GMT  
		Size: 25.0 MB (25022688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b586b36ea17ddafa7263c1cebbc6907ff3e6157f2f0aecb426ab4d46289f20ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa13a0a65c31fae70f4870a68c9f56165ce51bcad320051fd3f50cd18461284a`

```dockerfile
```

-	Layers:
	-	`sha256:ea1fc5f61063a468b8cabd3b4a5b514d09e9ef180b61b85425aad3a606ee868e`  
		Last Modified: Tue, 03 Feb 2026 02:46:10 GMT  
		Size: 4.1 MB (4121455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9c34bf090a72835e533ff53cef0cd169ffcc5c8a6209e2c035f2e97b5ffb0de`  
		Last Modified: Tue, 03 Feb 2026 02:46:10 GMT  
		Size: 7.2 KB (7178 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5f28ae2f91c5ae10243cbb9639a1b636cc954206e2bcbda99e92b3c752bcf6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77583556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd31d2d884c7bec38ee988dbb087cd9ee1230368b5fb1547907466248466523b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b536877d3c0a030ad79a6593cd07fd6d9d694a4ee908632c85159f47caa880c2`  
		Last Modified: Tue, 03 Feb 2026 01:15:09 GMT  
		Size: 50.8 MB (50805135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82aa8569021d347e27d65aa0b48a5747ad08b2dd9fedb936660291f168eeed9`  
		Last Modified: Tue, 03 Feb 2026 02:49:59 GMT  
		Size: 26.8 MB (26778421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:893cd0b571bd96bf674b8fcdad77c862453dda340b1dc0f10bf3e65fda4a38f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51318d743d30774de211c4deda26bc1b60f6ac99cfc320a4b21367fecfec184`

```dockerfile
```

-	Layers:
	-	`sha256:74f369dd54af1aed0e46c9e7473675da79d74f5a86ec3b21c83f4d020e2e4c5d`  
		Last Modified: Tue, 03 Feb 2026 02:49:58 GMT  
		Size: 4.1 MB (4117020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d096cdc2be09a9261a5c47aa3a159f0e34d2852a29cd1b3346f4f2f49ca45`  
		Last Modified: Tue, 03 Feb 2026 02:49:58 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0a7cb44704f0c1e43720dcf7dbfe1293bfcac750ad6b281c7d976aa92566f5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80110259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b80cb78af919df94a9c1b87c325f59a5b9c761fc46b9fcca236cf0ff0a45c03`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bdc2ae5f94587ddf291ce56c3dd3c244bdeaf3ba39bf6598fe7a02816ade7e`  
		Last Modified: Tue, 03 Feb 2026 05:24:24 GMT  
		Size: 27.0 MB (26998144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:18bcd486b91ffbc8caf4517d3643c9cc37816b63ec3400be0f0a77caa81f4393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee36cf3b96ef70d1864fc8bf31bb855b9d9d933decb2d34a67229da966d8cf9`

```dockerfile
```

-	Layers:
	-	`sha256:2649f5268149aa9d13bf855f01acf022dcb29768f127a70f5bff05818c8aa9a1`  
		Last Modified: Tue, 03 Feb 2026 05:24:24 GMT  
		Size: 4.1 MB (4123761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4c922d8f3978a91453a0cc21910452a687e3efa543e7c25a975084bd32f526b`  
		Last Modified: Tue, 03 Feb 2026 05:24:23 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:953a04b991d3d7a0611fe965973cf3943b90400232dd97207e5e7cfbb496bb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72723579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7d71c6a4d4b2a66a9caa3a8fe4ecb87f80af742f20de94e5fba4c2d41cfc5d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:47:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:14 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7f36a5fa281a3384abd9a90a26442f28edb507f1b9c537a07e1f5aaeb769a1`  
		Last Modified: Fri, 16 Jan 2026 06:49:07 GMT  
		Size: 25.0 MB (24952736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:970b78aeb305e78337b319a0880be9a023e77b0ed16ec19ce3a7ad7355190ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba1c0e914965ebb49dafdbc315c3563c14d051e797e635e7afd854bdd7b61f8`

```dockerfile
```

-	Layers:
	-	`sha256:792dbab9a006e657d8bd23909e1b06c99e6b8a2347ee67d261ac404f58617137`  
		Last Modified: Fri, 16 Jan 2026 06:49:03 GMT  
		Size: 4.1 MB (4112425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff972c99913c6c88371cc6530c33f3f465080d896b017740658865328d3766ba`  
		Last Modified: Fri, 16 Jan 2026 06:49:02 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1e03b09baffb0df719407f5bc5f6d3add3c0482645f4098af6cd9a5e27a65c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76149095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5eca0f9701b2e66def73f230a3325414ff1e9d8e50e55f9aa71803e9e6d3f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef24c0cb82fa1ab6f1887f140586ec94ae060d22e6053b5747ce4acc96547b39`  
		Last Modified: Tue, 03 Feb 2026 03:45:31 GMT  
		Size: 26.8 MB (26794717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a336a411937a08cb16b99ec635388e0833eaed81799978417a1f0f94ecc226de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c585fbe39522fd18aef158f685e58b58e40957669d80f6ac1fbb7e78579d80`

```dockerfile
```

-	Layers:
	-	`sha256:a0f18a17b103acaf9d6ccd5caefa44b15de350c0780ea1ff4bfc196842b64488`  
		Last Modified: Tue, 03 Feb 2026 03:45:31 GMT  
		Size: 4.1 MB (4121323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3a540fa9f84d17350ce3eba9544c88bbb88d83584996e799e7c8849532af4a2`  
		Last Modified: Tue, 03 Feb 2026 03:45:30 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json
