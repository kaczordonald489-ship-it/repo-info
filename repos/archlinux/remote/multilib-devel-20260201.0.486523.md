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
