## `amazoncorretto:11-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:4e797c17fbbd584cddf5b724e7257f750326b3574de0515555046a327d55fe7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c3d59040ca56863d03683c9a92226d9a9bf1e729a10e636ccfad6913f8fa7ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147226633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccdf9444c18d4f3fc37757c827acc24c5c61cabb6a62cd1b1b07f22f1e4b05e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:45:21 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:45:21 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:45:21 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:45:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:45:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2732d781a6d3bb0cf7d06b3c76b875a07c2c8afeff3763810b8cb85626a7fa`  
		Last Modified: Wed, 28 Jan 2026 02:45:38 GMT  
		Size: 143.6 MB (143582891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d8eb30346be111328295dfe7b0bdd541b778569d23434244363a2744545fbd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 KB (602733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d91d594bcd3d66e3775823ebad257389e5c9b726071f50fe707d598f8a5993`

```dockerfile
```

-	Layers:
	-	`sha256:87dcbe73c5381ea14633ff632ba592dd10bc905e75aed23003f62ea5f75871cd`  
		Last Modified: Wed, 28 Jan 2026 02:45:35 GMT  
		Size: 593.4 KB (593359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f37222c39a657466205ed466d93db6e7c277d569612901918699b97787cc8fb`  
		Last Modified: Wed, 28 Jan 2026 02:45:35 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ed2d69e59aeb57e4c228688a5932619f9224d29fc1c97571dd9c220344bd3616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145840976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8a79fd6231312f8aa886da7377dacb9252276a4135269706aa4aabd98418a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:46:04 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:46:04 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:46:04 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:46:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:46:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5792be142746da8e1f5feb1d0afac898b5b1b15b1dec9b9fcff8ac56d0c1b11`  
		Last Modified: Wed, 28 Jan 2026 02:46:22 GMT  
		Size: 141.8 MB (141848096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:edaf3011813f25590e0bc5e60d92877c03637ff2330063eabadbc65f3de59449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.9 KB (602892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0cc2092ca5640db09eceee04608d6bafffdebd500a1de5d4b378349e4b5099a`

```dockerfile
```

-	Layers:
	-	`sha256:350fad1394c00b8f2caf5af323e84659f6663ba37a8193a20c45626fb358b998`  
		Last Modified: Wed, 28 Jan 2026 02:46:18 GMT  
		Size: 593.4 KB (593415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69157b0d13d62f8d424cc78c1fcf5443f26de2b8c64c096434f3281e52766698`  
		Last Modified: Wed, 28 Jan 2026 02:46:17 GMT  
		Size: 9.5 KB (9477 bytes)  
		MIME: application/vnd.in-toto+json
