## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:27632048f6effca303ec6a10e420115888a1a8c6bbd2662458ea76c56a8818cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:2b538fc302bd64f14934f3eade84182449a8f9abc9a0e7157932a8267cc7d805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.5 MB (495531661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f51a38ec7ce38069f494f5c2dca884a44057c72dfb0a8fd6eaf44b35a28667`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 20 Nov 2025 19:39:22 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:39:22 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:07:52 GMT
ARG version=1.8.0_472.b08-1
# Thu, 20 Nov 2025 20:07:52 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:07:52 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:07:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 20 Nov 2025 20:56:55 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 20 Nov 2025 20:56:56 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 20 Nov 2025 20:56:56 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 20 Nov 2025 20:56:56 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 20 Nov 2025 20:56:56 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 20 Nov 2025 20:56:56 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 20 Nov 2025 20:56:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 20 Nov 2025 20:56:56 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 20 Nov 2025 20:56:56 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 20 Nov 2025 20:56:57 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 20 Nov 2025 20:56:57 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 20 Nov 2025 20:56:57 GMT
ARG MAVEN_VERSION=3.9.11
# Thu, 20 Nov 2025 20:56:57 GMT
ARG USER_HOME_DIR=/root
# Thu, 20 Nov 2025 20:56:57 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 20 Nov 2025 20:56:57 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 20 Nov 2025 20:56:57 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440656998dc34d3cb5f4c7275c666ee0b42d5e57978f27ccab5808e1818b930e`  
		Last Modified: Thu, 20 Nov 2025 20:48:10 GMT  
		Size: 330.8 MB (330842584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b3256e6300c35cb6e84acb027a8ee5904e250136570cf5e0ab0970a86d56fd`  
		Last Modified: Thu, 20 Nov 2025 20:57:57 GMT  
		Size: 96.1 MB (96060944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5b681cc6766b7e49367f90beccd052b5ef092c2488dea6ad10c03a9333e466`  
		Last Modified: Thu, 20 Nov 2025 20:57:36 GMT  
		Size: 5.4 MB (5415502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27083490ce41493bdccd3534edaa1159a1a862e9877b9e128fed697549b6a827`  
		Last Modified: Thu, 20 Nov 2025 20:57:36 GMT  
		Size: 9.2 MB (9242569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a969f7d9a3e0bae7b7fb8f367fef89a5c407b7aeb5780aa6b0e7acd85dc081f8`  
		Last Modified: Thu, 20 Nov 2025 20:57:36 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d6b2b62f9f1b8e72e4c3b7e255767f100c947cecee31e849fd26073c489060`  
		Last Modified: Thu, 20 Nov 2025 20:57:36 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:7cf8fb029f76a3ea96e97d351f3968d42c1ba04fb97f181728fe2d69d548f0bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc29e55894073c723f00250dbca1c64d4c00b15065960c1ed4629e245544387d`

```dockerfile
```

-	Layers:
	-	`sha256:b1e9bcef86358f4950ee5d74ca12ccc0147fc0ac93db2c5568af63e052bc6968`  
		Last Modified: Thu, 20 Nov 2025 21:28:13 GMT  
		Size: 13.8 MB (13828199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d45e4917f14a2ea42f8bcb201531fa16b975a06322ef2f91be79ffb13321f84`  
		Last Modified: Thu, 20 Nov 2025 21:28:14 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0bbe94911b964cf61cb4c7c637e73561d18a17a70131fe3b40f3e34351f69078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.4 MB (285381900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7cc9bce680f6e18aeae4d9a0373741d733def7bde1a34959db9d1031675f06`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 20 Nov 2025 19:38:54 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:38:54 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:10:39 GMT
ARG version=1.8.0_472.b08-1
# Thu, 20 Nov 2025 20:10:39 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:10:39 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:10:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 20 Nov 2025 21:49:42 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 20 Nov 2025 21:49:44 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 20 Nov 2025 21:49:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 20 Nov 2025 21:49:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 20 Nov 2025 21:49:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 20 Nov 2025 21:49:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 20 Nov 2025 21:49:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 20 Nov 2025 21:49:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 20 Nov 2025 21:49:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 20 Nov 2025 21:49:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 20 Nov 2025 21:49:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 20 Nov 2025 21:49:45 GMT
ARG MAVEN_VERSION=3.9.11
# Thu, 20 Nov 2025 21:49:45 GMT
ARG USER_HOME_DIR=/root
# Thu, 20 Nov 2025 21:49:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 20 Nov 2025 21:49:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 20 Nov 2025 21:49:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ca899fcc925c235a0492929d8b4d84875d2b5c2029d15b71ecc2705fde239c`  
		Last Modified: Thu, 20 Nov 2025 21:20:32 GMT  
		Size: 117.9 MB (117926158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d6c5a1ae8ef136bb2a768bbcea85611ba5e966936bd2179ab80d6c2528ba6b`  
		Last Modified: Thu, 20 Nov 2025 21:50:25 GMT  
		Size: 92.6 MB (92608749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d81891b3202f941f17eed84653863a90e86b6b1d36c0d0c20f93cbad8e51ec`  
		Last Modified: Thu, 20 Nov 2025 21:50:14 GMT  
		Size: 12.7 MB (12733957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8386805d8896f32fbb3dec9ecaed067e896858cea1b7590f4b6188d34f3882d6`  
		Last Modified: Thu, 20 Nov 2025 21:50:16 GMT  
		Size: 9.2 MB (9242571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b760cf6610273101042d4a4c28c707dc5ffba315d241277212bb40143c7477ff`  
		Last Modified: Thu, 20 Nov 2025 21:50:16 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b2f68ce43e99b2874820bb652b8b0d6a3150bfe6da4c246fb1ab9c2b31ef6f`  
		Last Modified: Thu, 20 Nov 2025 21:50:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:5265f23d642f9680e73d8bcbee7a855a58b1fa2162c4bf308bd979c0e395a481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838bbecb68777400ef01fae13a219dba5568597caf07bd1d8807904115bf4f47`

```dockerfile
```

-	Layers:
	-	`sha256:8dfb29594a3f7fd666fb5ddf9337f06814a6528c1429141ab9f031db53a5dd5b`  
		Last Modified: Fri, 21 Nov 2025 00:28:19 GMT  
		Size: 6.6 MB (6609530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b99d5e707410156b5b399098a0c8b45b3f598b7652e7c77cc24927b8bbade32`  
		Last Modified: Fri, 21 Nov 2025 00:28:20 GMT  
		Size: 18.4 KB (18428 bytes)  
		MIME: application/vnd.in-toto+json
