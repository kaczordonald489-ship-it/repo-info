## `amazoncorretto:25-alpine-full`

```console
$ docker pull amazoncorretto@sha256:afb37b0939cf8e627e7a18569b661cd3470611e65639d128f7a709d65615482e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c20b42e7f7ddca31cec1f7c72f69f771e941253d1812b3f065c9d3d0a8a2aea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184621110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc3ccf703effdf9f798547fbc1d95dfb3b4db0896c32557eda228e31b14ae74`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:52:59 GMT
ARG version=25.0.2.10.1
# Wed, 28 Jan 2026 02:52:59 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:52:59 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:52:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:52:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce024e0c1fc281f3f61f3cf3a1e72dcd0c8f1a01d7b36ccd799f9d0d0de6c041`  
		Last Modified: Wed, 28 Jan 2026 02:53:20 GMT  
		Size: 180.8 MB (180759289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:83f8b889c6eac116004788a41ae274df9760cca74dd3d990709c75cc85c5399a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.8 KB (602814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459def8437806487585d0f721d3eadc0c8f5d24d0f0f7b0db8df26548d24babc`

```dockerfile
```

-	Layers:
	-	`sha256:f51030d32bec29592c094e88edd4e7d6b718ec2bc68137242922f62a7fb69733`  
		Last Modified: Wed, 28 Jan 2026 02:53:16 GMT  
		Size: 592.1 KB (592136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c8becfde8dddef8d841f4959ba8657cc9747f2eec30f49a57d31200109f31bb`  
		Last Modified: Wed, 28 Jan 2026 02:53:16 GMT  
		Size: 10.7 KB (10678 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1c7a3b38665d2ab136e75d34cb68ac1840806ac4b875e58a4963f343e683cb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182609351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b0674eadbdcd0c39415cba28bbabe222b61efe68ff24238e740f08eae50b6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:54:31 GMT
ARG version=25.0.2.10.1
# Wed, 28 Jan 2026 02:54:31 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:54:31 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:54:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:54:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea00285b52f6f6c9e088cd08bc54a41499c353ac64712efcaf2aff682f021f1a`  
		Last Modified: Wed, 28 Jan 2026 02:54:52 GMT  
		Size: 178.4 MB (178412260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:13429c87918d4a024b1788b23a6da2262e04ca833d237c1a8ce76559ff054538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.8 KB (601780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41feef8ec8f729072d975ca5d05911b02a936ed45877795d44a2748ad534ea6f`

```dockerfile
```

-	Layers:
	-	`sha256:af9b424a4812a6c5940d5596e34f2c61476368ae3331fa46678bfce11e3fd024`  
		Last Modified: Wed, 28 Jan 2026 02:54:48 GMT  
		Size: 591.0 KB (590950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f74c2ee69b616e4c93d7ad5cc327bf56dca41086c5c4bb465108e7477034d47d`  
		Last Modified: Wed, 28 Jan 2026 02:54:48 GMT  
		Size: 10.8 KB (10830 bytes)  
		MIME: application/vnd.in-toto+json
