## `amazoncorretto:17-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:9d082281d2d8203706616f976eaa105b2d486788846b0957a8b6d20ca5befa84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.22` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:823319681d75ccb0cf679db392ed6a8157f8eadd494bd81c92ad76158cdd4a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152173521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba3025f170d6293fcb10df36328bcb434383af0114a37606f5dbb660286524a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 21:34:56 GMT
ARG version=17.0.18.9.1
# Thu, 29 Jan 2026 21:34:56 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 29 Jan 2026 21:34:56 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:34:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 29 Jan 2026 21:34:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6385f56fa35456a377e4b701547498f0952a5a5884c77a34a68c04ac2514ca20`  
		Last Modified: Thu, 29 Jan 2026 21:35:15 GMT  
		Size: 148.4 MB (148368646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1447031be6e6f204380a206809ea021f2d43ce861f22876928f2a3b0966f1ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.5 KB (592510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6704e23edc76df7a05dd74f41ead95ed1223bdcaf1bab6f1b76c1b731b8cce`

```dockerfile
```

-	Layers:
	-	`sha256:b96ce94fc49c869b3551f8c2f4102574933d31fac03377a93f5131d871f5af6b`  
		Last Modified: Thu, 29 Jan 2026 21:35:11 GMT  
		Size: 583.1 KB (583136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da1f705d849c812847a8a02166fac68d7f95f490d7b54eab8566b4e2fa42445`  
		Last Modified: Thu, 29 Jan 2026 21:35:10 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fa55703ebe3b01ee1508165e06f078a4cd99ccb45213b20d36a7b7c1152284f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150852759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33168c6567c6243eb91938a13771d1da3bd2504464a0498a2359e038f7359110`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 21:33:20 GMT
ARG version=17.0.18.9.1
# Thu, 29 Jan 2026 21:33:20 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 29 Jan 2026 21:33:20 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:33:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 29 Jan 2026 21:33:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d28d00aa6a1621f4a5cfb04538b97665506621daa9986b5eb0ddcf60e02b6`  
		Last Modified: Thu, 29 Jan 2026 21:33:37 GMT  
		Size: 146.7 MB (146713240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d483065c9d8bd7efa0d842d2a8583a25e88a1ee6579018bd67138fc4a4be40a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.0 KB (592033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a713b0a7ddcf26b480940f7607e8f9dab3bc47b89b98be00af8a8752903e08f`

```dockerfile
```

-	Layers:
	-	`sha256:141de07c7a687e3cf57ef7bdbb137eaaa61479d18f74e959aa75d796365add1b`  
		Last Modified: Thu, 29 Jan 2026 21:33:34 GMT  
		Size: 582.6 KB (582555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:376742ea3283e2bcbcc441c6a8ac448712db57513b822e81436aae2348cdc1f7`  
		Last Modified: Thu, 29 Jan 2026 21:33:34 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
