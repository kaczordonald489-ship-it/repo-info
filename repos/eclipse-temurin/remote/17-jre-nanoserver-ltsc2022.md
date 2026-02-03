## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:dac1b40d81be6bfca39802f49bb25867bc23721c06421142a1e2d469991d5c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:f3bfa3f6b529611a4a767628440b1d9bd11f8c2d0f5c9bcab00e089b932ec57f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.7 MB (170665538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551633be0b1f1b8d1fb01f692ddccad6710f3df94a5674203923669f0c44619f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 13 Jan 2026 23:34:00 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:34:52 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 13 Jan 2026 23:34:52 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 13 Jan 2026 23:34:52 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:34:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:34:54 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:34:58 GMT
COPY dir:6bccbcbb352f3cf6e189ef0696470e3588f387208e54e5af3934c804c91ec072 in C:\openjdk-17 
# Tue, 13 Jan 2026 23:35:01 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:a385b5f5ebe1c2193a49568d4eeb52c97c065eb45f50bbdf48cd901e88678b9a`  
		Last Modified: Tue, 13 Jan 2026 23:35:07 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0d44157b6ce424febdbef0eabf44639239fee8c17be7d6cc30cad2689d6147`  
		Last Modified: Tue, 13 Jan 2026 23:35:07 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590c4822c938d0a6b627c8c8ff85a9e78c0192fcaec1b1515ea05c6b95067f07`  
		Last Modified: Tue, 13 Jan 2026 23:35:05 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16090babacdbbfc5b000ea7682626fe3b6d4325ec6658915df10267768dfdb8a`  
		Last Modified: Tue, 13 Jan 2026 23:35:05 GMT  
		Size: 76.5 KB (76497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a41f386f90e680ac25c16083cd3d3deec76024437bcc089cbeac05cea67d6c0`  
		Last Modified: Tue, 13 Jan 2026 23:35:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c728cfa85576b65c510606f2e5d09cc356697866112da98f3872470392afd1`  
		Last Modified: Tue, 13 Jan 2026 23:35:11 GMT  
		Size: 43.8 MB (43796056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03739c2e6bc2b5cd027e1ab7391e3a093f400afec08639534055d883c637966`  
		Last Modified: Tue, 13 Jan 2026 23:35:05 GMT  
		Size: 90.8 KB (90836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
