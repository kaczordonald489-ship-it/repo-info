## `eclipse-temurin:11-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:427c12aab1f86556e226a32fbdbdd68b1c8087a5b6da2220bded730c16bab6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:54250ef51f193d106eddbff0608a7f7d3df9cefd5926caf2bc3b38b11fc90b55
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1571095598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8792e05a2b1eaf021291b414f2743d170377eed59a83d54a30d33937ef881cc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:51:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:55:24 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 13 Jan 2026 22:55:36 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.29_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.29_7.msi ;     Write-Host ('Verifying sha256 (2113628e4feb65cc5e399c34bd1a070f8c8b931ef2899b8a7f7ac3179a3d24ce) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '2113628e4feb65cc5e399c34bd1a070f8c8b931ef2899b8a7f7ac3179a3d24ce') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 13 Jan 2026 22:55:41 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1683b1c0b751981760e021483daa24f623ab1f8d270f970baf3cb1b58348c5fd`  
		Last Modified: Tue, 13 Jan 2026 22:52:02 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be80418f3e5226f29a13050d94b1368e7ab5921fda356ce0887f5957b02b652d`  
		Last Modified: Tue, 13 Jan 2026 22:55:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da196bfb05483f6ff5febfda64b219ebdf5d191338222bc62efab9ba18b9b4e0`  
		Last Modified: Tue, 13 Jan 2026 22:55:52 GMT  
		Size: 75.0 MB (74961862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a7e000e5165b219936ba44ab0840d5849234007f4be3aa094dde746152df20`  
		Last Modified: Tue, 13 Jan 2026 22:55:45 GMT  
		Size: 370.8 KB (370848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
