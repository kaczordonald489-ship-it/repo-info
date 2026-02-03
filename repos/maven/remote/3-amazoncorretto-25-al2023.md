## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:b8de39689884cb8beed5c8cf828a3bbdeb1d2b0e7310fea58cf3bba5d40f7054
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:166b189cb13256c13b775d2a7c5999589976d784c940787d9257cfba1132f953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362088514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6699372feccdd2b1157f4d26c1f1900109ae48ce86a6ef49d6b44c58dfdb9b6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:10:02 GMT
ARG version=25.0.2.10-1
# Wed, 28 Jan 2026 04:10:02 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:10:02 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:10:02 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:10:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 28 Jan 2026 05:35:46 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Wed, 28 Jan 2026 05:35:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 05:35:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 05:35:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 05:35:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 05:35:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 05:35:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 05:35:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 05:35:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 05:35:47 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 05:35:47 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 05:35:47 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 05:35:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 05:35:47 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 05:35:47 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cb6fcb38396d39f54d43d1b722399b74f95aea87f5b449eac9d4eac383e396`  
		Last Modified: Wed, 28 Jan 2026 04:10:25 GMT  
		Size: 189.2 MB (189191028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae5e78464970371f5f29939b6a6735d8dd58bab0c03fe9c24a17ee11f128832`  
		Last Modified: Wed, 28 Jan 2026 05:36:04 GMT  
		Size: 109.6 MB (109560364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4736c58be23756be24dd65da869454e33d86300f6683aa4d41e4170b247184f2`  
		Last Modified: Wed, 28 Jan 2026 05:36:02 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f34f4b76a1766750f1f091d6cdb89071a6608abcad5b3a2cf41f746bbf1ea9`  
		Last Modified: Wed, 28 Jan 2026 05:36:01 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149b09fbf85a8965118e3521ed85b4e910841c8b64c0357104a16d5787ca0b2a`  
		Last Modified: Wed, 28 Jan 2026 05:36:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:ee2703d161fa70a1ebdf5bb587ec27ecf5a3defd01bccaec60af77c668c2c1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4e2cc678fc864598c3e7bcadf6a5641b44ba2c310dd49bd50cb64fbe72a41c`

```dockerfile
```

-	Layers:
	-	`sha256:804829970bd514f3a00ae3fb0ae9169d4966141f6af3729c1b3444eb8ad7f690`  
		Last Modified: Wed, 28 Jan 2026 05:36:02 GMT  
		Size: 6.2 MB (6207795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa6e4525071c2feade8052ccf0f4cea389af27edb2e0f966960bcd8422dc3f8`  
		Last Modified: Wed, 28 Jan 2026 05:36:01 GMT  
		Size: 16.4 KB (16350 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5a556340e699fa8304a2756364bb3960a1b53c7d662e566f3f75374f4d20f9f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.2 MB (358162970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b699c4a55c6759e37a3bc9dd0ddcef0b4ae45aee0df52556d6f387a015f083`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:31:03 GMT
ARG version=25.0.2.10-1
# Wed, 28 Jan 2026 04:31:03 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:31:03 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:31:03 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:31:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 28 Jan 2026 05:42:01 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Wed, 28 Jan 2026 05:42:01 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 05:42:01 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 05:42:01 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 05:42:01 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 05:42:01 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 05:42:01 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 05:42:02 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 05:42:02 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 05:42:02 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 05:42:02 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 05:42:02 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 05:42:02 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 05:42:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 05:42:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a396e73c665f4fa119c9cd20fbfa42ece312688cd9297587073bc7d229c333b4`  
		Last Modified: Wed, 28 Jan 2026 04:31:30 GMT  
		Size: 187.1 MB (187090861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d7a10398524d1e864ea0bc2254a2febd5bc3730c0b48c611a28d4cba37c93c`  
		Last Modified: Wed, 28 Jan 2026 05:42:20 GMT  
		Size: 108.8 MB (108842174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c246cfa865151ba2f51d21f6af8f0e87b384c9880c997320d879d8ff88a305f`  
		Last Modified: Wed, 28 Jan 2026 05:42:18 GMT  
		Size: 9.3 MB (9312252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5fe6ca60ec5d16163605ff14d77f36a37760349eada75d3b805e614d97e004`  
		Last Modified: Wed, 28 Jan 2026 05:42:17 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8737539af421331c3918fab4877fb40384271afe94658d59fedb0f5feccbb00b`  
		Last Modified: Wed, 28 Jan 2026 05:42:17 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:87bb6f68f8274c890b0d558307e3807f2108c577a8a9f3b4e2ac5f87667d38e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac55ea1ae9a86ab560987871048ee035769829324008b88dd643300f79ba2d3`

```dockerfile
```

-	Layers:
	-	`sha256:9c23c99d4d42fa9b210ccebfb6928c48640a0d520f350ee8200071d65025ba1c`  
		Last Modified: Wed, 28 Jan 2026 05:42:17 GMT  
		Size: 6.2 MB (6206739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a3e8e89eaa7b20b01dc71876745dfb41afad0b2528ce6a785b8462d1cc9089`  
		Last Modified: Wed, 28 Jan 2026 05:42:17 GMT  
		Size: 16.5 KB (16483 bytes)  
		MIME: application/vnd.in-toto+json
