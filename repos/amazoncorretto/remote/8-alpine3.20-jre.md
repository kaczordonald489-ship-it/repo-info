## `amazoncorretto:8-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:6228b225d9a5d791f46cee113e6d5c4f55691c08f7d69e6add7f0faac3b8cacd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b1f617f94dd0b54f5c5ccbb95ed69bf21d015ee6a79a3b735e505e856d124831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45370773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a848d8d585ae1c855c096959414bf316c46881f8acf3aef69ccc75c330544c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:24 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:40:24 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:40:24 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:40:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbcd30cf2aede157c58c52c3a5cff221dc086aff9c63656bee43dbb136a5645`  
		Last Modified: Wed, 28 Jan 2026 02:40:34 GMT  
		Size: 41.7 MB (41742909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d494782adfad6545298cc0d8cf674172c645b77121f4c8eecd76274aa6e8f1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 KB (191474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c424c3e42e49b1f7d8cf6a0a8c455ec030e9883cff7e8a2ed8cb28d7dcae3ea3`

```dockerfile
```

-	Layers:
	-	`sha256:1430383f55adaef2917014f3181f6d80c2d37f07865dd7d6b685cdc716c9a950`  
		Last Modified: Wed, 28 Jan 2026 02:40:32 GMT  
		Size: 182.8 KB (182818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08bea4138d773d86f682cfa0662c089cf193e41180b47e6f42300c736d2580a7`  
		Last Modified: Wed, 28 Jan 2026 02:40:32 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6caa2cd10311baeffa8980842b2707e070d22067408defbe26dc5d012c66b783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45548177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b38b76f4bb28c5e7d3cc695b4537e698c09c76d201d18e8a0fa0b332210e82d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:51 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:40:51 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:40:51 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:40:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7b208a3d0a3a6fd63db8af817b61a9d041730c604a0b50a1d174294a898867`  
		Last Modified: Wed, 28 Jan 2026 02:41:01 GMT  
		Size: 41.5 MB (41458219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fea147cddfc0a7d28f0faf0bdf306dbabab958691516826abecae0b2c581d7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 KB (191661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3353b12961f2e5394cd79c8a799da55968235bb940295a010fa8ffe1fbc1482`

```dockerfile
```

-	Layers:
	-	`sha256:4d9658108618e8e7e2b6e4b5af6f9db37b9214a9c8c4130616e04df41213ad76`  
		Last Modified: Wed, 28 Jan 2026 02:40:59 GMT  
		Size: 182.9 KB (182926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ca97024a81bba571ca8ed24a910fe4d7e166050fe4c8806996bb6fa955c37a`  
		Last Modified: Wed, 28 Jan 2026 02:40:59 GMT  
		Size: 8.7 KB (8735 bytes)  
		MIME: application/vnd.in-toto+json
