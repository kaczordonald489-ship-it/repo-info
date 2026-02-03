## `eclipse-temurin:8-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:4a365415c45e66dfc937386373380b0db6955d021f19307af946b496f7130f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:8-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

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
