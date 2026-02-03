## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:810c2a27c504c76b45b024bf5d7a4368f2303ab2d1685f4c239b22ef24645816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull mongo@sha256:a14f7dca76757b2cb2f910300f9575a30a770f6e7faacab06111ebc90f606773
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454548069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cfd98f811772b49c22af3527a43c50302bd69027fb906dbe0f4ca7e3b35002`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 28 Jan 2026 19:02:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 28 Jan 2026 19:02:57 GMT
ENV MONGO_VERSION=7.0.29
# Wed, 28 Jan 2026 19:02:58 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.29-signed.msi
# Wed, 28 Jan 2026 19:02:59 GMT
ENV MONGO_DOWNLOAD_SHA256=3bbf7db85f94cdf291c79dd14bc1d0f16c31b276249007d8320c6d83e2c882ab
# Wed, 28 Jan 2026 19:07:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 28 Jan 2026 19:07:58 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 28 Jan 2026 19:07:59 GMT
EXPOSE 27017
# Wed, 28 Jan 2026 19:08:00 GMT
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
	-	`sha256:1497ed98c351aaba5e69e7428410b1b0fcf6e03c45915151606c81ff53f492b3`  
		Last Modified: Wed, 28 Jan 2026 19:08:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5400f744f312439129f2e47cea1852f2fa58984705ec4960fbeec69493c756c4`  
		Last Modified: Wed, 28 Jan 2026 19:08:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f579dc752049a431d4466fba9ae3e307e679959d9a866f3710e0d74f607ef400`  
		Last Modified: Wed, 28 Jan 2026 19:08:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58a46fcd41d263aff8a98fc6a1e2fc9df85dd5f1fb477e061ee5a61c23e0380`  
		Last Modified: Wed, 28 Jan 2026 19:08:04 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3ace11018ab9eac1b430ba3377c2613b2a1fa041aa7c0d9c4fc5d74510b9a9`  
		Last Modified: Wed, 28 Jan 2026 19:09:06 GMT  
		Size: 618.9 MB (618879736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b267adcbf4eaeba55c898da84acfc95dff921a67c909da892fb31d6426f73a`  
		Last Modified: Wed, 28 Jan 2026 19:08:04 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499d0719abf353a6e9ec313f8b4f0c4c64387916545e34f4e40a1450076fb89e`  
		Last Modified: Wed, 28 Jan 2026 19:08:04 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14cdd89c2e695b91fa93a1d902317ee2cc2a1d40e22678700eca1c5ca6d1c9a`  
		Last Modified: Wed, 28 Jan 2026 19:08:04 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
