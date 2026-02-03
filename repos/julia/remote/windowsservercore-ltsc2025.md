## `julia:windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:44945c1cff47fef36afdd539dc2574e248191ed57c660d93cc4801219b35aa6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `julia:windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull julia@sha256:fcd0285fddab8bdc3b054cfc14e939a1ccddf7306c4f3167a3696d817b58ca85
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883095023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5c7fc606a32c721d34898b8ddca5d4e33c464da1b1aa4b0e2f6c4c7ca6fbd1`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:53:09 GMT
ENV JULIA_VERSION=1.12.4
# Tue, 13 Jan 2026 22:53:10 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.4-win64.exe
# Tue, 13 Jan 2026 22:53:10 GMT
ENV JULIA_SHA256=6b0e030497bd1abc0c12054105e70f0c5600f312be1dadd728d9b6624f9f8940
# Tue, 13 Jan 2026 22:54:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 22:54:47 GMT
CMD ["julia"]
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
	-	`sha256:e5a1488697ba85070835f53d3cd154bbc050994a1cd297f5782c52184219d86a`  
		Last Modified: Tue, 13 Jan 2026 22:54:53 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de821615b5f6a494b7b818718de824575bdda26534295178a9a24347d9358c51`  
		Last Modified: Tue, 13 Jan 2026 22:54:53 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4002cd59ca0fccc8693aab1e10bbdc358126e85f51e0529812e88dacde9e48`  
		Last Modified: Tue, 13 Jan 2026 22:54:53 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd8784976f50bb57446482deb15ebe275e3eb2be9a55d3e4912b11716ed1566`  
		Last Modified: Tue, 13 Jan 2026 22:55:51 GMT  
		Size: 387.3 MB (387328092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3351d80cdd5893bdbd8521d70fabb9eab94e61867aecba7685dbb5a042274a40`  
		Last Modified: Tue, 13 Jan 2026 22:54:53 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
