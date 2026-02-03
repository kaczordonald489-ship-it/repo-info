## `maven:3-amazoncorretto-21-alpine`

```console
$ docker pull maven@sha256:0eb229125fe88c4552998ae3d9b6b874e5fea7d676c20a8c2277cda22080d4f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:db916c1f8e8d682d8921241eef1f8af8dc3e06c7b8128382124250f1c28afbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177185505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3c7119caf3f65b2867ad211e60169daee1eac10d315d078f25f94c2681a235`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:50:24 GMT
ARG version=21.0.10.7.1
# Wed, 28 Jan 2026 02:50:24 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:50:24 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:50:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:26:48 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 28 Jan 2026 04:26:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 04:26:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:26:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:26:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 04:26:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 04:26:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 04:26:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 04:26:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 04:26:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 04:26:48 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 04:26:48 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 04:26:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 04:26:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 04:26:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0476ba18ce4a7d863df3375a1843d00caa67c25f77311a8828c2f340ca01d1fc`  
		Last Modified: Wed, 28 Jan 2026 02:50:43 GMT  
		Size: 161.6 MB (161590292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380b3cd65c565fa364556bdbd0734c2b70af44a0aeb0f54c210be6340050748c`  
		Last Modified: Wed, 28 Jan 2026 04:26:57 GMT  
		Size: 2.4 MB (2420112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdb233a44f97b96921847e55f813a8eaa5455bd27ea09948cd1c5c112639841`  
		Last Modified: Wed, 28 Jan 2026 04:26:57 GMT  
		Size: 9.3 MB (9312243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26b91d9f7d3ef0e710654b4e18922858036fd3975580258bd9280da0a84a58d`  
		Last Modified: Wed, 28 Jan 2026 04:26:57 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92258204be0e6b57c14f0796d36a714c332372d38a8f527ec8e6e8d6294c2834`  
		Last Modified: Wed, 28 Jan 2026 04:26:57 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:6712ce5dd7149cbcca6a59a912b5557f8f59d61be6d69a5c4d19fb1a74bfa55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.0 KB (743989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7ac066247698a3c05722095d250064cad22e784fa3ec20724d141327ac99d5`

```dockerfile
```

-	Layers:
	-	`sha256:41a34be0be0b8072b948c1b9858e1d7a05ffaebc0339dd1f7f0354843af6eed9`  
		Last Modified: Wed, 28 Jan 2026 04:26:57 GMT  
		Size: 727.6 KB (727627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fe73f8cd8022c604861a0a0fc0ddca9b65ccfedc708adac5c422b8b644fce92`  
		Last Modified: Wed, 28 Jan 2026 04:26:57 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:bfc01f798db9febc1c3b79875dc7565a09a406c592a25394b9036890805be903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175587116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c296a716b4423bc04d266a8b8533a3db0587a9b2292ad0c166cd3dbd015b3430`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:51:47 GMT
ARG version=21.0.10.7.1
# Wed, 28 Jan 2026 02:51:47 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:51:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:51:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:51:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:52:49 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 28 Jan 2026 04:52:49 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 04:52:49 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:52:49 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:52:49 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 04:52:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 04:52:49 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 04:52:49 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 04:52:49 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 04:52:49 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 04:52:49 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 04:52:49 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 04:52:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 04:52:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 04:52:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429b075c73c3fb61a2595fbd83c3d77b387659de25ba9b2d1de05f9d24ee5f70`  
		Last Modified: Wed, 28 Jan 2026 02:52:06 GMT  
		Size: 159.6 MB (159615593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861fd32947bc07175251647cff721170b995234d50cf800605f4e84a84b699ab`  
		Last Modified: Wed, 28 Jan 2026 04:52:55 GMT  
		Size: 2.5 MB (2461152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8130488f70a2df6337b6da28336e3c773c8c5ce3293c7e58471dbf92839d3e3d`  
		Last Modified: Wed, 28 Jan 2026 04:52:55 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0359cda9a8505701c20da4a71d88c33437f081622e6e92d1ca74a016c84e6c7e`  
		Last Modified: Wed, 28 Jan 2026 04:52:55 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c41eea70931c77162fc3ab501a35da3185695e05df2ef3ecff3e577ee801ba`  
		Last Modified: Wed, 28 Jan 2026 04:52:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:3fe4f2d760e14439f40626e0eaea945a5bb47ada4d304f385e2b86803117a4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 KB (742879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786fdc1784d091c13426f8e898d9233bacab25d6283d0506f225abcb61e6c686`

```dockerfile
```

-	Layers:
	-	`sha256:7824c26519bfda2143b15d560bab2aceb4551f8f23412a7cb67ea077858a673e`  
		Last Modified: Wed, 28 Jan 2026 04:52:55 GMT  
		Size: 726.4 KB (726384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb093424a4254dcd40cbb2a9682221e559848e569ab084a2c378dd86cfb0505b`  
		Last Modified: Wed, 28 Jan 2026 04:52:55 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
