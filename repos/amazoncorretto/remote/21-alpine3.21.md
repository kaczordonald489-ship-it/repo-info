## `amazoncorretto:21-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:1db2673b2e2a3fc87c0901f8005af1a6c6a19f26d73b97a9d83bd742f0ff2710
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c82701d37271d4e256f4c2ec34ef205e17f78006023477d662b17e66668aaef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165230856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f917c14f073c12cf36b3b883301b8baf2980523f6c59c86d38f903f8473a397d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:49:22 GMT
ARG version=21.0.10.7.1
# Wed, 28 Jan 2026 02:49:22 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:49:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:49:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:49:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd04bf1efc378da2cc76cc6f805928dbf3b8b5916c6ce49f0ecbb3143e96c3c4`  
		Last Modified: Wed, 28 Jan 2026 02:49:41 GMT  
		Size: 161.6 MB (161587114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:35850bb54220c0ff1bbde38a79307cb5a5c19415185a6313e3dcd5612ae9cec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.8 KB (595836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba80cde1f3a428065b9987ff0cfa38bc1795570317ef92ecc6c5238dbd6045f`

```dockerfile
```

-	Layers:
	-	`sha256:a99fb2b126cf1f08650628849c7ff2ee58c6cad1848f160fa408eeb2bc9d1e4d`  
		Last Modified: Wed, 28 Jan 2026 02:49:38 GMT  
		Size: 586.5 KB (586462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7d61dbe84e0323493cdd08d4269c69539395cbdd50d43401f6509f341514c37`  
		Last Modified: Wed, 28 Jan 2026 02:49:38 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:be523350ca6ff2eda9615d5a790664b31d6d399d76823a1923220821b8e7c57c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163600151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45197df8c2f41247c666a71e04bac10c9a8eb18acea03e62c7404d92e1ed5fe6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:50:10 GMT
ARG version=21.0.10.7.1
# Wed, 28 Jan 2026 02:50:10 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:50:10 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:50:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:50:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c900cbeb3bf0d6c86b211a9e672d4de8a4bd18353142baaaed73fb0755641b`  
		Last Modified: Wed, 28 Jan 2026 02:50:29 GMT  
		Size: 159.6 MB (159607271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:47ea5246dabb87e40d203b7227c81f1428e3c7f04c608b8c3650b5f2bc395816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 KB (595359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f2a291de910f7c43703ac9393b13ed160fe1b29f1184da8921f305330ca6d1`

```dockerfile
```

-	Layers:
	-	`sha256:52efa88461efc491f036036d53dccbfe0895ed12f8cea64a3d031ce1fb0ffa88`  
		Last Modified: Wed, 28 Jan 2026 02:50:25 GMT  
		Size: 585.9 KB (585881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:052ec6cbd44d0eaa35487a3a2f066f2d0de0993ef140de2ae28adc6bb17b6e88`  
		Last Modified: Wed, 28 Jan 2026 02:50:25 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
