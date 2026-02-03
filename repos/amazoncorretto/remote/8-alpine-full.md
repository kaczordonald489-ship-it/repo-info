## `amazoncorretto:8-alpine-full`

```console
$ docker pull amazoncorretto@sha256:690417be79f4ef95f9c197b27ae1b789ac9b7175a21c2a8892618e6ef1a76c5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ff864ef816a5e3e5b9ebf34cf37df66c768e32ea9160ed7227d7c6628278f19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104638741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3eecd3db73d8a970e8228e4cf8221842da6ddbb2e3cef600a76b24ad76752a2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:43:25 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:43:25 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:43:25 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:43:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:43:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6833e8b5869e0f48dfb0827fe8ce0f2ec7bc4abc9a375d40ddca18d755ab20`  
		Last Modified: Wed, 28 Jan 2026 02:43:38 GMT  
		Size: 100.8 MB (100776920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2274d3ee0a3fe24965ab0343b039202fb420dd051a086f9bd99a972f2aba9eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 KB (261174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04bb3ddcf3b86f143a0743e7c15618dc1dd5cc7f83a17298da392b6ab951905`

```dockerfile
```

-	Layers:
	-	`sha256:ea3d84eeb5914b227890be9e03a7f468b1238696c34ca3c9623f2926c2ef8329`  
		Last Modified: Wed, 28 Jan 2026 02:43:36 GMT  
		Size: 250.5 KB (250521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ba7f4ce446fd8cdbc9939e56abcfd0dd3ddd5b346e22316724e74203c2153f7`  
		Last Modified: Wed, 28 Jan 2026 02:43:35 GMT  
		Size: 10.7 KB (10653 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:630ba569851318f6148ee7fe3daf6e9c57cdf5faf5be50546ab92c86ea56c483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104760757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae44662c24e193a440a5d06cb3bfc2eeada6e5fca5797fe86f85e2cd876935ce`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:44:37 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:44:37 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:44:37 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:44:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:44:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6de2205b433b6497cae9348f3c144e29b2543b5f31a88ac9bd1041c4ca96f43`  
		Last Modified: Wed, 28 Jan 2026 02:44:51 GMT  
		Size: 100.6 MB (100563666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cf8be14732bf1cebe26bd820fe1800eb55bfa20220bb6945dc1f98d3630c8022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 KB (260855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26817eafba622825284535533ba4b39f5e291ca9f045e4ed0392091105b4bd2b`

```dockerfile
```

-	Layers:
	-	`sha256:051d31bf3ae537a545253dad1ecf2a0c1c5eb5f3903ea49768a38755bc044645`  
		Last Modified: Wed, 28 Jan 2026 02:44:49 GMT  
		Size: 250.1 KB (250051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1485826fcac9a56231e91ab18d5130b1870cb860a890b781fbd4be356e4a55d4`  
		Last Modified: Wed, 28 Jan 2026 02:44:49 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.in-toto+json
