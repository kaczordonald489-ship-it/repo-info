## `eclipse-temurin:21-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:208d9c0913eb6a2c1cc63e4ee8cfe97de2c069004f7088876bef9d88e6912023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:784fefcb6e3beb2e41393a0644b909a7d8f9e71fcaea5dcf52e994ab384243da
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.0 MB (401039677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666460ee753768fe801f1557e215d67521897242b800fb5a8242021b16a37022`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 23:41:15 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:41:16 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 13 Jan 2026 23:41:17 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 13 Jan 2026 23:41:17 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:41:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:41:23 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:41:39 GMT
COPY dir:ca3f22bac3b96b31650dd9d8b46eabc8cfc824f09a5d61f04cd758713bcc4892 in C:\openjdk-21 
# Tue, 13 Jan 2026 23:41:44 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Jan 2026 23:41:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d729f3d3a814ee245aa51e2d18ecf20910ef18f85c102b2f4237daa76e4870`  
		Last Modified: Tue, 13 Jan 2026 23:41:51 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4154e75cac494924006c5b499c3989d8a23d8c359259e34d1d02da85e1a329`  
		Last Modified: Tue, 13 Jan 2026 23:41:51 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5917b9a0bffb779453ee269da14394225f451a44d82fa9df9587d4d16a8a92`  
		Last Modified: Tue, 13 Jan 2026 23:41:50 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ae2261533c19c21e3247c6476fc4d391e1128ce14c3274a96020d90568cb7c`  
		Last Modified: Tue, 13 Jan 2026 23:41:50 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99c51af55cce420620751e4bddf50b4806ac6f716f8f79a46885a9a6e98b57a`  
		Last Modified: Tue, 13 Jan 2026 23:41:49 GMT  
		Size: 71.3 KB (71284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f82b5c80564bec31f300898eb599055315e7ca25bfc3c6943c21a5907e88f5`  
		Last Modified: Tue, 13 Jan 2026 23:41:49 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfbfd45441b30a9462c2e1c5446273df97a41e389a358280007987b88420ea22`  
		Last Modified: Tue, 13 Jan 2026 23:42:03 GMT  
		Size: 201.8 MB (201782407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c2647681f0716d8b0cfc2b461601ad378430dfa2e02908b8e147e696fbdce1`  
		Last Modified: Tue, 13 Jan 2026 23:41:49 GMT  
		Size: 102.9 KB (102934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22c1eab319c70fd318e475e909b97481710ab7c97b72444d396b04f2bdb416b`  
		Last Modified: Tue, 13 Jan 2026 23:41:49 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:f413c21220a73df308847557a6ed0147095bc740ddcbd2318c2f6406e30f8b2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.7 MB (328670433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c5360a03de940af5a690005104476f3cf37db8b79ac518a9f52d06957908d8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 13 Jan 2026 23:34:09 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:34:54 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 13 Jan 2026 23:34:55 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 13 Jan 2026 23:34:55 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:34:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:34:57 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:35:34 GMT
COPY dir:ca3f22bac3b96b31650dd9d8b46eabc8cfc824f09a5d61f04cd758713bcc4892 in C:\openjdk-21 
# Tue, 13 Jan 2026 23:35:38 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Jan 2026 23:35:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98bbecdd0bcd40d16482ede27cc28f3c57f40602c77e88d2a179c072e2a73fc`  
		Last Modified: Tue, 13 Jan 2026 23:34:24 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb67197ad0f9bed382ddf4594458ef8fc3271af9502a36d3c00fa8fe1b1ded0f`  
		Last Modified: Tue, 13 Jan 2026 23:35:44 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cd4d354048ec049f2e58cd21a0c12c9d2d882c8d72f72e0bb5f97cd1d4faa6`  
		Last Modified: Tue, 13 Jan 2026 23:35:44 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23508a0baecf9db94bdadf0159a39d26afdf794b54c6c4d61e040667205318d3`  
		Last Modified: Tue, 13 Jan 2026 23:35:44 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95cb688ce8d8696061a11a0c8852addff2ad7e5c64a42e6eece87fe874905f4e`  
		Last Modified: Tue, 13 Jan 2026 23:35:42 GMT  
		Size: 77.4 KB (77440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc59c1d7e9d2021cf3bb3b6e607a555c271770d081770f0af0ee820f68776f97`  
		Last Modified: Tue, 13 Jan 2026 23:35:42 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1752fce993417f501d24b89b804babf3602f1d9a23cfa88dece09b3585171773`  
		Last Modified: Tue, 13 Jan 2026 23:35:57 GMT  
		Size: 201.8 MB (201782556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ad6ae5fcbb4a1279ebc1663b573360c5e03c816bf814e4fda85aa4777f804c`  
		Last Modified: Tue, 13 Jan 2026 23:35:42 GMT  
		Size: 107.2 KB (107153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8131e0bd66790c805f3dadfc9d69c04e785160a31843e492b8b3667ab124030a`  
		Last Modified: Tue, 13 Jan 2026 23:35:42 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
