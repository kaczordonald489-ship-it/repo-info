## `amazoncorretto:21-alpine3.23`

```console
$ docker pull amazoncorretto@sha256:c64034bdceaff59b33bc366b9ab1b7fc5593d8155daf82cd978541b206555d1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.23` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0cc97139e3485d6a9592f9620be4618f4ae02b739b07c5356db7e01dd9ba37ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165452113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7eb4677b2dff9103504635a2a577b7a05346b52d76f27ed7b249470237e5147`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:50:24 GMT
ARG version=21.0.10.7.1
# Wed, 28 Jan 2026 02:50:24 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:50:24 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:50:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0476ba18ce4a7d863df3375a1843d00caa67c25f77311a8828c2f340ca01d1fc`  
		Last Modified: Wed, 28 Jan 2026 02:50:43 GMT  
		Size: 161.6 MB (161590292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.23` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:09ac6101409d3c1898d0fa804f7cae1153edf4c1c818f209785ff521ce809211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.7 KB (593722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59122cef05dac1e6f4f17efc48a0b28e4e6dfa871826c0b0790b25f1c3f1b4be`

```dockerfile
```

-	Layers:
	-	`sha256:c4c394ca924ab326e1c59a74e6fb98f20035015f616a713bbb247137ab05dd81`  
		Last Modified: Wed, 28 Jan 2026 02:50:39 GMT  
		Size: 583.0 KB (583040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2373e0de644c618814027d3e1e70208ddbc816a74b1766b2ce0b63e52b78873`  
		Last Modified: Wed, 28 Jan 2026 02:50:39 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:211fdb1ee557b74aae569df71aff6779e4848e6f3ae5de26e3a15ba9e9daf392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163812684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75e2e5fbf5aa957976af0f692c5de40cb2fc44826a4c4ca4142cddd72c4c92c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:51:47 GMT
ARG version=21.0.10.7.1
# Wed, 28 Jan 2026 02:51:47 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:51:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:51:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:51:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429b075c73c3fb61a2595fbd83c3d77b387659de25ba9b2d1de05f9d24ee5f70`  
		Last Modified: Wed, 28 Jan 2026 02:52:06 GMT  
		Size: 159.6 MB (159615593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.23` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6c25b341fa6ce05d09b18152b1d053364a8f225826a1e0e09290d6f9dbc896a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.7 KB (592691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f476cced034ad80ae10ee8da38128dde4aa353fc395354701b6fad2e550019b4`

```dockerfile
```

-	Layers:
	-	`sha256:c00cc17e70586da369ee0f8964b22e6c6befe0edcd633e06c2ab0799adf28cee`  
		Last Modified: Wed, 28 Jan 2026 02:52:03 GMT  
		Size: 581.9 KB (581857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69603eb53fbbe3f348ff1ad70c6a72c104c53a0c7bf0b775bf7e7c591f714a32`  
		Last Modified: Wed, 28 Jan 2026 02:52:03 GMT  
		Size: 10.8 KB (10834 bytes)  
		MIME: application/vnd.in-toto+json
