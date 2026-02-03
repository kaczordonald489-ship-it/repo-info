## `amazoncorretto:8-alpine3.23-jre`

```console
$ docker pull amazoncorretto@sha256:6c6ae8489aedc511beae68f6bba3ff2f9898f3a52233d5769f5521dda300a235
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.23-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fc14b91e95c7ee5d7b4967ae0c7f4c30cfab9250178dc7db3769ae43b1e28c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45604820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ba78e04d8b33b0992c2d46f5119b7cca8848854a357cd194d8ad9da9d28cde`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:43:40 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:43:40 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:43:40 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:43:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56bce2f690a45bdb524a96143280e7358469f0c8bc258d741956d49843af3bc`  
		Last Modified: Wed, 28 Jan 2026 02:43:51 GMT  
		Size: 41.7 MB (41742999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.23-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f88f34ec8928951a5d557bf633406af4d08b25e3e255e991086a8f4f1a6229d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.2 KB (197159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16f9cdd3386e1e2e3061612aecc7c57ec86e7dcd5d72fa48fbac3dcdac7511f`

```dockerfile
```

-	Layers:
	-	`sha256:3b8b20b166c324213296285ebb2739cfe57a7ecc973bbf80156dc639822244c1`  
		Last Modified: Wed, 28 Jan 2026 02:43:49 GMT  
		Size: 187.8 KB (187843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94493e0a3deb0765ee00df49b15517d1c43fd2f13b313d5554975a0133f70826`  
		Last Modified: Wed, 28 Jan 2026 02:43:49 GMT  
		Size: 9.3 KB (9316 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.23-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:95b53275c6caf742eb7adadff5e57ed8de3cfd25b49070a0c37383f44f16c347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45656132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c30d68550d877642a3fd86867643a513e925bbcab67e9292678121d8689b76`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:44:55 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:44:55 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:44:55 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:44:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5896e461ef72f6e747c204fd99bcebc0f3b3dae713093de91497493aae628fb1`  
		Last Modified: Wed, 28 Jan 2026 02:45:05 GMT  
		Size: 41.5 MB (41459041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.23-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eaf75bfe2650d68662eb58e0aada0c067bfd743b860ddaa53a6876dee69289db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 KB (196745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f344eaea39627e522366e0ed0f5575a5628b053b6cbf14aa52e5dd68f58cba21`

```dockerfile
```

-	Layers:
	-	`sha256:4286191a32e070c5e57777ed197df4066d4e15536239cf72e88d7790062fb128`  
		Last Modified: Wed, 28 Jan 2026 02:45:04 GMT  
		Size: 187.3 KB (187325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:066035c47d2d7da4f65beaf24968ef0b3de6b6c16cafa42030edd41c5b75c4d0`  
		Last Modified: Wed, 28 Jan 2026 02:45:03 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.in-toto+json
