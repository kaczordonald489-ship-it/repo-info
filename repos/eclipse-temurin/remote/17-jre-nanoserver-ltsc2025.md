## `eclipse-temurin:17-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1292373363a79add87c497ad84a927ce415bed108b8ebcef637f423bbd13b068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:a8f9c47438753a9c3e3f1dc60e7bf0e6f903536b9f9007188103d52ad8e5cfee
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243076719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2948d96cef7413b4618bd218ee067629570db04acef8efd47e19bd8d3c82c019`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 23:39:50 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:39:51 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 13 Jan 2026 23:39:51 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 13 Jan 2026 23:39:52 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:39:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:39:58 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:40:05 GMT
COPY dir:6bccbcbb352f3cf6e189ef0696470e3588f387208e54e5af3934c804c91ec072 in C:\openjdk-17 
# Tue, 13 Jan 2026 23:40:09 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6acaab0d61ed33ace7d103c6051ef10936657c8cde6584d1379ede6a52410d`  
		Last Modified: Tue, 13 Jan 2026 23:40:14 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f93afd65df89ef2c7e42f9aeae6787a5094decd235575fbc844fa0607f63db`  
		Last Modified: Tue, 13 Jan 2026 23:40:14 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c221f11594ace9092e0afd3c8a01fd7e33ec9b202b7342d1f9ce9652a2ad524`  
		Last Modified: Tue, 13 Jan 2026 23:40:15 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268d819d7c41f4d6d3af9cdf6a1ec27004ded007554e6eb37f49d57397ffef67`  
		Last Modified: Tue, 13 Jan 2026 23:40:13 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe98c55a50b8c6a54edab8a5e0fb34fa75c3e5af2ff57ccec3712c9bf2ad6b5`  
		Last Modified: Tue, 13 Jan 2026 23:40:13 GMT  
		Size: 84.1 KB (84078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89ad94b8e8d4187824e5f17877435429b9b06a5faf9775e27c2a2dc16834ecc`  
		Last Modified: Tue, 13 Jan 2026 23:40:13 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68004d2fdf8d8e38c65164080f328081afed381a40e9a8690c4c393bd61fcdf`  
		Last Modified: Tue, 13 Jan 2026 23:40:19 GMT  
		Size: 43.8 MB (43796226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6418c87f575586403f276f006e639ee45f62d96ff7d606dc1499b56cfdc9a50e`  
		Last Modified: Tue, 13 Jan 2026 23:40:13 GMT  
		Size: 114.5 KB (114542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
