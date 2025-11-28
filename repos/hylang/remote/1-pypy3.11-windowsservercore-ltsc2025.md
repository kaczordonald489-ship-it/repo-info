## `hylang:1-pypy3.11-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:6ba299bf7c47e49143d4e24cfde007f60dec2fc76cf5a0024c6b2c75d9817177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `hylang:1-pypy3.11-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull hylang@sha256:2117ef1239da2e8e10bc068251d78a0b181446d24274c277e8c4f5b69da3c0a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3290863173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bc71b90ea4ba0f084a9903e063d35667844706c41778542f27d0ffe0529b00`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:27:14 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:27:23 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:27:23 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 11 Nov 2025 19:28:06 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:28:07 GMT
CMD ["pypy"]
# Thu, 20 Nov 2025 19:44:30 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:44:31 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:45:30 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 20 Nov 2025 19:45:30 GMT
CMD ["hy"]
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
	-	`sha256:8285ac56aa8dfc6927624dc14fae2bfc7d25d53da7342eb169af1b4433e08d02`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3946b48a3a8e69231ebe93558658226c6e53f281d568fd74b5e2fda8d16fc17`  
		Last Modified: Tue, 11 Nov 2025 19:28:24 GMT  
		Size: 358.9 KB (358917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ce9f865a1fbb63ea6ed95fd2f3ea88bbf38551e91515451f0636e5b698aae1`  
		Last Modified: Tue, 11 Nov 2025 19:28:25 GMT  
		Size: 15.5 MB (15529573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f628114af2eda98472aa5ec10fdc837f8ec8a924a4c0306bb2b28686529694cb`  
		Last Modified: Tue, 11 Nov 2025 19:28:24 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6b8c56e76c031cbd1e553f2eb5d1e8af9cb75b0b1d6046d6c87d0b6daa2c95`  
		Last Modified: Tue, 11 Nov 2025 19:28:27 GMT  
		Size: 30.7 MB (30670943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fbf78de2bbdb6d3dd6712af6b8568aa09ef6135c1639945a7e3c8ac78b4739`  
		Last Modified: Tue, 11 Nov 2025 19:28:24 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51553d7ef7b6784ddc172b974527503ebabc753edc57bf3361523c780584aa5`  
		Last Modified: Thu, 20 Nov 2025 19:45:42 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f44ddd8e5847c59fe60403e4b67008529261dd26ef36456416f412cb053a04`  
		Last Modified: Thu, 20 Nov 2025 19:45:42 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea642060bf8e61750450bf45ba4d0ede87d1eda3807058a426b2e0411ab548db`  
		Last Modified: Thu, 20 Nov 2025 19:45:43 GMT  
		Size: 8.8 MB (8840144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84de9dcbad826db5b329fe417c0cbc2bbcc82be7edf6353f2b5b29ca70ec7e2e`  
		Last Modified: Thu, 20 Nov 2025 19:45:42 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
