## `openjdk:26-ea-25-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:3b72e6d70604a981d1a333b42ce8178520233761b74eba2f1884d7f7aef56c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `openjdk:26-ea-25-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull openjdk@sha256:e3426c7231edd7ea0b9276595f3f992ed94662193c265e490ceef9d7ec74c539
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1994467761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32c72efba602ec93c0f5b98c7ac005e4f1c667b2c61473432ce011360c7912e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Mon, 24 Nov 2025 21:54:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:40:50 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:40:51 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 24 Nov 2025 22:40:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:40:58 GMT
ENV JAVA_VERSION=26-ea+25
# Mon, 24 Nov 2025 22:41:00 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_windows-x64_bin.zip
# Mon, 24 Nov 2025 22:41:01 GMT
ENV JAVA_SHA256=4fcd9d7036d75a47ff7d0ace16d6b27dec02549a4d110860c2ff45c1ac790029
# Mon, 24 Nov 2025 22:42:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:42:06 GMT
CMD ["jshell"]
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
	-	`sha256:4aad132d44253f5455efa330566900fe031331917e6f95f4055d2072ead42290`  
		Last Modified: Mon, 24 Nov 2025 22:10:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d5690eb8763a7986fb72e4d44ad6466abb11aa2dbf4ae609110cd3f3e252f0`  
		Last Modified: Mon, 24 Nov 2025 22:42:34 GMT  
		Size: 501.1 KB (501084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeeac7142afbb261a27c3da0069adb5f0669bddcfaaf61af41040ad7ba4516cc`  
		Last Modified: Mon, 24 Nov 2025 22:42:34 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f795b633508338331cc4560847afa2d110240926ec5f2208c8ca370e8ad324a`  
		Last Modified: Mon, 24 Nov 2025 22:42:34 GMT  
		Size: 348.8 KB (348804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e70b091e29d137dcd01b5a7fc4b268ded5c04567edb4b9acf650cf19dec6bf`  
		Last Modified: Mon, 24 Nov 2025 22:42:34 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eeed71bf66533b999d80389cd77682a503532c7576baffd2578eb56a04e9a42`  
		Last Modified: Mon, 24 Nov 2025 22:42:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b682b53972d652083baa76920bc5cb9ebdfa23aa5074c5078886b2ff66ee960`  
		Last Modified: Mon, 24 Nov 2025 22:42:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b750ab81cfc6790bdf5e5fe8155e9abf6255ee3a3f97f3f3ffeefafd56ef4716`  
		Last Modified: Mon, 24 Nov 2025 23:12:10 GMT  
		Size: 223.6 MB (223648459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456195b5f41f15e5e81b1861f6457744104171c36c41c525fdcc91fe57128d39`  
		Last Modified: Mon, 24 Nov 2025 22:42:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
