## `maven:3-amazoncorretto-8-alpine`

```console
$ docker pull maven@sha256:66589e4471e5f9f2a188cfe73b2ccb965d0c3f84133d1bb134234ba7453df137
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:ec657707aa8c10cc01437eb1ae2bfe1c8ff219faa6721f3973fed4d4cc70a78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116358132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce9030018a52e0e990f272e1b74bbaa4a9aae4b4f5f3cb37101f88c801ac4ab`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:43:25 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:43:25 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:43:25 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:43:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:43:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:26:45 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 28 Jan 2026 04:26:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 04:26:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:26:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:26:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 04:26:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 04:26:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 04:26:45 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 04:26:45 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 04:26:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 04:26:45 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 04:26:45 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 04:26:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 04:26:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 04:26:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6833e8b5869e0f48dfb0827fe8ce0f2ec7bc4abc9a375d40ddca18d755ab20`  
		Last Modified: Wed, 28 Jan 2026 02:43:38 GMT  
		Size: 100.8 MB (100776920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1341fb8c3468504634d750d6286d1b313ab51b98427687eb935da6e24b28541`  
		Last Modified: Wed, 28 Jan 2026 04:26:53 GMT  
		Size: 2.4 MB (2406114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bb71697bfe17e84226809e8a888374e90f1a2745e76c91f081ed187714a40f`  
		Last Modified: Wed, 28 Jan 2026 04:26:54 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee84f76532d5c15c9fdc7b78a28b652decf15a7d8a4e6bc7bf4b8288f7501091`  
		Last Modified: Wed, 28 Jan 2026 04:26:53 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913909a275e05c17d57a1630bebdff677274b2d944d1a53b7f7a0f5088c23281`  
		Last Modified: Wed, 28 Jan 2026 04:26:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:8c136c8f78f15224378cf84d4f51efd4e4ddabdc8e0c975865398d287cebb9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.6 KB (408619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f378ee1c6ef1beec64f167deb8b8f841fad722aedd100724297eddc71928d6c`

```dockerfile
```

-	Layers:
	-	`sha256:0aaa3eb5e65aa4fea4343749ba3d6b56e3296f8663219ff01377b144bdcd8783`  
		Last Modified: Wed, 28 Jan 2026 04:26:54 GMT  
		Size: 392.3 KB (392266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22668d44311612ce9750437f99f395f09c63742e6832b79e3f01d13ea0b0a129`  
		Last Modified: Wed, 28 Jan 2026 04:26:53 GMT  
		Size: 16.4 KB (16353 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:65144bcc35543cbb4d4bcf98b800dafab06253631ad54ac00cf337be5587d9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116522810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddbfe3277944fc7b64fb82af3ad44733033fad4a37e6fff94e0a0319563faee`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:44:37 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:44:37 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:44:37 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:44:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:44:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:53:12 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 28 Jan 2026 04:53:12 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 04:53:12 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:53:12 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:53:12 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 04:53:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 04:53:12 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 04:53:12 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 04:53:12 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 04:53:13 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 04:53:13 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 04:53:13 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 04:53:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 04:53:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 04:53:13 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6de2205b433b6497cae9348f3c144e29b2543b5f31a88ac9bd1041c4ca96f43`  
		Last Modified: Wed, 28 Jan 2026 02:44:51 GMT  
		Size: 100.6 MB (100563666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cb426ef2bdeaafd0fff4d363969f3f4827a8236eb77cd638a5f264c478834d`  
		Last Modified: Wed, 28 Jan 2026 04:53:20 GMT  
		Size: 2.4 MB (2448763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4c15993e7998fdb915348306105276925cc4208e55f50ba1c372c55f518075`  
		Last Modified: Wed, 28 Jan 2026 04:53:20 GMT  
		Size: 9.3 MB (9312252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1452f1256951a075630eab8933fa6958aa62d196911f24c379f971642e4efa`  
		Last Modified: Wed, 28 Jan 2026 04:53:20 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1497e6c1fe7b58acb628c773d898bbd9db125559c9dd38ecec33276cd4595966`  
		Last Modified: Wed, 28 Jan 2026 04:53:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:618af63a8e795b690479ace10cd305b8d38482e57bb5e18ff86421cf7257be6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.2 KB (408222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b7665ced802b57f0102818ade98b3c12c86ae9dd996b945f03cb7d2164ee6d`

```dockerfile
```

-	Layers:
	-	`sha256:39c7f2a8efd3819a6f56c9ccca408058803cb11238b4ea5a4b8e5e799d6960cc`  
		Last Modified: Wed, 28 Jan 2026 04:53:20 GMT  
		Size: 391.7 KB (391736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1a30eaca29595f9545f4e6d0d2bdd095db67505153d9f55bfe5db40a3546ed6`  
		Last Modified: Wed, 28 Jan 2026 04:53:20 GMT  
		Size: 16.5 KB (16486 bytes)  
		MIME: application/vnd.in-toto+json
