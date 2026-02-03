## `alt:sisyphus`

```console
$ docker pull alt@sha256:363afc87bf5e54f15123348a42dbe7869823b9612b31455367aba9d5c7519ef8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `alt:sisyphus` - linux; amd64

```console
$ docker pull alt@sha256:7eeb9f35faf4b1f656830ea1c00cb8bd78fcdf250477cb380f3606709f7b7c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46573725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fe33706f26dd0c3e5bb90472e183a79df307e75466a2355266a4994fa5dea9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 17:55:24 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Tue, 20 Jan 2026 17:55:24 GMT
LABEL org.opencontainers.image.licenses=GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Tue, 20 Jan 2026 17:55:24 GMT
ADD alt-sisyphus-x86_64.tar.xz / # buildkit
# Tue, 20 Jan 2026 17:55:24 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Tue, 20 Jan 2026 17:55:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:048ca6a64522b0ff82894a3db026a84912f7e00dfa916f83eb4ecfe93e9add74`  
		Last Modified: Tue, 20 Jan 2026 17:55:35 GMT  
		Size: 46.6 MB (46573533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2be5a3b2d4675037dabf3940ad67da74d7e90de6b722504b4d8e10de338d2ab`  
		Last Modified: Tue, 20 Jan 2026 17:55:34 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:d3f354bae3f8a47624a22e4b87715b12a322985de0ac1144ac0d75805115d39d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754e77423888878d16968040b8d6c4565137312a56fcf73b64d94c4ae489f298`

```dockerfile
```

-	Layers:
	-	`sha256:706eddb7d40b21efcac57a528a7646515d2ba58804dd702566cf2164d692b9bb`  
		Last Modified: Tue, 20 Jan 2026 17:55:35 GMT  
		Size: 2.6 MB (2618916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c665b0c151c3138cbb9058397a7c03284548c28d195fdd7a1fc14f711945293`  
		Last Modified: Tue, 20 Jan 2026 17:55:34 GMT  
		Size: 6.1 KB (6078 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:38ddc95ee3e6a854e6d221acc7aa15dd8a7ba6068f6ee4284d946b2f434111ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45280877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16709c9cec1d52b302246823f21563245c2b1507bf6cf4751d9a30bf1613cdb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 18:00:28 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Tue, 20 Jan 2026 18:00:28 GMT
LABEL org.opencontainers.image.licenses=GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Tue, 20 Jan 2026 18:00:28 GMT
ADD alt-sisyphus-aarch64.tar.xz / # buildkit
# Tue, 20 Jan 2026 18:00:28 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Tue, 20 Jan 2026 18:00:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:beaae112720b80f9cf707e0a59568ef94f9684b8892c2f6a5d81e1ffd1b4b712`  
		Last Modified: Tue, 20 Jan 2026 18:00:41 GMT  
		Size: 45.3 MB (45280686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891b3097d82d7a00bdeb058128312e657d54a5ef29b88a5578cbcd8f379f4a91`  
		Last Modified: Tue, 20 Jan 2026 18:00:39 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:6f1f9d188ebfd36229b6e6ac2ab257d46872f9fa0c47039453c2d3e8bd32c01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6e6d5c47111c245ef89814d117c6785ac6f863d80b409bb67916d1df28ad5f`

```dockerfile
```

-	Layers:
	-	`sha256:f1aabc793364c0184a5ad4305deaad3198ad4972127ccaf586bdf51418692820`  
		Last Modified: Tue, 20 Jan 2026 18:00:39 GMT  
		Size: 2.6 MB (2618333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76e8d33bddc7b989ea7948f4f2cd85df859eda013dec0ae9a8cd53bb9fa4ddc9`  
		Last Modified: Tue, 20 Jan 2026 18:00:39 GMT  
		Size: 6.1 KB (6128 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; 386

```console
$ docker pull alt@sha256:53e953e8127b709e06743c09070643cb51b7d15352c0130c00cb9867cc256315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46618458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bde2d3b11d21df06c09249f797a8d134f09649c370acb88c24e968dcc941117`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 17:53:22 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Tue, 20 Jan 2026 17:53:22 GMT
LABEL org.opencontainers.image.licenses=GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Tue, 20 Jan 2026 17:53:22 GMT
ADD alt-sisyphus-i586.tar.xz / # buildkit
# Tue, 20 Jan 2026 17:53:22 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Tue, 20 Jan 2026 17:53:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:57932e48720ca7bec75b3fc1d0af03da3e2d34695ea669fb8988758d7c2263a2`  
		Last Modified: Tue, 20 Jan 2026 17:53:33 GMT  
		Size: 46.6 MB (46618269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b86063068a6548f0c5d79964207c9fe9d9baf1ec1822f33588070735f75392`  
		Last Modified: Tue, 20 Jan 2026 17:53:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:54f979b49df35d392a248d2126837c9fe42ce360c7aeb92b66feeb4acaa4671c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2623702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a066b32cfd834d7eae342a38e45785f0b7988f45f629987bddba6312a7cafb26`

```dockerfile
```

-	Layers:
	-	`sha256:9140e54fafd82d5fecbbe1ce71cbe9f454e7932693c42f37a4299ff12c7f6602`  
		Last Modified: Tue, 20 Jan 2026 17:53:32 GMT  
		Size: 2.6 MB (2617642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:153f27023e0d010d4c773895b28f81f9db45448359dbd71ad6065ffa13456455`  
		Last Modified: Tue, 20 Jan 2026 17:53:32 GMT  
		Size: 6.1 KB (6060 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; riscv64

```console
$ docker pull alt@sha256:3cf5bc6acfc8273dc2052faea43de4db6ad0007cd0cd63af5081bcc90e81332b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44486087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d2a588d57b588ae5273d2a515302542b60a3ceda71458c6a4f6c0e93075f90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Jan 2026 05:23:03 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Thu, 22 Jan 2026 05:23:03 GMT
LABEL org.opencontainers.image.licenses=GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 22 Jan 2026 05:23:03 GMT
ADD alt-sisyphus-riscv64.tar.xz / # buildkit
# Thu, 22 Jan 2026 05:23:04 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 22 Jan 2026 05:23:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ba25e668b40b2efaa9085cfdb237dd3fdac12bee44a47b6d0f8175d7c3eaa120`  
		Last Modified: Thu, 22 Jan 2026 05:24:49 GMT  
		Size: 44.5 MB (44485897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f644b3bca52aac38924d1e8d7515b0cb5ec91079fe48391b191fff649a9e5d`  
		Last Modified: Thu, 22 Jan 2026 05:24:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:52c85bd8165d1b5da180d18ce920bf9ce8a74fa34e27d1b515834cf7883c8a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2623698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18908b805353e0f803018b9e1dd6005bf5bd9b4b37efe28ddc7accfa6f6309bd`

```dockerfile
```

-	Layers:
	-	`sha256:7398354c4d28200d04aa4b30f5da872e5946e83d13d627671a9f01c40d73aa65`  
		Last Modified: Thu, 22 Jan 2026 05:24:42 GMT  
		Size: 2.6 MB (2617596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6598b1c5289c5c942753cee096d29bcbe5743711a88b57e9a06da50f3ed0ae98`  
		Last Modified: Thu, 22 Jan 2026 05:24:42 GMT  
		Size: 6.1 KB (6102 bytes)  
		MIME: application/vnd.in-toto+json
