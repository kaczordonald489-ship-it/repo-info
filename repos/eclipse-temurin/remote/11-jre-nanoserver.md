## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:62c43fb1ee547cf42da2f3db47605ea063ed776d1dac86011b36e077854657df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:64769529fb5df8d958e5c18a96393826aeb40f4e7bb83eea24f935618aa0b4b0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242951999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18864200db5c6d55656d8e105ac544b5cbb24bc77c30ebe7ae7f91a14d3d0601`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 23:38:54 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:38:55 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 13 Jan 2026 23:38:57 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 13 Jan 2026 23:38:58 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:39:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:39:02 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:39:08 GMT
COPY dir:4835e564d5b678d207d3850b6f40a90e0afa12e9d665c48e7909a88923b1a7a8 in C:\openjdk-11 
# Tue, 13 Jan 2026 23:39:12 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c3018f35c73af59a36350615c430cd199174009bb767471c37deb2372b9478`  
		Last Modified: Tue, 13 Jan 2026 23:39:18 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4439769f1bf0b87f77b9deecb91d2ba9bf0b20e94f929cbc18a174ad60fa976`  
		Last Modified: Tue, 13 Jan 2026 23:39:18 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfcb5dabc365b64c030fdc3e4f441ae4af3a628c988200a10c70ef7c0096f39`  
		Last Modified: Tue, 13 Jan 2026 23:39:18 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28452a5492665bb5348c68b763ab8e33341e92ffe3bd531c5f3c62bae4b8da6f`  
		Last Modified: Tue, 13 Jan 2026 23:39:16 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb86e56ae7385a93c920ef6382e89750ffa07f91d1f232d6cafaa29175ce60c`  
		Last Modified: Tue, 13 Jan 2026 23:39:16 GMT  
		Size: 71.3 KB (71338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0ad30e40bfb6fca7a5abdd572ccad76453c14747626f3e0694a44691e07923`  
		Last Modified: Tue, 13 Jan 2026 23:39:16 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7af5d9222134f014477822b7f6d5b1c9973e66c9b7e1eac4d3953da3df580d`  
		Last Modified: Tue, 13 Jan 2026 23:39:22 GMT  
		Size: 43.7 MB (43695068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f122ac1b0a3234ef536cc858aae5382be24c3a639faf52eb8e507294565e68`  
		Last Modified: Tue, 13 Jan 2026 23:39:16 GMT  
		Size: 103.7 KB (103687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:e69c924f3f30cb691ad48bd0d2344ca655d7c4e7e95d7215d4b2f18f692f8d3a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170564675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e796487acffb6e54f54185a773dc01b456d0d40274aa6fa5f0130ce7c1e18cb5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 13 Jan 2026 23:34:09 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:34:09 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 13 Jan 2026 23:34:09 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 13 Jan 2026 23:34:10 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:34:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Jan 2026 23:34:12 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:34:16 GMT
COPY dir:4835e564d5b678d207d3850b6f40a90e0afa12e9d665c48e7909a88923b1a7a8 in C:\openjdk-11 
# Tue, 13 Jan 2026 23:34:18 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98bbecdd0bcd40d16482ede27cc28f3c57f40602c77e88d2a179c072e2a73fc`  
		Last Modified: Tue, 13 Jan 2026 23:34:24 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b6789c084571b69cf3f4fac202ecedde9b9293148d3e59e5fc965bdf462eba`  
		Last Modified: Tue, 13 Jan 2026 23:34:24 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aba17fd6cbd1967870778c9759737cea4f809fef7124e9c6f7f83f1bc8019ff`  
		Last Modified: Tue, 13 Jan 2026 23:34:24 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fff3601ba9bc5122fc63eec816bc14c8616eae6a9a4d4eba7591bd8e02c1d58`  
		Last Modified: Tue, 13 Jan 2026 23:34:22 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ed3483479e45e8d22bbc013945045685d530771e7daba60ca32b8137e29f21`  
		Last Modified: Tue, 13 Jan 2026 23:34:23 GMT  
		Size: 77.0 KB (77023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7a4d079187bbe65097e08ec2dd5686a4d01698340de0f4bfa9095124ee29546`  
		Last Modified: Tue, 13 Jan 2026 23:34:23 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20e8cc8b45243f7445001e890d5ba931342e65d19f6d2b82d9626883c70e3c`  
		Last Modified: Tue, 13 Jan 2026 23:34:28 GMT  
		Size: 43.7 MB (43694914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a76fee2002bea74d763ce89974dc051f758db11606f39002edb2728598a07d5`  
		Last Modified: Tue, 13 Jan 2026 23:34:22 GMT  
		Size: 90.5 KB (90498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
