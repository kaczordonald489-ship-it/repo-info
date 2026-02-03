## `openjdk:26-ea-33-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:3b7dd422af849fa269998705048ca26cc85daf23687e422b88acf74b4c404d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `openjdk:26-ea-33-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:fe2f0dfb5a7f36bf71374dd11b15009b8527b04d1aa52fdef96d34a74f53358d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.2 MB (423155614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e56a2b546ff95cd2f4b8e09d663c311cf036319461f08308072222c83e9f0f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Sat, 31 Jan 2026 00:09:04 GMT
SHELL [cmd /s /c]
# Sat, 31 Jan 2026 00:09:04 GMT
ENV JAVA_HOME=C:\openjdk-26
# Sat, 31 Jan 2026 00:09:05 GMT
USER ContainerAdministrator
# Sat, 31 Jan 2026 00:09:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 31 Jan 2026 00:09:13 GMT
USER ContainerUser
# Sat, 31 Jan 2026 00:09:14 GMT
ENV JAVA_VERSION=26-ea+33
# Sat, 31 Jan 2026 00:10:12 GMT
COPY dir:4b0b09721eb8a6a23e669a427b9022937722c5088501379523ae0d075ca2bcf0 in C:\openjdk-26 
# Sat, 31 Jan 2026 00:10:18 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 31 Jan 2026 00:10:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682cb22764550cdf219965aea53123175f7f9e922516dacc51dfa62e8da1be2c`  
		Last Modified: Sat, 31 Jan 2026 00:10:28 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db14f31e16b8b1da83fcc1a0c03814bae19f8f5c096222dd72ad9da3247cdbdc`  
		Last Modified: Sat, 31 Jan 2026 00:10:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cd20e5c99170fa29633ff21d0ed9b51e3a3dac7ff8cc037b8ae039f34e1152`  
		Last Modified: Sat, 31 Jan 2026 00:10:27 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124007c5b337a684a05b20457464ba09cdc1734217793c14fff1533fcb27760d`  
		Last Modified: Sat, 31 Jan 2026 00:10:27 GMT  
		Size: 69.9 KB (69897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5439181426ae77bc8d47422f71e861310a7d9a1946a96591cbbf9cac6205ffff`  
		Last Modified: Sat, 31 Jan 2026 00:10:26 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941735d93d1c326279450be9b4932bb9927623d431f2f32de4dea07de9ec7bdd`  
		Last Modified: Sat, 31 Jan 2026 00:10:26 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b9c69749161f458f26e2139ad6679dab8d2e82090dc011089563b5e4d254c0`  
		Last Modified: Sat, 31 Jan 2026 00:10:42 GMT  
		Size: 223.9 MB (223878929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a024f97447272a6cefd181bd05efeb673285be071cf8772ee83c9a8d6d96fa`  
		Last Modified: Sat, 31 Jan 2026 00:10:26 GMT  
		Size: 123.8 KB (123831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38055a0ebb7a04c61bad75643be2efbb1e8fdde5097a5737ffedf02dd431571`  
		Last Modified: Sat, 31 Jan 2026 00:10:26 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
