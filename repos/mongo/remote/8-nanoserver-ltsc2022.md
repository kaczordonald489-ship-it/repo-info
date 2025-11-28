## `mongo:8-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:65b2527991ba5a86e909211598b37b2d5a697a41b9839b5f4028f1e48bb78c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `mongo:8-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull mongo@sha256:3ead94ec9be8217afcff66976f3f00891b3fc11b936cf5487aaa68e0ba00d2a0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **940.7 MB (940696896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10c060b703dea572070b1cb557eb8bdb7d64d71484dd12c61d482f67cb40780`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 20 Nov 2025 00:27:02 GMT
SHELL [cmd /S /C]
# Thu, 20 Nov 2025 00:27:02 GMT
USER ContainerAdministrator
# Thu, 20 Nov 2025 00:27:06 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 20 Nov 2025 00:27:08 GMT
USER ContainerUser
# Thu, 20 Nov 2025 00:27:10 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Thu, 20 Nov 2025 00:27:11 GMT
ENV MONGO_VERSION=8.2.2
# Thu, 20 Nov 2025 00:27:50 GMT
COPY dir:34b17986dc7f69da0f0036b088796e7e44f1eda590d700b8613e7d7fcb8f43d9 in C:\mongodb 
# Thu, 20 Nov 2025 00:28:14 GMT
RUN mongod --version
# Thu, 20 Nov 2025 00:28:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 20 Nov 2025 00:28:14 GMT
EXPOSE 27017
# Thu, 20 Nov 2025 00:28:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2e66ec09344e865d88dd24b74f4db64afc996301489233928f8b6dd119bdc4`  
		Last Modified: Thu, 20 Nov 2025 00:29:44 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a45efd4a9d458cb2a364b5dbf455866aba9180001525634e94b8f18489ac5d`  
		Last Modified: Thu, 20 Nov 2025 00:29:44 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887f0bfdf44096126d2881cfe79a8b5456d671c3f6dbf987c2837b36432e9539`  
		Last Modified: Thu, 20 Nov 2025 00:29:44 GMT  
		Size: 70.6 KB (70589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded437782dd8e6d10e05216c79cc1c08d14edb9ba897f8eb2f024361afc608b2`  
		Last Modified: Thu, 20 Nov 2025 00:29:44 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d721995962bd996213ca2fef8261c2110842bbc090b5b80e24e1c928d0fc38`  
		Last Modified: Thu, 20 Nov 2025 00:29:44 GMT  
		Size: 275.2 KB (275215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853ce2962c88559dd914be714d10b510fcc659b0fd00517445f037ac272ad304`  
		Last Modified: Thu, 20 Nov 2025 00:29:44 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78d142314f4387345fdfca545e7a72edb90df9107e06c3117ee5fd639b7f2e5`  
		Last Modified: Thu, 20 Nov 2025 02:08:35 GMT  
		Size: 813.9 MB (813906854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483529b3c60100dff5d093505594ccf1fa8b8b95b15e190b898f53a4b45c3b1e`  
		Last Modified: Thu, 20 Nov 2025 00:29:44 GMT  
		Size: 87.6 KB (87645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39bf27c745d5c10c156542f9b2b41463ba104d23beb909ec04a0f741bd63acb9`  
		Last Modified: Thu, 20 Nov 2025 00:29:44 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7cc03e44015fd4e8d90af1dc695311d79b363232b8b042b7bb645d17fdc38b`  
		Last Modified: Thu, 20 Nov 2025 00:29:44 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8a57c8342e007d57349cc8b9bb04dd7ae59ed62114a36d837fa7352f796612`  
		Last Modified: Thu, 20 Nov 2025 00:29:44 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
