## `eclipse-temurin:8-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:3669988eae72bc83bb49a5cf2b360c489de807219686060463a5b27d36e53c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:f26dea329a2c850a5e372b9dd9dba8bfaa9d84ab2283a59bf7b19b88dbe125b6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301710897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba68691be40a0eedb2d2700f9ce94e02a776400016c0d781339875c8ff537004`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 23:38:54 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:38:55 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 13 Jan 2026 23:38:55 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 13 Jan 2026 23:38:56 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:39:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:39:03 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:39:16 GMT
COPY dir:2635c350952b93f594bde5c3dd80336e4c4ce35889642cd7d3de9ae358e6cda3 in C:\openjdk-8 
# Tue, 13 Jan 2026 23:39:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdee3c11b72bcc7f72f7032a24f71c381fadd5b2c72a6401313081707cbf67f`  
		Last Modified: Tue, 13 Jan 2026 23:39:26 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f307b1c4fa7eb372b31934968387efcab904d4076f46ccfe7e3bd93c7cf5262`  
		Last Modified: Tue, 13 Jan 2026 23:39:26 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7097d87310e9e6096c588fc531795dcb3e58dd256ee626fc3fa3e9f34c2cc4db`  
		Last Modified: Tue, 13 Jan 2026 23:39:26 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52e4b94d787e73f040fd472c0998467697c16df125bfbe66baae18f5dec61d6`  
		Last Modified: Tue, 13 Jan 2026 23:39:24 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a606f78aec306ea6067e754d8360c878ec6f970a52db46f4cd05e397321b9f0`  
		Last Modified: Tue, 13 Jan 2026 23:39:24 GMT  
		Size: 77.2 KB (77184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df062b21a53aa5c9a5e747ec430ae924824372af3a84ca644e1c362256a890a`  
		Last Modified: Tue, 13 Jan 2026 23:39:25 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5d69c253361199abf37b54cef67d5cc3cc8a7c5e8cc3305125c48f0c7e06b8`  
		Last Modified: Tue, 13 Jan 2026 23:39:32 GMT  
		Size: 102.4 MB (102438071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a4247eb27c2a12a1c1ff936f9770b1a73d76a49ea0cef28cdab00b169a4f11`  
		Last Modified: Tue, 13 Jan 2026 23:39:25 GMT  
		Size: 113.7 KB (113684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:15a8d349dc09df2c894efa75d5736031803b10fe0d28e32068a72048246d7a7b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.3 MB (229311474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972cf276993cbaf0e5bda01c863ff2df94b1616504649bb43de6fb7e35e7ac27`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 13 Jan 2026 23:33:23 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:33:24 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 13 Jan 2026 23:33:24 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 13 Jan 2026 23:33:24 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:33:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:33:27 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:33:32 GMT
COPY dir:2635c350952b93f594bde5c3dd80336e4c4ce35889642cd7d3de9ae358e6cda3 in C:\openjdk-8 
# Tue, 13 Jan 2026 23:33:36 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:61aa537b2fcdf734f1a2491d2f5664b3bc66d624ab8c2e6b8e7da3d28199be00`  
		Last Modified: Tue, 13 Jan 2026 23:33:41 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfafb9ff33f39a1af7d49d364428299bacb111ac970b0370c7ef48bb67389edc`  
		Last Modified: Tue, 13 Jan 2026 23:33:41 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448a2d40ccdfaead93db18fc7ec90220a94139d92b1f666c46e4ea9d7052a051`  
		Last Modified: Tue, 13 Jan 2026 23:33:40 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dc23a509145c42935377dc28f7abb913f8f8d8d84cbbae4703898c0960647b`  
		Last Modified: Tue, 13 Jan 2026 23:33:40 GMT  
		Size: 72.3 KB (72322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad403919d8d4caceab15369c88c86565d1519d1e2ac39e5d1b65d744f7da6e3`  
		Last Modified: Tue, 13 Jan 2026 23:33:40 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a7c2ff3fb6b2884637fdba9cf38dce5550f6500a77be18bbdff4d1ed2642e8`  
		Last Modified: Tue, 13 Jan 2026 23:33:47 GMT  
		Size: 102.4 MB (102438104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cfd241b0d4f82e5b419f746cf24fc8e5669581fa860b5ea58683968837789d`  
		Last Modified: Tue, 13 Jan 2026 23:33:40 GMT  
		Size: 98.9 KB (98907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
