## `hylang:python3.13-windowsservercore`

```console
$ docker pull hylang@sha256:1ee5f5247d84b6acf82dadea8c5af517a1c48836035bdd2d74dde48e6a7eb360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `hylang:python3.13-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull hylang@sha256:19e191efd937b16019f972ac765063db7550aec09f6bb56e54b60806d5a039bd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3302641581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a606d3a2d18a95218aacbeb9706414018f2f598f7e35c2b9c418225fc164a120`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:27:59 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 11 Nov 2025 19:27:59 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 11 Nov 2025 19:27:59 GMT
ENV PYTHON_SHA256=200ddff856bbff949d2cc1be42e8807c07538abd6b6966d5113a094cf628c5c5
# Tue, 11 Nov 2025 19:28:35 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:28:36 GMT
CMD ["python"]
# Thu, 20 Nov 2025 19:43:04 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:43:05 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:43:56 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 20 Nov 2025 19:43:57 GMT
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
	-	`sha256:be9f07b1dfc8cfffe7adad4b99c34fdda9b3fc97e420f709121bbaab91813acd`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab975a82477a44cd9717da308b1ef3a69e270cd0d669c7d0838af2a7a0981d2`  
		Last Modified: Tue, 11 Nov 2025 19:28:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954d1bcc9d03905361dd9d691a2961cb3d386be3bf6d2bd2711d16aa454097c4`  
		Last Modified: Tue, 11 Nov 2025 19:28:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e671a052e90e79409ef01516ab73e20b423def3ffd2365897914fe4d48892f18`  
		Last Modified: Tue, 11 Nov 2025 19:28:54 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d648c6b8d9c0da5e7d35dd5a40eef1a7932641e85614aa877beb2358c3d825`  
		Last Modified: Tue, 11 Nov 2025 19:29:10 GMT  
		Size: 58.7 MB (58684320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016bb192f0905ca80ab485621c99db90c499446bbeca55f7dbfc5fd0328845de`  
		Last Modified: Tue, 11 Nov 2025 19:28:54 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3d67ccab880b55a034fb431dfaac9b0c5d52916b7f3f2ffbfbc181e5ee725a`  
		Last Modified: Thu, 20 Nov 2025 19:44:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b029ea43114bd708dcb930c67a3c407b13b2f777c51fa191eda75c0b633085b`  
		Last Modified: Thu, 20 Nov 2025 19:44:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db1ee592d69ab4a2947e27011b9dfa2309b598b0363f2632454c3b7e0ebc370`  
		Last Modified: Thu, 20 Nov 2025 19:44:10 GMT  
		Size: 8.5 MB (8491039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca10c4d7d9e449e6ad40df2f8b5bad93527aac0ab10e22883b073003ab96d42`  
		Last Modified: Thu, 20 Nov 2025 19:44:09 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.13-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull hylang@sha256:2c3cd35a3d6cfda8dd7c31a02505835e3117806e78de455f5dae8f992edd07b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1837227532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd6627003acefca267abd6ecd167b14bfb1ba18bf4173cf29faa2eff6cd1c00`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:28:10 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 11 Nov 2025 19:29:23 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 11 Nov 2025 19:29:23 GMT
ENV PYTHON_SHA256=200ddff856bbff949d2cc1be42e8807c07538abd6b6966d5113a094cf628c5c5
# Tue, 11 Nov 2025 19:30:10 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:30:10 GMT
CMD ["python"]
# Thu, 20 Nov 2025 19:42:59 GMT
ENV HY_VERSION=1.1.0
# Thu, 20 Nov 2025 19:43:01 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 20 Nov 2025 19:44:14 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 20 Nov 2025 19:44:15 GMT
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
	-	`sha256:4b29d7d66d7f4ac3f8cb78bc5a6de4c14e194db152f15ca5ab40a5eff0480557`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73838e40e1af50d120f4cf2803f8806778c9e9cb15dea399e878d946d8cdebe1`  
		Last Modified: Tue, 11 Nov 2025 19:29:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147ed04d813eb6f3c62d5e92135e080d3d3f9dce9f81677b1b28bb897fa4d67`  
		Last Modified: Tue, 11 Nov 2025 19:30:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca8fc1a94602ac2d78bac4c005d611a158fe3e03f95a8d58cc526c3aec78bd2`  
		Last Modified: Tue, 11 Nov 2025 19:30:33 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6279a00ead958027dae89528a16a4df27f1bacc61cd65248bcb7fc3363446b48`  
		Last Modified: Tue, 11 Nov 2025 19:30:38 GMT  
		Size: 58.8 MB (58799899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162de7bf198c74b1dc61454d3c69c0c31a8ce59d974c525e2d3b8467af5be9d1`  
		Last Modified: Tue, 11 Nov 2025 19:30:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b52d95b93256487a00160270fecbdc4d5c4a0d16594f8c219ee64408e8fd731`  
		Last Modified: Thu, 20 Nov 2025 19:44:28 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8955eb0ebd65d582ad01fc1189a25531ef07a8acc53d9bcedb580f5f1067a5fd`  
		Last Modified: Thu, 20 Nov 2025 19:44:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744e48c08729c390c93b70d05744572e30608ba0e7588178e4cc67b8a897dc3b`  
		Last Modified: Thu, 20 Nov 2025 19:44:29 GMT  
		Size: 8.5 MB (8455601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7270565f20e90dd02d4cde367755a892b9780ed8357131b04a1745ffbfc846`  
		Last Modified: Thu, 20 Nov 2025 19:44:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
