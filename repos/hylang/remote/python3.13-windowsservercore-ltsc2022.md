## `hylang:python3.13-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:46884d39100f214a19855c9dcb4ff8cbda775f24d79b6ffba292d962b3db4af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `hylang:python3.13-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull hylang@sha256:ba7fedfaf32fc2048fd8135a65ebfc1d7edd219ab9c0b068b8787378675c3d72
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902917294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5c112144daa9990098fd9e360c784d0483d3cc4b90434d4a29bb711f898709`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:53:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:12:37 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 13 Jan 2026 23:12:38 GMT
ENV PYTHON_VERSION=3.13.11
# Tue, 13 Jan 2026 23:12:38 GMT
ENV PYTHON_SHA256=30d4654b3eac7ddfdf2682db4c8dcb490f3055f4f33c6906d6b828f680152101
# Tue, 13 Jan 2026 23:13:21 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:13:22 GMT
CMD ["python"]
# Wed, 14 Jan 2026 22:02:51 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 22:02:53 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 22:04:05 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 Jan 2026 22:04:06 GMT
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
	-	`sha256:9f681901ae8b8270ef4ad40879b419cd45d092d5d347a675266218039d5b88a0`  
		Last Modified: Tue, 13 Jan 2026 22:54:23 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592680e3698d8f38797a3d48148155e0f3ed6fd84fe59b55aa983306e8e7430e`  
		Last Modified: Tue, 13 Jan 2026 23:13:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98725bbfac9e58f5e9f204d42ddeac79b826f28e2cba15876058fb24804ba2b`  
		Last Modified: Tue, 13 Jan 2026 23:13:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576db8afdbb7e2ca01068a1839bba93677d4059bba9b7e0dc0c2017fbff3927d`  
		Last Modified: Tue, 13 Jan 2026 23:13:27 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2409f31cd7c69f59ef9c0897b436fcbeb4c7c5c7b455fb494ff4c2b804b2f1d7`  
		Last Modified: Tue, 13 Jan 2026 23:13:34 GMT  
		Size: 58.9 MB (58852398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9acb5c3d35d8880f2106ce6ea2d85b131872f1c02b0f89eabd16b383be1e80`  
		Last Modified: Tue, 13 Jan 2026 23:13:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed48a7d8f39a36ed94b630e9e9a02e101b9f9cfd92f9821d30a1adfb435bd393`  
		Last Modified: Wed, 14 Jan 2026 22:04:10 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e048196329adf3748a416e6773d1a9ce4e893a4e33e920f24d71f20e8fc2f6ed`  
		Last Modified: Wed, 14 Jan 2026 22:04:10 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ff3bf51f8dae23e294c453f7a62d6c1fc6922d971458e5679aa7c202199e3`  
		Last Modified: Wed, 14 Jan 2026 22:04:12 GMT  
		Size: 8.4 MB (8395302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a40633d402c5ab01c15c05685a2d580824c71cb07a35d9d3ace6dc348090d46`  
		Last Modified: Wed, 14 Jan 2026 22:04:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
