## `sapmachine:21-jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:581b1cb25ae05c9ae9bc62149885ae5eb8b0f6de2e9da4d3c98b0878355bc476
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:e2b2300f5f4940119ae480c978027e742e17b81b72237313181ee4f9628948cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64626135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ee34afb48407aef695a9428b604a6ea226016822ff9610070abe35da709ac4`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:48:56 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jre=21.0.10-r0 # buildkit
# Wed, 28 Jan 2026 03:48:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jre
# Wed, 28 Jan 2026 03:48:56 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe1b209b7d67912228014ca35b80ee8ce05b0741ffc0ff584538e6b4f66690b`  
		Last Modified: Wed, 28 Jan 2026 03:49:09 GMT  
		Size: 60.8 MB (60821260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cbcae4269c3087eca2c2f5f84953726e1e8e4fa866f8feacdc45afe30bb1780c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.9 KB (434880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1400cee3a5156af98c6d5f81e232a29c631176e943ec07580c293373b88dbc37`

```dockerfile
```

-	Layers:
	-	`sha256:b272e90a0e7fa32d615f3fc8e9ed1b13658a399a4821cd680b885780b7d128d2`  
		Last Modified: Wed, 28 Jan 2026 03:49:07 GMT  
		Size: 427.3 KB (427272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bad84439a9d100abe46b9c825f800fdb0b1d4b2d54e0c2780c12ebc5a95cdf0`  
		Last Modified: Wed, 28 Jan 2026 03:49:07 GMT  
		Size: 7.6 KB (7608 bytes)  
		MIME: application/vnd.in-toto+json
