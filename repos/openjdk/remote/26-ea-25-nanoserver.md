## `openjdk:26-ea-25-nanoserver`

```console
$ docker pull openjdk@sha256:8c50ba56b399f3be0bc0c64fa97b6c4ebd6d28fce36e60519d24f0fab632a48f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `openjdk:26-ea-25-nanoserver` - windows version 10.0.26100.7171; amd64

```console
$ docker pull openjdk@sha256:8b86b4acbac9ff53a97531f189910def1abd6de484c473b45521dbdcbec1aecd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.4 MB (421398413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb654767dc5496da9650d0206014cf139294f2048ccae33f89e978b13c521dad`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Mon, 24 Nov 2025 23:14:32 GMT
SHELL [cmd /s /c]
# Mon, 24 Nov 2025 23:14:34 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 24 Nov 2025 23:14:35 GMT
USER ContainerAdministrator
# Mon, 24 Nov 2025 23:14:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 24 Nov 2025 23:14:49 GMT
USER ContainerUser
# Mon, 24 Nov 2025 23:14:49 GMT
ENV JAVA_VERSION=26-ea+25
# Mon, 24 Nov 2025 23:15:58 GMT
COPY dir:05b9f2f26dbe5a838bb1099ecf20e5ed19fee08619b465df90f821afcc5c8301 in C:\openjdk-26 
# Mon, 24 Nov 2025 23:16:08 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 24 Nov 2025 23:16:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0019def9eb0001626dfeec44b68d6fcc09216d76d4599798923d7c510f4f731`  
		Last Modified: Mon, 24 Nov 2025 23:16:37 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae71dc8c187052732424905e071add352456a6ea1ec4375a96ee09b11ae71d30`  
		Last Modified: Mon, 24 Nov 2025 23:16:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe802802ab32f1b095beba9f8df55eef67e29b1c47c6f44e6eb537732238369`  
		Last Modified: Mon, 24 Nov 2025 23:16:37 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3f0161046bc78271234cbedbf8fed92761bbbf2e1cdf445277fc9823e3ecb4`  
		Last Modified: Mon, 24 Nov 2025 23:16:37 GMT  
		Size: 71.9 KB (71880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75272604e10d53581f0f4727ed75698ee4a5791f18d6d53c46a32ef3b825406d`  
		Last Modified: Mon, 24 Nov 2025 23:16:37 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0709da459a4f021117036d5df5c2aa3d10f018e2a017295949b169cbd0687dff`  
		Last Modified: Mon, 24 Nov 2025 23:16:37 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f871598fba416dce69c9a19300782ae8329eaf254373a1228f20c08015efdac9`  
		Last Modified: Tue, 25 Nov 2025 01:24:18 GMT  
		Size: 223.3 MB (223260100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0684d11e76661ed38fd08b5392b9f0e4b0ba796c51949c702baeb1e91f4d2ed`  
		Last Modified: Mon, 24 Nov 2025 23:16:37 GMT  
		Size: 123.5 KB (123524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68495fe619a2e728332256f937c34d1b60700804d8dae3eb495e5889ec223905`  
		Last Modified: Mon, 24 Nov 2025 23:16:37 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-25-nanoserver` - windows version 10.0.20348.4405; amd64

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
