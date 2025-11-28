## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:b843ce7fa9d315d21fa1c432eb8cde875a87e190473a24bdc314ff9573fc9594
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:1919092902cb43764d7eb2c1e1b9d59dbfd7e382cab921660855c2bfa8c02e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 MB (326302940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b3ef21edb6c9f2bddae7e11f5824e1eadf84da73ce2632840e3032a6e242f2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 20 Nov 2025 19:39:22 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:39:22 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:09:52 GMT
ARG version=17.0.17.10-1
# Thu, 20 Nov 2025 20:09:52 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:09:52 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:09:52 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:09:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 20 Nov 2025 21:37:31 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 20 Nov 2025 21:37:34 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 20 Nov 2025 21:37:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 20 Nov 2025 21:37:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 20 Nov 2025 21:37:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 20 Nov 2025 21:37:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 20 Nov 2025 21:37:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 20 Nov 2025 21:37:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 20 Nov 2025 21:37:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 20 Nov 2025 21:37:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 20 Nov 2025 21:37:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 20 Nov 2025 21:37:34 GMT
ARG MAVEN_VERSION=3.9.11
# Thu, 20 Nov 2025 21:37:34 GMT
ARG USER_HOME_DIR=/root
# Thu, 20 Nov 2025 21:37:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 20 Nov 2025 21:37:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 20 Nov 2025 21:37:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a352c054111bbf2209425369e3e6faa0c692949aa92f0ccf546936dca5a1fa`  
		Last Modified: Thu, 20 Nov 2025 21:25:26 GMT  
		Size: 156.9 MB (156898397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afc0824719d871e018313ba17345005483584934cdabbc7a4bb2aebb817a055`  
		Last Modified: Thu, 20 Nov 2025 21:38:25 GMT  
		Size: 93.7 MB (93702462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55759e07d0b27009eb689005bfd6d0392ef91240f6555bd4ba7e9daac13917a4`  
		Last Modified: Thu, 20 Nov 2025 21:38:11 GMT  
		Size: 12.5 MB (12489441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f73c02672d17e5e1ea86e6169796ec83f814d355ecfd2540c0a9bfdfe1d33d0`  
		Last Modified: Thu, 20 Nov 2025 21:38:09 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7117c41a1262172f2e7738cb3c8f8b680c26e97849816d13a37207e6b88eb12`  
		Last Modified: Thu, 20 Nov 2025 21:38:08 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49da253dfba85448ffe350fb374aeea22e9caf1722113dfc8b0c440a9dc17346`  
		Last Modified: Thu, 20 Nov 2025 21:38:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:0af2956e9b926d146a3f4ed5ea632cd80d7fd9aebca15fadd2b80d937acf404a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe33e914d560a52203a7dd6e86128599e400be5a777fb262aca6f49a17fe249`

```dockerfile
```

-	Layers:
	-	`sha256:9980f898579afc721357ac8b7ee960e23b71c63ad4b7b4dae27ef28740d69d57`  
		Last Modified: Fri, 21 Nov 2025 00:27:40 GMT  
		Size: 6.2 MB (6232024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ebd2dff33bea10e39ee7c40cd9cbf58e2bb42fb204439148ddc3c99bf2f3f16`  
		Last Modified: Fri, 21 Nov 2025 00:27:41 GMT  
		Size: 18.3 KB (18285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e19db785ef1dcd850700c822e1dc42b459ef124d8c2031856cc2f8bd5968881f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323187943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1162a5ca55811e720990d6606b2ec858f14ba4b4fa2513f119eb1074f243b0d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 20 Nov 2025 19:38:54 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:38:54 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:12:47 GMT
ARG version=17.0.17.10-1
# Thu, 20 Nov 2025 20:12:47 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:12:47 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:12:47 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:12:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 20 Nov 2025 21:48:49 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 20 Nov 2025 21:48:52 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 20 Nov 2025 21:48:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 20 Nov 2025 21:48:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 20 Nov 2025 21:48:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 20 Nov 2025 21:48:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 20 Nov 2025 21:48:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 20 Nov 2025 21:48:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 20 Nov 2025 21:48:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 20 Nov 2025 21:48:52 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 20 Nov 2025 21:48:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 20 Nov 2025 21:48:52 GMT
ARG MAVEN_VERSION=3.9.11
# Thu, 20 Nov 2025 21:48:52 GMT
ARG USER_HOME_DIR=/root
# Thu, 20 Nov 2025 21:48:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 20 Nov 2025 21:48:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 20 Nov 2025 21:48:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf284244ed6b0961eb49ffe3358b8817213a3f733a7e11727a9005bc6521e65`  
		Last Modified: Thu, 20 Nov 2025 20:29:09 GMT  
		Size: 155.7 MB (155708222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af8c02ecefd45fe0b40c3b09b212e136c1a47b7f08e6432f99c9d80fb6772a0`  
		Last Modified: Thu, 20 Nov 2025 21:49:42 GMT  
		Size: 92.6 MB (92614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47087d77fee4927d7016ea9e2d4fa3eb241593712caf7bfd909dfab71d7b6dd2`  
		Last Modified: Thu, 20 Nov 2025 21:49:20 GMT  
		Size: 12.8 MB (12751978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2db5f58034ba2bcba0175853bd608537503aa8b22b5f3ddf6614a2a352bc662`  
		Last Modified: Thu, 20 Nov 2025 21:49:19 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a567a33c7cc012644547ddc3858bceb3bc1bddcbd42ee59f101354c4fe4eb2`  
		Last Modified: Thu, 20 Nov 2025 21:49:18 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d667f26b2cc2550354568217f2a4e2f90e6eb08c84d70df227152df2566ab8`  
		Last Modified: Thu, 20 Nov 2025 21:49:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:c7be7289d3c8d2d300a3b8805ee123db8cf7397f1545ca84fb17e78b2c83b748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6249386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0973a8645a5be982a1ec1c755f26e2bef84ff8ca3af7a31c5c1d52135659a6d6`

```dockerfile
```

-	Layers:
	-	`sha256:568b0d037d881ae148c7a2f05882d393b27ba3030dad2582dabfbb9b3358da62`  
		Last Modified: Fri, 21 Nov 2025 00:27:47 GMT  
		Size: 6.2 MB (6230954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f8a4a65ceb362efdbde9b935c0fd7fbf682c51bd38ca7f629e36fbabad1d8df`  
		Last Modified: Fri, 21 Nov 2025 00:27:48 GMT  
		Size: 18.4 KB (18432 bytes)  
		MIME: application/vnd.in-toto+json
