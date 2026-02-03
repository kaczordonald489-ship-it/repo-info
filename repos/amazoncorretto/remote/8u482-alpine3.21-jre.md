## `amazoncorretto:8u482-alpine3.21-jre`

```console
$ docker pull amazoncorretto@sha256:c54b1c910dcf2e95c1577254c137f504f7c51d822d3930a90d0717748fc25c7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u482-alpine3.21-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:91be468fa22a70c7f6d80b26c99adad349693aa16d40a3d14d9738f77ba4c2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45387712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ec19c3f3c6eaef43f6ac844032a689c8e7712738af28c11c032d95beae1e9b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:41:36 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:41:36 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:41:36 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:41:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9423c2e63b810fcde874737d818a4ef23f7253921aa23ad8c0b0099673b24b7a`  
		Last Modified: Wed, 28 Jan 2026 02:41:46 GMT  
		Size: 41.7 MB (41743970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:73d6712020ede3444a4538bf8a1e683b41f3df5ba8da9f23017ea835147bac3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 KB (197376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43eebb37691422ffb082896377ab718998b65679d94a5fe540bb91898912e03d`

```dockerfile
```

-	Layers:
	-	`sha256:573a9a36b5e268b5b47457a87868f03d599a26c73e0f91ea54cd845ca7f2b786`  
		Last Modified: Wed, 28 Jan 2026 02:41:45 GMT  
		Size: 188.7 KB (188721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2896af1729d537bd2e69cee0d398517d1b19ed800ba50646ed1dea46f755cde`  
		Last Modified: Wed, 28 Jan 2026 02:41:45 GMT  
		Size: 8.7 KB (8655 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u482-alpine3.21-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8b3c45e597df7227ad2231d3013ab347defa9d1ae07f8f68602cb39531ced2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45449388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabdb3ee91839cdcc6fd1596ef6fed8ecfa76cb12ce370e552cd48c0023fef4a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:42:09 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:42:09 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:42:09 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:42:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce787cbe35d50c26b3162fe58bf9a4aa324ae841a617cebdccc982688961238e`  
		Last Modified: Wed, 28 Jan 2026 02:42:19 GMT  
		Size: 41.5 MB (41456508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0abe86f433b12f6735b3013c82f4adbe1c1e8754ccf7832075d8e378fa911336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.6 KB (197564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecee825305487c51665bed62c07630cf322ab5c38bbda85dd7de3dca0469d53`

```dockerfile
```

-	Layers:
	-	`sha256:5573600f9cd75c83b8aa7876d2be5d18fcab5a8dba63b0477e43fa05792023e8`  
		Last Modified: Wed, 28 Jan 2026 02:42:18 GMT  
		Size: 188.8 KB (188829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e6a7cf8af702ef2cd3586955fb03ba9fee287b61e77b19fddcbd71b511bcea2`  
		Last Modified: Wed, 28 Jan 2026 02:42:18 GMT  
		Size: 8.7 KB (8735 bytes)  
		MIME: application/vnd.in-toto+json
