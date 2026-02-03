## `sapmachine:17-jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:f73930e8447525074800e9bbecf0b0fd6b0d33e95ae43af4721e88a06cdc0a50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:a94eff5a5f6221fc10dc9be5bdb72373f6897f1caf359fc7c80c05e11ea423aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58515031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abf846291019bae9609c681e4bda97ded93a5f587add19b1b660676f7b74cd77`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:21 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jre=17.0.18-r0 # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jre
# Wed, 28 Jan 2026 03:49:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7686c26fc7a4a594120d6a5f59840c58a68183d367afe69c385122509f4c83ce`  
		Last Modified: Wed, 28 Jan 2026 03:49:33 GMT  
		Size: 54.9 MB (54871289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:be24e9eef5fc043b29582ddc08fc59095004534de6e9cea852ff72437dbc50e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.2 KB (433208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7225287ebad830f6ede0e95334f51e392197bd94e0f03fb3f2b7c8505d770d7e`

```dockerfile
```

-	Layers:
	-	`sha256:4433db193fcea561ede7e020941fa6f7db26bf7501c63804b3f8bddf452f1950`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 426.2 KB (426248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c4e7724a8b20484e12a0af46b7afb93d1e0d4347fb88b57648cb23f4b5263e`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 7.0 KB (6960 bytes)  
		MIME: application/vnd.in-toto+json
