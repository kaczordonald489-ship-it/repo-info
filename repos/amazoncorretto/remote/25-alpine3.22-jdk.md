## `amazoncorretto:25-alpine3.22-jdk`

```console
$ docker pull amazoncorretto@sha256:3ffb0afccd262c33a0ae14f2fdde129eb44d18de9c4288379f9c3eeb701af5a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ebb2df6dcac6b0dfb116e3f1dcadd0cab0db23e84bee0dca3e048a0eaf5d2aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184570354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c941081ae7611c0d0dbf6904dfd80fe110596b8d113691ada3ece0f96ddb80`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:52:08 GMT
ARG version=25.0.2.10.1
# Wed, 28 Jan 2026 02:52:08 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:52:08 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:52:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:52:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7736552575071636d1881ed4344ff4ecaaafa86bb652a96dd4698654440a067`  
		Last Modified: Wed, 28 Jan 2026 02:52:28 GMT  
		Size: 180.8 MB (180765479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:20be6d4a41da066532b2065385c271ac9dbb928d7fac5e963bd02f7f3f84812d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.5 KB (601509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7e1ca6b0ac0b969190653211aa915e5c2504ad9ea039e56b25d4657c132e15`

```dockerfile
```

-	Layers:
	-	`sha256:5ce368ef2712dab417ac97028e81ffdba59a1c9e50d386243435fc69d99611b0`  
		Last Modified: Wed, 28 Jan 2026 02:52:24 GMT  
		Size: 592.1 KB (592137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de51618a9660399354eb86e128ca2c2204828ce9222e9eab6b68f0779cef6727`  
		Last Modified: Wed, 28 Jan 2026 02:52:24 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cb3b2ee367dfcfcfe22e53419ab71514d306a71d972756ef66b80811df497f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182550236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f806f28c44302c898cf40d19825f173216a985ba822a9c9501d9dc8f9089e1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:53:50 GMT
ARG version=25.0.2.10.1
# Wed, 28 Jan 2026 02:53:50 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:53:50 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:53:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:53:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263218ab86b250e3dcde1ed7655ecd26b18c58ec900bdca4cf1ad5fe4478084c`  
		Last Modified: Wed, 28 Jan 2026 02:54:10 GMT  
		Size: 178.4 MB (178410717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:24b07e4abea40cd002058b7dd5b7fd97d80ff1f47d51005f07908ad18ca19424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 KB (601029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36e19d935dd86c37e00448ba0f12e7285a239cfe2b79d45b9f031dfdd810a90`

```dockerfile
```

-	Layers:
	-	`sha256:67a4984e915c2c928d5fa6f10288fc0eeb18e037702473d0c39e12bf8a144d27`  
		Last Modified: Wed, 28 Jan 2026 02:54:07 GMT  
		Size: 591.6 KB (591553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f3838bd9ccd89bb20fb098775c39b6a380d69492d25d38000d777e4409b8a77`  
		Last Modified: Wed, 28 Jan 2026 02:54:07 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
