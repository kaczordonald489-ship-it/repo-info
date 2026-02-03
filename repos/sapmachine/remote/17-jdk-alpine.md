## `sapmachine:17-jdk-alpine`

```console
$ docker pull sapmachine@sha256:a185cafc899cda3d8f51127422de64227be969f1f6e658073c086254a1c445b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jdk-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:004dcb12fbdf6303c6a04f9afafc506120de63a9ff3080ed27e5df204d963964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.2 MB (206153984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de53114a3162fc263b670f77fc99794fc3a1633f0fa186e262c310f73c1bb6db`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:48:58 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jdk=17.0.18-r0 # buildkit
# Wed, 28 Jan 2026 03:48:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jdk
# Wed, 28 Jan 2026 03:48:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d1442320b814701229f0f6369d76f9575b94d91510dddf1c2eb3fcdb336015`  
		Last Modified: Wed, 28 Jan 2026 03:49:19 GMT  
		Size: 202.3 MB (202349109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f3a4845d962063f5e4944f1ef6e1cd3aa3524e98d9d4d444c8618f867eb00fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.3 KB (520265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3177100aba077dec25d7d2700763c5cf8e442b1ba131fd2cda25aa5f18c85049`

```dockerfile
```

-	Layers:
	-	`sha256:3c453b17e46ca00c5370958adf81d1eef4a935dc42250b258250c1e6afcab49f`  
		Last Modified: Wed, 28 Jan 2026 03:49:15 GMT  
		Size: 511.4 KB (511359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4fdaff7d7ea78cf769cefef196ad95e813e0989fb66d49467d52b9283c39e90`  
		Last Modified: Wed, 28 Jan 2026 03:49:15 GMT  
		Size: 8.9 KB (8906 bytes)  
		MIME: application/vnd.in-toto+json
