## `eclipse-temurin:11-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:9a6354bfb94200fa798111dd3e3612cfa8b0044a903e8c5fbf3a4ee5dbd2a14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:64769529fb5df8d958e5c18a96393826aeb40f4e7bb83eea24f935618aa0b4b0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242951999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18864200db5c6d55656d8e105ac544b5cbb24bc77c30ebe7ae7f91a14d3d0601`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 23:38:54 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:38:55 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 13 Jan 2026 23:38:57 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 13 Jan 2026 23:38:58 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:39:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:39:02 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:39:08 GMT
COPY dir:4835e564d5b678d207d3850b6f40a90e0afa12e9d665c48e7909a88923b1a7a8 in C:\openjdk-11 
# Tue, 13 Jan 2026 23:39:12 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c3018f35c73af59a36350615c430cd199174009bb767471c37deb2372b9478`  
		Last Modified: Tue, 13 Jan 2026 23:39:18 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4439769f1bf0b87f77b9deecb91d2ba9bf0b20e94f929cbc18a174ad60fa976`  
		Last Modified: Tue, 13 Jan 2026 23:39:18 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfcb5dabc365b64c030fdc3e4f441ae4af3a628c988200a10c70ef7c0096f39`  
		Last Modified: Tue, 13 Jan 2026 23:39:18 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28452a5492665bb5348c68b763ab8e33341e92ffe3bd531c5f3c62bae4b8da6f`  
		Last Modified: Tue, 13 Jan 2026 23:39:16 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb86e56ae7385a93c920ef6382e89750ffa07f91d1f232d6cafaa29175ce60c`  
		Last Modified: Tue, 13 Jan 2026 23:39:16 GMT  
		Size: 71.3 KB (71338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0ad30e40bfb6fca7a5abdd572ccad76453c14747626f3e0694a44691e07923`  
		Last Modified: Tue, 13 Jan 2026 23:39:16 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7af5d9222134f014477822b7f6d5b1c9973e66c9b7e1eac4d3953da3df580d`  
		Last Modified: Tue, 13 Jan 2026 23:39:22 GMT  
		Size: 43.7 MB (43695068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f122ac1b0a3234ef536cc858aae5382be24c3a639faf52eb8e507294565e68`  
		Last Modified: Tue, 13 Jan 2026 23:39:16 GMT  
		Size: 103.7 KB (103687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
