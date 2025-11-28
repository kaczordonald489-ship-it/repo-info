## `openjdk:26-ea-25-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:f23ff598e00a120ad903654ce02106afdf652e68d293a922a6be141b05353dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `openjdk:26-ea-25-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull openjdk@sha256:7e8d71f21272efb204e6f3ad4f1c3da6de0a37533753b9f4a94ba65445f251a9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.8 MB (349794148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144c69f3314864ef386b38ed2b1a80ee18dba04f151c0a9a6ab43c8728887e6a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Mon, 24 Nov 2025 23:12:23 GMT
SHELL [cmd /s /c]
# Mon, 24 Nov 2025 23:12:25 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 24 Nov 2025 23:12:25 GMT
USER ContainerAdministrator
# Mon, 24 Nov 2025 23:12:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 24 Nov 2025 23:12:38 GMT
USER ContainerUser
# Mon, 24 Nov 2025 23:12:38 GMT
ENV JAVA_VERSION=26-ea+25
# Mon, 24 Nov 2025 23:13:44 GMT
COPY dir:05b9f2f26dbe5a838bb1099ecf20e5ed19fee08619b465df90f821afcc5c8301 in C:\openjdk-26 
# Mon, 24 Nov 2025 23:13:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 24 Nov 2025 23:13:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484690b3ec068e04bd5855d863e773c98bad0a043cec4d286e297d8a51766e85`  
		Last Modified: Mon, 24 Nov 2025 23:14:20 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fccea5fec619a065b977019ba1b0849f8081e04ea4e0136cc36e022c7f4b75`  
		Last Modified: Mon, 24 Nov 2025 23:14:20 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78629baa842578ae4ae2b56403d080491a2148ee794e50a3c6484aa754b0041`  
		Last Modified: Mon, 24 Nov 2025 23:14:20 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5546f82b43a6ef1e4cbb779da59da465a3d9af274532ffaee9ec4ed51a5b01c9`  
		Last Modified: Mon, 24 Nov 2025 23:14:20 GMT  
		Size: 70.6 KB (70559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837ac0d762a5bb895d33c418c6c4f09a9e92d349d45e4f1e048b6b4eefa79339`  
		Last Modified: Mon, 24 Nov 2025 23:14:20 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058495e51a63d7324b852a24ce64ced4b7d6a4d19713283ebd721f3d33692145`  
		Last Modified: Mon, 24 Nov 2025 23:14:20 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2944073c7f6630f98c211107c32358622d1a5a1145f3667ddced2a14dad7fa8`  
		Last Modified: Tue, 25 Nov 2025 01:24:22 GMT  
		Size: 223.3 MB (223260706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b531f457891448baed04bab5a88c1e3d9f66663627d1f2967d12259fb11e9fa`  
		Last Modified: Mon, 24 Nov 2025 23:14:22 GMT  
		Size: 107.4 KB (107405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ad56f6504d8e9ac067449a89583baf692341000a3d85a59d87c573ae133e52`  
		Last Modified: Mon, 24 Nov 2025 23:14:21 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
