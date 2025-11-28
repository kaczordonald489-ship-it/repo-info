## `maven:3-amazoncorretto-25`

```console
$ docker pull maven@sha256:c80d6398506a1178fad0ca28ba0036cc66bdc802e613aaaf9569103fba19db26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25` - linux; amd64

```console
$ docker pull maven@sha256:50ed931dd0b2f312bc5be6ed8e0f77e014ed760e06961baeeb0581523dbd6ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.8 MB (355815099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01bae19780c745f53209366634d81d21a28fe09fe2be76f5ba507ac8ac2cbdf`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 20 Nov 2025 19:39:22 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:39:22 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:13:27 GMT
ARG version=25.0.1.9-1
# Thu, 20 Nov 2025 20:13:27 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:13:27 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:13:27 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:13:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 20 Nov 2025 21:38:35 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Thu, 20 Nov 2025 21:38:35 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 20 Nov 2025 21:38:35 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 20 Nov 2025 21:38:35 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 20 Nov 2025 21:38:35 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 20 Nov 2025 21:38:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 20 Nov 2025 21:38:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 20 Nov 2025 21:38:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 20 Nov 2025 21:38:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 20 Nov 2025 21:38:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 20 Nov 2025 21:38:35 GMT
ARG MAVEN_VERSION=3.9.11
# Thu, 20 Nov 2025 21:38:35 GMT
ARG USER_HOME_DIR=/root
# Thu, 20 Nov 2025 21:38:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 20 Nov 2025 21:38:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 20 Nov 2025 21:38:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73615f162427717bb524bb65d17f76492dd2ba484b36570400ed1948c74aa5ed`  
		Last Modified: Thu, 20 Nov 2025 21:34:24 GMT  
		Size: 189.1 MB (189136491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0091d760349eda0f148fa22bb69afedd43a0dd7ff7c6b6d9372fa7ae0bd9d5ca`  
		Last Modified: Thu, 20 Nov 2025 21:39:29 GMT  
		Size: 103.5 MB (103465967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278138afd689a089ba9d78816cf1b478302e8eb4f852cce93110c34eeb9cc4c1`  
		Last Modified: Thu, 20 Nov 2025 21:39:03 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3aa05450e3e9ac088964e07d4b9838c13fdf6d7d13303978d095bdbb2c5558`  
		Last Modified: Thu, 20 Nov 2025 21:39:03 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a461295dcd3409ca372bcc368aca7b58757839f980876808b64a4fc1e57fff`  
		Last Modified: Thu, 20 Nov 2025 21:39:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25` - unknown; unknown

```console
$ docker pull maven@sha256:24288ac05b4158d7d9f1ffb7467a2669ed14b93e7cfe2a151eb0eadd6e76ac6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6226555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a65a8068165e970e711df667eb2eb000fc10f1115024c66957ebaa806119c3a`

```dockerfile
```

-	Layers:
	-	`sha256:e950ea462e54fc7789251e362f8e410f354d1056213b8a02f4b1f3702d30c40b`  
		Last Modified: Fri, 21 Nov 2025 00:27:24 GMT  
		Size: 6.2 MB (6209006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd8b17e3473341b5a25687e16c9614c5ad5195c80cc92ebdbdb2b5c75d4427ec`  
		Last Modified: Fri, 21 Nov 2025 00:27:25 GMT  
		Size: 17.5 KB (17549 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:bed12f9a800039fceaedcdc481e071899c4990678bed241f4ed7f8a4dde9a091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.8 MB (351823543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725bc28c01f0dc8f03cb1eee1713abb3c7e66e1938770a1dd5a54bccc5721b72`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 20 Nov 2025 19:38:54 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:38:54 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:16:56 GMT
ARG version=25.0.1.9-1
# Thu, 20 Nov 2025 20:16:56 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:16:56 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:16:56 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:16:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 20 Nov 2025 21:48:47 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Thu, 20 Nov 2025 21:48:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 20 Nov 2025 21:48:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 20 Nov 2025 21:48:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 20 Nov 2025 21:48:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 20 Nov 2025 21:48:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 20 Nov 2025 21:48:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 20 Nov 2025 21:48:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 20 Nov 2025 21:48:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 20 Nov 2025 21:48:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 20 Nov 2025 21:48:48 GMT
ARG MAVEN_VERSION=3.9.11
# Thu, 20 Nov 2025 21:48:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 20 Nov 2025 21:48:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 20 Nov 2025 21:48:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 20 Nov 2025 21:48:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89032ad19d026518bda7c21ccdf4d5da20cfd0f783042990bddb410e19dc6d4d`  
		Last Modified: Thu, 20 Nov 2025 20:23:40 GMT  
		Size: 187.1 MB (187059620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603759db1886e728408c9063248d65b27dddd70947aa17c5f5823cf530e54aeb`  
		Last Modified: Thu, 20 Nov 2025 21:49:42 GMT  
		Size: 102.7 MB (102650885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ced1ec0d83ddba25c15c8c3c6e748d83465c2fb37fb85bacebc0390fc571e2d`  
		Last Modified: Thu, 20 Nov 2025 21:49:17 GMT  
		Size: 9.2 MB (9242576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918f14d64dae22e8d51eb98cd6eb6ed5850e98afdd1f07a65052e61c2de246b1`  
		Last Modified: Thu, 20 Nov 2025 21:49:16 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6244a6b8a29ba5253acf7e40de984d9eceaaacc7713a0e3765f12fe134d68f0d`  
		Last Modified: Thu, 20 Nov 2025 21:49:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25` - unknown; unknown

```console
$ docker pull maven@sha256:509b1eb842676aafab09461d33e7f3db83a08ea6dff5e932018e780c588025ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6225728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38fd768a358aa277744593b5f3a049bb5f7d9700af32b8f03a34eeed41234c67`

```dockerfile
```

-	Layers:
	-	`sha256:c843b6d46ecd3db0ea1f984c364d6fb596e06f5d8d1439cbb0d08f8a39afc611`  
		Last Modified: Fri, 21 Nov 2025 00:27:30 GMT  
		Size: 6.2 MB (6207998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5834c331527d8a5a4c2764150b1169ca1763909458ac0319fd92bc15196b8151`  
		Last Modified: Fri, 21 Nov 2025 00:27:31 GMT  
		Size: 17.7 KB (17730 bytes)  
		MIME: application/vnd.in-toto+json
