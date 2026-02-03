## `eclipse-temurin:8-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:f08e5d1a3cdff260bf13ecfc58a9198b6bd7e258ac9a7192a0b275f949abba2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:8-jre-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:c852dbd4ebec90cf4da26f069e780050c423753352d8b643fe2c7fba3e925a1e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1568828630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae029a72b3ab96c144f5001b89581b25d272c0974ed973b6266686068b594ed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:53:42 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 13 Jan 2026 22:53:58 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_windows_hotspot_8u472b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_windows_hotspot_8u472b08.msi ;     Write-Host ('Verifying sha256 (2099c63f97bab0dea8c70fb2f32a7a8a2ad8e53167f0523f42c8f62d03bcc66a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '2099c63f97bab0dea8c70fb2f32a7a8a2ad8e53167f0523f42c8f62d03bcc66a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 13 Jan 2026 22:54:04 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b835fba333e570083fb72b246efd784f0facce6d32c9a0f56dcf392cebad8a`  
		Last Modified: Tue, 13 Jan 2026 22:54:08 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654df533eb5a27d4f255d83633280bd5d063720b5018ba5d007bc615a1972c4a`  
		Last Modified: Tue, 13 Jan 2026 22:54:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03d177175166a6d66e12ffe46d761385e46fad5afa50098c14e68dfc8fad9bc`  
		Last Modified: Tue, 13 Jan 2026 22:54:14 GMT  
		Size: 72.7 MB (72678821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3002d905c90af93435efea4013ffa303e54ab6f6d34b308fbf0670b5f9a7a54`  
		Last Modified: Tue, 13 Jan 2026 22:54:08 GMT  
		Size: 386.9 KB (386895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:42252d1a9e56f2887c6e861298603f5c0ab562f03effc47b55479f450c3c38db
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908794613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da38c233bcf75d7cfe080d45c9e7306cd8f50f3823a805df805fb1d5cee2166b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:52:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:03:22 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 13 Jan 2026 23:03:35 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_windows_hotspot_8u472b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_windows_hotspot_8u472b08.msi ;     Write-Host ('Verifying sha256 (2099c63f97bab0dea8c70fb2f32a7a8a2ad8e53167f0523f42c8f62d03bcc66a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '2099c63f97bab0dea8c70fb2f32a7a8a2ad8e53167f0523f42c8f62d03bcc66a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 13 Jan 2026 23:03:41 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:05a0d275cb0351c261395acf080ca5b3e97a23bd3d8c039e16ca5ae8c7e28ac6`  
		Last Modified: Tue, 13 Jan 2026 22:53:53 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7b6570e5f82d129934d38ffc5c472115afc6b6986f56685df45240a91acab8`  
		Last Modified: Tue, 13 Jan 2026 23:03:45 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d185802dc8cb3bbb1d7be46a5ffb511c4554b6681b72defe7aca56246c62cad8`  
		Last Modified: Tue, 13 Jan 2026 23:03:51 GMT  
		Size: 72.8 MB (72782097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0626cbbbfe10825bb83aa566881b5b08f2b1c4c7b28c0f6b2b96748b6e2b58`  
		Last Modified: Tue, 13 Jan 2026 23:03:45 GMT  
		Size: 350.7 KB (350717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
