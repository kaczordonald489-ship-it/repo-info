## `gradle:6-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:7665e16aba7fa4950e607f1fcbb8399161f0cb3cb054f7960f2e1874816ccb33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:a9ab106e30feb0a646301f9e8abef81097379dcae22a0e512c6bdaaa588c7acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.3 MB (558311651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f1700017d7832fb88d3c06b632df32500bfbccb69b3d5fba54792a716eb9e2`
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
# Thu, 20 Nov 2025 20:48:56 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 20:48:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 20:48:56 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 20:48:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 20 Nov 2025 20:48:56 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 20:48:56 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 20:48:56 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 20 Nov 2025 20:48:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 20 Nov 2025 20:48:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 20:48:58 GMT
USER gradle
# Thu, 20 Nov 2025 20:48:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 20 Nov 2025 20:48:59 GMT
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
	-	`sha256:eb2f4967ea0599a75c65402520472800ac4496333181cc9a9bae3c204b88d7f7`  
		Last Modified: Thu, 20 Nov 2025 21:05:41 GMT  
		Size: 65.4 MB (65370133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a7525d55ca6498a304cd0e50c5e888246ecfc7b98d01eb52af895c4460679`  
		Last Modified: Thu, 20 Nov 2025 21:05:04 GMT  
		Size: 1.9 KB (1942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6844a3b2d65973a7141d18ff60dc51c3cb1d78fa5e9f365770be475e13d1b975`  
		Last Modified: Thu, 20 Nov 2025 21:05:19 GMT  
		Size: 107.7 MB (107696664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70b9b88d21bef472d93a5d6cc8e3b0940cd2e99ae9a019155276778d861dc97`  
		Last Modified: Thu, 20 Nov 2025 21:05:31 GMT  
		Size: 431.3 KB (431275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:c5f4c745ec3ef224509d2dc19def3af11c5ec96c7baa695cb4de110e5d918055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18066807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3345515c14161ac3323c5785488f41aa0bff5717e791e3da7a8227f3c7e70b`

```dockerfile
```

-	Layers:
	-	`sha256:a2db26bbd4c8650b8278bcf962959605aed5f8a90f577566fe57f7068d2b36d8`  
		Last Modified: Thu, 20 Nov 2025 21:19:32 GMT  
		Size: 18.0 MB (18045942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cf3ad80c8a95fb68751ae542e7e5edc4e07ca4cdd83b11987426f526677b7d2`  
		Last Modified: Thu, 20 Nov 2025 21:19:33 GMT  
		Size: 20.9 KB (20865 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0c2708bc75038b37e1f95fc94d445db3a70449bf9004a3b9d17fe8da8b8c57df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.4 MB (364433994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728f583865ffe0ddf3e66779d41bd10a382b9cf2f34b6ca713acb23fef53b52b`
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
# Thu, 20 Nov 2025 21:43:42 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 21:43:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 21:43:42 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 21:43:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 20 Nov 2025 21:43:42 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 21:43:42 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 21:43:42 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 20 Nov 2025 21:43:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 20 Nov 2025 21:43:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 21:43:44 GMT
USER gradle
# Thu, 20 Nov 2025 21:43:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 20 Nov 2025 21:43:44 GMT
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
	-	`sha256:e9f3b370ba417411eb81272554535fab9faf7bb36f0bd6b87f879e5498e25929`  
		Last Modified: Thu, 20 Nov 2025 21:44:46 GMT  
		Size: 85.5 MB (85515054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad221892c4fd7418ec15c379a47290f666b8c9b7d033e7aa3914e912ef2ae70`  
		Last Modified: Thu, 20 Nov 2025 21:44:35 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea98f60d0daf3bb138b1372e5aafd39a98a728d89b2f761cdb3bb71785f3338`  
		Last Modified: Thu, 20 Nov 2025 21:44:56 GMT  
		Size: 107.7 MB (107696665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b6bf980717d190e807069d6e5fa4d4ee6d97779e2a11dd73accb98c2bbb365`  
		Last Modified: Thu, 20 Nov 2025 21:44:35 GMT  
		Size: 425.0 KB (425020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:adee325b823ca31e8ecf5b880f743de9a43da679e4227c9db7fce7f39b018d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11631146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551012e9b5069c0b5ed38bc398bd407e98bc9dc40a76d42b99ec66bbc6667557`

```dockerfile
```

-	Layers:
	-	`sha256:d2e0d5e058617e4b1ff50a6d73e20d62600721d91d4b86f3ea21b8e2e73acf30`  
		Last Modified: Fri, 21 Nov 2025 00:17:46 GMT  
		Size: 11.6 MB (11610108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c0e0dfd903d247ffab8af209e78fd5b0e3e133432cbce2058f68dc3afb1fd80`  
		Last Modified: Fri, 21 Nov 2025 00:17:47 GMT  
		Size: 21.0 KB (21038 bytes)  
		MIME: application/vnd.in-toto+json
