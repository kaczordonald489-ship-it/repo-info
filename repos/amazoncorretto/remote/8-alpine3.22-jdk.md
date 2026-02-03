## `amazoncorretto:8-alpine3.22-jdk`

```console
$ docker pull amazoncorretto@sha256:f04ca03f002da525ba20134a41ccf91959f9db2e87525874784739d932f9959c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7075877a4bb1386192e95e4d2adab97f35c18dd5059d3091025d426b85a2366d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104579785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144bee287d3a4119ab32b554b41a35c35fd9fc109e14c09882fdbd023e2cc0a6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:42:10 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:42:10 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:42:10 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:42:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:42:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f9a43f049ea25a81da607ffb2173ccbd05bf1c4e5e479384ebfd9309a10462`  
		Last Modified: Wed, 28 Jan 2026 02:42:24 GMT  
		Size: 100.8 MB (100774910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f81ff5cf2f6099591ef2b7bbc99e871dab828f1c6ca599e3f97a82a708545f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 KB (257029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c1bf89067f99ca7dfa12cccba7f0432e93b0246dca43be47c61a407214df3c`

```dockerfile
```

-	Layers:
	-	`sha256:f683283eafee5f8b3d7799525197ffb2a50fa722393869110b205e4f7f0e0065`  
		Last Modified: Wed, 28 Jan 2026 02:42:22 GMT  
		Size: 247.7 KB (247674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6682bdd3ef7fb62066a7adf183baa4ce0f1dfb150e7955e70fc8a17103f1705`  
		Last Modified: Wed, 28 Jan 2026 02:42:22 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0ec907d3e945badf0976ba6c0a4e6b46446cdd99864ece031e3e71bc6724ca37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104700699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0acb52437c63783af83b0ad31a3d67f88a6fdcefdf9badd716f73f94bcc9719`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:42:51 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:42:51 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:42:51 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:42:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:42:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4254d7e7050666c4c4fbb0583edfead90f52e83e8b48e41a8f8f0ee3c4963f17`  
		Last Modified: Wed, 28 Jan 2026 02:43:06 GMT  
		Size: 100.6 MB (100561180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:45435f0e2d5662225c870525522b9d7186b0670cc2fa19bd91c0fa78c95e7683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 KB (257265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854abf47f8565fdcecb3a335d9b4f4fed0e8abb488e18064d2531776acde42a6`

```dockerfile
```

-	Layers:
	-	`sha256:f8f1722c35a3b317169d9520aa398e7e8a8af1c70fd3b59117369ed1968ccb25`  
		Last Modified: Wed, 28 Jan 2026 02:43:04 GMT  
		Size: 247.8 KB (247806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac2f907b1145b75a0fdb7a2fc8b37d7e9d5a224c3d309f4f5e188eb4f01fff99`  
		Last Modified: Wed, 28 Jan 2026 02:43:03 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json
