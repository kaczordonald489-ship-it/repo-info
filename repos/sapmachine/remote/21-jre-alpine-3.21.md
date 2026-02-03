## `sapmachine:21-jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:7a5eb2206565ffda9dd218187733c387eed60b2d6070cad4ee65a2e276568683
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:7288b70beac7c5fd39ac96696590f899a1363dd9edbd4fb6acf702228429a243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64336545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bb25762d46c09c9333d54daa3a10263f79680248dcbf7446aeae0928bd752b`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:48:59 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jre=21.0.10-r0 # buildkit
# Wed, 28 Jan 2026 03:48:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jre
# Wed, 28 Jan 2026 03:48:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d372c4f5b4fdd1ac7ea7f83bcce09a158445b217ebad25fef38fd551e73d155`  
		Last Modified: Wed, 28 Jan 2026 03:49:12 GMT  
		Size: 60.7 MB (60692803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:52340bd645aa981405029565f06b5fbd7e30418ec00efbfeb03cba0885fe92a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.5 KB (434484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4c700e7293f47857a5ae0f0d78fc54d09d5aed1ce8a57fd7ca8ae9be9aba6f`

```dockerfile
```

-	Layers:
	-	`sha256:b3e11e8cfff1d92a6fb9e11638bbf281d46b1d120c60bcaeb74d51211e2b7b15`  
		Last Modified: Wed, 28 Jan 2026 03:49:10 GMT  
		Size: 427.5 KB (427524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b0d0b5551aaee8e3059accedeb6a12ff991d6d1a7205a27b071de8f44a3e5f5`  
		Last Modified: Wed, 28 Jan 2026 03:49:10 GMT  
		Size: 7.0 KB (6960 bytes)  
		MIME: application/vnd.in-toto+json
