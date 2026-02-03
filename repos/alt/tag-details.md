<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `alt`

-	[`alt:latest`](#altlatest)
-	[`alt:p10`](#altp10)
-	[`alt:p11`](#altp11)
-	[`alt:sisyphus`](#altsisyphus)

## `alt:latest`

```console
$ docker pull alt@sha256:52e8c6c4508284246fc418bce8b67514ab42ed78b4d4fa509320773af3c2b5aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `alt:latest` - linux; amd64

```console
$ docker pull alt@sha256:1d217259914e1adad17b026ccdd3e10d110239fdb28ce1c9464fe3370a0e2fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46187749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bea2dd50f467bd6a095a95c40e99aab0bd5215485fe0fa0cb9bb74900d2625d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 17:55:26 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Tue, 20 Jan 2026 17:55:26 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Tue, 20 Jan 2026 17:55:26 GMT
ADD alt-p11-x86_64.tar.xz / # buildkit
# Tue, 20 Jan 2026 17:55:26 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Tue, 20 Jan 2026 17:55:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a42ab2bfe1dca20e462dfa701542c5e6c214bfb0bccfee4e997a586ae2a94b84`  
		Last Modified: Tue, 20 Jan 2026 17:55:38 GMT  
		Size: 46.2 MB (46187558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47b0e5f9f51af46d21e517d7864d8faf43b023ae649849a95a7052f3cab6fb2`  
		Last Modified: Tue, 20 Jan 2026 17:55:36 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:8b8d1aa122f638cd9f383dac4e0debd9525dc2de6cef0f44ce6f0f2f75911341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5305ca66131dee977c4f253e5641a90cc6abcbbe3d8d6ab3722a28a149c5cc5a`

```dockerfile
```

-	Layers:
	-	`sha256:5108ab31d49fc17fd97950f5037929cb2adee190f4cb139cdfd40a9536e5e10b`  
		Last Modified: Tue, 20 Jan 2026 17:55:36 GMT  
		Size: 2.6 MB (2630729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03dcf19b128a76a1c4148f037dc6e21847e076ef94b7676de7533d0998490f95`  
		Last Modified: Tue, 20 Jan 2026 17:55:36 GMT  
		Size: 6.4 KB (6371 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:latest` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:64cc0e3302963a56bdc3bc1d947ca7a13788e10e5d8a0fd874719f716bd699b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44958892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d3e1c77529e1ae5a2cb8d664b6c8a0023b6a25b01738362c3703016cda67cf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 18:01:36 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Tue, 20 Jan 2026 18:01:36 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Tue, 20 Jan 2026 18:01:36 GMT
ADD alt-p11-aarch64.tar.xz / # buildkit
# Tue, 20 Jan 2026 18:01:37 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Tue, 20 Jan 2026 18:01:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e1fb665c097503c7dfacbed2dddb14736389057aa34ed7f7139edc7207d1ebd7`  
		Last Modified: Tue, 20 Jan 2026 18:01:48 GMT  
		Size: 45.0 MB (44958701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e738cf7d22b87712324288bc2229b66d3eb1128a7a16b1dc4378424f5ebc5705`  
		Last Modified: Tue, 20 Jan 2026 18:01:47 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:e6a1ff29de851f26a111c09e69d660d7e8d398bb55c47c8f95bb4dcd9ac2b77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe69b62349d3af6292a503046fc4f2bd13e22f281fd58e4d7fea0f787bcd5f3`

```dockerfile
```

-	Layers:
	-	`sha256:9de4bd7a0cda7c00b5f619c90ac9bf97d0c1cfb3aab3922b257b372260a8e699`  
		Last Modified: Tue, 20 Jan 2026 18:01:47 GMT  
		Size: 2.6 MB (2630158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75552eb452ed622d6813409bd6fff26db4ac352a16bdbaffda3d171dc648d74b`  
		Last Modified: Tue, 20 Jan 2026 18:01:47 GMT  
		Size: 6.4 KB (6432 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:latest` - linux; 386

```console
$ docker pull alt@sha256:632fc5e52bab81eb0a03c37ecdefc66c6ae2d67ea57227cf0968b8dbdb39073b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46229655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab158fa88892c0b5e3a12a6175600738130ad38d4091b67c1282395217c3b590`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 17:54:14 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Tue, 20 Jan 2026 17:54:14 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Tue, 20 Jan 2026 17:54:14 GMT
ADD alt-p11-i586.tar.xz / # buildkit
# Tue, 20 Jan 2026 17:54:14 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Tue, 20 Jan 2026 17:54:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d26ad202d8a1fe005099e4edaa028e55f74139bd5505992855513094619adbfe`  
		Last Modified: Tue, 20 Jan 2026 17:54:26 GMT  
		Size: 46.2 MB (46229464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015981243408993c6207cf5a2d7cbc60143b29c0432098e1847e8bbab0004935`  
		Last Modified: Tue, 20 Jan 2026 17:54:25 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:bf05b7b0755b9f5797941d890c0f93dea038cbc306e14f731f03b3cf4993b41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3913297315640982028aa67717051555bc3df3971e42e0ac6fee699406fd213`

```dockerfile
```

-	Layers:
	-	`sha256:f3c3f17f99fa161d8d7fa3ee3f9964aab5f8ed01d195dce040da2ff9458b192f`  
		Last Modified: Tue, 20 Jan 2026 17:54:25 GMT  
		Size: 2.6 MB (2629450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c00e0a465a54c1062a34932fc9423f6428e4470c341c95d0dc6fae5a9f4adb4`  
		Last Modified: Tue, 20 Jan 2026 17:54:25 GMT  
		Size: 6.3 KB (6348 bytes)  
		MIME: application/vnd.in-toto+json

## `alt:p10`

```console
$ docker pull alt@sha256:2583370db34a7c29f3505fac2601cc22ebae885f732f7615f68db8935ef99e9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `alt:p10` - linux; amd64

```console
$ docker pull alt@sha256:f25dbb6dd5916eb38ec4b111dc59fdc64b68d8adc34a7ec5337a4a0c611a437f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47432381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3270b77937731ebf65ab1b1bb56778e6f049f5ca5965362ae44953860ac90539`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 17:55:17 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Tue, 20 Jan 2026 17:55:17 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Tue, 20 Jan 2026 17:55:17 GMT
ADD alt-p10-x86_64.tar.xz / # buildkit
# Tue, 20 Jan 2026 17:55:18 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Tue, 20 Jan 2026 17:55:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dae52fca8f90712a5d902825fe9b2521dfea6c6d86d1f00bf60ebb4564d98d50`  
		Last Modified: Tue, 20 Jan 2026 17:55:29 GMT  
		Size: 47.4 MB (47432190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba6045a07b52cb8b7871b3c57d9a9b8f25a32210885c57ffafbc43cb7dc8764`  
		Last Modified: Tue, 20 Jan 2026 17:55:28 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:131249a055e8a8fa09300d76db119c2c6225074a27200829b4ed3756f54f0d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2602829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7e6f35eca0a9c029efd67d34b7237c7c39b9fb5a16e59e6801e2617acb032c`

```dockerfile
```

-	Layers:
	-	`sha256:cbbe5577979e0843af1dbf4c6372c2e0ba696f270fbd760d55851c25c1293ef4`  
		Last Modified: Tue, 20 Jan 2026 17:55:28 GMT  
		Size: 2.6 MB (2596750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759ee5732bd73d454a21a2625f0a21c64527627a67880a4642a3b5f2ee5bcd0b`  
		Last Modified: Tue, 20 Jan 2026 17:55:28 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p10` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:f96ee475862767bf27bf1424a9c7b4dc564c4aef14c96d6f4ae0a1d8b72b42e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46604829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cab5b84c37b2208884ee7af39d638c752ffe67a7de92a3e6f27513ca62fcf16`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 18:00:22 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Tue, 20 Jan 2026 18:00:22 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Tue, 20 Jan 2026 18:00:22 GMT
ADD alt-p10-aarch64.tar.xz / # buildkit
# Tue, 20 Jan 2026 18:00:22 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Tue, 20 Jan 2026 18:00:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:14b579c38d772f168c795186c6a5184dcf20bb4b169de6c2c81fea745bd9c2b8`  
		Last Modified: Tue, 20 Jan 2026 18:00:35 GMT  
		Size: 46.6 MB (46604636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f169ea4be3c78fe796ace8f60c39bd6eabf201be445425577ce04e6584a4c1`  
		Last Modified: Tue, 20 Jan 2026 18:00:36 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:f1d7378e52d429502de762d4370b5dc88336992b28ca8e78a907ee4b456cc7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2601520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ada7690a7999143c7e3a6a8dea890b27241839d8f82a029f70f7052697ed20`

```dockerfile
```

-	Layers:
	-	`sha256:268c53cc50cc295517e1012e2d8344aafd81439ba083bc65468fee7fb61fb474`  
		Last Modified: Tue, 20 Jan 2026 18:00:34 GMT  
		Size: 2.6 MB (2595391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9611dee118de2b09b2f8caf5ef2d5e8431cf82bd8d4cd4c50af76b06cbae385d`  
		Last Modified: Tue, 20 Jan 2026 18:00:43 GMT  
		Size: 6.1 KB (6129 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p10` - linux; 386

```console
$ docker pull alt@sha256:0ea7c34bbdae0f9955ed5fd565fed7938e8906a09aa9e697b431f44fa882ebea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48200209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8ae222f3cf357fe9ff6d81aaed71b05dd8a6eb05213738697ac6394a1fab65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 17:52:52 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Tue, 20 Jan 2026 17:52:52 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Tue, 20 Jan 2026 17:52:52 GMT
ADD alt-p10-i586.tar.xz / # buildkit
# Tue, 20 Jan 2026 17:52:53 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Tue, 20 Jan 2026 17:52:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9c2412fcc433b862be21f6c522c8a0f4ea75727ed33c5df4764e6c8c59b2bf2a`  
		Last Modified: Tue, 20 Jan 2026 17:53:05 GMT  
		Size: 48.2 MB (48200017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70deb1f322886b48fabebdc107fbf2c8fc4f331a9949a02b781fa18eb711935a`  
		Last Modified: Tue, 20 Jan 2026 17:53:03 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:865983f693ba158627dcdf870f98d89f3a9c936b05531774d8a7f360a82085eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2604659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba973a71388242732c636dca98416f688e9e0911d4b0414ba6d96f6b1d71293`

```dockerfile
```

-	Layers:
	-	`sha256:5b7e7aefd9876656e92345bde5aa13fa09e60a565d2597e41e7989e3dc9d362b`  
		Last Modified: Tue, 20 Jan 2026 17:53:03 GMT  
		Size: 2.6 MB (2598598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30fb54bc57cbf0f48ef863fbead72b8822816c061e1d03dad71381cb3a6a6292`  
		Last Modified: Tue, 20 Jan 2026 17:53:03 GMT  
		Size: 6.1 KB (6061 bytes)  
		MIME: application/vnd.in-toto+json

## `alt:p11`

```console
$ docker pull alt@sha256:52e8c6c4508284246fc418bce8b67514ab42ed78b4d4fa509320773af3c2b5aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `alt:p11` - linux; amd64

```console
$ docker pull alt@sha256:1d217259914e1adad17b026ccdd3e10d110239fdb28ce1c9464fe3370a0e2fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46187749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bea2dd50f467bd6a095a95c40e99aab0bd5215485fe0fa0cb9bb74900d2625d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 17:55:26 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Tue, 20 Jan 2026 17:55:26 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Tue, 20 Jan 2026 17:55:26 GMT
ADD alt-p11-x86_64.tar.xz / # buildkit
# Tue, 20 Jan 2026 17:55:26 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Tue, 20 Jan 2026 17:55:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a42ab2bfe1dca20e462dfa701542c5e6c214bfb0bccfee4e997a586ae2a94b84`  
		Last Modified: Tue, 20 Jan 2026 17:55:38 GMT  
		Size: 46.2 MB (46187558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47b0e5f9f51af46d21e517d7864d8faf43b023ae649849a95a7052f3cab6fb2`  
		Last Modified: Tue, 20 Jan 2026 17:55:36 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:8b8d1aa122f638cd9f383dac4e0debd9525dc2de6cef0f44ce6f0f2f75911341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5305ca66131dee977c4f253e5641a90cc6abcbbe3d8d6ab3722a28a149c5cc5a`

```dockerfile
```

-	Layers:
	-	`sha256:5108ab31d49fc17fd97950f5037929cb2adee190f4cb139cdfd40a9536e5e10b`  
		Last Modified: Tue, 20 Jan 2026 17:55:36 GMT  
		Size: 2.6 MB (2630729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03dcf19b128a76a1c4148f037dc6e21847e076ef94b7676de7533d0998490f95`  
		Last Modified: Tue, 20 Jan 2026 17:55:36 GMT  
		Size: 6.4 KB (6371 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p11` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:64cc0e3302963a56bdc3bc1d947ca7a13788e10e5d8a0fd874719f716bd699b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44958892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d3e1c77529e1ae5a2cb8d664b6c8a0023b6a25b01738362c3703016cda67cf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 18:01:36 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Tue, 20 Jan 2026 18:01:36 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Tue, 20 Jan 2026 18:01:36 GMT
ADD alt-p11-aarch64.tar.xz / # buildkit
# Tue, 20 Jan 2026 18:01:37 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Tue, 20 Jan 2026 18:01:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e1fb665c097503c7dfacbed2dddb14736389057aa34ed7f7139edc7207d1ebd7`  
		Last Modified: Tue, 20 Jan 2026 18:01:48 GMT  
		Size: 45.0 MB (44958701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e738cf7d22b87712324288bc2229b66d3eb1128a7a16b1dc4378424f5ebc5705`  
		Last Modified: Tue, 20 Jan 2026 18:01:47 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:e6a1ff29de851f26a111c09e69d660d7e8d398bb55c47c8f95bb4dcd9ac2b77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe69b62349d3af6292a503046fc4f2bd13e22f281fd58e4d7fea0f787bcd5f3`

```dockerfile
```

-	Layers:
	-	`sha256:9de4bd7a0cda7c00b5f619c90ac9bf97d0c1cfb3aab3922b257b372260a8e699`  
		Last Modified: Tue, 20 Jan 2026 18:01:47 GMT  
		Size: 2.6 MB (2630158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75552eb452ed622d6813409bd6fff26db4ac352a16bdbaffda3d171dc648d74b`  
		Last Modified: Tue, 20 Jan 2026 18:01:47 GMT  
		Size: 6.4 KB (6432 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p11` - linux; 386

```console
$ docker pull alt@sha256:632fc5e52bab81eb0a03c37ecdefc66c6ae2d67ea57227cf0968b8dbdb39073b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46229655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab158fa88892c0b5e3a12a6175600738130ad38d4091b67c1282395217c3b590`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 17:54:14 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Tue, 20 Jan 2026 17:54:14 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Tue, 20 Jan 2026 17:54:14 GMT
ADD alt-p11-i586.tar.xz / # buildkit
# Tue, 20 Jan 2026 17:54:14 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Tue, 20 Jan 2026 17:54:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d26ad202d8a1fe005099e4edaa028e55f74139bd5505992855513094619adbfe`  
		Last Modified: Tue, 20 Jan 2026 17:54:26 GMT  
		Size: 46.2 MB (46229464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015981243408993c6207cf5a2d7cbc60143b29c0432098e1847e8bbab0004935`  
		Last Modified: Tue, 20 Jan 2026 17:54:25 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:bf05b7b0755b9f5797941d890c0f93dea038cbc306e14f731f03b3cf4993b41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3913297315640982028aa67717051555bc3df3971e42e0ac6fee699406fd213`

```dockerfile
```

-	Layers:
	-	`sha256:f3c3f17f99fa161d8d7fa3ee3f9964aab5f8ed01d195dce040da2ff9458b192f`  
		Last Modified: Tue, 20 Jan 2026 17:54:25 GMT  
		Size: 2.6 MB (2629450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c00e0a465a54c1062a34932fc9423f6428e4470c341c95d0dc6fae5a9f4adb4`  
		Last Modified: Tue, 20 Jan 2026 17:54:25 GMT  
		Size: 6.3 KB (6348 bytes)  
		MIME: application/vnd.in-toto+json

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
