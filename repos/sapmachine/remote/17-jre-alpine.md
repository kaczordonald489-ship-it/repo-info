## `sapmachine:17-jre-alpine`

```console
$ docker pull sapmachine@sha256:6b0d97b04ee723430617d0a056865ef330bf1f6bea85de7f52f51a94f53fdc9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jre-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:02b61d6a2526fbb2019e8a1860bb18f8b9b947e734cc9a42a9b49bad08dae579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58808902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ff2f2555d5104afffa24b0acc84e193edbf659d39c4f00faf78de771707908`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:01 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jre=17.0.18-r0 # buildkit
# Wed, 28 Jan 2026 03:49:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jre
# Wed, 28 Jan 2026 03:49:01 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6c350aea95e3650291c286981689f2b46e682a51cf9fcd14704d0ed2560f11`  
		Last Modified: Wed, 28 Jan 2026 03:49:13 GMT  
		Size: 55.0 MB (55004027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8ef64412924f341d4dd6bbebcb82f0d77eec9162cf1073d0adaf3856f9642bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.6 KB (433606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fcb00abe6d053f23c7d3e5e52dde50c3b447943ba199075155dbf02df7c0e4`

```dockerfile
```

-	Layers:
	-	`sha256:d4a8d414a9007ab7a1b983d868d049c98628a0c9a1b1afefc2c254d6275f355c`  
		Last Modified: Wed, 28 Jan 2026 03:49:11 GMT  
		Size: 426.0 KB (425996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c9e5d1bdf1e45704fbec571c934b6d4f6adaba44726f8748e28f834ebd71e6e`  
		Last Modified: Wed, 28 Jan 2026 03:49:11 GMT  
		Size: 7.6 KB (7610 bytes)  
		MIME: application/vnd.in-toto+json
