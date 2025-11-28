## `hylang:1-python3.14-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:072a174dc2dfe3f17c0707735463e6b2d4117a7968a12684869e1c37bc0a87c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `hylang:1-python3.14-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull hylang@sha256:660d0da4e3eb2986040fcdb131a81d5c2e739dc0905e54a71ab6f9988e26b8d3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1839303779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55f0a85d698a5649933094c9673338d7bf3d327d496c8c6c883c2b43c26f9cd`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:29:16 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 11 Nov 2025 19:29:17 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 11 Nov 2025 19:29:17 GMT
ENV PYTHON_SHA256=52ceb249f65009d936e6504f97cce42870c11358cb6e48825e893f54e11620aa
# Tue, 11 Nov 2025 19:29:58 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:29:59 GMT
CMD ["python"]
# Thu, 20 Nov 2025 19:40:18 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:40:19 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:41:18 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 20 Nov 2025 19:41:19 GMT
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
	-	`sha256:5c47b7190b9ffc37d6229c244251af53d022884b4b7dab60e0c54d9354c4adc5`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418bbdf766763bf02cd3dee58d3a6fc0159716525580f2c308cb278ee448e10b`  
		Last Modified: Tue, 11 Nov 2025 19:30:17 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1848a7309b90d8a9ccbe5193fd9a77bb3d0fb68a31905530f9c9137c7ecf33a7`  
		Last Modified: Tue, 11 Nov 2025 19:30:17 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3979c420f3c2129c3114593b1af9690d977830f6fda7ba407040103dc96d74`  
		Last Modified: Tue, 11 Nov 2025 19:30:17 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d228f7f5fdfc142ea4d0800ca21b14d89d4712e187bb1d6bdf833abc5eb630`  
		Last Modified: Tue, 11 Nov 2025 19:30:24 GMT  
		Size: 60.9 MB (60853956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706456b291493cedef846bdac9237a021e4ab410c6d8cf47c1036728d6629ce`  
		Last Modified: Tue, 11 Nov 2025 19:30:17 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d314a37b37e619bca38f573ea894e8058bb26af9c93766dfbb5b1278fc89877`  
		Last Modified: Thu, 20 Nov 2025 19:41:35 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ed64bbc63466ea0f51543cbd39dffc91ca6d2c61b5dd363f572e8d1d92ddbf`  
		Last Modified: Thu, 20 Nov 2025 19:41:35 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f2c5af84b45ea9bc9ae109b8e07bed3ee919decaf42e8ba8665caaa3adbb90`  
		Last Modified: Thu, 20 Nov 2025 19:41:37 GMT  
		Size: 8.5 MB (8477770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2ce8f503f98256c31f8a00f0673f06e318e76c700a873bf692e65909661af8`  
		Last Modified: Thu, 20 Nov 2025 19:41:35 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
