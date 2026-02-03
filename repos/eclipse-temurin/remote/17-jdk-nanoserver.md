## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:5b3098f565cb87833063c6cffc6118706592ee8314c554c13698ae0bb7478a8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:3b8a5c56b1ef5c82774c9ce0917da03a79bb4f903d2373cbfd0604f0d2a7504e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.8 MB (386768438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd70b40b5ba3aa810faf426ac9b4f916c0ab8b07597bc7054229b9daae3e68e4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 23:39:23 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:39:24 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 13 Jan 2026 23:39:24 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 13 Jan 2026 23:39:24 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:39:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:39:30 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:39:44 GMT
COPY dir:2018c1c9eb6dc671bed9b2018ab32e648d405ad10a017a184613d399d49818ed in C:\openjdk-17 
# Tue, 13 Jan 2026 23:39:49 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Jan 2026 23:39:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449a8f38121ad9ab7bb32fd54119825e5f6c3a13152940fa400e7a44dd22a6bf`  
		Last Modified: Tue, 13 Jan 2026 23:39:55 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c0edb3b9a23e4ffd0be481b1f432562f47fa7464f857c9d74c298a1d454849`  
		Last Modified: Tue, 13 Jan 2026 23:39:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acb424cf073417dc2728cb85c6096157054bdd87e2b6c12889a65923e122401`  
		Last Modified: Tue, 13 Jan 2026 23:39:55 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c332f77b7806c31009aebb1efc6ea00df7db31439a7de14c0f16d58790e89171`  
		Last Modified: Tue, 13 Jan 2026 23:39:55 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02196ae2f036ff52895f3e8f051f287ef93876a3e0b1ee7e5483436ab1f93a3`  
		Last Modified: Tue, 13 Jan 2026 23:39:54 GMT  
		Size: 70.6 KB (70628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c33ddcfb9ae81eb0fb1498717d7aa84f9acc4f2d02b5af4811ecc9911adcfac`  
		Last Modified: Tue, 13 Jan 2026 23:39:54 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1750d7ae9f9f795bb91fd02b0fcf326706f94987b6328fa4adba43e552fc756`  
		Last Modified: Tue, 13 Jan 2026 23:40:06 GMT  
		Size: 187.5 MB (187510870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517023251aa77eb2719943de497c1032f91e2056b12bc9915cea2347139a7b0d`  
		Last Modified: Tue, 13 Jan 2026 23:39:54 GMT  
		Size: 103.9 KB (103948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610c0b783211014cec78952d6efea70c4fab314897770652e867c5933539958`  
		Last Modified: Tue, 13 Jan 2026 23:39:54 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.4648; amd64

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
