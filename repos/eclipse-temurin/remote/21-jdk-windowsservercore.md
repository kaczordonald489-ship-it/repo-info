## `eclipse-temurin:21-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:82d9ee8cb18e15c6dfc0b786bf60f8fe80ac95067f943d700d34ebd152096993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:21-jdk-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:ba209feee1aa79e6aab5a640210c9280a76b48f23716eb9db9b033bd795b0184
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1876842201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce681f384c2b68bea8e2b2cdaca2153a74d55bba9e15d645206bdab49c0b4759`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:57:49 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 13 Jan 2026 22:58:12 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_windows_hotspot_21.0.9_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_windows_hotspot_21.0.9_10.msi ;     Write-Host ('Verifying sha256 (e97f44c7915866c3127565a91373d03adb639916186b24fc5e0f818a3bde8d3f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e97f44c7915866c3127565a91373d03adb639916186b24fc5e0f818a3bde8d3f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 13 Jan 2026 22:58:18 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 13 Jan 2026 22:58:18 GMT
CMD ["jshell"]
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
	-	`sha256:1e7aff17162d2cb5e918833b1a4e963942abbb31ff4a04d9ddcb090cf1a68131`  
		Last Modified: Tue, 13 Jan 2026 22:58:22 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b86a8d6e958a733c8ee714a7254848d021d84254ed7af71c69e2e01467c7760`  
		Last Modified: Tue, 13 Jan 2026 22:58:42 GMT  
		Size: 380.7 MB (380715112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968b0b89a174bb65ed06826259862e9398abf81469e9a3f228ea4e5fd7eb9972`  
		Last Modified: Tue, 13 Jan 2026 22:58:22 GMT  
		Size: 362.8 KB (362847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c66627daf99e8cfaf454cfa786c54538618b56e93d4d06e39bda6e28ec68aa7`  
		Last Modified: Tue, 13 Jan 2026 22:58:22 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:d1861b71657521b3972d688dcccde0ed887b251ea3508e9baac869a1b4e77ff3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216868647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727680c09cc36018c530378cfeda3e1c8c27265e312b6fce3e09b1caff43cdfd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:53:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:04:09 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 13 Jan 2026 23:05:20 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_windows_hotspot_21.0.9_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_windows_hotspot_21.0.9_10.msi ;     Write-Host ('Verifying sha256 (e97f44c7915866c3127565a91373d03adb639916186b24fc5e0f818a3bde8d3f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e97f44c7915866c3127565a91373d03adb639916186b24fc5e0f818a3bde8d3f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 13 Jan 2026 23:05:27 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:05:28 GMT
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
	-	`sha256:2b66bcc5dc6d3aaa7c66e1e850b7913643ad68c20c1b5e2f0a0f33bc0b2abc19`  
		Last Modified: Tue, 13 Jan 2026 22:55:09 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6a86dcc99acfe768d547a42447d2406f1c6a114cf919a08bf53c748240303f`  
		Last Modified: Tue, 13 Jan 2026 23:05:33 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57584bc83d3061a36cfc2afcf793851a5dc3a386bb92cf54bb8e66fe7c50d8f4`  
		Last Modified: Tue, 13 Jan 2026 23:05:54 GMT  
		Size: 380.9 MB (380852408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23763a6d58824a7ff626a45c3ea90e5ce6f9e9a27a1c8f8c00af775ebe5d9270`  
		Last Modified: Tue, 13 Jan 2026 23:05:33 GMT  
		Size: 353.1 KB (353116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578951edca0f9bd40f0c6bef63a165ec06583976a191cd9e1fe0d4f213ca3446`  
		Last Modified: Tue, 13 Jan 2026 23:05:33 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
