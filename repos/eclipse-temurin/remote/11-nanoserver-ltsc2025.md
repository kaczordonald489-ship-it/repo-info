## `eclipse-temurin:11-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:227946dafff64bdc1c5ff86a37703c4befe492161310e3bc43588c0e85594e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:11-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:72262abce46da19f6a7293a724b8e1ddec52c0d502fa979516d86ee69b8f7331
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.9 MB (393906730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318622ee7a7e5b925cc9bc2faa77707cc5d90c3d5c89fa37f64819c5e27a13d7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 23:39:09 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:39:09 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 13 Jan 2026 23:39:10 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 13 Jan 2026 23:39:10 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:39:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:39:15 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:39:26 GMT
COPY dir:207a50c3961430a3231a748eb9ce354eec00313f0753b2d5e8f279d3afd46cd8 in C:\openjdk-11 
# Tue, 13 Jan 2026 23:39:30 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Jan 2026 23:39:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec5cb376d95cf1b842a29fcd4023bd5991c87bb8329d76e240455d3d5b6787b`  
		Last Modified: Tue, 13 Jan 2026 23:39:36 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e79cac5a5e7fe47b1838336f5253daa0ea758f2dfeb4b11099944e129bc09a`  
		Last Modified: Tue, 13 Jan 2026 23:39:36 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8140ab88736fcc9b42b90453440341ea9bf81914f38a4696efb86970967a5d0`  
		Last Modified: Tue, 13 Jan 2026 23:39:36 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87adf3421da9eba987a10281141dd92a259978e7dd7b0d8f08ad69b2903ac79f`  
		Last Modified: Tue, 13 Jan 2026 23:39:36 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e35d9ebc18f41501fdc8f03d2b0b3e63a8821c144362efe3ca0cc2c2662b88`  
		Last Modified: Tue, 13 Jan 2026 23:39:35 GMT  
		Size: 69.7 KB (69656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d0d189d97270ba0f4c7a7054a6b566864f84e737c72b2e1980baa3a3e6ed1a`  
		Last Modified: Tue, 13 Jan 2026 23:39:34 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624b84509281bde67349f9b1ec1ad7a3324076009564b37e40a804dcb8373133`  
		Last Modified: Tue, 13 Jan 2026 23:39:47 GMT  
		Size: 194.7 MB (194670828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5832b949815f5d7245538a24b4facefba4dd5d0ce1f9d5a4b5f365206827ee`  
		Last Modified: Tue, 13 Jan 2026 23:39:35 GMT  
		Size: 83.3 KB (83268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6c0381d120040f0438e8dd9b3dde839caba3ecd6f258e4d096182dd75f7c1`  
		Last Modified: Tue, 13 Jan 2026 23:39:34 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
