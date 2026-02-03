## `eclipse-temurin:21-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:36e5860d4b4e3aab411cca03b5ef4e833602c2c5b27141971f5dfb214192653b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:21-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

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
