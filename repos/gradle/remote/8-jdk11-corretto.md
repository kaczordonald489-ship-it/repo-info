## `gradle:8-jdk11-corretto`

```console
$ docker pull gradle@sha256:7b0c31922394924e3cc8cd47d43703ede6bb1bc21943d24dc32db50c2127b057
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:9b596afac54aaab63c50f46b23318b4c3f61ad7eee2d8e3ca13a247bd616bc64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430875672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9334731df214d8a91dc78b9b646ce97c66ada70719e2ea676253700ea2c3db15`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:06:57 GMT
ARG version=11.0.30.7-1
# Wed, 28 Jan 2026 04:06:57 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:06:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:06:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 28 Jan 2026 04:56:16 GMT
CMD ["gradle"]
# Wed, 28 Jan 2026 04:56:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 28 Jan 2026 04:56:16 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 28 Jan 2026 04:56:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 28 Jan 2026 04:56:16 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 28 Jan 2026 04:56:16 GMT
WORKDIR /home/gradle
# Wed, 28 Jan 2026 04:56:16 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 28 Jan 2026 04:56:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 28 Jan 2026 04:56:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 28 Jan 2026 04:56:19 GMT
USER gradle
# Wed, 28 Jan 2026 04:56:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 28 Jan 2026 04:56:19 GMT
USER root
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402caadba9faf237352f0a6218ffdc967bda733b1529ca888757943968898ade`  
		Last Modified: Wed, 28 Jan 2026 04:07:18 GMT  
		Size: 153.4 MB (153366942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44df8ff47fb445ae560b497d150324afb62071d2301090e46c23ce491228c217`  
		Last Modified: Wed, 28 Jan 2026 04:56:53 GMT  
		Size: 86.0 MB (86040036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1a735a4450f8a1306aca47e648183b51f5abe19dff82dd1fedbc95caf0b9cb`  
		Last Modified: Wed, 28 Jan 2026 04:56:49 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b636625686d50641d1f8bac357955f6402838987969abab72f55022452dbcb`  
		Last Modified: Wed, 28 Jan 2026 04:56:54 GMT  
		Size: 137.4 MB (137388270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bc9abe295daa869316d61b304e9d70e6bde6422a2e2d8feb3a5867fe79ce5a`  
		Last Modified: Wed, 28 Jan 2026 04:56:49 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:036f9fe8fcadea990653653b96f62ba0fd90f69bbc4631947ded25c427054a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40faba0f5a5423a27d3478d94c8de24a8634920b0bc56286e5204b29173c8123`

```dockerfile
```

-	Layers:
	-	`sha256:e0767f816031e5edd1fca379b886efceeddc3b60cbaebf43e7246736498e3929`  
		Last Modified: Wed, 28 Jan 2026 04:56:49 GMT  
		Size: 11.4 MB (11365982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68a14390f1e9a691a566fdc5ac1f39e7c7e43080fe3fbe97339a658d83748af7`  
		Last Modified: Wed, 28 Jan 2026 04:56:49 GMT  
		Size: 21.5 KB (21523 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a82f6a7e9db98ee376ffdc84bb1a8d00448e4a1e9d2595d4b9745eb68225c95e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.8 MB (427799173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1951c79cfadb920abc2b11c27773824d338ab66302cd2519a5bfb1ce0454f330`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:27:23 GMT
ARG version=11.0.30.7-1
# Wed, 28 Jan 2026 04:27:23 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:27:23 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:27:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 28 Jan 2026 05:38:04 GMT
CMD ["gradle"]
# Wed, 28 Jan 2026 05:38:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 28 Jan 2026 05:38:04 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 28 Jan 2026 05:38:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 28 Jan 2026 05:38:04 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 28 Jan 2026 05:38:04 GMT
WORKDIR /home/gradle
# Wed, 28 Jan 2026 05:38:04 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 28 Jan 2026 05:38:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 28 Jan 2026 05:38:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 28 Jan 2026 05:38:07 GMT
USER gradle
# Wed, 28 Jan 2026 05:38:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 28 Jan 2026 05:38:07 GMT
USER root
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e130b48db658a3d47222a6ded8a1fec4b2b4ea85450905bcd926798478f901`  
		Last Modified: Wed, 28 Jan 2026 04:27:44 GMT  
		Size: 151.9 MB (151921736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d18b7d06b0c7379a8f831622aacca95fa0dff52424f3ca100bff23ba6412dc`  
		Last Modified: Wed, 28 Jan 2026 05:38:38 GMT  
		Size: 85.5 MB (85511331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02d85ec981c054121a5b61408daa901ac1a6d42bc1c7db258ddbd4cd3fba2ad`  
		Last Modified: Wed, 28 Jan 2026 05:38:35 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204ba29c220a2d07688a697091394addf664208f6952699e4a03a8b43969403`  
		Last Modified: Wed, 28 Jan 2026 05:38:39 GMT  
		Size: 137.4 MB (137388266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f349de88c78d76443939e7ecd73a1e776ccfe3dc59aa22080f5bf2239212c74`  
		Last Modified: Wed, 28 Jan 2026 05:38:35 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:9ced897452c397c4d7b3a7da9e689a733eedd6ceab0166337994cabe19f1d259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53966b4760bc58d59a7516809f6fbd37a0e77e1a05d922389a5aeac9d1099787`

```dockerfile
```

-	Layers:
	-	`sha256:602e14f90bad3e03762228e942b13d558b7a62895cdbdb683c333153df98a6c1`  
		Last Modified: Wed, 28 Jan 2026 05:38:35 GMT  
		Size: 11.4 MB (11365825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abb53066af1c78ead9925826221689326b51e09010350019c5db09228894cda7`  
		Last Modified: Wed, 28 Jan 2026 05:38:35 GMT  
		Size: 21.7 KB (21719 bytes)  
		MIME: application/vnd.in-toto+json
