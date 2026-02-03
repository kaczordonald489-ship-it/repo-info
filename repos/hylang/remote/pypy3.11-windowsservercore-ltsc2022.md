## `hylang:pypy3.11-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:c2221c1ccc8780f8026df72687350d8f85f34efd9d87363583a3a919ebd92c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `hylang:pypy3.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull hylang@sha256:38ae998d113556f54c5efebd61d0b2e43b9626ebd4788de1a1d10579bf53672b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1891098369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0652ad8522bca333246be72ce814e810cfcbc613b89c78bab9a3dbd4f2406e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:54:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:11:56 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:12:05 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:12:06 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 13 Jan 2026 23:12:42 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:12:42 GMT
CMD ["pypy"]
# Wed, 14 Jan 2026 22:03:34 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 22:03:35 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 22:04:28 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 Jan 2026 22:04:29 GMT
CMD ["hy"]
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
	-	`sha256:2f08760e06519dd29e9a52391dac11e5952f68046c79c4bdea23cb54196c9897`  
		Last Modified: Tue, 13 Jan 2026 22:59:44 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27312a9f7bf9397d877f52fa65cc2a37431648e3defc89630bd9b9ffe4828206`  
		Last Modified: Tue, 13 Jan 2026 23:12:47 GMT  
		Size: 486.1 KB (486093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35263fd2f63c29340963f82cb88e73ee7e4cc3e5c91c06dd678d444d1b88f0d9`  
		Last Modified: Tue, 13 Jan 2026 23:12:49 GMT  
		Size: 15.5 MB (15528198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ec3d1f7c2afb3e7f80fe185d930a03fd99911031e8521616817190b1e4228c`  
		Last Modified: Tue, 13 Jan 2026 23:12:47 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47515769f526c0f3652f708639ecaa989b6e48dd5eb642bb48dfd548f5af7d7`  
		Last Modified: Tue, 13 Jan 2026 23:12:51 GMT  
		Size: 30.7 MB (30664641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a30789d9bbf357e1d8e8941e629b59f6266af5c945c580c412b034567a046b3`  
		Last Modified: Tue, 13 Jan 2026 23:12:47 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c613227aa92be1086d56c3212b415b0d519ca5a46bcbd7bec43f3b9fea7074`  
		Last Modified: Wed, 14 Jan 2026 22:04:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a5c36dbda7b4062faf5af7aa7f4afd62529dd1672f7265695a045724154d42`  
		Last Modified: Wed, 14 Jan 2026 22:04:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12a219e1ef69a8eeb4b27fd400d6f7ec23f1f0faaaa8ac92b14e1e09be319a6`  
		Last Modified: Wed, 14 Jan 2026 22:04:35 GMT  
		Size: 8.8 MB (8752447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f9fe6cddf0512da31eba94cb858503c09f0a11f79a9bab19e3aa3a4a1395ec`  
		Last Modified: Wed, 14 Jan 2026 22:04:34 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
