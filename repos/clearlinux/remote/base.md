## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:ea82c1042e56f70b697844a9060d49c87bf4193c5cb9a2f34c45ee3e756019f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:e9aef15e29788a0beec6b91c51e648719fbd926e21ef7087c3992548b72cc082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70593539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c393abd5219460940dee8dc336f366f8dc1a6a61fc3789d14a62f19681322fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Jun 2025 16:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 12 Jun 2025 16:22:54 GMT
ADD base.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:22:54 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 12 Jun 2025 16:22:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fc1c4db2aede84aec87f4f4ea1364d0a09df26295ec3358c351a578dbf211b3d`  
		Last Modified: Mon, 16 Jun 2025 21:45:47 GMT  
		Size: 70.6 MB (70593325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900c47dea25013fbe2692251291107af1a72277ebbea7a3f0bfa834f3f6a9692`  
		Last Modified: Mon, 16 Jun 2025 21:45:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:8acd28700a458138a391c560d3b7d663a365f7acecf78a89d52f88420680df53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9557cdb9978619a4f51e3b315e66324abd8acc363dde6e9a887ab7dbeeb28cf8`

```dockerfile
```

-	Layers:
	-	`sha256:071e93876c0bdf27ffa689418b9c83c68c43fed299c6c80620df3a22bcf8a065`  
		Last Modified: Mon, 16 Jun 2025 21:45:45 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
