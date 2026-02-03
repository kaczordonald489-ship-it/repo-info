## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:a75618f99c97f57ebf294d4902aa20e7dd24c3274a7e6307f749eeb36b038a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:efe27269dd220002a102e572cf55686f8d4fa6ac77e85c0c70d6822f277b23d4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314397896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a391648ba4120a8b64aefa872fbd3d846afc66e73a945da9d1e2dfd73ad5db0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 13 Jan 2026 23:33:23 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:34:25 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 13 Jan 2026 23:34:25 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 13 Jan 2026 23:34:26 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:34:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:34:28 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:34:35 GMT
COPY dir:2018c1c9eb6dc671bed9b2018ab32e648d405ad10a017a184613d399d49818ed in C:\openjdk-17 
# Tue, 13 Jan 2026 23:34:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Jan 2026 23:34:40 GMT
CMD ["jshell"]
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
	-	`sha256:f0176d296438353774ca5c9b570595ce81851c58bc314dfaa9a69cfda5d2331a`  
		Last Modified: Tue, 13 Jan 2026 23:34:46 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08374232bb12a734770fb8bf47a8fe014b2ed16033656c42442a8a367ea69762`  
		Last Modified: Tue, 13 Jan 2026 23:34:46 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bed35af4e105db41aa8d428b92731362a148dfad848a2621aa6fa485b6fd57`  
		Last Modified: Tue, 13 Jan 2026 23:34:46 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34edb07cd91aa13a3e64233f3caefc7aa5ffd098c7626a2763cf2068d2d0fa9e`  
		Last Modified: Tue, 13 Jan 2026 23:34:44 GMT  
		Size: 76.7 KB (76678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f78956f171bd3e4173de0180bc0c6f48170f7a3f070319ec08e7f5527c27a56`  
		Last Modified: Tue, 13 Jan 2026 23:34:44 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b053edbd958487072119eb5a53a8d229b2ac832b18fed4f3ae97ef7e097e7b`  
		Last Modified: Tue, 13 Jan 2026 23:34:57 GMT  
		Size: 187.5 MB (187511054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49352f2450ed5568aea7196541e107f4c322d52250a36042a0a9fe44651a04d`  
		Last Modified: Tue, 13 Jan 2026 23:34:44 GMT  
		Size: 107.0 KB (106958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117816090a3ab23d7389a5ecf9133e915a393a449bf343854341c27919d61bcc`  
		Last Modified: Tue, 13 Jan 2026 23:34:44 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
