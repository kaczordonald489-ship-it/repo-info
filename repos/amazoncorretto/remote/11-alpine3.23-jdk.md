## `amazoncorretto:11-alpine3.23-jdk`

```console
$ docker pull amazoncorretto@sha256:78cb024e505a61370d3f31f2634e6bf125d6511a6d7bd18691ef6a37ef30355c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.23-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:865dde956c32bba55ce0e5309eb670fc50ce75f1e64126d57cbc7cc197446572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147447698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fca4edc9487d665040f35754f4308eb96fffa20d72f2e960a48d516d0b262de`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:46:21 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:46:21 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:46:21 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:46:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:46:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d986d7e858d6100508f42bc906b71c57de3eadb7c1b125079ed3f059f3f83221`  
		Last Modified: Wed, 28 Jan 2026 02:46:38 GMT  
		Size: 143.6 MB (143585877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:72034307c503ed790b3266b8c9bfcc0770d7aa0bc7025e40f7c144d4e008f5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.6 KB (599611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048f99cc431125d5849132ee52143a8a1e4de02547d103cc78a70b31a0e3de10`

```dockerfile
```

-	Layers:
	-	`sha256:2648d7b5bb643ce264e3aa5cd359e250928ddfb92744b57ed2637fd534055ada`  
		Last Modified: Wed, 28 Jan 2026 02:46:34 GMT  
		Size: 588.9 KB (588929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c50ac0720f14cdc05848940bc58bf3163a47e025123ecbb42d7ff07d51b12f8`  
		Last Modified: Wed, 28 Jan 2026 02:46:34 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.23-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:acc56871de7e710ab6c7094dfe2bec5f924ccd3299e5ceacac30fb13fa094640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146052825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425434ce2a95501296e5eefa2889818c00bfe5aec32ebfed95310b9ac9f1aad8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:47:01 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:47:01 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:47:01 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:47:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:47:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552dd13d8c7000c34c67e3db376e66141f2a096e4c79b9abd594731ea071a2d`  
		Last Modified: Wed, 28 Jan 2026 02:47:19 GMT  
		Size: 141.9 MB (141855734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:98a2ae769e1e5b2184f504c17c08f31636251cb5acbf4a208d1b165f427fa04e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.2 KB (599217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef699def435c606a10ec2612f58ec45289f3a470386849765072be4f6ca2bdff`

```dockerfile
```

-	Layers:
	-	`sha256:b0a86f5e887a283cfe1846c043116d03bf4b94f8729e777af35551d9b5ff6b9c`  
		Last Modified: Wed, 28 Jan 2026 02:47:15 GMT  
		Size: 588.4 KB (588383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa743d7e996a49d06b53c2be99a92ae924e2643f5e28660b9c7d76120ac1a1db`  
		Last Modified: Wed, 28 Jan 2026 02:47:15 GMT  
		Size: 10.8 KB (10834 bytes)  
		MIME: application/vnd.in-toto+json
