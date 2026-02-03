<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260201.0.486523`](#archlinuxbase-202602010486523)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260201.0.486523`](#archlinuxbase-devel-202602010486523)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260201.0.486523`](#archlinuxmultilib-devel-202602010486523)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:9b8e02df0f0a08fa8144d901932bd85d751257f83e00314053314a27ff87884f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:ef9175f7d68acc29965aaadbf35edf8faadf9457151e6df411b605998c52da0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176478473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db2337dce953d567245583cfe3a1e55714f97b2f269602d9b452f6e7641341b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.version=20260201.0.486523
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.created=2026-02-01T00:07:02+00:00
# Mon, 02 Feb 2026 18:44:27 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Feb 2026 18:44:30 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260201.0.486523' /etc/os-release # buildkit
# Mon, 02 Feb 2026 18:44:30 GMT
ENV LANG=C.UTF-8
# Mon, 02 Feb 2026 18:44:30 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3073b417e59bc720f58f6924fc38b95081720554da79de78fce3cfc3c6bab0c5`  
		Last Modified: Mon, 02 Feb 2026 18:45:04 GMT  
		Size: 176.5 MB (176469724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b3e517c7304ca0ab9cf17bc907800a5fa560a1b683a8667099b23a67c164d5`  
		Last Modified: Mon, 02 Feb 2026 18:44:59 GMT  
		Size: 8.7 KB (8749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:3d7f002b7d1b4bde2c2e06ec6604f4275869a1c1898d7c274613edb22b06dbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8409969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c8a7ca83648c2c48033e947091ee31cf8de6af34494d6ba52476373a3c5400`

```dockerfile
```

-	Layers:
	-	`sha256:8bd72a2256816440fb41c0f13202ba47615c97f79bfa12c3a82da8f3721e4aae`  
		Last Modified: Mon, 02 Feb 2026 18:45:00 GMT  
		Size: 8.4 MB (8398040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:758da1cc47a49374fb6d3b67f3a1656883d6542e73d8133d9bc0cd5dd3252329`  
		Last Modified: Mon, 02 Feb 2026 18:44:59 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260201.0.486523`

```console
$ docker pull archlinux@sha256:9b8e02df0f0a08fa8144d901932bd85d751257f83e00314053314a27ff87884f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260201.0.486523` - linux; amd64

```console
$ docker pull archlinux@sha256:ef9175f7d68acc29965aaadbf35edf8faadf9457151e6df411b605998c52da0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176478473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db2337dce953d567245583cfe3a1e55714f97b2f269602d9b452f6e7641341b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.version=20260201.0.486523
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.created=2026-02-01T00:07:02+00:00
# Mon, 02 Feb 2026 18:44:27 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Feb 2026 18:44:30 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260201.0.486523' /etc/os-release # buildkit
# Mon, 02 Feb 2026 18:44:30 GMT
ENV LANG=C.UTF-8
# Mon, 02 Feb 2026 18:44:30 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3073b417e59bc720f58f6924fc38b95081720554da79de78fce3cfc3c6bab0c5`  
		Last Modified: Mon, 02 Feb 2026 18:45:04 GMT  
		Size: 176.5 MB (176469724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b3e517c7304ca0ab9cf17bc907800a5fa560a1b683a8667099b23a67c164d5`  
		Last Modified: Mon, 02 Feb 2026 18:44:59 GMT  
		Size: 8.7 KB (8749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20260201.0.486523` - unknown; unknown

```console
$ docker pull archlinux@sha256:3d7f002b7d1b4bde2c2e06ec6604f4275869a1c1898d7c274613edb22b06dbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8409969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c8a7ca83648c2c48033e947091ee31cf8de6af34494d6ba52476373a3c5400`

```dockerfile
```

-	Layers:
	-	`sha256:8bd72a2256816440fb41c0f13202ba47615c97f79bfa12c3a82da8f3721e4aae`  
		Last Modified: Mon, 02 Feb 2026 18:45:00 GMT  
		Size: 8.4 MB (8398040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:758da1cc47a49374fb6d3b67f3a1656883d6542e73d8133d9bc0cd5dd3252329`  
		Last Modified: Mon, 02 Feb 2026 18:44:59 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:938749229e882c7a5b60a1de200b4b6c139264595656e594ccb07f53b944f7cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:5f3d3a5f337c95caa50a70dc65337506acc0dee83b14369a2784e978f4676732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.0 MB (294029302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0377e5e79f15b317e0744e0cfa49ec21c2fd3a75527b2711032b9052379b92bb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.version=20260201.0.486523
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.created=2026-02-01T00:07:02+00:00
# Mon, 02 Feb 2026 18:45:39 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Feb 2026 18:45:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260201.0.486523' /etc/os-release # buildkit
# Mon, 02 Feb 2026 18:45:46 GMT
ENV LANG=C.UTF-8
# Mon, 02 Feb 2026 18:45:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e7ac0e85699f5a8fea8761bf03e59bfd0c9bfc8a3b87dbaf7ac81da109b5440a`  
		Last Modified: Mon, 02 Feb 2026 18:46:37 GMT  
		Size: 294.0 MB (294019954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a858d39768706cf42afc8f64065528b9f17910be478c07d889935f38e24d13b`  
		Last Modified: Mon, 02 Feb 2026 18:46:31 GMT  
		Size: 9.3 KB (9348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:968447374724df550c79dfc4d02550ccae1ece453b26126958aaea3e5216d9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12172076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563688429d4b8e0edc1d832bd0ab6d5334ddbc24b9176b7519db89067e1dd71b`

```dockerfile
```

-	Layers:
	-	`sha256:84fba314f20a732ba7d05c73d65e676e55913fb38cc417b169aa2a93ce3a11f6`  
		Last Modified: Mon, 02 Feb 2026 18:46:32 GMT  
		Size: 12.2 MB (12160365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:380531a8ede4bcdb57240c1e4a5a43de445d86b58125df5ec4492cb09ea62c34`  
		Last Modified: Mon, 02 Feb 2026 18:46:32 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260201.0.486523`

```console
$ docker pull archlinux@sha256:938749229e882c7a5b60a1de200b4b6c139264595656e594ccb07f53b944f7cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260201.0.486523` - linux; amd64

```console
$ docker pull archlinux@sha256:5f3d3a5f337c95caa50a70dc65337506acc0dee83b14369a2784e978f4676732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.0 MB (294029302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0377e5e79f15b317e0744e0cfa49ec21c2fd3a75527b2711032b9052379b92bb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.version=20260201.0.486523
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 02 Feb 2026 18:45:39 GMT
LABEL org.opencontainers.image.created=2026-02-01T00:07:02+00:00
# Mon, 02 Feb 2026 18:45:39 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Feb 2026 18:45:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260201.0.486523' /etc/os-release # buildkit
# Mon, 02 Feb 2026 18:45:46 GMT
ENV LANG=C.UTF-8
# Mon, 02 Feb 2026 18:45:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e7ac0e85699f5a8fea8761bf03e59bfd0c9bfc8a3b87dbaf7ac81da109b5440a`  
		Last Modified: Mon, 02 Feb 2026 18:46:37 GMT  
		Size: 294.0 MB (294019954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a858d39768706cf42afc8f64065528b9f17910be478c07d889935f38e24d13b`  
		Last Modified: Mon, 02 Feb 2026 18:46:31 GMT  
		Size: 9.3 KB (9348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260201.0.486523` - unknown; unknown

```console
$ docker pull archlinux@sha256:968447374724df550c79dfc4d02550ccae1ece453b26126958aaea3e5216d9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12172076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563688429d4b8e0edc1d832bd0ab6d5334ddbc24b9176b7519db89067e1dd71b`

```dockerfile
```

-	Layers:
	-	`sha256:84fba314f20a732ba7d05c73d65e676e55913fb38cc417b169aa2a93ce3a11f6`  
		Last Modified: Mon, 02 Feb 2026 18:46:32 GMT  
		Size: 12.2 MB (12160365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:380531a8ede4bcdb57240c1e4a5a43de445d86b58125df5ec4492cb09ea62c34`  
		Last Modified: Mon, 02 Feb 2026 18:46:32 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:9b8e02df0f0a08fa8144d901932bd85d751257f83e00314053314a27ff87884f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:ef9175f7d68acc29965aaadbf35edf8faadf9457151e6df411b605998c52da0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176478473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db2337dce953d567245583cfe3a1e55714f97b2f269602d9b452f6e7641341b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.version=20260201.0.486523
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 02 Feb 2026 18:44:27 GMT
LABEL org.opencontainers.image.created=2026-02-01T00:07:02+00:00
# Mon, 02 Feb 2026 18:44:27 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Feb 2026 18:44:30 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260201.0.486523' /etc/os-release # buildkit
# Mon, 02 Feb 2026 18:44:30 GMT
ENV LANG=C.UTF-8
# Mon, 02 Feb 2026 18:44:30 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3073b417e59bc720f58f6924fc38b95081720554da79de78fce3cfc3c6bab0c5`  
		Last Modified: Mon, 02 Feb 2026 18:45:04 GMT  
		Size: 176.5 MB (176469724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b3e517c7304ca0ab9cf17bc907800a5fa560a1b683a8667099b23a67c164d5`  
		Last Modified: Mon, 02 Feb 2026 18:44:59 GMT  
		Size: 8.7 KB (8749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:3d7f002b7d1b4bde2c2e06ec6604f4275869a1c1898d7c274613edb22b06dbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8409969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c8a7ca83648c2c48033e947091ee31cf8de6af34494d6ba52476373a3c5400`

```dockerfile
```

-	Layers:
	-	`sha256:8bd72a2256816440fb41c0f13202ba47615c97f79bfa12c3a82da8f3721e4aae`  
		Last Modified: Mon, 02 Feb 2026 18:45:00 GMT  
		Size: 8.4 MB (8398040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:758da1cc47a49374fb6d3b67f3a1656883d6542e73d8133d9bc0cd5dd3252329`  
		Last Modified: Mon, 02 Feb 2026 18:44:59 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:0c672642172699694b4c8fcc5bf7878ec27ec5a766850090cfa4fbc7ee1581c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:3fd66e68b64d8aaa5403981bcb0b053bd93e3f0b5ad12de089cb282d75687c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345352831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff07239341b7236538581da6ced1e73dca1bcd4cfec5b9ff115fc00562f3c054`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.version=20260201.0.486523
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.created=2026-02-01T00:07:02+00:00
# Mon, 02 Feb 2026 18:45:43 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Feb 2026 18:45:50 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260201.0.486523' /etc/os-release # buildkit
# Mon, 02 Feb 2026 18:45:50 GMT
ENV LANG=C.UTF-8
# Mon, 02 Feb 2026 18:45:50 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:85ef67454716a78496882955bef184c15cbce73ce07f523c6aa2f167ed1f617a`  
		Last Modified: Mon, 02 Feb 2026 18:46:52 GMT  
		Size: 345.3 MB (345342406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d64ebc94f59fee30f43ae43f40a83dc06bfcadbb9c37ff1f49fb93260a360c`  
		Last Modified: Mon, 02 Feb 2026 18:46:44 GMT  
		Size: 10.4 KB (10425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:5d6e25c703a4dcba9198d65b68b00c26061de7b4976297c577c71567140bd367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12442008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c6942334fbef8b384440f4446481161183f432650eebf6556e215fd458cb2a`

```dockerfile
```

-	Layers:
	-	`sha256:2d4069229ccada2b3d8e32ec424586215fc537fa7ad09931630bcf7ec7588844`  
		Last Modified: Mon, 02 Feb 2026 18:46:45 GMT  
		Size: 12.4 MB (12430240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfa5c90449850f04613c5c433f0982fd8fd658843df435ceb265f6ede1b009ef`  
		Last Modified: Mon, 02 Feb 2026 18:46:44 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260201.0.486523`

```console
$ docker pull archlinux@sha256:0c672642172699694b4c8fcc5bf7878ec27ec5a766850090cfa4fbc7ee1581c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260201.0.486523` - linux; amd64

```console
$ docker pull archlinux@sha256:3fd66e68b64d8aaa5403981bcb0b053bd93e3f0b5ad12de089cb282d75687c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345352831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff07239341b7236538581da6ced1e73dca1bcd4cfec5b9ff115fc00562f3c054`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.version=20260201.0.486523
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 02 Feb 2026 18:45:43 GMT
LABEL org.opencontainers.image.created=2026-02-01T00:07:02+00:00
# Mon, 02 Feb 2026 18:45:43 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Feb 2026 18:45:50 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260201.0.486523' /etc/os-release # buildkit
# Mon, 02 Feb 2026 18:45:50 GMT
ENV LANG=C.UTF-8
# Mon, 02 Feb 2026 18:45:50 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:85ef67454716a78496882955bef184c15cbce73ce07f523c6aa2f167ed1f617a`  
		Last Modified: Mon, 02 Feb 2026 18:46:52 GMT  
		Size: 345.3 MB (345342406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d64ebc94f59fee30f43ae43f40a83dc06bfcadbb9c37ff1f49fb93260a360c`  
		Last Modified: Mon, 02 Feb 2026 18:46:44 GMT  
		Size: 10.4 KB (10425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260201.0.486523` - unknown; unknown

```console
$ docker pull archlinux@sha256:5d6e25c703a4dcba9198d65b68b00c26061de7b4976297c577c71567140bd367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12442008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c6942334fbef8b384440f4446481161183f432650eebf6556e215fd458cb2a`

```dockerfile
```

-	Layers:
	-	`sha256:2d4069229ccada2b3d8e32ec424586215fc537fa7ad09931630bcf7ec7588844`  
		Last Modified: Mon, 02 Feb 2026 18:46:45 GMT  
		Size: 12.4 MB (12430240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfa5c90449850f04613c5c433f0982fd8fd658843df435ceb265f6ede1b009ef`  
		Last Modified: Mon, 02 Feb 2026 18:46:44 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
