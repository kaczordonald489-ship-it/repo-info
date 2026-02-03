## `eclipse-temurin:25-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:fb3c62bbc271dcf11887e21deb6af165afd15a3c641672c01be3104092c8c888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:25-jdk-nanoserver` - windows version 10.0.26100.32230; amd64

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

### `eclipse-temurin:25-jdk-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:5258b34079d1fe0dc25763cad95f7daa8585c4ab7d98d47d00b51fb4b6a52f09
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264837156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8884d0d3b758b0b8185e3d53b70df69bffbccf6df3f07fbf4b3e25df1b20cb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 13 Jan 2026 23:34:02 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:35:32 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Tue, 13 Jan 2026 23:35:32 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 13 Jan 2026 23:35:33 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:35:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:35:35 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:35:41 GMT
COPY dir:889642903e29f32ff0f0b6da5f64cf6a40ecfa6d85d0926e4981ccbc885ac0c0 in C:\openjdk-25 
# Tue, 13 Jan 2026 23:35:45 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Jan 2026 23:35:45 GMT
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
	-	`sha256:1d10c8fcde576a410cc93aba794d1581bcd731f0768bb23e09b216c68c51114e`  
		Last Modified: Tue, 13 Jan 2026 23:35:51 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993b95022cb046a56aacabaacbb001e107db22c7efc1a09b786007b7916502fe`  
		Last Modified: Tue, 13 Jan 2026 23:35:51 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ca078aaf31811b84657a7ebde781fca72272f53aa4822f8a0efa022ce02757`  
		Last Modified: Tue, 13 Jan 2026 23:35:51 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228be9a677a11f9e107bb5219e22562cd5fde88378ea726dd08a613897fd9254`  
		Last Modified: Tue, 13 Jan 2026 23:35:49 GMT  
		Size: 75.9 KB (75925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0bc35f93c44f04138f020580de0d8e205519e68517e72e46e76b6ae9ca3401`  
		Last Modified: Tue, 13 Jan 2026 23:35:49 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dfda07ce9346ca11927876d2874c02e54aebff0c9dbef9cfa805f84f732438`  
		Last Modified: Tue, 13 Jan 2026 23:36:02 GMT  
		Size: 138.0 MB (137951792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52186644096e547d47307a6839b4a5bab1cc0f83ded55c50d03cccf9593e7e6b`  
		Last Modified: Tue, 13 Jan 2026 23:35:49 GMT  
		Size: 106.2 KB (106194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dab82e5c48d1160634162c2532112bc6f9ab028c37ecf51e0d8d88f5aedef35`  
		Last Modified: Tue, 13 Jan 2026 23:35:49 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
