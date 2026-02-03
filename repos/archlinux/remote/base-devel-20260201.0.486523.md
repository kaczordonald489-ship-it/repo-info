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
