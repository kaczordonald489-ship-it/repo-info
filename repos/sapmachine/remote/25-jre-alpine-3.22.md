## `sapmachine:25-jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:98937ef35475b30977eff6292614dc04fa313e9723ba7947430480d8d534fa77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:25-jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:ff86fd26ba25287428c16d0a48bfc5535b47d25052d87327ea95f912c6b91d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61786983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb6d0d7690e15a75c47f81a796b98717edcee75cfbc49fa85efcfefb372ebca`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:48:05 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jre=25.0.2-r0 # buildkit
# Wed, 28 Jan 2026 03:48:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jre
# Wed, 28 Jan 2026 03:48:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36775c501a241e6f617cf794680a47db23489838006565364393d15ff4e16152`  
		Last Modified: Wed, 28 Jan 2026 03:48:17 GMT  
		Size: 58.0 MB (57982108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:63b7f8ca8c8077f40be37f6b972515b4c3aedce950b7d35ad65b46265e689cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.0 KB (442012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aadc35fcdd68c04692a2a67b1e6fdbe48c7ed871f9870649d513e79c2684ebd`

```dockerfile
```

-	Layers:
	-	`sha256:fcb7ad4bc65e02f042c6c5c3c89e5f4f9699556938d32ad88536b97fc8e3125b`  
		Last Modified: Wed, 28 Jan 2026 03:48:15 GMT  
		Size: 433.1 KB (433115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e72830f1770c90d61b245e538d36505430559be1172c973bca7690af15e0e22c`  
		Last Modified: Wed, 28 Jan 2026 03:48:15 GMT  
		Size: 8.9 KB (8897 bytes)  
		MIME: application/vnd.in-toto+json
