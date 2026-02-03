## `amazoncorretto:8-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:e4e3c677b426c44208f711c21549e5d1a7b079f7006aa9f5f8ab34d2286ec9f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:befdcd236ad5d5e699344644080305c7bb2014f9069ded52ee439182afc0b8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104402724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68c41c38696d11f883eff1970913412d5f4bf1d0f7a04ef86d7227e232e4a84`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:39:49 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:39:49 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:39:49 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:39:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:39:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7874207ab763900d913e9c255284f79e444c83a98e9bd7ded9c44b9713d37a22`  
		Last Modified: Wed, 28 Jan 2026 02:40:03 GMT  
		Size: 100.8 MB (100774860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ef869cd0ed5a2bc236eef7d9e3972f7cd8c958312964bcbf1f93e62be781685e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 KB (254380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d31896e04d6a02b6ec888c115b4f858368eea922ea739bf7a6503e9b7048d2`

```dockerfile
```

-	Layers:
	-	`sha256:3c5a54ad7718fb617115917c86aacd9ead7cf66f055d80bcb9ea362d9a5d4917`  
		Last Modified: Wed, 28 Jan 2026 02:40:00 GMT  
		Size: 245.0 KB (245026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9523450b0fcbf3a9fbec59c0defd18517600d31175ee9a821723c8ff0306c8`  
		Last Modified: Wed, 28 Jan 2026 02:40:00 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:061696b611fc89d6e52a556fff69fe8d50099a5d80ca70774c32031a5ead3fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104650860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750daeb943c0ec305691ea14d9f23caf638956da3cc913048da7e80a3c315b1a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:20 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:40:20 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:40:20 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:40:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:40:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ba33c15abc20177bcddbdace242e84005ae88da6286c6063a36041b2ed852d`  
		Last Modified: Wed, 28 Jan 2026 02:40:34 GMT  
		Size: 100.6 MB (100560902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:217c74d0b26e2120189fe7c5a68978eff530d2607229d565187dfb30ba0edfa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 KB (254617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7018c363456e1730063fb4ad0a64e92284a9d0a06403ee754635f9fc54b22b53`

```dockerfile
```

-	Layers:
	-	`sha256:0ffdc164b88cd557136a863c48577dd8555dfc2072e199e70401fc22388f75c6`  
		Last Modified: Wed, 28 Jan 2026 02:40:31 GMT  
		Size: 245.2 KB (245158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f152a8345b960534a9dfb93ceaad0124330b359defc69a15741f8ad4d0e325e5`  
		Last Modified: Wed, 28 Jan 2026 02:40:31 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json
