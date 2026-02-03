## `mongo:windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:c54dbd91bc89cf52801070a15667f6bf8cf10d2282665a4cb6a4e77b98a31b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `mongo:windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull mongo@sha256:1676059fd323be60849af220a71a0db149ea8aecfef4f6ce2544a97db2725f8e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2651721087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5335a3e6564e25cc343a2fc6fad7abf3e45ef9a644592f0646e2b3e0df9d550b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 28 Jan 2026 19:00:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 28 Jan 2026 19:00:22 GMT
ENV MONGO_VERSION=8.2.4
# Wed, 28 Jan 2026 19:00:23 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.4-signed.msi
# Wed, 28 Jan 2026 19:00:25 GMT
ENV MONGO_DOWNLOAD_SHA256=f8a7d1f49890ea91842d7eface71ff789a2e797fbd225ba31d3b65a4c878603e
# Wed, 28 Jan 2026 19:06:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 28 Jan 2026 19:06:38 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 28 Jan 2026 19:06:39 GMT
EXPOSE 27017
# Wed, 28 Jan 2026 19:06:40 GMT
CMD ["mongod" "--bind_ip_all"]
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
	-	`sha256:463ab9bfe56c2e9d2d3d44b25195d169f9711260d3b4a879439fe93bb1095cd4`  
		Last Modified: Wed, 28 Jan 2026 19:06:46 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec5ae53ef72313c0fb49c34b02a9918b027f4931fec4770b53382e6b5c9be3`  
		Last Modified: Wed, 28 Jan 2026 19:06:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab1c9d139d270aa46dafd2cdcb29dda37038d230daf1496a4ab5e8bf087ed22`  
		Last Modified: Wed, 28 Jan 2026 19:06:46 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c700b1bd57dc3e7d1285b7863e3367061065d883aba7ea92799c5f3ae6a881df`  
		Last Modified: Wed, 28 Jan 2026 19:06:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13fb072183face6f1e128eb488322cf98dce3315dc6db179568cf3e39ae0fb6d`  
		Last Modified: Wed, 28 Jan 2026 19:08:04 GMT  
		Size: 816.1 MB (816052765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d2d5a66924a5df39f36420c58b0d3dee745c6419e372391c635a4af2cebf73`  
		Last Modified: Wed, 28 Jan 2026 19:06:45 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2172cf867119eddf2a4a1bd61de98da8bfd8822e39d83e7c05226582fc76c4`  
		Last Modified: Wed, 28 Jan 2026 19:06:44 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8a823447dc089db4d16fae5338d7f42338147e7c9c69a8bde01b4ea15a3064`  
		Last Modified: Wed, 28 Jan 2026 19:06:44 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
