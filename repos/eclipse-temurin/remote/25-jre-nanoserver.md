## `eclipse-temurin:25-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ab86dbf22fd0a9460464942cba21a9ca09501622682f6e089ca9315dd8b9cd4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:25-jre-nanoserver` - windows version 10.0.26100.32230; amd64

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

### `eclipse-temurin:25-jre-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:b935a189ed2997ef14005df5fc4f7c3e186b45448e2d2d2b9e385236c18d874a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185433473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47fea20ee685fb10d37384f0de664c19d22b6a7de5d6f6208b68ab9c70110e31`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 13 Jan 2026 23:33:23 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:35:25 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Tue, 13 Jan 2026 23:35:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 13 Jan 2026 23:35:26 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:35:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:35:28 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:35:35 GMT
COPY dir:38f2d146da8b2d45f6309f76e3864fba66a43ff9541e6e5522e91b15798552e5 in C:\openjdk-25 
# Tue, 13 Jan 2026 23:35:38 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c25f87ad72679f18a1492f30026900d89850955868135e06b3ef22d32b466c2`  
		Last Modified: Tue, 13 Jan 2026 23:33:41 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17f0f7fa53ab38a88a52d1004aa4b38502dd3da7c548ce57eb1faf89a82d329`  
		Last Modified: Tue, 13 Jan 2026 23:35:43 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9713ec95c30bdc56b819a6f48db78aedfd85fcf5b88e03347a96eb4a6f76d9f`  
		Last Modified: Tue, 13 Jan 2026 23:35:43 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1f8da3d75e3a538c1ddfa3ffaa48e31516427c4775ecc153dcded73e74152c`  
		Last Modified: Tue, 13 Jan 2026 23:35:42 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4617f45368e0d33b071a01db023cc6f3d651e44bf9a5dd8bcdf9d19401bc531c`  
		Last Modified: Tue, 13 Jan 2026 23:35:42 GMT  
		Size: 76.8 KB (76761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0496b0eb37797f829d48fdc83a01f31730d481b3a3395f9a002223f4333b85`  
		Last Modified: Tue, 13 Jan 2026 23:35:42 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a661e3d73affa9d77712ada6c8c5ebf78364f9d28645f1fd85bcbbb2aa57e50`  
		Last Modified: Tue, 13 Jan 2026 23:35:50 GMT  
		Size: 58.6 MB (58563781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661ec85f777dd3981ae4abb5a66501d0ad6fa92a282a5d94dfbfa69c706fc277`  
		Last Modified: Tue, 13 Jan 2026 23:35:42 GMT  
		Size: 90.8 KB (90780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
