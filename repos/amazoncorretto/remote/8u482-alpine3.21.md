## `amazoncorretto:8u482-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:f88de1a2e7eaed3848006d85a86cb0a678d537d646160174e06528dd7cc3250b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u482-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8edbc8db43b21f99fa4f5a61476ff6057780177b610a9571b417c2c4c700821e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104419834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8dc831f4bb6b9cd97cc5de6b4cdc3e1ed5144630b8a5424d1d46895516ab9e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:58 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:40:58 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:40:58 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:40:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:40:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad04cce4ac51c398476b4cf4bf77aa6a5a031730dba4e828e1ef8d9cf034194`  
		Last Modified: Wed, 28 Jan 2026 02:41:12 GMT  
		Size: 100.8 MB (100776092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:958f5e428666fe2a843a3c43d208c3aa1f39e80053f9ca47f6f0a09c9e023b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 KB (260284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a8583f185eb8024c014ca8a7263cc33fc5cbb33e36fe30cb2b605b454a8885`

```dockerfile
```

-	Layers:
	-	`sha256:d57ac12f16182b5508155d5ba36b8be4e307a1d4dbc4b6d150d2f31d0c19cab2`  
		Last Modified: Wed, 28 Jan 2026 02:41:10 GMT  
		Size: 250.9 KB (250929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a50a84409bd1e438abbea2bf0c0fadbdf030b9329b8d4f64a6210aeb95b1e9`  
		Last Modified: Wed, 28 Jan 2026 02:41:10 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u482-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7c0e90a03eb1affca816a79875c855a0583a5f446ca1157181b0dba4d6f49cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104555030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd38ff1d2bea3ba37317896abcf21518ed4867f29aca5fa8b57933f0cd35aa74`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:41:43 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:41:43 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:41:43 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:41:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:41:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50368358d3dfe16224b20e8a3506d765775cd07f33c1ec475f9625f3f362979f`  
		Last Modified: Wed, 28 Jan 2026 02:41:57 GMT  
		Size: 100.6 MB (100562150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:97a4f6be23f2deb23d892558079e4b3738029ceff884dfe3ade3b4bd39a198de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 KB (260520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0bcd2cd87e9eab6938228cfb74db215dcf0e0c1aa5fa3b82be8a4c9773adeb`

```dockerfile
```

-	Layers:
	-	`sha256:feaf5d2adc741509665b15ecb4581129ff3e36ba3f54670287016b7289fabdb0`  
		Last Modified: Wed, 28 Jan 2026 02:41:55 GMT  
		Size: 251.1 KB (251061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:109bd6b5dddc175a7721d5fc8823d0fcef40b228502d8638db97c323827d0c11`  
		Last Modified: Wed, 28 Jan 2026 02:41:55 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json
