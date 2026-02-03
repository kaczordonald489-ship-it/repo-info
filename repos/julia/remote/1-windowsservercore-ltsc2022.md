## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:7ddf59d3cd244b2f09d9c83b105af36a1a8be861849a4fb7aee0066e8e928005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull julia@sha256:00d5df777995908220afc68ffbbf6fede7f62509353dba9f2b55e5b5fc7d8775
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2223114224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51809c009065e8dd01c949d043974bae4949cd07c6fb79b945ea4ba2a855a67`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:54:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:54:44 GMT
ENV JULIA_VERSION=1.12.4
# Tue, 13 Jan 2026 22:54:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.4-win64.exe
# Tue, 13 Jan 2026 22:54:45 GMT
ENV JULIA_SHA256=6b0e030497bd1abc0c12054105e70f0c5600f312be1dadd728d9b6624f9f8940
# Tue, 13 Jan 2026 22:59:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 22:59:33 GMT
CMD ["julia"]
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
	-	`sha256:c6b26cfcc8005482a695d92d8a8d40b0d82eefb4b1d5b354a25239b22e55768d`  
		Last Modified: Tue, 13 Jan 2026 22:59:43 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2241af51a7e56595a48e7051008a309b34fe1e74c4c8c932f12291cbdacacd`  
		Last Modified: Tue, 13 Jan 2026 22:59:42 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e6b6019050029db0da94e57b834dbe82f230f7b771b3e75aee90981b059ce7`  
		Last Modified: Tue, 13 Jan 2026 22:59:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b8cbdb95ad25a747da650aa70d50539531b343338f5bfb5873700776ee5a28`  
		Last Modified: Tue, 13 Jan 2026 23:00:38 GMT  
		Size: 387.4 MB (387448537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c15c2c0dc8a081766847b9c6fb6a1e23b2d1c40cbcf5d107ebae7e7b03af1f3`  
		Last Modified: Tue, 13 Jan 2026 22:59:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
