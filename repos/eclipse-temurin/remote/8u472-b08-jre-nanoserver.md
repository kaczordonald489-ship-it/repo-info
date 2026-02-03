## `eclipse-temurin:8u472-b08-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:c3168a4adf12a8bbfa10c65adf5b51752915a05f2dc04dcdfb41b55c99151c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:8u472-b08-jre-nanoserver` - windows version 10.0.26100.32230; amd64

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

### `eclipse-temurin:8u472-b08-jre-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:07cd8699353168f334e8471b87f6c49c5428b30d6f91515085214ac2a437613c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167433738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37c60628e1870819c99269de55231e7081b2a933569b20e5b72350684da2b23`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 13 Jan 2026 23:34:00 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:34:00 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 13 Jan 2026 23:34:00 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 13 Jan 2026 23:34:01 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:34:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:34:03 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:34:06 GMT
COPY dir:d46ae848a780de83988aca6679aeefb6cb592f306ae2eca344ddb66bc6559a89 in C:\openjdk-8 
# Tue, 13 Jan 2026 23:34:09 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc58112f1d1d638f65a75c8bcdb844fc8acda257ce27f49b05ca59ae6852b63`  
		Last Modified: Tue, 13 Jan 2026 23:34:15 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4bf1f48fdd87de04aaf7774e6d6d93cc6df6bf8cc9b77378edd21bb7298393`  
		Last Modified: Tue, 13 Jan 2026 23:34:16 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6553d6d9ed2a18003815afb769163b97f88e92339de05d60197f2d440cec206`  
		Last Modified: Tue, 13 Jan 2026 23:34:15 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a45cfcb51bbbea939ebb61881d8ff15bf4f4f5e98658627d072378de8e92dbd`  
		Last Modified: Tue, 13 Jan 2026 23:34:14 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3348de03407e7a64d7aa16d0672e9de247e692f89f8fc3979ec860c818b903`  
		Last Modified: Tue, 13 Jan 2026 23:34:14 GMT  
		Size: 77.6 KB (77647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42737df7d6f0be5df1d3c5774b08486804b91c36c8419672163db10dc267135`  
		Last Modified: Tue, 13 Jan 2026 23:34:14 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65e1abf922bdb93718ef31703984018bc8e8560c69ca3a724424aae7f1fda3b`  
		Last Modified: Tue, 13 Jan 2026 23:34:18 GMT  
		Size: 40.6 MB (40555105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c52ce534dde8f197a0476c8d6325f0b1ef798904f4ac22aa6666654d247e1e`  
		Last Modified: Tue, 13 Jan 2026 23:34:14 GMT  
		Size: 98.9 KB (98907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
