## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:4f709cae1db898fd1ad6745f38c5e6d8ffec6e83cb8cc00d76f82fbd247675a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
