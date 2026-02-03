## `openjdk:27-ea-7-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:123072c6ad28701615cac280183cbc242de3e94ca8a7f7bbde2ce7ecf535a531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `openjdk:27-ea-7-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:04b4ee1854449509107060ac10ca1e4ce6e930ed3e5d3213128344b9631301b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1721249567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bc5c9c393fe7a7d75d285c7768d8d7ba56da87149163d2e4ac1af7af7b64eb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Fri, 30 Jan 2026 23:42:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 30 Jan 2026 23:43:10 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:43:12 GMT
ENV JAVA_HOME=C:\openjdk-27
# Fri, 30 Jan 2026 23:43:18 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:43:18 GMT
ENV JAVA_VERSION=27-ea+7
# Fri, 30 Jan 2026 23:43:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_windows-x64_bin.zip
# Fri, 30 Jan 2026 23:43:20 GMT
ENV JAVA_SHA256=5940fbffa36c927e8b186d5bcdaa99e332aebc16b642bb272e05e5cce059d4a3
# Fri, 30 Jan 2026 23:44:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:44:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d6c59707690a6c1c49a677c44b0642f22ab69aaa1916fe7e12b7baddc52a0c`  
		Last Modified: Fri, 30 Jan 2026 23:44:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615f012ffbc34e881b32b35ca9bc9df3053c0ba7d8478ea5c40f617063c0ddfb`  
		Last Modified: Fri, 30 Jan 2026 23:44:09 GMT  
		Size: 415.7 KB (415697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5f643c58f50967ebbf73acebe4c139fc44125b612de9619b5f1b6ab89c51dc`  
		Last Modified: Fri, 30 Jan 2026 23:44:09 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a39ec7825ed4337f1a9bf404a4bacddfcfc3bc8a0b02456b945b60f47455ff`  
		Last Modified: Fri, 30 Jan 2026 23:44:09 GMT  
		Size: 401.1 KB (401066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247210eb0ff1470790b27a79720b14089e0269fbe70cce383a9a656d6378705b`  
		Last Modified: Fri, 30 Jan 2026 23:44:07 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b25d9c6d0dfcf013769af9bfc48276225b4422540b829ca0694445fe3a0fa0`  
		Last Modified: Fri, 30 Jan 2026 23:44:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0fe790cb78a7ae24ac1b46c35f8caa88f7daf48def5409f4300d0caf4aaeb78`  
		Last Modified: Fri, 30 Jan 2026 23:44:07 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d74e25ae1676d8df44fc1c2f24ae0269a99fbe096258335196228893e1bd530`  
		Last Modified: Fri, 30 Jan 2026 23:44:22 GMT  
		Size: 224.7 MB (224664649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50313fdc2885c8b8a09008abfda283a919d8408f9e00963ee39df212ae217698`  
		Last Modified: Fri, 30 Jan 2026 23:44:07 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
