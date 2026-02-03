## `amazoncorretto:21-alpine3.22-jdk`

```console
$ docker pull amazoncorretto@sha256:303e53dd99567a29633e45d306157394f02c1963051bee456e4bb2d1f400bc23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:feea14919c5b2378aec4dbe707e89f814366d42edc7a2923e3f70bd64bb7f8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165397891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ace6cf0ace86f486a08df89d6a8e8af5e45a549aaed3da48807337bc487c615`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:49:47 GMT
ARG version=21.0.10.7.1
# Wed, 28 Jan 2026 02:49:47 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:49:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:49:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:49:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86372aba352b7bb4b74237437987f81b3148d589ad7c5ab0ee7b72346cd10a2c`  
		Last Modified: Wed, 28 Jan 2026 02:50:04 GMT  
		Size: 161.6 MB (161593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a349535bc98d9a42df1ef76786a92be4712cb6ec5c54d3df3bedc380c6ac69a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.4 KB (592413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13175f53cb1f0f89514701937b7164c7ce3c3b4b01e16745a93c07aa11f172f`

```dockerfile
```

-	Layers:
	-	`sha256:1ac24c9b98a39886575bf1a026a4efdd89be34456094eec68e297fd69adfcbb6`  
		Last Modified: Wed, 28 Jan 2026 02:50:01 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8d72fbc29f5f7fcf117c017a8daf55b23e01c3f13119fde5dabb7495289f27`  
		Last Modified: Wed, 28 Jan 2026 02:50:01 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f1f9e49348dcac5dabaf76ed666f7650dfa9e8bdd6efbdecacc073ef2f2fe8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163754423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9774995906ef9ef6a124c6b3e483c8f4f0dfa55269ce4a88736ee0db005224b8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:50:57 GMT
ARG version=21.0.10.7.1
# Wed, 28 Jan 2026 02:50:57 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:50:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:50:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:50:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4062e45d331572360e41429e3aff7543e42b2dff05bcf09b42ef6cbf0222cf`  
		Last Modified: Wed, 28 Jan 2026 02:51:15 GMT  
		Size: 159.6 MB (159614904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fcfa744dafea9ca9f451c9538358b9be725bb583575bb7c47855ebc43f2a7d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.9 KB (591936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c4286c23836b7ef0504072f92623f58c3d548dae2c0abda1e41be8cbe853a4`

```dockerfile
```

-	Layers:
	-	`sha256:7694ae225516d1bd0ef8a13a86f218ce85078daf235906dd493d280e7b5effa7`  
		Last Modified: Wed, 28 Jan 2026 02:51:12 GMT  
		Size: 582.5 KB (582458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3797d604bb40a3c944f1b3fe93f534367f633e76738f8cf62ea5d8693b78f6b7`  
		Last Modified: Wed, 28 Jan 2026 02:51:12 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
