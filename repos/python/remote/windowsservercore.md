## `python:windowsservercore`

```console
$ docker pull python@sha256:a8ffda0b6fdf26e6610bb9f79fed0d21f5f166a1d88db7cb5e7a75fdf6c16a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `python:windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull python@sha256:fb33fab7dcd79665b6d66890bbbf59ffee1ad6e2098c23777a09ba44e4d3cafb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556688523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e678ad4ee2c3f6fc02c7a0a91aa869f567be44243d8871fdc4ddf6545d454ff2`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:53:11 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 13 Jan 2026 22:53:12 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 13 Jan 2026 22:53:13 GMT
ENV PYTHON_SHA256=9db919cefe30a0051658c600a9912acb0cd2b872aaf35842c9ec2bf401efa848
# Tue, 13 Jan 2026 22:54:02 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 22:54:03 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4c348082658f8a5ab278a6856dfa04fa2a0bb282804f2a57c36436a6688e78`  
		Last Modified: Tue, 13 Jan 2026 22:54:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7406e948e74291cdc5905b66f33026f1ad4de3e9480650c627fc1f6b4d2497`  
		Last Modified: Tue, 13 Jan 2026 22:54:09 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a9bbd5a9a7ccac63082093a7ec5833b388af4dd276a46a5a9fc4b83c1fa23`  
		Last Modified: Tue, 13 Jan 2026 22:54:09 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b5338ec1f2fb294bb5ab6f8422587814fd49b59f1e971d96595182b03f163b`  
		Last Modified: Tue, 13 Jan 2026 22:54:09 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09b3ced76e049cd23a977f60ab2e553df2cf0030ca556474076910ea1c68e6c`  
		Last Modified: Tue, 13 Jan 2026 22:54:15 GMT  
		Size: 60.9 MB (60921665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cf9876fd6e51157ded13cccea948367966f638ef559198342a82406ad08702`  
		Last Modified: Tue, 13 Jan 2026 22:54:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull python@sha256:e0f64f57d689848c17e62a8aab3f2eb0408b4067ea55e87a3f8cfd553b517d67
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896611089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901dd1e74bd316de5daf29486c05179a097ab368a527430e1230f7ec58223f69`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:53:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:53:32 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 13 Jan 2026 23:12:32 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 13 Jan 2026 23:12:32 GMT
ENV PYTHON_SHA256=9db919cefe30a0051658c600a9912acb0cd2b872aaf35842c9ec2bf401efa848
# Tue, 13 Jan 2026 23:13:20 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:13:21 GMT
CMD ["python"]
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
	-	`sha256:2b66bcc5dc6d3aaa7c66e1e850b7913643ad68c20c1b5e2f0a0f33bc0b2abc19`  
		Last Modified: Tue, 13 Jan 2026 22:55:09 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4c7a2c73fbb702a7634e591a8deffb401988837f04b065770a17cdd6eb5f57`  
		Last Modified: Tue, 13 Jan 2026 22:55:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5de4e88f071073922fa3cadd4835f4e12a9bd94e18c7f841ec7a724a73a9f5e`  
		Last Modified: Tue, 13 Jan 2026 23:13:27 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dd83fa0cf30718e5b9fae5a8ceadc74aa91fa7a9f56f3b292752aa90010f14`  
		Last Modified: Tue, 13 Jan 2026 23:13:27 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b46e72ea394959370b557dc126eed00cf920910d311268c79281f18b6d6f557`  
		Last Modified: Tue, 13 Jan 2026 23:13:33 GMT  
		Size: 60.9 MB (60945328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4efc477f332b9523229810f82131c13b8aea792db5a920bf731cb4e0ed0f952`  
		Last Modified: Tue, 13 Jan 2026 23:13:27 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
