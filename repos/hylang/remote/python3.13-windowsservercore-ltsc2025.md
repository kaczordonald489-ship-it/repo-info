## `hylang:python3.13-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:ed0e92a1ef77739514e6c86fc3dbc14a23f5d2ae15d1e62057a7c1f2dd1b386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `hylang:python3.13-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull hylang@sha256:217dc5dfec27ed92720a8d7f5836c919c769f09443d3b8996be71e134188fcec
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1563094828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a057fcaddfb24d49ccb9ac042598ad1995189b0603451f85f7cab99af087a1`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:01:24 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 13 Jan 2026 23:01:24 GMT
ENV PYTHON_VERSION=3.13.11
# Tue, 13 Jan 2026 23:01:25 GMT
ENV PYTHON_SHA256=30d4654b3eac7ddfdf2682db4c8dcb490f3055f4f33c6906d6b828f680152101
# Tue, 13 Jan 2026 23:02:03 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:02:04 GMT
CMD ["python"]
# Wed, 14 Jan 2026 22:02:33 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 22:02:34 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 22:03:36 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 Jan 2026 22:03:38 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e80c7a7f1e619446ad0a75155ab3ad1a8da7712a1614331cebc9b4d2f8665b8`  
		Last Modified: Tue, 13 Jan 2026 22:55:08 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a3f9db7bb6367c3f39b3002ca5e40d5262cc734f61dc1be2e0543b728f5a5b`  
		Last Modified: Tue, 13 Jan 2026 23:02:08 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c964053a13707fe67dc8b53aa5b6c9ac064cdba1a11e572ae98e3cf5f4dd543`  
		Last Modified: Tue, 13 Jan 2026 23:02:08 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca01222e389a3dd818e7ba7cfeb41d6b4974eee525e705f638be6f9f2c2ca08`  
		Last Modified: Tue, 13 Jan 2026 23:02:08 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4e337a8bb209adb29e364cd3209832f16408e79d5382615ac0f398107291af`  
		Last Modified: Tue, 13 Jan 2026 23:02:14 GMT  
		Size: 58.8 MB (58826548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b630af33bded8b9b71370129a5588bfa980fc851f7be2391d2c70d3be8f6dd8a`  
		Last Modified: Tue, 13 Jan 2026 23:02:08 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dbe76e04ae9d804cdf39acb1c297a5e60412dbbca1b4014999d74e588f006d`  
		Last Modified: Wed, 14 Jan 2026 22:03:43 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8153469da7af40c43eef4ee2551e260b2de13265b29f1884a64a63e7b66445de`  
		Last Modified: Wed, 14 Jan 2026 22:03:42 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b7939998381cc55059e5092dbdc6d3327bc81d925b4a4add9c4c48df839bd9`  
		Last Modified: Wed, 14 Jan 2026 22:03:44 GMT  
		Size: 8.5 MB (8497427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f0ce0d91761014d14708c2494d4e9473801177bac71f74ec813554e841d5a8`  
		Last Modified: Wed, 14 Jan 2026 22:03:42 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
