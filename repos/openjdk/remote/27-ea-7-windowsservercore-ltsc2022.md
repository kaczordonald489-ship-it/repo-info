## `openjdk:27-ea-7-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:8948e3ac3935ddb86788e791f17fb467d7115418049a4ee4b2228e3a62686d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `openjdk:27-ea-7-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:f75ac09d075ea464f8bd56aa32a591d883984aae443d9cdc8eef38c614f6b1a7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2061181213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e12837eec8cc945b8db6b19b12b4a3a326314b735cbf86ecf355a73d11c7a42`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Fri, 30 Jan 2026 23:45:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 30 Jan 2026 23:46:36 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:46:36 GMT
ENV JAVA_HOME=C:\openjdk-27
# Fri, 30 Jan 2026 23:46:43 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:46:44 GMT
ENV JAVA_VERSION=27-ea+7
# Fri, 30 Jan 2026 23:46:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_windows-x64_bin.zip
# Fri, 30 Jan 2026 23:46:45 GMT
ENV JAVA_SHA256=5940fbffa36c927e8b186d5bcdaa99e332aebc16b642bb272e05e5cce059d4a3
# Fri, 30 Jan 2026 23:48:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:48:09 GMT
CMD ["jshell"]
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
	-	`sha256:88b32703314e87d13fb9507dba672f55c597c0b0f0179fb8711740c684336383`  
		Last Modified: Fri, 30 Jan 2026 23:48:17 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74657ea3c21ea7ed28c4a53d17444a15b8b8020b198de93f990fc51990c6717a`  
		Last Modified: Fri, 30 Jan 2026 23:48:18 GMT  
		Size: 511.3 KB (511273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14c46c88484b39244aea83d59c79f9dc44b01920196e360912a5e5633d76d10`  
		Last Modified: Fri, 30 Jan 2026 23:48:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484de465f93498ba5cf672381d09327b181bdf1b9d0795ec928937d3fa973438`  
		Last Modified: Fri, 30 Jan 2026 23:48:18 GMT  
		Size: 358.1 KB (358108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae551e0fb968703be7257e964fbf1d0996487d1230473cb8e717c575c7a6575`  
		Last Modified: Fri, 30 Jan 2026 23:48:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545b2fe9a896f56e14dbdaae2c1682f98429042d562d498a2a43a52d96434bae`  
		Last Modified: Fri, 30 Jan 2026 23:48:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4568237bab4a097967d0a5c5964ed77ee7214109d8d03231033f256b5d2b8c81`  
		Last Modified: Fri, 30 Jan 2026 23:48:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f126f009209b32000ccd9fc76d8ac5c8c061d1454d9ab95de51018b806060e`  
		Last Modified: Fri, 30 Jan 2026 23:48:32 GMT  
		Size: 224.6 MB (224644851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071db900bbb3ccd27222b7e0fcff4333c1a4fb6d71203010cc720e25df16909e`  
		Last Modified: Fri, 30 Jan 2026 23:48:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
