## `mongo:8-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:4cda32852f1df4063c34d06163a56e1b76a9952301caad236d56f87f48d847e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `mongo:8-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull mongo@sha256:885898ea952b08bfa12beb4c90511eddb64730343f1c164ed14351fc4ecbd5a9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311750359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ea64da91af98b52526d741b5e96e5287ebbb31557fba3c34fbbe375a583c4d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Wed, 28 Jan 2026 18:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 28 Jan 2026 18:58:35 GMT
ENV MONGO_VERSION=8.2.4
# Wed, 28 Jan 2026 18:58:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.4-signed.msi
# Wed, 28 Jan 2026 18:58:36 GMT
ENV MONGO_DOWNLOAD_SHA256=f8a7d1f49890ea91842d7eface71ff789a2e797fbd225ba31d3b65a4c878603e
# Wed, 28 Jan 2026 19:01:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 28 Jan 2026 19:01:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 28 Jan 2026 19:01:23 GMT
EXPOSE 27017
# Wed, 28 Jan 2026 19:01:24 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e8daa8a1404dec4f1e9a3005a32988319fdc5e5fcc909140238e26b3c70230`  
		Last Modified: Wed, 28 Jan 2026 19:01:30 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50cbb425f028c17f8d9a26ac41c19c716f5c5918d7518d2c4303aba86261377`  
		Last Modified: Wed, 28 Jan 2026 19:01:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec9ebddac805fb002aa0e3f4ba846601f2fb446f15d42c865211003946a032c`  
		Last Modified: Wed, 28 Jan 2026 19:01:29 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6cdd26d44185eec53f156a8ec8148d43bc21eb7e443561fcebacf01d8ea536`  
		Last Modified: Wed, 28 Jan 2026 19:01:28 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4daebb594b16e19977462c0a163b3d4e651b0172802afb6731999940a6db5c0e`  
		Last Modified: Wed, 28 Jan 2026 19:02:47 GMT  
		Size: 816.0 MB (815980810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d01b5c045f4676fd6d6d04d308622dca6afe8febf9f3d674e9faa8d823b336`  
		Last Modified: Wed, 28 Jan 2026 19:01:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1800d63e94b9cec5ec1e63f5e16b5362740a49bc702eeb66829e33301fdcf589`  
		Last Modified: Wed, 28 Jan 2026 19:01:28 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bed320bf1a1ae25616896b7ca10a25765357b8c99cb598f8442cf8439e9722`  
		Last Modified: Wed, 28 Jan 2026 19:01:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
