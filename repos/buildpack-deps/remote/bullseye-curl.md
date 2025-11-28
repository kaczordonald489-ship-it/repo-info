## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:06e103f3ee129d166d3743532ade8e8e5ad133587f307bfa8545ceb8e67625c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ad60c33283c7063464e8adb0f560ccc67786587ee4108e7a73d96a6658812503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69520617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8592143a9cb700040b493f7e64bb4c1952346ad597cd764a1337cab3d9e2bd47`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:10:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5b6134fa8a3ac5c0189f873bc3e294ab88c8b51487dbaf69fa8590338d4f47`  
		Last Modified: Tue, 18 Nov 2025 05:10:17 GMT  
		Size: 15.8 MB (15764186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c79a4a3be7c1156dc66e2458f7a9e92cc5ad61e8cdb1830cfd4ab2a1e1e53fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5eb8c360ce058b9801c421179fa9ace6d76ee43687f593ef27921a3f13915a`

```dockerfile
```

-	Layers:
	-	`sha256:e6cd7ccdcc3b6dd66c183d48c2ab5815a8a393db191ae3fe18425c38ff4207f6`  
		Last Modified: Tue, 18 Nov 2025 08:20:42 GMT  
		Size: 4.6 MB (4629099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc29e03c24623d62773cdf76bebd9d1060a47cd37cdaa238b25b064855decd2b`  
		Last Modified: Tue, 18 Nov 2025 08:20:42 GMT  
		Size: 6.8 KB (6764 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8ecda00255184f97edc6bbb5cf7849889b69f0f59b64873f81a1ed5bd67d007d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63925819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb2355497be9c2d866755c98c0ac9607b118fc47e16fb101636a06d8c6ffdac`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:57:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:516616c63b11e5af36116ed0b70c230c2287eab3b74b11a00eb299cc4575af64`  
		Last Modified: Tue, 18 Nov 2025 01:14:16 GMT  
		Size: 49.0 MB (49046365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2280342788a66a44d1f2e4bd1eaf8389d9bef9428e09fa0ae948652bfaeee4b8`  
		Last Modified: Tue, 18 Nov 2025 03:58:13 GMT  
		Size: 14.9 MB (14879454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ec015f2510ee0af8cfbb428c8b98f245fc5ee8d2e0668abade12748228412505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4637563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294a8d31060bc3f14d904802d6fa6a93eded2188e06e5fc2dc2fc0923178ec35`

```dockerfile
```

-	Layers:
	-	`sha256:973e8a60afd96836f0b08beeacbaafe527a30767f91cbf28e2be5dff12e2fff4`  
		Last Modified: Tue, 18 Nov 2025 05:22:30 GMT  
		Size: 4.6 MB (4630735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922b33ee237c8952167e32525cbb78e398e100741604add47d03ceb191a99186`  
		Last Modified: Tue, 18 Nov 2025 05:22:31 GMT  
		Size: 6.8 KB (6828 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0e2b36d3845517ac9ce2f5448fef76146c258e61d39a6f392617e528e37c1d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68007256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bdc6fe88a6e614c687d43a1517b00af4cc8f09de382166d969738c61f25199`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:23:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf5c6e26abbf2d346305acdea26f4c77227ae8be9882711816b29b75df95827`  
		Last Modified: Tue, 18 Nov 2025 06:23:37 GMT  
		Size: 15.7 MB (15749561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:77e448f8c26580dc8b73b7ce8b03cd9e4c4c126a0177ffc8945dbb1d840e6167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac4385b9ff5e7954980cb5cfa70cdf7b232e6f9ad6d6472a236fbaa0c8b577d`

```dockerfile
```

-	Layers:
	-	`sha256:e52b4bba296e2efc8607fd485d3d3f839ef9cfacc06c4922ecad5f244e75e442`  
		Last Modified: Tue, 18 Nov 2025 08:20:50 GMT  
		Size: 4.6 MB (4628713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21909d5942aeb609da3ef5efeac4256e1b33bfa9a0a83901c390877ac653d7a2`  
		Last Modified: Tue, 18 Nov 2025 08:20:51 GMT  
		Size: 6.8 KB (6844 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:576a0941f693bcd4e83b414c1c7a777891dc08e0959fbcba3f1188da7fb432ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c237d0c97403486b13659cf13cba0dda5c50b6a917f45f9302a6e35f00b6daaf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 02:56:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ff276d829f31f5253bbd1b7f53ddf75bfd6004f7fcc06ea8ad1b23a242b12d3b`  
		Last Modified: Tue, 18 Nov 2025 01:13:28 GMT  
		Size: 54.7 MB (54699599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91162d93e41e901767fb0ecc9c7694fbbb7b80a5384451f5ee29e2889d7672be`  
		Last Modified: Tue, 18 Nov 2025 02:56:26 GMT  
		Size: 16.3 MB (16267715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d3a24e9ec85d51f03db2251f3f170a91e201e008a4c6c6b8e49db4f380718dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4632344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37397d6a3ceeacf02629020f783bf627142f4e6124751b162fdc360487f0709d`

```dockerfile
```

-	Layers:
	-	`sha256:d1fb21440ee01a5d981e5b989930e977cc1fbd7f1159470b2776b229e0cef3df`  
		Last Modified: Tue, 18 Nov 2025 05:22:39 GMT  
		Size: 4.6 MB (4625602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:867117da99ec36980d12de3f013dc33ed576144edd1ebac4ebf98ee9f1d7d2d9`  
		Last Modified: Tue, 18 Nov 2025 05:22:39 GMT  
		Size: 6.7 KB (6742 bytes)  
		MIME: application/vnd.in-toto+json
