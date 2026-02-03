## `amazoncorretto:17-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:a40ee132da6bf9de4aaa9e756297f74c9dcaf67399a0112b2b90cdadb44577e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:82723166c93d2273fc252f05331684a97073ef60e898e7bc810a6e942395276c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (152010354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb2dd2e9f8a0488dd08d72d0a6bec56a3f80c2c4a8b827a13cf833fcb1cb492`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 21:33:29 GMT
ARG version=17.0.18.9.1
# Thu, 29 Jan 2026 21:33:29 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 29 Jan 2026 21:33:29 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:33:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 29 Jan 2026 21:33:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259d316d4dbb5b8bfdc5610e4d11b42b4763b8552846e63e5bfd381c3d716ce5`  
		Last Modified: Thu, 29 Jan 2026 21:33:48 GMT  
		Size: 148.4 MB (148366612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d937199dabb7c84f98fa3b322eb6dd3031d4a8d50d3c9b554af54dbf2e860ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.9 KB (595933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68bffb56c3071da39617bd2fa1152230055b22e5e83c61b86a53f63c42ca820`

```dockerfile
```

-	Layers:
	-	`sha256:4824f35243cdd8e3d5d60e3047a2a255f877f36694229024b868850cf952e735`  
		Last Modified: Thu, 29 Jan 2026 21:33:44 GMT  
		Size: 586.6 KB (586559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a819438715a1b6929ca9d798aa766c84217fca4844f61edbe8d40547fbcd2c65`  
		Last Modified: Thu, 29 Jan 2026 21:33:44 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.21-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ebc7ba70a21ac01b0ea023e092fd8c79fe4d2049caeea2945e5917e67eafba4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150695394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750d0b489081063951a057c780f17da26f56aee9d8abdd9da9c15d43b84527bb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 21:32:56 GMT
ARG version=17.0.18.9.1
# Thu, 29 Jan 2026 21:32:56 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 29 Jan 2026 21:32:56 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:32:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 29 Jan 2026 21:32:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2f064b1739df300854d40532351c5788d7b365b8ec8da8c6b8b431c51f688f`  
		Last Modified: Thu, 29 Jan 2026 21:33:14 GMT  
		Size: 146.7 MB (146702514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5f5d5a72f51574f80d02835cd0491be40e2c04b915aee1db20c6b5d45934c177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.5 KB (595456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083ea00247c33f1cfdd91021961dc328c1aaa79e3b76a313cd6f2ccf34aeda5c`

```dockerfile
```

-	Layers:
	-	`sha256:aa387b0c4ccaf7a136ad7a65e3638c8657640591d4296195a091d644c5fd1bf8`  
		Last Modified: Thu, 29 Jan 2026 21:33:11 GMT  
		Size: 586.0 KB (585978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:192ee2ded85e6021cd50c8e1561b73b457d848ff802cba3a6c16ac56512142a2`  
		Last Modified: Thu, 29 Jan 2026 21:33:11 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
