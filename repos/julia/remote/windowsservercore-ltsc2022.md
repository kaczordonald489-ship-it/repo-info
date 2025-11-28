## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:543d2532e513d8a1a42648f9dc78c42b9ce1a8a2d68676b185fbd36c75ec2dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:b19a0355653e5bcf77bd963149b5b0d5daee9d33495c665554f25360d61575fd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156065454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff53739fcaa993184fc9260a3e1520a8d2b789ada88a284fc7383f281ff09cb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Mon, 24 Nov 2025 21:54:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:35:00 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:39:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:39:17 GMT
CMD ["julia"]
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
	-	`sha256:4aad132d44253f5455efa330566900fe031331917e6f95f4055d2072ead42290`  
		Last Modified: Mon, 24 Nov 2025 22:10:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c75b500a462b83a39b4fcad48acc61a24d9e5de87a8720e03bdf25e13feb4ba`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b738f0f264c3ca50e1f4bb1b056a9c9b262ce66bc0b3c7f5a9ac92ee37cb5`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc7adf8835efbc83d4960db10242b44009e37c8653b8b5081d79d18e21bfcfa`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d3eb5dffd1df8b0325f75b73663fb4dcfe07865e4523235c38b62f88a0389f`  
		Last Modified: Tue, 25 Nov 2025 00:03:05 GMT  
		Size: 386.1 MB (386097304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d1c145a6db855fb1b3f59e92beac660753ab469d40ddf7e32f5efe7907521`  
		Last Modified: Mon, 24 Nov 2025 22:40:36 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
