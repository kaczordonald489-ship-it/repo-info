## `sapmachine:25-jdk-alpine-3.21`

```console
$ docker pull sapmachine@sha256:e69cb1b04414939fa0f98c7c1506e2c77904639784266703929acf711f1f8a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:25-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:00b00224b4810289f9f7074d7f38ef8540e9a201d0025aea53f611c4aa68e25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226257735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4830117143c2f3080dc9ea0d15fe23964ea86fa98e9d5f897a761e41494db0a8`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:48:30 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jdk=25.0.2-r0 # buildkit
# Wed, 28 Jan 2026 03:48:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jdk
# Wed, 28 Jan 2026 03:48:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243d3763db1dc5fa422d1d5885b6c14f09be478dbc7b46f5db416eb0914adf90`  
		Last Modified: Wed, 28 Jan 2026 03:48:51 GMT  
		Size: 222.6 MB (222613993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ebffbc327a38d9cb65419ddb86319eed2cd1ce4017a52042710cf456aeeba729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.2 KB (514245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d89c29c2a61810315588fb72f0c5a3a792c7d8cfd166ee1292eb62c1567685`

```dockerfile
```

-	Layers:
	-	`sha256:e0c7cb6ad77a504aba4eaf5512555b29b17096d0c904942722e17b5585ba6733`  
		Last Modified: Wed, 28 Jan 2026 03:48:47 GMT  
		Size: 505.3 KB (505335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e1949eaed1b622666e4358b894a6b8ca2dec4d4f62a3a676e5e4672d76cc1d1`  
		Last Modified: Wed, 28 Jan 2026 03:48:47 GMT  
		Size: 8.9 KB (8910 bytes)  
		MIME: application/vnd.in-toto+json
