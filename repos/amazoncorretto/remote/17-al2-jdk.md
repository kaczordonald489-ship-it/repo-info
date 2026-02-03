## `amazoncorretto:17-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:0f903a0da1ff5dc3dc94c0704f123b7f15bb09c66469ac449111cb9490281938
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8c1b64afcf49c7cff3b0380d6df3fe585a8d8daa6a1745dd6aabc59c35ed19a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215424934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed128685f10c95805174af783209abddf301abde57d858fa5bb43733aea2a96`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 21:31:57 GMT
ARG version=17.0.18.9-1
# Thu, 29 Jan 2026 21:31:57 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 29 Jan 2026 21:31:57 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:31:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8326e4bb78b88f1d188237c6144a0f1f66da758b1b6fc8d8639c42d704a4202`  
		Last Modified: Thu, 29 Jan 2026 21:32:18 GMT  
		Size: 152.5 MB (152461225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3c8309c50dcc637b61f00ea5257c599c733155e192f43778960ebfea56c50a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13899542c1455c8f4dbe1632ce7cb3f2a15555978c0a0afc770ce44d6e83ad3`

```dockerfile
```

-	Layers:
	-	`sha256:f86428187ff8fdb6f7e9075346881a24af4a123e3730d7801846ce7cc8833cd7`  
		Last Modified: Thu, 29 Jan 2026 21:32:15 GMT  
		Size: 5.5 MB (5535704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c956511538350e38c1e1cc6ba19bebeeddf6d6f4e518e5f004aecd5df9c6053`  
		Last Modified: Thu, 29 Jan 2026 21:32:15 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:06e79dc8caea0c452b109329fde2c2165266ff3c6e59a1e82cdc3a317d7db30f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215779256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004f736fe961d985e0d079b3b27fb1824572d9f637dd84b273718acced7c915d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:05 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 21:33:05 GMT
ARG version=17.0.18.9-1
# Thu, 29 Jan 2026 21:33:05 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 29 Jan 2026 21:33:05 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:33:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ee4d8a45ac6dbdf61b0ee55fe6f15b35ac70940c33ec3b405fba90deb89a65`  
		Last Modified: Thu, 29 Jan 2026 21:33:27 GMT  
		Size: 151.0 MB (150980367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:669843174137c3b82537652c6f6e57d48974e7ac07d610837bca0aeff6fbced9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1644755c0c54936bd534270737e4192ab5e6583a7b05218d8456f3847a29f4`

```dockerfile
```

-	Layers:
	-	`sha256:d48613644249fbcf61f295f03b899ad0f8585befa65254e4255da79daca4a1fd`  
		Last Modified: Thu, 29 Jan 2026 21:33:24 GMT  
		Size: 5.5 MB (5534393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:515a6b337d9cef3143300c0747335777b549ed97cf2f259791492fc6cd33a8fe`  
		Last Modified: Thu, 29 Jan 2026 21:33:24 GMT  
		Size: 11.4 KB (11364 bytes)  
		MIME: application/vnd.in-toto+json
