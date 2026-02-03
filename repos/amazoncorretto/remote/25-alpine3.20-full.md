## `amazoncorretto:25-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:007cbc80b4c6d7a7209fc84b836a9f52ab46a822ed518ce8dffd0097a2e85760
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:087b0c44c7b7376bf1cc2d3688bbc1f03c3716ae276aa972b2733658bbb870f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184379016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61e00639e690ca4f6b5f7d5fb11925b42db1b7241bb550d646470a0024aadfa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:50:57 GMT
ARG version=25.0.2.10.1
# Wed, 28 Jan 2026 02:50:57 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:50:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:50:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:50:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307d6170e04765e491324329a6097cc32161772d7bb12602a8a131b29b740948`  
		Last Modified: Wed, 28 Jan 2026 02:51:17 GMT  
		Size: 180.8 MB (180751152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:631ec6952f29fa0fde3e454757b2b5d0b9fefda1d241b3cec63b0e46c2d0fd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.0 KB (599026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b61083d683b3ec1d34d09a8ac9653068d4bfbe580a074d4891b0921165c61b`

```dockerfile
```

-	Layers:
	-	`sha256:13f25dcf239198bb1d9709b8e56b2a91392382d97905a3662f2e7c1bb04d1a7f`  
		Last Modified: Wed, 28 Jan 2026 02:51:13 GMT  
		Size: 589.7 KB (589655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9c67094018f208172a0870ddd992aa7b136c12cc5e66ff7c3850e5d7154c7b2`  
		Last Modified: Wed, 28 Jan 2026 02:51:13 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8db7498426428e375b05543c331ff0d62b23e31a34ecbf7dd8f6c161266c6243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182506310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b5d947381889a42a88a779f3fa6e844b55adf7e5316fcd157783c53760a922`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:52:05 GMT
ARG version=25.0.2.10.1
# Wed, 28 Jan 2026 02:52:05 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:52:05 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:52:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:52:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966f33a6006e3bb7f1002b5e5b12495b348fd5d390d56ee51c1c0e81779d68ce`  
		Last Modified: Wed, 28 Jan 2026 02:52:26 GMT  
		Size: 178.4 MB (178416352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b0f633c6a8a7659679086f9a77fae46c0f8bc264642309bce883a09400e5748e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.5 KB (598547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4117c0b4ba3f456d4d8866d3637af6327ac7bba170de73c18ff95f5e70d8ed4`

```dockerfile
```

-	Layers:
	-	`sha256:4d6bf03911b70923e210357f900910283fb7c95e31ea3f461b9c02f731b5260a`  
		Last Modified: Wed, 28 Jan 2026 02:52:22 GMT  
		Size: 589.1 KB (589071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbe26ce2b3651aaab7d812266f62630ad02cd484047494b58922a4fc41f24f37`  
		Last Modified: Wed, 28 Jan 2026 02:52:22 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
