## `eclipse-temurin:8u472-b08-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:bd5d58a92251661be5b0d007b4b67f2d49d26e964c7a4615ee07ec6c3f2b9273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:8u472-b08-jdk-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:d1cd6f137de9869ce4d7c4bd714834ba7f00a2ca9acda612f71db17953fd9878
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1687469079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb6898c3c321df8bfa55dd9fa0d2411c5414fc6bc605a2c9158fd33d16a3ed8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:53:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 13 Jan 2026 22:53:45 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u472b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u472b08.msi ;     Write-Host ('Verifying sha256 (810c04469e75c2f1cf83091e9dc78497b84e48ad21269291d9b7ff59b5cbb404) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '810c04469e75c2f1cf83091e9dc78497b84e48ad21269291d9b7ff59b5cbb404') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 13 Jan 2026 22:53:52 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9be5a805d67347b826e7569fea58f855566235f29986ebdf211b524b6b781a5`  
		Last Modified: Tue, 13 Jan 2026 22:53:56 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d428ab0336b6bf8900f80a6e26899ee6eb49f01d3f4141f365abfe3422069112`  
		Last Modified: Tue, 13 Jan 2026 22:53:56 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001a4e052374d197111ef6a084c69585816659ba51db61f7123814dfd122aba0`  
		Last Modified: Tue, 13 Jan 2026 22:54:06 GMT  
		Size: 191.3 MB (191318873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ba90bd2e4327421e8fbc8f0a33a8557ee5bbfb22278e7115d38b40669db908`  
		Last Modified: Tue, 13 Jan 2026 22:53:56 GMT  
		Size: 387.3 KB (387318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u472-b08-jdk-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:2f2dc58147a9877ecde8644961b1e3c0f26f838af038ec8b8fc04dfbea61a4d0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2027431971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20d70b6c3405688cfb1dda7685744e2e7821c3235755f132249fa30a53e5c15`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:53:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:02:38 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 13 Jan 2026 23:03:21 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u472b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u472b08.msi ;     Write-Host ('Verifying sha256 (810c04469e75c2f1cf83091e9dc78497b84e48ad21269291d9b7ff59b5cbb404) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '810c04469e75c2f1cf83091e9dc78497b84e48ad21269291d9b7ff59b5cbb404') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 13 Jan 2026 23:03:29 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:9f681901ae8b8270ef4ad40879b419cd45d092d5d347a675266218039d5b88a0`  
		Last Modified: Tue, 13 Jan 2026 22:54:23 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4d1a1aa85d833ade8dd71fa494a67b3bb4969cf8c8546f796d47606dda5f0f`  
		Last Modified: Tue, 13 Jan 2026 23:03:33 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb43e31caa3cc01d3b27eb9b9844defe46b0f16295fbf27c330b607121a183a0`  
		Last Modified: Tue, 13 Jan 2026 23:03:45 GMT  
		Size: 191.4 MB (191416894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa7e325941a8d7e7d22195b70d060ace9a8f1c878352577e8ce9020f282f19a`  
		Last Modified: Tue, 13 Jan 2026 23:03:34 GMT  
		Size: 353.3 KB (353288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
