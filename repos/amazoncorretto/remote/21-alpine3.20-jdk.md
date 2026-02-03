## `amazoncorretto:21-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:9978d05008758d625cbff0d5355cf2af0f5de95649d83dbe68ad7d97ae6e7607
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a5d7175503b5e4526ac85d4a889853586360adfdac2bfeb7722372683a0d8a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165205984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77fd02cce3d0008cc249f1322b201bea11ba9f9bd5fa485b593b27e26d90223`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:48:46 GMT
ARG version=21.0.10.7.1
# Wed, 28 Jan 2026 02:48:46 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:48:46 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:48:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:48:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b361f814b6886f0da2cc6f6c4f46b2fadaa7dcae4177efc119f5dae490c4f2`  
		Last Modified: Wed, 28 Jan 2026 02:49:05 GMT  
		Size: 161.6 MB (161578120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:34a00fe882eca9e1898702daf13424143b3489828b289b4fe118b81cd75e629e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.9 KB (589930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee12bcd4648371da822321ca4e9f7b078afcfafd547bcfbaa46d6266ecf7232`

```dockerfile
```

-	Layers:
	-	`sha256:29328acb49075b9f09034cfedb18186bab1a3e98c6b2211deac7e34e585af48c`  
		Last Modified: Wed, 28 Jan 2026 02:49:01 GMT  
		Size: 580.6 KB (580557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9391ebda45107c4ec1e36330379c3351d95d16b72fa966ebddc615744fe09d5`  
		Last Modified: Wed, 28 Jan 2026 02:49:01 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1bf9b0f6964c20e7f9e95d2d1d33055fef876a73b28fb16122f069e679a3123f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163709475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651b3c5d0d5ec85d3b592067b498b682acb4786faa39f11d021b46512be6c8a5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:49:41 GMT
ARG version=21.0.10.7.1
# Wed, 28 Jan 2026 02:49:41 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:49:41 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:49:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:49:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b27e4cdd49cd069ea5635bb14261282663cf6fe0e5f9ce0e9ac02c352b8c22d`  
		Last Modified: Wed, 28 Jan 2026 02:50:01 GMT  
		Size: 159.6 MB (159619517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a5c5570dede8e5b0c5ed754be73a8e22564b81bf1e0f13d1f473371ebf7f0cae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 KB (589454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88972dd94d62f704b52e94d2e4e8adb5298c5b46eca1b7f8e1e8cb38236f94bc`

```dockerfile
```

-	Layers:
	-	`sha256:55c4243f7c2b0bc805bed650850a4dc71d89311e9cdcb6cc93b10268b31f3469`  
		Last Modified: Wed, 28 Jan 2026 02:49:56 GMT  
		Size: 580.0 KB (579976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7372ea496dfc9f3bd0291dd061895bd1f6d8aa4826fc6fce0a397bd8e5f9fcff`  
		Last Modified: Wed, 28 Jan 2026 02:49:56 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
