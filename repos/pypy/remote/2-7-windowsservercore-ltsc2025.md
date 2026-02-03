## `pypy:2-7-windowsservercore-ltsc2025`

```console
$ docker pull pypy@sha256:ea9b05df5372e75efae31eb86680c7033ecfd8ae995fa50c93f87b258088e246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `pypy:2-7-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull pypy@sha256:5792c0767c7c2d45b68fa456809ef45ce1a0c59a7d7358869140c5de7203fe44
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1536898373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e642c8358ab420c00591efb8eac4691aa1f3a371672f5d24d25af9f824e2cd1`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:01:15 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 13 Jan 2026 23:01:20 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:01:29 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:01:29 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 13 Jan 2026 23:01:59 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy2.7-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '76d02853601ef8d3c9dd821a9faa84cabf9bc469d6b77797b21ed311b25d5419'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy2.7-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:02:00 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91938e162987eb0675b8773bfe45efb2af9a96d1e9473d3ebd4a447259bcc862`  
		Last Modified: Tue, 13 Jan 2026 22:54:06 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448a3a45fd799f46e214e88d37ed343553b31bcf75c754a91099d6e8a2fcf494`  
		Last Modified: Tue, 13 Jan 2026 23:02:06 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3212cebdf11126969c0a3b19b77d3103be92397b09b834535d41bb9864dc5259`  
		Last Modified: Tue, 13 Jan 2026 23:02:05 GMT  
		Size: 374.4 KB (374388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0708c7c885e1dba0f17fcaadbe4bf5bd442197909bdbecb3aca015dbf25129c8`  
		Last Modified: Tue, 13 Jan 2026 23:02:07 GMT  
		Size: 15.6 MB (15552141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67e53baaaa5a03b4a82f4e164754d8760fb4156c969cea9e7c3835356ffde91`  
		Last Modified: Tue, 13 Jan 2026 23:02:05 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceaa8409a8dbd2e6c4d37b1b38146a5d345522852f9b66fe4389c23457af7194`  
		Last Modified: Tue, 13 Jan 2026 23:02:08 GMT  
		Size: 25.2 MB (25206278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2f47299f9db577742a4eebf283230ebe7e809914dc6374b51d0560d84a23a6`  
		Last Modified: Tue, 13 Jan 2026 23:02:05 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
