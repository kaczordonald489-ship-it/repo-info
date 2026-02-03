## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:cb93282c122629cbc3cbd39aa37fc325d311d95f380149283e24b4b4d685bd30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.26100.32230; amd64

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

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:897ac2a953c2b8bc150f1855117b66791ae94f60650937fcbdbcda5dc2208628
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321560396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddc9f97166b63101d9fed8e43f1fa12db267938c5f6ae9cde443d7a5d60ba22`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 13 Jan 2026 23:34:02 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:34:02 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 13 Jan 2026 23:34:03 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 13 Jan 2026 23:34:03 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:34:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:34:06 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:34:33 GMT
COPY dir:207a50c3961430a3231a748eb9ce354eec00313f0753b2d5e8f279d3afd46cd8 in C:\openjdk-11 
# Tue, 13 Jan 2026 23:34:37 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Jan 2026 23:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d687fc4849e46782e4a7b35552cab83fee04281eaa1a506432a892eadbcf023b`  
		Last Modified: Tue, 13 Jan 2026 23:34:43 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923451f3445d4e853b212ab69c0892b26ba2bb7fc47d0378b7ea98167996a333`  
		Last Modified: Tue, 13 Jan 2026 23:34:43 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c85a948fd77724fdb2095b1799a4568790ecf2d29f92ede61e69ef715ea62a`  
		Last Modified: Tue, 13 Jan 2026 23:34:43 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60dc47a669b335bc3aa399d9c3db4d9306b900d0d67632d2cecce47175b11f8`  
		Last Modified: Tue, 13 Jan 2026 23:34:43 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fff995e1d2b3717c38eb8c255ab2510b1cbbdf426bae63922a55f78dcf179c9`  
		Last Modified: Tue, 13 Jan 2026 23:34:42 GMT  
		Size: 79.2 KB (79194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4622718a5f0ec262373f782a3d4adf1639fea23fa5be17acab418a063d0b440c`  
		Last Modified: Tue, 13 Jan 2026 23:34:42 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38acf9be9d1c4b76bd62764ca0a79527cdf4f4d7e34fa3352e931ef6647743a3`  
		Last Modified: Tue, 13 Jan 2026 23:34:55 GMT  
		Size: 194.7 MB (194670809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4359f0485114499c4f7a6e9ddb0070a119a084d9751864da8fa4350b616378b`  
		Last Modified: Tue, 13 Jan 2026 23:34:42 GMT  
		Size: 107.1 KB (107133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca06dd4632ca1549d5f019fb6b9078177852f8f41fdc8937341317c6922fda39`  
		Last Modified: Tue, 13 Jan 2026 23:34:42 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
