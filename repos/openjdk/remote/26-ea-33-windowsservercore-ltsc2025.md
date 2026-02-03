## `openjdk:26-ea-33-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:a0d548dec9b702a3255ea3ce5b14bae161c7c8a2448d3bdd56226897e78341e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `openjdk:26-ea-33-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:26729fbb19a4dadc5e6b522ee4595ebabd6dfabb6ce89481ae06c6b9eef7d72f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1720897038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de885a2f00bbf11e302617f7c24851f2eed6f0c135d63adf74b1722fb4a41591`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Fri, 30 Jan 2026 23:39:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 30 Jan 2026 23:39:27 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:39:28 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 30 Jan 2026 23:39:34 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:39:35 GMT
ENV JAVA_VERSION=26-ea+33
# Fri, 30 Jan 2026 23:39:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_windows-x64_bin.zip
# Fri, 30 Jan 2026 23:39:36 GMT
ENV JAVA_SHA256=1613acc47081355dcb54aca5db4a0cc088734861b42bd254657ab88fd50944ec
# Fri, 30 Jan 2026 23:40:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:40:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6d232d985647bac5bb6eb0323db9939978fe35ce0400678ab358bb526cbbf6`  
		Last Modified: Fri, 30 Jan 2026 23:40:22 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b8329748e243b493f5f5841dcae9b09c85e7ed14c65a0e712c34f7fb05072d`  
		Last Modified: Fri, 30 Jan 2026 23:40:23 GMT  
		Size: 416.9 KB (416880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7706ba72d33ad14c1e782a84ded0723ca55fccda4e202a29137e634a99469292`  
		Last Modified: Fri, 30 Jan 2026 23:40:22 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cb2831b370174c7dd2acdaf6674ebebf64c87ce135b0bf93f0be2ad538de9b`  
		Last Modified: Fri, 30 Jan 2026 23:40:23 GMT  
		Size: 401.0 KB (401039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0250baab51d53441f7e2fd1ce28b784c9d54a751e17fef8a73af06783510a1cc`  
		Last Modified: Fri, 30 Jan 2026 23:40:21 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c81b233b494a09ad1fc903642ffb0fd16b1920990675e33121899fb876b9d5`  
		Last Modified: Fri, 30 Jan 2026 23:40:21 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd73c7832edd93b2f1eed1f16b8df0712688604d326a2b5271494ee9df802a4`  
		Last Modified: Fri, 30 Jan 2026 23:40:21 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc74dd3f905a5624dbc9e410ba273338c8db410e063d54a81b0d7a4150bc496`  
		Last Modified: Fri, 30 Jan 2026 23:40:36 GMT  
		Size: 224.3 MB (224310912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcfba226fa310cccf26760ee72738e8d5d8ef91dd20d7a6862c7cd61e2be1543`  
		Last Modified: Fri, 30 Jan 2026 23:40:21 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
