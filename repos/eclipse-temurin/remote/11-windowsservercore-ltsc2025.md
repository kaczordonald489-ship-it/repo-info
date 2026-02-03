## `eclipse-temurin:11-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:d9e11e6e1e709f9981f238109b56bae6fed4e44142fd7893885bfba5500367b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:11-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:586ee95a8c6e316f12071f6bc60526e2508b0f7acea26f87e8e810e68ffb6c81
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1865621517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0277fc28fd8dc0b1ead6e54e09a5c17954f576a951a467ad607f7f58f0e86367`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:55:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:55:03 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 13 Jan 2026 22:55:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.29_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.29_7.msi ;     Write-Host ('Verifying sha256 (219e88a862ccdde521c42d8ebc001cc711279cdef79157b568ec2ae16b3abde0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '219e88a862ccdde521c42d8ebc001cc711279cdef79157b568ec2ae16b3abde0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 13 Jan 2026 22:55:40 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 13 Jan 2026 22:55:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3f1cc7695915e69cb162ef9e41d3fa34b60087e3a381105e07c3c278d5214b`  
		Last Modified: Tue, 13 Jan 2026 22:55:44 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91eca6b98471a0ed28d9428e729d40db2eff15f100a21edb369e66e6140a6ea9`  
		Last Modified: Tue, 13 Jan 2026 22:55:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11d96b786e461512c58a330289ca399b0f1c5a52fb10017657ffa0dc4ad2303`  
		Last Modified: Tue, 13 Jan 2026 22:56:50 GMT  
		Size: 369.5 MB (369471645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a021687c6f6a2d77c9cda8fe69a1deece1b6359d82dc970848851130011ee3`  
		Last Modified: Tue, 13 Jan 2026 22:55:44 GMT  
		Size: 385.7 KB (385679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c345d2767b51a97890fa578a28af3fe9ff89ec23c9fc5e12bab4bcd3a1efcee5`  
		Last Modified: Tue, 13 Jan 2026 22:55:44 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
