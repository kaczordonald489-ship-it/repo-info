## `eclipse-temurin:21-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:2abc2a80520ba3cebcefc9282bea89a52c4841a3c7846d888b508f89ca7eb3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:21-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:f6a22cecea3e372521b1eade5961463465ed830d6a594a6f3f3e449ea1353656
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1579754969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e576e37944a4dc74500539286929de5f23c9212259d94e0780b6a365cb061e4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:57:54 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 13 Jan 2026 22:58:07 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_windows_hotspot_21.0.9_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_windows_hotspot_21.0.9_10.msi ;     Write-Host ('Verifying sha256 (56b167659821fe125ea3b2974b0da1bac725b886b77193629d8ef880d38517e1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '56b167659821fe125ea3b2974b0da1bac725b886b77193629d8ef880d38517e1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 13 Jan 2026 22:58:12 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91938e162987eb0675b8773bfe45efb2af9a96d1e9473d3ebd4a447259bcc862`  
		Last Modified: Tue, 13 Jan 2026 22:54:06 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e3f634cf5544c0126ea14c85d839ef19496b4b7897a03e3908c72187f2808d`  
		Last Modified: Tue, 13 Jan 2026 22:58:16 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22179ed72cc5ad9b5ec404691fe38efe6a18a94665c2eea934840b2cb2881048`  
		Last Modified: Tue, 13 Jan 2026 22:58:25 GMT  
		Size: 83.6 MB (83624708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0421d08ac8eb9ba1540e669ff2ab63139bb22f5f2be2940c19b2a478896f10ed`  
		Last Modified: Tue, 13 Jan 2026 22:58:16 GMT  
		Size: 367.4 KB (367352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
