## `eclipse-temurin:8u472-b08-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:26b7c5a49c12fe55df6a2492175f59547a2d2400936d051ebfcc91a2e1e84256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:8u472-b08-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:71ef31b72ec4e8b8c7a67d4c4fdd23330b46ae467422742e9c0c4e1a363a5a93
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239810945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e1495d0bdee219b769ed488eaf74a23240afbdc948d215798347c5a6c5634e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 23:38:47 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:38:48 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 13 Jan 2026 23:38:48 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 13 Jan 2026 23:38:49 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:38:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:38:54 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:39:00 GMT
COPY dir:d46ae848a780de83988aca6679aeefb6cb592f306ae2eca344ddb66bc6559a89 in C:\openjdk-8 
# Tue, 13 Jan 2026 23:39:04 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8eb1f094e5b679fb0ca96745ee5422533f85a56bc0d4fc4531d47d1aa8578ca`  
		Last Modified: Tue, 13 Jan 2026 23:39:10 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0676422138c9315843e86d11841167b6c66f2ae009de578ea731a8a203420b`  
		Last Modified: Tue, 13 Jan 2026 23:39:10 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4fbb0e2ed7abfbc60096a1e3fd895ec04ebb9a97d6a240ee97937810df7988`  
		Last Modified: Tue, 13 Jan 2026 23:39:10 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee70fe3f27344db2c9e0d2e848691e32ba280cf716b32876e1d060863b2d8db`  
		Last Modified: Tue, 13 Jan 2026 23:39:08 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f494a27469fe885638944051fc820992f24042bf21737dc2734beddac19111a`  
		Last Modified: Tue, 13 Jan 2026 23:39:08 GMT  
		Size: 76.8 KB (76812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc789aaa83f17e6c7325c417ff306dc7a7b7b5b5ebf78631b8c09140c92d9146`  
		Last Modified: Tue, 13 Jan 2026 23:39:08 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a6f4c5ee9d565b42a13f9f3e4c8b576037dec277567338c27907a2194e8517`  
		Last Modified: Tue, 13 Jan 2026 23:39:12 GMT  
		Size: 40.6 MB (40555250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac210ed629fc713bf16e61b56de135c528ab7c2d57bdd17d4966430b4b3247c6`  
		Last Modified: Tue, 13 Jan 2026 23:39:08 GMT  
		Size: 97.0 KB (96974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
