## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:41e4aae5f24b99fc0351110d128081b652fa1685ed0909c2e1365f6244e671eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:670a4d9fdeef79d036f7ec34051bd9e97e6d6d379b7800b58e9f9ba61f5309a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211094865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fe21b317a32f4b85a9d5e03a0bc8fe1e07e2000ae37ef58d1d32b3ec24dcda`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:06:40 GMT
ARG version=11.0.30.7-1
# Wed, 28 Jan 2026 04:06:40 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 28 Jan 2026 04:06:40 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:06:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340cef2339d12ec141de515488553d7e4c289a0b47b24df9b035a69e2a865b72`  
		Last Modified: Wed, 28 Jan 2026 04:07:00 GMT  
		Size: 148.1 MB (148131156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b9570564517483553b5af7abc6545f30241eb31c77be6f23212a4702590e37f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff2ce922b8424d6b408318c2c8ebddbe9cc765346d657c2e39fe93590146529`

```dockerfile
```

-	Layers:
	-	`sha256:cb983adb86c6fa84ba5e825643f1a3f07831d3e2ac48bac765ab4f7cbbe0e81e`  
		Last Modified: Wed, 28 Jan 2026 04:06:56 GMT  
		Size: 5.5 MB (5543009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:715ef3cd9b8eb7d6cb469e9c458390733db06de451c30a7f6a9db137924adda2`  
		Last Modified: Wed, 28 Jan 2026 04:06:56 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c2de9938bc52454ba7dfeb14dcd17489d17eb291756f0c436914f41f308f95eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210023116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42dbd780636356d6980459884e2a730849c0ee2703bb22bb54d9e8fb179cb83`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:05 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:27:08 GMT
ARG version=11.0.30.7-1
# Wed, 28 Jan 2026 04:27:08 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 28 Jan 2026 04:27:08 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:27:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c848e8ff28e37232003d119f3814367e3bd0c965552f4ce08dfd6f5d55ede073`  
		Last Modified: Wed, 28 Jan 2026 04:27:29 GMT  
		Size: 145.2 MB (145224227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:06b9b5d6e2376dd632c6bbf19bc9bc405997a8c6c138fa089e6ed8d6d9ae5ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12191902928711d806efcc2a4f7b007c0d6acdd558854e95dd1e602741aff968`

```dockerfile
```

-	Layers:
	-	`sha256:786f3067db96fee80a3c8646b13f8b059479e51c3c6117d23c476ae9df1607a6`  
		Last Modified: Wed, 28 Jan 2026 04:27:25 GMT  
		Size: 5.5 MB (5542503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ab15fff7f344dacaa69d181756224f216cb6caaad6054fd80231e768327fefb`  
		Last Modified: Wed, 28 Jan 2026 04:27:25 GMT  
		Size: 11.4 KB (11363 bytes)  
		MIME: application/vnd.in-toto+json
