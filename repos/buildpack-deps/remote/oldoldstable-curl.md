## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:9968481231599ecb4520f652e73de47689bd7d84b3febb24bc8bf82d86236368
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

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1cfeac970045ec521be6c07809ea2c460b7a472e6e21414988d8214d0da015e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69521857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a45e64c0e63d570f34f7ce41989d6c6fb6468477cfc0a8b5fa1a7c4a4260737`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:42:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee799e8390add15bd75ca0b567540a98a55aa9abc40d4c0985dca18f87c25044`  
		Last Modified: Tue, 03 Feb 2026 02:42:11 GMT  
		Size: 15.8 MB (15765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9dff7c517e6f407988f7d6b8ee5b7b59b7b9ead6bace3fe62adea7f3c0c31cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10477c80ed691a0f92109dff2691d8bfdf16dc053c5ff7fb0244e3d270534b10`

```dockerfile
```

-	Layers:
	-	`sha256:0745cd008dc387364fb03c06228726e2e7ed141883c7cb96f3896e22c580fc3e`  
		Last Modified: Tue, 03 Feb 2026 02:42:10 GMT  
		Size: 4.6 MB (4629099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36d5c0a2f19d3d66b6ec1e67c6c2d948e9cfac0501135dbfb033e644137cdde2`  
		Last Modified: Tue, 03 Feb 2026 02:42:10 GMT  
		Size: 6.8 KB (6764 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a89e000bbcfaa1db499add622395ebdd40e7305fa6af471cb3e42df60332bfb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63929043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00214dce347876436b30bff18e18f892146f37a96456fec47322ee595b7ba4ab`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:30:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6ca5f53d580fbc72887807a74d2d1c2f8900fc3f535a8082d3df4fc3f9e84caa`  
		Last Modified: Tue, 03 Feb 2026 01:13:42 GMT  
		Size: 49.0 MB (49047418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b496e431ca97183650bec266004dde0fc1c85e5f1c690d4146afd2ea94035dc`  
		Last Modified: Tue, 03 Feb 2026 03:30:31 GMT  
		Size: 14.9 MB (14881625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:79d3de106ab89bd8b1bf97be400fafa7bc0a2a5926236a1accf9855b9c3e8857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4637563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94837b75a21fadd57e91896905ea2b4e123c4513fb7c12f4b0be35752c5240a`

```dockerfile
```

-	Layers:
	-	`sha256:2cf2e8c4af14da5b8837ebdc496798c37335e32dcd4d2fc163dbc08a80368530`  
		Last Modified: Tue, 03 Feb 2026 03:30:31 GMT  
		Size: 4.6 MB (4630735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7640833e198b29bd8bfd8447b9c59eaee249f30eb382de68caac50d3345e6ef0`  
		Last Modified: Tue, 03 Feb 2026 03:30:31 GMT  
		Size: 6.8 KB (6828 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e8f1b443dbd26ddf7e7a43875b89c8357725eb61e270c078ba17808117a09c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68009966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5600b8f5b75ffd8217f18b106fbafd312cd6ba2fa5d69286b6f693dee5e3651b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:45:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8786fbba60dc8d61eaf8fb6b0cf5291a807641e61a5c761e1cba765ef879da43`  
		Last Modified: Tue, 03 Feb 2026 02:45:17 GMT  
		Size: 15.8 MB (15751646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:17d1ede81b64f1b9265f408256853b1df9fb13540724c4a16ef5a02dcd136fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57ee84c01338f21a56b00378d640e52ddbb37fda3561ec7db2a393f7b343115`

```dockerfile
```

-	Layers:
	-	`sha256:a5068dbcb7074035a3f9304d3894786ab1c7db3721b208f3a87bc7c10a7e4625`  
		Last Modified: Tue, 03 Feb 2026 02:45:17 GMT  
		Size: 4.6 MB (4628713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe350473bd924d04283a55f235cfaaad2f8da16f1863567906867ee78598b1f9`  
		Last Modified: Tue, 03 Feb 2026 02:45:16 GMT  
		Size: 6.8 KB (6844 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:632eda47b27d4dfe44cbb068f0a2bf8237f83a85dac02b620de6402e14fd1cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70970324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001c3e944562af50c10bab78106e9b9f7a9cc6e3c1399661c85e3b597c556081`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:49:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f6d70808fcfec5fc2c45e150a669aa79950bfd30968e7ba0de2c962cff56fc33`  
		Last Modified: Tue, 03 Feb 2026 01:13:58 GMT  
		Size: 54.7 MB (54699582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83b8227b1b97d84c4a7d4b36dd8fcd700f5f0189b543ddd06f7510ecfd20ed9`  
		Last Modified: Tue, 03 Feb 2026 02:49:37 GMT  
		Size: 16.3 MB (16270742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7f0ebae647d83ae9ca83cbc836246c54d0d804eb686005b47e84ef3e8b6d0508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4632344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4124143eab1c727056c104206d00250424eb77f84646e2cde2dd159f47c29fd8`

```dockerfile
```

-	Layers:
	-	`sha256:32eb57aaa3b272824e7d80e8bc59561c4630a05b96871ed4a6dda71d35594b84`  
		Last Modified: Tue, 03 Feb 2026 02:49:37 GMT  
		Size: 4.6 MB (4625602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe89622ea5b5e8859cc2b4dadcf495f6afb156d5bc7a8b1ef74c7bef5d7e020c`  
		Last Modified: Tue, 03 Feb 2026 02:49:36 GMT  
		Size: 6.7 KB (6742 bytes)  
		MIME: application/vnd.in-toto+json
