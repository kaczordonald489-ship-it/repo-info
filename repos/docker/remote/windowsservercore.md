## `docker:windowsservercore`

```console
$ docker pull docker@sha256:3823b5757f67d3bb596d43a9fe6c756ae8413951f74f6e95ca0eb2956d8cf03a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `docker:windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:f94341834aa25a76061fcd4a2fa288da1066e0e3709974283823f1474bd6453c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301910125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13053b5fb9fbc32bb0a3dbec0eb61098926ca9e0804e8ace52e9c557a6ce6169`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 25 Nov 2025 00:53:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Nov 2025 00:54:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Nov 2025 00:54:02 GMT
ENV DOCKER_VERSION=29.0.4
# Tue, 25 Nov 2025 00:54:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.4.zip
# Tue, 25 Nov 2025 00:54:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Nov 2025 00:54:13 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 25 Nov 2025 00:54:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 25 Nov 2025 00:54:14 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 25 Nov 2025 00:54:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Nov 2025 00:54:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 25 Nov 2025 00:54:23 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 25 Nov 2025 00:54:23 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 25 Nov 2025 00:54:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a90421c799539c586927180cd90f218f1977cd1f4807ed21a13ffb8e25e7ae5`  
		Last Modified: Tue, 25 Nov 2025 01:03:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f875cf12996d4cd618dedb2a86b6f0472a3502b59e5a36e9c00927d64686133`  
		Last Modified: Tue, 25 Nov 2025 01:03:02 GMT  
		Size: 386.7 KB (386683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac8e49b923546f6ab91ba84330cf76f6023c19ff18f3a2f9461ba69ff6609e6`  
		Last Modified: Tue, 25 Nov 2025 01:03:02 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670ac296f167cf75005c2ba7486650bb71616a177155bc6d915c74afb3f80f18`  
		Last Modified: Tue, 25 Nov 2025 01:03:02 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377766ea852ac304913c984e3ed52c632f569f8f0b28d67455772210b9a3033c`  
		Last Modified: Tue, 25 Nov 2025 01:03:05 GMT  
		Size: 19.4 MB (19433542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a074c9ade90673efb21567c9aeb574d8ac757d6800b875d51ab2dd65a8f36aee`  
		Last Modified: Tue, 25 Nov 2025 01:03:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1de6b633c1737f8cee5df6ef0392961f635880bc86aae522535fe62f509634f`  
		Last Modified: Tue, 25 Nov 2025 01:03:03 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83da9ad61f4c14c40bcb6bdccae6408d2e00653311464c4376e1d071b113acf`  
		Last Modified: Tue, 25 Nov 2025 01:03:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d22d2f8e3a1eeb7cd44e028e1c09f20c6aeccfdd39fc3c811a8a16d261cfd4`  
		Last Modified: Tue, 25 Nov 2025 03:08:23 GMT  
		Size: 23.9 MB (23936262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1f5a3462b8759056dde195c4de992b23d5ec88b221175e6898780464ee31ff`  
		Last Modified: Tue, 25 Nov 2025 01:03:04 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055e3b11c2f87e1cd971233f1114e392cb6ff1453263ce7b1dd5b5628e77092f`  
		Last Modified: Tue, 25 Nov 2025 01:02:57 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5f59c93342ed01c562f791c7616a1b9808e339a64507dd26f8f4ed5d39b9c9`  
		Last Modified: Tue, 25 Nov 2025 01:02:58 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda27f5dab3f2ce4f971e76a8a4dc99c7732771abc233e2a1c0fe07cdeaeec16`  
		Last Modified: Tue, 25 Nov 2025 01:03:00 GMT  
		Size: 22.7 MB (22686111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:ff88740ec03f1317d371143f8c5966d5b2603541ebabfef9c2d45459c09f4548
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1836558690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8feda5db3d1c77b8ec5d6578900b2c9403b314e38015b2e877cf9272467ee7b0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 25 Nov 2025 00:55:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Nov 2025 00:56:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Nov 2025 00:56:42 GMT
ENV DOCKER_VERSION=29.0.4
# Tue, 25 Nov 2025 00:56:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.4.zip
# Tue, 25 Nov 2025 00:57:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Nov 2025 00:57:03 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 25 Nov 2025 00:57:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 25 Nov 2025 00:57:06 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 25 Nov 2025 00:57:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Nov 2025 00:57:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 25 Nov 2025 00:57:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 25 Nov 2025 00:57:30 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 25 Nov 2025 00:57:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5d37bddde33b3f5435ad9be54cc7a73aa6d4a3994eac62a107667db733de46`  
		Last Modified: Tue, 25 Nov 2025 01:10:49 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1006742d9b54b486423d87bc146bbb40e0182001308bc28e88cf61c7bb556b06`  
		Last Modified: Tue, 25 Nov 2025 01:10:49 GMT  
		Size: 518.5 KB (518528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5890b1b74a5241cb2bb8db68a4aa1e38953b916651aa163222deff1b34f1c0cb`  
		Last Modified: Tue, 25 Nov 2025 01:10:49 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fc26aa6d4f658e0c1d01ede574fea9cea92f252b8c85d3ef31a62044d394d3`  
		Last Modified: Tue, 25 Nov 2025 01:10:49 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ab40b799f9588b2869f495cfc653308c4aaeca86435736a3991063e0f7e93c`  
		Last Modified: Tue, 25 Nov 2025 01:10:51 GMT  
		Size: 19.4 MB (19436566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031c16635d881e5ac63576a18a34b3a825a01177e3b53fa9f10ca866b2cb2413`  
		Last Modified: Tue, 25 Nov 2025 01:10:49 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9039ed7e725ad646e3ad536233b1e8cdaa32cf09e442fdf2c0cdc3f52f0a19`  
		Last Modified: Tue, 25 Nov 2025 01:10:50 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50df5e66a667bbcef231d14d27a204faf0305213a960293ddcffb209520e364`  
		Last Modified: Tue, 25 Nov 2025 01:10:53 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47e928b64133e31d3ab2da124239e4144f380b1db35fc661ed87157ce5bef33`  
		Last Modified: Tue, 25 Nov 2025 01:10:59 GMT  
		Size: 23.9 MB (23940214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427ae450abc2adfef786ca340b43d32d50f02ef85f024e55632144a663e5e847`  
		Last Modified: Tue, 25 Nov 2025 01:10:53 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e99988d5ca7574eef1f8c395bfe48cb240e3afd91d766856e8d765cdde1a12`  
		Last Modified: Tue, 25 Nov 2025 01:10:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f401eb82b39ee0266ae76eab594e8e2395cc4869a5be47da2e33faa5ab7c981`  
		Last Modified: Tue, 25 Nov 2025 01:10:54 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6a79f92917edac5035c32eac18caf19660b78676df385f2a4bf28aba97f434`  
		Last Modified: Tue, 25 Nov 2025 05:26:28 GMT  
		Size: 22.7 MB (22690014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
