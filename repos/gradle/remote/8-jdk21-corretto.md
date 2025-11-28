## `gradle:8-jdk21-corretto`

```console
$ docker pull gradle@sha256:2e8851dd9f3b107213f355996ec2e1f2bbc6dd41502b7227f966aaae9c8d4795
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:72d7a514dc8e52a5ec112ac9ced67b1e3ac2fa0ea4010ca03aeb1c8e65579118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.6 MB (447627433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013bd46d5aad54489b4475d592692a65f44593f1540e9ac7652bbcb8175df74a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 20 Nov 2025 19:39:22 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:39:22 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:11:41 GMT
ARG version=21.0.9.11-1
# Thu, 20 Nov 2025 20:11:41 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:11:41 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:11:41 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:11:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 20 Nov 2025 21:36:26 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 21:36:26 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 21:36:26 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 21:36:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 20 Nov 2025 21:36:27 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 21:36:27 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 21:36:27 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 20 Nov 2025 21:36:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 20 Nov 2025 21:36:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 21:36:29 GMT
USER gradle
# Thu, 20 Nov 2025 21:36:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 20 Nov 2025 21:36:30 GMT
USER root
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766ae2bcb1221650d1330a870592c726c7d82833b2d2a4596f046d37e99261c8`  
		Last Modified: Thu, 20 Nov 2025 21:34:22 GMT  
		Size: 170.2 MB (170185490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae89e79fb64cb67a54dab631adedaf0bb228bd664612a27f3c64b27585349558`  
		Last Modified: Thu, 20 Nov 2025 21:37:15 GMT  
		Size: 86.0 MB (86021135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61ce80795bcd40a5b6c19b1369ef255c8fedd5aff8bb918990842fd156a9e73`  
		Last Modified: Thu, 20 Nov 2025 21:37:08 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c246f98eec287fc509c8da11539932caa8a6ff4f31cd9465833e91d7c3f25c3`  
		Last Modified: Thu, 20 Nov 2025 21:39:40 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89573a7f5df720412eef482223c70d6863af975f95ddf411c1978aa9abc69e9`  
		Last Modified: Thu, 20 Nov 2025 21:37:09 GMT  
		Size: 54.9 KB (54910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:e609dc1c386581593aa081cff0e40a054267e10b1dc67d114828288347f65025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11363136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47ea44972816efe64baa5d5b1dcd704bf4c7913d5643f885defe6c770f167fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa5c6c0eae3a2bf13094b92d7a5e308a30de7a58dcc1f8ea6e0f6a07af569efb`  
		Last Modified: Fri, 21 Nov 2025 00:20:50 GMT  
		Size: 11.3 MB (11342256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fd8a518a18cb049ed88fdd3b00b2186b73b151e4bd6065a3b2495f99454b131`  
		Last Modified: Fri, 21 Nov 2025 00:20:51 GMT  
		Size: 20.9 KB (20880 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b41e33d8bb02baa2e6f694bb0da581e19a8129eb534e79d50bcf8b801eb34031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.3 MB (444295116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14f124aea9f0de74360e88ea9b7e6926fcbfbdccc12c630f5c56bba9958f01e`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 20 Nov 2025 19:38:54 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:38:54 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:14:54 GMT
ARG version=21.0.9.11-1
# Thu, 20 Nov 2025 20:14:54 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:14:54 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:14:54 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:14:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 20 Nov 2025 21:41:32 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 21:41:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 21:41:32 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 21:41:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 20 Nov 2025 21:41:33 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 21:41:33 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 21:41:33 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 20 Nov 2025 21:41:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 20 Nov 2025 21:41:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 21:41:35 GMT
USER gradle
# Thu, 20 Nov 2025 21:41:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 20 Nov 2025 21:41:36 GMT
USER root
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3d3760161956214a91ef56a6ea274e4642a96cab84483933958bfb31c8f6c3`  
		Last Modified: Thu, 20 Nov 2025 20:23:13 GMT  
		Size: 168.4 MB (168441796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1643805bd3db5063bb7df6c425ed2b4ae1415d434d3f93a9a6c40dce5935230f`  
		Last Modified: Thu, 20 Nov 2025 21:42:24 GMT  
		Size: 85.5 MB (85527487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c981ecfbd3f1236f789c33f04e53fe520dc5035d72fd2a0241a3e779c72d4793`  
		Last Modified: Thu, 20 Nov 2025 21:42:14 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319680c66a6ed66650456f83b56673376715cdae1a77aa18f0d0b21395dd30c6`  
		Last Modified: Thu, 20 Nov 2025 22:25:23 GMT  
		Size: 137.4 MB (137395193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d714c62a514ebeb867c751294c097ae45f997bc2f10a817efe007a6f2c69b74`  
		Last Modified: Thu, 20 Nov 2025 21:42:14 GMT  
		Size: 59.5 KB (59538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:7fd9dda88897b91f10f02897ac4e3c1910096c26cccdab18cad3a71a280d064b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11362288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d11b844408d6b56066daee2862a641cf362b1450de48afd7435e6a6a4691f3`

```dockerfile
```

-	Layers:
	-	`sha256:1bffd9b67f8429c5e42a1f0a22f588824dd68bab5923f66e9d91967195979193`  
		Last Modified: Fri, 21 Nov 2025 00:21:00 GMT  
		Size: 11.3 MB (11341234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfde9c2cd2494d7f2fa5d1fe0957125900b97eeab24c23d2fa8b07edc1f440d7`  
		Last Modified: Fri, 21 Nov 2025 00:21:01 GMT  
		Size: 21.1 KB (21054 bytes)  
		MIME: application/vnd.in-toto+json
