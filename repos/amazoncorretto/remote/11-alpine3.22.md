## `amazoncorretto:11-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:a7b06fa48f33ac343f9144823f1314f21eba51fcca5df18111e6bcfb87b1d6b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.22` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:beae1c75d05e6c7fc410bdcf194b793c0a7cf3c16333e81db54b9d8951c3c8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147394627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bafbcd7967e582b7888943b5defed30650488b4ea6f85f717c00bd706f1d1ae1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:45:54 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:45:54 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:45:54 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:45:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:45:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8837d612de9dcbdbac2596daec96b61b87a34ec893f8c6ff685184af55bf82`  
		Last Modified: Wed, 28 Jan 2026 02:46:12 GMT  
		Size: 143.6 MB (143589752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6684ad900cd1f8745dcad62b9ef62c818498eb5380d00bd55eb520ce0ff8246a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.3 KB (598301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0eaeb820964e32626e05135516237acdc9006b22c918a27056306dac1f5f9f6`

```dockerfile
```

-	Layers:
	-	`sha256:ed6f9973c2a163ac32502fd9cd40c9fc87d0ddfbdae7a3f6955a8ffb9cad7840`  
		Last Modified: Wed, 28 Jan 2026 02:46:08 GMT  
		Size: 588.9 KB (588928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89783e3b7619f5a74e45087804609673c8349cd4f67880c81be27e0384f1577f`  
		Last Modified: Wed, 28 Jan 2026 02:46:08 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1d081ab94747073b00e39a971500ed95130c3141aa223ceee636d77f48468180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (145993910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e60d36c20caebc4dda8609cc296fd0610b67f5a5731470b060e12621e062331`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:46:23 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:46:23 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:46:23 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:46:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:46:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893ff2fceb40633df4836121e2da8e236f5e40e10441271df8e1d8d9e649bc56`  
		Last Modified: Wed, 28 Jan 2026 02:46:40 GMT  
		Size: 141.9 MB (141854391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:901c6e6aa7836275d371eb119cc2384e3d2e3299ed075db8024bd78b2c19e43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.5 KB (598461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51867f3afe97ad9e655f50ed863079d2ae33446339ac6cdff3e3e1ac9fbe5de4`

```dockerfile
```

-	Layers:
	-	`sha256:a3b4f14d4cfbc2c390a40f411c001dc9a5711de38226536ce31ff0b8b61f7b11`  
		Last Modified: Wed, 28 Jan 2026 02:46:37 GMT  
		Size: 589.0 KB (588984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a3f296aa19cb70daf45bde2ba5a838b185fbd4bd435448e2bb991324540f3ee`  
		Last Modified: Wed, 28 Jan 2026 02:46:37 GMT  
		Size: 9.5 KB (9477 bytes)  
		MIME: application/vnd.in-toto+json
