## `openjdk:27-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:9e08307a5c8c3807f0cb1de2d38bed5e2c3a9f1204d887bfd647a5d9b0c39d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `openjdk:27-ea-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

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
