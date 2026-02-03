## `maven:3-amazoncorretto-11-alpine`

```console
$ docker pull maven@sha256:d0566dd95949f039290d1a3116016f2ec482473ca83a7abef1577933ef37dc78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:433d738c6036adf522683fac04ab13160af2b39769e61cc3331fac5607f81115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159181201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1ec9fe505f963622770e841954f8cb5efb3548f2beba210c5ea6358e98ccb2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:46:21 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:46:21 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:46:21 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:46:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:46:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:26:32 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 28 Jan 2026 04:26:32 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 04:26:32 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:26:32 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:26:32 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 04:26:32 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 04:26:32 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 04:26:33 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 04:26:33 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 04:26:33 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 04:26:33 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 04:26:33 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 04:26:33 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 04:26:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 04:26:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d986d7e858d6100508f42bc906b71c57de3eadb7c1b125079ed3f059f3f83221`  
		Last Modified: Wed, 28 Jan 2026 02:46:38 GMT  
		Size: 143.6 MB (143585877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fae00589c117bacdb3668cf95ce2cb854f09c20945f24357e98c6b4a80bff5a`  
		Last Modified: Wed, 28 Jan 2026 04:26:40 GMT  
		Size: 2.4 MB (2420228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae33969029618c0515447529c37516d6e976dba6ef742f1fed45a7e136c2060`  
		Last Modified: Wed, 28 Jan 2026 04:26:40 GMT  
		Size: 9.3 MB (9312238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18376bdad276c9cccd866fe0b4e45ecc8e6a42793d2297db44fb2944fd15d81d`  
		Last Modified: Wed, 28 Jan 2026 04:26:40 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e5728a2dd32ba4a23c4c7d8e8cd93f5ae8baeaf2882aa69c354ac8089ecdcf`  
		Last Modified: Wed, 28 Jan 2026 04:26:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:2ed77924cfa3145a23a222dbe43ee298109ba91fa2d117d67dc3f207d28b9607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.9 KB (749878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c748d2835b4a4c1a55b570cc5a42e1695e8e96caab859e6aaa107e947d1405`

```dockerfile
```

-	Layers:
	-	`sha256:897aa9901b88c9be94a0c69e63f753fb6256d4eac301958ca3c9bcdc843e7ab7`  
		Last Modified: Wed, 28 Jan 2026 04:26:40 GMT  
		Size: 733.5 KB (733516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb39cca2a7faeab9379e60c7eb032301dae0f9efe435f54c4dae2f2cec4097c8`  
		Last Modified: Wed, 28 Jan 2026 04:26:40 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f07b9359c8f472cc3f05998fc231901c7368489ebaa69161601498db5923d5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157827445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae2029fb0c6acd55d9485d39d5eb207337ec8530dd5c9a2839cc89f5fc1b513`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:47:01 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:47:01 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:47:01 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:47:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:47:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:52:26 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 28 Jan 2026 04:52:31 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 04:52:31 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:52:31 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:52:31 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 04:52:31 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 04:52:31 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 04:52:31 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 04:52:31 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 04:52:31 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 04:52:31 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 04:52:31 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 04:52:31 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 04:52:31 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 04:52:31 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552dd13d8c7000c34c67e3db376e66141f2a096e4c79b9abd594731ea071a2d`  
		Last Modified: Wed, 28 Jan 2026 02:47:19 GMT  
		Size: 141.9 MB (141855734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0ad1c0f32089f5c377bb3ed7c1d2edc91753e75627172ad469b604beece845`  
		Last Modified: Wed, 28 Jan 2026 04:52:38 GMT  
		Size: 2.5 MB (2461342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e2b9873fd38b1701f40665ee4736b94bc19cad3824c1b4c96ea81aa1d128e1`  
		Last Modified: Wed, 28 Jan 2026 04:52:38 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac302f4c0f08847f5eb818576f866892d00028a079e0393b6221802151f5a83`  
		Last Modified: Wed, 28 Jan 2026 04:52:38 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783a1b3f16d518e1162f1844ae6ec27a687357d466141e498f727dc730de3402`  
		Last Modified: Wed, 28 Jan 2026 04:52:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:50859c4a4204b04a1a57d6fea337fdc8a0198b5183ca045e45183cf6b424699c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.4 KB (749405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e312ffc8349116b9ccef5450d86c6e51e6a1d19df4b0eb0cc85c7f62d2d00ffa`

```dockerfile
```

-	Layers:
	-	`sha256:0a49c1b5ce49aeed309675d878d7dcf53737e5f370c75619253937dd7318e1a9`  
		Last Modified: Wed, 28 Jan 2026 04:52:38 GMT  
		Size: 732.9 KB (732910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8b0c10cf0bb2344b80a7339d7429bda6ebb8143032c087d3685331dfbb73fe8`  
		Last Modified: Wed, 28 Jan 2026 04:52:38 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
