## `maven:3-amazoncorretto-17-alpine`

```console
$ docker pull maven@sha256:e95c1f513f8fcd63faee872aabc9b67ef9d6c361419621f12baf4d469350e684
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:6603718c305bcedde2c05da92761f5f14e38b643d8be259cd09b7c056db5fc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163962691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707d3a8581e05cbad346041e4a5350b4c220606466ef743755b7c14a814b1b3b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 21:32:59 GMT
ARG version=17.0.18.9.1
# Thu, 29 Jan 2026 21:32:59 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 29 Jan 2026 21:32:59 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:32:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 29 Jan 2026 21:32:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 29 Jan 2026 22:12:47 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Thu, 29 Jan 2026 22:12:53 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 29 Jan 2026 22:12:53 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 29 Jan 2026 22:12:53 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 29 Jan 2026 22:12:53 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 29 Jan 2026 22:12:53 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 29 Jan 2026 22:12:53 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 29 Jan 2026 22:12:53 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 29 Jan 2026 22:12:53 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 29 Jan 2026 22:12:53 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 29 Jan 2026 22:12:53 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 29 Jan 2026 22:12:53 GMT
ARG USER_HOME_DIR=/root
# Thu, 29 Jan 2026 22:12:53 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 29 Jan 2026 22:12:53 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 29 Jan 2026 22:12:53 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6290ed2724dad5b9d68e62935d09eb0e1dbd86d11cc766d6d0c81d0e3a60fe`  
		Last Modified: Thu, 29 Jan 2026 21:33:15 GMT  
		Size: 148.4 MB (148367541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc9df1d0d8a78a70b4c4af0dca19bcb307d67e430b28fc0282d8d527e4c0b97`  
		Last Modified: Thu, 29 Jan 2026 22:13:00 GMT  
		Size: 2.4 MB (2420050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e35f931dddcdb20af83377a9729181f18e179a130176969ad9508d3e6a0d77`  
		Last Modified: Thu, 29 Jan 2026 22:13:00 GMT  
		Size: 9.3 MB (9312243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467a5f74aa9aae7ceb46ca2d0d6a490ee50534194d618842a3973c027048deba`  
		Last Modified: Thu, 29 Jan 2026 22:12:59 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ca60a5e7b5e6745a450dceed596e9d0352805be1de63554527bb9d335d8617`  
		Last Modified: Thu, 29 Jan 2026 22:12:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:9ea959b14d3555aa16fe9ded01722cb48ffda124a639e3816d93d15dae4959ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.1 KB (744086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10da69d939a66459bf43c77344aa24d4194d9791adb6f66fa01db2da59f82bb`

```dockerfile
```

-	Layers:
	-	`sha256:bd8b970e6afaf8f97acc921cf8d2f17b740a0c4c91e912a46efb5f566192df92`  
		Last Modified: Thu, 29 Jan 2026 22:12:59 GMT  
		Size: 727.7 KB (727724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d577c7a44f5c2bb076daeda568aa439626cc88d8c1722e45e00a29558ac1a65`  
		Last Modified: Thu, 29 Jan 2026 22:12:59 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3315e592d4ece3cf2c3c00e7807a097cb8c25fd6ba346cbdc723df2b61f1c27a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162683753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f93add8313cb3e6a36f2de2bb325dbb6e703c348803bb803fe55452ed69e3e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 21:32:51 GMT
ARG version=17.0.18.9.1
# Thu, 29 Jan 2026 21:32:51 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 29 Jan 2026 21:32:51 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:32:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 29 Jan 2026 21:32:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 29 Jan 2026 22:12:17 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Thu, 29 Jan 2026 22:12:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 29 Jan 2026 22:12:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 29 Jan 2026 22:12:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 29 Jan 2026 22:12:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 29 Jan 2026 22:12:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 29 Jan 2026 22:12:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 29 Jan 2026 22:12:22 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 29 Jan 2026 22:12:22 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 29 Jan 2026 22:12:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 29 Jan 2026 22:12:22 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 29 Jan 2026 22:12:22 GMT
ARG USER_HOME_DIR=/root
# Thu, 29 Jan 2026 22:12:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 29 Jan 2026 22:12:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 29 Jan 2026 22:12:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a1b2b27fdd6627a7a5ca56c15c20d0c298fbaa72189065a764f30f5dd81e08`  
		Last Modified: Thu, 29 Jan 2026 21:33:10 GMT  
		Size: 146.7 MB (146712279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8527b20612f78b1fcb47c3576b857155de5e23e6432cc33ebeaa29c90e9955`  
		Last Modified: Thu, 29 Jan 2026 22:12:28 GMT  
		Size: 2.5 MB (2461104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2525d0dbea464c2198382bb14e96fcdc2d519dc2da7a3285930e59a0d4c67de0`  
		Last Modified: Thu, 29 Jan 2026 22:12:29 GMT  
		Size: 9.3 MB (9312243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b825af9cb8c4a4f6b22633255b12c30e6ddc45a8ebdfb62455bc82f344766a93`  
		Last Modified: Thu, 29 Jan 2026 22:12:28 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb47cace738b9ea1fb02750917fce3b6ceb8b72895254c5137cd4f2aafcde178`  
		Last Modified: Thu, 29 Jan 2026 22:12:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:e8b954fde20ed3aff3b1a78efd162ef27b3ac30093c121b582c6f52e40102b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **743.0 KB (742976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c1eb24cadb343479cc854746dda0ffb034c705fb92eab68a094f1f6c02e1a4`

```dockerfile
```

-	Layers:
	-	`sha256:16ad7d24a8000ad54bf353c1882f64c034621848d63a41a552cdc6cbf84599fd`  
		Last Modified: Thu, 29 Jan 2026 22:12:28 GMT  
		Size: 726.5 KB (726481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca3350476124ef0def0f9fcf6d4f8ae702f825eca5fed7e079cca188241e0be`  
		Last Modified: Thu, 29 Jan 2026 22:12:28 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
