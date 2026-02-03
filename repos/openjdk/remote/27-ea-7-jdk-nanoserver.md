## `openjdk:27-ea-7-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:806a6fa50ad7f86061b05af2338fa9aeb5cd6b3508dabb0298115688dbdd5761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `openjdk:27-ea-7-jdk-nanoserver` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:99154afe1adafeec3d03282871b59c1f6e344b8a972ed95b8d3faec23f994146
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.5 MB (423470458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283c1a57d67be458fb28d09f39a69051a287f815f9fdfbcdc9246b8785d0d9a5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Sat, 31 Jan 2026 00:09:11 GMT
SHELL [cmd /s /c]
# Sat, 31 Jan 2026 00:09:11 GMT
ENV JAVA_HOME=C:\openjdk-27
# Sat, 31 Jan 2026 00:09:11 GMT
USER ContainerAdministrator
# Sat, 31 Jan 2026 00:09:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 31 Jan 2026 00:09:18 GMT
USER ContainerUser
# Sat, 31 Jan 2026 00:09:19 GMT
ENV JAVA_VERSION=27-ea+7
# Sat, 31 Jan 2026 00:10:04 GMT
COPY dir:76eebc3ec90e26d61797b94158298a9f6d9a357a62ce831433f35d5314564117 in C:\openjdk-27 
# Sat, 31 Jan 2026 00:10:10 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 31 Jan 2026 00:10:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c3e19264a96161572d167a79b682d75ba9473e6bd8f158f0316d7bdec9d27f`  
		Last Modified: Sat, 31 Jan 2026 00:10:21 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabc9bb13ce1b8d5b4ffb2a64ae2149aa4840b4ceda80e0a3658538bfd39854a`  
		Last Modified: Sat, 31 Jan 2026 00:10:21 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5334685a5ad830650d2c23920175171df6abaea430fd484079fc9fb9bef6ff6`  
		Last Modified: Sat, 31 Jan 2026 00:10:21 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d51bbf511a1b7faa3e332c67983243735f2d671403a5599053c55c4cb8541b`  
		Last Modified: Sat, 31 Jan 2026 00:10:21 GMT  
		Size: 69.6 KB (69601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9d094ab2995b47c22c79e14b80d7dc43c0e3b221dcdb0b170d10bb4318c681`  
		Last Modified: Sat, 31 Jan 2026 00:10:19 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dec39097829617d5a22a5d8f261d4b67b8bfd9f28d6ef9e982f30fca8c9518`  
		Last Modified: Sat, 31 Jan 2026 00:10:19 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4ea48553139bddc0c88ffa13a5788f7068a0a839f853bfcdffc8fa6c1e3e3`  
		Last Modified: Sat, 31 Jan 2026 00:10:35 GMT  
		Size: 224.2 MB (224233032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f20dc1c93ffe77d28cf53b10db46cc3b6ea612babada15b7f50da58315d4a0`  
		Last Modified: Sat, 31 Jan 2026 00:10:19 GMT  
		Size: 84.9 KB (84877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9820a3c28971cf87193903996c0eb85b5cda825fba759463856b69bce1e92c6c`  
		Last Modified: Sat, 31 Jan 2026 00:10:19 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-7-jdk-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:25c32c57fd5628af2a13bf56a86289bdd09de3618d6d9c1dc868f96aabd6b5b9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351115714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33610083adda61dc0299276df7e21bcb5c5b8f7d08d1ab5bb66d1bc2cf3bd4f5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Sat, 31 Jan 2026 00:09:25 GMT
SHELL [cmd /s /c]
# Sat, 31 Jan 2026 00:09:26 GMT
ENV JAVA_HOME=C:\openjdk-27
# Sat, 31 Jan 2026 00:09:27 GMT
USER ContainerAdministrator
# Sat, 31 Jan 2026 00:09:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 31 Jan 2026 00:09:34 GMT
USER ContainerUser
# Sat, 31 Jan 2026 00:09:35 GMT
ENV JAVA_VERSION=27-ea+7
# Sat, 31 Jan 2026 00:10:16 GMT
COPY dir:76eebc3ec90e26d61797b94158298a9f6d9a357a62ce831433f35d5314564117 in C:\openjdk-27 
# Sat, 31 Jan 2026 00:10:23 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 31 Jan 2026 00:10:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e96615bad713aca1668b1467324113d0a13c02d501e71a0632b194c36f80ea`  
		Last Modified: Sat, 31 Jan 2026 00:10:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dff01f24d8622d2160561b62a49cf916c79b4ec78b84961699a3b32dbeea4f0`  
		Last Modified: Sat, 31 Jan 2026 00:10:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6148e9f4c3c1802a00e3c877c9aa77a359afdbf5165b8bbe23efd6ad612042fb`  
		Last Modified: Sat, 31 Jan 2026 00:10:29 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aa3ff3f6a5ec2c9c4e1e8dc7495bea0418fb6689285b1bba5f93e51abb542d`  
		Last Modified: Sat, 31 Jan 2026 00:10:29 GMT  
		Size: 71.3 KB (71344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d800da4d8375a9081fb36fcc2be53a65b044ae0407880eeed3e991ddcb645f85`  
		Last Modified: Sat, 31 Jan 2026 00:10:27 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3404c9c6b698ead5c2a32b41db5df2685a61cc15ac53d90d1bbca96694276e`  
		Last Modified: Sat, 31 Jan 2026 00:10:27 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c89c4db7dcf2cdb02f1c3c83eb27ae32cf85964b63a34d052d3fcbc32fe739d`  
		Last Modified: Sat, 31 Jan 2026 00:10:43 GMT  
		Size: 224.2 MB (224232761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82d0a0d2372ee8d22d58073675983b93efb63c9b9f0b6f00bb0851e1f6ff0ab`  
		Last Modified: Sat, 31 Jan 2026 00:10:27 GMT  
		Size: 108.3 KB (108330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b609d11cca4b79c4ff94732facbd43fce80206d0f8c9ed66cb3e63b8b882b63`  
		Last Modified: Sat, 31 Jan 2026 00:10:27 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
