## `gradle:8-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:8c516c234405fb242663a6dc3ff788f334f7a8ff0612fcdf7d18ac87025c898e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:39b2dd2073c0fc062960cc8f7f58d90672bac94dc9b90d84507408003e139fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.3 MB (434335032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c5ac73f49aa2bba8c9b80f78e582fcb1db5259a214f98b09f61d3fa56d3cc4`
-	Default Command: `["gradle"]`

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
# Thu, 20 Nov 2025 21:36:25 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 21:36:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 21:36:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 21:36:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 20 Nov 2025 21:36:25 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 21:36:25 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 21:36:25 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 20 Nov 2025 21:36:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 20 Nov 2025 21:36:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 21:36:27 GMT
USER gradle
# Thu, 20 Nov 2025 21:36:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 20 Nov 2025 21:36:28 GMT
USER root
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
	-	`sha256:7a762b1c1f683d7b96ddbd999a2c42d534b79567f5c69889928c8d068e5e0344`  
		Last Modified: Thu, 20 Nov 2025 21:37:17 GMT  
		Size: 86.0 MB (86015839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e39ca245d9ddadb30e981db5aa4c4ca9e050c5d83fddf6eac6d28938ec28ef`  
		Last Modified: Thu, 20 Nov 2025 21:37:06 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c021a124a2049ef07ab6a35a84abc0c291e80c6ccdcc0277d0d100709aece00`  
		Last Modified: Fri, 21 Nov 2025 00:32:53 GMT  
		Size: 137.4 MB (137395195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf1ce0ef26ddd55d27e532f7dda217313f5703fa255ecc21adb6ad7e0942cc7`  
		Last Modified: Thu, 20 Nov 2025 21:37:06 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:e2092d8241cdbd7bad864ed4f1b3254047f20a817d5a71ccaa675fc291d49570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11360569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f6a9fe17f16e240f29298abb97ba27526a2de5538615ea828293893d6e9dd8`

```dockerfile
```

-	Layers:
	-	`sha256:dc0997e6daec4ef2ac2180a10c910f0931bfeda753dc6cc5546161a126485daa`  
		Last Modified: Fri, 21 Nov 2025 00:20:31 GMT  
		Size: 11.3 MB (11339842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65197721607d9e17ed15f401a370e9109266c60f509e0942b2d9efb5d1b6b29a`  
		Last Modified: Fri, 21 Nov 2025 00:20:32 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c6ec4d7ef7cb3ed07b047b01ffdbc17ab88af0fc858e9dd8b8d993ce0d2d6b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.6 MB (431559868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac67ccc144b46d7169bdbea6aea090fe82c247f2dd765d3abcd8cf8b2ede18ec`
-	Default Command: `["gradle"]`

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
# Thu, 20 Nov 2025 21:41:45 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 21:41:45 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 21:41:45 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 21:41:46 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 20 Nov 2025 21:41:46 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 21:41:46 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 21:41:46 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 20 Nov 2025 21:41:46 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 20 Nov 2025 21:41:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 21:41:48 GMT
USER gradle
# Thu, 20 Nov 2025 21:41:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 20 Nov 2025 21:41:49 GMT
USER root
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
	-	`sha256:168c21c933f61b9b65e8ff1c6180e4e87d2cfb7e3c5571e8728767e623c5fc9d`  
		Last Modified: Thu, 20 Nov 2025 21:42:42 GMT  
		Size: 85.5 MB (85525820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e5b447713e0a7b27efc1617490000b5c915cc80814c35cdbda45bb747c7a19`  
		Last Modified: Thu, 20 Nov 2025 21:42:27 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2197844f1c817f5f92317c1cd96310efdb59d05240af77292def14adb3754486`  
		Last Modified: Fri, 21 Nov 2025 06:24:48 GMT  
		Size: 137.4 MB (137395194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfbf8a40598fc2c608a56fcf26b741cd922f298ea45f9a059b104f8b9a2b4fd`  
		Last Modified: Thu, 20 Nov 2025 21:42:27 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:37af2ce453e0edde40dccaae3e14b8f58e63330a13a2518eaf55c59ed819dffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11359717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224ff841437840cf234a291ac3cf5d2571223d38c471c05ded14c31bc60ed6a4`

```dockerfile
```

-	Layers:
	-	`sha256:5e7b27567f18925d07a04854d19fedc83d25c6f0d036005413c73e991f8d3826`  
		Last Modified: Fri, 21 Nov 2025 00:20:43 GMT  
		Size: 11.3 MB (11338817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:713267656dda8dffab83d104f27200927a2d444660c27ff2d5306f205432b682`  
		Last Modified: Fri, 21 Nov 2025 00:20:45 GMT  
		Size: 20.9 KB (20900 bytes)  
		MIME: application/vnd.in-toto+json
