## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:a3cbaa23b459680c6705513fc9b1a7c9764d4e610092a949a5ecc3d116c13563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull mongo@sha256:22e3bbfdfa33c4563f3175e4d86c510dafd59b68563373fb5f35c7a9c3c2b537
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.8 MB (744840299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88e26eb0085e70ffcdc2199f212567a64a913d339faf7e278fad31c1cb58c58`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 28 Jan 2026 19:27:33 GMT
SHELL [cmd /S /C]
# Wed, 28 Jan 2026 19:27:34 GMT
USER ContainerAdministrator
# Wed, 28 Jan 2026 19:27:43 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 28 Jan 2026 19:27:44 GMT
USER ContainerUser
# Wed, 28 Jan 2026 19:27:46 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Wed, 28 Jan 2026 19:27:47 GMT
ENV MONGO_VERSION=7.0.29
# Wed, 28 Jan 2026 19:28:21 GMT
COPY dir:539f819475bf7591bf5d2b5f5ca5ac2f12e1ed24873715f3ec1534ebe7d01465 in C:\mongodb 
# Wed, 28 Jan 2026 19:28:35 GMT
RUN mongod --version
# Wed, 28 Jan 2026 19:28:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 28 Jan 2026 19:28:36 GMT
EXPOSE 27017
# Wed, 28 Jan 2026 19:28:37 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020f166db649bef57023066678981ed933c505a3f7376c90fad56f7f60bbf2b`  
		Last Modified: Wed, 28 Jan 2026 19:28:44 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c98ff1770b31b649defae1d275b3a614313efbd699b6e8b733f7362799c92b8`  
		Last Modified: Wed, 28 Jan 2026 19:28:44 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890594f8be652ee66c2bbabe2a8a9f29c1f81c231222d6d22b008a934f098da0`  
		Last Modified: Wed, 28 Jan 2026 19:28:43 GMT  
		Size: 73.0 KB (72998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc81147378a1658de2fd29357540650193f896dadaf6a76230cd73a92c76208`  
		Last Modified: Wed, 28 Jan 2026 19:28:42 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d2ff02fcb0f6ca8f35c1c6d5a71cfe39c5b014c0d036a1859c24abcd1529fb`  
		Last Modified: Wed, 28 Jan 2026 19:28:43 GMT  
		Size: 275.2 KB (275214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e069df4875ea88c1f25121bb76790b15bc5525c1eb55319146216953d266df`  
		Last Modified: Wed, 28 Jan 2026 19:28:42 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72725064588a690a5b5ea2d12b07fa8f1501004d8d48b4ce36fa5c8894521f63`  
		Last Modified: Wed, 28 Jan 2026 19:29:43 GMT  
		Size: 617.7 MB (617701159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d7a9d272729090b1e02660ceb63a415adda74867ab41e5ce57210e3f3072bb`  
		Last Modified: Wed, 28 Jan 2026 19:28:41 GMT  
		Size: 86.7 KB (86661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1743a79cd79ad6b3fca51d72062170dc5f01a4271e417641f41212612a60f1c9`  
		Last Modified: Wed, 28 Jan 2026 19:28:41 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443a7a1e5c74898a4cb0f90c58a7d8303d6af5fa2f25f5a7fb98495d13a63ce7`  
		Last Modified: Wed, 28 Jan 2026 19:28:41 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829acdc30ac314c8591c820f13841afcb5675d44fbd65614bdbccdb251c138f`  
		Last Modified: Wed, 28 Jan 2026 19:28:41 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
