## `hylang:pypy3.11-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:7cf32893f4b2b003af0d554c9a96abe41cddda6aa576b50941bd4932c9160694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `hylang:pypy3.11-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull hylang@sha256:13d913e72399713f3bc01abea4b4986d231f488e429a992b97ce121b705f5744
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1551192951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc10342980d50751ff96cb47b46eccbb37a087e1a6ff4ae1d5352ec40723477b`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:01:06 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:01:15 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:01:15 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 13 Jan 2026 23:01:50 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:01:52 GMT
CMD ["pypy"]
# Wed, 14 Jan 2026 22:03:56 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 22:03:57 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 22:05:07 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 Jan 2026 22:05:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efa37c091ab5ec4869e2ab85fd61db9ffc02e5ee0f087000562c7b74d0ace95`  
		Last Modified: Tue, 13 Jan 2026 22:54:55 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811f9956f15897d4609b84a7a598d1b6af09c6095cffb78e1eb3bd7cca1dfb89`  
		Last Modified: Tue, 13 Jan 2026 23:01:56 GMT  
		Size: 383.8 KB (383812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a237c7c700c6a65c03052392f2bca636915dea66276acda9f090e4f6708b532b`  
		Last Modified: Tue, 13 Jan 2026 23:01:58 GMT  
		Size: 15.6 MB (15560688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cf56576cf098e66e238684e1d61a9bfd768a06d5c5e0ac7d7addbf8411633b`  
		Last Modified: Tue, 13 Jan 2026 23:01:56 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50569a64d765a7719bc9198243edd1db5e9cadd60d603c4f6607f08aa6fc5b72`  
		Last Modified: Tue, 13 Jan 2026 23:02:00 GMT  
		Size: 30.7 MB (30693687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f699ce7062aa7938a793d08a8845e1869af2ff8402c5336f6df0cf2f161cc2`  
		Last Modified: Tue, 13 Jan 2026 23:01:56 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f25fcde554117b23b433b580406795ae989e447e738bee07df39de68766d6ad`  
		Last Modified: Wed, 14 Jan 2026 22:05:12 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7046cbefdba9fcf1c9568e8d16ad7660e1cd9610ecd97ade65b3908caa6289`  
		Last Modified: Wed, 14 Jan 2026 22:05:12 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903bdf01a771d51c073c6227eedab7f15d00ad4eea1de4895d581a3bf9a0359f`  
		Last Modified: Wed, 14 Jan 2026 22:05:14 GMT  
		Size: 8.8 MB (8786569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd57a5ba11baf90c0ab1dfc4ae5dd694d71b75356e45d469e6cf87d32889e99c`  
		Last Modified: Wed, 14 Jan 2026 22:05:12 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
