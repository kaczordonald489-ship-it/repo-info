## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:5946397936e0bdad44046f0d7ab115db2c1f4f795199b09b90fc11a54ad57fa9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:4c4d4305ffb898f013eb3870533e9f4f6015fdcafc8ddbcb06ceae712df20108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.5 MB (332538084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58875c7c6c9c3ae3c2579c1a3db2700aa5f812cf29998a58ace01c7789bffe1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 21:32:21 GMT
ARG version=17.0.18.9-1
# Thu, 29 Jan 2026 21:32:21 GMT
ARG package_version=1
# Thu, 29 Jan 2026 21:32:21 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 29 Jan 2026 21:32:21 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:32:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 29 Jan 2026 22:12:50 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 29 Jan 2026 22:12:52 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 29 Jan 2026 22:12:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 29 Jan 2026 22:12:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 29 Jan 2026 22:12:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 29 Jan 2026 22:12:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 29 Jan 2026 22:12:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 29 Jan 2026 22:12:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 29 Jan 2026 22:12:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 29 Jan 2026 22:12:52 GMT
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
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bcfb83c2e453e939721a922013646100eb7e7c7d5c82e4ecd27e63620b69bd`  
		Last Modified: Thu, 29 Jan 2026 21:32:47 GMT  
		Size: 156.9 MB (156915770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df03161cfd7cc9df14a906742f502b7d6f9dd7a81f872cfd9d5bfdd96f2885ac`  
		Last Modified: Thu, 29 Jan 2026 22:13:11 GMT  
		Size: 99.8 MB (99788154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57acb31fdd0d9a58f9007dc3fd188abeedd894885dd891e6b72c79bf01d141bd`  
		Last Modified: Thu, 29 Jan 2026 22:13:08 GMT  
		Size: 12.5 MB (12497037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8799aca4258445f72b95cb33b0f0eb15346beffac559d0ca034a4aa50e341f9`  
		Last Modified: Thu, 29 Jan 2026 22:13:08 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d049e45af0f2bffabcfbecdb95e9c463166dfce479113d5c105db02de1dc1fb0`  
		Last Modified: Thu, 29 Jan 2026 22:13:08 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26433e119562f13d459c795523b0c5e8748b310946efde589923d622c0adf91`  
		Last Modified: Thu, 29 Jan 2026 22:13:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:f5086959c7036b791ae7f59a33351f4e9344a8d8f2d24f26405ff0c5a2e4f089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515d27dcbc0c233672d4debac5f3f37950e2cb2cb01a701b7bec9b952c0dfdc6`

```dockerfile
```

-	Layers:
	-	`sha256:bb6ba1778dff1eafc7b55623ef58dd2072f2310254d181e325d332e36ef04f20`  
		Last Modified: Thu, 29 Jan 2026 22:13:08 GMT  
		Size: 6.2 MB (6232025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79fb18a7353fc9ab4133c981e881d29f0fbb7ac6514ebee8e139b43f39c268e0`  
		Last Modified: Thu, 29 Jan 2026 22:13:08 GMT  
		Size: 18.3 KB (18285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:60e2eff3d91d1969e58b9093615eaf85be22acfd2e33ad6072babe3e72436d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.5 MB (329512361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f84cab607d282e0958e28769625d02414c9ec93abc1223a65872b6e6fbab469`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 21:32:24 GMT
ARG version=17.0.18.9-1
# Thu, 29 Jan 2026 21:32:24 GMT
ARG package_version=1
# Thu, 29 Jan 2026 21:32:24 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 29 Jan 2026 21:32:24 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:32:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 29 Jan 2026 22:12:30 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 29 Jan 2026 22:12:33 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 29 Jan 2026 22:12:33 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 29 Jan 2026 22:12:33 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 29 Jan 2026 22:12:33 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 29 Jan 2026 22:12:33 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 29 Jan 2026 22:12:33 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 29 Jan 2026 22:12:33 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 29 Jan 2026 22:12:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 29 Jan 2026 22:12:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 29 Jan 2026 22:12:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 29 Jan 2026 22:12:34 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 29 Jan 2026 22:12:34 GMT
ARG USER_HOME_DIR=/root
# Thu, 29 Jan 2026 22:12:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 29 Jan 2026 22:12:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 29 Jan 2026 22:12:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065d21b4470e9f024846f039ffce24548a54e0966b2b32586c3e1d734b91367b`  
		Last Modified: Thu, 29 Jan 2026 21:32:49 GMT  
		Size: 155.7 MB (155728159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703ac3366c09c5ffb34a5fe9f5524f521cf80febcb9bfd2445dd76a2b66dcae2`  
		Last Modified: Thu, 29 Jan 2026 22:12:54 GMT  
		Size: 98.8 MB (98795298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2cc65c0429c19d8783475048542e77565b9460d5dc17b2624bc5aa8ec47976`  
		Last Modified: Thu, 29 Jan 2026 22:12:51 GMT  
		Size: 12.8 MB (12758978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3939c6c2341a318b7e3400004c1dd76aff2570ebe37767b7d7569678e6f00`  
		Last Modified: Thu, 29 Jan 2026 22:12:51 GMT  
		Size: 9.3 MB (9312243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0558e2dd0cfdb8d2014f375672245ed5852f86dd48ba3b11b2731b0712c966c`  
		Last Modified: Thu, 29 Jan 2026 22:12:50 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ae13103470d4f52003313d6ab3db357b04e9a6e6eb839e258e9c2f3c654b61`  
		Last Modified: Thu, 29 Jan 2026 22:12:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:fc0b287dcdcfc710a4a1e1958764ab7ce6c15c09223cd769ae2bcc0dc2633c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6249388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a401672daa3652732e6fa299de62e16fe6fa07ef15b65114eb3cd67f858b7f`

```dockerfile
```

-	Layers:
	-	`sha256:376dc8a37e07a5284328a529299e00125d590acd2a5f847f1e4c2ed89ef63ca6`  
		Last Modified: Thu, 29 Jan 2026 22:12:50 GMT  
		Size: 6.2 MB (6230955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7a63220771a444abcdd067f772ff54cc13cea1a53805e509477dbb481692ec3`  
		Last Modified: Thu, 29 Jan 2026 22:12:50 GMT  
		Size: 18.4 KB (18433 bytes)  
		MIME: application/vnd.in-toto+json
