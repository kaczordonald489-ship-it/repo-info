## `amazoncorretto:8u482-alpine3.22-jre`

```console
$ docker pull amazoncorretto@sha256:5f7ec538a707e3c9db0869e489d406600c321575ec00bf34f9dbebeb0f54cdd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u482-alpine3.22-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6e6d48c99af777f63b38544d4a9e81579cefa23787e69064cbc92152b68cfbc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45548755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10085b19b6a85d7bd71b24cacb5956e744542972a5f28636a05bf5d64425c94`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:42:45 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:42:45 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:42:45 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4383c58d345813c60f4ad6279df8eea400bc064d924c6689891e9be91fa853`  
		Last Modified: Wed, 28 Jan 2026 02:42:55 GMT  
		Size: 41.7 MB (41743880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.22-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:62e5b7b5107283cc07ddf5cc4464f32a733254aeb727a4434e78c1a9282133a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 KB (197146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7248f814db4adb2ea0e14a9b2ab5d7dce58eea430d9b92f13cf6404e7cf802`

```dockerfile
```

-	Layers:
	-	`sha256:68beee2432678265c83ca5c96eb68d325a10583c7fe14ddd09dc25c13e6865a2`  
		Last Modified: Wed, 28 Jan 2026 02:42:54 GMT  
		Size: 188.5 KB (188490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e0112d386124264a618bc1da16c9ce7764cb6df4d377a10279e9f919db8b51a`  
		Last Modified: Wed, 28 Jan 2026 02:42:54 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u482-alpine3.22-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c89dffc7488d8ea76003ec4c227d6eae3eade1b3cef001cb7e95a74eb97f8108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45597702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb45841fab9959e32a7ea43333a5ec301a2198337171eb4de6b7763400e3afad`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:43:31 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:43:31 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:43:31 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:43:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d90df31545855eec34d0debee24a43ebd2edb86117c743db1ce8f11946580d`  
		Last Modified: Wed, 28 Jan 2026 02:43:41 GMT  
		Size: 41.5 MB (41458183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.22-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b9bc74c330a3e7eb7900a93bbda8090f812399015250a7a7119b01c7ec1ed89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 KB (197334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a2d3feabb59ef64c1711a4f4f89abf8f5941470a4c6c257c52d744536fa3a5`

```dockerfile
```

-	Layers:
	-	`sha256:facb167d18eb2dda30f44d0489e527d95384c7faa4d5c80b199eaf9381383a8f`  
		Last Modified: Wed, 28 Jan 2026 02:43:40 GMT  
		Size: 188.6 KB (188598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a0221c91627bad1346128e471bdbe5af9971b341df6c0e6bd4d194c80b6fdf6`  
		Last Modified: Wed, 28 Jan 2026 02:43:40 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.in-toto+json
