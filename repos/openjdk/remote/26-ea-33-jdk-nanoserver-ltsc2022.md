## `openjdk:26-ea-33-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:ec813b7d2d5d5c1ae477c3381a719ebc3b57a5d2b055b7c98c62c438d17eccf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `openjdk:26-ea-33-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:5066923dd04fd8421d391fbea9104af262c3c84a06edb8db39032492b2385527
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350783910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a049196557d8e0f310449e960eea65a087e70ab79a2d5f380ba9691a6195f31`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Sat, 31 Jan 2026 00:09:28 GMT
SHELL [cmd /s /c]
# Sat, 31 Jan 2026 00:09:30 GMT
ENV JAVA_HOME=C:\openjdk-26
# Sat, 31 Jan 2026 00:09:30 GMT
USER ContainerAdministrator
# Sat, 31 Jan 2026 00:09:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 31 Jan 2026 00:09:40 GMT
USER ContainerUser
# Sat, 31 Jan 2026 00:09:42 GMT
ENV JAVA_VERSION=26-ea+33
# Sat, 31 Jan 2026 00:10:25 GMT
COPY dir:4b0b09721eb8a6a23e669a427b9022937722c5088501379523ae0d075ca2bcf0 in C:\openjdk-26 
# Sat, 31 Jan 2026 00:10:35 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 31 Jan 2026 00:10:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6d2ffdba51777e00582f18574a9979f6652f8a50f977383500a7f518c270f3`  
		Last Modified: Sat, 31 Jan 2026 00:10:41 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3380d85234d9831084c6aafe6f23b1e0d65a6da3896356dc028ed5f9335d80d7`  
		Last Modified: Sat, 31 Jan 2026 00:10:41 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b6fbf3552dea93b385d9b4fefb36cf959bd28e34ee7a4659efd67c360e0f8e`  
		Last Modified: Sat, 31 Jan 2026 00:10:41 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd047bf9e141b2dfd46a79addb44705ee1f2051b3d94aaca366ee9e5c99847c`  
		Last Modified: Sat, 31 Jan 2026 00:10:41 GMT  
		Size: 73.7 KB (73681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1893548cd2d82bec6c2b727467b222472af472cfb8f1f298f356ece7fd322fb0`  
		Last Modified: Sat, 31 Jan 2026 00:10:39 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba0832c8b573a0a765ff34e3f9e18646341f1d243e47b3a3faacda46ff5fef3`  
		Last Modified: Sat, 31 Jan 2026 00:10:39 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c2254e12233208113c11f67759994915784f9750515654a775bfcfa82fcecc`  
		Last Modified: Sat, 31 Jan 2026 00:10:55 GMT  
		Size: 223.9 MB (223878888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05160f0947be415ea4c092c2c7d2c82fb3e24b6ebe5fd19c28f852dde969470`  
		Last Modified: Sat, 31 Jan 2026 00:10:39 GMT  
		Size: 128.1 KB (128119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee209257b19198924bf82da23fc2d83ad1e7d2669836c21e025a47e976fff55`  
		Last Modified: Sat, 31 Jan 2026 00:10:39 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
