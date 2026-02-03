## `eclipse-temurin:25-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:d71d4dc989f48d3a1103997160970f968660944611f444b1a045571d64f66b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:25-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:b5c66849361b81eb3576a6922fa08bc2a2f434445427f1587309465c03a8aff9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257811979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac58fa98c78846658064ad42e1450eb602fe49fab2f3c096df54f9a1f8f5e79`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 23:38:54 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:40:21 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Tue, 13 Jan 2026 23:40:21 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 13 Jan 2026 23:40:22 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:40:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:40:24 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:40:29 GMT
COPY dir:38f2d146da8b2d45f6309f76e3864fba66a43ff9541e6e5522e91b15798552e5 in C:\openjdk-25 
# Tue, 13 Jan 2026 23:40:32 GMT
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
	-	`sha256:79927f66f8a9857ac110686b8d75f3889345c5423338ff6deb1a06cb037863b6`  
		Last Modified: Tue, 13 Jan 2026 23:40:37 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f788d5018a3871cdfec1fddbb8da6e5993ff185411d29693f0a13cf09ea785cd`  
		Last Modified: Tue, 13 Jan 2026 23:40:37 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa5725fa5dffae640c4b8e22e1e4f460a6e50136a99f4689b4664e5c5c0b870`  
		Last Modified: Tue, 13 Jan 2026 23:40:36 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c4a6793b60afd43c9e9661ff4cf007d2675c45fbb7eeaf06b6e11d97b25231`  
		Last Modified: Tue, 13 Jan 2026 23:40:36 GMT  
		Size: 73.2 KB (73250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e8b65fa384826ed74082f5bf799653cd7c460d710d17599b81279c6a25a38c`  
		Last Modified: Tue, 13 Jan 2026 23:40:36 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03057a253f43f34fa6be1e8ade1eee0cbb8adb0f9b7e48d861e11bb765dd703`  
		Last Modified: Tue, 13 Jan 2026 23:40:43 GMT  
		Size: 58.6 MB (58564080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af9e1ddb843bd17c10e1c1d743ae87bccf4255fa68c8fdf26b93ca2b4bdee15`  
		Last Modified: Tue, 13 Jan 2026 23:40:36 GMT  
		Size: 92.7 KB (92717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
