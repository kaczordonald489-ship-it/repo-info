## `eclipse-temurin:17-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:599c3d40cddeccd97d63b0d8ab9f1f678dce16c3dfb75ac95de42548f577c9ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:17-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:6173d5121b18dffd61314ca9b853404bcbb7362c73ffa766b37da277d560a53d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1851717863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b5351bc9f6a9e8082011f4b3813771afeca694af48b3b257b10c1972339c6a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:51:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:56:12 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 13 Jan 2026 22:56:36 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_windows_hotspot_17.0.17_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_windows_hotspot_17.0.17_10.msi ;     Write-Host ('Verifying sha256 (df491b4dbad46dcb77fcba22a0edac4c53a89448f699b33a5cdd5349bd5865dd) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'df491b4dbad46dcb77fcba22a0edac4c53a89448f699b33a5cdd5349bd5865dd') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 13 Jan 2026 22:56:42 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 13 Jan 2026 22:56:42 GMT
CMD ["jshell"]
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
	-	`sha256:c543e2302ce858b803b3747c7284708ad53d5a6ca9367047e9f4c9f3b264d8e4`  
		Last Modified: Tue, 13 Jan 2026 22:56:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3def9cd8ded51f71456eccbe547e0fb8a1c31f3d07f27891544dffc6a9bd8130`  
		Last Modified: Tue, 13 Jan 2026 22:57:05 GMT  
		Size: 355.6 MB (355571119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fff6a42890c39a810e8e49d44890a6216be3eb0815cb5d845a33b5c3b35e41`  
		Last Modified: Tue, 13 Jan 2026 22:56:46 GMT  
		Size: 382.5 KB (382538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661fb1866203929e46827008019c14143f1a58aee530560bf7b0b2dbfe8d78a8`  
		Last Modified: Tue, 13 Jan 2026 22:56:46 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
