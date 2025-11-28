## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:cd92840e72d3d648241784b2473ba92d0e5d7a7986f43f3a9509f15752cf755d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

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
