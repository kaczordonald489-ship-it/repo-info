## `sapmachine:lts-jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:d26c78321e27e5d7fcc2d631d974da20aa3234dcf455fe78d9eb893c212d521d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:lts-jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:df89688d39b26aa6df330b0edbbc37eec4e7fe345b25483cdf540296cec63a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61491023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6da7c4f1e1292210f4e9bcd7713e93a0786cc0a692e2779eb442941feef97b9`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:48:25 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jre=25.0.2-r0 # buildkit
# Wed, 28 Jan 2026 03:48:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jre
# Wed, 28 Jan 2026 03:48:25 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ab0896d8f8b54d4a9881b9c70cd52c0abd2d156474b5fcc3f481e8f6610d13`  
		Last Modified: Wed, 28 Jan 2026 03:48:38 GMT  
		Size: 57.8 MB (57847281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f8861694728a1e3de5e3582bf15c42619e5362e5471a9292297da2ad87a8694b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.3 KB (440346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc024bba00075b8cb85841977b7997c9b66040f6505e1f0f02e7409abdb505bc`

```dockerfile
```

-	Layers:
	-	`sha256:0bb3ecb4f4c595f1f50ee488efa75771c4882b31591fe105366e486d9e8d7252`  
		Last Modified: Wed, 28 Jan 2026 03:48:36 GMT  
		Size: 432.7 KB (432733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:324d4a6d684f53c247f9f9fa5ed774455ba4ec3ad4e5c0afcf6b08bf45cb52d1`  
		Last Modified: Wed, 28 Jan 2026 03:48:36 GMT  
		Size: 7.6 KB (7613 bytes)  
		MIME: application/vnd.in-toto+json
