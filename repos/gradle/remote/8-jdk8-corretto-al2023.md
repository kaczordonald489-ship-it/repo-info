## `gradle:8-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:f6d6b610b92ae0a65db8a7935fb78df8896f2446f0f438c02fc2df39eb035bd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:f17f09587b45ce13f53bba7e8b714740c569c53da04ee4a36a2206fc9a387572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.6 MB (587635926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052cc007654ac4959edbafcdd9d770fe0033223f5bec50d35b4b80b32834bd89`
-	Default Command: `["gradle"]`

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
# Thu, 20 Nov 2025 20:47:57 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 20:47:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 20:47:57 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 20:47:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 20 Nov 2025 20:47:57 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 20:47:57 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 20:47:57 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 20 Nov 2025 20:47:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 20 Nov 2025 20:48:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 20:48:00 GMT
USER gradle
# Thu, 20 Nov 2025 20:48:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 20 Nov 2025 20:48:00 GMT
USER root
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
	-	`sha256:5f455a36ef0f126369fdfe11229b74c6180ec09c811df60700149c416d0d750c`  
		Last Modified: Thu, 20 Nov 2025 21:20:00 GMT  
		Size: 65.4 MB (65372268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fb207d24e39a896764494c689304521849e2de7941f5e3a2295d9fa5c96249`  
		Last Modified: Thu, 20 Nov 2025 21:19:43 GMT  
		Size: 1.9 KB (1942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455202a11c7542bb5e3771e9dfff74132511a25501ff30c7e50ade5b0a754965`  
		Last Modified: Thu, 20 Nov 2025 21:20:14 GMT  
		Size: 137.4 MB (137395175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb768a900ddb508b3527f100bd3b03d20ffc3590e2260387c0cca2f6815e019`  
		Last Modified: Thu, 20 Nov 2025 21:19:58 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:c6e4c3fb164a76d32898c4ce7efee8449eb50273385ca43846cce93f0d982ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18175374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f30c644b9d0d3b04d6ee4317b64a9393ec08952634f1df71132b48bf12aed1`

```dockerfile
```

-	Layers:
	-	`sha256:a4a6f5a69768daa592ce5ccbf2b364e1665fb366094ced37a7c84360f9cc6913`  
		Last Modified: Thu, 20 Nov 2025 21:22:20 GMT  
		Size: 18.2 MB (18153859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0711e1c00129232c4262dcda54aa9118c9c7375e70dbc5e9256a6f0bd0bb4f8`  
		Last Modified: Thu, 20 Nov 2025 21:22:22 GMT  
		Size: 21.5 KB (21515 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9b4432de18c1cf69942ee59256e78267d3e70647c12b7df85b96a1b78cea7996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393766809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92df94c1e7ed2d7394c7bab280f4609a3cde778c89c7802966c49efc52a5bcc`
-	Default Command: `["gradle"]`

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
# Thu, 20 Nov 2025 21:42:26 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 21:42:26 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 21:42:26 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 21:42:26 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 20 Nov 2025 21:42:26 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 21:42:26 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 21:42:26 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 20 Nov 2025 21:42:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 20 Nov 2025 21:42:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 21:42:29 GMT
USER gradle
# Thu, 20 Nov 2025 21:42:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 20 Nov 2025 21:42:30 GMT
USER root
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
	-	`sha256:d5458025f963fa1fe92c6f9bdb60d0bbf2e527dd17957ba5889791bbd30446f4`  
		Last Modified: Thu, 20 Nov 2025 21:43:28 GMT  
		Size: 85.5 MB (85514825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14205df2622033714c88859cb3335f95b8f20bbbed7ca8b2b35d6d2778d5af17`  
		Last Modified: Thu, 20 Nov 2025 21:43:21 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb8228920a5c6c508373012644d3e4132475b0509547f1c215b868eff8d61c2`  
		Last Modified: Thu, 20 Nov 2025 21:50:32 GMT  
		Size: 137.4 MB (137395194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9df58f0434fc34a80a2985fb6cc1da34b8f822b240f93724812a62696446ab`  
		Last Modified: Thu, 20 Nov 2025 21:43:21 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:96c5d8a2a95079460d9277c8e6dfe902f862186aa179c222c951f984e596f22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11739759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39dbcf5d5457ae89d98a9bf5037029845d42b356edfe691485ed006118dc95c`

```dockerfile
```

-	Layers:
	-	`sha256:9ee69974921b279d3d4dad39ac0fb3b0719bf1df5d62cd58314651d66022ab57`  
		Last Modified: Fri, 21 Nov 2025 00:21:11 GMT  
		Size: 11.7 MB (11718049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c876238abcfb4c599595c156fd34463bca3c29a848523c709bb821d6e02320e`  
		Last Modified: Fri, 21 Nov 2025 00:21:12 GMT  
		Size: 21.7 KB (21710 bytes)  
		MIME: application/vnd.in-toto+json
