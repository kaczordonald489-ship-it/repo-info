## `openjdk:26-ea-25-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:9b11a6c8a20d3e242ae6bab77f192e9740788c34ec00920c0d82a696f8edbbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `openjdk:26-ea-25-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull openjdk@sha256:9b2ca02d6e30c4b08c5070b2483c53f9d1218f76612a1fa9b78619d46966cef0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459860585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b22297880d9384247261f5d1b47245558ac2c9add9332e335cea411dfd2366`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Mon, 24 Nov 2025 21:55:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:38:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:38:18 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 24 Nov 2025 22:38:23 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:38:23 GMT
ENV JAVA_VERSION=26-ea+25
# Mon, 24 Nov 2025 22:38:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_windows-x64_bin.zip
# Mon, 24 Nov 2025 22:38:24 GMT
ENV JAVA_SHA256=4fcd9d7036d75a47ff7d0ace16d6b27dec02549a4d110860c2ff45c1ac790029
# Mon, 24 Nov 2025 22:38:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:38:45 GMT
CMD ["jshell"]
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
	-	`sha256:2fbc05ed4b88c9841b3c2e452d7b00e7b0a7c04e26a7cb1757ba50deeefc6513`  
		Last Modified: Mon, 24 Nov 2025 22:17:06 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac64a4be516e9e4bc89d8ac2927a4a4cd2aea973ed39755417d4da91689d609e`  
		Last Modified: Mon, 24 Nov 2025 22:39:13 GMT  
		Size: 379.7 KB (379719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a691710a9513fcc77127c82a79d333e80daf6667883776a6150346777848ad4`  
		Last Modified: Mon, 24 Nov 2025 22:39:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b755e7219dfff1eeff92f410105405fd3788e31e540c70e5a795d7fb8fb261`  
		Last Modified: Mon, 24 Nov 2025 22:39:14 GMT  
		Size: 355.4 KB (355435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7dcc351fee94909607672b64b1f83f18e3d4a75fac8e67258a67f2cbfd5528`  
		Last Modified: Mon, 24 Nov 2025 22:39:14 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c382ed0649e191618ad91d29204dcad32f4eaf495aaf43888b2f201580703041`  
		Last Modified: Mon, 24 Nov 2025 22:39:14 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78901018f590f374d6823eca55dde9253d32e465d6323807c73e8cf5095fbb5`  
		Last Modified: Mon, 24 Nov 2025 22:39:17 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bba285b49ec22dafee3bb10372f43f0bb8b015f442de56fac3ea5e6b8d52f3`  
		Last Modified: Mon, 24 Nov 2025 23:14:18 GMT  
		Size: 223.7 MB (223661705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a85e9504d5f8928344d81ad2ac7b3d705026712aa50e599ca0317d0a79108f6`  
		Last Modified: Mon, 24 Nov 2025 22:39:15 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
