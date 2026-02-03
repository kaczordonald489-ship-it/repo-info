## `eclipse-temurin:8u472-b08-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:dac8c8ca75071d83fbb81ecffa5d83dbd42ce3c53f04f4dc489e69288895cfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:8u472-b08-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:07cd8699353168f334e8471b87f6c49c5428b30d6f91515085214ac2a437613c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167433738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37c60628e1870819c99269de55231e7081b2a933569b20e5b72350684da2b23`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 13 Jan 2026 23:34:00 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:34:00 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 13 Jan 2026 23:34:00 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 13 Jan 2026 23:34:01 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:34:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:34:03 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:34:06 GMT
COPY dir:d46ae848a780de83988aca6679aeefb6cb592f306ae2eca344ddb66bc6559a89 in C:\openjdk-8 
# Tue, 13 Jan 2026 23:34:09 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc58112f1d1d638f65a75c8bcdb844fc8acda257ce27f49b05ca59ae6852b63`  
		Last Modified: Tue, 13 Jan 2026 23:34:15 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4bf1f48fdd87de04aaf7774e6d6d93cc6df6bf8cc9b77378edd21bb7298393`  
		Last Modified: Tue, 13 Jan 2026 23:34:16 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6553d6d9ed2a18003815afb769163b97f88e92339de05d60197f2d440cec206`  
		Last Modified: Tue, 13 Jan 2026 23:34:15 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a45cfcb51bbbea939ebb61881d8ff15bf4f4f5e98658627d072378de8e92dbd`  
		Last Modified: Tue, 13 Jan 2026 23:34:14 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3348de03407e7a64d7aa16d0672e9de247e692f89f8fc3979ec860c818b903`  
		Last Modified: Tue, 13 Jan 2026 23:34:14 GMT  
		Size: 77.6 KB (77647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42737df7d6f0be5df1d3c5774b08486804b91c36c8419672163db10dc267135`  
		Last Modified: Tue, 13 Jan 2026 23:34:14 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65e1abf922bdb93718ef31703984018bc8e8560c69ca3a724424aae7f1fda3b`  
		Last Modified: Tue, 13 Jan 2026 23:34:18 GMT  
		Size: 40.6 MB (40555105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c52ce534dde8f197a0476c8d6325f0b1ef798904f4ac22aa6666654d247e1e`  
		Last Modified: Tue, 13 Jan 2026 23:34:14 GMT  
		Size: 98.9 KB (98907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
