## `hylang:1-windowsservercore`

```console
$ docker pull hylang@sha256:253f6e405dd0c3c72018cc05075a688977636cd71e892f48012de34557b7b8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `hylang:1-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull hylang@sha256:20383e22e047c7b7694c02c2e24417acc5a211c672eb401818971139f9b57f03
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1565207689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7873fa233b93c4bdd268747d47985228baeac2b03e02807288527fd9e1421591`
-	Default Command: `["hy"]`
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
# Wed, 14 Jan 2026 22:01:23 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 22:01:25 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 22:02:41 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 Jan 2026 22:02:42 GMT
CMD ["hy"]
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
	-	`sha256:82a467fc3bd09d021362fb78eb43db891079cedd056d7577f15bfaf44a54e0f0`  
		Last Modified: Wed, 14 Jan 2026 22:02:47 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5781bb8d0d0387b62b1957ea49ce1fe8430e37896154262e95caef054ba06cf8`  
		Last Modified: Wed, 14 Jan 2026 22:02:47 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19c997194cd1ab3fbe1bab3bf525049d4ffc3292f69301bf1671b875e56666b`  
		Last Modified: Wed, 14 Jan 2026 22:02:48 GMT  
		Size: 8.5 MB (8515168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d892297e3609879569456bf2b87cfa096a9afe7c307d429b95858fdebbf8f204`  
		Last Modified: Wed, 14 Jan 2026 22:02:47 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull hylang@sha256:55d890637dac89bf278ca3f111ce20f65f73802adee5763754c87246db02ddc6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1905007864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ff29226edb89da4f3c29cee9ee70d2f0d44a8204165882abcc1956fe5b3506`
-	Default Command: `["hy"]`
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
# Wed, 14 Jan 2026 22:01:59 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 22:02:00 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 22:02:53 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 Jan 2026 22:02:54 GMT
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
	-	`sha256:edaf5155b30681cc55be2b4c999f1dd0ba4c28eb838081c33f1d2fd9a1e66e15`  
		Last Modified: Wed, 14 Jan 2026 22:02:58 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b627565233d9397cf50f6af4901c0131cac3e94d57f656150b59b878bc122`  
		Last Modified: Wed, 14 Jan 2026 22:02:58 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8270824e01330f11691cefcbae0d0ee441b3c5d349b2ff989f27e6b06b1467e2`  
		Last Modified: Wed, 14 Jan 2026 22:03:00 GMT  
		Size: 8.4 MB (8392850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658c9a45d8f38f8d522e3bfc13ea09687fa637c118f534fdcdefea522424581d`  
		Last Modified: Wed, 14 Jan 2026 22:02:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
