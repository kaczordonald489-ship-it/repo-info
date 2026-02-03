## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:25233863901918872bf17b591083767ce1faeefc993a94cfc1b17bf516664a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull nats@sha256:85686b0c19dc2cf95ddcbfe8a4cd19da2d2cd35f0ec50058780642e0d2a2dade
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1843326026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350724f2d07f8320ce38c7c37d1836d561c501d51842a5a2294c05c286633391`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 27 Jan 2026 21:02:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 27 Jan 2026 21:02:19 GMT
ENV NATS_DOCKERIZED=1
# Tue, 27 Jan 2026 21:02:19 GMT
ENV NATS_SERVER=2.12.4
# Tue, 27 Jan 2026 21:02:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.4
# Tue, 27 Jan 2026 21:02:21 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.4/nats-server-v2.12.4-windows-amd64.zip
# Tue, 27 Jan 2026 21:02:22 GMT
ENV NATS_SERVER_SHASUM=99efb643ef399299ed5736e4fc7220551e8450fe9351adc3c2f678b5737815f5
# Tue, 27 Jan 2026 21:02:45 GMT
RUN Set-PSDebug -Trace 2
# Tue, 27 Jan 2026 21:03:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 27 Jan 2026 21:03:06 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 27 Jan 2026 21:03:06 GMT
EXPOSE 4222 6222 8222
# Tue, 27 Jan 2026 21:03:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 27 Jan 2026 21:03:07 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:7163b7e4ed4603533d1fda3d54c2c9bd222c3767dfe7b8def9f7dd49fab9d9ca`  
		Last Modified: Tue, 27 Jan 2026 21:03:15 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28002105b30a506ea71f81d135734fc2290d5709ceec675fa94dac86606e50b`  
		Last Modified: Tue, 27 Jan 2026 21:03:15 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e811110b9e834a35200f080893776ff6a0942f8d8b81ead09ef8b6d5cca4448`  
		Last Modified: Tue, 27 Jan 2026 21:03:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c95878a999406539b61a9cf2a1c93993151a5810c7cf62df0695f1824b7e556`  
		Last Modified: Tue, 27 Jan 2026 21:03:13 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f6b1127b820a407c09f03cba32195298037d7a4e62bf7fbe4e48aa6e0e68dc`  
		Last Modified: Tue, 27 Jan 2026 21:03:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cab9070ade4519b37ca4c5850d7caa0c9014f700a23e873d5c116c289dc975`  
		Last Modified: Tue, 27 Jan 2026 21:03:13 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee1c1bf73c67953ec9edc4463565cbf1d314ba3eaf3072f756261df4c83ef68`  
		Last Modified: Tue, 27 Jan 2026 21:03:13 GMT  
		Size: 507.3 KB (507329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9395ebafa33fffb1174b8933764abb540194af5c3c67197362e7abf5968c3e45`  
		Last Modified: Tue, 27 Jan 2026 21:03:13 GMT  
		Size: 7.1 MB (7145810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4af0169026bc8454cb3a35c7c962cb9420af4960c1ddd87670450b3fd289fe`  
		Last Modified: Tue, 27 Jan 2026 21:03:12 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc6e11b6268f0921828579f88e05cc6e97e36577c0a0ecd486f15ad7457a78e`  
		Last Modified: Tue, 27 Jan 2026 21:03:12 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf677c818932196a82eede373147a57f807e76fc3253349075985e67b2cca95b`  
		Last Modified: Tue, 27 Jan 2026 21:03:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72db2ac852987031e3dcf5336480ce4aab8ee8287719d1790630ab68849ee79`  
		Last Modified: Tue, 27 Jan 2026 21:03:12 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
