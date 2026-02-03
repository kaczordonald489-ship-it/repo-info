## `openjdk:26-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:5d7b2cf85310250a581b85a78de0da106c10426738071c4c0ee70e1189de3ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `openjdk:26-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:65c3c46583d86ee7e71d869b007a3a8f8d58766344b310b13d2fb77fc4264f1a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2060828234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf5d89d3e7e8a3ec85b952c5dd3b2fc9226e240560ed8fbf7df510e8600dc3c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Fri, 30 Jan 2026 23:39:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 30 Jan 2026 23:40:36 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:40:36 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 30 Jan 2026 23:40:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:40:43 GMT
ENV JAVA_VERSION=26-ea+33
# Fri, 30 Jan 2026 23:40:44 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_windows-x64_bin.zip
# Fri, 30 Jan 2026 23:40:45 GMT
ENV JAVA_SHA256=1613acc47081355dcb54aca5db4a0cc088734861b42bd254657ab88fd50944ec
# Fri, 30 Jan 2026 23:42:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:42:15 GMT
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
	-	`sha256:5bf12dbbc63ade9ffa2bc8a97522ec0c9b93b94327d9d4d29b884d5562aad768`  
		Last Modified: Fri, 30 Jan 2026 23:42:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ee7c5e9acd94a15471693e7c33250c1f40aefbf482cd02643fa42837823b54`  
		Last Modified: Fri, 30 Jan 2026 23:42:25 GMT  
		Size: 512.6 KB (512605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9f00ae2fa10bcf5329922222393accd763a60505a0ec64762c77a94c47eb78`  
		Last Modified: Fri, 30 Jan 2026 23:42:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566c6287bc76d30a151af0b81f492aa72ba379b10b405776dda15f8650607635`  
		Last Modified: Fri, 30 Jan 2026 23:42:25 GMT  
		Size: 360.4 KB (360395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016069b05e82df74afcb392c6275dc7fc7028e2b5d80cc1989245efdedc6de3d`  
		Last Modified: Fri, 30 Jan 2026 23:42:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d663aea12bc6c12ce098ed928c6a394935463f99431072dba8242a9f792ba23`  
		Last Modified: Fri, 30 Jan 2026 23:42:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e1c2842a2b8b5c68d9d5dda9b03b8444904fdc8217cd5419183e31323bbf88`  
		Last Modified: Fri, 30 Jan 2026 23:42:23 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8445808894c0c536502816e0d02fa3aaf47b40a34dc4c219a44352b9af76c496`  
		Last Modified: Fri, 30 Jan 2026 23:42:39 GMT  
		Size: 224.3 MB (224288220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f628ff06d5628fdbd128982c385f15f8b390733f29b5e7d3ef4608edc1da749d`  
		Last Modified: Fri, 30 Jan 2026 23:42:23 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
