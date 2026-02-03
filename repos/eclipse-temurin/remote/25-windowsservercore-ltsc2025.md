## `eclipse-temurin:25-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:ad6cd09f04a8ad4c128c4efea4f7cebf382e35b57da72cb91ef8c87bb37fa1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:25-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:a85ffdfaf063aeec3d2f2848e88e9c7bd0ab5fe9ae86d77e8ce53f4ab7969557
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1749650096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01a69505cc945de7bfaa23018c3f8ccef14d823796ca1b00f55b4a59e0c1e08`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:57:57 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Tue, 13 Jan 2026 22:58:18 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_windows_hotspot_25.0.1_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_windows_hotspot_25.0.1_8.msi ;     Write-Host ('Verifying sha256 (c49e19ba5b47bf119402b1e0a0a71ce5b19ddd9e4ac3e038ea99fe648bd0b3f9) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c49e19ba5b47bf119402b1e0a0a71ce5b19ddd9e4ac3e038ea99fe648bd0b3f9') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 13 Jan 2026 22:58:24 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 13 Jan 2026 22:58:24 GMT
CMD ["jshell"]
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
	-	`sha256:6b7ee79e8b0b5b548303b75052ef26e4df4bff8ad92dd3de2b4f9c1c65beab11`  
		Last Modified: Tue, 13 Jan 2026 22:58:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803cab4eb11400c24dd34d29b06edd231d06280cf82efdf22331be7f09fa2a06`  
		Last Modified: Tue, 13 Jan 2026 22:58:45 GMT  
		Size: 253.5 MB (253531757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e5cad0463690bdd92a2c0df317564266ecbefe69c124ae7f48ee8ed2df112d`  
		Last Modified: Tue, 13 Jan 2026 22:58:28 GMT  
		Size: 354.1 KB (354138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9da526f9f9862016a35c5f2a038a96ea15e701c0ab51d9644610631f196634`  
		Last Modified: Tue, 13 Jan 2026 22:58:28 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
