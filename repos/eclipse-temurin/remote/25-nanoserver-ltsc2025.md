## `eclipse-temurin:25-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:fc53db2bd243b5b6c1863b6c5e43e75c0fbf5d981c576fdc451ed1c4861e35fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:25-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:f5747055a54093c2c9515ba4cf71911c80051732643de3adc8e56186908ed646
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.2 MB (337221596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75fff12fdbc92931084394482954aaf5fec6ba31d15110240d5f2e9a73a2580`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 23:41:10 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:41:11 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Tue, 13 Jan 2026 23:41:11 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 13 Jan 2026 23:41:12 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:41:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:41:18 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:41:28 GMT
COPY dir:889642903e29f32ff0f0b6da5f64cf6a40ecfa6d85d0926e4981ccbc885ac0c0 in C:\openjdk-25 
# Tue, 13 Jan 2026 23:41:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Jan 2026 23:41:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b62d678ebebbad1b379101a13ac16a90d25f0efcc9a37737214a4329157985`  
		Last Modified: Tue, 13 Jan 2026 23:41:40 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42d66a14a48b56100de1ad64ef6a625c74dae410900a62d2ea735a8d0c9736e`  
		Last Modified: Tue, 13 Jan 2026 23:41:40 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9778a0aa50cbaf8c1d293c8c6c693263e135f1bd1c713c83c76ac1babc23bff`  
		Last Modified: Tue, 13 Jan 2026 23:41:40 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba682cc405e5cc9b7ec8da0747ee91ed9b1c3f72f8aa316233f017e30a94b88d`  
		Last Modified: Tue, 13 Jan 2026 23:41:39 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db081c00e1f78d53eb59eb8163e0438b1bad41db979cc771f0631289a754b5fe`  
		Last Modified: Tue, 13 Jan 2026 23:41:38 GMT  
		Size: 72.2 KB (72210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd60b126ae09258b45dc7cf5c22a4dbfd06ab7200c6cf82f7c80f58d9301a51`  
		Last Modified: Tue, 13 Jan 2026 23:41:38 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f00209fa51c4d60571052c23e4bd060230cd52fe30f3ec6f936d3a40711573d`  
		Last Modified: Tue, 13 Jan 2026 23:41:50 GMT  
		Size: 138.0 MB (137951865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27f2f346347fefb1123bf5f42b277b6fb8cd3c9fc0fbdd92b7e34f09927ac14`  
		Last Modified: Tue, 13 Jan 2026 23:41:38 GMT  
		Size: 114.5 KB (114549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ee7dd38c07eaf98edac05d8ba9bfddf053fc323206d68bac513aa410f23266`  
		Last Modified: Tue, 13 Jan 2026 23:41:38 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
