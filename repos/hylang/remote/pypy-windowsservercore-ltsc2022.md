## `hylang:pypy-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:fe8ffa316522c76bb35e703549e2d68d5981b810729183b298d866b30d76793e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `hylang:pypy-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull hylang@sha256:df129f6d66851e1c2a1891c8af3744975af058b0769e6d4097289225ed31635c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1825488411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de3ae1bceeb233fe69db5c032d1690a72765a0a90ab61847d9270042ab9e382`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:28:14 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:28:24 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:28:25 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 11 Nov 2025 19:29:03 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:29:03 GMT
CMD ["pypy"]
# Thu, 20 Nov 2025 19:42:32 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:42:32 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:43:28 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 20 Nov 2025 19:43:28 GMT
CMD ["hy"]
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
	-	`sha256:442760c8d26f9c34d441d655bfed0213774e9ee1491b0a9d451ba3951353bd99`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d80c29a0842a34f8c512d7c99d3ec6a50bc0da8baa6234281af26593606c756`  
		Last Modified: Tue, 11 Nov 2025 19:29:21 GMT  
		Size: 487.9 KB (487935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c736ff67c1729815898cab1f0ce89d5cc7b38c9928a3fea417d6ad98d67de66`  
		Last Modified: Tue, 11 Nov 2025 19:29:22 GMT  
		Size: 15.5 MB (15529843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3ced131808af1789c74f41256a2ab4d8e46d6013f7e28cfdb0bb2633dc4b8f`  
		Last Modified: Tue, 11 Nov 2025 19:29:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9685518121426f07f379bea6b65794018f09c0c737b442db076d9db44acc80c1`  
		Last Modified: Tue, 11 Nov 2025 19:29:25 GMT  
		Size: 30.7 MB (30672291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea916fe33d8d87609385929be1936f8ca3934e23cec287a7b788a7fc5badf25`  
		Last Modified: Tue, 11 Nov 2025 19:29:21 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a788febd4647e53bca83411bacc17e560fbd0e54ed9b76a66879585bf81c30da`  
		Last Modified: Thu, 20 Nov 2025 19:43:40 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a675be48786f954763d72d3a128348086b736ba6950c7385816eac1388858a2c`  
		Last Modified: Thu, 20 Nov 2025 19:43:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde02c42db77134fc27b0ba615febed876dbc24b01f8c36f50c5dc0af14eda9e`  
		Last Modified: Thu, 20 Nov 2025 19:43:41 GMT  
		Size: 8.8 MB (8829029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2be63de21791d6f9c102c011e9fe8497ee4e74fa5db9710254ed31a90cddd40`  
		Last Modified: Thu, 20 Nov 2025 19:43:40 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
