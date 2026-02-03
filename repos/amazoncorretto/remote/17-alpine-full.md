## `amazoncorretto:17-alpine-full`

```console
$ docker pull amazoncorretto@sha256:9e6c3ad8117166620f8617c0611c54ab4912ef5775763265367f315cf6aecfdf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:aa4556c6e18aac334bcfbc6f6e1300b9f93f0707d208e397609a3cbcc40ad438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152229362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5190df72299564f4f3ee4638f8235becd2ed5a75993c5713c16a98090dbe576`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 21:32:59 GMT
ARG version=17.0.18.9.1
# Thu, 29 Jan 2026 21:32:59 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 29 Jan 2026 21:32:59 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:32:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 29 Jan 2026 21:32:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6290ed2724dad5b9d68e62935d09eb0e1dbd86d11cc766d6d0c81d0e3a60fe`  
		Last Modified: Thu, 29 Jan 2026 21:33:15 GMT  
		Size: 148.4 MB (148367541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f895f99f2f2a6a71afea0dd0188cbdf18886a975196ac1f18f9dfd8d0ad2988f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.8 KB (593819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2db2ef11980b48248b03dbd4792651ea56c750437427e8336790b1f8a7a0f6`

```dockerfile
```

-	Layers:
	-	`sha256:d866420822277a11664819993097b61baaad9716fcfbfaeaa67c411dfb161a77`  
		Last Modified: Thu, 29 Jan 2026 21:33:12 GMT  
		Size: 583.1 KB (583137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2802ac3f16ee8e6f767ae0b9c6a2be5df39eebddd889557e5b7f5c354189772c`  
		Last Modified: Thu, 29 Jan 2026 21:33:12 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4be91a47f2abc29ed81303551ba0f4dd1c26dac99e105d741e3072abb57fb0e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150909370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ee2ab8fbf916353bafa279fc88819415fdf665d576fd3458cb5239f4739f45`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 21:32:51 GMT
ARG version=17.0.18.9.1
# Thu, 29 Jan 2026 21:32:51 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 29 Jan 2026 21:32:51 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:32:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 29 Jan 2026 21:32:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a1b2b27fdd6627a7a5ca56c15c20d0c298fbaa72189065a764f30f5dd81e08`  
		Last Modified: Thu, 29 Jan 2026 21:33:10 GMT  
		Size: 146.7 MB (146712279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:baedc6af8a071f463d9c035a61f5fbcaa417f706a6a19892acc3269f4652ba50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.8 KB (592788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70872b59ca2c24a0aecf5928685f84825acddc1343093038f1a3b3a06ad8034f`

```dockerfile
```

-	Layers:
	-	`sha256:6956bc0e1d44550ed7187a0a52a45b036f9983a45951372873bcd3178df3ae3b`  
		Last Modified: Thu, 29 Jan 2026 21:33:06 GMT  
		Size: 582.0 KB (581954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a51db0156ff14f832b0aa1847fc254abbdd8e4c98e9ced6e4c8a795d24ddbf42`  
		Last Modified: Thu, 29 Jan 2026 21:33:06 GMT  
		Size: 10.8 KB (10834 bytes)  
		MIME: application/vnd.in-toto+json
