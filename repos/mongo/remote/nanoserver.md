## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:34c29b71ee88fa5a31f2e592cf77f49a3136cabfcc5fae60fe3b9fca18c91610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `mongo:nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull mongo@sha256:2405bcebdce678b00deb4f68ff026cb4dc3f23164d93d32a1370254cebd47da0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **942.0 MB (941996981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a596eb03b795bdfa535d70a03ed8acebf5a4e0be43595f79a7e9c768507494`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 28 Jan 2026 19:27:23 GMT
SHELL [cmd /S /C]
# Wed, 28 Jan 2026 19:27:25 GMT
USER ContainerAdministrator
# Wed, 28 Jan 2026 19:27:33 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 28 Jan 2026 19:27:34 GMT
USER ContainerUser
# Wed, 28 Jan 2026 19:27:35 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Wed, 28 Jan 2026 19:27:37 GMT
ENV MONGO_VERSION=8.2.4
# Wed, 28 Jan 2026 19:28:16 GMT
COPY dir:ce889a16f493f8dcee624064e673d3d28c30425d3566dc48d6adcd33c125da77 in C:\mongodb 
# Wed, 28 Jan 2026 19:28:37 GMT
RUN mongod --version
# Wed, 28 Jan 2026 19:28:38 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 28 Jan 2026 19:28:38 GMT
EXPOSE 27017
# Wed, 28 Jan 2026 19:28:39 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a428e9257b6ab8453119a8ecfbe733274d158e7a42acb4390a865524a342cb`  
		Last Modified: Wed, 28 Jan 2026 19:28:47 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8198807972cae0b6d14012aeb5f8bbc4cb6a3108fa55b4b4d20a805a752f38eb`  
		Last Modified: Wed, 28 Jan 2026 19:28:47 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4c9202d18d91e4531e653b1bc6937650d1f6241fd8d49e79ee2991768eda`  
		Last Modified: Wed, 28 Jan 2026 19:28:45 GMT  
		Size: 82.7 KB (82723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a92330e722c8b7fce6e57b1701345620c09b1cc53a8725d249ec3cf0c1083a`  
		Last Modified: Wed, 28 Jan 2026 19:28:45 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647fcb3e5e55fa448f440711e399b442ca6b0988ab6ebf122fc81aae428e91c7`  
		Last Modified: Wed, 28 Jan 2026 19:28:45 GMT  
		Size: 275.2 KB (275190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbd5b2a23992b4d7461cccaa38f34861ed435441adc94ed87c32ee3f0ca0b2f`  
		Last Modified: Wed, 28 Jan 2026 19:28:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4ed85a1d27a3b46f3456b4ad3cf53894239ad1bf8fc87b8d2f1eeb07be2b8d`  
		Last Modified: Wed, 28 Jan 2026 19:30:03 GMT  
		Size: 814.8 MB (814838000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb8460972ad2556f92a0121d9aedfefef5dc870c257113e5d89f66bd478d617`  
		Last Modified: Wed, 28 Jan 2026 19:28:43 GMT  
		Size: 96.7 KB (96748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d177dd826f454ba3d27a426fa4bc12ef90f556621948a5ba1b1cd2585c8057`  
		Last Modified: Wed, 28 Jan 2026 19:28:43 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33ba569f26c043938f69102354f12eb79d7f9e4a175ce714ece21380fe7d07d`  
		Last Modified: Wed, 28 Jan 2026 19:28:43 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1785c2ff54c351478908be2e9c29df58b68afd07ab3e4eb752aa8bcc183c2a27`  
		Last Modified: Wed, 28 Jan 2026 19:28:43 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
