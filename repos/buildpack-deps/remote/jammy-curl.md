## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:2d44895add090e50d16109b602c9c995e63396ff03b4d5e71ffe3e57544a6e41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fb5adfdb06821eb3c639c1d9967e8373b7d5724f651683df30a4e4d1942fe0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36643017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a799773cad394c9dfd349878faec4d457d813f30ea6883a02ea9b49a5d0892a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e9c2d709d1a081127422a39a26861612ac4b73362a9abfb7ce643122e4082a`  
		Last Modified: Thu, 13 Nov 2025 23:09:24 GMT  
		Size: 7.1 MB (7106219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d1096a8eba2592e8cc134c9c587b1db2488faefce04486109a2e21d3555b53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3212096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2376ef10fa5fed309442470566f7de8ab72b82eb7840c6981390afd0636792a4`

```dockerfile
```

-	Layers:
	-	`sha256:8a1ab00fbfd2b94e3838c8694094ec405199e756d1cd2baf6e2880d99fe230e5`  
		Last Modified: Fri, 14 Nov 2025 02:20:12 GMT  
		Size: 3.2 MB (3205215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88f8897b71d5d871b9bd6d36a5226eb9a1972e432c9f167be18c00a162556f37`  
		Last Modified: Fri, 14 Nov 2025 02:20:13 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4185db2f75f3d9e9ea02dc4179bb18e566325b6618d08c1f2f28d5214156f7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33653192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9851e0ce1c52b5539febdb0506fc2247c7eb7f4f6042573212a98f036775af1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:24:03 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:24:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:24:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:24:03 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:24:06 GMT
ADD file:94045c8d87683c20b28046857f569ac4ad9ec1c53b4f70e51c2badd873183cea in / 
# Mon, 13 Oct 2025 17:24:06 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:08:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4179ba9965faf453aec60ab64b5f5722816899d199d00def462ceb5d7057ad8b`  
		Last Modified: Wed, 15 Oct 2025 15:02:27 GMT  
		Size: 26.6 MB (26643386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9739de5d0afd9dca9ee20aee0e521243eef34d61181c7d41fe75a6734b107392`  
		Last Modified: Thu, 13 Nov 2025 23:09:03 GMT  
		Size: 7.0 MB (7009806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:127c4a122cbae2003842aaa0af8683cf1fa0b85c4580d713374655dbfc8969d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3214467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eef5f24550bec74b9819e61c531039a04a6c6e4e99149bb1373b4b5ed6d90bd`

```dockerfile
```

-	Layers:
	-	`sha256:23d3c4544a5cb07b15c4d67a94cf5d69382e0ff3766537de09cee1c2818aaed3`  
		Last Modified: Fri, 14 Nov 2025 02:20:17 GMT  
		Size: 3.2 MB (3207522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdc56220154335082fece549e6a9f3d526bf98f0ed3031d8aee7cef806b93a33`  
		Last Modified: Fri, 14 Nov 2025 02:20:18 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1b51ed5bbac1c4ae01bc4a46e047c0b4c244f45eb31f1579417272f3e83b567b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34436373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e9455cd1530a7499c81460469e237a1a5a740ad2b831d27c84e820fb0ea9de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e799c76d7a2425b1efa4aab18a6ff0211a5844ff8737a1e027e934d92c1ac935`  
		Last Modified: Thu, 13 Nov 2025 23:09:14 GMT  
		Size: 7.1 MB (7052496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6019cea49e3172ca712c632f97efce76330f9a94090f52ab804c61e574f7dfbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3212443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a63b259081f4ed336a7d7b6468cd4540042fce99e27edb2e99a3bce3922fb7c`

```dockerfile
```

-	Layers:
	-	`sha256:408dc2421d6728d94a9b6a0d6f8e0fbbb53312860c4f3e78db18cecd5184687f`  
		Last Modified: Fri, 14 Nov 2025 02:20:22 GMT  
		Size: 3.2 MB (3205482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfaf77ed5c46882f6e2c188225d47a29c3dc3da347f78259924ef24f3c9782c2`  
		Last Modified: Fri, 14 Nov 2025 02:20:23 GMT  
		Size: 7.0 KB (6961 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c6125ec3adb342f83a685713d4b0f277681d9403a82a0a9dab9703d104e0f24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42631362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a87038d0d8e6e13a3d055f6a23faf221c96b5a930b79921c4ece006dbc359a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:08:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b4eeb4fa727e52ece1ec36da1e56c3bc96b88b022439cbbda81d3cb75e1cb5`  
		Last Modified: Thu, 13 Nov 2025 23:09:20 GMT  
		Size: 8.2 MB (8184640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cb283d4773bf9768e612051c8b301fa57cbef17cc4a364f57e3acf9215f5e420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3216764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0964bccc1d7dba7fb5ed24b2f094f59fae0e113727cb82dfa844042942f4699`

```dockerfile
```

-	Layers:
	-	`sha256:b4ee2f8205614a37392a355b2279c18cc973dacae5640160447dffccb46bbc08`  
		Last Modified: Fri, 14 Nov 2025 02:20:27 GMT  
		Size: 3.2 MB (3209851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b5f91c98dc8c292dc0045c00395fb6e519a72173d289f0aca77ba445b29cba`  
		Last Modified: Fri, 14 Nov 2025 02:20:28 GMT  
		Size: 6.9 KB (6913 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cd22bd4a3c98c4a196b2fa3e3b58fb24ff20b021e23f5114ee17071d80ac6335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34160169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a40cb611af58389e49cc4acb7a8ff2a54d2de7b0fac64d5c843cca413d1d550`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:49:58 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:49:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:49:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:49:59 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:50:36 GMT
ADD file:16753c6442cb9871940bcae347672f49a6a001793657c89f4fff53584922f035 in / 
# Mon, 13 Oct 2025 17:50:39 GMT
CMD ["/bin/bash"]
# Sat, 15 Nov 2025 13:00:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5284c23c7e2d64db45a1d6cd39e83038698f86052acddf8ba9fa989a1c5ca270`  
		Last Modified: Sat, 15 Nov 2025 10:01:45 GMT  
		Size: 27.0 MB (27042158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7443a254ed640b3e9cc4214e379249f0da2318389406feff1663a907d6beb399`  
		Last Modified: Sat, 15 Nov 2025 13:01:35 GMT  
		Size: 7.1 MB (7118011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:28a36259baa7237ba610db3c54ac1ba580ed17446dd46540f57214d263fc72ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3206016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7380f11f9de70e93543996c92c4e1b6c75ef2d592cb473502347f9522061f9`

```dockerfile
```

-	Layers:
	-	`sha256:8289918a3041a22f6e7192d4ed9ecd1cda78789d156a481a6128a5c24b5f3162`  
		Last Modified: Sat, 15 Nov 2025 14:19:29 GMT  
		Size: 3.2 MB (3199103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec700c7d731a42c058cf0334b37b439f3189281e28c3007bad2bdd8a59bfaff6`  
		Last Modified: Sat, 15 Nov 2025 14:19:30 GMT  
		Size: 6.9 KB (6913 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:67ce15f9534e5b94f41d4dd28abc6d690af300e527d748353deff33d9a9df03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35021389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616fcde8431c785e6f26ad957d6c9c9c344c74cf70f15db21abb076591640a54`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:08:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2764735b13b9a123bf68ddb184df4ab1cf34712d89ac583a3087b795e7427c5`  
		Last Modified: Thu, 13 Nov 2025 23:09:20 GMT  
		Size: 7.0 MB (7018104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bfbeae7256747941673fab55d34b3114f4bbecff098e207eb7b73ecf1c06f32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3214313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53552bcebfbdbd636171a83bae7cfa1b983c4cc0221a0985499683fc6da1abf`

```dockerfile
```

-	Layers:
	-	`sha256:48c82519d7b41fe281a0e180748ab56b41b8198af882bdbc5a637df622fbe88e`  
		Last Modified: Fri, 14 Nov 2025 02:20:35 GMT  
		Size: 3.2 MB (3207432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d54d8d2d4877b238d37e9a094c16193be0aed4fa9cff6642d23f30747675c7ed`  
		Last Modified: Fri, 14 Nov 2025 02:20:36 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json
