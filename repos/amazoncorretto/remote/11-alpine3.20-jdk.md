## `amazoncorretto:11-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:252441c8977b90e89f62523bf77a19d1cf5017b4812aa05e133d491b8026ab85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6b70b453484a17a2b2163e8aeeb621d8e92be9bbb1d1efac4d4c1bb8114b52a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147204214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa24388752880f1944cb2b9fd41520b5b628d8ce0ebd9223b4c775f74bc67d7e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:44:40 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:44:40 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:44:40 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:44:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:44:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ada83a3ba195182e8a9925b59ed2af14afefc96064c21366efd2587cb04d2a`  
		Last Modified: Wed, 28 Jan 2026 02:44:56 GMT  
		Size: 143.6 MB (143576350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0528bf37d94c2bf5303248c10b2ab4a4f11f98d46cb12534ffb20e161b8be15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.8 KB (596828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e070be8419e9c98f687a4a2ff6f6b670cb773a2810652435ee526063c6325ad`

```dockerfile
```

-	Layers:
	-	`sha256:525131439faae7485d5594419e8bcdbcecdbcb7fa02df7a8168f7138ece51632`  
		Last Modified: Wed, 28 Jan 2026 02:44:53 GMT  
		Size: 587.5 KB (587454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2c9a90618383730da26ecb283ec12e3462642a6a9409d5d2608e071bdafff86`  
		Last Modified: Wed, 28 Jan 2026 02:44:53 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ec66200d6a74edc7930abab50dadaa445f9fd7f00eec859f3485db5b31ea5315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145948147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4899b5a98f0c0e847c90c5a04715e98a2355e7b1c4767d8fb55aac8f892136f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:45:35 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:45:35 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:45:35 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:45:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:45:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530ca849354327e9677c412efb9aceb67885a4bab57a82e593cc9b2b3b33be07`  
		Last Modified: Wed, 28 Jan 2026 02:45:52 GMT  
		Size: 141.9 MB (141858189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:df62b05fddd5e052181c6188ab9ef2f3ec3135c1bd359343fbcc545b72970504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.0 KB (596988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6e0ab90073b0de1322f1e6ffb8f60e341721a555f4a9587a0d7099877fd036`

```dockerfile
```

-	Layers:
	-	`sha256:d69f6904de66ac00bdaf8abfcba4ac8a6b9eb314c999f7eb400dd08dabec74c4`  
		Last Modified: Wed, 28 Jan 2026 02:45:48 GMT  
		Size: 587.5 KB (587510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14fa6e19aa3aa5187347ecc397857f9543e4e4ccd23f54a106b76b376ca71b2`  
		Last Modified: Wed, 28 Jan 2026 02:45:48 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
