## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:557c2a4bc76b6024bcba75bd9c4ff91f32bba60a776f5187c2e7cbd4d7c0e159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `mongo:7-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull mongo@sha256:2cd38739db1c6069440b18d70f81650ab5ee4951737f6a16e965664bc0f6ca3b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3853638574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403aabd9521a2b3fd242550ed488f519d0b7d52a8681dfe3dab247dce79c1be8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Thu, 20 Nov 2025 00:00:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Nov 2025 00:00:20 GMT
ENV MONGO_VERSION=7.0.26
# Thu, 20 Nov 2025 00:00:21 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.26-signed.msi
# Thu, 20 Nov 2025 00:00:22 GMT
ENV MONGO_DOWNLOAD_SHA256=034920396de70b2fdf95071bbe06f15a237ac74c2a125640e0afba68bf9d73a2
# Thu, 20 Nov 2025 00:02:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 20 Nov 2025 00:02:55 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 20 Nov 2025 00:02:56 GMT
EXPOSE 27017
# Thu, 20 Nov 2025 00:02:56 GMT
CMD ["mongod" "--bind_ip_all"]
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
	-	`sha256:1ecd189a98be2e46ecdb4a5ff48b938e8760dc3c4f1a3d4f8cb6dc5cbef55edb`  
		Last Modified: Thu, 20 Nov 2025 00:24:17 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f9b1f25a5f1916d5a78d527e6cc059b2dffc28724c032344d7bab07643d82f`  
		Last Modified: Thu, 20 Nov 2025 00:24:17 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debe28055eeaef9314b0bc96d471df7b11c766794d396fe7e0b5d4ab27aa274f`  
		Last Modified: Thu, 20 Nov 2025 00:24:17 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a583b5f0e25db8c0cf10b43f4d6e45e8dcbc849356f1af8112530e9c68a4b5`  
		Last Modified: Thu, 20 Nov 2025 00:24:17 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0d45b0f746f0fb1f99dd5a774577f279f3fa21ccd301fdc5083eb26c87bf06`  
		Last Modified: Thu, 20 Nov 2025 02:08:26 GMT  
		Size: 618.2 MB (618173675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6201521c467faee969f0e313cedb23af601c33ecc732e35e6d60695a2c56a62`  
		Last Modified: Thu, 20 Nov 2025 00:24:17 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a781852d6591b6d75edf83af94dce098de9300ac339cea7f3683e64cdb9c86c`  
		Last Modified: Thu, 20 Nov 2025 00:24:17 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aed6a7c253c5a42ce6ad903471310b646d6f9e8c6e4a3829c62a0a12161e26`  
		Last Modified: Thu, 20 Nov 2025 00:24:17 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull mongo@sha256:f480150ab3c242b746210f56e77ab4970d32e900e7cd2c6d53ce93e9f326211e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2388299238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b15b07a746565a19aa3969391c8c833c85fac2f7bef756d91b0f9acb5fbff90`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 20 Nov 2025 00:02:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Nov 2025 00:02:50 GMT
ENV MONGO_VERSION=7.0.26
# Thu, 20 Nov 2025 00:02:52 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.26-signed.msi
# Thu, 20 Nov 2025 00:02:53 GMT
ENV MONGO_DOWNLOAD_SHA256=034920396de70b2fdf95071bbe06f15a237ac74c2a125640e0afba68bf9d73a2
# Thu, 20 Nov 2025 00:11:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 20 Nov 2025 00:11:08 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 20 Nov 2025 00:11:10 GMT
EXPOSE 27017
# Thu, 20 Nov 2025 00:11:12 GMT
CMD ["mongod" "--bind_ip_all"]
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
	-	`sha256:ac7f56443bcbb98aa15175376dca79bb1d2e12f947812e031aa5c7faf0352175`  
		Last Modified: Thu, 20 Nov 2025 00:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887712845346de340c3f69632370b635f3ec285919579dd17d4dae8d4d98fd6b`  
		Last Modified: Thu, 20 Nov 2025 00:24:47 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c25e50fc8a67e48861be2eec05f48905df59ded7df1f37216dc405c52d5d810`  
		Last Modified: Thu, 20 Nov 2025 00:24:47 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c26abc72ea236eb09fcf08972931ffaec68e6f05e8504fc4a7d920cdec066e0`  
		Last Modified: Thu, 20 Nov 2025 00:24:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98a73d93ff7cd7f5a9a2c2fc27ba67dc4ff7051d12fb256c91a297cf8b4b0b2`  
		Last Modified: Thu, 20 Nov 2025 01:15:44 GMT  
		Size: 618.3 MB (618328517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565edfaf0a6aae96e5557e25e591b4f0093c5c7e6ff2abd84fc0f92d3ea644b9`  
		Last Modified: Thu, 20 Nov 2025 00:24:47 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194371ef76ceb33a19891b71bd2f8e077fa4ced85dfc7a8c30fa3f9e5b0a482e`  
		Last Modified: Thu, 20 Nov 2025 00:24:47 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f08d68607f960b46f4ff953da633ef9773124f7512f273d325a796672a79a71`  
		Last Modified: Thu, 20 Nov 2025 00:24:47 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
